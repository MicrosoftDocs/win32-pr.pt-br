---
title: A função named_type_free_local de dados
description: Os stubs chamam a função local de tipo livre para liberar a memória alocada por uma chamada \_ ao tipo nomeado para a rotina \_ \_ \_ \_ local.
ms.assetid: 8e8c6a46-20c1-483b-b804-0772391e9918
keywords:
- named_type_free_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 123e0eb12a187ee6a5b7665ec126ba98153638e9d766015a0c9e7b1c7aec7dee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924076"
---
# <a name="the-named_type_free_local-function"></a>A função \_ local livre de tipo \_ \_ nomeado

Os stubs chamam a função local de tipo **\_ \_ livre** para liberar a memória alocada por uma chamada ao [tipo nomeado para a rotina \_ \_ \_ local.](the-named-type-to-local-function.md) Ele não libera a memória alocada pelo stub. O protótipo de função é definido como:

``` syntax
void __RPC_USER <local_type>_free_local(<named_type> __RPC_FAR *);
```

O parâmetro é um ponteiro para a memória alocada pelo **tipo \_ nomeado para \_ \_ local.**

 

 




