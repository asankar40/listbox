# listbox
package Lsst;

import org.openqa.selenium.By;
import org.openqa.selenium.Keys;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.openqa.selenium.interactions.Action;
import org.openqa.selenium.interactions.Actions;
import org.openqa.selenium.support.ui.Select;

public class LLB {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		WebDriver driver = new FirefoxDriver();
		driver.get("C:\\sankar\\Java\\listbox.html");
		driver.manage().window().maximize();
		WebElement ele = driver.findElement(By.xpath("html/body/select"));
		Select sel = new Select(ele);
		Actions act = new Actions(driver);
		Action act1 = act.keyDown(Keys.CONTROL).click(sel.getOptions().get(1)).click(sel.getOptions().get(3)).keyUp(Keys.CONTROL).build();
		act1.perform();
		

	}

}

