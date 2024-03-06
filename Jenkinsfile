pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Check out the source code from the repository
                git 'https://github.com/SajjanKhanal/wordpress.git'
            }
        }

        stage('Build') {
            steps {
                // Build your WordPress site or perform any necessary build steps
                // For example, if using Docker, you might build the Docker image here
                sh 'docker build -t wordpress-site .'
            }
        }

        stage('Test') {
            steps {
                // Run tests to ensure the code quality and functionality
                // You might run automated tests here, such as PHPUnit tests for WordPress plugins/themes
                // Example: sh 'phpunit tests/'
            }
        }

        stage('Deploy') {
            steps {
                // Deploy the changes to your web server
                // This could involve pushing the Docker image to a registry or deploying directly to a server
                // Example: sh 'docker push username/wordpress-site:latest'
                // Example: sh 'scp -r /path/to/wordpress-site user@web-server:/var/www/html/'
            }
        }
    }
}

