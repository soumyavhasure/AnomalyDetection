- Using quix because it has:
  - Stateful operations (anytime system restarts, it continues from where it stopped last time)
  - Exactly once processing (no need to worry about multiple reprocessing about same data)
  - Data sink (can write to custom data sinks -- Elastic Search, etc)
  - Pure Python (code is easy to understand and integrate with other systems)
- We will have a separate application that will scale up or down however you want
  - Producer that is separate from the anomaly detection engine
    - If you need to produce heavy compute, increase compute power of producer
    - If you need to crunch a lot of data, increase compute power of anomaly detection engine
    