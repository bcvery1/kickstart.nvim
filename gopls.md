# GoPLS
Golang language server fix

There is a bug with the async system call command which causes the gopls lsp to return nil for

```bash
go env GOMODCACHE
```

This can be fixed by changing the local variable in:
`~/.local/share/nvim/lazy/nvim-lspconfig/lua/lspconfig/server_configurations/gopls.lua`
to be the output of the above command.
