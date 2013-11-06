
I was talking with [Scott Weingart](https://twitter.com/scott_bot/) about his recent [analysis of Digital Humanities 2014 submissions](http://www.scottbot.net/HIAL/?p=39588) and got to thinking I might be able to re-purpose my code from my [4S2013 visualiation](http://bl.ocks.org/mcburton/6314426) for DH 2014. Scott was kind enough to send me a CSV file containing a count of submissions per institution as listed by submitting author. **NOTE: This doesn't represent all authors and all institutions, just those who performed the submission and their affiliated institution.** Using my old code that automatically fetched location information Google's GeoCoding APIs and visualized it in D3 I figured it wouldn't be too much effort to brew up another visualization as a distraction from [my dissertation](http://lofhm.org/discursive-infrastructure). 

At a high level this is what I did:

- Cleaned the data Scott sent me.
- Fetch location information for each institution using [geopy](https://code.google.com/p/geopy/)
- Manually clean the data fetched from Google by removing duplicates and either filling in or removing those institutions Google's geocoding API couldn't find (unfortunately those listed as independent researchers were dropped b/c I didn't have their location information).
- Count the submissions by country and transform country names into country codes
- Drop the new data into an HTML & d3.js document.
- Make PDF and PNG versions of the visualization.
- Touch up the IPython Notebook & push to github.

This IPython Notebook encapsulates most of the work I did to generate the DH2014 choropleth. I've done my best to document work done *outside* the IPython Notebook (mainly data cleaning using Excel). However, I haven't gone through and added much narrative above and beyond the raw code. What this means is you need to be somewhat familiar with python to understand follow my workflow. At some point, I would like to spend a bit more time documenting the code and the workflow, but I haven't the time today.

So I suppose you will have to make due with the the visualization([pdf](https://github.com/mcburton/dh2014-grok/raw/master/dh2014-world-dist.pdf), [png](https://raw.github.com/mcburton/dh2014-grok/master/dh2014-world-dist.png)), the notebook([nbviewer link](http://nbviewer.ipython.org/urls/raw.github.com/mcburton/dh2014-grok/master/dh2014-choropleth.ipynb)) which captures most of the workflow, and a [github repository](https://github.com/mcburton/dh2014-grok) containing the project's history. 

enjoy!