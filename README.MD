# BERTģ�ʹ�ѵ��������ȫ����

Tag: BERT ѵ�� ����
## Ե��
��Ⱥ�￴������������ʹ��BERTģ�ͣ����϶�������ֻ�ᵽ��ģ�͵�ѵ��������������������𼰵��ò�û��˵����
���ʱ��ʹ��BERTģ������˴�����׼�������������ȫ���̣����������������������Ҳο���

�������ҽ���һ�����ֻ����۵���з��ࡱΪ���ӣ���Ҫ˵����ѵ���������ȫ�����̡�������ɺ����ʹ��һ����ҳ���н�����ʵʱ�ض���������������з����жϡ�

## �����ܹ�
�����ܹ�Ϊ��
```mermaid
graph LR
A(BERTģ�ͷ����) --> B(API�����)
B-->A
B --> C(Ӧ�ö�)
C-->B
```
�ܹ�˵����
**BERTģ�ͷ����**
	����ģ�ͣ�����ʵʱԤ��ķ���
    ʹ�õ��� BERT-BiLSTM-CRF-NER 

**API�����** 
	����ʵʱԤ�����ΪӦ���ṩAPI�ӿڵķ�����flask��д�� 

**Ӧ�ö�**
	���յ�Ӧ�öˣ�
	������ʹ��һ��HTML��ҳ��ʵ�֣�

