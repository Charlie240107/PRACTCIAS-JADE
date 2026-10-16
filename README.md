Prácticas de agentes inteligentes con JADE
1. Objetivo general
Comprender el funcionamiento de los agentes inteligentes en la plataforma JADE, utilizando diferentes tipos de comportamientos para ejecutar tareas, controlar su ciclo de vida y establecer comunicación mediante el envío y la recepción de mensajes.
2. Agente Hello World (HelloWorldAgent.java)
Esta práctica introduce la creación de un agente básico en JADE. El agente utiliza el método setup() para mostrar un mensaje de bienvenida en la consola y posteriormente finalizar su ejecución mediante doDelete().
3. Comportamiento OneShot (OneShotAgent.java)
El comportamiento OneShotBehaviour permite ejecutar una tarea una sola vez. En esta práctica, el agente muestra un mensaje y termina el comportamiento después de ejecutar su método action(). Es útil para realizar tareas puntuales que no requieren repetición.
4. Comportamiento cíclico (CyclicAgent.java)
El comportamiento CyclicBehaviour permite ejecutar una tarea repetidamente mientras el comportamiento permanezca activo. En el ejemplo, el agente imprime un mensaje continuamente. Este tipo de comportamiento es útil para procesos que deben mantenerse activos, como la supervisión o la espera constante de eventos.
5. Comportamiento genérico (GenericAgent.java)
El comportamiento Behaviour permite definir una tarea personalizada mediante los métodos action() y done(). En esta práctica, el agente utiliza un contador para repetir una operación hasta alcanzar un límite de 20 iteraciones. Cuando se cumple la condición, el comportamiento termina y el agente ejecuta doDelete().
6. Comunicación entre agentes: emisor (AgenteEmisor.java)
Esta práctica introduce el intercambio de mensajes entre agentes. El agente emisor crea un objeto ACLMessage, establece el destinatario y el contenido del mensaje, y utiliza send() para enviarlo al agente receptor.
7. Comunicación entre agentes: receptor (AgenteReceptor.java)
El agente receptor utiliza el método receive() para consultar su cola de mensajes. Cuando recibe un mensaje, muestra la información en la consola y finaliza su comportamiento mediante una variable booleana que controla su terminación.
8. Recepción de mensajes con bloqueo (BlockReceptor.java)
En esta práctica se incorpora el método block() para suspender temporalmente el comportamiento cuando no hay mensajes disponibles. Esto evita que el agente ejecute repetidamente las instrucciones de consulta mientras espera la llegada de un mensaje.
9. Conceptos principales
- Agent: clase base para crear agentes en JADE.
- Behaviour: clase que permite definir las tareas que ejecutan los agentes.
- OneShotBehaviour: ejecuta una tarea una sola vez.
- CyclicBehaviour: repite una tarea mientras permanezca activo.
- SimpleBehaviour: permite crear comportamientos personalizados con una condición de finalización.
- ACLMessage: representa los mensajes que intercambian los agentes.
- send() y receive(): permiten enviar y recibir mensajes.
- block(): suspende temporalmente un comportamiento.
- done(): indica si un comportamiento ha terminado.
10. Conclusión general
Las prácticas permitieron conocer los fundamentos de la programación de agentes inteligentes con JADE. Se estudiaron distintos comportamientos, desde tareas que se ejecutan una sola vez hasta procesos cíclicos y personalizados. Asimismo, se comprendió cómo los agentes pueden comunicarse mediante mensajes ACL y cómo utilizar mecanismos de bloqueo para gestionar la espera de mensajes. Estos conocimientos constituyen una base para desarrollar sistemas multiagente capaces de ejecutar tareas independientes, coordinar actividades e intercambiar información.
