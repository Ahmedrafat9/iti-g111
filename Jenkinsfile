stages {
    stage ("verfiy Branch")
        stpes{
            echo "$GIT_BRANCH"
        }
    }

    stage("Docker Build")
        stpes {
                pwsh(script:"docker image -a")
                pwsh(script: """
                    cd 
                    docker images -a
                    docker build -t jenkins-pipeline .
                    docker images -a               
                    cd ..
                    """)

        }