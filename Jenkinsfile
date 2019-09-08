pipeline{
		agent any
				stages{
			stage('One'){
					steps{
							echo "Hi, THis is Tushar from Panvel"
						 }
			}
		    stage('Two'){
					steps{
					
						echo "Input option not working"
					     }
			}
			stage('Three'){
					when{
						not{
							 branch "master"
						   }
						}
					steps{
							echo "Hello"
						 }
			}
			stage('Four'){
					parallel{
						stage('Unit Test'){
									steps{
											echo "Running unit test...."
										 }
						}
						stage('Build Test'){
									steps{
												echo "creating build...."
                        mvn clean install
											   }
						}
					}
			}
			
		}					
}
