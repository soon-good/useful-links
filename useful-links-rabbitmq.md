# Useful Link (RabbitMQ)

- [cloudamqp.com/blog/part1-rabbitmq-best-practice.html](https://www.cloudamqp.com/blog/part1-rabbitmq-best-practice.html)
  - RabbitMQ 운영시 실제 운영에 맞는 지침들을 설명하고 있다. 예를 들면 [Split your queues over different cores](https://www.cloudamqp.com/blog/part1-rabbitmq-best-practice.html#split-your-queues-over-different-cores) 섹션에서는 이렇게 설명하고 있다.
    - Queue performance is limited to one CPU core. You will, therefore, get better performance if you split your queues into different cores, and into different nodes, if you have a RabbitMQ cluster.
    - 이 말은 돌려 말하면 큐 하나에 코어 하나로 생각하고 설계하라는 이야기인 것 같다. 만약 카톡같은 채팅방 하나 하나를 모두 auto-delete 큐에 매칭 시키면, 래빗엠큐가 뻗는다.
    - 메시징 설계를 잘해서 필요한 곳에 큐를 사용하도록 설계해야 할 듯 하다.
  - 이 외에도 샤딩, Quorum Queue 사용, 레플리케이션 등등 운영에 필요한 각종 지침들을 언급하고 있다. 래빗엠큐를 직접 운영까지 가려면 단순히 호기로만 부딪히면 안되는 것 같다. 어느정도는 노련하게 천천히 스케일 업 해나가야 할 것 같다.

