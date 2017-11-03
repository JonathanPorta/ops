### Dependencies
```
  yarn add prettier eslint eslint-plugin-react eslint-plugin-react-native eslint-plugin-prettier
```

### package.json
```
"scripts":{
  "test": "./node_modules/.bin/eslint . && node node_modules/jest/bin/jest.js",
  "prettify": "find . -name '*.js' -o -path ./node_modules -prune | xargs ./node_modules/.bin/prettier --write"
...
}
...
"prettier":{
  "semi": false,
  "singleQuote": true
}

```

### .eslintrc.json
```
{
  "extends": "prettier",
  "plugins": [

    "react",
    "react-native", "prettier"
  ],
  "parser": "babel-eslint",
  "rules": {
    "prettier/prettier": "error"
  },
  "env": {
    "browser": true,
    "node": true,
    "jest": true
  },
  "ecmaFeatures": {
    "jsx": true
  }
}
```

### Test Run
```
  ./node_modules/.bin/eslint .
```

### Edit in Place
```
  yarn run prettify
```
