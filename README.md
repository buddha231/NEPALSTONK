


# STONK
Complete NEPSE solution in command line

https://user-images.githubusercontent.com/52292457/123103383-a924c500-d455-11eb-94a4-b1fde8ff8c48.mp4
## Installation
```console
pip install nepal_stonks
````
After the installation you can use the cli application with the priceof command

## Usage
```console
usage: priceof [-h] [-c [...]] [-f] [-n] [-m] [-ms] [-d] [-cu] [-ci]
               [--losers] [--gainers] [--supply] [--demand] [--turnover]
               [--volume] [--transactions]

STONK, complete NEPSE solution in command line

optional arguments:
  -h, --help            show this help message and exit
  -c [ ...], --company [ ...]
                        symbols of companies seperated by space
  -f, --floorsheet      get floorsheet
  -n, --nepse           get NEPSE index and subindices
  -m , --market_depth   get market depth of the company(enter symbol)
  -ms, --market_summary get market summary
  -d , --get_detail     get the non price related detail of the company
  -cu , --custom        custom list in data.py
  -ci , --change_index  change the value of id sent as a payload in the post
                        request
  --losers              get the top losers
  --gainers             get the top gainers
  --supply              get the scripts with maximum supply
  --demand              get the scripts with maximum demand
  --turnover            get the scripts with maximum turnover
  --volume              get the scripts with maximum volume
  --transactions        get the scripts with maximum transactions
```

## Please change the index with -ci flag.
https://user-images.githubusercontent.com/52292457/123106754-a1b2eb00-d458-11eb-924c-591f24bcb4e2.mp4


Since i can't afford to pay for the nepse api(I don't think I would, even if I could, but anyways). 
There are some caviets to retrieving data from api endpoints from the nepse's newweb website. Nepse decided
to change the request method for some api endpoints from get to post. The payload sent along with the
post request changes randomly at different intervals. 
The payload looks like 
```
{
  "id" : 123
}
```
Here 123 is a random number. This number can be changed using the -ci flag. This is demonstrated in the video above



