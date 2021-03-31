---
title: " elif"
description: A diretiva \ elif marca uma cláusula opcional de um bloco de compilação condicional definido por uma diretiva \ ifdef, \ ifndef ou \ If.
ms.assetid: 432b8543-7e1a-411a-8191-cc0f0e4a2e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a548cff74151dadf4a83a1e7d91ceedeafe07e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005653"
---
# <a name="elif"></a>\#elif

A diretiva **\# elif** marca uma cláusula opcional de um bloco de compilação condicional definido por uma diretiva **\# ifdef**, **\# ifndef** ou **\# If** . A diretiva controla a compilação condicional do arquivo de recurso verificando a expressão constante especificada. Se a expressão constante for diferente de zero, o **\# elif** direcionará o compilador para continuar processando instruções até a próxima diretiva **\# endif**, **\# else** ou **\# elif** e, em seguida, passará para a instrução após **\# endif**. Se a expressão constante for zero, o **\# elif** direcionará o compilador para pular para a próxima diretiva **\# endif**, **\# else** ou **\# elif** . Você pode usar qualquer número de diretivas de **\# elif** em um bloco condicional.

``` syntax
#elif constant-expression
```

<dl> <dt>

<span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*expressão de constante*
</dt> <dd>

Expressão a ser verificada. Esse valor é um nome definido, uma constante de inteiro ou uma expressão que consiste em nomes, inteiros e operadores aritméticos e relacionais.

</dd> </dl>

## <a name="example"></a>Exemplo

Neste exemplo, o **\# elif** instrui o compilador a processar a segunda instrução de [**bitmap**](bitmap-resource.md) somente se o valor atribuído à versão de nome for menor que 7. A diretiva **\# elif** em si só será processada se a versão for maior ou igual a 3.

``` syntax
#if Version < 3
BITMAP 1 errbox.bmp
#elif Version < 7
BITMAP 1 userbox.bmp
#endif
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Diretivas de pré-processador](preprocessor-directives.md)
</dt> </dl>

 

 




