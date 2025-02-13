pipeline {
    agent any
    environment {
        CC = "/usr/bin/g++"  // Set the correct compiler path
    }
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/AbhishekHerbertSamuel/CppAutomationRepo.git'
            }
        }
        stage('Compile C++ Program') {
            steps {
                sh '$CC -o hello hello.cpp'
            }
        }
        stage('Run C++ Program') {
            steps {
                sh './hello'
            }
        }
    }
}
