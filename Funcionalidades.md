#include <iostream>
#include <string>
#include <conio.h>
#include <stdlib.h>
//#include <windows.h>
using namespace std;

int main ()
{
    int puestos =40, hora, minuto, opc, opc2, puestoocupado, puestosdispo, modificar, modificar2, tarifa2 = 3000, tarifa = 50,tarifat, i = 40, parking, parkingh , parkingm, entrada, hora2, minuto2;
    bool par[40];
    int carros[40];
    char placa[6];
    int puestos_disponibles = 0; // Variable para almacenar la cantidad de puestos disponibles
    int horas=0, minutos=0, segundos= 0; bool reloj = true; //reloj
    
    /*while(reloj)
    {
        if(horas < 12)
        {
            cout<< horas <<":" << minutos <<":"<<segundos;
            //Sleep(1000);
        }
        else
        {
            cout<< horas <<":" << minutos <<":"<<segundos;
            //Sleep(1000);
        }
        segundos++;
        if(segundos == 60)
        {
            minutos++;
            segundos = 0;
        }
        if(minutos == 60)
        {
            horas++;
            minutos = 0;
        }
        if(horas >= 24)
        {
            horas=0;
            minutos=0;
            segundos=0;
        }
    }*/
    while (opc != 5)
	{
	  cout << endl << "1. Entrada de coche" << endl;
	  cout << "2. Salida de coche" << endl;
	  cout << "3. Modificar la tarifa del parqueadero" << endl;
	  cout << "4. Consultar" << endl;
	  cout << "5. Salir" << endl;
	  cout << "Opción: ";
	  cin >> opc;
	  switch (opc)
		{
		case 1:
		    for(int i=0;i<40;i++){
		    if(par[i]==0){
		        cout<<i;
		        par[i]=1;
		    do{
		    cout << "Digite la placa del coche: ";
		    for(int i=0;i<6;i++){
		    cin >> placa[i];
		    }
		    //do{
		    cout << "\nDigite hora de entrada";
		    cout << "\nHora: "; 
		    cin >> hora;
		    if(hora>23||horas<0)
		    {
		        cout<<"Digite una hora correcta, por favor.";
		        getch();
		    }
		    }while(hora>23||horas<0);
		    do{
		  cout << "Minuto: ";
		  cin >> minuto;
		  if(minuto>59||minuto<0)
		  {
		    cout<<"Digite los minutos correctos, por favor.";
		    getch();
		  } 
		  }while(minuto>59||minuto<0);
		  
		  //Informacion del coche 
		  cout << "Informacion de la entrada";
		  cout << "\nPlaca del coche: " ;
		  for(int i=0;i<6;i++){
		  cout << placa[i];
		  }
		  cout << "\nHora de entrada: " << hora << ":" << minuto;
            
		  /*for(){
		     if(bool==0){
		     cout<<asi
		     break;
		     }else
		     {

		     }
		     } */
		     i=40;
		}
		}
		  break;
		    
		

		case 2:
		  cout << "Digite placa del coche: ";
		  //cin >> placa(6);
		  do{
		  cout << "\nDigite hora de salida";
		  cout << "\nHora: ";
		  cin >> hora2;
		  
		  if(hora2>23||hora2<0)
		  {
		    cout<<"Digite una hora correcta, por favor.";
		    getch();
		  } 
		  }while(hora2>23||hora2<0);
		  do{
		  cout << "\nMinuto: ";
		  cin >> minuto2;
		  if(minuto2>23||minuto2<0)
		  {
		    cout<<"Digite los minutos correctos, por favor.";
		    getch();
		  } 
		  }while(minuto2>59||minuto2<0);
		  cout << "\nTiempo de parking hora: "; parkingh=hora2 - hora ;
		  cout <<parkingh ;
		  cout << "\nTiempo de parking minutos: "; parkingm=minuto2 - minuto; 
		  cout << parkingm;
		  tarifat = (tarifa * parkingm) + (tarifa2 * parkingh);
		  cout << "\nSu tarifa de pago es de: " << tarifat;
		  break;
		case 3:
		  cout <<
			"Ingrese la tarifa en horas que desea implementar de ahora en adelante: ";
		  cin >> modificar2;
		  tarifa2 = modificar2;
		  cout << "Su tarifa es de: " << tarifa2 << " por hora." << endl;
		  cout <<
			"Ingrese la tarifa en minutos que desea implementar de ahora en adelante: ";
		  cin >> modificar;
		  tarifa = modificar;
		  cout << "Su tarifa es de: " << tarifa << " por minuto." << endl;
		  break;
		case 4:
		  cout << "¿Que deseas consultar?" << endl;
		  cout << "1. Consultar cantidad y porcentaje de puestos disponibles"
			<< endl;
		  cout << "2. Consultar ingresos monetarios" << endl;
		  cout << "Opción: ";
		  cin >> opc2;
		  switch (opc2)
			{
			case 1:
                 puestos_disponibles = 1;
                for (int i = 1; i < puestos; i++) {
                    if (!par[i]) {
                            puestos_disponibles++;
                    }
                }
			  cout << "La cantidad de parqueaderos son : " << puestos_disponibles << endl;
			  cout << "Los puestos disponibles son : " << (puestos_disponibles / puestos) * 40 << endl;
			  break;
			case 2:
			  cout << "Los ingresos monetarios del dia de hoy son: " << endl;
			  break;
			}
		case 5:
	    cout << "Volver al menu principal " << endl;	
		}
		getch();
		return 0;
	}
}
