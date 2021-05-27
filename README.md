# PrimeNumberCalculatorScript
Java script that calculates given amount of primenumbers.
Notes: The code could be refactored more by splitting in to smaller functions and optimized.

Work is based on code from here https://www.javatpoint.com/prime-number-program-in-java
```Java
public class PrimeSearcher{

   static boolean checkPrime(int n){  
       //System.out.println("checking prime: "  + n + " -> "); 
      int i,m=0;
      boolean prime=true;      
      m=n/2;      
      if(n==0||n==1){  
       //System.out.println(n+" is not prime number");  
       return false;
      }
      else{  
         for(i=2;i<=m;i++){      
             if(n%i==0){      
                 //System.out.println(n+" is not prime number");      
                 prime=false;  
                 return false;
            }      
       }      
       if(prime==true)  { 
           System.out.println(n+" is prime number"); 
           return true;
        }  
      }//end of else  
      return false;
    }  
     public static void main(String args[]){   
    
        //How many primes to get
        int amountOfPrimesToGet = 100;
        

        int amountOfPrimesFound = 0;
        int primeCandidate = 0;
        System.out.println("Getting " + amountOfPrimesToGet + " primes"); 
        System.out.println("------------------------------------------");
        
        while (amountOfPrimesFound < amountOfPrimesToGet){
             if(checkPrime(primeCandidate)){
                 amountOfPrimesFound +=1;
             }
             primeCandidate++;
         }
    }    
}
```
