# Heroku Buildpack: S3 downloader

TODO(avi): - the entire repo needs to be renamed

This is a [Heroku buildpack](https://devcenter.heroku.com/articles/buildpacks)
that
  - Grabs your artifact based on the `ARTIFACT` environment variable from s3
  given a `BUILD_ID`.
  - Uses amazon credentials `AWS_ROOT_ARENA_ACCESS_KEY_ID` and 
  `AWS_ROOT_ARENA_SECRET_ACCESS_KEY`
  - (currently unused) You can alternatively set a `CUSTOM_ARTIFACT_URL` to fetch the artifact from a custom URL (no auth)
  - Once the artifact is downloaded, it is decompressed into a top-level `bin`
  directory in odin
