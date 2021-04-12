pipeline {
    agent {
        docker { image "ubuntu:18.04"
                  args '-u root:root -v $HOME/workspace/myproject:/myproject'
            
        }
    }
    stages {
       stage('Checkout SCM') {
            steps {
                echo '> Checking out the source control ...'
                checkout scm
            }
        }
        stage('Test') {
            steps {
                sh '''
                echo "test-again"
                cat README.md
                '''
            }
        }

    }
}
