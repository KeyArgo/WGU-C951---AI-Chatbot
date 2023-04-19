# WGU-C951---AI-Chatbot

Introduction to Artificial Intelligence – C951
NIP2 TASK 1: CHATBOT
A. Explain the functionalities of the chatbot and how they will meet the needs described in the 
scenario.
The chatbot will help the user find a potential career path based on their degree in Computer Science. 
It will determine their interests by asking a series of questions that help identify the user’s best career 
placement within the development, networking, security, management, or support. This satisfies the 
scenario’s requirements of developing a conversational agent in the Pandorabot environment that 
can interact with students who are about to graduate and assist them with identifying their ideal job
description to determine a career to pursue.
B. Identify five computing job types that your chatbot can recommend based on student 
interaction with the chatbot.
a. Front End/Back End or Database Developer
b. IT Technician or System Administrator
c. Cyber Security Analyst
d. IT Director or Program Manager
e. Network Engineer or Administrator
C. Provide the generated chatbot code files to support the five identified job types from part B.
<?xml version="1.0" encoding="UTF-8"?>
<aiml version="2.0">
 
 <category>
 <pattern>start</pattern>
 <template>Hello! I am a Computer Science career bot. Would you like help 
determing which career to pursue based off your personal interests?
 <button>
 <text>Yes</text>
 <postback>interests</postback>
 </button>
 <button>
 <text>No, I'd like to exit chat</text>
 <postback>exit</postback>
 </button> 
 </template>
 </category>
 
 <category>
 <pattern>hello</pattern>
 <template>Hello! I am a Computer Science career bot. Would you like help 
determing which career to pursue based off your personal interests?
 <button>
 <text>Yes</text>
 <postback>interests</postback>
 </button>
 <button>
 <text>No, I'd like to exit chat</text>
 <postback>exit</postback>
 </button> 
 </template>
 </category>
 
 <category>
 <pattern>hi</pattern>
 <template>Hello! I am a Computer Science career bot. Would you like help 
determing which career to pursue based off your personal interests?
 <button>
 <text>Yes</text>
 <postback>interests</postback>
 </button>
 <button>
 <text>No, I'd like to exit chat</text>
 <postback>exit</postback>
 </button> 
 </template>
 </category>
 
 <category>
 <pattern>exit</pattern>
 <template>Thank you for stopping by!
 </template>
 </category>
 
 <category>
 <pattern>itquestion</pattern>
 <template>Do you like coding?
 <br></br><br></br>
 <button>
 <text>Yes</text>
 <postback>codingquestion</postback>
 </button>
 <button>
 <text>No</text>
 <postback>nextquestion</postback>
 </button>
 </template>
 </category>
 <category>
 <pattern>developer</pattern>
 <template>You should consider being a Front, Backend or Database Developer.
 <br></br><br></br>
 <button>
 <text>Restart Bot</text>
 <postback>start</postback>
 </button>
 <button>
 <text>Exit</text>
 <postback>exit</postback>
 </button>
 </template>
 </category>
 <category>
 <pattern>networkingquestion</pattern>
 <template> Do you prefer working with routers and switches, or securing 
computer networks from bad actors?
 <button>
 <text>Working with routers and switches</text>
 <postback>networking</postback>
 </button>
 <button>
 <text>I want to protect networks</text>
 <postback>cybersecurity</postback>
 </button>
 </template>
 </category>
 
 <category>
 <pattern>networking</pattern>
 <template> You should consider being a Network Engineer or Administrator.
 <br></br><br></br>
 <button>
 <text>Restart Bot</text>
 <postback>start</postback>
 </button>
 <button>
 <text>Exit</text>
 <postback>exit</postback>
 </button>
 </template>
 </category>
 
 <category>
 <pattern>cybersecurity</pattern>
 <template> You should consider being a Cyber Security Analyst.
 <br></br><br></br>
 <button>
 <text>Restart Bot</text>
 <postback>start</postback>
 </button>
 <button>
 <text>Exit</text>
 <postback>exit</postback>
 </button>
 </template>
 </category>
 
 <category>
 <pattern>it</pattern>
 <template> You should consider being an IT Technician or System Administrator.
 <br></br><br></br>
 <button>
 <text>Restart Bot</text>
 <postback>start</postback>
 </button>
 <button>
 <text>Exit</text>
 <postback>exit</postback>
 </button>
 </template>
 </category>
 
 
 <category>
 <pattern>interests</pattern>
 <template>To get to know you and your interests better, I will ask you a few 
questions.
 <br></br><br></br>
 Do you enjoy coding?
 <button>
 <text>yes</text>
 <postback>codingquestion</postback>
 </button>
 <button>
 <text>No</text>
 <postback>nextquestion</postback>
 </button>
 </template>
 </category>
 <category>
 <pattern>codingquestion</pattern>
 <template>Would you prefer a job where you code all day, occasionally or not at 
