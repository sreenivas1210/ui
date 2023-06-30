pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
             echo 'in build step'
             sh'npm install'   
            }
        }
        
        stage('build second stage') {
            steps {
                echo 'second stage'
                sh 'npm run build'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'in deploy stage'
                sh 'aws s3 sync dist/angular-demo/ s3://vasuui'
            }
        }
    }
    
}