node{
   stage('SCM Checkout'){
     git 'https://github.com/kishoraswar/pro1'
   }
   stage('Compile-Package'){
      // Get maven home path
      echo "executing maven package"
      def mvnHome =  tool name: 'maven', type: 'maven'   
         bat(/"${mvnHome}\bin\mvn" clean package/)     
         }
    }
