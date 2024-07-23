# React-issues

npm install --save-dev eslint prettier eslint-config-prettier eslint-plugin-prettier husky lint-staged


Create a file named .eslintrc.json in the root of your project with the following content:

{
  "extends": ["eslint:recommended", "plugin:prettier/recommended"],
  "plugins": ["prettier"],
  "rules": {
    "prettier/prettier": "error",
    "semi": ["error", "always"],
    "quotes": ["error", "single"],
    "no-unused-vars": "warn"
  }
}

Create a file named .prettierrc in the root of your project with the following content:

{
  "singleQuote": true,
  "trailingComma": "all",
  "printWidth": 80,
  "tabWidth": 2,
  "semi": true
}

package.json
{
  "husky": {
    "hooks": {
      "pre-commit": "lint-staged"
    }
  },
  "lint-staged": {
    "src/**/*.{js,jsx}": [
      "eslint --fix",
      "prettier --write",
      "git add"
    ]
  }
}

create .husky
npx husky-init
npm i

and in huky pre commit file 
add npx lint-staged
