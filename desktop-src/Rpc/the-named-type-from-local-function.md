---
title: A função named_type_from_local
description: Os stubs chamam o \_ tipo nomeado \_ da \_ função local.
ms.assetid: ba35e2fb-957e-4e62-b0d4-ae76e30fa343
keywords:
- named_type_from_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94606a197f3763770db8e0d455a9d0b09f5dab0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291970"
---
# <a name="the-named_type_from_local-function"></a>O \_ tipo nomeado \_ da \_ função local

Os stubs chamam o \_ tipo nomeado \_ da \_ função local. Ele converte o tipo que o aplicativo usa no tipo que os stubs transmitem pela rede. A função é definida como:

``` syntax
void __RPC_USER <named_type>_from_local ( 
    <local_type> __RPC_FAR *, <named_type> __RPC_FAR * __RPC_FAR *);
```

O primeiro parâmetro é um ponteiro para os dados do aplicativo. O segundo parâmetro é um ponteiro para um ponteiro. A função a aponta para os dados transmitidos. A função deve alocar memória para o tipo transmitido.

 

 




