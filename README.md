[![Build and Test](https://github.com/milliewalky/setup-pwsh/actions/workflows/sample.yml/badge.svg)](https://github.com/milliewalky/setup-pwsh/actions/workflows/sample.yml)

# Setup PowerShell (pwsh)

This action downloads, unpacks, and configures PowerShell (pwsh) for use in GitHub Actions workflows. PowerShell is a powerful scripting language and shell developed by Microsoft. PowerShell is unpacked under the temporary directory of a runner.

# Usage

<!-- start usage -->
```yaml
- uses: milliewalky/setup-pwsh@v1
  with:
    # PowerShell release tag from its GitHub Releases page e.g. v7.5.0.
    # default: latest
    tag: ""
```
<!-- end usage -->

This action appends PowerShell to a temporary PATH file, thereby selecting a shell in a subsequent step of your defined `action.yml` file after setting up PowerShell should result in PowerShell becoming available in a somewhat native fashion, given how shells are handled by GitHub Actions runners.
```yaml
- name: peek PowerShell version
  shell: pwsh
  run: $PSVersionTable.PSVersion
```
Thus, this works.

# License

The scripts and documentation in this project are released under the [MIT License](LICENSE)
