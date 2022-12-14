# Course class
import java.util.ArrayList;
public class Course {
		  private String course;
	    static ArrayList<String> studentNames=new ArrayList<String>();
	    static ArrayList<Student> student=new ArrayList<Student>();
	    
	    public Course(String course)
		{
	    	this.course = course;
	    }
	    public void addStudent(Student enroll){
	        studentNames.add(enroll.getName());
	        student.add(enroll);
	    }
	    public ArrayList roll(){
	        return studentNames;
	    }
	    public int average(){
	        int avg=0;
	        for(Student tester:student){
	            avg+=tester.average();
	        }
	        return avg/student.size();
	    }
}

# main
    Address school = new Address("800 Lancaster Ave.", "Villanova", "PA", 19085);
    Address jHome = new Address("21 Jump Street", "Blacksburg", "VA", 24551);
    Student john = new Student("John", "Smith", jHome, school, 90,70,80);
    Address mHome = new Address("123 Main Street", "Euclid", "OH", 44132);
    Student marsha = new Student("Marsha", "Jones", mHome, school,90.3,90,70);

		System.out.println(john);
		System.out.println();
		System.out.println(marsha);
		System.out.println(marsha.average());
		
		Course math = new Course("math");
		math.addStudent(marsha);
		math.addStudent(john);
		System.out.println(math.roll());
		System.out.println(math.average());
