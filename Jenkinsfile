pipeline {
    agent any
    triggers { upstream(upstreamProjects: 'Fraser_test/master,Fraser_test/staging', threshold: hudson.model.Result.SUCCESS) }
    stages {
        stage('child stage') {
                steps {
                    script{
                        def causes = currentBuild.getBuildCauses()
                        echo("${causes}")
                        def specificCause = currentBuild.getBuildCauses('hudson.model.Cause.UpstreamCause')
                        echo("${causes}")
                        echo("I have run my ${env.BRANCH_NAME}, the question is, will my child")
                    }
                }
        }
    }
}