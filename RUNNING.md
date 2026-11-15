

<!-- local-development:start -->
# Desarrollo local

Puedes abrir este repositorio en VS Code, Antigravity o Sublime Text. El compilador y los servicios necesarios dependen del componente indicado abajo.

## HTML

Para páginas estáticas, inicia un servidor HTTP desde la carpeta de la página. Si usan un backend o una base de datos, hay que preparar ese servicio aparte.

```powershell
py -3.12 -m http.server 8000 --bind 127.0.0.1
```

## Archivos ignorados

`.gitignore` excluye credenciales locales, estado del editor y salidas de las herramientas detectadas. No deja de versionar archivos que ya estaban en Git. Los manifiestos, archivos de bloqueo, recursos fuente y scripts de esquema forman parte del código.
<!-- local-development:end -->

<!-- platform-tools:start -->
## Herramientas para otros componentes

### iOS / macOS

Los proyectos de Xcode requieren macOS, Xcode y sus SDK. Puedes editar los archivos en los editores de Windows, pero la compilación y el simulador de iOS deben prepararse en un Mac. Las bibliotecas Visual C++ incluidas como dependencias no convierten la aplicación iOS en una aplicación Windows.

### C / C++

Los proyectos `.vcxproj` requieren la carga de trabajo C++ de Visual Studio, el Windows SDK y las bibliotecas nativas que declaran. Revisa `PlatformToolset` y la arquitectura antes de migrarlos a VS 2022. Las comprobaciones C# de esta guía no cubren esas bibliotecas nativas.
<!-- platform-tools:end -->
