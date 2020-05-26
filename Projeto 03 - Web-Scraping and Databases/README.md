## Data Gathering Project - Tourist destinations and their relationship with the exchange rate

Context: A company about tourism seeking for insight of how exchange rate can affect the business and which destinies should have different business strategies.

## Objective

**The main idea in this project is to gather information using Web Scraping, API tools or Selenium and save in data base.**

## Description

The project does the following extractions: 
* **Web scraping** from a brazilian tourism website and their recommended destination information.
    * [Tourism Web Site](https://viagemeturismo.abril.com.br/materias/os-100-lugares-mais-lindos-do-mundo/)
* **Web scraping** the list of countries and currencies, with the ISO code
    * [ISO Code Web Site](https://www.sport-histoire.fr/en/Geography/Currencies_countries_of_the_world.php)
* **Web scraping** to translate country names (Tourism Web Site is written in portuguese while ISO code Web Site in english) 
    * [Country table PT-EN](https://brazil-help.com/countries.htm)
* **API** - Extracting currency quote information for destinations
    * [Original Site](https://docs.awesomeapi.com.br/api-de-moedas)
    * [API UR](https://economia.awesomeapi.com.br/json/all)
* **Selenium** - A problem found was that the API only allowed to extract information at the requested moment and if someone wants to do an analysis of values not captured in the past it would not be possible. For this reason, a code was created using Selenium to extract information from the Brazil Central Bank's website that allows changing the date and viewing the exchange rate ratio of the real versus all other currencies.
    * [Brazil Central Bank's URL](https://www.bcb.gov.br/conversao)
* **Save** the extracted data into **Postgres** data base with SQL
* **Retrieve** data from **Postgres** data base

   
   
## Future jobs

* Try Selenium wait ("wait until") from Selenium or "driver.implicit wait" to reduce extraction time from Brazil Central Bank's WebSite
* Create a pipeline from this process to be able to scale
* Manage to change the day in calendar with Selenium on the Brazil Central Bank's Website to automatize past extraction
* Transform into the most of the code into functions 

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.


## Requirements

* requests==2.23.0
* selenium==3.141.0
* pandas==1.0.3
* numpy==1.18.1
