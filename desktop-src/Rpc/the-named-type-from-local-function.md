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
# <a name="the-named_type_from_local-function"></a><span data-ttu-id="8716d-104">O \_ tipo nomeado \_ da \_ função local</span><span class="sxs-lookup"><span data-stu-id="8716d-104">The named\_type\_from\_local Function</span></span>

<span data-ttu-id="8716d-105">Os stubs chamam o \_ tipo nomeado \_ da \_ função local.</span><span class="sxs-lookup"><span data-stu-id="8716d-105">The stubs call the named\_type\_from\_local function.</span></span> <span data-ttu-id="8716d-106">Ele converte o tipo que o aplicativo usa no tipo que os stubs transmitem pela rede.</span><span class="sxs-lookup"><span data-stu-id="8716d-106">It converts the type that the application uses into the type the stubs transmit across the network.</span></span> <span data-ttu-id="8716d-107">A função é definida como:</span><span class="sxs-lookup"><span data-stu-id="8716d-107">The function is defined as:</span></span>

``` syntax
void __RPC_USER <named_type>_from_local ( 
    <local_type> __RPC_FAR *, <named_type> __RPC_FAR * __RPC_FAR *);
```

<span data-ttu-id="8716d-108">O primeiro parâmetro é um ponteiro para os dados do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8716d-108">The first parameter is a pointer to the application data.</span></span> <span data-ttu-id="8716d-109">O segundo parâmetro é um ponteiro para um ponteiro.</span><span class="sxs-lookup"><span data-stu-id="8716d-109">The second parameter is a pointer to a pointer.</span></span> <span data-ttu-id="8716d-110">A função a aponta para os dados transmitidos.</span><span class="sxs-lookup"><span data-stu-id="8716d-110">The function points it to the transmitted data.</span></span> <span data-ttu-id="8716d-111">A função deve alocar memória para o tipo transmitido.</span><span class="sxs-lookup"><span data-stu-id="8716d-111">The function must allocate memory for the transmitted type.</span></span>

 

 




