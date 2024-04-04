#include <iostream>
using namespace std;
int main()
{
    int puestos = 40, opc, opc2, placa, puestoocupado, puestosdispo, modificar, tarifa = 50;
    
    cout<<"1. Entrada de coche"<<endl;
    cout<<"2. Salida de coche"<<endl;
    cout<<"3. Modificar la tarifa del parqueadero"<<endl;
    cout<<"4. Consultar"<<endl;
    cout<<"Opción: "; cin>>opc;
    switch(opc)
        {
        case 1:
            cout<<"Digite placa del coche: "; cin>>placa;
            placa = puestos - 1;
            puestoocupado = placa;
            
            cout<<"Su puesto ocupado es el: "<<puestoocupado;break;
            
        case 2:
            cout<<"Digite placa del coche: "; cin>>placa;
            placa = puestos + 1;
            puestosdispo = placa;
            cout<<"Puesto disponibles: "<<puestosdispo<<endl;
            cout<<"Su tarifa de pago es de: ";break;
        case 3:
            cout<<"Ingrese la tarifa que desea implementar de ahora en adelante: "; cin>>modificar;
            tarifa = modificar;
            cout<<"Su tarifa es de: "<<tarifa<<" por minuto."<<endl;break;
        case 4:
            cout<<"¿Que deseas consultar?"<<endl;
            cout<<"1. Consultar cantidad y porcentaje de puestos disponibles"<<endl;
            cout<<"2. Consultar ingresos monetarios"<<endl;
            cout<<"Opción: "; cin>>opc2;
            switch(opc2)
            {
                case 1:
                    cout<<"La cantidad de puestos disponible es:"<<endl;
                    cout<<"El porcentaje de puestos disponibles es: "<<endl;break;
                case 2:
                    cout<<"Los ingresos monetarios del dia de hoy son: "<<endl;break;
            }
        }
}



