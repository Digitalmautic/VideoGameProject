pipeline {
  agent any
  stages {
    stage('1st Blue Ocean Project') {
      parallel {
        stage('1st Blue Ocean Project') {
          steps {
            git(url: 'https://github.com/Digitalmautic/VideoGameProject.git', branch: 'Main', poll: true, changelog: true)
          }
        }

        stage('2nd Step') {
          steps {
            withGradle()
          }
        }

      }
    }

    stage('3rd') {
      parallel {
        stage('3rd') {
          steps {
            sh '''package myTests;

import org.openqa.selenium.Alert;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;

public class Alerts {

	public static void main(String[] args) throws InterruptedException {
		
		System.setProperty("webdriver.chrome.driver", "C://Drivers//chromedriver_win32/chromedriver.exe");
		WebDriver driver = new ChromeDriver(); 
		
		driver.get("https://the-internet.herokuapp.com/javascript_alerts");
		
		
		//JavaScript Alert with OK
		driver.findElement(By.xpath("//button[normalize-space()=\'Click for JS Alert\']")).click();
		Thread.sleep(3000);
		driver.switchTo().alert().accept();
		
		
		//JavaScript Alert with OK & Cancel /confirmation
		driver.findElement(By.xpath("//button[normalize-space()=\'Click for JS Confirm\']")).click();
		Thread.sleep(3000);
		driver.switchTo().alert().accept();
		//driver.switchTo().alert().dismiss();
		
		
		//JavaScript Alert with Input Box
		driver.findElement(By.xpath("//button[normalize-space()=\'Click for JS Prompt\']")).click();
		Thread.sleep(3000);
		Alert alertwindow=driver.switchTo().alert();
		alertwindow.sendKeys("Welcome");
		alertwindow.accept();
				
	}

}
'''
          }
        }

        stage('4th') {
          steps {
            echo 'Successful Pipeline'
          }
        }

      }
    }

  }
}