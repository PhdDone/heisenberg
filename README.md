###How to deploy


####Start https server
sudo python SimpleHTTPSServer.py

####Start kaldi gstream server
python kaldigstserver/master_server.py --port=9004 --certfile=../heisenberg/cert.pem  --keyfile=../heisenberg/cert.pem

####Start kaldi gstream worker
python kaldigstserver/worker.py -u wss://localhost:9004/worker/ws/speech -c sample_worker.yaml

####Start ditection
open https://192.168.1.39/dictate/