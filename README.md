

Installation
      2.1 Prometheus 
           To install prometheus : 

           1. cd /directory

           2. wget https://github.com/prometheus/prometheus/releases/download/v2.31.1/prometheus-2.31.1.darwin-amd64.tar.gz

           3. tar -xvzf prometheus-2.31.1.darwin-amd64.tar.gz

      2.2 Alertmanager
           To install alertmanager : 

           1.  cd /directory

           2.  wget https://github.com/prometheus/alertmanager/releases/download/v0.23.0/alertmanager-0.23.0.darwin-amd64.tar.gz

           3. tar -xvzf alertmanager-0.23.0.darwin-amd64.tar.gz

Check AlertManager File Validation

        1 ./amtool check-config /path_to/alertmanager.yml

Check Prometheus File Validations

        1 ./promtool check rules /path_to/xyz_rules.yml

        2 ./promtool check config /path_to/prometheus.yml




To send alerts through alertmanager to slack channel, we already have pre-defined templates.

          1. cd to your prometheus folder and copy prometheus.yml and rules.yml from here.

          2. cd to your alertmanager folder and copy alertmanager.yml from here. Replace slack_api_url and channel fields with your credentials.

       Run prometheus and alertmanager using  ./prometheus --log.level=debug and ./alertmanager --log.level=debug respectively.

      Go to browser and check localhost:9090, localhost:9093 to confirm services running or not. 

      If running prooperly, in sometime - you will see Watchdog alert will be fired to your mentioned slack channel.

