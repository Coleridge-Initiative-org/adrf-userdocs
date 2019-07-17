# ADRF User Documentation

### How to update live site
Pushing commits to the `master` branch will automatically update https://adrf.readthedocs.io

### How to build and view locally
**Prerequisite Installs**  
`pip install sphinx`  
`pip install sphinx_rtd_theme`

**Build**  
`cd docs`
`make html`

**View**  
Open `_build/html/index.html` in a browser.

**If you don't see what you'd expect**
Run `make clean`, then `make html`. This will completely empty and rebuild the `_build` directory.
