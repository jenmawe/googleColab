Here are my Google Colab jupyter notebooks. The first one was to search Shared Print Retention Information. The other one was to experiment with the OCLC Knowledge Base API. These Google Colab notebooks were created with the help of Co-Pilot.

# OCLC Knowledge Base API and eResources Management
The bulk of our eResources come from OCLC's Collection Manager. With delete files, I've seen that sometimes the title isn't deleted from the OCLC Knowledge Base. Rather, the title is removed from one WorldCat record and set on a different one. Because I don't use OCLC numbers as a match point, the local record can be updated if the title is still a part of the Knowledge Base. I experimented with the Knowledge Base API. The first one using ISBNs and then using title. I found that the accuracy was better with the title search rather than the ISBN. I have included both here.

## OCLC_KB_API_ISBN
You will need a csv file where the first line of that csv is isbn. Then there is an ISBN on each line.

## OCLC_KB_API_title
You will need a csv file where the first line is title. Then there is the primary title on each line. This notebook will do 4 passes with 4 different types of searches as well as normalize the title.

# OCLC WorldCat Metadata API & Token
We frequently deal with our shared resources. We are part of EAST or the Eastern Academic Scholarly Trust program for both print monographs and serials. We also belong to the Rosemont Alliance shared print program. When we are weeding or doing other cleanup projects, we need to take into consideration our shared print retention and information about an item's shared retentions. To do this, I relied on the WorldCat MetadataAPI. Originally, I investigated the Goolge Extension for Chrome called the Shared Print Retention Google Add-on. Because our Google has some limitations where I work, this Chrome extension didn't work. I went to copilot to investigate the creation of a Google Colab notebook to do this. Unlike the add-on, the notebook requires a token before querying the information. After this, it groups the results together by OCLC number.

## oclc_retained_holings_colab_groupedOCLCNumber
You will need a csv file where the first line is oclcNumber. Then there is an OCLC number on each line.