��Ŀ����Դ���ַ��[BERT��ѵ��������gitԴ��](https://github.com/xmxoxo/BERT-train2deploy)

## �ؼ��ڵ�
��Ҫ�������¹ؼ��ڵ㣺
* ����׼��
* ģ��ѵ��
* ģ�͸�ʽת��
* ����˲���������
* API�����д�벿��
* �ͻ���(��ҳ�˵ı�д�벿��


## ����׼��
�����õ��������ֻ������ۣ����ݱȽϼ�,��������: -1,0,1 ��ʾ���棬�������������
���ݸ�ʽ���£�

```
1	�ֻ��ܺã�Ư��ʱ�У���Ʒһ��
1	�ֻ��ܺá���װҲ����������ƷҲ���յ��������Ͼͷ�����
1	��һ���ڵ���������ֻ� ��ʼ�ܵ��� ������һ������Ʒ ������
1	�ܲ��� ������ ϵͳ����
1	��֪����٣����ŵ�Ұ�
1	���ͦ��ģ���ҫ10�ָл��ǲ����ģ����˻����߻�����������ǰ������
1	���ܿ죬�ֻ����ָо��ܿᣬ��ɫ�ʺ�Ůʿ���ܾ��ޣ����ã������ٶȿ죬������
1	����һ��������ۣ��������ԣ�������
1	��Ӱ���ܺÿ������Ų�ϵ��ʱ��ʱ����ʱ�У��ٶȿ죬��������?����Ż���ģ�����?
1	����ٶȿ죬���ޣ��������µ����°档��װ�����������������ϲ����׻��䡣
0	�ֻ�������Ĥ�ñ������о�������Ĥ���������ܷ���
0	����һ��ʱ�䣬�����ֻ�����������������
0	����һ��
1	ͦ�õģ���һ�����ֻ��ܺã���ϲ��
0	�ֻ����У������ֻ��տ���ʱ��Ļ�ͱ����кܶ�ָ�ƺۼ����ֻ��Ǹ�**�ڵ���ĥ���Ƶģ��ü���ӡ�ӡ�Ҫ���ǿ����ܰ���Щ�ۼ������������˻��鷳���͸����ˡ��Ͳ��ܹ��ؾ�������ô�������͵Ķ���ʲô���������˶��ֻ�����һ�ȣ������ֻ�����Ĺ̶��ֻ���**�����ϵĶ���һ����ɫ������Ҳ��ͼƬ�����������������Ѿ�ע�ᣬ��֪����ô��������ģ�Ҫ���ͱ��ͻ������ͣ�Ҫ�����͹��ؾصģ���Ȼ��������˾��ò����������ûʲô��
-1	�ֻ����廹���ԣ�����Ҳ�������Ҳ������֧�ֻ�Ϊ����һ������Ϊ��ȱ�ݣ��͵Ķ����ǻ��ģ�����������̫�࣬��ҪһЩ�����������£��Ժ����ע��ϸ�ڣ�����������
0	ǰ�����ģ�  ���Ż��У� ָ�ƽ�����Ӧ������
1	�߶˴����ϵ��Ρ�
-1	��λС����ע������������û�еģ���Ҫ������
0	��۲������о��ܺĵ簡����ʹ�ö�ʱ������
1	�ֻ��ǳ��ã��ܺ���
-1	û�з�Ʊ��ͼƬ��ʵ�ﲻһ��
1	ϰ���ھ����ɹ���Ʒ�������ݣ���ʱ��Ʊ���б���������Ա����Ҳ���ܵ��������ֻ��յ�ʱû�е磬�о���������
1	�߶˴����ϵ��ΰ�������Ӱ����Ϸ���ƺ�ˬ����Ļ����

```

�����ܹ�8097������6:2:2�ı�����ֳ�train.tsv,test.tsv ,dev.tsv���������ļ�

## ģ��ѵ��
ѵ��ģ�;�ֱ��ʹ��BERT�ķ��෽������ԭ����`run_classifier.py` ���Ƴ������޸�Ϊ `run_mobile.py`������ѵ���Ĵ������Ϻܶ࣬�Ͳ�չ��˵���ˣ���Ҫ�����·�����

```python
#-----------------------------------------
#�ֻ�������з������ݴ��� 2019/3/12 
#labels: -1���� 0���� 1����
class SetimentProcessor(DataProcessor):
  def get_train_examples(self, data_dir):
    """See base class."""
    return self._create_examples(
        self._read_tsv(os.path.join(data_dir, "train.tsv")), "train")

  def get_dev_examples(self, data_dir):
    """See base class."""
    return self._create_examples(
        self._read_tsv(os.path.join(data_dir, "dev.tsv")), "dev")

  def get_test_examples(self, data_dir):
    """See base class."""
    return self._create_examples(
        self._read_tsv(os.path.join(data_dir, "test.tsv")), "test")

  def get_labels(self):
    """See base class."""

    """
    if not os.path.exists(os.path.join(FLAGS.output_dir, 'label_list.pkl')):
        with codecs.open(os.path.join(FLAGS.output_dir, 'label_list.pkl'), 'wb') as fd:
            pickle.dump(self.labels, fd)
    """
    return ["-1", "0", "1"]

  def _create_examples(self, lines, set_type):
    """Creates examples for the training and dev sets."""
    examples = []
    for (i, line) in enumerate(lines):
      if i == 0: 
        continue
      guid = "%s-%s" % (set_type, i)

      #debug (by xmxoxo)
      #print("read line: No.%d" % i)

      text_a = tokenization.convert_to_unicode(line[1])
      if set_type == "test":
        label = "0"
      else:
        label = tokenization.convert_to_unicode(line[0])
      examples.append(
          InputExample(guid=guid, text_a=text_a, label=label))
    return examples
#-----------------------------------------
```
Ȼ������һ��������

```python
  processors = {
      "cola": ColaProcessor,
      "mnli": MnliProcessor,
      "mrpc": MrpcProcessor,
      "xnli": XnliProcessor,
      "setiment": SetimentProcessor, #2019/3/27 add by Echo
  }
```

**�ر�˵��**��������һ��Ҫע�⣬�ں��ڲ����ʱ����Ҫһ��label2id���ֵ䣬����Ҫ��ѵ����ʱ��ͱ�����������`convert_single_example`�������������һ�Σ�

```python
  #--- save label2id.pkl ---
  #���������label2id.pkl , add by xmxoxo 2019/2/27
  output_label2id_file = os.path.join(FLAGS.output_dir, "label2id.pkl")
  if not os.path.exists(output_label2id_file):
    with open(output_label2id_file,'wb') as w:
      pickle.dump(label_map,w)

  #--- Add end ---
```

����ѵ����ͻ���������ļ��ˡ�

ʹ����������ѵ��ģ�ͣ�Ŀ¼��������ݸ��Ե�����޸ģ�

```shell
cd /mnt/sda1/transdat/bert-demo/bert/
export BERT_BASE_DIR=/mnt/sda1/transdat/bert-demo/bert/chinese_L-12_H-768_A-12
export GLUE_DIR=/mnt/sda1/transdat/bert-demo/bert/data
export TRAINED_CLASSIFIER=/mnt/sda1/transdat/bert-demo/bert/output
export EXP_NAME=mobile_0

sudo python run_mobile.py \
  --task_name=setiment \
  --do_train=true \
  --do_eval=true \
  --data_dir=$GLUE_DIR/$EXP_NAME \
  --vocab_file=$BERT_BASE_DIR/vocab.txt \
  --bert_config_file=$BERT_BASE_DIR/bert_config.json \
  --init_checkpoint=$BERT_BASE_DIR/bert_model.ckpt \
  --max_seq_length=128 \
  --train_batch_size=32 \
  --learning_rate=2e-5 \
  --num_train_epochs=5.0 \
  --output_dir=$TRAINED_CLASSIFIER/$EXP_NAME
```
�������ݱȽ�С��ѵ���ǱȽϿ�ģ�ѵ����ɺ󣬿��������Ŀ¼�õ�ģ���ļ��������ģ���ļ���ʽ��.ckpt�ġ�
ѵ�������
```
eval_accuracy = 0.861643
eval_f1 = 0.9536328
eval_loss = 0.56324786
eval_precision = 0.9491279
eval_recall = 0.9581805
global_step = 759
loss = 0.5615213

```

����ʹ���������������Ԥ�⣺

```shell
sudo python run_mobile.py \
  --task_name=setiment \
  --do_predict=true \
  --data_dir=$GLUE_DIR/$EXP_NAME \
  --vocab_file=$BERT_BASE_DIR/vocab.txt \
  --bert_config_file=$BERT_BASE_DIR/bert_config.json \
  --init_checkpoint=$TRAINED_CLASSIFIER/$EXP_NAME \
  --max_seq_length=128 \
  --output_dir=$TRAINED_CLASSIFIER/$EXP_NAME

```


## ģ�͸�ʽת��

����ģ�ͷ����ʹ�õ���.pb��ʽ��ģ���ļ���������Ҫ�����ɵ�ckpt��ʽģ���ļ�ת����.pb��ʽ��ģ���ļ���
�������ṩ��һ��ת������:`freeze_graph.py`��ʹ�����£�

```shell
usage: freeze_graph.py [-h] -bert_model_dir BERT_MODEL_DIR -model_dir
                       MODEL_DIR [-model_pb_dir MODEL_PB_DIR]
                       [-max_seq_len MAX_SEQ_LEN] [-num_labels NUM_LABELS]
                       [-verbose]
```

����Ҫע��Ĳ����ǣ�

* `model_dir` ����ѵ���õ�.ckpt�ļ����ڵ�Ŀ¼
* `max_seq_len` Ҫ��ԭ��һ�£�
* `num_labels` �Ƿ����ǩ�ĸ���,��������3��


```shell
python freeze_graph.py \
    -bert_model_dir $BERT_BASE_DIR \
    -model_dir $TRAINED_CLASSIFIER/$EXP_NAME \
    -max_seq_len 128 \
    -num_labels 3

```

ִ�гɹ�����Կ�����`model_dir`Ŀ¼������һ��`classification_model.pb` �ļ���

## ����˲���������

���ڿ��԰�װ������ˣ�ʹ�õ��� BERT-BiLSTM-CRF-NER����Ŀ��ַ��[https://github.com/macanv/BERT-BiLSTM-CRF-NER](https://github.com/macanv/BERT-BiLSTM-CRF-NER)

���ش��벢��װ ��

```shell
cd O:\��Դϵͳ\NLP\
git clone https://github.com/macanv/BERT-BiLSTM-CRF-NER
cd BERT-BiLSTM-CRF-NER
py setup.py install
```

��װ������з���ͬʱָ������ HTTP 8091�˿ڣ���ʹ��GPU 1���ܣ�

```shell
cd /mnt/sda1/transdat/bert-demo/bert/bert_svr

export BERT_BASE_DIR=/mnt/sda1/transdat/bert-demo/bert/chinese_L-12_H-768_A-12
export TRAINED_CLASSIFIER=/mnt/sda1/transdat/bert-demo/bert/output
export EXP_NAME=mobile_0

bert-base-serving-start \
    -model_dir $TRAINED_CLASSIFIER/$EXP_NAME \
    -bert_model_dir $BERT_BASE_DIR \
    -model_pb_dir $TRAINED_CLASSIFIER/$EXP_NAME \
    -mode CLASS \
    -max_seq_len 128 \
    -http_port 8091 \
    -port 5575 \
    -port_out 5576 \
    -device_map 1 
```
**ע��**��port �� port_out ������������API���õĶ˿ںţ�
Ĭ����5555��5556,�����׼��������ģ�ͷ�����һ��Ҫָ���Լ��Ķ˿ںţ������ͻ��
�������Ǹ�Ϊ�� 5575 �� 5576

�������û������������������Щģ��ûװ��,���� bert_base/server/http.py�����õģ�װ�Ͼͺ��ˣ�

```
sudo pip install flask 
sudo pip install flask_compress
sudo pip install flask_cors
sudo pip install flask_json
```

�������������2��GTX 1080 Ti�����ʱ��˫�����������ڷ��ӳ����ˣ�GPU 1����Ԥ�⣬GPU 0�����Լ���ѵ��ģ�͡�

���з������Զ����ɺܶ���ʱ��Ŀ¼���ļ���Ϊ�˷���������������ɽ���һ������Ŀ¼��������������д��һ��shell�ű���
���ﴴ������`mobile_svr\bertsvr.sh` ���������ԱȽϷ�������÷���������ʱ�Զ�������������������ÿ������ʱ�Զ������ʱ�ļ�

�������£�

```shell
#!/bin/bash
#chkconfig: 2345 80 90
#description: ����BERT����ģ�� 

echo '�������� BERT mobile svr...'
cd /mnt/sda1/transdat/bert-demo/bert/mobile_svr
sudo rm -rf tmp*

export BERT_BASE_DIR=/mnt/sda1/transdat/bert-demo/bert/chinese_L-12_H-768_A-12
export TRAINED_CLASSIFIER=/mnt/sda1/transdat/bert-demo/bert/output
export EXP_NAME=mobile_0

bert-base-serving-start \
    -model_dir $TRAINED_CLASSIFIER/$EXP_NAME \
    -bert_model_dir $BERT_BASE_DIR \
    -model_pb_dir $TRAINED_CLASSIFIER/$EXP_NAME \
    -mode CLASS \
    -max_seq_len 128 \
    -http_port 8091 \
    -port 5575 \
    -port_out 5576 \
    -device_map 1 

```

### �˿ڲ���

����ʹ��curl����������һ��

```

curl -X POST http://192.168.15.111:8091/encode \
  -H 'content-type: application/json' \
  -d '{"id": 111,"texts": ["�ܵ���˵������ֻ��Լ۱����ر�ߵġ�","�۸���ۺ���񣡣�������ۿ�"], "is_tokenized": false}'

```

ִ�н����
```
>   -H 'content-type: application/json' \
>   -d '{"id": 111,"texts": ["�ܵ���˵������ֻ��Լ۱����ر�ߵġ�","�۸���ۺ���񣡣�������ۿ�"], "is_tokenized": false}'
{"id":111,"result":[{"pred_label":["1","-1"],"score":[0.9974544644355774,0.9961422085762024]}],"status":200}

```
���Կ�����Ӧ���������ۣ�Ԥ����һ����1����һ����-1��������ٶȻ��Ƿǳ��ܿ�ġ�
ͨ�����ַ�ʽ�����û��ǲ�̫���㣬֪�������ͨѶ��ʽ�����ǿ�����flask��дһ��API����Ϊ���е�Ӧ��ͳһ�ṩ����


## API�����д�벿��
δ�����...

## �ͻ���(��ҳ�˵ı�д�벿��
δ�����...
