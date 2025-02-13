pipeline {
    agent any
    environment {
        CXX_INCLUDE_PATH = "/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/usr/include/c++/v1"
    }
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/AbhishekHerbertSamuel/CppAutomationRepo.git'
            }
        }
        stage('Compile C++ Program') {
            steps {
                sh 'echo "Using C++ Standard Library Path: $CXX_INCLUDE_PATH"'
                sh 'g++ -I$CXX_INCLUDE_PATH -o hello hello.cpp'
            }
        }
        stage('Run C++ Program') {
            steps {
                sh './hello'
            }
        }
    }
}
