pipeline {
    agent any
    stages {
        stage("Compile") {
            steps {
                sh "./gradlew compileJava"
            }
        }
        stage("Build") {
            steps {
                  // Gradle 실행 권한 추가
                sh 'chmod +x ./gradlew'
                // Gradle 빌드 실행
                sh './gradlew clean build'
            }
        }
        stage("Unit test") {
            steps {
                sh "./gradlew test"
            }
        }
    }
}
