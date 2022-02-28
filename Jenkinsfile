pipeline {
    agent any

    stages {
        stage('Declarative SCM Checkout') {
            steps {
                 sh git clone 'https://github.com/Krishna3-cloud/jenkins-nginx-pipeline.git'
            }
        }
        stage('remote copy to nginx server') {
            steps {
                sh scp index.html root@172.31.45.226:/usr/share/nginx/html/index.html
            }
        }
        
    }
}
