---
title: " else"
description: A diretiva \ else marca uma cláusula opcional de um bloco de compilação condicional definido por uma diretiva \ ifdef, \ ifndef ou \ If. A diretiva \ else deve ser a última diretiva antes da Diretiva \ endif.
ms.assetid: 982466d9-ae77-4e1c-89f3-511335165da7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086acd9e6323f7be11a65951a33b2b11b680ad46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636039"
---
# <a name="else"></a>\#else

A diretiva **\# else** marca uma cláusula opcional de um bloco de compilação condicional definido por uma diretiva **\# ifdef**, **\# ifndef** ou **\# If** . A diretiva **\# else** deve ser a última diretiva antes da diretiva **\# endif** .

``` syntax
#else
```

Essa diretiva não tem parâmetros.

## <a name="example"></a>Exemplo

Este exemplo compila a segunda instrução de [**bitmap**](bitmap-resource.md) somente se debug não estiver definido:

``` syntax
#ifdef DEBUG
    BITMAP 1 errbox.bmp
#else
    BITMAP 1 userbox.bmp
#endif
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Diretivas de pré-processador](preprocessor-directives.md)
</dt> </dl>

 

 




