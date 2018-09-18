# Prettier

```json
{
  "arrowParens": "avoid",
  "bracketSpacing": true,
  "jsxBracketSameLine": false,
  "parser": "babylon",
  "semi": true,
  "singleQuote": true,
  "tabWidth": 2,
  "trailingComma": "all",
  "useTabs": false
}
```

1. ### arrowParens
    > "avoid" - Omit parens when possible. Example: x => x
    <br>
    > "always" - Always include parens. Example: (x) => x

2. ### parser

    > babylon: JS  
      flow  
      typescript  
      postcss  
      json  
      graphql  
      markdown

3. ### jsxBracketSameLine

    ```html
    /* true */
    <button
      className="btn">
      Click Here
    </button>

    /* false */
    <button
      className="btn"
    >
      Click Here
    </button>
    ```
    
4. ### trailingComma

    > **none** - No trailing commas.  
      **es5** - Trailing commas where valid in ES5 (objects, arrays, etc.)  
      **all** - Trailing commas wherever possible (including function arguments). This requires node 8 or a transform.

<br>

# Linting

1. ### Airbnb
    - Packages to be installed:

    ```
      yarn add -D eslint babel-eslint eslint-config-airbnb eslint-plugin-import eslint-plugin-jsx-a11y eslint-plugin-react
    ```

    - `eslintrc` file

    ```json
    {
      "parser": "babel-eslint",
      "extends": "airbnb",
      "rules": {
        "react/jsx-filename-extension": 0,
        "import/prefer-default-export": 0,
        "arrow-body-style": 0
      },
      "env": {
        "browser": true,
        "jest": true
      }
    }
    ```

    <hr/>

    #### ** Shortcut **

    ```
      npx install-eslint salhotra-eslint
    ```

    Then add `jest` flag in env inside eslintrc.
