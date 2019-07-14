Pipeline
{
	agent any
		stages
		{
			stage(‘One’)
			{
				echo ‘Hi, this is Sudarsana’
			}
			stage(’Two’)
				{
				steps
					{
					input(‘Do you want to proceed ?’)
					}
				}
			stage(’Three’)
			{
				parallel
				{
					stage(‘Unit Test’)
						{
						steps
							{
							echo “Running the unit test”
							}
						}
					stage(‘Integration Test’)
						{
							agent
							{
								docker
								{
									reuseNode false
									image ‘ubuntu’
								}
							}
							steps
								{
								echo ‘Running the Integration test’
								}
						}			

				}
			}
		}
}
