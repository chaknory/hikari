pipeline {
    agent any
    environment {
        POM_VERSION = readMavenPom().getVersion()
    }
    tools { 
        maven 'maven-3.6.3' 
        jdk 'JAVA_HOME' 
    }
    stages {
        stage('clone') {
            steps {
                echo 'clone..'
            //    git 'https://github.com/chaknory/hikari.git'
            }
        }
        stage('Build') {
            
        
            steps {
                script {
                    if (env.NODE_NAME == 'master') {
                        echo 'I only execute on the master branch'
                    } else {
                        echo 'I execute elsewhere'
                    }
                }

                echo 'Building..0'
                echo "${POM_VERSION}"
                
                sh 'printenv'
                echo 'Building..'
               // sh 'mvn clean install'
            }
        }
        
    }
}
