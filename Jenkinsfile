node{

stage('CheckOutCode'){
git credentialsId: 'f52a7301-4cbc-4389-91fd-0e6ef69c493d', url: 'https://github.com/DevOpsproject-asn/nodeJs-project.git'
}

stage('Build'){
nodejs(nodeJSInstallationName: 'nodejs22.40.0'){
sh "npm install"
}
}

stage('ExecuteSonarQubeReport'){
nodejs(nodeJSInstallationName: 'nodejs22.40.0'){
sh "npm run sonar"
}
}

/*
stage('UploadArtifactsIntoNexus'){
sh "npm publish"
}
*/

stage('RunNodeJsApp'){
sh "npm start"
}

}

