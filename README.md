# Redbubble_shop_analysis


📊 Project's goal:


An analysis of a Redbubble store in the print-on-demand business aimed at increasing sales.


 
🗂️ Data:



Source: (Redbubble's shop sales raports and visitors chart)

Range: (sales, products, margin, audience traffic)

Format: (CSV, Audience traffic chart printsceens in Word file)


 
🔧 Tools and technologies:



Excel - data collection, data cleaning, tables, calculation formulas

Power Query - merging files, data cleaning

Power BI – analysis and visualization



📝 The analysis process:


Reviewing the available data and preparing it for analysis.


Requirements from a client:
- I’d like to draw and have my work sell.
- I’d like to make more profit from my shops.
- I’d like to know which niches are working and in which niches I could still publish?
- I’d like to know who my audience is and how to expand it?
- I’d like to get some more tips, but to be honest, I don’t know what kind.


What does an analyst see when they receive requirements from a client?


Main tasks:
- Sales analysis
- Niche analysis
- Customer analysis
- Providing additional recommendations


🗂️ Redbubble store visitor data.


Redbubble still does not offer the option to use Google Analytics 4. It only provides an interactive graph showing visitor numbers over the course of a year.

<img width="878" height="462" alt="Traffic" src="https://github.com/user-attachments/assets/426646b6-f645-44cb-9a83-0ae83b66c4f7" />


The client provided a Word document containing screenshots of charts from the past two years. This data needs to be transferred to Excel to provide a complete overview of the entire period. Of course, artificial intelligence could be used, but there isn’t much data, so even typing it in manually only took a moment.


<img width="684" height="331" alt="traffic excel" src="https://github.com/user-attachments/assets/ef2efd6b-a4eb-4aa0-8ba3-75277ea81677" />


To make it easier to add further rows later and analyse the data, I will insert a table.


<img width="725" height="355" alt="traffic tabela" src="https://github.com/user-attachments/assets/8efa688d-2f30-4359-a555-0e77b8599bdf" />


What can I already see, or what will be worth preparing from the data I have received?

- Customer sources – it is already clear that I will be able to suggest to our client to increase their social media activity

- Seasonality – there is a noticeable increase in store traffic during periods such as the pre-Christmas season


🗂️ Redbubble store sales data.


Data from the Redbubble shop is sent, at the artist’s request, to the email address provided when setting up the shop. It is in CSV format, with each month in a separate file.

<img width="704" height="347" alt="csv" src="https://github.com/user-attachments/assets/6f291dc3-09b5-4b98-bf84-486c8fb9bc26" />

Therefore, the best option is to put everything in a single folder, combine the data using Power Query, and then organise it there so that it is ready for analysis.


<img width="661" height="348" alt="files" src="https://github.com/user-attachments/assets/1117335a-7ab1-4890-90d7-29dc4751b8af" />


Once all the files have been merged, it looks like this:

<img width="652" height="347" alt="power" src="https://github.com/user-attachments/assets/db5d75d1-e9f3-46f9-a473-06d4a81f5870" />

I am now cleaning the data in Power Query and preparing it for analysis. At first glance, it is clear that I will need to set the columns as headers or rename them. I will also need to remove duplicate rows, where the duplicates result from merging multiple files. I will  also check if there are any empty cells. It’s also worth filtering the data by date or sales figures at this stage.

<img width="652" height="347" alt="duplikat" src="https://github.com/user-attachments/assets/ca464329-025e-49cc-9d26-7f6159ec4cde" />

Duplicates have been removed. The columns containing the names of the files from which the product payment status data was sourced have been removed. There are a few empty values in the column labelled ‘state’ or ‘region’, but this will not affect the calculations and may provide some additional information, so this column will remain.

<img width="651" height="347" alt="filtr" src="https://github.com/user-attachments/assets/8f660217-147a-4964-92ae-8e564f8b567b" />


I have also changed the date format to make filtering easier. I now have clean data in Excel ready for further analysis.

<img width="667" height="336" alt="clean" src="https://github.com/user-attachments/assets/1bda36bd-5f11-4938-866d-b23460201df4" />

📈 Data analysis and visualisation.


Customer analysis.


Let’s start by looking at the customers, as a particular issue has been raised here.


Problem: correctly identifying the audience.


On Redbubble, artists ‘like’ each other’s work purely out of a desire to help others, so that their shops can grow and attract more visitors. The problem arises because people who have no intention of buying the products in the first place visit artists’ shops and add their artwork to their favourites. As an artist, I’m therefore turning to my analytical self to address this issue.

<img width="692" height="340" alt="sources" src="https://github.com/user-attachments/assets/ae662694-8430-4f4d-9c92-1d3ea19c8839" />

There is a breakdown of the sources of traffic to the shop on Redbubble site. Based on the descriptions, my experience of publishing images, and observing the changes in the sales tracking chart, I can surmise that the proportion of visitors who enter the shop without any intention of making a purchase will be categorised under ‘Direct’.


Therefore, the best way to check the number of actual customers is to add up all other visitor sources, excluding the ‘Direct’ category.

<img width="689" height="340" alt="indirect" src="https://github.com/user-attachments/assets/caf606fd-77cc-4f47-a342-22886f86d586" />


In my customer analysis, I will consider:
- the total number of visitors and their sources
- total sales, i.e. customers who have purchased products from the shop
- customers’ place of residence by country of origin
- I will estimate the likely number of visitors interested in making a purchase


I will be using Power BI for further analysis and visualisation. I uploaded the data from my Excel file, checked that everything was correct, and started creating the dashboard. I also had to change a few options in the settings to ensure that all the charts I wanted to create worked properly.

<img width="641" height="339" alt="powerbi" src="https://github.com/user-attachments/assets/21a76ff4-24e9-4e42-91ec-a34e8cc31fe6" />

Customer analysis.


<img width="773" height="447" alt="1 Odwiedzający Visitors" src="https://github.com/user-attachments/assets/7c401677-9074-487d-bb2d-243659ca2e02" />


It is clear, that the countries of origin of the shop’s customers are mainly the United States, Australia and Western European countries.


Below is a breakdown of visitors to the shop from the time it was set up until the end of March this year. I used the same breakdown of customer sources as on the official Redbubble website. And, as in the reported issue, this assumption has been confirmed. The ‘Direct’ category has the largest share.
That is why, in the chart on the left, I have compared direct and indirect visitors. The term ‘Indirect’ covers all other sources, including customers who reach the shop via those sources.


What does this mean?
The tables above show that the total number of visitors is 2,000. The total number of indirect visitors, however, is 507. Therefore, of all visitors to the shop, around 25% are people who are genuinely interested in purchasing products.


The total number of products sold is 76. This means that around 15% of real customers make a purchase.


Looking at the various sources of visitors, as a creator on Redbubble, I really only have control over social media. Whether we add Instagram, Pinterest or other social media platforms to our shop tab is entirely up to us. That’s why we can increase visitor numbers through our social media activity.


We can also see here that, due to additional calculations and the identification of potential customers, the line graph shows the seasonal pattern even more clearly, particularly the significant surge in the number of people interested in purchasing products in the run-up to Christmas.


Sales analysis.

<img width="775" height="447" alt="2 Sprzedaż Sales" src="https://github.com/user-attachments/assets/703be18f-1824-470b-992b-be1ac936a57c" />

I have already mentioned seasonality in the chart relating to potential customers, and as you can see, this is confirmed in the case of shop customers. The highest sales were recorded in December. November can also be considered part of the pre-Christmas period. On the other hand, the high sales in September may be linked to children returning to school, and considering the character of the graphics, which are aimed mainly at children, teenagers and women, this could have been the reason for the increased sales.


Looking at the pie chart, we can see which products are bought most often, namely: stickers, socks, cards, T-shirts and mugs. The other products account for a smaller share.


The last chart shows profit margins by product type. And here, my ‘analytical self’ took my ‘artistic self’ by surprise. I thought the margin on stickers was so small that the profit from selling fewer but larger items—such as T-shirts or mugs, which are, however, more expensive—would outweigh the profit from stickers.
As you can see, T-shirts only surpassed greeting cards, and the volume of stickers and socks sold allows for better profit margins.


What advice can be given to the artist on this basis?
It is worth designing larger quantities of simple graphics that sell well as stickers. A larger number of graphics produced in a shorter time, thanks to their simpler design, can generate higher revenue than focusing on large, time-consuming graphics.


Niche analysis.

<img width="776" height="447" alt="3 Analiza nisz Niche Analysis" src="https://github.com/user-attachments/assets/aa2c041e-4078-4654-a1e5-2f43bdf57051" />


I have created a chart here showing the titles of the works that have sold. This allows us to highlight a few of the best-selling categories and identify niche markets.


I have included tables showing how many items have been sold and which products featuring a particular design are the most popular.


I also added a filter to see customer preferences in different countries.
At this point, I have to combine my analytical and cultural knowledge, because there’s no other explanation for it. K-POP Demon Hunters helped this shop to grow. I’d created ‘I LOVE K-POP’ graphics long before that, but following the release of the blockbuster film – which was loved by children and adults alike – my Korean-themed graphics started to sell.


Business conclusions:
1.    Keep an eye on current trends and fashion.
2.    Do not copy other people’s work; respect copyright. The words ‘I LOVE K-POP’ were enough – it is not worth risking having your shop shut down.


Apart from Korean prints, the following also sold well: cats, cute animals, a silly goose, and family-themed designs, such as a gift for the best mum.


What are the customers and target audience, then?
Children, teenagers, women or parents, animal lovers.


Which niches are worth developing?


Asian – Korean graphics can also be complemented with more Japanese and Chinese illustrations.


Children’s – graphics designed with children in mind: colourful, charming, sometimes funny, or related to children’s interests.


Family – gifts for loved ones for various occasions; here, you can include more seasonal designs to mark the holiday season.


Animal lovers – graphics featuring animals, cats, dogs and others.


Funny – amusing and charming graphics such as Silly Goose.


Summary

<img width="769" height="446" alt="4 Podsumowanie Summary" src="https://github.com/user-attachments/assets/65cac7cb-154c-46cb-aed4-4933a2c697f5" />



What can an artist do to boost sales in their shop?
1.    Focus solely on indirect visitors, particularly potential customers who follow the shop’s social media. It’s worth increasing activity and expanding reach to new platforms, as well as creating more engaging content.
2.	The best niches right now are: Korean, cats, cute animals, silly goose, and gifts for family. Creating content in these niches will continue to be profitable. You can also expand these niches—for example, the Korean niche—to include graphics related to Japan and China as well.
3.	Due to seasonality, it’s worth creating more seasonal graphics.
4.    Stickers are the most popular purchases, so creating more simple graphics instead of more time-consuming ones can bring better results.



Please note:
This is a project created for a portfolio. The data comes from the project author’s actual shop. Only some of the data can be shared. The project addresses a real business problem, and the conclusions drawn will be put into practice.

https://www.redbubble.com/people/HugSomeNettles/shop?asc=u


