pipeline {
    agent any
    options {
        buildDiscarder(logRotator(numToKeepStr: '5'))
        timeout(time: 10, unit: 'MINUTES')
        timestamps()  // Timestamper Plugin
        disableConcurrentBuilds()
    }
    tools {
        jdk 'jdk11'
        maven 'maven36'
    }
    stages {
        stage('Build') {
            steps {
                echo """java home ${env.JAVA_HOME}"""
                echo """path ${env.PATH}"""

                sh 'java -version'

                sh 'javac -version'

                sh 'mvn --version'
            }
        }
    }
}