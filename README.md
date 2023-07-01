# Laptop UPS Alert (LUPSA)

This playbook sets up your laptop to monitor if it's on AC power. If it switches to battery power it will send an alert.

Under the hood it simply checks the value of `/sys/class/power_supply/AC/online`:
<img width="359" alt="image" src="https://github.com/hedche/ansible-laptop-ups-alerts/assets/64991745/a10f6f6c-7fa4-4d4b-a533-880675b20ac1">

