# ScrapG1
The code you've provided uses the requests library to make a GET request to the website https://g1.globo.com/. It then uses the BeautifulSoup library to parse the HTML content of the website, and uses CSS selectors to find specific elements on the page, in this case the news articles.
It creates an empty list named lista_noticias, and then uses the findAll() method to find all elements with the class feed-post-body, which correspond to the div elements that contain the news articles.

For each of these elements, it uses the find() method to find the elements within that contain the title and the link, it extracts the text and href attributes and appends it to the list. It also looks for the element that contains the subtitle, if it exist, it appends it to the list otherwise it appends an empty string.

After that it creates a pandas DataFrame with the data extracted, where the columns are 'Título', 'Subtítulo' and 'Link'. And at the end it prints it on the screen.

Please note that the code includes a commented line that use to_excel function to export the Dataframe to an excel file, the data will be saved in the current working directory with the name noticias.xlsx
Also please make sure that you have the necessary dependencies installed before running it and that the website allows scraping.
