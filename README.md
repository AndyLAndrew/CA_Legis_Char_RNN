# CA_Legis_Char_RNN
A California Legislature Bill Webscraper + Character RNN GUI

Updated: June 17th, 2023

Welcome! This is my attempt at creating a simple Character RNN interface complete with web scraping built-in for the California Legislature Bills!

I noticed a lack of easy-to-access interface on their own bill search website, and who really wants to copy and paste a lot of text manually? So, this little application should take care of that issue if the raw text is what you truly desire!

How the process works:
1. In the left panel of the window, add in the ranges of bills you wish to scrape along with any keywords you want to search for/filter. 
2. The web scraper will automagically scrape the CA Legis website of all bill content and neatly convert it into both a csv with Bill Number, Session Years, Authors, etc. Note the website mysteriously omits some of this info so if its missing here, its missing in the website.
3. You will also have a concatenated text file of all of the bills you scraped! Both the .csv and .txt will be saved as temp files that you may use for your own processes.
4. Once you've collected your bill text, you can now feed it into a Character RNN where you will be able to optimize it to your heart's content (within limitations).
5. After training your model and several cups of tea or coffee later, you will be able to see and evaluate the results! Then feel free to save the weights for your own fun!

*Some limitations + Other Background Things to Be Aware Of*
- This utilizes Python 3.9+ jupyter, please ensure you have these installed before installed/setting up anything else cause it won't work if you don't!
	- I will be making a standalone .py version soon so jupyter will not be necessary on the next commit
- The packages this relies upon are
	- PyTorch
	- PySimpleGUI
	- Matplotlib
	- BeautifulSoup (bs4)
	- Requests
	- threading

- This was developed on an M1 Max with heavy reliance on mps (aka the M1 GPU). It is perfectly possible to run this on your CPU or other GPU, but be sure to install PyTorch Correctly and edit the device declaration at the beginning of said code. Otherwise you will have training running solely (and painfully) off the CPU.

- For now, the Char RNN is a *single hidden layer only*, I will be integrating non-linearity function and additional hidden layer options within the GUI soon!

-Special thanks to Professor Zhuowen Tu of UCSD for the project opportunity and knowledge being passed on.