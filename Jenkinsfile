pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('SonarQube Analysis') {
            steps {
                sh '''
                mvn sonar:sonar \
                -Dsonar.projectKey=my-app \
                -Dsonar.host.url=http://192.168.70.138:9000 \
                -Dsonar.login=sqa_5cbdcbd906624437698da290905467033de836db
                '''
            }
        }

        stage('Upload to Nexus') {
            steps {
                sh 'mvn clean deploy -DskipTests'
            }
        }
    }
}
