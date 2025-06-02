**Title:** Updated Project Dependencies to Latest Stable Versions

**Body:**

Project dependencies, including both `dependencies` and `devDependencies`, were found to be outdated. They have now been updated to their latest stable versions to ensure compatibility, security, and access to the latest features.

**Key Updated Packages:**

*   **Lit:** Updated to `^3.3.0`
*   **TypeScript:** Updated to `^5.3.3`
*   **ESLint:** Updated to `^8.57.0` (along with related `@typescript-eslint/eslint-plugin` and `@typescript-eslint/parser` to `^7.7.0`)
*   **Prettier:** Updated to `^3.2.5`
*   **lit-analyzer:** Updated to `^2.0.3`
*   **@web/test-runner:** Updated to `^0.18.0`
*   Other devDependencies were also updated as part of this process.

**Resolution:**

*   The `package.json` file has been updated with the new versions of these packages.
*   `npm install` was run to install the updated packages and regenerate the `package-lock.json` file accordingly.

This ensures the project is using up-to-date dependencies.
