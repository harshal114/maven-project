pipeline
{
	agent any
	
		stages
		{
			stage('scm checkout')
			
			{ 
				steps
				{
					git branch: 'master', url:'https://github.com/harshal114/maven-project'
				}
			}
		
			stage ('validate code')
			{
				steps
				{
				withMaven(maven: 'localmaven') {
					sh 'mvn validate'
						
						}
			
				}
			}
			
			stage ('compile code')
			{
				steps
				{
				withMaven(maven: 'localmaven') {
					sh 'mvn compile'
						
						}
			
				}
			}
			
			stage ('Test code')
			{
				steps
				{
				withMaven(maven: 'localmaven') {
					sh 'mvn test'
						
						}
			
				}
			}
				stage ('package  code')
			{
				steps
				{
				withMaven(maven: 'localmaven') {
					sh 'mvn package'
						
						}
			
				}
			}
			
				stage ('verify  code')
			{
				steps
				{
				withMaven(maven: 'localmaven') {
					sh 'mvn verify'
						
						}
			
				}
			}
			
				stage ('install  code')
			{
				steps
				{
				withMaven(maven: 'localmaven') {
					sh 'mvn install'
						
						}
			
				}
			}
	}
}
