pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                
                    sh 'mvn -f mavewebappdemo/pom.xml clean install'
                
            }
        }

        stage ('Testing Stage') {

            steps {
                
                    sh 'mvn -f mavewebappdemo/pom.xml  test'
                
            }
        }
        stage('Deploy to Tomcat'){
        steps {
        sh 'cp -r /root/.jenkins/workspace/yv1/mavewebappdemo/target/* /opt/apache-tomcat-8.5.30/webapps/'
        }
        }


        
    }
}
