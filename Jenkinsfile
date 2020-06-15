node {
    properties([parameters([string(defaultValue: 'ronaldo', description: '', name: 'name', trim: false)])])
   def mvnHome
   stage('Preparation') { // for display purposes
     checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/linuxacademy/content-cje-prebuild.git']]])
           
      
   }
   stage('Build') {
      // Run the maven build
         sh 'mvn clean package'
         }
   stage('Post Job'){
       sh 'bin/makeindex'
   }
   stage('Results') {
      archiveArtifacts 'index.jsp'
   }
}
