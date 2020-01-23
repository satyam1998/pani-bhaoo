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

                  }

            }

            stage('Deploy') {

                  steps {

                        echo "Deploying in Staging Area"

                  }

            }

            stage('Deploy Production') {

                  steps {

                        echo "Deploying in Production Area"

                  }

            }

      }

}
