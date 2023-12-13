node('built-in')
{
    stage('continousDownload_master')
    {
        
        git 'https://github.com/Ramesh9949/bhavyabhav.git'
    }
    
    stage('continousBuild_master')
    {
        
        sh 'mvn package'
    }
    stage('continousDeployment_master')
    {
        sh 'scp /root/.jenkins/workspace/ramesh/webapp/target/webapp.war ubuntu@10.0.2.201:/var/lib/tomcat9/webapps/testapp.war'
        
    }
    stage('continousTessting_master')
    {
        
         git 'https://github.com/Ramesh9949/FunctionalTesting.git'
         
         sh 'java -jar /root/.jenkins/workspace/ramesh/testing.jar'
    }
    stage('continousDelivery_master')
    {
        
        sh 'scp /root/.jenkins/workspace/ramesh/webapp/target/webapp.war ubuntu@10.0.3.195:/var/lib/tomcat9/webapps/prodapp.war'

    }
    
    
}
