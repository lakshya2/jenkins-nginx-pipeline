pipeline {
    agent any

    stages {
        stage('get git repository') {
            steps {
               git branch: 'master', credentialsId: '0f716d97-7c49-40ec-b8be-d4be71a1fa58', url: 'https://github.com/lakshya2/jenkins-nginx-pipeline.git'
            }
            
        }
        stage('remote copy to nginx server') {
            steps {
                sh 'scp -i /home/ubuntu/ngi.pem -o StrictHostKeyChecking=no index.html ubuntu@172.31.45.117:/var/www/html/index.html'
            }
        }
        
    }
}
