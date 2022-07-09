# CLI Docs

Perfect! if you are here it means you want to learn more about our cli, of course then it will be done, but to follow the steps below i need you to [install our CLI](/docs/cli/install) first. After that we can proceed with the steps.

## Steps

- [new](#new)
- [contribution](/docs/contribution)

### New

the new subcommand is for the dt cli to generate something, this is a new thing. a great example is when you want to generate a "new" project from a template and you use the new subcommand. See below the structure of the new command:

```sh
USAGE:
    dt new [OPTIONS]

OPTIONS:
    -h, --help                        Print help information
    -t, --template <template_name>    Generate files/folders from a template
```

#### Template Options

The template option is for using a template, basically you pass the exact name of a template, you can see more about templates [here](/docs/templates). But basically the name of the template you put right in front of the `--template` or `-t` will be fetched from our [template list](/templates) and then we will take the whole template file structure and recreate it in the directory where the CLI was called. right after that we will execute the commands configured in the template, in case you don't understand much, I suggest you access the [templates documentation](/docs/templates)

Example of using a template:

```sh
dt new -t node-mvc
```
