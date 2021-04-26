# Welcome to Clue 2! 

## The URL of this page is https://otc-cisriley.github.io/CIS150InfoL2/

To solve this clue, you will use TFS to open the project you created in Clue 1.


1.	Move to a different computer (you probably have done this!) Restart your computer if it is the only one you use.

2.	Open Visual Studio, Connect to tfs. [Here is a link to that quick reference](https://github.com/OTC-CISRiley/CIS150InfoLevel1/blob/master/docs/ConnecttoTFS.pdf)

3.	Use Team Explorer, Source Control Explorer to find the project you checked in while solving clue 1

4.	Use the Source Control Explorer to get the latest version of the clue 1 project. Open the project folder.

5.  Double click on the .sln file to open the project. Use Solution Explorer to verify the project contents.
    (you may have to re-create your clue 1 project if it did not check in properly)
    
6.	Update the Main method to prompt for a site to display. Code shown below. The first two lines 
    were added in clue 1, so use them as a reference for adding the new code.

                sites[i] = sitePre + i + @"0Info/";
            }

          --- new code below
            int siteToDisplay;
            // set up our site to display
            Write("\nWhich site to display? ");
            while (int.TryParse(ReadLine(), out siteToDisplay) == false)
            {
                Write("\nWhich site to display? ");
            }

            // open the site based on user input
            Write("\nPreparing to open site " + sites[siteToDisplay] + " . . .");
            ReadLine();

            Process.Start(sites[siteToDisplay]);
          --- end of new code
        }

7.  If there is a compile error, do some research. Are we missing a using statement?

8.  Does the process start command work (a web browser should open with the final instructions)? It depends on your environment. If it does not work, update the code to        include a web browser. For example:
        Process.Start("C:/Program Files (x86)/Google/Chrome/Application/chrome.exe", sites[siteToDisplay]);

9.	After testing is complete, check in the updated solution to tfs. Remain in Visual Studio with your project open.

10.	Run the complete site selection project and choose 10 for the number of sites and site 5. If you follow instructions correctly, you will be rewarded with the next Clue.


[Return to the Level 1 site](https://otc-cisriley.github.io/CIS150InfoLevel1/)
