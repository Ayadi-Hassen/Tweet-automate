# Tweet-automate
automation of tweets with Selenium

## Installation
git clone https://github.com/Ayadi-Hassen/Tweet-automate

cd Tweet-automate

npm install

## Usage
```python
sign_in=wait.until(EC.visibility_of_element_located((By.NAME,"text")))
sign_in.send_keys("input your user_name") 
passwd=driver.find_element(By.NAME,"password")
passwd.send_keys("input your password")


```

- sign_in : Twitter account username.
- passwd :  Twitter account password.

This will allow access to your twitter account. 

## Automate Post
This will allow to publish a tweet automatically. we have used different ways for example: By.CSS_SELECTOR, By.XPATH, By.NAME...   

```python
new_post=driver.find_element(By.CSS_SELECTOR,"br[data-text='true']")

time.sleep(4)

new_post.send_keys("Add your post")

tweet_button=driver.find_element(By.XPATH,'//[@id="reactroot"]/div/div/div[2]/main/div/div/div/div/div/div[2]/div/div[2]/div[1]/div/div/div/div[2]/div[3]/div/div/div[2]/div[3]/div/span/span')

tweet_button.click()

clique=driver.find_element(By.XPATH,'//*[@id="react-root"]/div/div/div[2]/header/div/div/div/div[2]/div/div/div/div/div[2]/div/div[2]/div/div/div[4]/div')

clique.click()


```

## Want to help 
If you like this application, please star this repository.

If you create an app using this application, please mention this repository.

If you want to contribute to this application, feel free to create a pull request

## Contact 

[LinkedIn](https://www.linkedin.com/in/hassen-ayadi-8534661ba/)



