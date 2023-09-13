# Implementar una llave GPG en GitHub

Breve explicación de cómo implementar una llave GPG en GitHub para hacer `commits` verificados.

Si estás usando **Linux**, asegúrese de tener instalado `xclip`:

```zsh
sudo apt install xclip
```

## ¿Cómo envío commits a GitHub verificados?.

Para empezar, debes crear una llave `GPG` con el siguiente comando:

```zsh
gpg --gen-key
```

Y luego, copie la llave GPG pública al portapapeles usando el siguiente comando en función del sistema operativo que estés utilizando.

### En Linux

```zsh
gpg --armor --export <tu-id-de-llave-gpg> | xclip -selection clipboard
```

> El identificaador de la llave pública GPG debe verse así:
> ```zsh
> 
> gpg --armor --export 290444824C41E17433B08638A665DDAF2B7E77E6 | xclip -selection clipboard
> ```

### En Windows:

```zsh
gpg --armor --export <tu-id-de-llave-gpg> | clip
```


### En macOS

```zsh
gpg --armor --export <tu-id-de-llave-gpg> | pbcopy
```

Después de seguir los pasos anteriores, agregue su llave GPG acá:

[Agregue su llave GPG aquí](https://github.com/settings/gpg/new "Agregar llave GPG")


> **Por** David E Luna M

