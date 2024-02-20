### notes 
J'ai bien les REGEX :D 
# 1 Francais ! 

## prerequis 

```sh 
export french="/usr/share/dict/french"
```

Pas obligatoire, si vous ne voulez pas l'utiliser, remplacer : `$french` par `/usr/share/dict/french`

## Q1 

```sh
grep titi $french 
```

## Q2

```sh
grep "ren.ren" $french
```

## Q3 

```sh
grep "r.\+w" $french
```
equivalent a : 

```sh
grep "r..*w" $french
```

## Q4

sol avec 2 `-e` :
```sh
grep -e "k.\+w" -e "w.\+k" $french
```
`-e` : permet, si utilise a repetition de specifier 2 expressions regulieres  !

sol avec `|` (ou) :  
```sh 
grep -e "\(k.\+w\|w.\+k\)" $french
```
## Q5

```sh 
grep "latif\$" $french
```

## Q6 

Ici, je vais etre sincere... j'ai pas d'accent sur mon ordi... donc j'ai utilise les classes 
d'equivalence `[=e=]`. 
```sh
grep "^d[=e=].*d[=e=]\$" $french
```

Pour plus tard :
```sh
grep "^\(d[=e=]\).*\\1\$" $french
```


## Q7 

`.\{4\}` c'est plus jolie que `....` :P 

```sh 
grep "^ent.\{4\}ent\$" $french
```

## Q8 

!!! `^` et `^` ont pas la meme signification !! 

```sh 
grep "^[^st]*st\$" $french
```

## Q9 

```sh 
grep "\(.\+-.\+\)\{3\}" $french
```

## Q10 

TODO : a tester ! 
```sh 
grep "\([=e=]t\+\)\{2\}[=e=]" $french
```

## Q11 

```sh 
grep -o ".\$" $french | sort | uniq -c | sort -n
```
## Q12 

```sh
grep -o "..\$" $french  | grep -o "^." |  sort | uniq -c | sort -n
```


# Exercise 2 

Suivre les enonces de RegexOne ! 

# Exercies 3 

TODO : A voir ! 
