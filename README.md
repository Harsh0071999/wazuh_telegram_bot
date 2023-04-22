# wazuh_telegram_bot
Send alert in telegram from wazuh


# use the setp provided here for fetch the log from wazuh to telegram.
Step 1: open telegram

Step 2: search for Bot Father AI in telegram.

Step 3: Start the bot (just click start).

Step 4: right /newbot for creat a new bot for your wazuh integration.

Step 5: Give the name for bot.

Step 6: Provide the name for username with bot at last of the username.

Step 7: Copy and save the API token for furthr work.

Step 8: Open the me.bot after creating the bot.

Step 9: Start the conversiation.

Step 10: Create a new group for bot and provide the group name.

Step 11: Now open the Telegram Bot Raw Ai #https://t.me/RawDataBot or use these link #https://codesandbox.io/s/get-telegram-chat-id-q3qkk?from-embed or use these url #https://api.telegram.org/bot<YourBOTToken>/getUpdates

Step 12: Paste the token in it after starting the conversion.

Step 13: Now move back to server.

Step 14: nano /var/ossec/integrations/custom-telegram

Step 15: paste the file name custom-telegram and custom-telegram.py from git repo.

Step 16: save and close the file.

Step 17: nano /var/ossec/integrations/custom-telegram.py

Step 18: save and close.

Step 19: change the permission of both the file.

Step 20: chown root:wazuh /var/ossec/integrations/custom-telegram*

Step 21: chmod 750 /var/ossec/integrations/custom-telegram*

Step 22: open the ossec.conf # nano /var/ossec/etc/ossec.conf

Step 23: upload the followwing command

        <integration>
            <name>custom-telegram</name>
            <level>3</level>
            <hook_url>https://api.telegram.org/bot*YOUR API KEY*/sendMessage</hook_url>
            <alert_format>json</alert_format>
        </integration>
Step 24: Restart the wazuh-manager # systemctl restart wazuh-manager.



## Acknowledgements

 - [OpenSecureCo](https://github.com/OpenSecureCo/Demos/blob/main/Telegram%20Integration)
 - [BotFather](https://telegram.me/BotFather)
 - [ChatID](https://sean-bradley.medium.com/get-telegram-chat-id-80b575520659)
 - [RawDataBot](https://t.me/RawDataBot)


## Authors

- [@harsh0071999](https://github.com/Harsh0071999)

