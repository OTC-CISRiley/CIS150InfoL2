# Welcome to Level 2!

In this level, you will use TFS to open the project you created in Level 1.


1.	Move to a different computer (you probably have done this!)

2.	Open Visual Studio, Connect to tfs. [Here is a link to that quick reference](https://github.com/OTC-CISRiley/CIS150InfoLevel1/blob/master/docs/ConnecttoTFS.pdf)

3.	Use Team Explorer, Source Control Explorer to find the project you checked in in level 1

4.	Use the Source Control Explorer to get the latest version of the level 1 project. Open the project folder.

5.  Double click on the .sln file to open the project. Use Solution Explorer to verify the project contents.
    (you may have to re-create your level 1 project if it did not check in properly)
    
6.	Update the Main method to prompt for a site to display. Code shown below. The first two lines 
    were added in Level 1, so use them as a reference for adding the new code.

                sites[i] = sitePre + i + @"0Info/";
            }

          --- new code below
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

7.	After testing is complete, check in the updated solution to tfs. Remain in Visual Studio with your project open.

8.	Run the complete site selection project and choose site 5. You will be directed to the Level 3 site.
