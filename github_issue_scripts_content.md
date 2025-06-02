**Title:** Updated `package.json` Scripts to Modern Tools and Syntax

**Body:**

Several scripts in `package.json` were found to be using deprecated tools or outdated command syntax. These have been updated to ensure compatibility with modern tooling and best practices.

**Specific Script Changes:**

*   **`lint:lit-analyzer`**: This script was reviewed and updated. While the command `lit-analyzer 'src/**/*.ts'` might appear similar, the underlying `lit-analyzer` dependency was updated to version `^2.0.3`, ensuring the script utilizes the latest version of the tool.
*   **`analyze`**: This script was significantly updated. It previously used `wca analyze` (web-component-analyzer), which has been replaced with `cem analyze --globs "src/**/*.ts" --outdir .` from the `custom-elements-manifest` package. This change aligns with current best practices for generating custom elements manifest files.

**Resolution:**

*   The `package.json` file has been updated with the corrected script commands.
*   `custom-elements-manifest` (version `^2.1.0`) was added as a `devDependency` to support the updated `analyze` script.
*   `npm install` was run to install the new dependency.

These changes ensure that the project's scripts are using up-to-date and actively maintained tools.
