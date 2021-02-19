pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
                sh "mvn clean package"
            }
            
        }
        stage("Deploy"){
            steps{
                deploy adapters: [tomcat7(credentialsId: 'b9a3e5e9-6b92-4451-9c54-88e5a44298bd', path: '', url: 'http://ec2-3-128-200-170.us-east-2.compute.amazonaws.com:8080/')], contextPath: 'javawebapp', war: '**/java-web-project.war'
            }
        }
    }
}
