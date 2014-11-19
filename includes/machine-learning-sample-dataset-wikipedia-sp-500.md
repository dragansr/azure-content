Data is derived from Wikipedia (<a href="http://www.wikipedia.org/">http://www.wikipedia.org/</a>) based on articles of each S&P 500 company, stored as XML data.<p>Before uploading to Azure ML Studio, the dataset was processed as follows:<ul><li>Extract text content for each specific company</li><li>Remove wiki formatting</li><li>Remove non-alphanumeric characters</li><li>Convert all text to lowercase</li><li>Known company categories were added</li></ul><p>Note that for some companies an article could not be found, so the number of records is less than 500.