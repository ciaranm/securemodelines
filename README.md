# securemodelines
A secure alternative to Vim modelines

Vim's internal modeline support allows all sorts of annoying and potentially insecure options to be set. This script implements a much more heavily restricted modeline parser that permits only user-specified options to be set. 

The g:secure_modelines_allowed_items array contains allowable options. By default it is set as follows: 
```vim
    let g:secure_modelines_allowed_items = [ 
                \ "textwidth",   "tw", 
                \ "softtabstop", "sts", 
                \ "tabstop",     "ts", 
                \ "shiftwidth",  "sw", 
                \ "expandtab",   "et",   "noexpandtab", "noet", 
                \ "filetype",    "ft", 
                \ "foldmethod",  "fdm", 
                \ "readonly",    "ro",   "noreadonly", "noro", 
                \ "rightleft",   "rl",   "norightleft", "norl" 
                \ ] 
```
The `g:secure_modelines_verbose` option, if set to something true, will make the script warn when a modeline attempts to set any other option. 

The `g:secure_modelines_modelines` option overrides the number of lines to check. By default it is 5. 

If `g:secure_modelines_leave_modeline` is defined, the script will not clobber &modeline. Otherwise &modeline will be unset. 

Install into your plugin directory of choice.

vim.org: http://www.vim.org/scripts/script.php?script_id=1876
