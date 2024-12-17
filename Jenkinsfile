pipeline {
    agent any
 
    stages {
        stage('Build') {
            agent{
                docker{
                    image 'node:18-alpine'
                    reusNode true
                }
            }
            steps {
                sh '''
                    ls -la
                    node --version
                    npm --version
                    np, ci
                    npm run build
                    ls -la
                    
                '''
            }
        }

        stage('Test'){
            agent{
                docker{
                    image 'node:18-alpine'
                    reusNode true
                }
            }
            steps{
                sh '''
                    test -f build/index.html
                    npm test
                '''
            }


        }
    }
}