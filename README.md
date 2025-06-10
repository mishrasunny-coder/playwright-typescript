# playwright-typescript
Playwright TypeScript Training

## UNIT 1: Install Latest Version of Node

# Download and install nvm:
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash

# in lieu of restarting the shell
\. "$HOME/.nvm/nvm.sh"

# Download and install Node.js:
nvm install 24

# Verify the Node.js version:
node -v # Should print "v24.2.0".
nvm current # Should print "v24.2.0".

# Verify npm version:
npm -v # Should print "11.3.0".

# Install latest version of npm
npm install -g npm@latest

################################################################


## UNIT 2: Install Playwright

# Run
npm init playwright@latest

# After running the command above go through the questions and install for TypeScript
Select the language you want to use for your tests. We recommend TypeScript.
Select the name of the test directory. We recommend tests.
Add a GitHub Action for automating tests. We recommend Yes.
Install Playwright browsers. We recommend selecting the default of True.

The output tells us that a new npm project was created with a package.json file, and that Playwright Test was installed. It also tells us the files that were created:

playwright.config.ts: The Playwright Test Configuration file.
.github/workflows/playwright.yml: GitHub Action for automating tests
tests/: Top-level folder that Playwright searches recursively for tests with an example test script.
tests-examples/: Staging folder with a demo todo app test script to try out.
package.json: The npm project file.


To run tests in Playwright, use the npx playwright test command. The command runs all the tests in the tests/ folder, which is the folder name we defined in step 2 when installing.

`npx playwright test`

Let's open the HTML report to see more details about the test run.

`npx playwright show-report`

To run the tests only on chromium
`npx playwright test --project chromium`