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
   
}
