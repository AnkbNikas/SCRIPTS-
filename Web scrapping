import requests

from bs4 import BeautifulSoup

 

def scrape_website(url):

    try:

        # Send a GET request to the URL

        response = requests.get(url)

        response.raise_for_status()  # Check for request errors

       

        # Parse the HTML content

        soup = BeautifulSoup(response.content, 'html.parser')

       

        # Extract data, for example all the headings

        headings = soup.find_all('h1')

        if headings:

            for heading in headings:

                print(heading.get_text())

        else:

            print("No headings found.")

   

    except requests.RequestException as e:

        print(f"An error occurred while fetching the URL: {e}")

    except Exception as e:

        print(f"An unexpected error occurred: {e}")

 

if __name__ == "__main__":

    target_url = input("Enter the target website URL: ")

    scrape_website(target_url)
