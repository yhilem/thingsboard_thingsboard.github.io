---
layout: docwithnav-edge
title: Bidirectional Attribute Subscription And Update with Post-Processing
description: Bidirectional Attribute Subscription And Update with Post-Processing

routeMessagesToCloud:
    0:
        image: /images/edge/config/subscribe-to-attribute/1-rule-chain-templates.webp
        title: 'Log in to the <b>ThingsBoard Cloud</b> and go to the <b>Edge management > Rule chain templates</b> section and click on the <b>Rule chain</b> assigned to your <b>Edge instance.</b><ul><li>If you are using <b>Edge 4.0</b> or later, stay in your <b>Edge</b> instance and go to the <b>Rule chains</b> section. To edit a rule chain, click the appropriate <b>Rule Chain</b>.</li></ul>'
    1:
        image: /images/edge/config/subscribe-to-attribute/2-add-push-to-cloud.webp
        title: 'On the <b>Rule Chain</b> edit page, in the Node search bar find the <b>"push to cloud"</b> node. It pushes messages from Edge to Cloud. Drag and drop the node onto the <b>Rule Chain</b> sheet. Then, in the <b>"Add rule node"</b> pop-up window enter the node title and select the <b>"Client attributes"</b> option in the <b>"Entity attributes scope"</b> field. Click the <b>"Add"</b> button to proceed.'
    2:
        image: /images/edge/config/subscribe-to-attribute/3-save.webp
        title: 'Connect the <b>“save attributes”</b> and <b>“save time series”</b> nodes to the <b>"push to cloud"</b> node and set the <b>"Success"</b> link label. Click the <b>“Apply changes”</b> button on the <b>Rule Chain</b> sheet.'

backToEdge:
    0:
        image: /images/edge/config/subscribe-to-attribute/4-rule-chain.webp
        title: 'Go to the <b>Rule Chains</b> section, to modify the <b>Rule Chain.</b>'
    1:
        image: /images/edge/config/subscribe-to-attribute/5-add-script.webp
        title: 'On the <b>Rule Chain</b> edit page, in the Node search bar find the <b>"script"</b> node. It allows modification of message payload, metadata or message type with JavaScript. Drag and drop the node onto the <b>Rule Chain</b> sheet. Then, in the <b>"Add rule node: script"</b> pop-up window enter the node title and enter the script below. Click the <b>"Add"</b> button to proceed.'
    2:
        image: /images/edge/config/subscribe-to-attribute/5-add-push-to-edge.webp
        title: 'On the <b>Rule Chain</b> edit page, in the Node search bar find the <b>"push to edge"</b> node. It pushes messages from Cloud to Edge. Drag and drop the node onto the <b>Rule Chain</b> sheet. Then, in the <b>"Add rule node"</b> pop-up window enter the node title and select the <b>"Shared attributes"</b> option in the <b>"Entity attributes scope"</b> field. Click the <b>"Add"</b> button to proceed.'
    3:
        image: /images/edge/config/subscribe-to-attribute/6-save.webp
        title: 'Connect the <b>“save attributes”</b> and <b>“save time series”</b> nodes to the <b>"push to edge"</b> node and set the <b>"Success"</b> link label. Click the <b>“Apply changes”</b> button on the <b>Rule Chain</b> sheet.'

terminal:
    0:
        image: /images/edge/config/subscribe-to-attribute/10-subscribe-post-update-attributes-mqtt.webp
        title: 'Once you have subscribed to attribute updates, you will receive updates as the attributes change. We have used the <b>MQTT protocol</b> as an example. The updates were received after new attributes were published.'

checkResultOnDevice:
    0:
        image: /images/edge/config/subscribe-to-attribute/7-confirm-on-device-1.webp
        title: 'To confirm if the <b>client-side attributes</b> are received, go to the <b>Entities > Devices</b> section of your <b>Edge</b> and click on the <b>device</b>. On the <b>"Device details"</b> page, select the <b>"Attributes"</b> tab and select the <b>"Client attributes"</b> option in the <b>"Entity attributes scope"</b> drop-down menu.'

checkResultOnEdge:
    0:
        image: /images/edge/config/subscribe-to-attribute/8-confirm-on-edge-node-1.webp
        title: 'To confirm if the attributes message is received and pushed to Cloud, go to the <b>Rule chains</b> section of your Edge instance and click on the <b>Rule chain</b>. Click on the <b>"push to cloud"</b> node.'
    1:
        image: /images/edge/config/subscribe-to-attribute/8-confirm-on-edge-node-2.webp
        title: 'On the <b>"Push to cloud"</b> page, select the <b>"Events"</b> tab. If you have debug mode enabled, select the <b>"Debug"</b> option in the <b>"Event type"</b> drop-down menu. You should see the new records - <b>"IN"</b> and <b>"OUT"</b>, where the <b>"IN"</b> record defines the attributes received from the device, and the <b>"OUT"</b> record defines the attributes message pushed to the <b>Cloud</b>.'

checkResultOnCloud:
    0:
        image: /images/edge/config/subscribe-to-attribute/9-confirm-on-cloud-node-1.webp
        title: 'To confirm if the attributes message is received on the Cloud and pushed back to the Edge, go to the <b>Rule chains</b> section of your Cloud and click on the <b>Rule chain</b>. Click twice on the <b>"push to edge"</b> node.'
    1:
        image: /images/edge/config/subscribe-to-attribute/9-confirm-on-cloud-node-2.webp
        title: 'On the <b>"Push to edge"</b> page, select the <b>"Events"</b> tab. If you have debug mode enabled, select the <b>"Debug"</b> option from the <b>"Event type"</b> drop-down menu. You should see two new records - <b>"IN"</b> and <b>"OUT"</b>, where the <b>"IN"</b> record defines the attributes received from Edge, and the <b>"OUT"</b> record defines the attributes message pushed back to <b>Edge</b>.'

---
{% assign docsPrefix = "edge/" %}
{% include docs/edge/user-guide/config/subscribe-to-attribute.md %}