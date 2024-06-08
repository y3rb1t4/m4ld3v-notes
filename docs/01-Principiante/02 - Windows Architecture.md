
## Introducción

Este módulo detalla la arquitectura de Windows y los procesos internos que ocurren en las aplicaciones y procesos de Windows.

## Arquitectura de Windows

Un procesador en una máquina que ejecuta el sistema operativo Windows puede operar bajo dos modos distintos: Modo Usuario y Modo Kernel. Las aplicaciones se ejecutan en modo usuario, mientras que los componentes del sistema operativo operan en modo kernel. Cuando una aplicación necesita realizar una tarea, como crear un archivo, no puede hacerlo por sí misma. La única entidad capaz de completar la tarea es el kernel, por lo que las aplicaciones deben seguir un flujo específico de llamadas a funciones. El diagrama a continuación muestra un nivel alto de este flujo.

![[Pasted image 20240424014105.png]]

- **Procesos de Usuario** - Un programa o aplicación ejecutado por el usuario, como el Bloc de notas, Google Chrome o Microsoft Word.

- **DLLs de Subsistemas** - DLLs que contienen funciones de la API que son llamadas por los procesos de usuario. Un ejemplo de esto sería kernel32.dll, que exporta la función de la API de Windows [CreateFile](https://learn.microsoft.com/en-us/windows/win32/api/fileapi/nf-fileapi-createfilea) (WinAPI). Otras DLLs comunes de subsistemas incluyen ntdll.dll, advapi32.dll y user32.dll.

- **Ntdll.dll** - Una DLL de ámbito sistémico que es la capa más baja disponible en modo usuario. Esta es una DLL especial que crea la transición del modo usuario al modo kernel. A menudo se le refiere como la API Nativa o NTAPI.

- **Kernel Ejecutivo** - Esto es lo que se conoce como el Kernel de Windows y llama a otros controladores y módulos disponibles dentro del modo kernel para completar tareas. El kernel de Windows está parcialmente almacenado en un archivo llamado ntoskrnl.exe en "C:\Windows\System32".








