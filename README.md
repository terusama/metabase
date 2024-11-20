# Velostics Metabase

We have done a fork of the official [Metabase Github Repository](https://github.com/metabase/metabase) in order
to deploy Metabase to Heroku since the buildpack has been deprecated after the release of [Metabase v0.45](https://www.metabase.com/releases/Metabase-0.45).

## Instructions to deploy into Heroku
### 1. Clone this repository locally and get into the root of the project
```
git clone git@github.com:terusama/metabase.git && cd metabase
```

### 2. Login into the Container Registry
```
heroku container:login
```

### 3. Get into the root of this repo locally and create the image
```
docker build -t web .
```

### 4. Push this image into the Container Registry of the Metabase Heroku App
```
heroku container:push web --app velostics-metabase
```

### 5. Release this image into the web dyno the Metabase Heroku App
```
heroku container:release web --app velostics-metabase
```

## License

This repository contains the source code for both the Open Source edition of Metabase, released under the AGPL, as well as the [commercial editions of Metabase](https://www.metabase.com/pricing), which are released under the Metabase Commercial Software License, together with some specific modifications to support Heroku deployment.

See [LICENSE.txt](./LICENSE.txt) for details.

Unless otherwise noted, all files © 2024 Metabase, Inc.

## [Metabase Experts](https://www.metabase.com/partners/)

If you’d like more technical resources to set up your data stack with Metabase, connect with a [Metabase Expert](https://www.metabase.com/partners/?utm_source=readme&utm_medium=metabase-expetrs&utm_campaign=readme).
