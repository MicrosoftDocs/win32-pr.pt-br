---
title: A função named_type_from_local função
description: Os stubs chamam o tipo nomeado \_ \_ da função \_ local.
ms.assetid: ba35e2fb-957e-4e62-b0d4-ae76e30fa343
keywords:
- named_type_from_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c294398913a3bf6fe8b88eed5c42ceec84abf6b23ed994c85ff0fae8f21f2e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127616"
---
# <a name="the-named_type_from_local-function"></a>O tipo \_ nomeado \_ da função \_ local

Os stubs chamam o tipo nomeado \_ \_ da função \_ local. Ele converte o tipo que o aplicativo usa no tipo que os stubs transmitem pela rede. A função é definida como:

``` syntax
void __RPC_USER <named_type>_from_local ( 
    <local_type> __RPC_FAR *, <named_type> __RPC_FAR * __RPC_FAR *);
```

O primeiro parâmetro é um ponteiro para os dados do aplicativo. O segundo parâmetro é um ponteiro para um ponteiro. A função o aponta para os dados transmitidos. A função deve alocar memória para o tipo transmitido.

 

 




