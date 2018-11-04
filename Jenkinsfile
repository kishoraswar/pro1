node{
   stage('SCM Checkout'){
     git 'https://github.com/kishoraswar/pro1'
   }
   stage('Compile-Package'){
      // Get maven home path
      echo "executing maven package"
      def mvnHome =  tool name: 'maven', type: 'maven'   
         bat(/"${mvnHome}\bin\mvn" -Dmaven.test.failure.ignore clean package/)     
      
   }
   
   stage('Slack Notification'){
       slackSend baseUrl: 'https://hooks.slack.com/services/',
       channel: '#jenkins-pipeline-demo',
       color: 'good', 
       message: 'Welcome to Jenkins, Slack!', 
       teamDomain: 'javahomecloud',
       tokenCredentialId: 'slack-demo'
   }
}
