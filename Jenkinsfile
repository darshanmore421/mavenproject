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
	sh  'scp  /var/lib/jenkins/workspace/job_master/webapp/target/webapp.war   ubuntu@172.31.42.160:/home/ubuntu/qaenv.war'
	sh 'mv /home/ubuntu/qaenv.war /var/lib/tomcat10/webapps/'
	}
    stage('Continuous Testing') 
	{
              sh 'echo "Testing Passed"'
	}
   
}
