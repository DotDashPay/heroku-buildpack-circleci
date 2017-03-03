# Heroku Buildpack: CircleCI
This is a [Heroku buildpack](https://devcenter.heroku.com/articles/buildpacks)
that
- retrieves the CircleCI token from
  [`CIRCLECI_TOKEN`](https://devcenter.heroku.com/articles/buildpack-api#bin-compile)
  - retrieves the CircleCI project from
  [`CIRCLECI_PROJECT`](https://devcenter.heroku.com/articles/buildpack-api#bin-compile)
  - retrieves the CircleCI build number from
  [`CIRCLECI_BUILD_NUM`](https://devcenter.heroku.com/articles/buildpack-api#bin-compile)
  - retrieves the location of the
  [`CIRCLECI_ARTIFACT`](https://devcenter.heroku.com/articles/buildpack-api#bin-compile)
  - retrieves the CircleCI repo number from `CIRCLECI_REPO_NUM`
  from the [CircleCI artifacts API](https://circleci.com/docs/api#build-artifacts)
- retrieves the artifact from Circle
- decompresses it
