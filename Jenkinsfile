pipeline {
    agent any
    options {
        buildDiscarder(logRotator(numToKeepStr: '5'))
        timeout(time: 10, unit: 'MINUTES')
        timestamps()  // Timestamper Plugin
        disableConcurrentBuilds()
    }
    environment {
        GREETINGS_TO = 'Jenkins Techlab'
        CURRENT_BUILD_ID = ${env.BUILD_ID}
    }
    stages {
        stage('Greeting') {
            steps {
                echo "Hello, ${env.GREETINGS_TO} ${env.BUILD_ID}!"
            }
        }
    }
}
