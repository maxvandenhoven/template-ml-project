.PHONY: install-pre-commit
install-pre-commit:
	@pre-commit install
	@pre-commit install --hook-type commit-msg


.PHONY: sync-all
sync-all:
	@$(MAKE) --no-print-directory --directory=engine sync


.PHONY: format-all
format-all:
	@$(MAKE) --no-print-directory --directory=engine format


.PHONY: lint-all
lint-all:
	@$(MAKE) --no-print-directory --directory=engine lint


.PHONY: type-all
type-all:
	@$(MAKE) --no-print-directory --directory=engine type


.PHONY: check-all
check-all:
	@$(MAKE) --no-print-directory --directory=engine check
