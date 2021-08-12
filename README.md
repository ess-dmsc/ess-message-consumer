# ESS command-line message consumer
  - Kafka commandline message consumer specific to handle ESS flatbuffer messages
    of types

    |name|description|
    |----|-----------|
    |pl72|Run start|
    |6s4t|Run stop|
    |f142|Log data|
    |ev42|Event data|
    |x5f2|Status messages|
    |answ|File-writer command response|
    |wrdn|File-writer finished writing|
Installing
==========

`ess_message_consumer`

Create virtual environment with Python 3.6 or later:

    git clone https://github.com/ebadkamil/ess-message-consumer.git
    cd ess-message-consumer
    python3 -m venev {env_name}

Activate virtual environment and install `ess-message-consumer`:

    source {env_name}/bin/activate
    pip install .

Usage:

- Start consuming ESS flatbuffer messages from given topics

        start_consumer -b {broker_address} -t {topics_to_consume_msg_from} --rich_console
        broker_address: for eg. "localhost:9092"
        topics_to_consume_msg_from: "topic_1, topic_2, ..."
        rich_console: optional for rich layout console.

- List all available topics on a broker

        list_topics -b {broker_address}