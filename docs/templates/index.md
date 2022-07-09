# Template Docs

Templates are a combination of folders, files and commands, for example, a command that will create a js file that when run displays the message "Hello World" would have the following structure:

```sh
.
├── dev-template.json
└── structure
    └── index.js
```

```json
// dev-template.json
{
  "name": "hello-world",
  "description": "this template displays the message \"Hello world\" in the console as a simple greeting as this is the first official template.",
  "commands": []
}
```

```javascript
// structure/index.js
console.log("Hello World");
```

All non-empty files and folders inside the `structure` folder (the name of this folder can be customized, when publishing a template you can choose the folder in the "Select folder" field) will be downloaded in the root directory from where the user starts the project . example: Joe opened his terminal and navigated to the "hello" folder and there he typed `dt new -t Hello-World` everything inside the `structure` folder will be downloaded to the folder where he is currently, in the bag a "hello" folder. something similar to this is `git clone`.

The `dev-template.json` file is a configuration file, where you can add everything you need to configure your template. Example: you want to create a template called "hello-world" just put the `"name": "hello-world"` and it will be done, this will be the name of your template. See below the fields that are currently allowed:

```json
{
  "name": "string", // the name of the template
  "description": "string", // the description of the template
  "commands": [ // this commands will be executed after the structure folder be cloned into the base folder. will be executed in same folder that all files and folders of structure are
  "string",
  ],
  "version": "1.0", // the version of the template
}
```

That's basically it, and with this information you already know everything about templates, and you can even make your own templates, how about learning how to publish your own template? lets go!

## My own template

First create a folder with the name of your template (this name must be unique, that is, there cannot be any template with the same name), example:

```sh
mkdir my-own-template
cd my-own-template
```

Now create a configuration file, the filename can be anything, just make sure it has the `.json` extension

```sh
touch my-own-configuration.json
```

Inside that file add the settings based on what was said above about template settings. example:

```json
{
  "name": "my-own-template",
  "description": "my own template",
  "commands": ["yarn"]
}
```

Now create a folder where your project's base structure will be, a folder that was explained above. example:

```sh
mkdir my-own-base
```

Inside there add all your code, for example let's create an api in nodejs, so inside I can just create an api, example:

```sh
.
├── node_modules
├── package.json
├── server.js
└── yarn.lock
```

Now create a [repository on github and push](https://docs.github.com/en/get-started/using-git/pushing-commits-to-a-remote-repository) your template for that repository. Example: all `my-own-template` folder... Example of repository: [https://github.com/dtemplate/Hello-World](https://github.com/dtemplate/Hello-World)

now you need to create an account on the site [https://dtemplate.org](https://dtemplate.org) with a github account that has access to the repository you created see an example:

![create a new account](https://ik.imagekit.io/Theryston/create-account-dtemplate-org_jRQsvWNtu.gif)

Now just go to "templates" in the menu, then in "Publish a template" select your repository in the field "Select a repository" then select the base folder in the field "Select Folder" (in this example the folder `my-own-base`) and the configuration file in the field "select a configuration file" (in this example the file `my-own-configuration.json`) and click the publish button. example:

![publish a template](https://ik.imagekit.io/Theryston/publish-a-template-dtemplate-org_MpoCcCi-Z.gif)

Then that's it! now you have a template ready and published, just send the link to your friends and everyone will benefit (including you) with the agility and productivity that the templates provide.
