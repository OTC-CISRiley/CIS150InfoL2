# Welcome to Level 2!

In this level, you will open the project you created in Level 1 and update it.


1.	Move to a different computer (you probably have done this!)
2.	Open Visual Studio, Connect to tfs. [Here is a link to that quick reference](https://github.com/OTC-CISRiley/CIS150InfoLevel1/blob/master/docs/ConnecttoTFS.pdf)
3.	Use Team Explorer, Source Control Explorer to find the project you checked in in level 1
4.	Use tfs to get latest version of the level 1 project
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

7.	After testing is complete, check in the updated solution to tfs.
8.	Run the complete program and choose site 5 for Level 3 instructions
