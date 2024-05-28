pipeline{
        agent {
            label 'venky-agent'
        }
        parameters {
          string defaultValue: 'master', name: 'repo_name'
        }
        stages {
            stage("checkout the code"){
                steps{
                    git branch: "$repo_name", url: 'https://github.com/Vyankatesh95/javademo.git'
                }
            }
             stage("build the code"){
                steps{
                    sh "mvn package"
                }
            }  
        }
        post {
                always{
            cleanWs()
                }
            }
}
