---
title: " Ifndef"
description: A diretiva \ ifndef controla a compilação condicional do arquivo de recurso verificando o nome especificado.
ms.assetid: b83d7b0e-1a37-47a8-b495-0eab05ed3a9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23728acabc0ca0179c544a66657a2d1b8343d5eae24556018e0e65025420bfba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472982"
---
# <a name="ifndef"></a>\#Ifndef

A **\# diretiva ifndef** controla a compilação condicional do arquivo de recurso verificando o nome especificado. Se o nome não tiver sido definido ou se sua definição tiver sido removida usando a diretiva **\# undef,** **\# ifndef** direcionará o compilador para continuar processamento de instruções até a diretiva **\# next endif**, **\# else** ou **\# elif** e, em seguida, ignorar para a instrução após a **\# diretiva endif.** Se o nome for definido, **\# ifndef** direcionará o compilador para ignorar para a próxima diretiva **\# endif**, **\# caso afirmativo** ou **\# elif.**

``` syntax
#ifndef name
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*Nome*
</dt> <dd>

Nome a ser verificado pela diretiva .

</dd> </dl>

## <a name="example"></a>Exemplo

Este exemplo compila a [**instrução BITMAP**](bitmap-resource.md) somente se Optimize não estiver definido:

``` syntax
#ifndef Optimize
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Diretivas de pré-processador](preprocessor-directives.md)
</dt> </dl>

 

 




