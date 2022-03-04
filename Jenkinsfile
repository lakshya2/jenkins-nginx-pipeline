pipeline {
    agent any

    stages {
        stage('get git repository') {
            steps {
                git branch: 'master', credentialsId: '6d8a218a-670f-4df4-868b-23621e541445', url: 'https://github.com/lakshya2/jenkins-nginx-pipeline.git'
            }
            
        }
        stage('remote copy to nginx server') {
            steps {
                sh 'scp -i /home/lakshya/Downloads/ngi.pem -o StrictHostKeyChecking=no index.html ubuntu@15.207.107.213:/var/www/html/index.html'
            }
        }
        
    }
}
