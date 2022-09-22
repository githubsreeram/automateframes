
## frame automated by sreeram
package UiComponents;

import java.util.List;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;

public class Frames {

	public static void main(String[] args) {
		
		

		System.setProperty("webdriver.chrome.driver","C:\\Users\\SREE RAM\\Downloads\\chromedriver_win32 (3)\\chromedriver.exe");
		WebDriver driver=new ChromeDriver();
		driver.manage().window().maximize();
		driver.navigate().to("http://testleaf.herokuapp.com/pages/frame.html");
		
		 driver.switchTo().frame(0);
		WebElement frame= driver.findElement(By.id("Click"));
		frame.click();
		driver.switchTo().defaultContent();
		
		
		driver.switchTo().frame(1);
		driver.switchTo().frame("frame2");
		//WebElement frame2= driver.findElement(By.id("frame2"));
		//frame2.click();
		WebElement frame3= driver.findElement(By.id("Click1"));
		frame3.click();
		
		
		driver.switchTo().defaultContent();
		List<WebElement> list= driver.findElements(By.tagName("iframe"));
		int total= list.size();
		System.out.println(total);
		
		
		
		
		
		
		
	}

}

## sreeram