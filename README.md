# Reddit_chats
I've always wondered how a chat bot would work rather I should say communicate, if it is trained on data which is made up of "internet slang".And we all know the best place to find such content is "Reddit". Reddit is a platform, that I would say, where the whole world speaks in the "internet slang".The language used is aggresive and harsh in tone. People like to troll each other and sarcasm is the essesnce of Reddit.The topics vary widely from sports,comedy,romance,science,books etc to dark humour,crime,action,horror etc.

The data is in the form of JSON, below is a sample of the format

{"score_hidden":false,"name":"t1_cnas8zv","link_id":"t3_2qyr1a","body":"Most of us have some family members like this. *Most* of my family is like this. ","downs":0,"created_utc":"1420070400","score":14,"author":"YoungModern","distinguished":null,"id":"cnas8zv","archived":false,"parent_id":"t3_2qyr1a","subreddit":"exmormon","author_flair_css_class":null,"author_flair_text":null,"gilded":0,"retrieved_on":1425124282,"ups":14,"controversiality":0,"subreddit_id":"t5_2r0gj","edited":false}
{"distinguished":null,"id":"cnas8zw","archived":false,"author":"RedCoatsForever","score":3,"created_utc":"1420070400","downs":0,"body":"But Mill's career was way better. Bentham is like, the Joseph Smith to Mill's Brigham Young.","link_id":"t3_2qv6c6","name":"t1_cnas8zw","score_hidden":false,"controversiality":0,"subreddit_id":"t5_2s4gt","edited":false,"retrieved_on":1425124282,"ups":3,"author_flair_css_class":"on","gilded":0,"author_flair_text":"Ontario","subreddit":"CanadaPolitics","parent_id":"t1_cnas2b6"}

About the important featues of data:
1)every object has a unique "name".
2)It has a "body" which is nothing but the comment text.
3)It has score which is no.of votes/like.
4)It has a "parent_id" which is the "name" of its parent comment.
5) "subreddit" which is the topic to which the comment belongs.
6)the file is about 15gb

About the reddit_chatbot_create_database .ipynb
1) It creates parent comment and child comment pairs(with highest score) and stores them in a database.
2)The headers are "pcomment"-parent comment,"comment"-child comment,"score"-likes/upvotes,"comment_id"-name,"parent_id"-parent comment id,"subreddit"-subreddit of the comment
3)DB file is created using sqlite3
4)the file is about 2 gb
5)One can select their favorite topic and train the chatbot on that particular topic.(cool isn't it?)

About the NMT with attention on 10000 pairs.ipynb
1)data preprocessing,starting from tokenisation, then onehotencoding,padding to fedding it to NMT.
2)Results not accurate as desired, still in progress.

credits:sentdex youtube channel
