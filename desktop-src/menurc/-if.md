---
title: " if"
description: A diretiva \ if controla a compilação condicional do arquivo de recurso verificando a expressão constante especificada.
ms.assetid: 4d0f26a0-1a2d-4fad-b5ce-b9441397d2c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3d898d0089ab6abeefb8c11e3a781446e498ed7c0f490545189987ec4857f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119599706"
---
# <a name="if"></a>\#Se

A **\# diretiva if** controla a compilação condicional do arquivo de recurso verificando a expressão constante especificada. Se a expressão constante for diferente de **\# zero,** se direcionar o compilador para continuar ing instruções até a próxima diretiva **\# endif**, **\# else** ou **\# elif** e, em seguida, ignorar para a instrução após a diretiva **\# endif.** Se a expressão constante for zero, **\# se** direcionar o compilador para ignorar para a próxima diretiva **\# endif**, **\# caso afirmativo** ou **\# elif.**

``` syntax
#if constant-expression
```

<dl> <dt>

<span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*constant-expression*
</dt> <dd>

Expressão a ser verificada. Esse valor é um nome definido, uma constante de inteiro ou uma expressão que consiste em nomes, inteiros e operadores aritméticos e relacionais.

</dd> </dl>

## <a name="example"></a>Exemplo

Este exemplo compila a [**instrução BITMAP**](bitmap-resource.md) somente se o valor atribuído Version for menor que 3:

``` syntax
#if Version < 3
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Diretivas de pré-processador](preprocessor-directives.md)
</dt> </dl>

 

 




