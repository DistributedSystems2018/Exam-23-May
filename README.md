# Exam

## Rules:

### Conduct

* You are not allowed to use any sort of chatting tool and any other electronic device than the University computer, failing to follow this rule fails the student from the course and may be subject of sanctions in the form of the University rules.
  * Acts that put the student behavior under suspicious will cancel the exam and the student will be subject to a new exam under fully-controlled environment.

* The only allowed websites are Google (for search), the official Oracle documentation and Github (including previous classes).

* Equal or similar exams cancel both exams.

* In case of misconduct, the examiner will not, at any time, take arguments in consideration during the exam. The student exam is cancelled, the student is notified and, in case the student does not agree, the decision must be appealed after the exam.


### Exam Rules
* You can use methods that you find convenient/better (e.g. different Serialization) as far as you fulfill the requirements (e.g. send a full object, create an RMI server etc)

* In case of retake, the greatest grade is the valid one

* The exam must be finished 10 minutes prior the lab reservation is over (i. e. 9:50)

* With the exam grades there will be the time and place to re-check the exam with the examiner.

* When finishing the exam, you must send this assignment to ferrari@caesar.elte.hu with copy to svu938@inf.elte.hu. **for performing it, you shall call the examiner**.
  * The usage of e-mail tools without the examiner supervision is forbidden.

## Rock-paper-scissors game

Your task is to develop a Rock-Paper-Scissors game. This revolutionary game is transparent so, all the users will always set their hands to the server, which will exchange the given hand with the other user. The user will then check out if he won or not using a second server.

How it works step-by-step:
* The user connects to the server and send his hand object which stores an option (paper -p , scissor -s or rock - r). For making it simple we use only the first letters.

* The server accepts two users, receives one object **Hand** from each of them and exchange the objects.

* The client receives back the hand selected by its opponent and makes a RMI call to **WinnerChecker**, sends the options and receives a String result with a text saying if the user won, draw or lost.


## 2 Points

* Adapt the class **Hand** so that its instances can be sent over the network
* Create a **Client** class that connects to one **Server**
* Create a **Server** class that accept two **Client** connections
* Make the **Server** exchange two instances of **Hand** between the two different clients
* Using the empty constructor of **Hand**, send it to the **Server**
* Read the two objects and print their information in the Client console (e.g., but not necessarily, "you played s your opponent played p")

## 3 Points
* Adapt the class **DeclareWinnerInterface** so that it can be used as a remote interface
* Adapt the class **DeclareWinner** so that you can call its methods using RMI

## 4 Points
* Deploy one object of **DeclareWinner** in a RMI service, call this service *verifyWinner*


## 5 Points
* Develop the **Server** using a multithread context, develop one thread for every dispute (i.e. two Clients)
