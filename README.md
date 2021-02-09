# trafikode

---

🍴: Forked from <https://github.com/securisec/code-traefikode>. I had some issues with the original plugin so I created this fork mainly to comment out or remove some code.

Todo:

- [ ]: Provide documentation on various commands when using `gh` (not sure what the non-vim name for this command is).
- [ ]: Syntax highlight variable names differently. The thing is, Traefik var names are positional, not syntactical. This means it should be fairly easy to devise some hardcoded highlighting rules based on a string between two periods after some prefix.
- [ ]: Highlight the string `traffic` as an error. I have been bitten by this one before... speaking of which, I really wish they had named the project something other than a misspelling of a common word.

Initial readme follows.

---

Simple [Traefik](https://docs.traefik.io/routing/providers/docker/) snippets and autocomplete for VS Code.

Supports Traefik **version 2.1+**

## Work in progress

**Help Needed** Please refer to the TODO section for help required.

## Usage

- [VSCode Marketplace](https://marketplace.visualstudio.com/items?itemName=securisec.traefikode)
- The autocompleter will trigger when a `-` is followed by `--`, i.e cli options
- A `-` followed by the word traefik

## Intellisense

#### Caveat

The Red Hat yaml plugin disables intellisense in docker compose files, so for intellisense to work, make sure to disable it in VSCode extensions. This yaml plugin on the other hand is used in the `traefik.yaml` file for dynamic config yaml intellisense. Pull requests are welcome to fix this.

Intellisense works for the following:

- Cli and provider arguments that are passed to traefik cli
- Traefik labels for a container.
- Provide intellisense in `traeik.yaml` files for dynamic configuration.

<p align="center">
    <img src="https://github.com/securisec/code-traefikode/raw/master/resources/%20cli.gif" width="65%">
</p>

## Snippets

Snippets are provided for traefik labels for a container.

<p align="center">
    <img src="https://github.com/securisec/code-traefikode/raw/master/resources/snippet.gif" width="65%">
</p>

## Known issues

- Does not work when the Redhat yaml extension is installed
