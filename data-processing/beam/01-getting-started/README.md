
### 핵심
- Pipeline 생성
- Transform을 Pipeline에 적용(데이터 전처리)
- Input에서 데이터 읽기
- ParDo Transform 실행
- Beam SDK가 제공하는 Transform(Count 등) 실행
- Output 저장하기
- Pipeline 실행하기


---


### Pipeline 생성
- `from apache_beam.options.pipeline_options import PipelineOptions
`을 사용해서 Option 정의

```python
from apache_beam.options.pipeline_options import PipelineOptions

input_file = 'gs://dataflow-samples/shakespeare/kinglear.txt'
output_path = 'gs://my-bucket/counts.txt'

beam_options = PipelineOptions(
    runner='DataflowRunner',
    project='my-project-id',
    job_name='unique-job-name',
    temp_location='gs://my-bucket/temp',
)
```

- `beam.Pipeline(options=beam_options`로 Pipeline 객체 생성

```python
pipeline = beam.Pipeline(options=beam_options)
```