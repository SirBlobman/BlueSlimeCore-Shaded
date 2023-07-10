pipeline {
    agent any

    options {
        githubProjectProperty(projectUrlStr: "https://github.com/SirBlobman/BlueSlimeCore-Shaded")
    }

    environment {
        MAVEN_DEPLOY = credentials('MAVEN_DEPLOY')
    }

    triggers {
        githubPush()
    }

    tools {
        jdk "JDK 17"
    }

    stages {
        stage("Gradle: Build") {
            steps {
                withGradle {
                    script {
                        sh("./gradlew --refresh-dependencies clean build")

                        if (env.BRANCH_NAME == "main") {
                            sh("./gradlew publish")
                        }

                        sh("./gradlew stop")
                    }
                }
            }
        }
    }

    post {
        success {
            archiveArtifacts artifacts: 'full/build/libs/BlueSlimeCore-NMS-full-*.jar', fingerprint: true
        }
    }
}
