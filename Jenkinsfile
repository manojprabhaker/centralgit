// declarative //
pipeline {
    agent any
    stages {
        stage('check') {
            steps {
                mkdir test
                cd test
                touch testfile
            }
        }
        stage('Test') {
            steps {
                cat test/testfile
            }
        }
        stage('deploy') {
            steps {
                echo "this is a declarative jenkinsfile testfile" >> test/testfile
             }
        }
        stage ('build') {
            steps {
                echo "pipeline run correctly" >> pipeline
            }
        }
    }
}
