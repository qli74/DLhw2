# DLhw2-ParlAi
## Codes
1. fork ParlAI
```
git clone https://github.com/facebookresearch/ParlAI
cd ParlAI; python setup.py develop install
```
2. train model
```
python examples/train_model.py -t twitter -mf /tmp/tr_twitter_2 -m seq2se
q  -bs 8 -lr 0.00001 -ttim 111000 -stim 100 -bi True -att general -emb fasttext_cc -lfc True
```
3. fork AADeLucia's logger
```
git clone -b interactive-logger https://github.com/AADeLucia/ParlAI.git ~/my-parlai
cd ~/my-parlai; python setup.py develop
```
4. record chat logs of the trained model
```
python -m parlai.scripts.interactive -mf \tmp\tr_twitter_2 --save-world-logs True --report-filename mybot1.jsonl --world-logs-format forever
```
5. record chat logs of a ParlAI model in zoo
```
python -m parlai.scripts.interactive -mf zoo:convai2/kvmemnn/model --save-world-logs True --report-filename kvmemnn1.jsonl --world-logs-format forever

```
## ppl
valid:390.1

test:399.0
