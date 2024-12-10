# Hugo sass/scss subfolders reload bug repository

This repository is a minimal reproduction of a bug in Hugo when using sass/scss in assets/styles/subfolders.

The bug was introduced in Hugo [0.123.0](https://github.com/gohugoio/hugo/releases/tag/v0.123.0).

When chaning styles in a subfolder of `assets/styles`, the live server does not reload the changes.

If we change a file that triggers a reload correctly, the changes in the subfolder will be reflected.

## Steps to reproduce

1. Clone this repository
2. Run `hugo server`
3. Open `http://localhost:1313/` in your browser
4. Change the `background-color` in assets/styles/components/_container.scss. The change will not be reflected in the browser.
5. Change the `background-color` in assets/styles/_typography.scss. Hot reload will work as expected.
