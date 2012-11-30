This `prepare-commit-msg` Git hook may be used for automatic generation of commit message for a SugarCRM bug fix.

How it works:

1. Determines bug number from current branch name. The branch name must look like _bugXXXXX_, where _XXXXX_ is a bug number.
2. Uses [sugarcrm-soap-client](http://github.com/morozov/sugarcrm-soap-client) to create commit message based on bug number.
3. That's it.

What should I do to make it working?

1. Setup [sugarcrm-soap-client](http://github.com/morozov/sugarcrm-soap-client).
2. Add path to `ssc` to the `PATH` environment variable.
3. Make sure that `prepare-commit-msg` has execute permissions.
4. Create symlink from the working hook to your repository
   ```
   ln -s /path/to/sugarcrm-prepare-commit-msg/prepare-commit-msg /path/to/repo/.git/hooks/
   ```

