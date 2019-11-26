Download and modify the Doc
===========================

This documentation relies on [MkDocs](https://www.mkdocs.org/) to create a nice looking website from a minimal [Markdown](https://daringfireball.net/projects/markdown/) document.

This tutorial will take you through the process of cloning the documentation on your computer, building the website from the source, and adding your own courses and ressources.

## Download and build the documentation locally

This first step is to download the documentation from its [github page](https://github.com/deepnetteam/formation)

```bash
$ git clone https://github.com/deepnetteam/formation.git
```

Then, we need to install mkdocs itself. You can follow the [official documentation](https://www.mkdocs.org/#installation), but we'll supply you with a couple of commands if you're feeling lazy:

```bash
$ cd formation
$ sudo apt install python3.7
$ sudo -H pip3 install --upgrade --user pip virtualenv
$ virtualenv -p python3.7 .env
$ . .env/bin/activate
(.env) $ pip install -r requirements.txt
```
Don't hesitate to check out our [Python installation course](installs/python.md) for more information about virtual environments.

We can now properly build the documentation:
```bash
(.env) $ mkdocs build --clean --site-dir _build/html --config-file mkdocs.yml 
```

Done ! You can now open the home page, located in `_build/html/index.html` locally, with your favorite web browser.

## Add your contribution
Let's start by creating a markdown file in the `docs` folder. You can create as many subfolders as necessary, as it will not impact the final website.

Once this is done, you should add it to the website hierarchy by completing the `mkdocs.yml` file.

To check if everything comes out as you thought, you can build the website and check it directly.

## Sharing your contribution
Once you are satisfied with your contribution, you can push it to the repo. For that part, you may need some kind of autorization from the depo manager.

Everything else is automatic, [Read the Docs](https://readthedocs.org/) will build and deploy the website !