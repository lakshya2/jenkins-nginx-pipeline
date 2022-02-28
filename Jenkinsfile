pipeline {
    agent any

    stages {
        stage('get git repository') {
            steps {
                 git credentialsId: '163d4f57-b8ef-4eaf-b037-bb1b6c65fe01', url: 'https://github.com/Krishna3-cloud/jenkins-nginx-pipeline.git'
            }
        }
        stage('remote copy to nginx server') {
            steps {
                sh 'scp -i index.html ubuntu@172.31.45.226:/usr/share/nginx/html/index.html'
            }
        }
        
    }
}
