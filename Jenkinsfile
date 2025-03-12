pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M398"
    }

    stages {
        
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
               // git branch: 'main', url: 'https://github.com/Kandpal-Gaurav/jenkins-hello-world.git'
                // Run Maven on a Unix agent.
                sh "mvn clean package -DskipTests=true"

                // To run Maven on a Windows agent, use
                // bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }
        }
        
        stage('Test') {
            steps {
                
                sh 'mvn test'
            }
        }
        
        stage('Deploy') {
            steps {
                sh 'echo Deploying'
                // sh 'java -jar target/hello-demo-*.jar '
            }
        }
    }
    
}
