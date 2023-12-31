# Laptop UPS Alerts (LUPSA)

This playbook sets up your laptop to monitor if it's on AC power or not. Alerts can be sent a variety of ways.

### Is this for me?
If you answer yes to the following questions then it might be what you need:
1. Do you use a laptop in your homelab?
2. Does it have a battery?
3. Do you experience brownouts || blackouts?


### How it works
Under the hood it checks the value of `/sys/class/power_supply/AC/online`:

<img width="359" alt="image" src="https://github.com/hedche/ansible-laptop-ups-alerts/assets/64991745/a10f6f6c-7fa4-4d4b-a533-880675b20ac1">

If the value changes then an alert will be sent to the user.

### What it looks like in action
##### Logs
<img width="1452" alt="image" src="https://github.com/hedche/ansible-laptop-ups-alerts/assets/64991745/67b9f605-85b5-4ffa-a40d-6f7b351403e8">

##### WhatsApp
<img width="847" alt="image" src="https://github.com/hedche/ansible-laptop-ups-alerts/assets/64991745/e942ae9a-27d0-4619-9e23-193c9b2dbac7">


### WhatsApp notifications using CallMeBot (free + no sign up) [source](https://www.callmebot.com/blog/free-api-whatsapp-messages/)
1. Add the phone number +34 644 95 73 56 into your Phone Contacts. (Name it it as you wish)
2. Send this message "I allow callmebot to send me messages" to the new Contact created (using WhatsApp of course)
3. Wait until you receive the message "API Activated for your phone number. Your APIKEY is 123123" from the bot.
4. Edit the `inventory` file with your phone number and API Key that you got from step 3
5. Run the playbook against your laptop host
