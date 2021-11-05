# Cajero-Automatico2.0


#include<iostream>

using namespace std;

int main(){
int saldo_inicial=100, opc, nip; //aqui simnulo que en mi tarjeta hay 100 pesos
float agrego,saldo_actual=0,retiro;

cout<<"\t--------CAJERO AUTOMATICO------"<<endl;


cout<<"Ingrese NIP:\n "; 
cin>>nip;




//menu del cajero
cout<<"1.Ingresar dinero \n";
cout<<"2.Retirar dinero\n ";
cout<<"3.Consultar saldo\n ";
cout<<"4.Salir \n";
cout<<"¿Que tramite desea realizar? \n";cin>>opc;

switch (opc){
	//aqui estan los resultados de las opciones que el usuario elegira
	case 1:
		cout<<"Digite cantidad a ingresar: ";
		cin>>agrego;
		saldo_actual=saldo_inicial+agrego;
		cout<<"Su saldo actual es de \n"<<saldo_actual;
		
		break;
		case 2:
			
			cout<<"Digite la cantidad que desea retirar:\n ";
			cin>>retiro;
			
			if (retiro>saldo_inicial){
				cout<<"Fondos insuficientes \n";
			}
			else{
				saldo_actual=saldo_inicial-retiro;
				cout<<"Dinero en cuenta:\n "<<saldo_actual;
			}
			break;
			case 3:
				cout<<"Su saldo es de \n"<<saldo_inicial;
				
				break;
				case 4:
				
					break;
					
					}

return 0;
}
