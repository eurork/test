node {
    stage('Build') {
        sh 'echo "rozpoczynam budowanie . . ."'
        sh 'sleep 1'
        sh 'touch plik2.py plik3.rpm plik4.rpm'
        writeFile file: 'plik.sh', text: 'echo "kod w pliku sh. \n 9 \n 8 \n 7 \n 6 \n 5 \n 4\n 3 \n 2 \n 1 \n koniec kodu."'
        sh 'sleep 1'
        sh 'echo "koniec budowania."'
    }
    stage('Install') {
        sh 'echo "rozpoczynam instalacje . . ."'
        sh 'sleep 1'
        sh 'bash ./plik.sh'
        sh 'sleep 1'
        sh 'ls -al'
        sh 'echo "Instalacja zakonczona prawidlowo."'
    }
    stage('Deploy') {
        sh 'echo "rozpoczynam deploy . . ."'
        sh 'sleep 1'
        sh 'rm plik.sh plik2.py plik3.rpm plik4.rpm'
        sh 'sleep 1'
        sh 'ls -al'
        sh 'echo "Deploy zakonczony prawidlowo"'
    }
}
