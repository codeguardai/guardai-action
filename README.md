# guardai-action

A GitHub Action for running GuardAI in GitHub Workflows

<!-- action-docs-inputs source="action.yml" -->

## Inputs

| name           | description                                               | required | default        |
| -------------- | --------------------------------------------------------- | -------- | -------------- |
| `version`      | <p>Version of GuardAI to install</p>                      | `false`  | `latest`       |
| `provider`     | <p>AI provider</p>                                        | `true`   | `""`           |
| `model`        | <p>AI model to use</p>                                    | `false`  | `""`           |
| `directory`    | <p>Directory to scan</p>                                  | `false`  | `.`            |
| `changes_only` | <p>Scan only changed files</p>                            | `false`  | `false`        |
| `repo`         | <p>GitHub repository</p>                                  | `false`  | `""`           |
| `pr_number`    | <p>Pull request number</p>                                | `false`  | `""`           |
| `github_token` | <p>GitHub API token</p>                                   | `false`  | `""`           |
| `host`         | <p>Custom AI server host</p>                              | `false`  | `""`           |
| `port`         | <p>Custom AI server port</p>                              | `false`  | `""`           |
| `token`        | <p>Token for authenticating with the custom AI server</p> | `false`  | `""`           |
| `endpoint`     | <p>API endpoint for the custom server</p>                 | `false`  | `/api/v1/scan` |
| `output_file`  | <p>Optional output file to store GuardAI results</p>      | `false`  | `""`           |

<!-- action-docs-inputs source="action.yml" -->

<!-- action-docs-outputs source="action.yml" -->

<!-- action-docs-outputs source="action.yml" -->

<!-- action-docs-runs source="action.yml" -->

## Runs

This action is a `composite` action.

<!-- action-docs-runs source="action.yml" -->

<!-- action-docs-usage source="action.yml" project="codeguardai/guardai-action" version="v0.1.0" -->

## Usage

```yaml
- uses: codeguardai/guardai-action@v0.1.0
  env:
    # Optional: Environment variables required by the AI provider
    #
    # Set this if you are using OpenAI as the provider
    OPENAI_API_KEY: ${{ secrets.OPENAI_API_KEY }}

    # Set this if you are using Gemini as the provider
    GEMINI_API_KEY: ${{ secrets.GEMINI_API_KEY }}

  with:
    version:
    # Version of GuardAI to install
    #
    # Required: false
    # Default: latest

    provider:
    # AI provider
    #
    # Required: true
    # Default: ""

    model:
    # AI model to use
    #
    # Required: false
    # Default: ""

    directory:
    # Directory to scan
    #
    # Required: false
    # Default: .

    changes_only:
    # Scan only changed files
    #
    # Required: false
    # Default: false

    repo:
    # GitHub repository
    #
    # Required: false
    # Default: ""

    pr_number:
    # Pull request number
    #
    # Required: false
    # Default: ""

    github_token:
    # GitHub API token
    #
    # Required: false
    # Default: ""

    host:
    # Custom AI server host
    #
    # Required: false
    # Default: ""

    port:
    # Custom AI server port
    #
    # Required: false
    # Default: ""

    token:
    # Token for authenticating with the custom AI server
    #
    # Required: false
    # Default: ""

    endpoint:
    # API endpoint for the custom server
    #
    # Required: false
    # Default: /api/v1/scan

    output_file:
    # Optional output file to store GuardAI results
    #
    # Required: false
    # Default: ""
```

<!-- action-docs-usage source="action.yml" project="codeguardai/guardai-action" version="0.1.0" -->
