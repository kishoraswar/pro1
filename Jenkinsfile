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
   
     stage('Coverage report')
        {
           withSonarQubeEnv {
              sonar.projectKey=WEZVA
sonar.projectName=SonarDemo
sonar.projectVersion=1.0
sonar.source=src
sonar.javabinaries=bat (/"target\classes"/)
sonar.jacoco.reportPath=bat(/"target\coverage-reports\jacoco-unit.exec"/)
    // some block
          }
  }
}
