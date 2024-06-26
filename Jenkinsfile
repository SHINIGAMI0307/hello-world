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
                        sudo mkdir -p ${deployDir}
                        sudo cp -r * ${deployDir}
                    """
                }
            }
        }
    }
}
