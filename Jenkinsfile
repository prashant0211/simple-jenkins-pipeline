pipeline {

    agent any
    
    environment {
        PASS = credentials('registry-pass') 
    }

    stages {

        stage('Build') {
            steps {
                // sh '''
                //     ./jenkins/build/mvn.sh mvn -B -DskipTests clean package
                //     ./jenkins/build/build.sh

                // '''
                echo "this is build"
            }

            // post {
            //     success {
            //        archiveArtifacts artifacts: 'java-app/target/*.jar', fingerprint: true
            //     }
            // }
        }

        stage('Test') {
            steps {
               // sh './jenkins/test/mvn.sh mvn test'
               echo "this is test"
            }

            post {
                always {
                    //junit 'java-app/target/surefire-reports/*.xml'
                    echo "this is always"
                }
            }
        }

        stage('Push') {
            steps {
                //sh './jenkins/push/push.sh'
                echo "this is push"
            }
        }

        stage('Deploy') {
            steps {
                //sh './jenkins/deploy/deploy.sh'
                echo "this is deploy"
            }
        }
    }
}
