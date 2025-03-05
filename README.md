# 📝 Notes App

¡Bienvenido a la **Notes App**! 🎉 Esta es una aplicación web sencilla diseñada para ayudarte a tomar notas rápidas y organizarlas de manera eficiente. Desarrollada con HTML, CSS y JavaScript, esta aplicación te permite agregar, editar y eliminar notas con facilidad. ¡Perfecta para practicar conceptos clave de JavaScript! 🚀

## 🚀 Características Principales

- **Agregar notas**: Crea nuevas notas con un solo clic. ✨
- **Editar notas**: Modifica el contenido de tus notas en cualquier momento. 📝
- **Eliminar notas**: Elimina notas no deseadas con un doble clic. 🗑️
- **Persistencia de datos**: Tus notas se guardan en el almacenamiento local del navegador, por lo que no se perderán al recargar la página. 💾

## 🛠️ Tecnologías Utilizadas

- **HTML**: Estructura básica de la aplicación.
- **CSS**: Estilos y diseño atractivo.
- **JavaScript**: Funcionalidad dinámica y manejo de datos.

## 🎨 Diseño y Estilos

La aplicación cuenta con un diseño limpio y moderno, con un fondo degradado y notas que se adaptan dinámicamente al espacio disponible. Los estilos incluyen:

- **Fondo degradado**: Un suave degradado de colores para una experiencia visual agradable. 🌈
- **Notas interactivas**: Las notas cambian de estilo al pasar el cursor sobre ellas, proporcionando una experiencia de usuario intuitiva. 🖱️
- **Botón de agregar**: Un botón llamativo que te permite agregar nuevas notas con un solo clic. ➕

## � Funcionalidades Clave

### 📌 Agregar una Nueva Nota

Para agregar una nueva nota, simplemente haz clic en el botón **"+"** ubicado en la parte inferior derecha de la pantalla. Esto creará una nueva nota en blanco lista para que escribas en ella.

```javascript
function addNote() {
    const notes = getNotes();
    const noteObj = {
        id: Math.floor(Math.random() * 10000),
        content: "",
    };

    const noteEl = createNoteEl(noteObj.id, noteObj.content);
    appEl.insertBefore(noteEl, btnEl);

    notes.push(noteObj);
    saveNote(notes);
}
```

### 📝 Editar una Nota
Puedes editar el contenido de una nota en cualquier momento. Simplemente haz clic en la nota y comienza a escribir. Los cambios se guardan automáticamente.

```javascript
element.addEventListener("input", () => {
    updateNote(id, element.value);
});
```
### 🗑️ Eliminar una Nota
Para eliminar una nota, haz doble clic sobre ella. Se te pedirá confirmación antes de eliminar la nota definitivamente.

```javascript
element.addEventListener("dblclick", () => {
    const warning = confirm("Do you want to delete this note?");
    if (warning) {
        deleteNote(id, element);
    }
});
```

## 📂 Estructura del Proyecto
- index.html: Contiene la estructura básica de la aplicación.

- style.css: Define los estilos y el diseño de la aplicación.

- script.js: Implementa la lógica de la aplicación, incluyendo la creación, edición y eliminación de notas.

## 🚀 Cómo Ejecutar el Proyecto
1. Clona este repositorio en tu máquina local.

2. Abre el archivo index.html en tu navegador web.

3. ¡Comienza a tomar notas! 📝