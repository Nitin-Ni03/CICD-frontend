pipeline {
    
    stages {
        stage('Install') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build'
                // Example: sh 'npm install && npm run build'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                sh '''
                    cp -r dist/* /var/www/html/
                    sudo systemctl restart nginx
                '''
            }
        }
    }
}
