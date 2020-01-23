pipeline {

      agent any

      stages {

            stage('Init') {

                  steps {

                        echo 'Hi, this is Satyam from 3Pillar'

                        echo 'We are Starting the Testing'
                        git 'https://github.com/satyam1998/pani-bhaoo.git'

                  }

            }

            stage('Build') {

                  steps {

                        echo 'Building Sample Maven Project'
                        archiveArtifacts '**/*.*'

                  }

            }

            stage('Deploy') {

                  steps {

                        echo "Deploying in Staging Area"
                        deploy adapters: [tomcat9(credentialsId: 'e146d8f5-fef8-4a23-a417-cd9d82495697', path: '', url: 'http://52.15.132.162:9090/')], contextPath: '/', war: '**/*.war'

                  }

            }

            stage('Deploy Production') {

                  steps {

                        echo "Deploying in Production Area"

                  }

            }

      }

}
