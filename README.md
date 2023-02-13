# Crear_clase_Pila_en_Java
Esta es una clase Pila, donde se puede crear una pila nueva, agregar elementos, eliminarlos, mostrar los elementos de la pila, mostrar ultimo elemento y limpiar toda la pila.


public class Pilas_Construccion {
    
    int vectorPila[];
    int cima;

    public Pilas {
       
        vectorPila = new int[tamano];
        cima = 0;
    }

    public void limpiarPila(int tamano) {
        vectorPila = new int[tamano];
        cima = 0;
    }

    public void push(int dato) {
        vectorPila[cima] = dato;
        cima++;
    }

    public int pop() {
        int eliminar = 0;

        if (cima == 0)
        {
            System.out.println("pila vacia");
        } else
        {
            eliminar = vectorPila[cima - 1];
            cima--;
        }
        return eliminar;
    }

    public int tamano() {
        return vectorPila.length;
    }

    public boolean pilaVacia() {
        if (cima == 0)
        {
            return true;
        } else
        {
            return false;
        }
    }

    public boolean pilaLlena(int tamano) {
        if (cima == tamano)
        {
            return true;
        } else
        {
            return false;
        }
    }
//Muestra todos los numeros de la PILA
    public void mostrarPila() {

        while (pilaVacia() == false)
        {
            int valor = pop();
            System.out.println(valor);

        }
    }

    //Recorre toda la pila hasta mostrar el ultimo numero.
    public int mostrarFondo() {
        int valor = 0;
        while (pilaVacia() == false)
        {
            valor = pop();
        }
        return valor;
       
    }
    
}
