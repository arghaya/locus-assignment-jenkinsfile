node {
    def ci_pipeline
    stage('initial_clean_up') {
        cleanWs()
    }
    stage('git_code_pull') {
        git url: 'https://github.com/arghaya/locus-assignment1.git', branch: '**', credentialsId: '28e81a92-ece2-4b34-bfcf-edbbd30d6f3c'
    }
//     stage('code check') {
//         def scannerHome = tool 'sonar-scanner-4.2'
//         withSonarQubeEnv('sonar-server-7.7') {
//             for(int i=0;i<selectedProjects.size();i++){
//                 def currentProject = selectedProjects[i]
//                 sh """
//                     cd ${currentProject}
//                     ${scannerHome}/bin/sonar-scanner
//                 """
//             }
//         }
//     }
    stage('Build') {
        sh 'ls'
    }
    stage('Results') {
        sh 'pwd'
    }
    stage('Build Deploy Code') {
        if (env.BRANCH_NAME ==~ /(production)/) {
            sh 'echo "deploying production"'
        }
    }
    stage('postbuild_clean_up') {
        cleanWs()
    }
}
