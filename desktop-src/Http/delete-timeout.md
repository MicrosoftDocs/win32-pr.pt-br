---
title: delete timeout
description: Exclui um tempo limite global e faz com que o serviço de HTTP.sys reverta para os valores padrão.
ms.assetid: 5fcd5df4-023e-486d-b41a-639e210a128f
keywords:
- excluir tempo limite HTTP
topic_type:
- apiref
api_name:
- delete timeout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6ee436e1eb7f545a74aa56f6c146afbd1c57066
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2019
ms.locfileid: "105766910"
---
# <a name="delete-timeout"></a><span data-ttu-id="87c84-104">delete timeout</span><span class="sxs-lookup"><span data-stu-id="87c84-104">delete timeout</span></span>

<span data-ttu-id="87c84-105">Exclui um tempo limite global e faz com que o serviço de HTTP.sys reverta para os valores padrão.</span><span class="sxs-lookup"><span data-stu-id="87c84-105">Deletes a global timeout and makes the HTTP.sys service revert to default values.</span></span>

``` syntax
delete timeout [timeouttype=]{idleconnectiontimeout|headerwaittimeout}
 
```

## <a name="parameters"></a><span data-ttu-id="87c84-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87c84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87c84-107"><span id="_timeouttype___idleconnectiontimeout_headerwaittimeout_"></span><span id="_TIMEOUTTYPE___IDLECONNECTIONTIMEOUT_HEADERWAITTIMEOUT_"></span>**\[timeouttype = \] {idleConnectionTimeout \| HeaderWaitTimeout}**</span><span class="sxs-lookup"><span data-stu-id="87c84-107"><span id="_timeouttype___idleconnectiontimeout_headerwaittimeout_"></span><span id="_TIMEOUTTYPE___IDLECONNECTIONTIMEOUT_HEADERWAITTIMEOUT_"></span>**\[timeouttype=\]{idleconnectiontimeout\|headerwaittimeout}**</span></span>
</dt> <dd>

<span data-ttu-id="87c84-108">Especifica o tipo de configuração de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="87c84-108">Specifies the type of timeout setting.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="87c84-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="87c84-109">Examples</span></span>

<span data-ttu-id="87c84-110">**delete timeout timeouttype=idleconnectiontimeout**</span><span class="sxs-lookup"><span data-stu-id="87c84-110">**delete timeout timeouttype=idleconnectiontimeout**</span></span>

<span data-ttu-id="87c84-111">**delete timeout timeouttype=headerwaittimeout**</span><span class="sxs-lookup"><span data-stu-id="87c84-111">**delete timeout timeouttype=headerwaittimeout**</span></span>

 

 




