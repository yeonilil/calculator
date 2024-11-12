pipeline {
    agent any

    stages {
        stage("Compile") {
            steps {
                sh "./gradlew compileJava"
                }
            }

        stage('Checkout') {
            steps {
                // Git Repository에서 소스 코드 체크아웃
                git branch: 'main', url: 'https://github.com/yeonilil/calculator.git'
            }
        }

        stage('Build') {
            steps {
                // Gradle 실행 권한 추가
                sh 'chmod +x ./gradlew'
                // Gradle 빌드 실행
                sh './gradlew clean build'
            }
        }
    }
}
//202135704 곽서연