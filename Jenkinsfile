pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "mymaven"
    }

    stages {
        stage('demobuild') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/abbadiomer9/DevOpsClassCodes.git'

                // Run Maven on a Unix agent.
                sh "mvn install"

                // To run Maven on a Windows agent, use
                // bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }

            }
        }
}
