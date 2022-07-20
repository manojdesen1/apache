pipeline {
    
    agent any


    tools {
    jdk 'java'
    maven 'maven'

  }

    stages {
        
        stage('Git Clone') {
            steps {
                // Get some code from a GitHub repository
               git branch: 'master',
               url: 'https://github.com/manojdesen1/apache.git'
            }

        }
        stage('aws') {
            steps {
                // Get some code from a GitHub repository
                sh  '''
                  cd $WORKSPACE
                  aws s3 sync . s3://mano1995
                  '''

            }
        }
      }
     }
