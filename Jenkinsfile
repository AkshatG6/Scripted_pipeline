pipeline{
	agent any
	stages{
		stage('compile'){
			steps{
				echo "Compiled Successfully!!";
			}
		}
		stage('JUnit'){
			steps{
				echo "JUnit Passed Successfully!!";
			}
		}
		stage('Quality-Gate'){
			steps{
			echo "Sonar Cube Quality-Gate Passed Successfully!!";
		}
	}
stage('Deploy'){
steps{
echo " Passed !!!";
}
}
}
post{
always {
echo "This will always run"
}
success {
echo "This will run only if successful"
}
failure {
echo "This will run only if fail"
}
unstable{
echo "This will run only if runwas marked as unstable"
}
changed{
echo "This will run only if the state of the pipeline has changed"
echo "For example pipeline was previously failing but now successful"
}
}
}
