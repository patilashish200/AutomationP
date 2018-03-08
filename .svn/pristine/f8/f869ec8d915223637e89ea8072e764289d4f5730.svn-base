package com.ext.testCases;

import java.io.IOException;

import org.apache.log4j.xml.DOMConfigurator;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.testng.Assert;
import org.testng.annotations.BeforeClass;
import org.testng.annotations.BeforeMethod;
import org.testng.annotations.Listeners;
import org.testng.annotations.Test;

import com.ext.actions.Login_Action;
import com.ext.pageObjects.Login_Page;
import com.ext.utility.Constant;
import com.ext.utility.ExcelUtils;
import com.ext.utility.Log;
import com.relevantcodes.extentreports.LogStatus;

@Listeners(com.ext.utility.Listener.class)
public class TC_Login  extends BaseTestCase{
//public static WebDriver driver;

public int iTestCaserow;
	  
	  /*public static void main(String args[])
	  {
		  TC_Login tc1 = new TC_Login();
		  try {
			tc1.startTC();
		} catch (IOException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}
		  tc1.TC_Login1();
	  }
	  */
 @BeforeClass
   public void beforeMethod() throws IOException
    
 {
	 DOMConfigurator.configure("log4j.xml");

	String sTestCaseName = 	this.getClass().getSimpleName();
	//System.out.println("Test Case Name is "+sTestCaseName);
	 Log.startTestCase(sTestCaseName);
	 
	try {
		ExcelUtils.setExcelFile(Constant.file_Path,Constant.file_Name ,Constant.sheetName);
		
		Log.info("Set Excel Path, Name and Sheet "+Constant.file_Path +Constant.file_Name +Constant.sheetName );
	} catch (Exception e) {
	Log.error("Unable to set excel Path, Name and Sheet "+Constant.file_Path +Constant.file_Name +Constant.sheetName);
		e.printStackTrace();
	}

	iTestCaserow = ExcelUtils.getRowNum(sTestCaseName, Constant.col_TCname);
	//System.out.println("Test Case Row No "+iTestCaserow);
	
	/*driver = Utils.OpenBrowser(iTestCaserow);
	new BaseClass(driver);
	*/
}
   
@Test(priority=1)
public void  TC_Login1()
{
			
			logger = report.startTest("TC_Login1");
			
		//	System.out.println("Im inside the TC_Login1");
			try {
				Login_Action.excecute(iTestCaserow);
		//		Assert.assertTrue(driver.getTitle().equalsIgnoreCase("Register"), "Logged in notsuccessful");
			
				Log.info("Succesfully logged into system");
			} catch (Exception e) {
			Log.error("Unable to login into application");
				e.printStackTrace();
			}
			logger.log(LogStatus.INFO, "Logged in status");
		
}
/*@Test(priority=0)

	public void TC_Login2()
{
	
		
			logger = report.startTest("TC_Login2");
			
				String UNplaceholder =ExcelUtils.getCellData(iTestCaserow, Constant.col_UNPlaceholder);
				
				logger.setDescription(UNplaceholder);
			//	System.out.println("Exp pl hol "+UNplaceholder);

			String ActUNplaceholder = Login_Page.userName_txt().getAttribute("placeholder").toString();
				
			//	System.out.println("act pl hol "+ActUNplaceholder);
					
				Assert.assertEquals(ActUNplaceholder, UNplaceholder, "Placeholder is not matching");
				
				logger.log(LogStatus.INFO, "Place hoder status");		
	
}		*/
	/*@Test (priority=1)
	
	public void TC_Login3()
	
	{
		logger = report.startTest("TC_Login3");
		System.out.println("Im inside the TC_Login3");
		//Assert.assertTrue(true, "Test Case 3 Condition is true");
		Assert.assertEquals(false, "Test Case TC_Login3 failed");
		System.out.println("Im at the end of TC_Login3");
		
		
	}*/
/*@Test(priority=1)
public void TC_Login4()
{
//	Boolean msg = Login_Page.ErrorMsg().getAttribute("innerHTML").toString().equalsIgnoreCase("Invalid User Name or PassWord");

	String sActMsg = Login_Page.ErrorMsg().getAttribute("innerHTML").toString();
	String sExpMsg = "Invalid User Name or PassWord"; 
	System.out.println("Actual error message is " +sActMsg);
	
	Assert.assertTrue(sActMsg.contains(sExpMsg), "No error message is displayed");
}

*/
}