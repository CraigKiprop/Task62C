pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Use a build automation tool like maven"
                //bat 'mvn clean package'
                // Add actual build steps here
            }
        }

        stage('Unit and Integration Test') {
            steps {
                echo "Use test automation tools for unit and integration tests"
                //sh 'mvn test'
                // Add actual test steps here
            }
            post {
                always {
                    
                       mail to: "craigkorir@gmail.com",
                        subject: "Unit and Integration Test Status",
                        body: "Unit and Integration test logs attached"
                        
                
                }
            }
        }

        stage('Code Analysis') {
            steps {
                echo "Integrate a code analysis tool like SonarQube"
                //sh 'mvn sonar:sonar'
                // Add actual code quality check steps here
            }
        }

        stage('Security Scan') {
            steps {
                echo "Integrate a security scanning tool like OWASP ZAP"
                // sh 'zap-cli --spider <your_app_url>'
            }
            post {
                always {
                    
                        mail to: "craigkorir@gmail.com",
                        subject: "Security Scan Status",
                        body: "Security scan logs attached",
                        
                    
                }
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo "Run integration tests in the staging environment"
                // sh 'mvn verify -Pstaging'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo "Deploy to production using Ansible or other tools"
                // sh 'ansible-playbook -i inventory/production deploy.yml'
            }
        }
    }

    
}
