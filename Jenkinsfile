pipeline {
    agent any
    stages {
         stage('Static Code Analysis') {
             steps {
                 sh 'mvn verify org.sonarsource.scanner.maven:sonar-maven-plugin:sonar -Dsonar.projectKey=rrtech-azure -DskipTests'
             }
          }
//         stage('clean') {
//             steps {
//                 sh 'mvn clean'
//             }
//         }
//         stage('validate') {
//             steps {
//                 sh 'mvn validate'
//             }
//         }
//          stage('compile') {
//             steps {
//                 sh 'mvn compile'
//             }
//         }
//         stage('test') {
//             steps {
//                 sh 'mvn test -DskipTests'
//             }
//         }
//         stage('package') {
//             steps {
//                 sh 'mvn package -DskipTests'
//             }
//         }
//         stage('verify') {
//             steps {
//                 sh 'mvn verify -DskipTests'
//             }
//         }
//          stage('install') {
//             steps {
//                 sh 'mvn install -DskipTests'
//             }
//         }
//          stage('Deployment - Deploy a Artifact devtech-1.0.0.war file to Tomcat Server') { 
//             steps {
//                 sh 'curl -u admin:redhat@123 -T target/**.war "http://34.229.94.145:8080/manager/text/deploy?path=/azuredevops&update=true"'
//             }
//         }  
        stage('Stage-9 : SmokeTest') { 
            steps {
                sh 'curl --retry-delay 10 --retry 5 "http://34.229.94.145:8080/azuredevops"'
            }
        }
    }
}
