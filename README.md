# HW2_summer2019_philip_jung

## The program starts @ index.jsp
For that reason, the web.xml file was not editted at all.
This index.jsp file reads the text message located in the same logical directory.
  If the file is missing or erroneous, simply redirect to error.jsp which is a page that simply displays a message. 
  Else, the page is loaded, the string is parsed into city objects and stored in a session ArrayList<City> object called cityList.

## displayall2.jsp
When users clicks the "Display All" button, they will be redirected to this jsp. This jsp displays a list of all cities.
All cities, however, is only displayed when all the cities are listed and more than one city is in that list. Therefore,
if a textfile contains only one city, "All Cities" won't ever be displayed. 
Initially, the cities are sorted in alphabetical order A-Z:
When users click the different sorting methods
in the dropdown box, their choice is sent, through URL (get), to SortingServlet.java.

## SortingServlet.java
Sorts the ArrayList<City> cityList based on the value being passed to it and redirects to displayall3.jsp

## displayall3.jsp
Same page as displayall2.jsp except now the cities are sorted in however order the user picked

## cityinfo.jsp
When a user clicks the city name from the table in displayall2.jsp or displayall3.jsp, they will be redirected to cityinfo.jsp
Here, when cards are clicked, that card gets flipped and the corresponding city info is displayed.

