# Matar un Proceso en Linux

Created: 04-08-2022 00:55

## <span class="pink"> **Idea** </span>
Para matar un proceso en Linux se puede hacer lo siguiente:

```
ps ax | grep {nombre_proceso}
```

De la lista qué devuelva el comando anterior, se extraerá el `mid` del proceso.

Y finalmente se ejecturará el siguiente comando para matar el proceso.

```
kill -9 {miid}
```

## <span class="orange"> **Tags**</span>
<span class="tag"> #visible</span> <span class="tag"> #cheatsheet </span> 

## <span class="green"> **References**</span>
<span class="blue"> **West: similar** </span>
[[Encontrar registros repetidos en una base de datos]]
[[¿Cómo saber qué proceso usa un puerto?]]
<span class="blue"> **East: opposite** </span>
<span class="blue"> **North: theme/ question** </span>
<span class="blue"> **South: what does this lead to** </span>