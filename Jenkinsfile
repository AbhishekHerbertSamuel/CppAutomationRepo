pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/AbhishekHerbertSamuel/CppAutomationRepo.git'
            }
        }
        stage('Compile C++ Program') {
            steps {
                sh 'g++ -o hello hello.cpp'
            }
        }
        stage('Run C++ Program') {
            steps {
                sh './hello'
            }
        }
    }
}

