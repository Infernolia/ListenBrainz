<html>
<h1>PROJECT: Visualising Statistics and Building A Recommender Engine</h1>
<p>Email:         abolirm@gmail.com<br>
Github: 	https://github.com/Infernolia<br>
Linked In:	www.linkedin.com/in/abolimarathe<br>
Country:      	India<br>
</p>


<p>
PROJECT ABSTRACT
This project aims to contribute to ListenBrainz and thoroughly analyse and implement all the possible enhancements that could make it usable and savvy. I would like to divide my proposal into 2 sections:
Section A:
Improving the current visualisation techniques and adding innovative figures to highlight the statistics in an exciting way.
 Section B:
My own contribution, a complete recommender system and ChatBot for ListenBrainz.
 
PROJECT GOALS
-        To solve maximum number of issues currently faced by the application.
-        To understand the data structure of ListenBrainz thoroughly.
-        To create and implement innovative statistical and graphical visualizations for the user interface.
-        To develop a Recommender System and ChatBot for ListenBrainz users using Collaborative Filtering.
</p>



<p>
 
Here are the suggested statistics that ListenBrainz can incorporate:
(I have added rough figures to depict the nature of the visualisation. The final plots are on github)
 -        Album choice and time correlation for all users
 
 
 
-        Number of albums played by user compared to others in a specific amount of time
 
 
 
-        Top Singers/Bands/Musicians of user
 
 
 
-        Top Language(of Song) heard by User

 
-        Tendency of User to pick a trending song
 
 
This plot requires a combination of data from the leading songs on ListenBrainz, and the best rated songs of the user.

 
-        Graph of variation of genres, moods and other factors for a user over time
 
 
 
 
 
 
-        Time duration of album selected by user
 
 
-        Song topic visualization for user-
This word cloud representation rates song topic words on frequency and displays them to the user.


 
 
Here are some samples of the plots using d3.js:

The choropleth depicts the regions producing music liked by user, and the colour intensity shows the density of albums liked from that region.
 

The circular packing is used to show the popularity of genre, according to the data of user.
 
 
The stacked radial bar graph is being used to show how the data of moods of the songs chosen by user varies. 

This ridge plot is being used to show how the data on genre of music chosen by user varied in a period of time.

This network graph is a colourful representation of different labels in the music data, and their usage on ListenBrainz by all the users. The density of connections shows high popularity for that particular feature.
 
 
The codes for the d3.js plots are present <a href="https://github.com/Infernolia/ListenBrainz">here</a>
 
Along with the generated plots, we can add Correlation Heat maps, Box plots and Pearson Correlation Heat maps and a Classification Report to provide a fully-fledged visualization to the user. One of these visualisation snippets from my personal projects is shown below:
 
We could correlate the popularity of a song, with the danceability, or the genre with the language which can be written on the Python shells of Apache Spark:
 
Here is a code snippet for making the plots:
train_dataset.hist(bins=50,figsize=(20,15))
 
fig, (ax1,ax2) = plt.subplots(1,2, figsize=(20,5))
ax1.scatter(nadropped_train_dataset. danceability, nadropped_train_dataset. genre)
ax1.set(xlabel="danceability ", ylabel="genre")
 
ax2.scatter(nadropped_train_dataset. danceability, nadropped_train_dataset. mood)
ax2.set(xlabel="danceability ", ylabel="mood ")
 

 
ax = sns.heatmap(uniform_data)

</p>

<p>
<B>Dashboard Design</B>
Here is the link for the sample dashboard UI <a href="https://github.com/Infernolia/ListenBrainz/blob/master/UI.png">here</a>.

</p>

<p>
 SECTION B<BR>
RECOMMENDATION SYSTEM<BR>
I propose a collaborative-filtering based recommendation system. The recommendation system lies on the rating column of the data, indicating the user’s liking of the album, recorded and stored in user history.
The recommender system is item-based and not user-based as the data on the music is more likely to provide a basis for filtering the data.
We extract the utility matrix from the main database using SQL shells provided in Apache spark.


The Root Mean Squared Error shall be used to find the accuracy of the trained model, using the dataset currently available, and till the final greatest accuracy is obtained, the correlation factors are tweaked and the model is fine tuned.
The SVD   (Singular Value Decomposition) method will be used to reduce the error to the minimal level. X is the utility matrix, U a left singular and S depicts the strength of latent factors. V transpose is a right singular matrix, indicating the similarity between items and latent factors.


I have created a sample UI for the recommendation system <a href="https://github.com/Infernolia/ListenBrainz/blob/master/RecoSystemUI.png">here</a>.

</p>


