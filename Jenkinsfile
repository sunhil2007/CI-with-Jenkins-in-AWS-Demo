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
                scp -o StrictHostKeyChecking=no /tmp/abcd.txt sunhil2007@devops3-tomcat:/tmp/.
            }
        }
    }
}
