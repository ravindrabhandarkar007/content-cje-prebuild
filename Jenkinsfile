node {
    properties([parameters([string(defaultValue: 'ronaldo', description: '', name: 'name', trim: false)])])
   def mvnHome
   stage('Preparation') { // for display purposes
       git clone https://github.com/ravindrabhandarkar007/content-cje-prebuild.git
      
   }
   stage('Build') {
      // Run the maven build
         sh 'mvn clean package'
         }
}
