pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps work too"
                    ls -lah
                '''   
            } 
        }
        withAWS(region:'us-west-2') {
            s3Upload(file:'static', bucket:'accidents-dashboard', path:'/home/mlaw/workspace/devops/static')
        }
    }
}

