node('built-in')
{
    stage('continousDownload_loans')
    {
        
        git 'https://github.com/Ramesh9949/bhavyabhav.git'
    }
    
    stage('continousBuild_loans')
    {
        
        sh 'mvn package'
    }
    stage('continousDeployment_loans')
    {
        sh 'scp /root/.jenkins/workspace/ramesh/webapp/target/webapp.war ubuntu@10.0.2.201:/var/lib/tomcat9/webapps/testapp.war'
        
    }
    
    
}
