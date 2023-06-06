pipeline{
   agent {
       node {
           label 'workstation'
       }
   }
   triggers{ pollSCM('H/2 * * * *') }
    options {
           ansiColor('xterm')
       }
   parameters {
               string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
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
           sh 'echo person- ${PERSON}'
        }
      }
   }
      post {
           always {
               sh 'echo post cleanup steps'
           }
       }


}