all?
 <br></br><br></br>
 <button>
 <text>All Day</text>
 <postback>developer</postback>
 </button>
 <button>
 <text>Ocassionally</text>
 <postback>nextquestion</postback>
 </button>
 <button>
 <text>Not all all</text>
 <postback>nextquestion</postback>
 </button>
 </template>
 </category>
 <category>
 <pattern>management</pattern>
 <template> You should consider being an IT Director or Program Manager.
 <br></br><br></br>
 <button>
 <text>Restart Bot</text>
 <postback>start</postback>
 </button>
 <button>
 <text>Exit</text>
 <postback>exit</postback>
 </button>
 </template>
 </category>
 
 <category>
 <pattern>nextquestion</pattern>
 <template> Do you enjoy working with routers and switches? 
 <button>
 <text>yes</text>
 <postback>networkingquestion</postback>
 </button>
 <button>
 <text>No</text>
 <postback>nextquestion2</postback>
 </button>
 </template>
 </category>
 
 <category>
 <pattern>nextquestion2</pattern>
 <template> Do you think of yourself as a leader or a team member?
 <button>
 <text>Leader</text>
 <postback>management</postback>
 </button>
 <button>
 <text>Team Member</text>
 <postback>nextquestion3</postback>
 </button>
 </template>
 </category>
 
 <category>
 <pattern>nextquestion3</pattern>
 <template> Do you enjoy helping people with their IT problems?
 <button>
 <text>Yes</text>
 <postback>it</postback>
 </button>
 <button>
 <text>No</text>
 <postback>nextquestion4</postback>
 </button>
 </template>
 </category>
 
 <category>
 <pattern>nextquestion4</pattern>
 <template> You should reconsider your career path outside of information 
technology. Computer Science though generally used for IT and science related fields 
is a very ambidextrous degree. Consider career paths in public service, Math, 
teaching or get creative. Thank you for using the WGU IT Advice Bot. Come back 
anytime!
 <button>
 <text>Restart Bot</text>
 <postback>start</postback>
 </button>
 <button>
 <text>Exit</text>
 <postback>exit</postback>
 </button> 
 </template>
 </category>
</aiml>
D. Explain how the chatbot training cases were selected and how you used artificial intelligence 
markup language (AIML) to enhance the functionality of the chatbot. Provide examples of 
the chatbot’s functionality that represent the selected cases at the end of the training 
process in support of your explanation.
Training cases were selected by picking students who were either very interested in 
programming, moderately interested in programming, or not interested in 
programming at all. For those that were interested in programming full-time, a career 
in development was recommended. Those who were not interested in developing 
full-time were asked additional questions to direct towards networking, security, 
leadership, or a support role. 
I used AIML to ensure that students don’t get stuck asking questions the chatbot does 
not recognize, wasting time and causing user frustration. Initially, I wrote the code to 
allow a more humanlike interaction, but quickly found running test cases and knowing 
the right questions to ask that it was easy to confuse the bot which I found irritating
to deal with and to account for. The end-user would be much less forgiving. 
Knowing such a bot would require many students to test different questions and 
contexts I didn’t foresee; I abandoned this style of a chatbot for a more directed 
approach. There is more than one way to direct the conversation, however, I found 
the selectable answer method the most user-friendly.
Case 1: Mike is a student who enjoys programming but doesn’t want to do it full-time 
or as the primary job. He enjoys networks and prefers to secure them.
Answer: The chatbot will eliminate a career in development from the 
recommendations. It will ask him about his interests in networking and securing 
networks and will recommend a career as a Cyber Security Analyst.
Case 2: John is a student who enjoys programming and would like to do it as a fulltime job.
Answer: The chatbot will recommend John consider a career path in Front End/Back 
End or Database Developer
E. Create an installation manual for the chatbot that includes the web link to access the live 
chatbot in the Pandorabot platform.
1. Through a browser, log into pandorabots.com or register for a new 
account, then login.
2. Go to https://home.pandorabots.com/dash/bot-directory.
3. In the search bar type: BSCS_Career_Advisor
4. Click on the “BSCS_Career_Advisor listing
5. Click the orange message button at the bottom right of the screen
6. In the chat box type “Hi” or “Hello” or “Start” to begin bot
F. Assess the strengths and weaknesses of the chatbot development environment and explain 
how they supported or impeded the construction of the chatbot.
Strengths: Easy creation and deployment a chatbot
Weaknesses: Chatbot development interface could implement a GUI to easily employ different AIML 
functions to allow increased useability and AI functionality. Currently, the user is expected to know 
or research how to use AIML.
While it was easy to create and deploy a chatbot, there was no assistance with its development. 
Additional assistance with development can create stronger and more complex chatbots by providing 
a more polished user interface.
G. Explain how the chatbot will be monitored and maintained to improve the final user 
experience.
Requests for feedback from students will be emailed in survey form. We will allow the student to 
leave a few sentences on what can be improved upon to better assist them and other students in the 
future. Additional questions can be then added to improve the direction the career bot descends the 
question tree.
H. Provide a Panopto video recording that includes a verbal summary of the capabilities of your 
chatbot and an example of human interaction with the chatbot in which it provides 
meaningful career advice.
https://wgu.hosted.panopto.com/Panopto/Pages/Sessions/List.aspx#folderID=%22fe1bc53a-a660-
4c5e-addb-a8ef01259bdc%22
