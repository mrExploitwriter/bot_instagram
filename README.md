# ❤️In the name of Allah❤️
# bot_instagram
Bot follwo instagarm!!

# Attention:
If it does not run, download its web driver from the link below and hug it because it is needed to open sites.
link https://github.com/mozilla/geckodriver/releases

# Warning!
❌Responsible for using this bot. It's yours and I do not accept anything❌
# Description
In the name of Allah

A hot Instagram bot that takes your username and password and the idea of ​​the person you want to enter, then opens Firefox and Lu Gain and then follows

how's it?

# code:
    from selenium import webdriver
    import time
    import os
    from colorama import Fore, init
    import sys


    close = lambda: os.system('cls')
    close()

    print(Fore.GREEN,"""----𝑰𝒏 𝒕𝒉𝒆 𝒏𝒂𝒎𝒆 𝒐𝒇 𝑨𝒍𝒍𝒂𝒉❤️----""")
    print("""\n _         _                              _         _   
     (_)_ _  __| |_ __ _ __ _ _ _ __ _ _ __   | |__  ___| |_ 
     | | ' \(_-<  _/ _` / _` | '_/ _` | '  \  | '_ \/ _ \  _|
     |_|_||_/__/\__\__,_\__, |_| \__,_|_|_|_| |_.__/\___/\__|
      / _|___| | |_____ |___/                                
     |  _/ _ \ | / _ \ V  V /                                
     |_| \___/_|_\___/\_/\_/""")

    print(Fore.BLUE,"""\n [01] Start!
     [00] exit()""")

    while True:
            key = input(Fore.RED+"\n{X_X} :>> ")

            if key == "01":
                    usr = input(Fore.BLUE+"\nPlease You r User (email, number): ")
                    paswd = input(Fore.CYAN+"Ok You password ? ")
                    fllow_list = input(Fore.YELLOW+"You r id accont the follow(id1,1d2,...) #")
                    follow = fllow_list.split(',')

                  time.sleep(2)
                  print(Fore.WHITE,"to instagram ...")

                web = webdriver.Firefox()

                #----------------------------------------------------------------------
                #start bot!
                try:
                        web.get('https://www.instagram.com/accounts/login/')

                        user_name = web.find_element_by_xpath('/html/body/div[1]/section/main/article/div[2]/div[1]/div/form/div/div[1]/div/label/input')
                        user_name.send_keys(usr)
                        time.sleep(3)

                        password = web.find_element_by_xpath('/html/body/div[1]/section/main/article/div[2]/div[1]/div/form/div/div[2]/div/label/input')
                        password.send_keys(paswd)
                        time.sleep(4)

                        login = web.find_element_by_xpath('/html/body/div[1]/section/main/article/div[2]/div[1]/div/form/div/div[3]/button')
                        login.click()
                        time.sleep(29)
                        for i in follow:
                                web.get(f"https://www.instagram.com/{i}/")
                                time.sleep(9)

                                follow = web.find_element_by_xpath('/html/body/div[1]/section/main/div/header/section/div[1]/div[1]/div/div/div/span/span[1]/button').click()
                                time.sleep(4)
                                web.close()
                except:
                        print(Fore.RED,"eror followe !")

        elif key == "00":
                print(Fore.CYAN,"\nGod by 👋")
                sys.exit()
      
        else: 
             print(Fore.RED,"\neror: whats? not comand! ")
             print(Fore.YELLOW,"try agin.")

