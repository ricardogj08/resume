# resume

Un generador simple de currículum vitae (cv) escrito en POSIX `sh`.

* [Ejemplo.](https://notabug.org/ricardogj08/cv)

## Dependencias

* [smu - a Simple Markup Language.](https://github.com/karlb/smu)
* [wkhtmltopdf - Convert HTML to PDF using Webkit (QtWebKit).](https://github.com/wkhtmltopdf/wkhtmltopdf)

## Instalación

```
cd resume
sudo cp resume /usr/local/bin
```

## Uso

```
mkdir micv
cd micv
resume -b
cat <<EOF > src/resume.md
# Foo

Hola mundo!
EOF
resume -b
```

## Flujo de trabajo

```
[micv]
  |-[docs]
  |-[src]
  |-resume.cfg
```

* `docs`: contiene tu currículum en HTML y PDF después de ejecutar `resume -b`.
* `src`: dentro de este directorio escribe en el archivo `resume.md` tu currículum en Markdown.
* `resume.cfg`: contiene variables de configuración para tu currículum. Ver el archivo `resume.cfg.def`.

## Referencias

* [Resume-md](https://github.com/siph/resume-md)
* [Markdown Resume](https://github.com/tengjuilin/markdown-resume)

## Licencia

```
resume -- Un generador simple de currículum vitae escrito en POSIX sh.

Copyright (C) 2024  Ricardo García Jiménez <ricardogj08@riseup.net>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.
```
