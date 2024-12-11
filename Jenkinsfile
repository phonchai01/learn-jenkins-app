pipeline {
    agent any
 
    stages {
        stage('with Docker') {
            agent{
                docker{
                    image 'node:18-alpine'
                }
            }
            steps {
                sh '''
                    echo "with docker"
                    npm --version
                    touch "with-container.txt"
                '''
            }
        }
        stage('without Docker') {
            steps {
                sh '''
                    echo "without docker"
                    touch "without-container.txt"
                '''
            }
        }
       
    }
>>>>>>> 0de0e65d5de6809f41b3588d0c4042eb24a7da6f
}