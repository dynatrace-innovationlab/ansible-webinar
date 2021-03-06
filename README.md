# Webinar: Deployment Automation and Self-Healing with Dynatrace & Ansible

![ansible + dynatrace](./assets/ansible+dynatrace.jpg)

In this repo you will find resources that have been presented in the joint webinar between Dynatrace and Ansible on December 11, 2018.

Link to the original webinar registration:
https://www.ansible.com/resources/webinars-training/deployment-automation-and-self-healing-with-dynatrace-and-ansible

(Update Dec 17, 2018) The recording can be found here: https://www.ansible.com/resources/webinars-training/deployment-automation-and-self-healing-dynatrace-and-ansible

## Deployment Automation

With the Dynatrace OneAgent role from Ansible Galaxy you can deploy the Dynatrace OneAgent on hundreds of hosts within a couple of minutes.

Link: https://galaxy.ansible.com/dynatrace/oneagent 

Demo execution from you local machine:
```
$ ansible-playbook oneagent.yml -i inventory --private-key ansible-test.pem --become
```
(`--become` executes the role with root privileges)

## Self-healing applications with Ansible and Dynatrace

### Application

The application shown in the demo can be found in the `manifest-sockshop` folder.

### Load generation

A simple load generation script can be found in the `load-generation` folder.

### Playbooks

Playbooks used in the demo
- `remediation.yml`: generic remediation playbook that is called via the Ansible Tower problem notification integration from Dynatrace
- `campaign.yml`: playbook to control the release and configuration of a promotional campaign. 
- `comment.yml`: example playbook showcasing how to use the Dynatrace comment role to add comments to a Dynatrace problem ticket.

## Links & Resources

- Set up Ansible Tower with Dynatrace to enable your self-healing applications
https://www.dynatrace.com/news/blog/set-up-ansible-tower-with-dynatrace-to-enable-your-self-healing-applications/ 
- Self-healing: Ansible Tower fixes Dynatrace-detected problems in real time https://www.dynatrace.com/news/blog/self-healing-ansible-tower-fixes-dynatrace-detected-problems-in-real-time/ 
- Enable self-healing applications with Ansible and Dynatrace https://www.ansible.com/blog/enable-self-healing-applications-with-ansible-and-dynatrace (Ansible) or https://www.dynatrace.com/news/blog/enable-self-healing-applications-with-ansible-and-dynatrace/ (Dynatrace)
- Slides from the webinar: [slides.pdf](./assets/slides.pdf)
- Dynatrace roles in Ansible Galaxy
https://galaxy.ansible.com/dynatrace and 
https://galaxy.ansible.com/dynatrace_innovationlab 
- Dynatrace free trial 
http://dynatrace.com/trial 

![dynatrace trial](./assets/dynatrace-trial.png)
