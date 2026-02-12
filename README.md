# test-myst-quarto-gfm
Testing repo for rendering Quarto documents as GitHub-Flavored Markdown (GFM) and as a MyST document.

# How to test

## Create and Activate the Conda Environment

Navigate into the root directory of the repository:

```console
cd test-myst-quarto-gfm
```

## Render the Provided Quarto doc as Markdown (GitHub Flavored)

The quarto document in this repo is copied from Chapter 6 of [JP Gannon](https://jpgannon.github.io/)'s [hydroinformatics](https://water-content-portal.cuahsi.io/hydroinformatics/) course taught at Virginia Tech.

You can render the Quarto document in a few ways:
- In Positron: Click the "Preview" button to render the document and see a preview in the "Viewer" Pane (this is probably easiest)
- In RStudio: Click the Render button 
- Or, go to the terminal and type `quarto render 06-Get-Format-Plot-hydrodata_COMPLETE.qmd`

This will generate a file called `06-Get-Format-Plot-hydrodata_COMPLETE.md` in the root directory.

Create the environment using the provided `environment.yml` file, which is configured with the necessary libraries for building and hosting the book. The environment's name is `test-myst-quarto-gfm`:

```console
conda env create --file environment.yml
```

Activate the newly created environment:

```console
conda activate test-myst-quarto-gfm
```

You will know the environment is active when your command prompt starts with the environment name.

## Serve the Book

You can now start the local development server and build the book in `jupyter book` (which uses MyST-markdown as a rendering engine):

```console
 jupyter-book start 
 ```
 
 You will then be able to view the book in the web browser (e.g., http://localhost:3000/).



