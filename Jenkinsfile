pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                tidy -q -e *.html
                withAWS(credentials: '7437fdc5-b7d9-4159-a312-ba024745682c', region: 'us-east-2') {
                   s3Upload(file: 'index.html', bucket: 'jenkins-pipeline-static', path: 'index.html')
               }
            }
        }
    }
}