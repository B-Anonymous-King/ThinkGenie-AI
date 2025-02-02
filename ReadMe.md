write the code in your vs code
##create a virtual environment
python -m venv myenv
##activate the virtual environment
\myenv\Scripts\activate


#Install libraries
pip install streamlit 
pip install google.generativeai

#Enter Your api key(Optional)
$env:GEMINI_API_KEY="enter your api key here - Use gemini-1.5-flash for free"  #for custom api everytime



#run the programme
streamlit run AI.py


###Note:
--> You cannot execute the programme directly, run the "streamlit run AI.py" in terminal
--> Make sure you have the required libraries installed in your virtual environment

--> If still it is showing error like the below
"API key not found. Set the GEMINI_API_KEY environment variable."

Go to settings, environment variable
create new add variable name as GEMINI_API_KEY
paste your api key in value

streamline run <paste the path of the file>
#(Not the relative path)


