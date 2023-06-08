pipeline { 
  
   agent any

   stages {
   
     stage('Install Dependencies') { 
       when {
        branch 'master'
      }
        steps { 
           sh 'echo "Install dependencies ..only for master"' 
        }
     }
     
     stage('Test') { 
       when {
           anyOf {
                    branch "dev"
                    branch "master"
                    branch "qa"
                    branch "stage"
                }
      }
        steps { 
           sh 'echo "testing application for dev,qa,master,stage........"'
        }
      }

         stage("Deploy application") { 
           when {
        not  {
                    branch "master"
                }
      }
         steps { 
           sh 'echo "deploying application..."'
         }

     }
  
   	}

   }
