pipeline{
  agent { label 'slave2' }
  stages{
      stage(changefolder){
        steps{
          cd /home/slave2
        }
      }
    
      stage(compile){
        steps{
          mvn compile 
        }
      }
      stage(build){
       steps{
         mvn package
       }
      }
     stage(deploy){
     steps{
        cp /home/slave2/java-mvn-hello-world-web-app/target/mvn-hello-world.war /opt/apache-tomcat-9.0.50/webapps
        }
     } 
  }
}
