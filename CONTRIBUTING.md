`.github/workflows/unittest.yml`

Runs a workflow that is designed to execute a unit test and then sets a commit status `Unittest`on the commit.

The intention is that the workflow runs unconditional on all commits and you can then create a ruleset, that expects this commit status to be `success`, in order to me merged onto `main`.

The workflow also supports a manual run, where you can force it to re-run and and bypass the test and force the commit status to `success` . This is obviously not recommended, but for emergency purpose also not entirely impossible.

The workflow will issue a clear warning on the run if the commit status is set through bypassing the tests.