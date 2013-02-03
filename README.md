# flagship-llc/git-hooks

Common Git hooks that Flagship, LLC uses. Hooks are language- or project- dependent.

## Project Types

### PHP (General)

* `pre-commit`: uses `php -l` to syntax check your PHP files before commit. Commit will be **aborted** if there is invalid PHP syntax.
