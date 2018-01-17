# Selenium-Test
package SampleTest;

import org.openqa.selenium.WebDriver;
import org.openqa.selenium.firefox.FirefoxDriver;

import sampleTest.Image;
import sampleTest.OCR;
import sampleTest.RenderedImage;
import sampleTest.URL;

public class screenshotLeverpool {
	public static void main(String args[]) throws InterruptedException{
		System.setProperty("webdriver.geckodriver.driver", "C:\\Firefox Gecko driver\\geckodriver.exe");
		WebDriver d=new FirefoxDriver();
		System.setProperty("webdriver.geckodriver.driver", "C:\\Firefox Gecko driver\\geckodriver.exe");
		FirefoxDriver d=new FirefoxDriver();
		d.get("https://itunes.apple.com/in/app/accuweather-weather-for-life/id300048137?mt=8");
		 String imageUrl=driver.findElement(By.xpath("//*[@id='content']/div/div[2]/div[4]/div[2]/div[1]/div[1]/div[1]/img")).getAttribute("src");
		 System.out.println("Image source path : \n"+ imageUrl);
		 URL url = new URL(imageUrl);
		 Image image = ImageIO.read(url);
		 String s = new OCR().recognizeCharacters((RenderedImage) image);
		 System.out.println("Text From Image : \n"+ s);
		 System.out.println("Length of total text : \n"+ s.length());
		 public void verifyTextPresent(String value)
		 {
		   driver.PageSource.Contains(value); ;
		 }
		 try
		 {
		   Assert.IsTrue(verifyTextPresent("LEVERPOOL"));
		   Console.WriteLine("LEVERPOOL is present on the home page");
		 }
		 catch (Exception)
		 {
		   Console.WriteLine("LEVERPOOL is not present on the home page");
		 }
		 driver.quit();
}}
}
