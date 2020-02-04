node {
    checkout scm
    def customImage = docker.build("hello-node_js")
    customImage.push()

    customImage.push('latest')
}
