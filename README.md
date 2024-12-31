Close specific websites whether it is already open or will be open with a screenshot of the closed website.

The tricky part here is what info do you need to identify these websites, how to get it and how to make the robot to keep watching:

1- Identification: Tab title? or maybe the URL -> The URL since not all pages of all websites include the trademark name in the title.

2- Getting the URL: The URL is an attribute of a UiElement which is a child of its container which is the browser tab.

2.2- Use "Find Children" without indication or a selector, set the "Scope" property to "find_top_levels" and set the "Filter" property to "<html app='chrome.exe' />".

2.5- Each child now is a tab which is a UiElement and that means it can be sent as target/input to the "get attribute" activity and it will return the URL.

2.8- now you have the URLs and the Restricted websites predefined list, loop through them and if a URL contains(_website.com_), take a screenshot and close it.

3- Keeping watch: a "Repeat Trigger" that will repeat the automation every x seconds.
