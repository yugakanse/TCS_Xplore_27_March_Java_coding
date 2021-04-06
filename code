// "static void main" must be defined in a public class.
import java.util.Scanner;
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Employee[] rg = new Employee[4];
        for(int i =0;i<4;i++){
            int employeeId = sc.nextInt();
            sc.nextLine();
            String name = sc.nextLine();
            String branch = sc.nextLine();
            double rating = sc.nextDouble();
            sc.nextLine();
            boolean companyT= sc.nextBoolean();
            sc.nextLine();
            rg[i] = new Employee(employeeId, name , branch, rating, companyT);
        }
        String input=sc.nextLine();
        int y =findCountOfEmployeesUsingCompT(rg,input);
        if(y==0){
            System.out.println("no such employee");
        }
        else{
            System.out.println(y);
        }
        Employee[] t = findEmployeeWithSecondHighestR(rg);
        if(t==null){
            System.out.println("All Employee using company transport");
        }
        else{
            System.out.println(t[1].getemployeeId());
            System.out.println(t[1].getname());
        }
    }
    public static int findCountOfEmployeesUsingCompT(Employee[] rg, String input){
        int count=0;
        for(int i =0;i<4;i++){
            if(rg[i].getbranch().equalsIgnoreCase(input)){
                count++;
            }
        }
        return count;
    }
    public static Employee[] findEmployeeWithSecondHighestR(Employee [] rg){
        Employee [] help = new Employee[4];
        int j=0;
        for(int i =0;i<4;i++){
            if(rg[i].getcompanyT()==false){
                help[j]=rg[i];
                j++;
            }
        }
        for(int i =0;i<j;i++){
            for(int k=i+1;k<j;k++){
                if(help[i].getrating()<help[k].getrating()){
                    Employee temp = help[k];
                    help[k]=help[i];
                    help[i]=temp;
                }
            }
        }
        return help;
    }
}
class Employee{
    private int employeeId;
    private String name,branch;
    private double rating;
    private boolean companyT;
    
    public int getemployeeId(){
        return employeeId;
    }
    public String getname(){
        return name;
    }
    public String getbranch(){
        return branch;
    }
    public double getrating(){
        return rating;
    }
    public boolean getcompanyT(){
        return companyT;
    }
    public void setemployeeId(int employeeId){
        this.employeeId=employeeId;
    }
    public void setname(String name){
        this.name = name;
    }
    public void setbranch(String branch){
        this.branch = branch;
    }  
    public void setrating(double rating){
        this.rating= rating;
    }
    public void setcompanyT(boolean companyT){
        this.companyT=companyT;
    }
    
    
    public Employee(int employeeId, String name, String branch,double rating, boolean companyT){
        this.employeeId= employeeId;
        this.name= name;
        this.branch=branch;
        this.rating= rating;
        this.companyT=companyT;
    }
}
