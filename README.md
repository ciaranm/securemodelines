# securemodelines
A secure alternative to Vim modelines

Vim's internal modeline support allows all sorts of annoying and potentially insecure options to be set. This script implements a much more heavily restricted modeline parser that permits only user-specified options to be set. 

The `g:secure_modelines_allowed_items` array contains allowed options.  See `:help securemodelines_options` for default values.

The `g:secure_modelines_verbose` variable, if set to something true, will make the script warn when a modeline attempts to set any other option.

The `g:secure_modelines_modelines` variable overrides the number of lines to check. By default it is 5.

If `g:secure_modelines_leave_modeline` is defined, the script will not clobber &modeline. Otherwise &modeline will be unset.

Keeping things up to date on vim.org is a nuisance. For the latest version, visit: http://github.com/ciaranm/securemodelines

Install into your plugin directory of choice.

vim.org: http://www.vim.org/scripts/script.php?script_id=1876
