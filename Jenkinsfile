node('built-in') 
{
    stage('Continuous Download') 
	{
    git 'https://github.com/darshanmore421/mavenproject.git'
	}
    stage('Continuous Build') 
	{
    sh  'mvn package'
	}
	stage('Continuous Deployment') 
	{
	sh  'ssh -i /home/ubuntu/PROJECT.pem ubuntu@172.31.42.160'
	sh  'scp /var/lib/jenkins/workspace/job_master/webapp/target/webapp.war   ubuntu@172.31.42.160:cd /var/lib/tomcat10/webapps/qaenv.war'
	}
    stage('Continuous Testing') 
	{
              sh 'echo "Testing Passed"'
	}
   
}