<p>
<br>GSOC Timeline
<br>Pre GSOC
<br>I shall be working on implementing and understanding all the functionalities and features of ListenBrainz, and MetaBrainz so I can contribute to it properly. Will touch up my JavaScript which is on the list of skills and make a project to understand the same. Further, I will start working on the tickets, and analysis of the code base of ListenBrainz. I will make a sample data visualization screen format, and send it for approval. After this I will develop a base code for my suggested new recommendation engine, which can be integrated into the original code.
<br>Community Bonding
<br>Getting acquainted with the code base of ListenBrainz and the preferred routines to submit code and get it reviewed. Discussing with the team on where exactly the issues appeared and past methods they’ve used to tackle them. I shall submit some sample codes to the team to be evaluated, and to get feedback on integration with main code. Brainstorm with the community how the implementation will unfold and how to use the resources provided.
<br>Week 1
<br>Understand the relevant parts of the ListenBrainz code base and try to figure out how the final product should look like, the visualisation formats, the front end changes, and the server handling codes. Will start on finding approaches to solve the existing issues, which have not been already thought of.
<br>Week 2
<br>Begin implementing the novel approaches to the problem solving. Will target at least 5-6 issues to be solved by this time.
<br>Week 3-4
<br>Continue working on the issues and will have reached a thorough understanding of the project by this time. Will simultaneously be testing the code, to raise more issues, if any. Start with the visualisation using D3.js, and extracting the data needed using python.
<br>Week 5–6
<br>Aim to finish maximum issues and the dashboard by this week. Will complete the statistics visualisation and get some feedback on the current visualization.
<br>Week 7–8
<br>Finish the dashboard and start extracting the necessary data in the format required for the recommendation system. Simultaneously, start coding for  the collaborative filtering.
<br>Week 9–10
<br>Test all the issues solved and find more if any through rounds of testing. Analyse the efficiency of the recommender system and keep tuning the model. Complete the model with the training data, and begin work on the ChatBot.
<br>Week 11–12
<br>Take feedback from the community and iterate on the designs and improvise on the code. Ensure the dashboard is working and the recommendation engine has reached a deployable stage. Finish the ChatBot backend and integration with the ListenBrainz site.
<br>Week 13
<br>This spare week has been left for any unforeseen circumstances, or unexpected work delay and for the completion of the ChatBot integration.
 
</p>


<p>

 
Personal Information
 
I am a Second Year undergraduate student, pursuing a B.E. degree in the field of Computer Engineering from Pune Institute of Computer Technology, India with a passion for machine learning. 
 
As a part of my curriculum I have taken Advanced Data Structures, Microprocessor, Data Structures and Algorithms, Object Oriented Programming, Computer Organization and Architecture.

Here are some of my latest Open Source group projects:
·       Dynamic Human Authentication for Access Control-DRDO [Shortlisted for SIH 2020]
A video based dynamic human authentication system, using Gait Recognition. Temporal features were extracted across the pose descriptors using LSTM and aggregated into one-dimensional identification vectors which were then classified with linear SVM.
·       Earth-X [Finalist at Shehack 2019]
A complete recommendation system to guide tourists visiting India to purchase handicraft at great deals from authentic vendors based on the trip specifications of the tourist, and his/her general taste in art.
·       Datawiz [IEEE(PISB) Event Credenz 2019]
Predicting the feasibility of an employee getting a job from a vast dataset. The work focused on data science, machine learning and used Python libraries like numpy, matplotlib, seaborn primarily.

Technical Skills
I enjoy coding in my fundamental languages C++, Java and Python and am familiar with NodeJS, HTML, Javascript and Bootstrap. The key web frameworks I have used are Django and Flask. In the field of ML, DL and NLP I have worked extensively with several libraries, tools including Tensorflow,  NLTK,  mlpack ,Spacy  and have worked with AWS, MongoDB and SQL data bases.



<br>My Contributions to the ListenBrainz Community
<br>Username: princessaada
<br>I am an active ListenBrainz member and  have worked on the tickets LB-469 and LB-487,  and determining how to split the test and training datasets for ListenBrainz.  I am currently working on the ticket LB-419.
<br>Question: Tell us about the computer(s) you have available for working on your SoC project!
<br>My laptop is an Asus ROG gaming laptop with an Intel i7-8750H  processor, 1 TB HDD and 256 GB SSD, 8 GB RAM, dual booted with Windows 10 and Ubuntu 16.04. It has a 4 GB Nvidia GeForce GTX 1050 Ti Graphics card. I also have a working Dell Inspiron 3000 with i3 core and 8GB ram in case of emergencies.
<br>Question: When did you first start programming?
<br>I started programming in 4th grade when we were introduced to the basics of LOGO and Scratch animation. We then progressed to HTML concepts and then C. In 10th we started Java and DBMS. I loved programming from the very first Scratch animation I designed!
<br>Question: What type of music do you listen to?
<br>My playlists have a wide variety of songs from Classical Hindi Shastriya sangeet, which was played by generations of my family to contemporary pop. Some of my favorite singers are Taylor Swift, Sia, Khalid and Avicii with their catchy beats!
<br>Question: Have you ever used MusicBrainz to tag your files?
<br>Yes,  I have used MusicBrainz Picard in the past to tag files.




</p>


</html>
