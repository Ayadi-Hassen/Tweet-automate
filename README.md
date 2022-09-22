# Tweet-automate
automation of tweets with Selenium

## Installation
git clone https://github.com/Ayadi-Hassen/Tweet-automate

cd Tweet-automate

npm install

## Usage
sign_in=wait.until(EC.visibility_of_element_located((By.NAME,"text")))
sign_in.send_keys("input your user_name") 
passwd=driver.find_element(By.NAME,"password")
passwd.send_keys("input your password")

- sign_in : Twitter account username.
- passwd :  Twitter account password.

## Automate Post 
new_post=driver.find_element(By.CSS_SELECTOR,"br[data-text='true']")

time.sleep(4)

new_post.send_keys("Add your post")

tweet_button=driver.find_element(By.XPATH,'//[@id="reactroot"]/div/div/div[2]/main/div/div/div/div/div/div[2]/div/div[2]/div[1]/div/div/div/div[2]/div[3]/div/div/div[2]/div[3]/div/span/span')

tweet_button.click()

clique=driver.find_element(By.XPATH,'//*[@id="react-root"]/div/div/div[2]/header/div/div/div/div[2]/div/div/div/div/div[2]/div/div[2]/div/div/div[4]/div')

clique.click()

