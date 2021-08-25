---
title: " elif"
description: A diretiva \ elif marca uma cláusula opcional de um bloco de compilação condicional definido por uma diretiva \ ifdef, \ ifndef ou \ if.
ms.assetid: 432b8543-7e1a-411a-8191-cc0f0e4a2e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92e131d40648bcda75025087717798ceb2ad1262d680877512dbb85a451fc86e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720896"
---
# <a name="elif"></a>\#elif

A **\# diretiva elif** marca uma cláusula opcional de um bloco de compilação condicional definido por uma diretiva **\# ifdef**, **\# ifndef** ou **\# if.** A diretiva controla a compilação condicional do arquivo de recurso verificando a expressão constante especificada. Se a expressão constante for diferente de zero, **\# elif** direcionará o compilador para continuar ing instruções até a próxima diretiva **\# endif**, **\# else** ou **\# elif** e, em seguida, ignorará para a instrução após **\# endif**. Se a expressão constante for zero, **\# elif** direcionará o compilador para ignorar para a próxima diretiva **\# endif**, **\# else** ou **\# elif.** Você pode usar qualquer número de **\# diretivas elif** em um bloco condicional.

``` syntax
#elif constant-expression
```

<dl> <dt>

<span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*constant-expression*
</dt> <dd>

Expressão a ser verificada. Esse valor é um nome definido, uma constante de inteiro ou uma expressão que consiste em nomes, inteiros e operadores aritméticos e relacionais.

</dd> </dl>

## <a name="example"></a>Exemplo

Neste exemplo, **\# elif** direciona o compilador para processar a segunda instrução [**BITMAP**](bitmap-resource.md) somente se o valor atribuído ao nome Version for menor que 7. A **\# própria diretiva elif** será processada somente se Version for maior ou igual a 3.

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

 

 




