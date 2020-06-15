node {
    properties([parameters([string(defaultValue: 'ronaldo', description: '', name: 'name', trim: false)])])
   stage('Preparation') { // for display purposes
       sh '''
       git clone https://github.com/ravindrabhandarkar007/content-cje-prebuild.git
      '''
   }
   stage('Build') {
      // Run the maven build
         sh 'mvn clean package'
         }
}
