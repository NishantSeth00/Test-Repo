pipeline {
  agent any

  stages {
    stage('Clone Repository') {
      steps {
        git branch: "main", url: "https://github.com/NishantSeth00/Test-Repo.git"
      }
    }

    stage('Publish HTML') {
      steps {
        publishHTML(
          target: [
            reportName: "Rendered HTML Page",
            reportDir: ".",
            reportFiles: "hello.html",   // <-- fixed key
            keepAll: true,
            alwaysLinkToLastBuild: true,
            allowMissing: false
          ]
        )
      }
    }
  }
}
