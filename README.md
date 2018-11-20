# securemodelines

## description

secure, user-configurable modeline support for {neo,}vim

vim's internal modeline support allows all sorts of annoying and potentially
insecure options to be set. this script implements a much more heavily
restricted modeline parser that permits only user-specified options to be set.

the `g:secure_modelines_allowed_items` array contains allowable options. by
default it is set as follows:

	let g:secure_modelines_allowed_items = [
		\ "textwidth",   "tw",
		\ "softtabstop", "sts",
		\ "tabstop",     "ts",
		\ "shiftwidth",  "sw",
		\ "expandtab",   "et",   "noexpandtab", "noet",
		\ "filetype",    "ft",
		\ "foldmethod",  "fdm",
		\ "readonly",    "ro",   "noreadonly", "noro",
		\ "rightleft",   "rl",   "norightleft", "norl",
		\ "cindent",     "cin",  "nocindent", "nocin",
		\ "smartindent", "si",   "nosmartindent", "nosi",
		\ "autoindent",  "ai",   "noautoindent", "noai",
		\ "spell", "nospell",
		\ "spelllang",
		\ "wrap", "nowrap",
		\ "syntax"
	\ ]

the `g:secure_modelines_verbose` option, if set to something true, will make
the script warn when a modeline attempts to set any other option.

the `g:secure_modelines_modelines` option overrides the number of lines to
check. By default it is 5.

if `g:secure_modelines_leave_modeline` is defined, the script will not clobber
&modeline. Otherwise &modeline will be unset.

## install details

install example using [plug](https://github.com/junegunn/vim-plug):

	Plug 'xero/securemodelines'
