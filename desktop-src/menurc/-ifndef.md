---
title: " ifndef"
description: A diretiva \ ifndef controla a compilação condicional do arquivo de recurso verificando o nome especificado.
ms.assetid: b83d7b0e-1a37-47a8-b495-0eab05ed3a9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 984a969123ea68fd68b14c1b98354b8bc5205aba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105781364"
---
# <a name="ifndef"></a>\#ifndef

A diretiva **\# ifndef** controla a compilação condicional do arquivo de recurso verificando o nome especificado. Se o nome não tiver sido definido ou se sua definição tiver sido removida usando a diretiva **\# undef** , o **\# ifndef** direcionará o compilador para continuar a processar instruções até a próxima diretiva **\# endif**, **\# else** ou **\# elif** e, em seguida, pular para a instrução após a diretiva **\# endif** . Se o nome for definido, **\# ifndef** direcionará o compilador para pular para a próxima diretiva **\# endif**, **\# else** ou **\# elif** .

``` syntax
#ifndef name
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*nomes*
</dt> <dd>

Nome a ser verificado pela diretiva.

</dd> </dl>

## <a name="example"></a>Exemplo

Este exemplo compila a instrução [**bitmap**](bitmap-resource.md) somente se Optimize não estiver definido:

``` syntax
#ifndef Optimize
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Diretivas de pré-processador](preprocessor-directives.md)
</dt> </dl>

 

 




