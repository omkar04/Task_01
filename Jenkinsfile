pipeline {
    agent {
        node {
            label 'agent_01'
        }
    }
    
    stages {
        stage('connect to server') {
            steps {
                echo 'Hello, World! fuck you'
                sh 'chmod 400 "RDP_key.pem"'
                sh 'ssh -i "RDP_key.pem" ubuntu@ec2-15-206-194-50.ap-south-1.compute.amazonaws.com'
            }
        }
    }
}
