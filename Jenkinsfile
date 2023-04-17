pipeline{
    agent any
    
    tools{
        maven "M3-A"
    }
    
    stages{
        stage('Checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/steffpotter/lbg-hello-world-maven'
            }
        }
        stage('Compile'){
            steps{
                sh "mvn clean compile"
            }
        }
        stage('Test') {
            steps {
                sh "mvn test"
            }
        }
        stage('Package') {
            steps {
                sh "mvn -Dmaven.test.skip package"
            }
        }
    }
}