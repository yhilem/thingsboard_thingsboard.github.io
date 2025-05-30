---
layout: docwithnav-edge
title: Edge Alarms
description: Edge Alarms Overview

push-to-edge:
    0:
        image: /images/edge/user-guide/manage-alarms/push-from-cloud-to-edge/0-device-profile-create-rule.png
        title: 'Log in to the <b>ThingsBoard Cloud</b> and go to the <b>Profiles > Device profiles</b> section to create or modify the Device profile. Select the appropriate <b>Default rule chain</b>. Then, configure the <b>Alarm Rule</b>.'
    1:
        image: /images/edge/user-guide/manage-alarms/push-from-cloud-to-edge/1-assign-the-profile.png
        title: 'Go to the <b>Entities > Devices</b> section. You can create a new <b>Device</b> or edit the existing one. On the <b>"Device details"</b> page, assign newly created (or updated) <b>Device profile</b> to this <b>Device</b>. Click the <b>“Apply changes”</b> button.'
    2:
        image: /images/edge/user-guide/manage-alarms/push-from-cloud-to-edge/2-assign-device-toEdge.png
        title: 'Go the <b>Edge management > Instances</b> section, select the <b>“Manage devices”</b> option and assign this device to the <b>Edge</b> instance.'
    3:
        image: /images/edge/user-guide/manage-alarms/push-from-cloud-to-edge/3-rule-chain-section.png
        title: 'Go to the <b>Rule Chains</b> section, to modify the <b>Rule Chain</b> you have assigned to the <b>Device profile</b>.'
    4:
        image: /images/edge/user-guide/manage-alarms/push-from-cloud-to-edge/4-push-node.png
        title: 'On the <b>Rule Chain</b> edit page, in the Node search bar find the <b>"push to edge"</b> node. It pushes messages from Cloud to Edge. Once message arrives to this node it will be converted into Edge event and saved to the local database. Drag and drop the node onto the <b>Rule Chain sheet</b>. Then, in the <b>"Add rule node"</b> pop-up window enter the node title and select the <b>"Server attributes"</b> option in the <b>"Entity attributes scope"</b> field. Click the <b>"Add"</b> button to proceed.'
    5:
        image: /images/edge/user-guide/manage-alarms/push-from-cloud-to-edge/5-select-link-labels.png
        title: 'Connect the <b>“device profile”</b> node to the <b>"push to edge"</b> node and set the <b>“Alarm Created”</b>, <b>“Alarm Updated”</b>, <b>“Alarm Severity Updated”</b>, and <b>“Alarm Cleared”</b> link labels. Click the <b>“Apply changes”</b> button in the <b>Rule Chain sheet</b>.'
    6:
        image: /images/edge/user-guide/manage-alarms/push-from-cloud-to-edge/6-telemetry.png
        title: 'To test if the rule and node are working, navigate to the <b>Entities > Devices</b> section, find your <b>Device</b> and open the <b>"Device details"</b> page. Click the <b>"Check connectivity"</b> button. Trigger the <b>Alarm Rule</b> by executing the corresponding command in the terminal.'
    7:
        image: /images/edge/user-guide/manage-alarms/push-from-cloud-to-edge/7-verify-alarm-on-cloud.png
        title: 'To verify the received Alarm notification, go to the <b>Entities > Devices</b> section, open the <b>"Device details"</b> page and select the <b>“Alarm”</b> tab. You also can view the incoming Alarm notification in the Notification center.'
    8:
        image: /images/edge/user-guide/manage-alarms/push-from-cloud-to-edge/8-verify-alarm-on-edge.png
        title: 'To verify that the notification is propagated to the <b>Edge</b>, log in to the <b>Edge</b> instance and go to the <b>Entities > Devices</b> section, open the <b>"Device details"</b> page and select the <b>“Alarm”</b> tab.'
    9:
        image: /images/edge/user-guide/manage-alarms/push-from-cloud-to-edge/9-acknowledge-clear.png
        title: 'Make sure to <b>Acknowledge</b> and <b>Clear</b> the notification after you received it. You can do it on either the <b>Cloud</b> or the <b>Edge</b>. If the <b>Uncleared Alarm</b> exists, it will be updated, instead of being created.'

