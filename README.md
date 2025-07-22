# Project 2

I found a dataset on the infrastructure of swimming spots published by the Department of Justice and Health on the Open Data platform of the state of Schleswig-Holstein. I combined it with a second one that had the names and descriptions of all swimming spots. The data was in horrible shape so it was a huge effort to get it all cleaned up. <br>
After that was done, I explored the dataset by asking some questions to determine which aspects would be most interesting for a story. Of course, this kind of data would be perfect for a general service piece, but I was very intrigued when I saw that there was information on wheelchair and public transport accessibility as I am very interested in questions of instrastructure and who it excludes from full participation. I though about further aspects that might prevent people from being able to go to the beach and decided to also look at the cost. For that, I scraped a website with all the beach tax amounts for baltic seaside resorts but ended up not needing that information. Originally, I wanted to compare the total cost in 2021 (before inflation really hit) to now but it was too complicated to find the historical data so I ended up just using the current data for a specific example and adding some remarks about changes in the graphic which I think works too.<br>
The dataset claimed that only 2% of all swimming spots had access to public transport. That seemed unrealistic to me - even for a state known for its bad public transport infrastructure. (I tried to figure out how they determined which spots had public transport but it's not in the documentation and from looking at the data, I couln't make any sense of it. I thought it was just the spots that had the exact same name as the bus stop or the ones with a train stop, but neither seems to be the case.) So I decided to do a spatial analysis with QGIS myself to determine which swimming spots are within a 10-minute walk from a bus/train stop. <br>
I already had the coordinates of all swimming spots and found the following geodata for my analysis:
<ul>
<li>All bus stops in the state</li>
<li>Roads (I excluded motorways and bridleways for the analysis to have only the streets people would be able to walk on)</li>
<li>Water shapefile to check whether the bathing locations were accurate (some where a little off but not so much that the analysis wouldn't work)</li>
<li>Double-checked with train stations to see whether there are spots that would be accessible by train but not by bus (turns out there are none)</li>
</ul>

I wanted to show that there are further problems with the infrastructe of public transport: infrequent service, complicated routes etc. So I compared the route taking a car and taking a bus using Google Maps. My initial idea was to to have them animated, showing the difference in travel time. I tried to get a Mapbox template to work for that but it was really difficult to get the code to do exactly what I wanted so I made a static map instead.<br>
I enjoyed exploring a dataset with lots of different information to see what I could pull out of it. This was a great opportunity to practice mapping skills and doing a spatial analysis with QGIS on my own. It was also nice to practice HTML/CSS/Javascript skills by combining different templates so the final result would look nice(-ish). With more time, I would have liked to do more styling (and try to get the animation to work). I'm also not super happy with the writing, but alas.<br>
I had a look at the distribution of swimming spots and also at income levels for each district but didn't really find any interesting patterns that I felt would be worth incorporating into my project.<br>

All data sources I used: 
<ul>
<li>https://opendata.schleswig-holstein.de/dataset/badegewasser-infrastruktur-aktuell</li>
<li>https://opendata.schleswig-holstein.de/dataset/badegewasser-stammdaten-2025-04-01</li>
<li>https://opendata.schleswig-holstein.de/dataset/haltestellenverzeichnis</li>
<li>https://public.opendatasoft.com/explore/dataset/georef-germany-land/export/?disjunctive.lan_code&disjunctive.lan_name&sort=year&refine.lan_name=Schleswig-Holstein&location=5,51.32941,10.45403&basemap=jawg.light</li>
<li>https://www.st-peter-ording.de/strandkoerbe/</li>
<li>https://gosch.de/speisekarten/st-peter-ording-buhne1/</li>
<li>https://www.giovannil.com/eiskarte/</li>
<li>https://www.google.com/maps/place/GOSCH+St.+Peter-Ording+Buhne+1/@54.313885,8.602933,3a,75y,90t/data=!3m8!1e2!3m6!1sCIHM0ogKEICAgICKssaZPA!2e10!3e12!6shttps:%2F%2Flh3.googleusercontent.com%2Fgps-cs-s%2FAC9h4noaQVvPtaoAn9qVH2OSA0wIJDlo77dVNRSSFYbj59eOt33XbV-U10ZO7kH08EJ-k2XoDkt3PrlEA9cmAQRGgXOTd99SZ16bAuUIi4Iv2ywqkFo8J1U3-EuO4KYcOCPo5mAfHksC%3Dw146-h195-k-no!7i3024!8i4032!4m11!1m2!2m1!1sfischbr%C3%B6tchen!3m7!1s0x47b466182132ae19:0xa2ba265140f8a5c3!8m2!3d54.3139256!4d8.6029215!10e9!15sCg5maXNjaGJyw7Z0Y2hlbloQIg5maXNjaGJyw7Z0Y2hlbpIBEnNlYWZvb2RfcmVzdGF1cmFudJoBI0NoWkRTVWhOTUc5blMwVkpRMEZuU1VObGRFbEhUMFozRUFFqgFWCgovbS8wZzV0MjdqEAEqEiIOZmlzY2hicsO2dGNoZW4oBTIeEAEiGp0wthNHjhaCgEuTOooc-zVkabATkvv6WMcyMhIQAiIOZmlzY2hicsO2dGNoZW7gAQD6AQUInAEQQQ!16s%2Fg%2F1th5yw3w?entry=ttu&g_ep=EgoyMDI1MDcxNS4xIKXMDSoASAFQAw%3D%3D</li>
<li>https://www.kn-online.de/schleswig-holstein/kurtaxe-in-schleswig-holstein-welche-orte-besonders-teuer-sind-436UXDYPGRGNFGQKLLGJT22WA4.html</li>
<li>https://www.nordseetourismus.de/aktuelle-nordsee-news/digitales-parken-am-strand-von-st-peter-ording</li>
<li>https://www.st-peter-ording.de/strandkoerbe/</li>
</ul>

Color palette: 
<ul>
<li>#15607a</li>
<li>#18a1cd</li>
<li>#f723b0</li>
</ul>
