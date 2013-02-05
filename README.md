# flagship-llc/git-hooks

Common Git hooks that Flagship, LLC uses. Hooks are language- or project- dependent.

## Mixing and Matching

For example, you have a PHP project that uses Compass. You would concatenate the appropriate tests to make sure that both PHP files and CSS files are validated.

## TO DO

These are things that would be nice, and I probably should do in the near future:

* Automatic concatenator / installer
	* A tool to install these hooks into your project, doing all the mixing and matching for you.
* JavaScript syntax validation

## Project Types

### PHP (General)

* `pre-commit`: uses `php -l` to syntax check your PHP files before commit. Commit will be **aborted** if there is invalid PHP syntax.

### PHP (WordPress + SCSS)

* `pre-commit`: uses `php -l` to syntax check your PHP files before commit. Commit will be **aborted** if there is invalid PHP syntax.
* `pre-commit`: uses `scss -c` to syntax check the main SCSS file (should be named `style.css.scss`)

### Compass

* `pre-commit`: Uses `scss --compass -c` to check all stylesheets in the `sass` directory. Will only check if changed.