push-to-cloud:
    0:
        image: /images/edge/user-guide/manage-alarms/push-from-edge-to-cloud/0-device-profile.png
        title: 'Log in to the <b>ThingsBoard Edge</b> and go to the <b>Profiles > Device profiles</b> section to create or edit the <b>Device profile</b>. Select the appropriate <b>Default rule chain</b>. Set the <b>Alarm Rule</b>.'
    1:
        image: /images/edge/user-guide/manage-alarms/push-from-edge-to-cloud/1-assign-profile.png
        title: 'Go to the <b>Entities > Devices</b> section. You can create a new device or edit the existing one. On the <b>"Device details"</b> page, assign newly created (or updated) <b>Device profile</b> to this device. Click the <b>“Apply changes”</b> button.'
    2:
        image: /images/edge/user-guide/manage-alarms/push-from-edge-to-cloud/2-rule-chain-template.png
        title: 'Log in to the <b>ThingsBoard Cloud</b> and go to the <b>Edge management > Rule chain templates</b> section to modify the <b>Rule Chain</b> you have assigned to the <b>Device profile</b>. <i>Note: If you use <b>Edge version 4.0</b>, you can proceed with <b>Rule Chain</b> configurations on the <b>Edge</b> instance.</i>'
    3:
        image: /images/edge/user-guide/manage-alarms/push-from-edge-to-cloud/3-push-to-cloud-settings.png
        title: 'On the <b>Rule Chain</b> edit page, in the Node search bar find the <b>"push to cloud"</b> node. It pushes messages from <b>Edge</b> to <b>Cloud</b>. Once message arrives to this node it will be converted into Cloud event and saved to the local database. Drag and drop the node onto the <b>Rule Chain sheet</b>. Then, in the <b>"Add rule node"</b> pop-up window enter the node title and select the <b>"Server attributes"</b> option in the <b>"Entity attributes scope"</b> field. Click the <b>"Add"</b> button to proceed.'
    4:
        image: /images/edge/user-guide/manage-alarms/push-from-edge-to-cloud/4-push-to-cloud-node.png
        title: 'Connect the <b>“device profile”</b> node to the <b>"push to edge"</b> node and set the <b>“Alarm Created”</b>, <b>“Alarm Updated”</b>, <b>“Alarm Severity Updated”</b>, and <b>“Alarm Cleared”</b> link labels. Click the <b>“Apply changes”</b> button in the <b>Rule Chain sheet</b>.'
    5:
        image: /images/edge/user-guide/manage-alarms/push-from-edge-to-cloud/5-send-telemetry-command.png
        title: 'To test if the rule and node are working, log in to your <b>Edge</b> instance and navigate to the <b>Entities > Devices</b> section. Find your device and open the <b>"Device details"</b> page. Click the <b>"Check connectivity"</b> button. Trigger the <b>Alarm Rule</b> by executing the corresponding command in the terminal.'
    6:
        image: /images/edge/user-guide/manage-alarms/push-from-edge-to-cloud/6-check-alarm-on-edge.png
        title: 'To verify the received alarm notification, go to the <b>Entities > Devices</b> section, open the <b>"Device details"</b> page and select the <b>“Alarm”</b> tab. You also can view the incoming alarm notification in the <b>Notification center</b>.'
    7:
        image: /images/edge/user-guide/manage-alarms/push-from-edge-to-cloud/7-check-alarm-on-cloud.png
        title: 'To verify that the notification is propagated to the <b>Cloud</b>, log in to the <b>ThingsBoard Cloud (Server)</b> and go to the <b>Entities > Devices</b> section, open the <b>"device details"</b> page and select the <b>“Alarm”</b> tab.'
    8:
        image: /images/edge/user-guide/manage-alarms/push-from-edge-to-cloud/8-acknowledge-clear.png
        title: 'Make sure to <b>Acknowledge</b> and <b>Clear</b> the notification after you received it. You can do it on either the <b>Cloud</b> or the <b>Edge</b>. If the <b>Uncleared Alarm</b> exists, it will be updated, instead of being created.'


---

{% assign docsPrefix = "edge/" %}
{% include docs/edge/user-guide/alarms.md %}