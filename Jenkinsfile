pipeline {

agent any

stages {
   stage( 'checkout' ) {
steps {
checkout scm
     }}
stage( 'Build' ) {
  steps {
  sh '/home/ubuntu/apache-maven-3.8.1/bin/mvn install '
}}
stage( 'Deployment' ){
  steps {
  sh 'sshpass -p "sam" scp target/LoginWebApp.war sam@172.17.0.2:/home/sam/demo/apache-tomcat-8.5.64/webapps'
  }}
}
}
