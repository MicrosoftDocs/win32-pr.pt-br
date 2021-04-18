---
title: " if"
description: A diretiva \ If controla a compilação condicional do arquivo de recurso verificando a expressão constante especificada.
ms.assetid: 4d0f26a0-1a2d-4fad-b5ce-b9441397d2c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 364d6f5eb818813f61f6428446effb4793b96b2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105791461"
---
# <a name="if"></a>\#que

A diretiva **\# If** controla a compilação condicional do arquivo de recurso verificando a expressão constante especificada. Se a expressão constante for **\# diferente de zero, o direcionará** o compilador a continuar processando instruções até a próxima diretiva **\# endif**, **\# else** ou **\# elif** e, em seguida, pular para a instrução após a diretiva **\# endif** . Se a expressão constante for zero, **\# o** direcionará o compilador para pular para a próxima diretiva **\# endif**, **\# else** ou **\# elif** .

``` syntax
#if constant-expression
```

<dl> <dt>

<span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*expressão de constante*
</dt> <dd>

Expressão a ser verificada. Esse valor é um nome definido, uma constante de inteiro ou uma expressão que consiste em nomes, inteiros e operadores aritméticos e relacionais.

</dd> </dl>

## <a name="example"></a>Exemplo

Este exemplo compila a instrução de [**bitmap**](bitmap-resource.md) somente se a versão de valor atribuído for menor que 3:

``` syntax
#if Version < 3
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Diretivas de pré-processador](preprocessor-directives.md)
</dt> </dl>

 

 




