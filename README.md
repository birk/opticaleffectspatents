# Optical Effects Patents

This list of patents was collected as part of the research for my dissertation *Image as Collective: A History of Optical Effects in Hollywood's Studio System* (2014). It does not claim to be a comprehensive list in the sense of containing all patents that cover the field but rather gathers those that were considered to be relevant at the time. There are a few key selections here and patents, which are part of one or more of these, are marked accordingly in the `collections` column. The `cpc` column provides information on each patent's classification according to the [Cooperative Patent Classification](http://www.cooperativepatentclassification.org).

[![goodtables.io](https://goodtables.io/badge/github/birk/opticaleffectspatents.svg)](https://goodtables.io/github/birk/opticaleffectspatents)  
[![DOI](https://zenodo.org/badge/98713492.svg)](https://zenodo.org/badge/latestdoi/98713492)

### Collections

* `WallSomePatents`: E. J. Wall, "Some Patents for Trick Photography," *Transactions of the Society of Motion Picture Engineers* 11, no. 30 (August 1927): 328–33. <https://archive.org/stream/transactionsofso29soci#page/328/mode/2up>
* `HinelineProcess`: H. D. Hineline, "Composite Photographic Processes," *Journal of the Society of Motion Picture Engineers* 20, no. 4 (April 1933), 283-300. <https://archive.org/stream/journalofsociety20socirich#page/282/mode/2up>
* `DunningPomeroyParamountDeal`: In 1930, the Dunning Process Company, Paramount Publix Corporation, and Roy J. Pomeroy, an employee of Paramount, signed an agreement to share their patents.
* `PatentPool`: In 1936 and after several legal conflicts, the major Hollywood studios agreed to share their rights in what came to known as the [patent pool](https://www.academia.edu/6221662/Roy_J._Pomeroy_Dunning_Process_Co._Inc._and_Paramount_Publix_Corporation_vs._Warner_Bros._Pictures_Inc._Vitaphone_Corporation_and_Frederick_Jackman_How_the_Movie_Industry_Turned_to_Rear_Projection).
* `StullProducersPool`: W. Stull, "Producers Pool Composite Process Patents," *American Cinematographer* 17, no. 11 (November 1936): 461, 466–68. An article on the patent pool that lists some but not all patents, which were part of the patent pool agreement.
* `WestheimerF*n*`: The Margaret Herrick Library holds the [Joseph and Katherine Westheimer collection of patents](http://catalog.oscars.org/vwebv/holdingsInfo?bibId=76520) but the exact origin of and intention behind this collection remains unclear. Joseph Westheimer, at some time, worked for Warner Bros, one of the studios involved in the patent conflicts of the early 1930s. This suggests that the studio compiled the collection as part of its technical and legal research. On the other hand, there are hints in the papers that rather refer to Paramount. The patents are organized in folders and are listed here accordingly:
	- Folder 4: Miscellaneous patents circa 1900-1962
	- Folder 7: United States Patents: Composite Pictures & Trick Photography -- volume I circa 1850-1911
	- Folder 8: United States Patents: Composite Pictures & Trick Photography -- volume II circa 1912-1916
	- Folder 9: United States Patents: Composite Pictures & Trick Photography -- volume III circa 1916-1920
	- Folder 10: United States Patents: Composite Pictures & Trick Photography -- volume IV circa 1920-1923
	- Folder 11: United States Patents: Composite Pictures & Trick Photography -- volume V circa 1923-1926
	- Folder 12: United States Patents: Composite Pictures & Trick Photography -- volume VI circa 1926-1931
	- Folder 13: United States Patents: Composite Pictures & Trick Photography -- volume VII circa 1931-1932
	- Folder 14: United States Patents: Composite Pictures & Trick Photography -- supplemental volume I circa 1890-1934, 1939

### Wikidata

The dataset has also been ingested into Wikidata.

```SPARQL
SELECT ?inventor ?inventorLabel ?patent ?patentLabel ?patentNumber ?publicationDate ?cpc 
WHERE {
  { ?patent wdt:P361 wd:Q73406392 } # part of the Westheimer collection
  UNION
  { wd:Q73409834 wdt:P2860 ?patent } # cited by Wall
  UNION
  { wd:Q73410099 wdt:P2860 ?patent } # cited by Hineline
  UNION
  { wd:Q73410716 wdt:P2860 ?patent } # cited by Stull
  ?patent wdt:P61 ?inventor ;
          wdt:P1246 ?patentNumber ;
          wdt:P577 ?publicationDate ;
          wdt:P5778 ?cpc .
  SERVICE wikibase:label { bd:serviceParam wikibase:language "[AUTO_LANGUAGE],en". }
}
```

<https://w.wiki/CX3>
