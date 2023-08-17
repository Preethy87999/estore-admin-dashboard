pipeline{
    agent any
    stages{
        stage('pushed from github'){
            steps{
                  checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Preethy87999/estore-admin-dashboard']])
                
            }
        }
        stage('installed project'){
            steps{
                 bat 'npm install -f'
            }
        }
        stage('build project'){
            steps{
                 bat 'npm run ng -- build'
            }
           
        }
    }
}

