pipeline {
    agent any
    triggers { upstream(upstreamProjects: 'Fraser_test/master,Fraser_test/staging', threshold: hudson.model.Result.SUCCESS) }
    stages {
        stage('child stage') {
                steps {
                    script{
                        def causes = currentBuild.getBuildCauses()
                        echo("${causes.upstreamProject}")
                    }
                }
        }
    }
}