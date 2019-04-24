---
layout: post
title:  "Trabajo Entorno de desarrollo"
date:   24-04-2019
---

<p class="intro"><span class="dropcap">E</span>n este post hablaré acerca de la inyección de dependencias.</p>
<p>Es un patrón de diseño orientada a objetos,en el que se suministran objetos a una clase 
 en lugar de ser la propia clase la que cree dichos objetos.
Esos objetos cumplen contratos que necesitan nuestras clases para poder funcionar (de ahí el concepto de dependencia).
Nuestras clases no crean los objetos que necesitan, sino que se los suministra otra clase 'contenedora' que inyectará la 
implementación deseada a nuestro contrato.  
Aparecieron dos conceptos para estructurar el código: la modularidad y la reutilización de los componentes: 
se crean bibliotecas de componentes reutilizables. El flujo se complica, saltando de componente a componente, 
y aparece un nuevo problema: la dependencia (acoplamiento) entre los componentes.  
  
{% highlight java %}

//Constructor:  
public class A {
  private B dependency;
  public A(B instancedepency){
    this.dependency=instancedepency;
  }
}  

//En un método:
public class A {
  private B dependency;
  public setDependecy(B instancedepency){
    this.dependency=instancedepency;
  }
}  

//En una variable de instancia:  
public class A {
  public B dependency;
}  
  
//Ejemplo claro:  
public class Vehiculo {
  private Motor motor = null;
  public void setMotor(Motor motor){
    this.motor = motor;
  }
  
  public Double enAceleracionDePedal(int presionDePedal) {
    Double velocidad = null;
    if (null != motor){
      motor.setPresionDePedal(presionDePedal);
      int torque = motor.getTorque();
      velocidad = ...
    }
    return velocidad;
  }
}  

public class VehiculoFactory {
  public Vehiculo construyeVehiculo() {
    Vehiculo vehiculo = new Vehiculo();
    Motor motor = new Motor();
    vehiculo.setMotor(motor);
    return vehiculo;
  }
}

{% endhighlight %}
