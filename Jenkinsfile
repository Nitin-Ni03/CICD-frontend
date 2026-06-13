pipeline {
    
    Stages {
        stage('Install') {
            Steps {
                sh 'npm install'
            }
        }

        stage('Build') {
            Steps {
                sh 'npm run build'
                // Example: sh 'npm install && npm run build'
            }
        }

        stage('Deploy') {
            Steps {
                echo 'Deploying application...'
                sh '''
                    cp -r dist/* /var/www/html/
                    sudo systemctl restart nginx
                '''
            }
        }
    }
}
