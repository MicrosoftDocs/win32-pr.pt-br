---
description: Você pode definir e atribuir escopos de entrada personalizados usando a sintaxe de expressão regular de manuscrito que é compreendida por alguns dos reconhecedores de manuscrito da Microsoft.
ms.assetid: e3afe735-eca8-4fda-bd5b-cc0ab0b6a872
title: Referência de sintaxe de expressão regular
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c0de50ff37795032719d9bc90ee81891324ba9
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104172421"
---
# <a name="regular-expression-syntax-reference"></a>Referência de sintaxe de expressão regular

Você pode definir e atribuir escopos de entrada personalizados usando a sintaxe de expressão regular de manuscrito que é compreendida por alguns dos reconhecedores de manuscrito da Microsoft. A sintaxe é um subconjunto da [implementação da linguagem de expressão regular](/documentation/?url=%2flibrary%2fcpgenref%2fhtml%2fcpconRegularExpressionsLanguageElements.asp%3fframe%3dtrue) no .NET Framework.

Há algumas diferenças na maneira como as expressões regulares manuscritas são usadas e a maneira como os outros tipos de expressões regulares são usados. A sintaxe de manuscrito é usada para especificar uma cadeia de caracteres exata que será correspondida pelo mecanismo de reconhecimento e não por uma subcadeia de caracteres. Por exemplo, a expressão regular s ( \[ a-z \] +) p retornaria correspondências para "sopa", "parar", "inetapa" e "esophagus". Enquanto que uma expressão regular de manuscrito equivalente, como s (! IS \_ ONECHAR) + p, corresponderia a "sopa" e "Stop", mas não "Instep" e "esophagus".

As expressões regulares manuscritas não dão suporte a espaços não separáveis em expressões regulares. Ou seja, você não pode usar a entidade "nbsp" em uma expressão regular de manuscrito.

As seções a seguir descrevem a sintaxe em mais detalhes.

## <a name="valid-operators"></a>Operadores válidos

Os operadores a seguir são válidos para a criação de expressões regulares para definir escopos de entrada para reconhecedores de manuscrito.



| Operador      | Descrição                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| \*<br/> | Operador unário de sufixo que significa zero ou mais ocorrências do operando.<br/> |
| +<br/>  | Operador unário de sufixo que representa uma ou mais ocorrências do operando.<br/>  |
| ?<br/>  | Operador unário de sufixo que significa zero ou uma ocorrência do operando.<br/>   |
| \|<br/> | Operador de infixos binários que significa "ou".<br/>                                        |
| ()<br/> | Usado para agrupar itens.<br/>                                                       |



 

A implementação da Microsoft de expressões regulares para reconhecedores de manuscrito permite aplicativos repetidos de operadores unários de sufixo. Por exemplo, a \* \* = (a \* ) \* = a \* , b?? = (b?)? = b?. Eles também permitem repetições não consecutivas, por exemplo: a \* ? \* = ((a \* )?) \* = (a \* ) \* = a \* . Isso é diferente de .NET Framework expressões regulares, que permitem apenas o? operador a ser repetido.

Outra diferença de .NET Framework expressões regulares é que as expressões regulares manuscritas não dão suporte a uma expressão vazia designada com um par de parênteses vazio, ().

> [!Note]  
> Somente caracteres na página de código 1252 têm suporte para expressões regulares de manuscrito.

 

## <a name="using-input-scopes"></a>Usando escopos de entrada

Você também pode usar o conjunto de escopos de entrada regulares que são definidos como parte da função [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) em suas expressões regulares. Por exemplo, o valor de mês (numérico) é \_ Data \_ mês. A sintaxe para especificar um escopo de entrada como parte de uma expressão regular é preceder o valor enumerado do escopo de entrada com um parêntese de abertura e um ponto de exclamação, (!, e colocar um parêntese de fechamento,) no final. Por exemplo:

(! É \_ Data \_ mês)

Se você combinar o \_ escopo de entrada padrão por Oring-lo com qualquer outro escopo de entrada, o efeito é que o reconhecedor pode retornar qualquer expressão única compatível com o modelo de idioma padrão (por exemplo, uma palavra do dicionário do sistema ou uma data) com ou sem pontuação, ou qualquer valor que atenda ao restante da expressão regular passada para o reconhecedor.

> [!Note]  
> Os seguintes membros de [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) não têm suporte em expressões regulares: is \_ formulalist, is \_ REGULAREXPRESSION, é \_ SRGS, é \_ XML.

 

## <a name="unsupported-operators"></a>Operadores sem suporte

Os operadores de expressão regular a seguir não têm suporte ao criar expressões regulares de manuscrito.



| Operador                                     | Descrição                                                         |
|----------------------------------------------|---------------------------------------------------------------------|
| .<br/>                                 | Caractere de período.<br/>                                        |
| \[\]<br/>                              | Colchetes. Use parênteses para agrupar itens.<br/>     |
| {}<br/>                                | Chaves.<br/>                                          |
| (?\# Comentário) e \# \[ Comentário\]<br/> | Comentários.<br/>                                                |
| $<br/>                                 | Caractere de cifrão.<br/>                                   |
| ^<br/>                                 | Caractere de cursor.<br/>                                         |
| -<br/>                                 | Caractere de traço. Deve ou ( \| ) reunir todos os conjuntos de itens.<br/> |



 

## <a name="escaping-characters"></a>Substituindo caracteres

Os caracteres comuns, além daqueles na tabela a seguir, correspondem a si mesmos. Ou seja, um "a" em uma expressão regular especifica que a entrada deve corresponder a um "a".

Outra diferença significativa na escrita de expressões regulares de manuscrito é que você só pode escapar um conjunto limitado de caracteres dentro de uma expressão regular. A tabela a seguir descreve o conjunto de caracteres permitido que pode ter escape. Qualquer outra tentativa de escapar de um caractere resultará em um erro sendo gerado pelo reconhecedor.



| Caractere       |
|-----------------|
| \\\*<br/> |
| \\+<br/>  |
| \\?<br/>  |
| \\(<br/>  |
| \\)<br/>  |
| \\\|<br/> |
| \\\\<br/> |
| \\!<br/>  |
| \\.<br/>  |
| \\\[<br/> |
| \\\]<br/> |
| \\^<br/>  |
| \\{<br/>  |
| \\}<br/>  |
| \\$<br/>  |
| \\\#<br/> |



 

 

 