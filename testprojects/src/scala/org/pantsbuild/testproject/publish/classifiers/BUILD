scala_library(name='classifiers',
  provides=artifact(
    org='org.pantsbuild.testproject.publish',
    name='classifiers',
    repo=testing,
    publication_metadata=pants_library('This is a test. This is only a test.')
  ),
  dependencies=[
    ':compiler-interface',
    ':incremental-compiler',
    ':sbt-interface',
  ],
  sources=['Hello.scala']
)

SBT_REV='0.13.7'

jar_library(name = 'compiler-interface',
            jars = [jar(org = 'com.typesafe.sbt', name = 'compiler-interface', rev = SBT_REV,
                        classifier='sources', intransitive=True,
                        artifacts=[ivy_artifact(name='compiler-interface', classifier='javadoc')])])

jar_library(name = 'incremental-compiler',
            jars = [jar(org = 'com.typesafe.sbt', name = 'incremental-compiler', rev = SBT_REV,
                        intransitive=True)])

jar_library(name = 'sbt-interface',
            jars = [jar(org = 'com.typesafe.sbt', name = 'sbt-interface', rev = SBT_REV,
                        intransitive=True,
                        artifacts=[ivy_artifact(name='sbt-interface', classifier='javadoc')])])
