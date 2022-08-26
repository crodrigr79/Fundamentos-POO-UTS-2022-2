# Ejercicios realizados en clase

## 1. Ejercicio de servicio de agua (Condicionales). 

![image](https://user-images.githubusercontent.com/31961588/184923865-82dbd8ad-0c40-43cc-a0f8-4a249ef7bfc1.png)


**Solucion**

```Java
package appservicioaguauts;

import java.util.Scanner;

public class AppServicioAguaUTS {

  
    public static void main(String[] args) {
        Scanner leer=new Scanner(System.in);
        
        System.out.println("Ingrese el documento");
        String numDocumento=leer.next();
        System.out.println("Ingrese el estado 1: activo o 2: suspendido");
        int estado=leer.nextInt();
        System.out.println("Ingrese el estrato: 1,2,3,4,5");
        int estrato=leer.nextInt();
        
        if(estado==1){
           if(estrato==1){
            System.out.println("Valor de la tarifa básica es: $10.000");   
           }else if(estrato==2){
            System.out.println("Valor de la tarifa básica es: $15.000");   
           }else if(estrato==3){
            System.out.println("Valor de la tarifa básica es: $30.000");   
           }else if(estrato==4){
            System.out.println("Valor de la tarifa básica es: $50.000");    
           }else{
            System.out.println("Valor de la tarifa básica es: $65.000");   
           }
        
        }else{
          System.out.println("Valor de la tarifa básica es: $0");
        
        }            
        
        
        
    }
    
}
```

## 3. Saludo

![image](https://user-images.githubusercontent.com/31961588/163828082-08d94056-7373-4cc9-bf23-a374f3e8e01d.png)

**Solución 1**

```Java

package appcirculo;

import java.util.Scanner;

public class AppCirculo {
   
    public static void main(String[] args) {
        
        Scanner leer=new Scanner(System.in);
        double radio,perimetro,area;
        System.out.println("Ingrese el radio: ");
        radio=leer.nextDouble();
        area=Math.PI*Math.pow(radio,2);
        perimetro=2*Math.PI*radio;        
        System.out.println("El perimetro es: "+perimetro+" "+"el area es: "+area);
        
    }
    
}
```

## 3. Circulo

![image](https://user-images.githubusercontent.com/31961588/163828347-f0f3f021-0456-43f8-b481-1d818a87be08.png)

**Solución 2**

## 4. Promedio

![image](https://user-images.githubusercontent.com/31961588/163828427-6376a283-0445-4b3b-bd5c-f26c4c82ee72.png)

**Solución 3**

## 5. Conversión de unidades de longitud
![image](https://user-images.githubusercontent.com/31961588/163828482-cdd2dd38-e805-4418-9db9-f3a3fd2ce958.png)

**Solución 4**

## 6. Número invertido
![image](https://user-images.githubusercontent.com/31961588/163828564-7e54ea4c-73a9-4ef7-aca9-21f1dd124d93.png)

**Solución**

```Java
package appcirculo;

import java.util.Scanner;

public class Invertido {
    public static void main(String[] args) {
        Scanner leer=new Scanner(System.in);
        System.out.println("Programa número invertido");
        int numero,invertido;
        System.out.println("Ingrese número: ");
        numero=leer.nextInt();
        
        invertido=(numero%10)*100; //Centenas
        numero=numero/10;
        invertido=invertido+((numero%10)*10); //Decenas
        numero=numero/10;
        invertido=invertido+numero; //Unidades
        
        System.out.println("Invertido es: "+invertido);  
    }
}

```

## 7. Pitágoras

![image](https://user-images.githubusercontent.com/31961588/163829448-e7ae3e2f-cf13-4058-88b8-6cdedbe19911.png)


```Java
package appcirculo;

import java.util.Scanner;

public class Pitagoras {

    public static void main(String arg[]) {
        Scanner leer = new Scanner(System.in);
        double c, a, b;
        System.out.println("Ingrese el cateto a: ");
        a = leer.nextDouble();
        System.out.println("Ingrese el cateto b: ");
        b = leer.nextDouble();
        c=Math.pow(a,2)+Math.pow(b,2);
        c=Math.sqrt(c);
        System.out.println("Hipotenusa: "+c);
    }

}

```


**Solución 6**


## 8. Hora futura

![image](https://user-images.githubusercontent.com/31961588/163829518-a0a27ed0-1f63-45e6-9b76-d6e08d0cc001.png)


**Solución 7**

```Java
package appcirculo;

import java.util.Scanner;


public class HoraFutura {
    
    public static void main(String args[]){
      Scanner leer=new Scanner(System.in);
      int hActual,numHoras,totalHoras;
      System.out.println("Ingrese la hora actual: ");
      hActual=leer.nextInt();
      System.out.println("Ingrese el número de horas: ");
      numHoras=leer.nextInt();
      totalHoras=hActual+numHoras;
      if(totalHoras<=24){
        System.out.println("Hora futuro es: "+totalHoras);
      }else{
        System.out.println("Hora futuro es: "+totalHoras%24); 
      }  
    }    
}
```

## 9. Parte decimal

![image](https://user-images.githubusercontent.com/31961588/163829563-509bc535-d528-47c7-a804-8725acb7a995.png)


**Solución 8**

## 10. Qué nota necesito

![image](https://user-images.githubusercontent.com/31961588/163829601-a7c25604-3947-4c9a-91a5-0ede2b01a018.png)


**Solución 9**
 
## 11. Año bisiesto

![image](https://user-images.githubusercontent.com/31961588/171307000-a088f237-f470-4fd5-adb6-d077a17695c5.png)


## 12. Vendedores usando for

![image](https://user-images.githubusercontent.com/31961588/186056512-c237f637-df8d-4437-9e3e-ce9b7ffafef6.png)

```Java

package appcirculo;

import java.util.Scanner;


public class VendedoresComision {
    public static void main(String arg[]){
      Scanner leer=new Scanner(System.in);
      //Variables
      int numeroVendedores;
      String cedula;
      int tipoVendedor;
      double valorVentasMes,comisiones;
      
      System.out.println("Ingrese el número de vendedores: ");
      numeroVendedores=leer.nextInt();
      
      for(int i=0;i<numeroVendedores;i++){
          System.out.println("Ingrese cedula: ");
          cedula=leer.next();
          System.out.println("Ingrese el tipo vendedor 1:pueta y 2:ejecutivo");
          tipoVendedor=leer.nextInt();
          System.out.println("Ingrese las ventas del mes: ");
          valorVentasMes=leer.nextDouble();
          if(tipoVendedor==1){
           comisiones=valorVentasMes*0.20;
          }else{
           comisiones=valorVentasMes*0.30; 
          }
          System.out.println("El valor de la comisión es: "+comisiones);    
      
      }
                
    }
}

```

## 13. Vendedores por comisión con while


![image](https://user-images.githubusercontent.com/31961588/186896326-71be6c72-4040-4f45-a54d-e7a6a30b74af.png)

**Solucion**

```Java

import java.util.Scanner;

public class VendedoresWhile {
    
    public static void main(String arg[]){
      Scanner leer=new Scanner(System.in);
      String cedula,nombre;
      int tipoVendedor;
      double ventas,comision;
      
      System.out.println("Ingrese la cedula: ");
      cedula=leer.next();
      while(!cedula.equals("999")){
         System.out.println("Ingrese el nombre: ");
         nombre=leer.next();
         System.out.println("Tipo de vendedor 1: puerta y 2: ejecutivo: ");
         tipoVendedor=leer.nextInt();
         System.out.println("Ingrese las ventas del mes: ");
         ventas=leer.nextDouble();         
         if(tipoVendedor==1){
           comision=ventas*0.20;
         }else{
           comision=ventas*0.30;
         }         
         System.out.println("La comsión es: "+comision);
         System.out.println("Siguiente empleado....");
         System.out.println("Ingrese la cedula");
         cedula=leer.next();         
      }      
      System.out.println("Fin de progrma...");    
    }
    
}

```

