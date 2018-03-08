package com.ext.testCases;

import java.awt.AWTException;
import java.io.IOException;

import org.testng.annotations.BeforeClass;
import org.testng.annotations.Test;

import com.ext.actions.Practice_Action;
import com.ext.actions.Widgets_Action;
import com.ext.utility.Constant;
import com.ext.utility.ExcelUtils;
import com.ext.utility.Log;

public class TC_Practice {
	
	public int iTestCaseRow;
	 /* @BeforeClass
	  public void startTestCase()
	  
	  {
		 String sTestCaseName = this.getClass().getSimpleName();
		
		 try {
				System.out.println("Im inside the   TC_Practice test suite");
			ExcelUtils.setExcelFile(Constant.file_Path, Constant.file_Name, Constant.sheetName1);
			System.out.println("sheet name n testcase name "+Constant.sheetName +sTestCaseName);
			
		} catch (IOException e) {
			e.printStackTrace();
		}
		 
		iTestCaseRow = ExcelUtils.getRowNum(sTestCaseName, Constant.col_TCname);
		 
	  }*/
	
	  @Test(priority=2)
	  
	  /*public void TC_Alert()
	  {
		  try {
			Practice_Action.execute();
			Log.info("Calling Practice_Action execute method ");
		} catch (Exception e) {
			Log.error("Unable to class Practice_Action ");
			e.printStackTrace();
		}
	  }*/
	  
	  public void TC_Widgets() throws AWTException
	  {
		  try {
			Widgets_Action.execute();
			Log.info("Calling Wdgets method");
		} catch (InterruptedException e) {
			Log.error("Unable to call Widgets_Action class");
			e.printStackTrace();
		}
	  }
	  
	  

}
