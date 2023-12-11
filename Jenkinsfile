pipeline {
    agent any

    stages {
        stage('Get Uptime on Slave') {
            agent {
                // Specify the label or name of the Jenkins slave
                node {
                    label 'slave-node'
                }
            }
            steps {
                script {
                    // Run the 'uptime' command on the slave
                    def result = sh(script: 'uptime', returnStatus: true)

                    // Display the result
                    echo "Uptime on slave: ${result}"
                }
            }
        }
        stage('Echo') {
            steps {
                // Use the 'sh' step inside a 'steps' block
                sh 'echo my-app'
            }
        }
    }
}
