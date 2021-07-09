pipeline{
  agent { label 'slave2' }
  stages{
      stage(changefolder){
        steps{
          sh 'cd /home/slave2'
        }
      }
    
      stage(compile){
        steps{
          sh 'mvn compile' 
        }
      }
      stage(build){
       steps{
         sh 'mvn package'
       }
      }
     stage(deploy){
     steps{
        sh 'cp /home/slave2/java-mvn-hello-world-web-app/target/mvn-hello-world.war /opt/apache-tomcat-9.0.50/webapps'
        }
     } 
  }
}
