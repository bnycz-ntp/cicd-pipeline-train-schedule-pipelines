node ('node-1') {
    try {
        docker.withRegistry('https://hub.docker.com/', 'docker-login') {
            
            stage (Deploy-nginx) {
                def nginx = docker.image('nginx:latest')
                nginx.pull()
        }
    }
    catch (e) {
        currentBuild.result = 'FAILED'
        throw e
    }
}