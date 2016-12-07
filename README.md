# ChatBot-Final
/**
 * Write a description of class CounselorChatbot here.
 * 
 * @author (your name) 
 * @version (a version number or a date)
 */
import java.util.Scanner;
import java.util.List; 
import java.util.ArrayList;
import java.lang.*;


public class CounselorChatbot
{
    // instance variables - replace the example below with your own
    private int x;


    /**
     * Constructor for objects of class CounselorChatbot
     */
    public CounselorChatbot()
    {
        // initialise instance variables
        x = 0;
    }


    /**
     * An example of a method - replace this comment with your own
     * 
     * @param  y   a sample parameter for a method
     * @return     the sum of x and y 
     */
    public void main()
    {
        Scanner user_input = new Scanner( System.in );
        System.out.println("Hello, How can I help you?");
        System.out.println("For help with classes, type in \"classes\"");
        System.out.println("For help with a transcript, type in \"transcript\"");
        System.out.println("For help with dropping classes, type in \"dropping class\"");
        System.out.println("For help with grades, type in \"grades\"");
        System.out.println("If you are done with me or you simply don't want to look at me,type in \"exit\"");
        String utility = user_input.next();
        if (utility.equals("classes")){
            Classhelp();
        }
        else if (utility.equals("transcript")){
            Transcripthelp();
        }
        else if (utility.equals("dropping classes")) {
            Droppinghelp();
        }
        else if (utility.equals("grades")) {
            Gradehelp();
            
        }
        else if (utility.equals("exit")) { 
            System.out.println("Close me now!"); 
            System.exit(1);
        }
        else if (utility.equals("joke")) {
            System.out.println("I would give you one, but your life is pretty much one");
        }
        
    }
    public void Classhelp()
    {
        ArrayList<String> messages = new ArrayList<String>(10);
        Scanner user_input = new Scanner( System.in );
        System.out.println("Recount all of your classes"); 
        System.out.println("When done, just type in \"done\"");
        String schoolwork = user_input.next(); 
        if (schoolwork.equals("done")) { 
            System.out.println("Ok, great!");
        }
        else {
            messages.add(schoolwork);
            Classhelp();
        }
        System.out.println("Here is what I got");
        System.out.println(schoolwork);
        //list will be printed in actual version
        //based on grades one of the input options will be displayed
        System.out.println("So your grades are doing well/bad.");
        System.out.println("We should workout a plan for bring your grade up.");
        System.out.println("Have you contacted your teacher yet?");
        String teacher = user_input.next();
        if (teacher.equals("no")) {
            System.out.println("Are you scared of him/her?");
            System.out.println("Teachers always want their students to succeed"); 
            System.out.println("Regardless of your fear go talk to them!"); 
        }
        else if (teacher.equals("yes")) {
            System.out.println("Great! If your teacher gave you any tips to follow, use them.");
            System.out.println("Additionally, if you have any other late work, get it done!.");
        }
        System.out.println("After you have turned in all your stuff lets see what you can do to improve your study habits");
        System.out.println("Do you have a planner.");
        String planner = user_input.next();
        if (planner.equals("no")) {
            System.out.println("I strongly suggest you get one to help you organize your work");
        }
        else if (planner.equals("yes")) {
            System.out.println("Make sure you use it on a regular basis");
        }
        System.out.println("In your planner write down all your homework and test dates every night look at your planner and see what you can do.");
        System.out.println("Lets also get you a tutor to help you. Are you free after school, before school, or at lunch?"); 
        System.out.println("What is your lowest class grade?");
        String courses = user_input.next();
        if (courses.equals("science")) {
            System.out.println("What kind of science");
            String science = user_input.next();
            if (science.equals("Chemistry")) {
                System.out.println("fill in"); 
            }
            else if(science.equals("Biology")) { 
                System.out.println("fill in");
            }
            else if(science.equals("Physics")) {
                System.out.println("fill in");
            }
            else if(science.equals("Forensics")) {
                System.out.println("fill in"); 
                
            }
        } 
        
        else if (courses.equals("math")) {
            System.out.println("What kind of math");
            String math = user_input.next();
            if (math.equals("Algebra I")) {
                System.out.println("fill in"); 
            }
            else if(math.equals("Geometry")) { 
                System.out.println("fill in");
            }
            else if(math.equals("Algebra II")) {
                System.out.println("fill in");
            }
            else if(math.equals("Pre-Calculus")) {
                System.out.println("fill in"); 
                
            }
            else if(math.equals("Statistics")) {
                System.out.println("fill in"); 
                
            }
            else if(math.equals("Calculus")) {
                System.out.println("fill in"); 
                
            }
        }    
           
        else if (courses.equals("Spanish")) { 
            System.out.print("fill in");
           }
        else if (courses.equals("French")) { 
            System.out.print("fill in");
            }
        else if (courses.equals("French")) { 
            System.out.print("fill in");
            } 
        
       
       System.out.println("Pay most attention to this grade and be considerate of how you handle work for this class");
       System.out.println("Let's stick with this plan for a few weeks and see from there what else we can do.");
       //more code option will be added but not provided here due to time constraints
       System.out.println("Thank you for stopping by and asking. BYE.");           
       main(); 
    }
    public void Transcripthelp()
    {
        Scanner user_input = new Scanner( System.in );
        System.out.println("Great I am glad to hear that your grades got you into a great college.");
        System.out.println("I would be glad to send your transcript to your school");
        System.out.print("What is the school that you are going to?");
        String college_name = user_input.next();
        System.out.print("That is fantastic!"); 
        System.out.print("Your transcript will reach them by 6:00 tonight");
        System.out.print("Have a great day and congrats once again."); 
        main();
    }
    public void Droppinghelp()
    {
        Scanner user_input = new Scanner( System.in );
        System.out.println("What class would you like to drop");
        System.out.println("If you would not mind, may I ask why you would like to drop that class");
        System.out.println("You have a good/bad grade in (class), why are/aren't you dropping/keeping class");
        System.out.println("Would you like to carry forward and drop the class?");
       //If yes: class has been dropped; If no: code resets
       main(); 
    }
    public void Gradehelp()
    {
       Scanner user_input = new Scanner( System.in );
       System.out.println("Ok great! Lets take a look at your grades.");
       System.out.println("So your grades are doing well.");
       System.out.println("So what do you plan to do to keep them up.");
       String grade_val = user_input.next();
       System.out.println("Ok that sounds great is there anything else you can do, because you are at the board line in some classes");
       System.out.println("So here something you can do; Contact your teacher ask if there is any extra credit opportunity and if there is make sure you do it to secure your grade.");
       System.out.println("Great hope to see you soon!");
       main();
    }
    
}
