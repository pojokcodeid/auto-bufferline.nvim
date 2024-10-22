# auto-lsp.nvim

- auto-bufferline.nvim is an automatic configuration for bufferline.nvim

# Instalation

- Lazy

```lua
return {
	"akinsho/bufferline.nvim",
	branch = "main",
	event = { "BufRead", "InsertEnter", "BufNewFile" },
	dependencies = "pojokcodeid/auto-bufferline.nvim",
	config = function()
		vim.opt.termguicolors = true
		local config = require("auto-bufferline").config()
		require("bufferline").setup(config)
	end,
	},
}
```

- Close Current Buffer

```lua
require("auto-bufferline.configs.utils").bufremove()
```
