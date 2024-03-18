pipeline {
    agent any
    
    stages {
        stage('SSH to EC2 Instance') {
            steps {
                script {
                    bat ' ping %host%'
                    // Change the permissions of the private key file
                    
                   // bat 'uname'
                    bat 'icacls "RDP_key.pem" /inheritance:r /grant:r "%USERNAME%":R"'
                    echo 'Permission of private key change '
                    
                    // SSH into the EC2 instance using the private key
                    bat 'ssh -i "RDP_key.pem" %user%@%Public DNS%'
                    echo "connected"
                    bat 'dir'
                    bat  'exit'
                    
                }
            }
        }
    }
}
