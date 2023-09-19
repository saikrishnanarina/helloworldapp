pipeline{
    agent any
    }
    tools{
        maven "M2_HOME"
    }
    stages{
        
        stage('Git'){
            steps{
              checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/saikrishnanarina/helloworldapp.git']])
            }
        }
        stage('Build'){
            steps{
                sh 'mvn clean install package'
            }
        }
    }
}
