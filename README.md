#### heroku-buildpack-cmd
just runs a simple build commnd when we are all done

### install
create a file at the root of your project called **.buildrun** with the command you want to run.

### sample .buildrun
```sh
#!/usr/bin/env bash

echo $SOURCE_VERSION > $1/.gitversion
export "SOURCE_VERSION=$SOURCE_VERSION"
cd $1/cli && ./build.sh $1 $2 $3
```
