# Encontrar registros repetidos en una base de datos

Created: 04-08-2022 00:46

## <span class="pink"> **Idea** </span>
Esta querie mostrará todos los registros en los qué los campos especificados estén repetidos:

```
SELECT COUNT(0),{campoA},{campoB} from {nombre_tabla}  
group by {campoA},{campoB} having count(0)>1
```


## <span class="orange"> **Tags**</span>
<span class="tag"> #visible</span>  <span class="tag"> #cheatsheet </span> 

## <span class="green"> **References**</span>
<span class="blue"> **West: similar** </span>
[[¿Cómo saber qué proceso usa un puerto?]]
<span class="blue"> **East: opposite** </span>
<span class="blue"> **North: theme/ question** </span>
<span class="blue"> **South: what does this lead to** </span>