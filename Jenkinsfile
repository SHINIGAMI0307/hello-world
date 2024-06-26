pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
                script {
                    // Define the base deployment directory
                    def baseDeployDir = '/var/www/html'

                    // Determine the branch-specific deployment directory
                    def deployDir = "${baseDeployDir}/${env.BRANCH_NAME}"

                    // Ensure the deployment directory exists
                    sh """
                        mkdir -p ${deployDir}
                        cp -r * ${deployDir}
                    """
                }
            }
        }
    }
}
