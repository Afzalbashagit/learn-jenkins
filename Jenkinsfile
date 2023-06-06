pipeline{
   agent {
       node {
           label 'workstation'
       }
   }
   stages{
      stage('one'){
        steps{
           sh 'echo hello world'
           sh 'echo hello universe'
        }
      }
   }
      post {
           always {
               sh 'echo post cleanup steps'
           }
       }
}