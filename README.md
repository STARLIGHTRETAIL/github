<div align="center">

# github

[![GitHub stars](https://img.shields.io/github/stars/StarlightRetail/github?style=for-the-badge&logo=github&colorB=blue)](https://github.com/STARLIGHTRETAIL/github/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/StarlightRetail/github?style=for-the-badge&logo=github&colorB=cyan)](https://github.com/STARLIGHTRETAIL/github/network/members)
[![GitHub issues](https://img.shields.io/github/issues/StarlightRetail/github?style=for-the-badge&logo=github&colorB=yellow)](https://github.com/STARLIGHTRETAIL/github/issues)
[![License](https://img.shields.io/github/license/StarlightRetail/github?style=for-the-badge&colorB=green)](https://github.com/STARLIGHTRETAIL/github/blob/main/LICENSE)
[![Last Commit](https://img.shields.io/github/last-commit/StarlightRetail/github?style=for-the-badge&logo=git&colorB=purple)](https://github.com/STARLIGHTRETAIL/github/commits)

<p align="center">
<a href="https://github.com/STARLIGHTRETAIL/github"><img src="https://img.shields.io/badge/View_on_GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="View on GitHub" /></a>
<a href="https://github.com/STARLIGHTRETAIL/github/issues/new"><img src="https://img.shields.io/badge/Report_Bug-FF0000?style=for-the-badge&logo=github&logoColor=white" alt="Report Bug" /></a>
<a href="https://github.com/STARLIGHTRETAIL/github/issues/new?labels=enhancement"><img src="https://img.shields.io/badge/Request_Feature-0080FF?style=for-the-badge&logo=github&logoColor=white" alt="Request Feature" /></a>
</p>

<br/>

*Part of the [StarlightRetail](https://github.com/StarlightRetail) organization*

---

</div>

# github
**GitHub Organization Management Repository for StarlightRetail**

---

## Overview

This repository serves as the cornerstone for managing GitHub automation and governance within the [StarlightRetail](https://github.com/STARLIGHTRETAIL) organization. It centralizes workflows and processes critical to ensuring a secure, compliant, and efficient setup for all repositories under the organization's ownership.

Key functionalities include enforcing repository visibility policies, maintaining a sanitized public-facing organization profile, and automating governance tasks to align with security and compliance best practices. These workflows simplify administrative overhead, improve organizational security posture, and ensure consistency across the GitHub presence of StarlightRetail.

---

## Key Features

- **Repository Visibility Hardening**: Automatically converts public repositories to private while preserving controlled public content in `STARLIGHTRETAIL/.github`.
- **Organization Profile Management**: Maintains the public-facing profile content in a separate repository (`STARLIGHTRETAIL/.github`) for sanitized visibility.
- **CI/CD Integration**: Streamlined workflows utilizing GitHub Actions for automation and governance.
- **Secure Access Management**: Utilizes organization secrets and scoped Personal Access Tokens for privileged operations.

---

## Tech Stack

| Technology           | Purpose                                               |
|-----------------------|-------------------------------------------------------|
| **GitHub Actions**   | Core automation platform for workflows and governance |
| **YAML**             | Workflow definitions for CI/CD automations            |
| **Markdown**         | Documentation and public-facing profile content       |

---

## Getting Started

The repository is designed for seamless operation within the StarlightRetail organization. Below are the steps to run the hardening workflows effectively:

### Prerequisites:

1. **GitHub Access**:
   - Ensure you are part of the [StarlightRetail organization](https://github.com/STARLIGHTRETAIL).
   - Have adequate permissions to execute workflows (e.g., Org Admin).
2. **Organization Personal Access Token**:
   - Store an `ORG_ADMIN_PAT` secret in this repository with the following scopes:
     - `admin:org`
     - `repo`

### Installation:

Clone the repository using Git:

```bash
git clone https://github.com/STARLIGHTRETAIL/github.git
cd github
```

No additional dependencies are required to execute workflows, as the repository utilizes native GitHub Actions functionality.

---

## Project Structure

The layout is oriented around workflows and organization governance:

```
.github/                 # GitHub meta-workflows and governance operations
├── workflows/           # CI/CD automation using GitHub Actions
│   ├── copilot-setup-steps.yml  # Workflow for Copilot initialization
│   ├── harden-repos.yml         # Workflow to enforce repository visibility
LICENSE                   # MIT License
README.md                 # Main documentation file
profile/                  # Public-facing content for STARLIGHTRETAIL/.github
├── README.md             # Sanitized content deployed as org profile
```

---

## Usage

### Running the "Harden Repository Visibility" Workflow

The workflow ensures all repositories in the StarlightRetail organization, except the public `.github` repository, remain private. Follow these steps:

1. Navigate to the Workflows section in the repository:  
   **Actions → Harden Repository Visibility**
2. Select **Run workflow** and configure the parameters:
   - `dry_run`: (default `true`) Set to `false` to apply changes.
3. Click **Run workflow** and monitor the logs for activity.

Triggered workflows perform the following:
- Validate repository visibility settings.
- Ensure public-facing content exists in the `.github/profile` repository.

---

## Contributing

Contributions to this repository are welcome! To ensure consistency and adherence to organizational policies, please follow these steps:

1. Fork the repository and create a feature branch.
2. Make your changes while adhering to the [MIT License](LICENSE) and organizational guidelines.
3. Submit a pull request for review.

For more details, review the [StarlightRetail contribution guide](https://github.com/STARLIGHTRETAIL/.github/blob/main/CONTRIBUTING.md).

---

## License

This repository is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.  

**Note**: All actions and workflows in this repository are subject to StarlightRetail's organizational policies. Ensure compliance with applicable governance rules when contributing or executing workflows.

---

---

<div align="center">

**[StarlightRetail](https://github.com/StarlightRetail)** — Building the future of retail technology

Made with :purple_heart: by the StarlightRetail team

</div>