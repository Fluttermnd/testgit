pipeline {
         agent {
                label 'master'
               }
         stages {
                 stage('Download image') {
                                steps {
                                    echo 'Download images!'
                                    sh "wget 'https://cdn.britannica.com/79/232779-050-6B0411D7/German-Shepherd-dog-Alsatian.jpg'"
                                    
                                }
                 }
                 stage('Added to zip archive') {
                                steps {
                                    echo ''Zip has been runned!
                                    sh 'zip archive.zip *.jpg'
                                }
                 }
                 stage('Show ls -la') {
                                  steps {
                                        sh 'ls -la'
                                  }
                 }

              }
                               post {
                    always {
                      archive "*.zip"
                      sh 'rm -rf *'
                      echo "Romoved all files!"
                    }
                               }
}
