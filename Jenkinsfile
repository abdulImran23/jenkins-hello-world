pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M398" and add it to the path.
        maven "M3916"
    }

    stages {
        stage('Echo Version') {
            steps {
                sh 'echo Print Maven Version'
                sh 'mvn -version'
            }
        }
        stage('Build') {
            steps {
                // Get some code from a Gitea repository specifying the main branch
                //git branch: 'main', url: 'https://github.com/abdulImran23/jenkins-hello-world.git'
                // Run Maven Package command and skip tests https://github.com/abdulImran23/jenkins-hello-world.git
                sh 'mvn clean package -DskipTests=true'
            }
        }
        stage('Unit Test') {
    steps {
        for (int i = 0; i < 60; i++) {
            echo "${i + 1}"
            sleep 1
        }
    }
    sh "mvn test"
}
    }
}
