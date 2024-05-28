pipeline{
        agent {
            label 'venky-agent'
        }
        stages {
            stage("checkout the code"){
                steps{
                    checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/cloud-dev-user/javademo.git']])
                }
            }
             stage("build the code"){
                steps{
                    sh "mvn package"
                }
            }
            stage("clean up workspace"){
                steps{
            cleanWs()
                }
            }
        }
}
