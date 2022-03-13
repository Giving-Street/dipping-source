## 소개
- Apache Beam은 배치, 실시간 데이터 처리 파이프라인을 정의할 수 있는 오픈소스
- Beam을 사용해서 Flink, Spark, Google Cloud Dataflow에 실행할 수 있음
- 선택 이유 : Beam 코드를 사용해 Dataflow에 올려본 경험은 많이 있는데, 더 체계적으로 알고 싶은 목적으로 선택했으며 대안과 차이를 비교해보고 싶었음(Spark, Kafka 등)


<br />

## 설치하기
- 가상 환경 생성(pyenv와 3.7.1은 설치되었다고 가정)

```
pyenv virtualenv 3.7.1 apache-beam
```

- 가상 환경 Activate

```
pyenv activate apache-beam
```


- 설치하기


```shell
pip3 install apache-beam
```


- 만약 GCP에서 사용하고 싶다면

```shell
pip3 install apache-beam[gcp]
```

- Sphinx를 사용해 Docs

```shell
pip3 install apache-beam[docs]
```

- Tests

```shell
pip3 install apache-beam[test]
```



## 대안
- [StackShare](https://stackshare.io/apache-beam/alternatives)에 따르면 Spark, Kafka, Airflow, Dataflow, Flink, Glue 등이 나옴
- 대안과의 비교
  - TBD


<br />

## 언제 사용하면 좋을지
- 배치, 실시간 데이터 처리를 하고 싶은 경우 사용
  - 배치 : 일회성?
  - 실시간 데이터 처리 : Spark Streaming과 비교
- Google Cloud Platform의 Dataflow Template을 사용하면 적은 코드로 사용할 수 있는 장점이 존재

<br />

## Reference
- [Learn Apache Beam In 30 Minutes - Apache Beam Tutorial For Beginners](https://youtu.be/waAwmY8xrgQ)
- [Beam Examples](https://github.com/apache/beam/tree/master/sdks/python/apache_beam/examples)


<br />

## 써본 후기



