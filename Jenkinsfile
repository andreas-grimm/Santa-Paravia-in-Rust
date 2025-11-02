pipeline {
    agent { label 'rust' }
    stages {
        stage('Build') {
            steps {
                sh 'cargo clean'
                sh 'cargo build --release'
            }
        }
        stage('Deploy') {
            steps {
                sh 'cp /home/jenkins/workspace/Santa-Paravia-in-Rust/target/release/santa_paravia /import/sol/work/Jenkins-Builds/Rust/Santa-Paravia'
            }
        }
    }
}
