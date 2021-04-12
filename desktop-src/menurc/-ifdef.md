---
title: " ifdef"
description: A diretiva \ ifdef controla a compilação condicional do arquivo de recurso verificando o nome especificado.
ms.assetid: 877c6b58-d8a1-4e68-8b69-29fe106d6cbd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38170fb2140f8405a86529c0899c1e4d4e93c026
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364034"
---
# <a name="ifdef"></a>\#ifdef

A diretiva **\# ifdef** controla a compilação condicional do arquivo de recurso verificando o nome especificado. Se o nome tiver sido definido usando uma diretiva de **\# definição** ou usando a opção de linha de comando **/d** com o compilador de recurso, o **\# ifdef** direcionará o compilador para continuar com a instrução imediatamente após a diretiva **\# ifdef** . Se o nome não tiver sido definido, o **\# ifdef** direcionará o compilador para ignorar todas as instruções até a próxima diretiva **\# endif** .

``` syntax
#ifdef name
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*nomes*
</dt> <dd>

Nome a ser verificado pela diretiva.

</dd> </dl>

## <a name="example"></a>Exemplo

Este exemplo compila a instrução [**bitmap**](bitmap-resource.md) somente se a depuração estiver definida:

``` syntax
#ifdef Debug
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Diretivas de pré-processador](preprocessor-directives.md)
</dt> </dl>

 

 




