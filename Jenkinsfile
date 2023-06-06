pipeline{
   agent {
       node {
           label 'workstation'
       }
   }
   environment {
          SAMPLE_URL="example.com"
       }
   stages{
      stage('one'){
        steps{
           sh 'echo hello world'
           sh 'echo hello universe'
           sh 'echo ${SAMPLE_URL}'
        }
      }
   }
      post {
           always {
               sh 'echo post cleanup steps'
           }
       }
}