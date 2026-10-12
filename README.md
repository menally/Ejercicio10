import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Introduce un valor numérico de temperatura: ");

        double temp = sc.nextDouble();
        //double temp:Guarda la temperatura

        System.out.println("Selecciona una opción (1 o 2):");
        System.out.println("1. Transformación Tipo X");
        System.out.println("2. Transformación Tipo Y");

        int opcion = sc.nextInt();
        //int opcion:Guarda la opción seleccionada//

        double resultado = 0;

        switch (opcion) {
            //switch: Permite elegir entre diferentes opciones//

            case 1:
                //case 1:Realiza la primera transformación//

                resultado = (temp * 9 / 5) + 32;
                System.out.println("Resultado de la transformación: "
                        + resultado + " Unidades_F");
                break;

            case 2:
                //case 2. Realiza la segunda transformación//

                resultado = (temp - 32) * 5 / 9;
                System.out.println("Resultado de la transformación: "
                        + resultado + " Unidades_C");
                break;
                //break: Termina la opción seleccionada//

            default:
                //default: Aparece cuando se introduce una opción diferente//

                System.out.println("Error: Opción no registrada en el sistema.");
        }

        sc.close();
    }
}
//El programa recibe una temperatura y permite elegir entre dos opciones para realizar una
// transformación de unidades