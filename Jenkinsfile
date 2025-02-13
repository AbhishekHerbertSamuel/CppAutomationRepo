pipeline {
    agent any
    environment {
        CC = "/opt/homebrew/bin/g++"  // Ensure it uses the correct compiler
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


