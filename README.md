# Sena-Actividad-3-C-Uso-de-if-Anidados
Programa para el Uso de If Anidados en C++.
#include <stdlib.h>

// Software para introducir datos a través de pantalla//
#include <iostream>
using namespace std;

int main ( ) {
	
	// Inicialización de las variables.
	
	int ref_calzado;
	int talla_calzado;
	int costo_calzado;
	int precio_venta;
	char descripcion[50];
	char disponible_venta;
	int cantidad_zapatos;
	float costo_total;
	float precio_total;
	float utilidad_unidad;
	float utilidad_total;
	float porcentaje_utilidad;
	
	// En este espacio se piden los datos para que sean procesados por el programa. 
	
	cout <<"Digite la Referencia:  " << endl; 
	cin>> ref_calzado;
	cout <<"Digite la Talla del Zapato:    "<< endl; 
	cin>> talla_calzado;
	cin.ignore(256, '\n');
	cout <<"Digite la Descripcion del calzado:    "<< endl;
	cin.getline(descripcion, 50);
	cout <<"Esta disponible S/N: "<< endl;
	cin >> disponible_venta;
	cout <<"Digite el costo del calzado:  "<< endl;
	cin>> costo_calzado;
	cout <<"Digite el precio de Venta:   "<< endl;
	cin>> precio_venta;
	cout <<"Digite la cantidad de calzados disponibles:   "<< endl;
	cin >> cantidad_zapatos;
	
	// Estas son las operaciones que se deben hacer para que el programa de los resultados esperados.
	
	costo_total = costo_calzado * cantidad_zapatos;
	precio_total = precio_venta * cantidad_zapatos;
	utilidad_unidad = precio_venta - costo_calzado;
	utilidad_total = utilidad_unidad * cantidad_zapatos;
	porcentaje_utilidad = utilidad_total * 100 / costo_total; 
	
	system ("cls");  
	
	cout <<"\nLa Referencia es:" <<ref_calzado<< endl;
	cout <<"\nLa talla del Zapato es:    "<<talla_calzado << endl;
	cout <<"\nLa Descripcion del calzado es:    "<<descripcion << endl;
	cout <<"\nEl costo del calzado es:     " <<costo_calzado << endl;
	cout <<"\nEl precio de venta es:     " <<precio_venta << endl;
	cout <<"\nEl costo total es:    " <<costo_total << endl;
	cout <<"\nEl precio total es:   " <<precio_total <<endl;
	cout <<"\nLa utilidad por unidad es:    "<<utilidad_unidad <<endl;
	cout <<"\nLa utilidad total es:  " <<utilidad_total << endl;
	cout <<"\nEl porcentaje de utilidad es:   " << porcentaje_utilidad << endl;
	
	// A continuación coloco las condiciones para determinar el tipo de calzado según el precio y el porcentaje de utilidad. 
	
		if (precio_venta<= 30000){
		cout <<"El Tipo de Zapato es A. El porcentaje de utilidad es del 50%";
		} 
		
		if (precio_venta >= 30000){
			if (precio_venta <60000)
		cout <<"El Tipo de Zapato es B. El porcentaje de utilidad es del 40%";
		} 

        if (precio_venta > 60000){
		   cout <<"El Tipo de Zapato es C. El porcentaje de utilidad es del 30%";
		} 
 		
	cout <<"\nGracias por Digitar la Informacion\n" << endl;
	cout <<"\nCodigo desarrollado por Jaidi Gonzalez\n" <<endl;
	system ("pause");
	
	return EXIT_SUCCESS; 
	
	
	}

