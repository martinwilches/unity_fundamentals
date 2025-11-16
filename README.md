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

## Sprite 

Imagen de 2 dimensiones en el juego (por ejemplo personajes u objetos).

### Texture Type

Cuando se importa una imagen en un proyecto configurado como 2D, esta automaticamente aparecera como Sprite 2D en la opcion de Texture Type.

### Sprite Mode:

- __Single:__ La textura solo tiene un elemento grafico.
- __Multiple:__ La textura esta compuesta por multiples elementos graficos.

### Pixeles por unidad

En la escena cada cuadrado de la cuadricula es una unidad. Por defecto su valor fijado es 100. Ejemplo, si la textura tiene una altura de 100px, esta ocupara una unidad, si es de 50px y el valor de unidad de Pixeles por unidad esta configurado en 100, la textura ocupara la mitad del cuadrado.

### Pivot

Punto del eje por el cual se mueve el Sprite. Por defecto la posicion del pivote del Sprite se encuentra en el centro (0,0).

Si se configura el pivote con el valor Top Left, este se ubicara en la parte superior izquierda del Sprite.

### Filter Mode

Es la manera que utiliza Unity para mejorar el aspecto o la calidad de una imagen.
   
- __Bilinear:__ Se añade un efecto de sombreado para que no se noten los pixeles.
- __Point:__ Sin filtro de mejora para que se vean los pixeles.

## Time.deltaTime

Tiempo que transcurre entre un frame y el siguiente. Se usa para que los movimientos y animaciones sean suaves y constantes sin importar cuantos FPS tenga el juego.

Si no se usa Time.deltaTime el juego ira mas rapido en computadoras con mas FPS y mas lento en computadoras con menos FPS.

```csharp
transform.Translate(1 * Time.deltaTime, 0, 0)
```

## Fisicas

### Componente RigidBody

Le indica a Unity que el GameObject es un objeto rigido y le afecta la gravedad.

### Collider

Componente que permite que un GameObject colisione con otro.

### Material

Ajustar la friccion y el rebote cuando un GameObject colisiona con otro.
