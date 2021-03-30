---
title: A função named_type_free_inst
description: Os stubs chamam a \_ função de tipo nomeado \_ Free \_ Inst para liberar memória associada ao tipo transmitido.
ms.assetid: 4b9e10cb-25bb-4f00-86a0-5436e5ac71d9
keywords:
- named_type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2d3b5103572eb58e4311c65b0e1cff02e91f66f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635432"
---
# <a name="the-named_type_free_inst-function"></a><span data-ttu-id="3897b-104">A \_ \_ \_ função instra gratuita de tipo nomeado</span><span class="sxs-lookup"><span data-stu-id="3897b-104">The named\_type\_free\_inst Function</span></span>

<span data-ttu-id="3897b-105">Os stubs chamam a função de **\_ tipo nomeado \_ Free \_ Inst** para liberar memória associada ao tipo transmitido.</span><span class="sxs-lookup"><span data-stu-id="3897b-105">The stubs call the **named\_type\_free\_inst** function to free memory associated with the transmitted type.</span></span> <span data-ttu-id="3897b-106">A função é definida como:</span><span class="sxs-lookup"><span data-stu-id="3897b-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <named_type>_free_inst(<type> __RPC_FAR *)
```

<span data-ttu-id="3897b-107">O parâmetro aponta para a instância do tipo transmitido.</span><span class="sxs-lookup"><span data-stu-id="3897b-107">The parameter points to the instance of the transmitted type.</span></span> <span data-ttu-id="3897b-108">Este objeto não deve ser liberado.</span><span class="sxs-lookup"><span data-stu-id="3897b-108">This object should not be freed.</span></span> <span data-ttu-id="3897b-109">Para obter uma discussão sobre quando chamar a função, consulte [o \_ atributo representar como](the-represent-as-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="3897b-109">For a discussion on when to call the function, see [The represent\_as Attribute](the-represent-as-attribute.md).</span></span>

 

 




