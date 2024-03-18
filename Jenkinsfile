pipeline {
    agent any
    
    stages {
        stage('SSH to EC2 Instance') {
            steps {
                script {
                    // Change the permissions of the private key file
                    echo 'done'
                    sh 'ls'
                    sh 'chmod 400 "RDP_key.pem"'
                    echo 'chmod done'
                    
                    // SSH into the EC2 instance using the private key
                    sh '''
                        ssh -i "RDP_key.pem" ubuntu@ec2-15-206-194-50.ap-south-1.compute.amazonaws.com
                        # Commands to execute on the EC2 instance
                        # For example:
                        ls -la
                        exit
                    '''
                }
            }
        }
    }
}
