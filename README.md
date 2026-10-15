## Diagrama de red


## Comandos vagrant

- **`vagrant up`**: Lee el Vagrantfile, descarga la imagen (box) si no la tiene, crea las máquinas virtuales en **VirtualBox**, las arranca y ejecuta los *scripts* de aprovisionamiento (.sh)

- **`vagrant up --provision: Para una máquina ya creada no se ejecuta el aprovisionamiento. Si quieres forzarlo, usa --provision.

- **`vagrant up máquina: levantar sólo una máquina en lugar de todas las del vagrantfile.

- **`vagrant ssh máquina: se conecta a una máquina por ssh.

- **`vagrant halt: Apagado ordenado.

- **`vagrant reload: Es un reiniciar que además vuelve a leer el Vagrantfile. Imprescindible si cambias algo en el Vagrantfile (como la RAM o una IP).

- **`vagrant reload www --provision: reinicia una máquina y ejecuta los bloques proivision.

- **`vagrant status: Muestra qué máquinas están encendidas, apagadas o no creadas.
**`vagrant destroy: Detiene las máquinas y borra los archivos de disco de las máquinas virtuales.


## Flujo GIT

## La primera vez

Creas en github un repositorio vacío: vagrantsad.

Clonas repositorio del profesor, lo inicias y le añades tu remote:

```
git clone https://github.com/pes130/vagrantsad.git
git init
git remote remove origin
git branch -M main
git remote add origin git@github.com:TU_USUARIO_DE_GITHUB/proyectosad.git
```

## Cambios locales

Commit de cambios locales y subida a rama en repositorio remoto:

```
git add *
git commit -m "Comentario con tus cambios"
git push -u origin RAMA (normalmente main)
```

## Cuando empieces nueva práctica

Asegúrate de estar en la rama principal(main) y tener todo al día:

```
git checkout main
git pull origin main
```

Crea una rama para la práctica:

```
git checkout -b nombre-de-la-practica
```

Trabajar y guardar (commit de lo que vayas haciendo cuando funcione). Recuerda que estás (deberías) en la rama de la práctica:

```
git add .
git commit -m "Mensaje descriptivo de lo que has hecho"
```

Subir la rama a github:

```
git push origin nombre-de-la-practica
```

Cuando termines → incorpora el cambio de la rama de la práctica a la rama main

```
git checkout main
git merge nombre-de-la-practica
git push origin main
```


## Comandos git de supervivencia

- git status: Te dice en qué rama estás y qué archivos has modificado.

- git log --oneline: Muestra el historial de cambios resumido.

- git diff: Muestra exactamente qué líneas has cambiado en los archivos.

- git checkout .: ¡PELIGRO! Borra todos tus cambios no guardados y deja el archivo como estaba.

- git branch: Lista todas las ramas que tienes creadas.
