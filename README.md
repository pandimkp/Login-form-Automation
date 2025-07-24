# Login-form-Automation

Login form Automation in Python with Selenium
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.common.keys import Keys

driver = webdriver.Chrome()
driver.get("https://www.google.com/")
search_box = driver.find_element(By.NAME, "q")
search_box.send_keys("Automation Selenium")
search_box.send_keys(Keys.RETURN)

assert "Automation" in driver.title
driver.quit()
