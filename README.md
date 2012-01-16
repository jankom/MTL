#J4M

Simple bash/*ix based backend for notes/todo tool for my work. Inspired partially by `how I imagine github works`. 

On top of it a parser will be built based on ideas from http://www.qwikitodo.com and other prototypes I made.


##State

We are making the basic backend work. On a proof of concept level we prooved it can work OK, so we are making it 
usable so we can start using as soon as possible (and then develop further). 


##Next

+ make the scripts work from /usr/bin .. by finding j4m dir in current or parent dirs or user home dir.
+ rename them to j4m_*** and make a command j4m *** work like invfox
- make a basic asortment of scripts really work w/ usage some err checking
+ make some inital way of cooperative work (so I can share this with colegue already) we have j4m sync
- use!!!
- ...


##Current commands

Things will of course get streamlined and automated as much as it makes sense. This is heavily WIP!

	  #cd to the dir of your project
	  j4m init   	    	#creates the .j4m dir structure
	  j4m create work	#creates doc work in .j4m dir and index/src files
	  j4m link work 	#creates a local symlink to the doc so you can edit it like local file
	  emacs work		#edit the file
	  j4m store work	#store the changes to the index
	  emacs work		#edit the file
	  j4m diff work		#compare the working file with last stored
	  j4m store work	#store the changes again
	  j4m log work		#show the log of stores
	  j4m cat work		#cat the last stored version (TODO: same numbers logic as diff and get)
	  emacs work		#make bad changes
	  j4m diff work 0	#compare working to last stored
	  j4m diff work 0 1	#compare the last 2 stored
	  j4m get work	  	#set working version from the last stored version
	  j4m get work 1	#set working version from previously stored version
	  j4m create urgent	#create new doc
	  j4m ls		#list the docs
	  
	  #first commands for the coop work
	  j4m sync /home/projectx/work	  	#2way sync all docs with another repo
	  j4m sync projectx@work.com:~/work	#2way sync all docs with remote repo over ssh

##Current plans

- improve all commands, add minimal argchecking
- START USING!!!
- make a dialect parser for notes/todos (this will enable additional context related commands)
- make some basic emacs more for j4m and notes/todos dialect
- think how to streamline/automate commands

##License

GNU GPL v2