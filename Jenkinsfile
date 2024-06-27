pipeline {
    agent {
        label 'nu-checker'
    }
    stages {
        stage('run scan') {
            steps {
                // Your build steps here
                container('nu-checker') {
                  sh """cat <<EOF > file.html
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>

</body>
</html>
EOF
"""
                  sh 'vnu-runtime-image/bin/vnu file.html'
                }
            }
        }

    }
}