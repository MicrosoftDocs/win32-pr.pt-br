---
title: A função named_type_free_local
description: Os stubs chamam o tipo de \_ \_ função local Free para liberar a memória alocada por uma chamada para o \_ tipo nomeado \_ para \_ rotina local.
ms.assetid: 8e8c6a46-20c1-483b-b804-0772391e9918
keywords:
- named_type_free_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f2796f33e9dc60364b6afda244d8dae47eef0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635431"
---
# <a name="the-named_type_free_local-function"></a>O \_ tipo nomeado \_ \_ função local gratuita

Os stubs chamam o tipo de função **\_ \_ local Free** para liberar a memória alocada por uma chamada para o [ \_ tipo nomeado para rotina \_ \_ local](the-named-type-to-local-function.md) . Ele não libera a memória alocada pelo stub. O protótipo de função é definido como:

``` syntax
void __RPC_USER <local_type>_free_local(<named_type> __RPC_FAR *);
```

O parâmetro é um ponteiro para a memória alocada **pelo \_ tipo nomeado \_ para \_ local**.

 

 




