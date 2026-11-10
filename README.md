# Lista de regalos de Reyes (Supabase + GitHub Pages)

## 1. Supabase (gratis)
1. Crea una cuenta en https://supabase.com y un proyecto nuevo (guarda la contraseña de la base de datos).
2. Abre **SQL Editor > New query**, pega el contenido de `supabase.sql` y pulsa **Run**.
3. Ve a **Project Settings > API** y copia:
   - **Project URL**
   - La clave **anon public** (en proyectos nuevos puede llamarse *Publishable key*).
4. Abre `index.html` y pega esos dos valores en las dos primeras líneas del script (`SUPABASE_URL` y `SUPABASE_KEY`).

## 2. GitHub Pages (gratis)
1. Crea un repositorio nuevo en GitHub y sube `index.html`.
2. En el repositorio: **Settings > Pages > Build and deployment > Deploy from a branch**, rama `main`, carpeta `/ (root)`.
3. Tras un minuto tendrás la dirección `https://TU-USUARIO.github.io/NOMBRE-REPO/`. Compártela con tu familia.

## Claves por persona
Al crear o editar a una persona puedes ponerle una **clave**. Su lista de regalos queda oculta (se ve el nombre con un candado) hasta que alguien introduce la clave con **Desbloquear**. La clave se recuerda solo mientras la pestaña está abierta, y con **Ocultar** se vuelve a cerrar.
- La protección es real: los regalos de una persona con clave no se pueden leer desde fuera sin ella, y la clave se guarda cifrada en Supabase.
- Los totales de arriba no incluyen las listas ocultas.
- Si olvidas una clave, se quita desde el SQL Editor: `delete from claves where persona_id = 'ID-DE-LA-PERSONA';`
- La página se actualiza sola cada 10 segundos.

## Ten en cuenta
- Sin inicio de sesión: **cualquiera que tenga el enlace puede ver y editar la lista** (salvo las listas con clave). No lo publiques en redes.
- La clave anon es pública por diseño, y en GitHub Pages gratis el repositorio es público; por eso conviene un nombre de repositorio poco evidente.
- Los proyectos gratuitos de Supabase se pausan tras una semana sin actividad. Si pasa, se reactivan con un clic desde el panel.
