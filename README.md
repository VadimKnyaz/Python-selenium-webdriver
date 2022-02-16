# Python-selenium-webdriver
from selenium import webdriver
import time

driver = webdriver.Chrome('./chromedriver')
driver.get('https://itcareer.pythonanywhere.com/')

# web_form = driver.find_element_by_class_name('form-group')
# print(web_form.get_attribute('innerHTML'))

time.sleep(2)

name_field = driver.find_element_by_id('name')
name_field.send_keys('Vadim')
time.sleep(1)

surname_field = driver.find_element_by_id('surname')
surname_field.send_keys('Itishnik')
time.sleep(1)

email_field = driver.find_element_by_id('email')
email_field.send_keys('VadimItishnik@gmail.com')
time.sleep(1)

password_field = driver.find_element_by_id('password')
password_field.send_keys('7777VVV')
time.sleep(1)

submit_button = driver.find_element_by_tag_name('button')
submit_button.click()

time.sleep(3)

driver.close()
