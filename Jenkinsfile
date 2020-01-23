pipeline {

      agent any

      stages {

            stage('GIT') {

                  steps {

                        echo 'Hi, this is Satyam from 3Pillar'

                        echo 'We are Starting the Testing'
                        git 'https://github.com/satyam1998/Jenkins.git'

                  }

            }
            stage('COMPILE_packege') {

                  steps {

                        echo 'COMPILE THE FILE'
                        def mvnhome=tool name: 'Local_maven', type: 'maven'
                        sh '${mvnhome}/bin/mvn package'

                  }

            }

            stage('Build') {

                  steps {

                        echo 'Building Sample Maven Project'
                        archiveArtifacts '**/*.war'
                        copyArtifacts filter: '**/*.war', fingerprintArtifacts: true, projectName: 'First-pipeline'

                  }

            }


      }

}
