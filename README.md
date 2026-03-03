# Branch Protection & PR Automation

## What This Repository Demonstrates

### Branch Protection
- Direct pushes to `main` are blocked
- PRs require status checks to pass before merge
- At least one approving review is required

### CI Pipeline (`.github/workflows/ci.yml`)
- `terraform fmt -check` — enforces consistent formatting
- `terraform init` — validates provider configuration
- `terraform validate` — checks syntax and internal consistency

### Auto-Labeler (`.github/workflows/labeler.yml`)
- `.tf` files → `terraform` label
- `.md` files → `docs` label
- `.github/workflows/` → `ci` label

### PR Checklist Bot (`.github/workflows/pr-checklist.yml`)
- Posts a structured checklist on every new PR
- Author and reviewer sections

### CODEOWNERS (`.github/CODEOWNERS`)
- Terraform files require platform team review
- Workflow files require DevOps lead review

## Key Learnings
- Branch protection prevents accidental direct pushes
- Required status checks enforce code quality gates
- CODEOWNERS automates reviewer assignment
- Auto-labeling improves PR triage at scale

# Submission