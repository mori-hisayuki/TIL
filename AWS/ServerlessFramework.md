

## 自分のアカウントにLambdadeploy
### deploy
```
yarn sls deploy --aws-profile <profile>
```

### remove
```
yarn sls remove -f example-function --aws-profile <profile>
```

### involke
```
yarn sls invoke -f example-function --path test/resources/example_request.json --aws-profile <profile>
```
