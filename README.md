"# RetoT-cnico" 
package EducacionIT;
import static org.junit.Assert.*;

import java.util.concurrent.TimeUnit;

import org.junit.*;

import org.openqa.selenium.*;

import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.firefox.FirefoxDriver;

public class laboratorio1 {
	
	@Test
	public void lab1_E2() {
		System.setProperty("webdriver.gecko.driver", "..\\EducacionIT\\Driver\\geckodriver.exe");
		
		WebDriver driver=new FirefoxDriver();
		
		driver.get("https://opensource-demo.orangehrmlive.com/web/index.php/recruitment/viewCandidates");
		
		driver.manage().window().maximize();
		
		WebElement txtUsername=driver.findElement(By.name("username"));
		txtUsername.sendKeys("Admin");
		
		WebElement txtPassword=driver.findElement(By.name("password"));
		txtPassword.sendKeys("admin123");
		
		WebElement btnLogin = driver.findElement(By.cssSelector("#app > div.orangehrm-login-layout > div > div.orangehrm-login-container > div > div.orangehrm-login-slot > div.orangehrm-login-form > form > div.oxd-form-actions.orangehrm-login-action > button"));
		btnLogin.click();
		
		driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);
		
		WebElement elementoAdd = driver.findElement(By.xpath("//button[@class=\"oxd-button oxd-button--medium oxd-button--secondary\"]"));
        elementoAdd.click();
        
		WebElement txtFirstname = driver.findElement(By.name("firstName"));
		txtFirstname.sendKeys("Test");
		
		WebElement txtMiddlename = driver.findElement(By.name("middleName"));
		txtMiddlename.sendKeys("Alexander");
		
		WebElement txtLastname = driver.findElement(By.name("lastName"));
		txtLastname.sendKeys("Romero");
		
		WebElement txtEmail = driver.findElement(By.xpath("//*[@id=\"app\"]/div[1]/div[2]/div[2]/div/div/form/div[3]/div/div[1]/div/div[2]/input"));
		txtEmail.sendKeys("romeropruebatest@gmail.com");
		
		WebElement txtContactnumber = driver.findElement(By.xpath("//*[@id=\"app\"]/div[1]/div[2]/div[2]/div/div/form/div[3]/div/div[2]/div/div[2]/input"));
		txtContactnumber.sendKeys("3203358896");
		
		WebElement txtKeywords = driver.findElement(By.xpath("//*[@id=\"app\"]/div[1]/div[2]/div[2]/div/div/form/div[5]/div/div[1]/div/div[2]/input"));
		txtKeywords.sendKeys("Prueba test");
		
		driver.manage().timeouts().implicitlyWait(15, TimeUnit.SECONDS);
		
		WebElement btnSave = driver.findElement(By.xpath("//*[@id=\"app\"]/div[1]/div[2]/div[2]/div/div/form/div[8]/button[2]"));
        btnSave.click();
		
	}
		
}
