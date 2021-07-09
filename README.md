# ▶️ Weather-Forecast-App ⛅
✅ Check the deployed project [here](https://weatherapp-avp.herokuapp.com/).
## ⭕ Introduction:
A weather forecast app is web-based application to get weather updates and any other climatic changes.
In this project, I've made a weather forecast application using **Streamlit**  and **PYOWM** libraries in Python and then deploy the project on Heroku platform which is absolute free hosting platform.

>**Concepts used in this project:**
* Application Development
* API calls
* Data Visualisation
* GitHub Integration (Heroku GitHub Deploys)

## ⭕ Features:
* Getting Weather forecast using Open Weather API
* City name based querying
* Parameters: Temperature, Wind speed, Cloud coverage, Sunrise & Sunset time, Graphical representation

## ⭕ Prerequisites:
>**Tools & Technologies used:**
* Python 
* [Streamlit](https://streamlit.io/)
* [Open Weather Map](https://openweathermap.org/)
* Matplotlib
* [PYOWM]((https://pyowm.readthedocs.io/en/latest/))
* [Heroku](https://www.heroku.com/free)

>Installation Guide:
``
pip install streamlit
`` 
``
pip install pyowm
``
``
pip install matplotlib
``
## ⭕ Steps:
>Divided Steps into two:

``A. Scripting in Python``
```
Step1: Firstly, Install all the required packages mentioned above and go through the respective documentation.
Step2: We have to register an account on https://openweathermap.org/ and generate an API Key.
       Note: I have used Current Weather Data, But you can use different kinds of API's and upgrade your app.
Step3: Here we initialize Pyowm with an API key.
Step4: We take the city Name as input and call the weather_manager() instance to fetch the weather data for that place.
       -Unlike the previous step where we called the temperature values, now we call the clouds and the wind functions.
       -Similarly, like the previous ones, to get the sunset and sunrise time,
        we call the sunset_time(‘iso’) and sunrise_time(‘iso’) functions of the weather object.
Step5: Now, let’s start with the FUN Part: Making the Python Web App using streamlit.
       -Streamlit has various unique methods to call for like title, header, textbox, buttons etc.
       -Read the streamlit documentation and explore other options and try to make it more interactive.
Step6: Plotting Graphs and Calculations using matplotlib.
       -The plot_line() and plot_bar() function is called by the our weather_detail() function.
       -The ‘days’ list that is passed contains the values in an encoded representation which we won’t understand. 
       -Hence to convert it into human- perceivable format, we use the dates.date2num and the set_major_formatter() function.
       -Now as per the user input we get the graphs plotted using the plt.plot(for line graph) and plt.bar(for bar graph). 
       -To print the graphs in Streamlit we use the st.pyplot() just like our standard plt.show(). 
       -At the end plt.clf() is used to clear the graphs making space for the next graph to be printed.
```

``B. Deployment``
```
Note: We're going to deploy our web application Heroku Platform. Deployment via Github Intergration is easy compared to other options.

Step1: Before beginning to deploy the app, there are very important steps that need to be followed in order to avoid errors ahead.
       - Create a requirements.txt file and write all the packages used in the project including their versions. Ex. pyowm==3.0.0
       - Create a runtime.txt file and include your python version in it. 
         Check https://devcenter.heroku.com/articles/python-support#supported-runtimes for supported
         versions of python by HEROKU app.
       - Create a Procfile which consist of command for the Heroku Server.
         Copy the following command to Procfile - [web: sh setup.sh && streamlit run script.py] 
       - Create a Setup.sh file that'll hold a command to create a directory in heroku platform.
         Check https://github.com/ColonelAVP/Weather-App/blob/master/setup.sh and copy the following code to the setup.sh file
Step2: Create a Github repository.
Step3: Create your account on Heroku Platform and login to it. Create a new project on Heroku.
Step4: Click deploying app and select Github Integration. Also connect Github to Heroku.
Step5: In manual deploy, Finally Click Deploy and wait till it gives you textbox to view deployed app.
```

## ⭕ References:
- [Open Weather Map](https://openweathermap.org/)
- [Streamlit docs](https://docs.streamlit.io/en/stable/)
- [Heroku deployment](https://devcenter.heroku.com/categories/deployment)
- [Blog](https://towardsdatascience.com/a-quick-tutorial-on-how-to-deploy-your-streamlit-app-to-heroku-874e1250dadd)

## ⭕ Contributions:
Contributions are always welcomed. Make sure you read the [Contribution](https://github.com/ColonelAVP/Weather-App/blob/master/Contribution.md) info before making pull request.

## ⭕ Screenshots:
![alt tag](https://raw.githubusercontent.com/ColonelAVP/Weather-App/master/IMG/1.1.png)
![alt tag](https://raw.githubusercontent.com/ColonelAVP/Weather-App/master/IMG/1.4%20(2).png)
![alt_tag](https://raw.githubusercontent.com/ColonelAVP/Weather-App/master/IMG/1.2%20(2).png)
![alt_tag](https://raw.githubusercontent.com/ColonelAVP/Weather-App/master/IMG/1.3%20(2).png)

