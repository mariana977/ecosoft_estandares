#  Guía de Estándares de Código - Proyecto Ecosoft

Este documento define los estándares de codificación generales para el proyecto Ecosoft, asegurando calidad, consistencia y buenas prácticas.

Reglas de nombres

Variables y funciones → usar camelCase (ej: userName, getData)

Componentes de React → usar PascalCase (ej: LoginForm, Navbar)

Clases CSS → usar kebab-case (ej: main-container)

Archivos → nombrar según lo que hacen (ej: Login.jsx, useAuth.js)

*Ej bueno*

const userEmail = "test@mail.com";
function getUserData() { ... }


 *Ej malo*

const User_email = "test@mail.com";
function GETUSERDATA() { ... }

*Comentarios*

Solo comentar lo necesario (explicar qué hace y por qué).

Usar JSDoc en funciones importantes:

*ej*
Calcula el total de una compra
@param {number[]} items - Lista de precios
@returns {number} Total de la compra
 */
function calcularTotal(items) { ... }

*No poner comentarios obvios como*

// suma 1
x = x + 1;

*Estilo de código*

Indentación: 2 espacios.

Comillas simples 'texto' (excepto en JSX).

Siempre poner ; al final de cada línea.

Dejar 1 línea en blanco entre bloques de código.

Imports en orden:

-Librerías externas

-Hooks

-Componentes internos

-Estilos o imágenes

*Ej correcto*

import React from "react";
import { useNavigate } from "react-router-dom";
import Button from "../components/Button";
import "../styles/index.css";

*Ejemplos de código*

*Incorrecto*

function login(){
    const EMAIL="TEST@MAIL.COM"
    console.log("logeando usuario")
}

*Correcto+

function Login() {
  const email = "test@mail.com";
  console.log("Logeando usuario...");
}




