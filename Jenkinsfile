pipeline {
    agent any
    triggers { upstream(upstreamProjects: 'Fraser_test', threshold: hudson.model.Result.SUCCESS) }
    stages {
        stage('child stage') {
                steps {
                    def causes = currentBuild.getBuildCauses()
                    echo("${causes}")
                    def specificCause = currentBuild.getBuildCauses('hudson.model.Cause.UpstreamCause')
                    echo("${causes}")
                    echo("I have run my ${env.BRANCH_NAME}, the question is, will my child")
                }
        }
    }
}