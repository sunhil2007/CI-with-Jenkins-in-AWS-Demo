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
        stage('Archive') { 
            steps {
            	echo "Archiving Artifacts..."
                sh "archiveArtifacts 'project/target/*.war'"
            }
        }
        
        
        
        stage('Deploy') { 
            steps {
            	echo "Deploying code using pipeline.."
                sh "deploy adapters: [tomcat9(credentialsId: '327c0133-dbef-4f1f-b0f8-fd62efb730f8', path: '', url: 'http://35.238.182.141:8080')], contextPath: null, onFailure: false, war: '**/*.war'"               
            }
        }
    }
}
