# dividers
finds numbers' dividers

#include <iostream>
#include <cmath>
#include <vector>

using namespace std;

int main(){
	
	int n;
	cin >> n;
	
	vector <int> list;
	for (int i = 1; i <= sqrt(n); i++){
		
		if (n % i == 0){
			
			list.push_back(i);
			if (n/i != i) list.push_back(n/i);
		}
	}
	
	for (int i = 0; i < list.size(); i++)
		cout << list[i] << " ";
}
