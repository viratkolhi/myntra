pipeline 
{
	agent any
	
	stages 
{
	    stage('Checkout') 
{
	        steps 
{
			checkout scm			       
		      }
}
		stage('Build') 
{
	           steps 
{
sh '/home/codemaster/Documents/Grras/apache-maven-3.8.7/bin/mvn install'
}
}
		stage('Deployment')
{
		    steps 
{
sh 'cp /home/codemaster/Documents/Grras/myntra/target/myntra.war /home/codemaster/Documents/Grras/apache-tomcat-9.0.71/webapps'
	}
}
}
post
{
always
{
emailext body: 'summary', subject: 'pipeline status', to: 'abhaymalaiya1995@gmail.com'
}
}
}
