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
                sh 'scp -i /home/lakshya/Downloads/ngi.pem -o StrictHostKeyChecking=no index.html ubuntu@15.207.107.213:/var/www/html/index.html'
            }
        }
        
    }
}
