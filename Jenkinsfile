node("") {
    stage("build") {
        git("https://github.com/lxbrllnt/jenkinsrepo.git")
        sh("./mvn package")
    }
    stage("deploy") {
        echo("Deploying the artifact")
    }
    stage("results") {
        junit("**/target/surefire-reports/TEST-*.xml")
        archive("target/*.jar")
    }
}
