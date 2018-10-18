# self-documenting-makefile


## Makefile
```
.DEFAULT_GOAL := help

# VARIABLES

# TARGETS

# See details at from http://marmelab.com/blog/2016/02/29/auto-documented-makefile.html
help: ## Prints this help message
	@grep -E '^[a-zA-Z_-]+:.*?## .*$$' $(MAKEFILE_LIST) | awk 'BEGIN {FS = ":.*?## "}; {printf "\033[36m%-30s\033[0m %s\n", $$1, $$2}'

foo: ## This line will be shown as documentation when `make` or `make help` command is used.
	bar
  

```  
