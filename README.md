# Tweet-automate
automation of tweets with Selenium

# Importing the necessary libraries

import selenium

from selenium import webdriver

from selenium.webdriver.common.by import By

from selenium.webdriver.common.keys import Keys

from selenium.webdriver.support import expected_conditions as EC

from selenium.webdriver.support.ui import WebDriverWait

import time


# Installation Chrome driver

PATH =  "C:\Program Files (x86)\chromedriver.exe"

driver=webdriver.Chrome(PATH)

wait=WebDriverWait(driver,30)


# Access the Twitter page 

twitt_home_page= 'https://twitter.com/'

driver.get(twitt_home_page)

driver.implicitly_wait(3)

driver.maximize_window()

# Sign In

sign_in=wait.until(EC.visibility_of_element_located((By.NAME,"text")))

sign_in.send_keys("input your user_name") 

time.sleep(2)

next_button= driver.find_element(By.XPATH,'//*[@id="layers"]/div[2]/div/div/div/div/div/div[2]/div[2]/div/div/div[2]/div[2]/div/div/div/div[6]/div')

time.sleep(3)

next_button.click()

passwd=driver.find_element(By.NAME,"password")

time.sleep(2)

passwd.send_keys("input your password")

login=driver.find_element(By.XPATH,"//*[@id='layers']/div[2]/div/div/div/div/div/div[2]/div[2]/div/div/div[2]/div[2]/div[2]/div/div[1]/div/div/div/div")

login.click()

# Add New Post
new_post=driver.find_element(By.CSS_SELECTOR,"br[data-text='true']")

time.sleep(4)

new_post.send_keys("Good morning to all! I hope today is a great day full of smiles, laughter, and blessings! Don’t hide the sunshine in you.")

tweet_button=driver.find_element(By.XPATH,'//*[@id="react-root"]/div/div/div[2]/main/div/div/div/div/div/div[2]/div/div[2]/div[1]/div/div/div/div[2]/div[3]/div/div/div[2]/div[3]/div/span/span')

tweet_button.click()

# Log out 
clique=driver.find_element(By.XPATH,'//*[@id="react-root"]/div/div/div[2]/header/div/div/div/div[2]/div/div/div/div/div[2]/div/div[2]/div/div/div[4]/div')

clique.click()

time.sleep(3)

se_deconnecter=driver.find_element(By.XPATH,'//*[@id="layers"]/div[2]/div/div/div[2]/div/div[2]/div/div/div/div/div/a[2]/div[1]/div')

se_deconnecter.click()

valider=driver.find_element(By.XPATH,'//*[@id="layers"]/div[2]/div/div/div/div/div/div[2]/div[2]/div[2]/div[1]/div')

valider.click()

print(driver.quit())


