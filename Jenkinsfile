pipeline {
agent any
stages {
stage('Github') {
steps{
echo "Fetching script from Github";
git changelog: false, credentialsId: 'ee9f90ec-fd6e-4535-9707-aff0c3a977e5', poll:
false, url: 'https://github.com/KevinShahgit/JenkinsTest'
}
	}
stage('Compile') {
steps{
echo "This is the compile stage";
bat 'javac Test.java'
}
}
stage('Execute') {
steps{
echo "This is the execution stage";
bat 'java Test'
}
}
}
post {
always {
echo "This will always run";
}
success {
echo "This will run only if successfull";
}
failure {
echo "This will run when failed";
}
unstable {
echo "This will run when unstable";
}
changed {
echo "This will run when there is change in builds";
}
	}
}
