---
layout: post
title:  "Trabajo Entorno de desarrollo"
date:   08-04-2019
---

<p class="intro"><span class="dropcap">E</span>s un patrón de diseño orientada a objetos, en el que se suministran objetos a una clase en lugar de ser la propia clase la que cree dichos objetos. Esos objetos cumplen contratos que necesitan nuestras clases para poder funcionar (de ahí el concepto de dependencia). Nuestras clases no crean los objetos que necesitan, sino que se los suministra otra clase 'contenedora' que inyectará la implementación deseada a nuestro contrato.  
  Aparecieron dos conceptos para estructurar el código: la modularidad y la reutilización de los componentes: se crean bibliotecas de componentes reutilizables. El flujo se complica, saltando de componente a componente, y aparece un nuevo problema: la dependencia (acoplamiento) entre los componentes.  
  
```java

//Constructor:  
public class A {
  private B dependency;
  public A(B instancedepency){
    this.dependency=instancedepency;
  }
} 

```
```
- puedes hacer referencia a éstos u otros 'sencillos
ejemplos'.  
- Estructura adecuadamente tu entrada/contenido pensando
que debe servir a quien lea,i enterarse de beneficios
del concepto.  
- Usar carpeta Compartida para compartir cualquier problema
(buscando ayuda en tus propios comañeros/as) al usar
github page. Merece la pena que sea presentado de esta
manera para que tengas una primer experiencia con lo que
sería la generación de tu "primer static site".
```
