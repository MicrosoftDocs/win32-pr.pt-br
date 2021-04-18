---
title: show servicestate
description: Mostra um instantâneo do serviço HTTP.
ms.assetid: a50a3ef5-5e62-412e-a443-11d453778f70
keywords:
- Mostrar HTTP do ServiceState
topic_type:
- apiref
api_name:
- show servicestate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f79bfdb946d286c31ce284efa09e75ad93c34438
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2019
ms.locfileid: "105770230"
---
# <a name="show-servicestate"></a><span data-ttu-id="5546e-104">show servicestate</span><span class="sxs-lookup"><span data-stu-id="5546e-104">show servicestate</span></span>

<span data-ttu-id="5546e-105">Mostra um instantâneo do serviço HTTP.</span><span class="sxs-lookup"><span data-stu-id="5546e-105">Shows a snapshot of the HTTP service.</span></span>

``` syntax
show servicestate [[view=]{session|requestq}] [[verbose=]{yes|no}]
 
```

## <a name="parameters"></a><span data-ttu-id="5546e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5546e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5546e-107"><span id="__view___session_requestq__"></span><span id="__VIEW___SESSION_REQUESTQ__"></span>**\[\[View = \] {Session \| requestq}\]**</span><span class="sxs-lookup"><span data-stu-id="5546e-107"><span id="__view___session_requestq__"></span><span id="__VIEW___SESSION_REQUESTQ__"></span>**\[\[view=\]{session\|requestq}\]**</span></span>
</dt> <dd>

<span data-ttu-id="5546e-108">Exiba o instantâneo do estado do serviço HTTP com base na sessão do servidor ou nas filas de solicitação.</span><span class="sxs-lookup"><span data-stu-id="5546e-108">View snapshot of HTTP service state based on server session or request queues.</span></span>

</dd> <dt>

<span data-ttu-id="5546e-109"><span id="__verbose___yes_no__"></span><span id="__VERBOSE___YES_NO__"></span>**\[\[verbose = \] {Sim \| não}\]**</span><span class="sxs-lookup"><span data-stu-id="5546e-109"><span id="__verbose___yes_no__"></span><span id="__VERBOSE___YES_NO__"></span>**\[\[verbose=\]{yes\|no}\]**</span></span>
</dt> <dd>

<span data-ttu-id="5546e-110">Exiba informações detalhadas mostrando informações de propriedade também.</span><span class="sxs-lookup"><span data-stu-id="5546e-110">View verbose information showing property information too.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="5546e-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5546e-111">Examples</span></span>

<span data-ttu-id="5546e-112">**Mostrar exibição de ServiceState = sessão**</span><span class="sxs-lookup"><span data-stu-id="5546e-112">**show servicestate view=session**</span></span>

<span data-ttu-id="5546e-113">**Mostrar exibição de ServiceState = requestq Verbose = Sim**</span><span class="sxs-lookup"><span data-stu-id="5546e-113">**show servicestate view=requestq verbose=yes**</span></span>

 

 




