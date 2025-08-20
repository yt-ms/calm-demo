# CALM demo walkthrough script

## Initially running VSCode

* From working directoy, run `code .`.
* Check extensions are installed.
* Make sure logged into GitHub Copilot.
* Switch to agent mode, and preferably Claude Sonnet 4 or newer.
* Install and start up the tools from `mcp.json`.


## Demo steps

### Create a simple CALM model for a three-tier app

```prompt
In the models folder, please create me a CALM file representing a very simple hypothetical three-tier web application.  You can make any assumptions needed.
```

This should create a new `.json` file with the CALM model in there, and **also** the agent should automatically run the `calm validate` command (via a tool) to check that it's correct - potentially fixing any errors.


### Visualise it

```prompt
Now can you visualise that as C4 using PlantUML?
```

This should create `.puml` files in the `plantuml` folder.  You should be able to open one up in VSCode and use `Alt-d` to show the preview render.


### Architecture documentation

```prompt
How about generating me documentation for this architecture?
```
This has generated the `website` folder, with the docs in `docs`.

> [!WARNING]
> Hack needed currently - rename `website/src/remark-replace-links.js` as `.mjs`, and update the import in `docusaurus.config.js` to have this file extension.

* If not done before, install the doc site with `npm i --prefix ./website`.
* Start up the docusaurus server with `flox start service docusaurus` or `npm start --prefix ./website`
* Launch a browser and go to `http://localhost:3000` and you can see some skeleton documentation based on the model.



