# Sequential Recommendation

- **Dataset**: [Yelp](../../md/yelp_seq.md)

- **Model**: [NARM](https://recbole.io/docs/user_guide/model/sequential/narm.html)

- **Hyper-parameter searching** (hyper.test):

  ```yaml
  learning_rate choice [0.005,0.001,0.0005,0.0001]
  n_layers choice [1,2]
  ```

- **Best parameters**:

  ```yaml
  learning_rate: 0.005
  n_layers: 1
  ```

- **Hyper-parameter logging** (hyper.result):

  ```yaml
  learning_rate:0.001, n_layers:1
  Valid result:
  recall@10 : 0.0681    mrr@10 : 0.0239    ndcg@10 : 0.0341    hit@10 : 0.0681    precision@10 : 0.0068
  Test result:
  recall@10 : 0.0631    mrr@10 : 0.0222    ndcg@10 : 0.0316    hit@10 : 0.0631    precision@10 : 0.0063

  learning_rate:0.0005, n_layers:1
  Valid result:
  recall@10 : 0.0682    mrr@10 : 0.0242    ndcg@10 : 0.0343    hit@10 : 0.0682    precision@10 : 0.0068
  Test result:
  recall@10 : 0.0625    mrr@10 : 0.0218    ndcg@10 : 0.0312    hit@10 : 0.0625    precision@10 : 0.0062

  learning_rate:0.005, n_layers:1
  Valid result:
  recall@10 : 0.0697    mrr@10 : 0.0246    ndcg@10 : 0.035    hit@10 : 0.0697    precision@10 : 0.007
  Test result:
  recall@10 : 0.0654    mrr@10 : 0.0236    ndcg@10 : 0.0333    hit@10 : 0.0654    precision@10 : 0.0065

  learning_rate:0.005, n_layers:2
  Valid result:
  recall@10 : 0.0701    mrr@10 : 0.0245    ndcg@10 : 0.035    hit@10 : 0.0701    precision@10 : 0.007
  Test result:
  recall@10 : 0.0645    mrr@10 : 0.0228    ndcg@10 : 0.0324    hit@10 : 0.0645    precision@10 : 0.0064

  learning_rate:0.0001, n_layers:2
  Valid result:
  recall@10 : 0.0623    mrr@10 : 0.0215    ndcg@10 : 0.0309    hit@10 : 0.0623    precision@10 : 0.0062
  Test result:
  recall@10 : 0.0577    mrr@10 : 0.0206    ndcg@10 : 0.0292    hit@10 : 0.0577    precision@10 : 0.0058

  learning_rate:0.0001, n_layers:1
  Valid result:
  recall@10 : 0.0658    mrr@10 : 0.023    ndcg@10 : 0.0329    hit@10 : 0.0658    precision@10 : 0.0066
  Test result:
  recall@10 : 0.0595    mrr@10 : 0.0211    ndcg@10 : 0.03    hit@10 : 0.0595    precision@10 : 0.0059

  learning_rate:0.001, n_layers:2
  Valid result:
  recall@10 : 0.0673    mrr@10 : 0.0232    ndcg@10 : 0.0334    hit@10 : 0.0673    precision@10 : 0.0067
  Test result:
  recall@10 : 0.0609    mrr@10 : 0.0219    ndcg@10 : 0.0309    hit@10 : 0.0609    precision@10 : 0.0061

  learning_rate:0.0005, n_layers:2
  Valid result:
  recall@10 : 0.0665    mrr@10 : 0.0234    ndcg@10 : 0.0334    hit@10 : 0.0665    precision@10 : 0.0067
  Test result:
  recall@10 : 0.0612    mrr@10 : 0.0215    ndcg@10 : 0.0306    hit@10 : 0.0612    precision@10 : 0.0061
  ```

- **Logging Result**:

  ```yaml
  best params:  {'learning_rate': 0.005, 'n_layers': 1}
  best result:
  {'model': 'NARM', 'best_valid_score': 0.035, 'valid_score_bigger': True, 'best_valid_result': OrderedDict([('recall@10', 0.0697), ('mrr@10', 0.0246), ('ndcg@10', 0.035), ('hit@10', 0.0697), ('precision@10', 0.007)]), 'test_result': OrderedDict([('recall@10', 0.0654), ('mrr@10', 0.0236), ('ndcg@10', 0.0333), ('hit@10', 0.0654), ('precision@10', 0.0065)])}
```
