package com.ext.testCases;

import java.io.IOException;
import java.util.concurrent.TimeUnit;

import org.testng.Assert;
import org.testng.annotations.BeforeClass;
import org.testng.annotations.BeforeMethod;
import org.testng.annotations.Test;

import com.ext.actions.Register_Action;
import com.ext.pageObjects.Register_Page;
import com.ext.utility.BaseClass;
import com.ext.utility.Constant;
import com.ext.utility.ExcelUtils;

public class TC_Register extends BaseTestCase{

  public int iTestCaseRow;
  @BeforeClass
  public void startTestCase()
  
  {
	 String sTestCaseName = this.getClass().getSimpleName();
	
	 try {
			System.out.println("Im inside the   TC_Register test suite");
		ExcelUtils.setExcelFile(Constant.file_Path, Constant.file_Name, Constant.sheetName1);
		System.out.println("sheet name n testcase name "+Constant.sheetName1 +sTestCaseName);
		
	} catch (IOException e) {
		e.printStackTrace();
	}
	 
	iTestCaseRow = ExcelUtils.getRowNum(sTestCaseName, Constant.col_TCname);
	 
  }
     @Test (priority=3)
     
     public void TC1_Register() throws InterruptedException
     {
    	 logger = report.startTest("TC1_Register");
    		System.out.println("Im inside the TC1_Register");
    	 Register_Action.excecute(iTestCaseRow,BaseClass.driver);	 
    	 
    	 driver.manage().timeouts().implicitlyWait(10,TimeUnit.SECONDS);
    	 Assert.assertTrue(driver.getTitle().equalsIgnoreCase("Web Table"), "Not rediected to Web table page");
     }
    /* @Test (priority=3)
     
     public void TC2_Register()
     {
    	 try {
			Register_Action.excecute(iTestCaseRow,BaseClass.driver);
		} catch (InterruptedException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
			
			
		}	
    	 Boolean errmsg = Register_Page.txt_msg().getAttribute("innerHTML").toString().contains("Email already exists");
    	 Assert.assertTrue(errmsg, "Email already exists message not displayed");
    	 
    	
     }
     */
     
     
     
     
     
     


}
