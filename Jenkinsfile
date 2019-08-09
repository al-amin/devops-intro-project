pipeline {
    agent any
    stages {
        stage('---clean---') {
            steps {
                sh "mvn clean -f /var/lib/jenkins/workspace/PipelineProject-2/practiceForAllianz/mavenProject/my-app"
            }
        }
        stage('--test--') {
            steps {
                sh "mvn test -f /practiceForAllianz/mavenProject/my-app"
            }
        }
        stage('--package--') {
            steps {
                sh "mvn package -f /practiceForAllianz/mavenProject/my-app"
            }
        }
    }
}
