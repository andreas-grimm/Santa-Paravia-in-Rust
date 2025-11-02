pipeline {
    agent { label 'rust' }
    stages {
        stage('Build') {
            steps {
                sh '/home/jenkins/.cargo/bin/cargo clean'
                sh '/home/jenkins/.cargo/bin/cargo build --release'
            }
        }
        stage('Deploy') {
            steps {
                sh 'cp /home/jenkins/workspace/Santa-Paravia-in-Rust/target/release/santa_paravia /import/sol/work/Jenkins-Builds/Rust/Santa-Paravia'
            }
        }
    }
}
