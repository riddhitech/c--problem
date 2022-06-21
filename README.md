# c-problem
question:
chef and Chefina are residing in a hotel.

There are 10 floors in the hotel and each floor consists of 10 rooms.

Floor 1 consists of room numbers 1 to 10.
Floor 2 consists of room numbers 11 to 20.
......
Floor i consists of room numbers 10*(i-1)+1 to 10*i.
You know that Chef's room number is X while Chefina's Room number is Y.
If Chef starts from his room, find the number of floors he needs to travel to reach Chefina's room.
solution:
#include<iostream>

using namespace std;

int main() {
	
	int n , x ,y , p ,q;
    cin >> n;
	while(n--){

	cin >> x >> y; 

	
	    int i = 1; 
	    while(i <= 10) {  
	        
	    if(((10*(i-1))+1) >= y && y <= (10*i)){
	        
	         p = i; //p= 1
             break;
	    }
	    else{
	    i++;
	    }
	}
	
		    int j = 1; 
		    while(j<=10){
		    
	    	    if(((10*(j-1))+1) >= y && y <= (10*j)){ 
	    	        
	      q = j;//q=10
	      break;
	    }
	    else{
	    j++;
	    }    
	}
	if(p>q)
	cout << (p-q) << endl;
	else
	cout << (q-p) << endl; 

}	
	return 0;
}
