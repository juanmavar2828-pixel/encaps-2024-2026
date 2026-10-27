# ENCAPS · Maestro de Errores (GitHub Pages)

Adaptación de la versión V5.10.4 del proyecto Maestro de Errores, conservando sus funciones de práctica, navegación, flashcards, FSRS-6, misiones, recompensas, historial, estudio de errores, respaldos y modos de examen.

## Publicación sin Firebase

1. Crear o abrir tu repositorio público `encaps-2024-2026`.
2. Subir `index.html` y `banco.json` en la raíz. Si ya existen, reemplazarlos con los de este paquete.
3. Entrar en **Settings → Pages → Deploy from a branch**, elegir `main` y `/(root)`, luego Save.
4. Abrir la URL indicada por GitHub Pages.

## Actualizar las clases sin rehacer la plataforma

Modificar **solo** `banco.json`, conservando los identificadores `bankId` y `code`. Al abrir o recargar la web, el HTML incorpora las lecciones sin borrar el historial local del usuario. En archivo sin conexión se utiliza el banco integrado.

## Teclado

- **A–D:** marcar respuesta según alternativa disponible.
- **← / →:** pregunta anterior / siguiente.
- **Espacio:** revelar respuesta de flashcard.
- **1:** Olvidé; **2:** Difícil; **3:** Bien; **4:** Fácil (FSRS).

## Funciones conservadas

- Banco de estudio, simulacro real cronometrado, reanudar, detener y revisar.
- Mapa de respuestas, historial, falladas/pendientes, «Solo mis errores» y repeticiones de errores.
- Misión diaria, radar, sala de dominio, rangos, Rambosoles y avatar.
- Flashcards por error o selección de texto, repaso espaciado FSRS-6 (requiere conexión para módulo externo) y bandeja de memoria.
- Favoritos, estadísticas por curso, importación de bancos, exportación y respaldo del progreso.

## Privacidad y límites

No se usa Firebase, inicio de sesión ni cobro de créditos. El avance se guarda en IndexedDB del navegador donde se estudia y **no se sincroniza automáticamente** entre dispositivos. Usa la opción de exportar respaldo para conservarlo o migrarlo. El sitio es público, pero el progreso local no se publica en el repositorio. Si se borra el almacenamiento del navegador sin haber exportado, se pierde el avance.

Las **100 preguntas** y sus claves fueron extraídas del PDF aportado. Las **preguntas 1–70** tienen lecciones extensas, explicaciones de distractores y ejercicios de refuerzo; las **71–100** están pendientes de desarrollo. Se recuperaron los bloques 11–35 del histórico de GitHub y se consolidaron en `banco.json` e `index.html`. Las letras proceden del PDF resaltado, **no representan cotejo independiente con la tabla oficial del MINSA**. Ante discrepancias, la clase muestra los matices sin cambiar la respuesta del PDF.
