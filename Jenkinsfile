properties([parameters([choice(choices: ['master', 'dev-1', 'dev-2'], description: 'Choose your branch', name: 'Branch'), string(defaultValue: 'https://github.com/javahometech/myweb', description: 'please choose your URL', name: 'URL', trim: true)])])

 

node{

   stage('SCM code pull'){
       git branch: "${params.Branch}", url: "${params.URL}"
   }    
   
   stage('Build the code'){
       sh '''cd /var/lib/jenkins/workspace/myweb
mvn clean package'''
   }
}
