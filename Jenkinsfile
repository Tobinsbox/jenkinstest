pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'printenv'
            }
        }
    }
    post{
        always{echo "All Phases Finished"}
        success {
            mail to:'bin.tang@unisys.com',
                subject:"Success Pipeline:%{currentBuild.fullDisplayName}",
                body:"Something is wrong with ${env.BUILD_URL}"
        }
    }
}
