# Workflow Setup

### Assuming Node.js is installed:
1. `npx create-react-app project-name`
2. `npm i --save-dev eslint`
3. Set `"lint": "eslint 'src/components/**/*.js'"` in package.json scripts
4. `npm init @eslint/config` to setup `.eslintrc.json`
5. Importing React is optional now so eslint will throw errors saying `"React" must be in scope when using JSX.` To fix:
    * Add to rules: `"react/react-in-jsx-scope": "off"`
    * Additional rule aside from those generated using init:
    
        ```json
        "no-multi-spaces": ["error"],
        "react/prop-types": "off"
        // Additional rules to be added here in future
        ```
6. Add `"jest": true` inside env since eslint will give `test or expect is not defined` error in `App.test.js`
7. Assuming setting is not applicable for **Workspace** and not **User**. Under *File > Preferences > Settings* look for **Code Actions on Save** and edit `settings.json`
    ```json
    {
        "editor.codeActionsOnSave":{
            "source.fixAll.eslint": true
        },
        "eslint.validate": ["javascript"]
    }
    ```

### Extensions:
* Comment Anchors
