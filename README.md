# How to?

### How to uninstall Python packages from environment?
- for windows
  - open PS(powershell)
  - `pip freeze | ForEach-Object { pip uninstall -y $_.split('==')[0] }`
  - similarly to the Unix version. It lists all installed packages (`pip freeze`), then for each package, it extracts the package name and uninstalls it (`pip uninstall -y`).

- for linux/mac
  - `pip freeze | xargs pip uninstall -y`
  - list all installed packages (`pip freeze`), then pass each package to the pip uninstall command to uninstall it (`xargs pip uninstall -y`).

#### NOTE: Please note that this command will uninstall all packages installed globally, including essential packages that are required for Python to function properly. Use it with caution, and consider creating a virtual environment for your projects to avoid affecting the global environment.

### Bonus: try this as well for many problems `pip cache purge`

