#include<iostream>
#include <stdio.h>
#include <stdlib.h>
using namespace std;
int main(){
int saldo_inicial=1000, opc, nip, resp, movimi,recarga,z,inte; //aqui simnulo que en mi tarjeta hay 100 pesos
float agrego,saldo_actual=0,retiro,x,y,donar;
char num[]={1234567890};
string usuario,contra, nueva;
int estatus=0,intentos=0;
cout<<"\t--------CAJERO AUTOMATICO------"<<endl;	

while(intentos=1){
cout<<"Usuario: \n"; cin>>usuario;
	cout<<"Contrasena:\n"; cin>>contra;
intentos++;
	if (usuario!= "kimberly" && contra!="1234"){
			cout<<"\nFavor de escribir los datos correctos\n";		
	cout<<"Usuario: ";	cin>>usuario;
		cout<<"Contrasena: ";cin>>contra;
		intentos++;
		intentos=intentos++;
cout<<"intentos totales: \n"<<intentos;
}
	else{
				cout<<"BIENVENIDO USUARIO\n";
				goto menu;
	}
	if (intentos>2){
			cout<<"\nNo se puede acceder, su cuenta ha sido bloqueada por 24 horas. \n";
	exit(-1);
	}
	}

menu:	
do{
//menu del cajero
cout<<"\n1.Ingresar dinero \n";
cout<<"2.Retirar dinero\n ";
cout<<"3.Consultar saldo\n ";
cout<<"4.Recargar telefono \n";
cout<<"5.Donar \n";
cout<<"6.Cambiar NIP\n";
cout<<"¿Que tramite desea realizar? \n";cin>>opc;

switch (opc){
	//aqui estan los resultados de las opciones que el usuario elegira
	case 1:
		cout<<"Digite cantidad a ingresar: ";		cin>>agrego;
		saldo_actual=saldo_inicial+agrego;
		cout<<"Su saldo actual es de \n"<<saldo_actual;
		movimi++;
		break;
		case 2:			
			cout<<"Digite la cantidad que desea retirar:\n ";			cin>>retiro;
			movimi++;
			
			if (retiro>saldo_inicial and retiro>saldo_actual){
				cout<<"Fondos insuficientes \n";				
			}
			else{
				saldo_actual=(saldo_inicial+agrego-retiro);
				cout<<"Dinero en cuenta:\n "<<saldo_actual;
			}
			break;
			case 3:
				saldo_actual=(saldo_inicial+agrego)-retiro;
				cout<<"Su saldo es de \n"<<saldo_actual;
				movimi++;
				break;
				
				case 4:
						cout<<"Cantidad a recargar: \n";				cin>>recarga;
				cout<<"Digite numero de telefono a recargar: \n";				cin>>num;			
				if(recarga<50){
					cout<<"No se puede realizar recarga menor a $50";
						}
					if(recarga>=50){
						saldo_actual=saldo_actual-recarga;
												cout<<"Recarga completad con exito al numero: "<<num;
						cout <<"\nSaldo actual:\n "<< saldo_actual;
					}
						movimi++;	
					break;
					case 5:
						cout<<"Bienvenido a la donacion: ";
						cout<<"Que cantidad desea donar? \n";						cin>>donar;
						if(donar<1){
							cout<<"Favor de donar una cantidad mayor a $0, no sea pasado:\n";							cin>>donar;
						}
						if(donar>=1){
							cout<<"Su donacion ha sido recibido, gracias.\n";
							cout<<"Su saldo actual es:\n "<<saldo_actual-donar;
						}
						movimi++;
						break;
						
						case 6:
							cout<<"Escriba  nueva contraseña: "; cin>>nueva;
							nueva=contra;
							cout<<"Nip guardado y actualizado\n";
							break;
					}
					cout<<"\n Desea seguir realizando movimientos? 1.SI 2.NO\n " ;
					cin>>resp;
									
}while(resp!=2);
cout<<"Cantidad de movimientos realizados: "<<movimi;
return 0;
}
