pipeline {
    agent {
        /*dockerfile {
        filename 'Dockerfile'        
        args '-v /.cache/ -v /.bower/  -v /.config/configstore/'
         }*/
        docker {
           image 'node:6-alpine' 
            args '-p 3000:3000' 
          }
        environment {
        HOME = '.'
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
    }
}
