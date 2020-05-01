# brainhack-proceedings.github.io/docs
This is the documentation of the Brainhack proceedings publishing platform. The most recent version of the docs is published on [brainhack-proceedings.github.io/docs](https://brainhack-proceedings.github.io/docs). The docs are built using the [sphinx](http://www.sphinx-doc.org!) library. Content is mostly composed of markdown files (with a few .rst) located in `source`, and the website itself is located in `build` (after compilation, not included in this repo). All `source` changes on the master branch will automatically update the website, through integration with [readthedocs](https://readthedocs.org/). To test updates to the website locally, clone or download this repository, install the dependencies (python3) using:
```
pip install -r requirements.txt
```

and then type
```
make html
```
which will update the content inside `build`. Note that some changes (e.g. change in the table of content) require to delete the content of `build` before compiling in order to get a clean build.

Here is an overview of the content files, which are located inside the `source` folder:
  * `index.rst`: this describes the documents to include in the documentation, as a list of files. For example, the line `REVIEWERS` means that `REVIEWERS.md` will be included (it is not necessary to add the extension).
  * `<FILE>.md`: a section of the documentation, in markdown format. For example `REVIEWERS.md`. This content needs to be listed in `index.rst` in order to be included in the documentation. It is not automatically detected.
  * `img`: this folder contains images. It can be referenced as `img/my_img.png` in the docs.
