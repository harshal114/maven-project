pipeline
{
	agent any
	
		stages
		{
			stage('scm checkout')
			
			{ 
				steps
				{
					branch: 'master', 'git:"https://github.com/harshal114/maven-project"'
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
			
			stage ('Test code')
			{
				steps
				{
				withMaven(maven: 'localmaven') {
					sh 'mvn test'
						
						}
			
				}
			}


	}
}
