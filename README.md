# StanfordDaily mobile app

[![Greenkeeper badge](https://badges.greenkeeper.io/TheStanfordDaily/StanfordDaily_Mobile.svg)](https://greenkeeper.io/)

# Setup
```
npm i
npm i -g expo-cli

npm run ios

# or
npm run android
```

# Release
expo build:ios --release-channel production
expo build:android --release-channel production

expo publish --release-channel production
