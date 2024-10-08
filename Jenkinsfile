pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the code...'
                // Example: Build with Maven
                // sh 'mvn clean package'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Running Unit and Integration Tests...'
                // Example: Test with JUnit
                // sh 'mvn test'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Performing Code Analysis...'
                // Example: Code analysis with SonarQube
                // sh 'sonar-scanner'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Performing Security Scan...'
                // Example: Security scan with OWASP Dependency Check
                // sh 'dependency-check --project <project-name> --scan <path>'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to Staging...'
                // Example: Deploy with AWS CLI
                // sh 'aws deploy ...'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Running Integration Tests on Staging...'
                // Example: Integration tests on staging
                // sh './run-staging-tests.sh'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploying to Production...'
                // Example: Deploy with AWS CLI
                // sh 'aws deploy ...'
            }
        }
    }

    post {
        always {
            emailext to: 'minullaksen@gmail.com',
                     subject: "Jenkins Pipeline: new new commit Build ${currentBuild.fullDisplayName}",
                     body: "Pipeline finished with status: ${currentBuild.currentResult}"
        }
    }
}
