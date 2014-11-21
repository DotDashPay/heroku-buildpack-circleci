# Heroku Buildpack: CircleCI
This is a [Heroku buildpack](https://devcenter.heroku.com/articles/buildpacks)
that
- retrieves the CircleCI token from
  [`ENV_DIR/CIRCLECI_TOKEN`](https://devcenter.heroku.com/articles/buildpack-api#bin-compile)
- finds the latest build for the last commit using the
  [CirlceCI build API](https://circleci.com/docs/api#recent-builds-project) for the
  [`ENV_DIR/CIRCLECI_PROJECT`](https://devcenter.heroku.com/articles/buildpack-api#bin-compile)
- retrieves the location of the
  [`ENV_DIR/CIRCLECI_ARTIFACT`](https://devcenter.heroku.com/articles/buildpack-api#bin-compile)
  from the [CircleCI artifacts API](https://circleci.com/docs/api#build-artifacts)
- retrieve the artifact from Circle
- decompress it
