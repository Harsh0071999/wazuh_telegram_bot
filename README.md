# wazuh_telegram_bot
Send alert in telegram from wazuh


# use the setp provided here for fetch the log from wazuh to telegram.
<br>
Step 1: open telegram <br>
Step 2: search for Bot Father AI in telegram .<br>
Step 3: Start the bot (just click start)<br>
Step 4: right /newbot for creat a new bot for your wazuh integration.<br>
Step 5: Give the name for bot.<br>
Step 6: Provide the name for username with bot at last of the username.<br>
Step 7: Copy and save the API token for furthr work.<br>
Step 8: Open the me.bot after creating the bot.<br>
Step 9: Start the conversiation.<br>
Step 10: Create a new group for bot and provide the group name.<br>
Step 11: Now open the Telegram Bot Raw Ai #https://t.me/RawDataBot or use these link #https://codesandbox.io/s/get-telegram-chat-id-q3qkk?from-embed or use these url #https://api.telegram.org/bot<YourBOTToken>/getUpdates<br>
Step 12: Paste the token in it after starting the conversion.<br>
Step 13: Now move back to server.<br>
Step 14: nano /var/ossec/integrations/custom-telegram<br>
Step 15: paste the file name custom-telegram.<br>
Step 16: save and close the file.<br>
Step 17: nano /var/ossec/integrations/custom-telegram.py<br>
Step 18: save and close.<br>
Step 19: change the permission of both the file.<br>
Step 20: chown root:wazuh /var/ossec/integrations/custom-telegram*<br>
Step 21: chmod 750 /var/osseec/integrations/custom-integration*<br>
Step 22: open the ossec.conf # nano /var/ossec/etc/ossec.conf<br>
Step 23: upload the followwing command<br>
    <integration>
        <name>custom-telegram</name>
        <level>3</level>
        <hook_url>https://api.telegram.org/bot *your_Bot_id_token_id*/sendMessage</hook_url>
        <alert_format>json</alert_format>
    </integration>
Step 24: Restart the wazuh-manager # systemctl restart wazuh-manager.
