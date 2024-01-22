pipeline {
    agent any
    parameters {
          string(name: 'firstname', defaultValue: '', description: 'what is your firstname?')
          string(name: 'secondname', defaultValue: '',  description: 'what is your secondname?')
          string(name: 'subject', defaultValue: '', description: 'what is your subject?')
          string(name: 'sports', defaultValue: '', description: 'what is your sports?')
          string(name: 'course', defaultValue: '', description: 'what is your course?')
        
    }
    stages {
        stage('user.sh') {
            environment { 
                  firstname = "${params.firstname}"
                  secondname = "${params.secondname}"
                  subject = "${params.subject}"
                  sports = "${params.sports}"
                  course = "${params.course}"
            }  
            steps {
                sh """
                echo 'This is user input data'
                /home/sohail/khan/user.sh $firstname $secondname $subject $sports $course
                """
            }
        }
    }
    
}
