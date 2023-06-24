# lego MQTT publisher/subscriber
Demostatres how securtity vulnerabilities materialize in the kinetic world, especially in thr IoT field.

# Application vulnerabilities
Often custom-deployed MQTT brokers are not secured against strong authentication/authorization mechanism. This is often seen in upper-layer LoRa security, where application layer security is not present in LoRa and LoRaWAN networks. It's not uncommon to see clear-text MQTT messages used over LoRa and LoRaWAN networks. In the field, I've seen 1. no authentication or authorization on MQTT broker and topics 2. no encryption on the transit data with TLS or mcrypt for payload encryption.

You should encrypt MQTT traffic with TLS 1.2. Considering on the processing cycles available on hardware, this may not always be possible. Because proper (v1.2) TLS implementation requires overhead for generating thecertificate, applying and verifying the validity and certificate chains.

# Uage
main_run.py runs on the Onion Omega

test_pub.py is the attacker publishing messages to the MQTT broker on the Onion Omega
