pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
               withAWS(credentials: 'AKIATIIEVA43RQVPKIVA', region: 'us-east-2') {
                   s3Upload(file: 'index.html', bucket: 'jenkins-pipeline-static', path: './index.html')
               }
            }
        }
    }
}