# Install
## {apps}/build.sbt
  resolvers += "github Maven Repository" at "https://github.com/koduki/maven-repos/raw/master"

# Publish
## checkout
  git clone git@github.com:koduki/maven-repos.git

## {apps}/build.sbt
  publishTo := Some(Resolver.file("local-github-repos", file("../maven-repos")))

## publish
  cd {apps}
  sbt publish 

  cd ../maven-repos
  git commit
  git push  
  
