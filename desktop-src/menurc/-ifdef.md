---
title: " ifdef"
description: A diretiva \ ifdef controla a compilação condicional do arquivo de recurso verificando o nome especificado.
ms.assetid: 877c6b58-d8a1-4e68-8b69-29fe106d6cbd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e834dc84d54e1d6f7725008b8bcf28f4ed49fc3fe45f36fb291ddc397d30eb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034474"
---
# <a name="ifdef"></a>\#Ifdef

A **\# diretiva ifdef** controla a compilação condicional do arquivo de recurso verificando o nome especificado. Se o nome tiver sido definido usando uma diretiva **\# define** ou usando a opção de linha de comando **/d** com o compilador de recursos, **\# ifdef** direcionará o compilador para continuar com a instrução imediatamente após a **\# diretiva ifdef.** Se o nome não tiver sido definido, **\# ifdef** direcionará o compilador a ignorar todas as instruções até a próxima **\# diretiva endif.**

``` syntax
#ifdef name
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*Nome*
</dt> <dd>

Nome a ser verificado pela diretiva .

</dd> </dl>

## <a name="example"></a>Exemplo

Este exemplo compila a [**instrução BITMAP**](bitmap-resource.md) somente se Depurar estiver definido:

``` syntax
#ifdef Debug
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Diretivas de pré-processador](preprocessor-directives.md)
</dt> </dl>

 

 




