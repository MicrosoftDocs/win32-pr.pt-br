---
description: Controla o cache quando um provedor de propriedades é descarregado.
ms.assetid: 8fc7de7a-889c-4d53-97ea-a676879de1d3
ms.tgt_platform: multiple
title: Classe __PropertyProviderCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PropertyProviderCacheControl
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 1d153049a9635b4b77a1ad09ca0ee64835b9bcfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169812"
---
# <a name="__propertyprovidercachecontrol-class"></a><span data-ttu-id="1f377-103">\_\_Classe PropertyProviderCacheControl</span><span class="sxs-lookup"><span data-stu-id="1f377-103">\_\_PropertyProviderCacheControl class</span></span>

<span data-ttu-id="1f377-104">A classe **\_ \_ PropertyProviderCacheControl** controla o cache quando um provedor de propriedades é descarregado.</span><span class="sxs-lookup"><span data-stu-id="1f377-104">The **\_\_PropertyProviderCacheControl** class controls the cache when a property provider is unloaded.</span></span> <span data-ttu-id="1f377-105">Essa classe existe somente no \\ namespace raiz.</span><span class="sxs-lookup"><span data-stu-id="1f377-105">This class exists only in the \\root namespace.</span></span>

<span data-ttu-id="1f377-106">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1f377-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1f377-107">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="1f377-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f377-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f377-108">Syntax</span></span>

``` syntax
class __PropertyProviderCacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="1f377-109">Membros</span><span class="sxs-lookup"><span data-stu-id="1f377-109">Members</span></span>

<span data-ttu-id="1f377-110">A classe **\_ \_ PropertyProviderCacheControl** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1f377-110">The **\_\_PropertyProviderCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="1f377-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1f377-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1f377-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1f377-112">Properties</span></span>

<span data-ttu-id="1f377-113">A classe **\_ \_ PropertyProviderCacheControl** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1f377-113">The **\_\_PropertyProviderCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1f377-114">**ClearAfter**</span><span class="sxs-lookup"><span data-stu-id="1f377-114">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f377-115">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1f377-115">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1f377-116">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1f377-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1f377-117">Intervalo de tempo após o WMI liberar um provedor de propriedades.</span><span class="sxs-lookup"><span data-stu-id="1f377-117">Time interval after WMI releases a property provider.</span></span> <span data-ttu-id="1f377-118">A hora está no formato de intervalo.</span><span class="sxs-lookup"><span data-stu-id="1f377-118">The time is in the interval format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1f377-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f377-119">Remarks</span></span>

<span data-ttu-id="1f377-120">A classe **\_ \_ PropertyProviderCacheControl** é derivada de [**\_ \_ CacheControl**](--cachecontrol.md).</span><span class="sxs-lookup"><span data-stu-id="1f377-120">The **\_\_PropertyProviderCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span> <span data-ttu-id="1f377-121">Para obter mais informações, consulte [descarregando um provedor](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1f377-121">For more information, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1f377-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f377-122">Requirements</span></span>



| <span data-ttu-id="1f377-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f377-123">Requirement</span></span> | <span data-ttu-id="1f377-124">Valor</span><span class="sxs-lookup"><span data-stu-id="1f377-124">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="1f377-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f377-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1f377-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1f377-126">Windows Vista</span></span><br/>       |
| <span data-ttu-id="1f377-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f377-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1f377-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f377-128">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="1f377-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="1f377-129">Namespace</span></span><br/>                | <span data-ttu-id="1f377-130">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="1f377-130">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="1f377-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f377-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f377-132">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="1f377-132">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




