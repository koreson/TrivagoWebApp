# TrivagoWebApp
Testing the functionality and testcase of TrivagoHotelWebApp#Each feature contains one feature
#Feature files use Gherkin langauge - business language
Feature: Testing to find landing page on Trivago hotel Web site

 #A feature may have given different specific scnarios
 #Scenarios use Given - When - Then structure
 Scenario: user launch Trivago Web site to see the landing page
 
 Given user launch Trivago Web site 
 When  user click on Trivago Web site cannot navigate to the landing page and see the advertisement
 Then user confirmed that the Trivago landing page needs to be fixed
 
 Given user click on search button to see Dusseldorf
 When user see many Dusseldorf hotels
 Then user confirmed the Dusseldorf hotels
 
 Given user click on the Expedia to make advance search 
 When user navigate to the landing page and see the advertisement working successfully
 Then user confirmed Expedia landing page


	 
	 @When("^user see many Dusseldorf hotels$")
	 public void user_see_many_Dusseldof(){
	 System.out.print("user see many Dusseldof hotels");  
	 
	 }
	 
	 @Then("^user confirmed the Dusseldorf hotels$")
	 public void user_confirmed_the_Dusseldof_hotes(){
     System.out.println("user confirmed the Dusseldorf hotels");
	 }
	 
	 @Given("^user click on the Expedia to make advance search$")
	 public void user_click_on_the_Expedia_to_make_advance_search(){
	 System.out.println("user click on the Expedia to make advance search");
	 
	 }
	 @When("^user navigate to the landing page and see the advertisement working successfully$")
	 public void user_navigate_to_the_landing_page_and_see_the_advertisement_working_successfully(){
	 System.out.println("user navigate to the landing page and see the advertisement working successfully");  
	 
	 }
	 @Then("^user confirmed Expedia landing page$")
	 public void user_confirmed_Expedia_landing_page(){ 
	 System.out.println("user confirmed Expedia landing page"); 
	 
	 }
	
}


package CucumberTrivagoTest;

import org.junit.runner.RunWith;

import cucumber.api.CucumberOptions;
import cucumber.api.junit.Cucumber;

@RunWith(Cucumber.class)

@CucumberOptions(
		
		features = "Features", glue = {"stepImplimentations"}
		)

public class CucumberTestRunner {

}
