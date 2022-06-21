# c-problem
question:
chef and Chefina are residing in a hotel.

There are 1010 floors in the hotel and each floor consists of 1010 rooms.

Floor 11 consists of room numbers 11 to 1010.
Floor 22 consists of room numbers 1111 to 2020.
\ldots…
Floor ii consists of room numbers 10 \cdot (i-1) + 110⋅(i−1)+1 to 10 \cdot i10⋅i.
You know that Chef's room number is XX while Chefina's Room number is YY.
If Chef starts from his room, find the number of floors he needs to travel to reach Chefina's room.
solution:
#include<iostream>

using namespace std;

int main() {
	// your code goes here
	int n , x ,y , p ,q;
    cin >> n; //1
	while(n--){

	cin >> x >> y; //1 100

	
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
	cout << (p-q) << endl; //3 1
	else
	cout << (q-p) << endl;  //9 0

}	
	return 0;
}
