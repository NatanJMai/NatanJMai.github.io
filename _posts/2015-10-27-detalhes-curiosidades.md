---
layout: post
title: Algumas das curiosidades de Haskell!
---

Algumas informações e curiosidades de Haskell que acabei esquecendo de colocar nos meus slides, fique a vontade :-) 

Como escrevi em outro post, sou um estudante iniciante em programação funcional e adotei Haskell como uma das minhas linguagens favoritas. Como dito na outra postagem também, falei duas vezes sobre o assunto, a primeira vez no FLISoL 2014 e a outra vez na semana acadêmica de Ciência da Computação aqui na UFFS.

Segue algumas das características que não coloquei nos slides:
_________

<h3>Guarded Equations</h3>

Vou ser sincero, quando vi isso pensei que não me ajudava em nada, mas hoje vejo que a sintaxe é muito mais simples e elegante do que o famoso *if then else then bla bla bla*.

É melhor enteder via exemplos:

	post a b 
		| a < b 	= b
		| otherwise = a

*O que isso significa?*
 	Bem, é uma função em Haskell que recebe dois argumentos (a, b) e retorna o maior entre eles.
	Lógico, se os dois valores forem iguais, o maior número vai ser ele próprio.

Qual a relação com *if-else?*

	if (a < b){
		return b;
	}
	else {	
		return a;
	}
    
É isso a relação, não fica mais fácil?

Para comprovar que a função *post* funciona, adicionei o código no arquivo function.hs e executei no interpretador *ghci*, no terminal digite:

	$ ghci
	Prelude>:set prompt "$ "
	$ :l function.hs
	[1 of 1] Compiling Main             ( function.hs, interpreted )
	Ok, modules loaded: Main.

	$ post 2 3
	$ 3

	$ post 3 2
	$ 3

	$ post 333 333
	$ 333

	$ post 'a' 'z'
	$ 'z'
 
_________

<h3>Pattern matching</h3>

Esse recurso é simplismente sensacional!

Haskell reconhece "padrões" que são descritos pelo programador, veja só essa função *andN* que criei.

	andN _ False 		= False
	andN False _ 		= False
	andN True True 		= True


Essa função simula a função AND entre valores lógicos (True e False). Lógico que é possível ajustar para que fique mais compacto, mas essa é uma forma fácil de entender *pattern matching*.

A função recebe dois parâmetros, na primeira linha dizemos que se o segundo parâmetro for *False*, independente do primeiro, a resposta sempre será *False*.

	andN _ False 		= False

Na segunda linha dizemos que se o primeiro parâmetro for *False*, independente do segundo, o resultado será *False*.

	andN False _ 		= False

E na terceira linha é referente quando os dois forem True, que deverá retornar True.

	andN True True	 	= True.


Era isso, valeu!
