pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
            	echo "Building code using pipeline.."
                sh "mvn clean package"
            }
        }
        stage('Test') { 
            steps {
            	echo "Testing code using pipeline.."
            }
        }
        stage('Deploy') { 
            steps {
            	echo "Deploying code using pipeline.."
                sh "scp -v -o StrictHostKeyChecking=no /tmp/abcd.txt tomcat8@devops3-tomcat:/tmp/."
            }
        }
    }
}
