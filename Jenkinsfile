pipeline {
    agent any
    environment {
        DISABLE_AUTH = 'true'
        DB_ENGINE    = 'sqlite'
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
            script {
                    if (env.BRANCH_NAME == 'master') {
                        echo 'I only execute on the master branch'
                    } else {
                        echo 'I execute elsewhere'
                    }
                }
        
            steps {
                echo 'Building..0'
               // echo "${env.NODE_NAME}"
                
                sh 'printenv'
                echo 'Building..'
               // sh 'mvn clean install'
            }
        }
        
    }
}