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
    }
    environment {
        HOME = '.'
        }
    stages {
        stage('Build/install the app') { 
            steps {
                sh 'npm install' 
                //sh 'npm start'
            }
        }
         stage('Docker build and deploy') { 
            steps {
                sh 'docker build . -t reactimage' 
                sh 'docker run reactimage'
                //sh 'docker exec -it 
                //sh 'npm start'
            }
    }
}
