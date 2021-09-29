pipeline {
    agent {label 'node2' }
   # parameters { 
        
    #    string (name:'NAME' , description: 'enter your name')
        
    #}
    #triggers{
     #   cron('H/3 * * * *')
        
    #}

    stages {
        stage('BUILD') {
            steps {
                echo 'this is build stage'
                sh ' sleep 5'
            }
        }
        stage ('DEPLOY'){
       parallel{
        stage ('DEPLOY1'){
            steps {
                
                 echo "this is depoly area"
                sh 'sleep 3'
            }
        }
         stage ('DEPLOY2'){
            steps {
                
                 echo "this is depoly area"
                sh 'sleep 5'
            }
        }
       }
       }
        stage ('TEST'){
            steps {
                echo 'this is test area '
                sh 'sleep 3'
                
            }
        }
       
    }
}

