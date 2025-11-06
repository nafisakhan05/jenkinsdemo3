pipeline {
     agent any 
     environment{
        PYTHON = 'C:\\Users\\nextgen\\AppData\\Local\\Programs\\Python\\Python312\\python.exe extract_file.py'
     }
        stages{
            stage('Checkout Code'){
                steps{
                   checkout scm
                }
               
            }
            stage('Extract Data'){
                steps{
                  bat "${env.PYTHON} extract_file.py"
                }
                
            }
        }
        post {
            success {
                echo "Success..."
            }
            failure {
                echo "Failure..."
            }
            always{
               echo "Always..."
            }
        } 
}
