
pipeline {
    agent any
    stages {
        stage('check') {
            steps {
                sh '''
                    data=`date | awk {'print $4'}`
                    mkdir /tmp/test-$data
                    touch testfile
                    '''
            }
        }
        stage('Test') {
            steps {
                sh 'cat testfile'
            }
        }
        stage('deploy') {
            steps {
                sh 'echo "this is a declarative jenkinsfile testfile" > testfile'
             }
        }
        stage ('build') {
            steps {
                sh 'echo "pipeline run correctly" >> pipeline'
            }
        }
        stage ('cleanup') {
            steps {
                sh '''
                   rm -r /tmp/test*
                   '''
            }
        }    
    }
}
