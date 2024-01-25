pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Define the Git repository and get the commit ID
                script {
                    def git_repo = "https://github.com/Ivista/gittestrepo.git"
                    commitId = sh script: "git ls-remote ${git_repo} refs/heads/main", returnStdout: true
                    commitId = commitId.substring(0, 40)
                    short_commitId = commitId.substring(0, 9)
                }
                echo 'Building..'
                echo 'Full commit ID: ${commitId}'
            }
        }
        stage('Test') {
            steps {
                // Test steps go here
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                // Deploy steps go here
                echo 'Deploying..'
            }
        }
    }
}
