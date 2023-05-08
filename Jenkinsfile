pipeline {
    triggers {
  pollSCM('* * * * *')
    }
    agent any
    tools {
  maven 'M2_HOME'
}
   

    stages {
        stage('maven package') {
            steps {
                sh 'mvn clean'
                sh 'mvn install'
                sh 'mvn package'
            }
        }
          stage('test') {
            steps {
               sh 'mvn test'
                
            }

        }
          #stage('deploy') {
            #steps {
               #sh 'mvn deploy'
                # echo 'deploy to Production'
            }
        }
          #stage('validate') {
            #steps {
             # sh 'mvn validate'
                #echo 'Validate all deployed codes to Prod'
                
            }
        }
    }
}
