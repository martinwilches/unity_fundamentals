# Unity

## GameObjects
- La parte mas basica de un juego
- Necesitan que se le añadan componentes con la funcion que se requiere que este tenga
- El componente transform es el unico que esta presente en todos los GameObjects. Tiene la posicion y la orientacion del GameObject en la escena.

Ejemplos de GameObject:
- Un personaje animado
- Una luz
- Un arbol
- Una fuente de audio

## Escena
Area de contenido del juego
- Se necesita al menos un GameObject camara para mostrar la escena.

- Escena (Menu)
    - GameObject
        - Componente
    - GameObject
        - Componente
- Escena (Gameplay)
    - GameObject
        - Componente
    - GameObject
        - Componente
     
## Ventanas del editor

### Ventana de proyecto
- Es la encargada de gestionar la carpeta assets, contener nuevos directorios, etc, que vayan a ser usados en el juego.

### Ventana de jerarquia
- Estructura de forma jerarquica todos los componentes y archivos disponibles en el juego en la escena actual. (Son instancias de los objetos añadidos al juego, si se eliminan de la escena, solo se eliminan de la escena actual mas no del directorio raiz donde se ha añadido el objeto).

### Ventana de inspector
- Muestra la informacion de cada GameObject.

### Ventana escena
- Representacion visual del juego

### Vista de juego
- Muestra una vista final o parcial del desarrollo del juego tal como lo veria el usuario.

### Camara
- Se encarga de renderizar los objetos de la escena en la vista del juego

## Scripts

Codigo utilizado para controlar el comportamiento de los objetos en el juego (Los componentes de un objeto son Scripts).

Ejemplo de variables y funciones

```csharp
int base;
int altura;
void CalcularArea()
{
    base = PedirBase();
    altura = PedirAltura();

    float r = base * altura/2;

    MostrarArea(r);
}

void MostrarArea(float resultado)
{
    Console.WriteLine(resultado);
}
```
