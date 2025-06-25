# Remora Documentation

This repository contains the documentation, both guides and .NET API docs, for Remora projects.

## Contribution

To get started with contribution, follow the steps below:

1. Fork this repository.
1. `git clone` your fork with the `--recurse-submodules` parameter
1. Navigate to `templates/discordfx/discordfx/` and rename `toc.html.tmlp` to `toc.html.primary.tmpl`

HINT: If you forgot to use the `--recurse-submodules` argument, you can run the following command to import submodules.:
```sh
git submodule update --init --recursive
```

After this is complete, you may follow the instructions below to add additional documentation.

### Adding a project

1. Under /docs, create a new directory with the name of the Remora project. We'll use Remora.MyProject for this guide.
1. Under /docs/Remora.MyProject, create a new file called toc.yml. This will be the toc file for all pages under this section. Add the following code:
```yml
items:
- name: Remora.MyProject
  href: index.md
```
3. Under /docs/Remora.MyProject, create a new file called index.md. This will be the index page for the library.
1. Open the git terminal to the project root `documentation/`
1. Run the following command: `git submodule add https://github.com/Remora/Remora.MyProject.git src/Remora.MyProject`
1. Navigate to the `src/` folder and update the toc.yml line. Add the following entry:
```yml
- name: Remora.MyProject
  href: Remora.MyProject/remora.myproject.yml
```

### Updating the API docs for a project

1. Open the git console.
1. Navigate to the submodule directory: `cd src/Remora.MyProject`
1. Pull the changes repo: `git pull origin main`
1. Go back to the root directory: `cd ../..`
1. Commit the changes.
```sh
git add src/Remora.MyProject
git commit -m "Update Remora.MyProject api documentation"
git push
```
