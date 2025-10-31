pipeline { 
agent any 
stages{ 
stage('checkout'){ 
steps{ 
git 'https://github.com/gracyteresa/Jenkins_CI-CD_Final-project.git'
 
            } 
        } 
        stage("Compile-Project"){ 
            steps{ 
                sh 'mvn compile' 
            } 
        } 
        stage("Test-project"){ 
            steps{ 
                sh 'mvn test' 
            } 
        } 
        stage('sonarqube-scanning'){ 
            steps{ 
                withSonarQubeEnv('SonarQube') { 
                    sh 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.7.0.1746:sonar'  
                }     
            } 
        } 
        stage("packaging-project"){ 
            steps{ 
                sh 'mvn package' 
            } 
        } 
        stage("Artifact-uploading to nexus"){ 
            steps{ 
               nexusArtifactUploader artifacts: [[artifactId: 'myapp', classifier: '', file: 'target/myapp.war', type: '.war']], credentialsId: 'nexus', groupId: 'in.gracy', nexusUrl: '184.73.106.207:8081', nexusVersion: 'nexus3', protocol: 'http', repository: 'final-project', version: '8.3.3-SNAPSHOT' 
            } 
        } 
        stage("Deploy to tomcat"){ 
            steps{ 
               deploy adapters: [tomcat9(alternativeDeploymentContext: '', credentialsId: 'tomcat', path: '', url: 'http://54.82.56.117:8080')], contextPath: 'myapp-gracy', war: '**/*.war'
            } 
        } 
        
        
}
}