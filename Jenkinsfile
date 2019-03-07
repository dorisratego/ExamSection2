node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "docker build -t ExamSection2:latest ."
}

stage('Docker login to hub and push the image'){
sh "docker login -u 'DRatego' -p 'Letitbe123$' "
sh "docker tag ExamSection2:latest DRatego/ExamSection2:latest"
sh "docker push DRatego/ExamSection2:latest"
}

stage('Apply changes to the environment') {
sh "ls -l"
}

stage('Expose port'){
sh "docker run --expose=3259"
}


}