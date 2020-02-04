node {
    checkout scm

    docker.withRegistry('https://registry.example.com', 'Dockerhub') {

        def customImage = docker.build("hello_node")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}
