---
layout: default
title: Contactar
---

<div id="contact">
  <h1 class="pageTitle">Contactar</h1>
  <div class="contactContent">
    <p class="intro">El código de esta página se encuentra en el archivo <code>contact.html</code>.</p>
    <p>Si quieres visitar mi página de <a href="http://github.com/tryn0/">github.</a> Sigueme.</p>
    <p>El correo aun no está disponible <a href="mailto:correo@correo.es">correo</a></p>
  </div>
  <form action="http://formspree.io/your@mail.com" method="POST">
    <label for="name">Nombre</label>
    <input type="text" id="name" name="name" class="full-width"><br>
    <label for="email">Correo electrónico</label>
    <input type="email" id="email" name="_replyto" class="full-width"><br>
    <label for="message">Mensaje</label>
    <textarea name="message" id="message" cols="30" rows="10" class="full-width"></textarea><br>
    <input type="submit" value="Envíar" class="button">
  </form>
</div>
