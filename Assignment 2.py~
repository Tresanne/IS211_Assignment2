#!/usr/bin/env python
# -*- coding: utf-8 -*-
"""Modules"""

# imports
import urllib2
import argparse
import logging
from datetime import datetime

LOG_FILENAME = 'error.log'
logging.basicConfig(filename=LOG_FILENAME,
                    filemode='w',
                    )

assignment2 = logging.getLogger("assignment2")
assignment2.setLevel(logging.ERROR)
# Part 2


def downloadData(url):
    return urllib2.urlopen(url).read()

# Part 3: Process data


def processData(content):
    
    d = dict() 
    for v in content:
        dd = v.split(',') 
        try:
            ID = dd[0]
            name = dd[1]
            bdate = dd[2]
        except IndexError:
            continue
      
      
# Part 5:
def main():
    #url = "https://s3.amazonaws.com/cuny-is211-spring2015/birthdays100.csv"

    parser = argparse.ArgumentParser(description='Assignment 2')
    parser.add_argument(
        '--url', help='url for getting the content', required=True)
    args = vars(parser.parse_args())

    csvData = downloadData(args['url'])
    data = csvData.split('\n')[1:]
    personData = processData(data)


if __name__ == '__main__':
    main()

