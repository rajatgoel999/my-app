pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                dir('my-app') {
                    sh 'mvn clean package'
                }
            }
        }

        stage('SonarQube Analysis') {
            steps {
                dir('my-app') {
                    sh '''
                    mvn sonar:sonar \
                    -Dsonar.projectKey=my-app \
                    -Dsonar.host.url=http://192.168.70.138:9000 \
                    -Dsonar.login=sqa_5cbdcbd906624437698da290905467033de836db
                    '''
                }
            }
        }

        stage('Upload to Nexus') {
            steps {
                dir('my-app') {
                    sh 'mvn deploy -DskipTests'
                }
            }
        }
    }
}
