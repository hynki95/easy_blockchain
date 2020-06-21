# easy_blockchain
문과생이 떠먹여주는 블록체인 실습 파일 입니다

# 지갑생성
    geth datadir. account new
비밀번호를 2번 입력합니다.(화면에는 원래 빈칸으로 출력 됨)

# 경로 설정
    cd ./walletexample

# 제네시스 블록 인식시키기
    geth --datadir . init .\genesis.json
이 과정을 거치면 geth 폴더가 생깁니다.

# geth 콘솔 들어가기
    geth --datadir . console

# 잔고 확인
    eth.accounts //전체 지갑 확인
    eth.accounts[0] //첫번째 지갑 확인
    eth.getBalance(eth.accounts[0]) //첫번째 지갑주소 잔고 확인

# 블록번호 확인
    eth.BlockNumber

# 채굴하기
    miner.start() //채굴 시작
    miner.stop() //채굴 중지

# 블록번호 및 잔고 확인
    eth.BlockNumber
    eth.getBalance(eth.accounts[0]) 

# 단위 변환
    web3.fromWei(1000000000000000000,"ether")//wei를 이더로 변환
    web3.toWei(1,"ether") //이더를 wei 단위로 변환
    web3.fromWei(eth.getBalance(eth.accounts[0),"ether")) //이더 단위로 잔고 변환해서 보기

