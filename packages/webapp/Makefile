build:
	pnpm wagmi generate
	pnpm next build
.PHONY: build

# Serves webapp in production environment (after building)
serve:
	pnpm next start
.PHONY: serve

# Serves webapp in dev environment (building not required)
dev:
	pnpm next dev
.PHONY: dev

# Serves webapp in dev environment (building not required), do not generate proofs, sends bogus
# proofs instead.
dev-noproofs:
	NO_PROOFS=1 pnpm next dev
.PHONY: dev-noproofs

# Runs linter (use make check instead which also checks typescript typing).
lint:
	pnpm next lint --max-warnings 0
.PHONY: lint

# Runs code quality checks.
check: lint build
.PHONY: check