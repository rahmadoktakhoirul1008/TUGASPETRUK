#include <iostream>
#include <cstring>

using namespace std;


int main(){
int carikata,cek,ditemukan;
ditemukan=0;
char input[100];
cout<<"\tGAME FIND WORD"<<endl;
char kata[15][15]={ 				{'t','g','b','w','w','i','n','t','e','r','w','s','e','s','n'},
						{'a','a','u','n','t','t','m','m','h','f','o','o','d','n','b'},
						{'j','l','w','c','q','l','d','z','m','p','m','v','d','m','r'},
						{'a','s','a','g','m','q','u','w','v','v','b','s','o','h','i'},
						{'b','w','p','l','o','t','a','n','a','d','t','p','g','n','c'},
						{'r','e','w','n','g','o','d','j','c','p','n','a','t','n','k'},
						{'e','e','o','t','w','o','s','b','q','h','a','r','r','s','a'},
						{'a','z','c','g','e','s','w','e','w','n','a','k','n','p','b'},
						{'d','i','n','n','e','r','q','o','d','l','w','d','c','a','r'},
						{'o','n','o','p','k','w','m','p','a','r','k','t','z','c','c'},
						{'q','b','f','r','o','g','m','a','m','w','p','w','e','e','y'},
						{'l','q','z','q','n','n','m','r','z','j','j','s','c','l','g'},
						{'m','o','s','g','z','c','z','e','t','d','b','o','o','t','o'},
						{'p','d','c','r','z','m','s','n','g','r','d','n','r','p','z'},
						{'o','h','n','k','z','w','a','t','e','r','j','g','t','r','a'}
						};
								
for(int i=0;i<15;i++){
for (int j=0;j<15;j++){
cout<<kata[i][j]<<" ";
}
cout<<endl;
}		
	
	
	
	///////////////////////// 
in:	
cout<<endl;cout<<"masukkan 3 kata"<<endl;
for(int i=0;i<1;i++){							//input kata
cout<<"Masukan kata : ";cin>>input;
}
	
	
		
carikata=strlen(input);					
										
for (int i=0;i<15;i++){
for (int j=0;j<15;j++){
if (input[0]==kata[i][j]){
				
for (int a=0;a<carikata;a++){						///HORIZONTAL KANAN 
	if (input[a]==kata[i][j+a]){
	cek=a;
	}
	else{
	break;
	}
}
	if (cek==carikata-1){
	ditemukan+=1;
	}
	else{
	ditemukan+=0;
	}
	cek=0;
				
				
for (int k=0;k<carikata;k++){						///HORIZONTAL KIRI
	if (input[k]==kata[i][j-k]){
	cek=k;
	}
	else{
	break;
	}
}
	if (cek==carikata-1){
	ditemukan+=1;
	}
	else{
	ditemukan+=0;
	}
	cek=0;
								
				
for (int k=0;k<carikata;k++){						///VERTIKAL BAWAH
	if (input[k]==kata[i+k][j]){
	cek=k;
	}
	else{
	break;
	}
}
	if (cek==carikata-1){
	ditemukan+=1;
	}
	else{
	ditemukan+=0;
	}
	cek=0;
				
				
for (int k=0;k<carikata;k++){						///Vertikal ATAS
	if (input[k]==kata[i-k][j]){
	cek=k;
	}
	else{
	break;
	}				
}
	if (cek==carikata-1){
	ditemukan+=1;
	}
	else{
	ditemukan+=0;
	}
	cek=0;

for (int k=0;k<carikata;k++){						//DIAGONAL KIRI ATAS
	if (input[k]==kata[i-k][j-k]){
	cek=k;
	}
	else{
	break;
	}
}
	if (cek==carikata-1){
	ditemukan+=1;
	}
	else{
	ditemukan+=0;
	}
	cek=0;
				
			
for (int k=0;k<carikata;k++){						//DIAGONAL KANAN ATAS
	if (input[k]==kata[i-k][j+k]){
	cek=k;
	}
	else{
	break;
	}
}
	if (cek==carikata-1){
	ditemukan+=1;
	}
	else{
	ditemukan+=0;
	}
	cek=0;
for (int k=0;k<carikata;k++){		//DIAGONAL KIRI BAWAH										
	if (input[k]==kata[i+k][j-k]){
	cek=k;
	}
	else{
	break;
	}
}
	if (cek==carikata-1){
	ditemukan+=1;
	}
	else{
	ditemukan+=0;
	}
	cek=0;
				
for (int k=0;k<carikata;k++){						//DIAGONAL KANAN BAWAH						
if (input[k]==kata[i+k][j+k]){
	cek=k;
	}
	else{
	break;
	}
}
	if (cek==carikata-1){
	ditemukan+=1;
	}
	else{
	ditemukan+=0;
	}
	cek=0;
				
}	
}
}

	
for(int i=0;i<1;i++){	
	if(ditemukan>0){
		cout<<"ADA";
	
}
else {
	cout<<"TIDAK ADA";
}	cout<<endl;
}
system ("pause");
goto in;
return 0;
}
