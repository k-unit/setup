# setup

A `repo` repository for managing the `kunit` multi-project.

To install repo:

  **$ curl https://storage.googleapis.com/git-repo-downloads/repo > ~/bin/repo<br>
  $ chmod a+x ~/bin/repo**

To setup the `kunit` project follow these simple steps:
 1. Create your *kunit root directory* and from within it issue:<br>
    `repo init -u https://github.com/k-unit/setup`<br>
 2. Update the project by issuing:<br>
    `repo sync`
 3. By default the versions checked out as defined in the repo manifest don't have a name and are called *no_branch*.<br>
    It is good pratice (though not mandatory) to set a branch name in all repositories in the project by issuing:<br>
    `repo start <branch_name> --all`<br>
    Where *branch_name* is to be the name of the local branch on each of the projet's git repositories.
 4. Finalize the project setup by running `./env/setup.sh` from project root. This completes project environment setup and you can now build and run it.<br>
    Use `./env/setup.sh --help` to see the script's usage options.<br>

Use `make --help` in the project root to see the available build options.

