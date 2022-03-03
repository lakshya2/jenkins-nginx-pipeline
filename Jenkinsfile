pipeline {
    agent any

    stages {
        stage('get git repository') {
            steps {
                git branch: 'master', credentialsId: '2ad6cb5a-8dc5-4820-b8dc-dc3eb755ecc6', url: 'https://github.com/paawanyadav/jenkins-nginx-pipeline.git'
            }
        }
        stage('remote copy to nginx server') {
            steps {
                sh 'scp -i "/home/pawan/Downloads/LEMPAWS.pem" index.html ubuntu@34.203.243.8:/var/www/html/index.html'
            }
        }
        
    }
}
