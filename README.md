//
//  main.c
//  SISTEMA DE PAPELERIA KARO
//
//  Created by Gail Keegan Lopez Monares on 26/03/20.
//  Copyright © 2020 López Monares Gail Keegan. All rights reserved.
//

#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <curses.h>


#include "Articulos.h"
#include "Compras.h"
#include "Ventas.h"
#include "Gastos.h"

/* */

int main (){
    
    char cOpcion;
    int eOpcionFA;
    int eOpcionFC;
    int eOpcionFV;
    int eOpcionFG;
    
    do {
    
        system("clear"); //No es el estandar 
        
        printf("\n\nEste modulo muestra el menú de todo el sistema \n\n");
        
        fflush(stdin);
        
        printf("Para  ingresar a una de las siguietes opciones ingrese la letra entre corchetes de la opcion correspondiente \n");
        printf("[A] Articulos \n");
        printf("[C] Compras   \n");
        printf("[V] Ventas    \n");
        printf("[G] Gastos    \n");
        printf("[S] Salir del programa \n");
        printf("Escriba en este renglon la opcion que desea: ");
        scanf("%c", &cOpcion);
        
        printf("\n\n\n\n");
        
        switch (cOpcion) {
            case 'A':
        
                Articulos(&eOpcionFA);
                break;
                
            case 'a':
                
                Articulos(&eOpcionFA);
                break;
                
            case 'C':
                Compras(&eOpcionFC);
                break;
                
            case 'c':
                Compras(&eOpcionFC);
                break;
                
            case 'V':
                Ventas(&eOpcionFV);
                break;
            
            case 'v':
                Ventas(&eOpcionFV);
                break;
                
            case 'G':
                Gastos(&eOpcionFG);
                break;
            
            case 'g':
                Gastos(&eOpcionFG);
                break;
                
            
            default:
                printf("La opcion ingresada es incorrecta \n");
                
                
                break;
        }

    } while (cOpcion != 'S');
    
    printf("EL PROGRAMA HA TERMINADO CORECTAMENTE \n");
    
}


