---
description: Controla quando um provedor de classe ou instância é descarregado.
ms.assetid: 4cbeb820-8a65-4fab-97f1-2a973b2a4310
ms.tgt_platform: multiple
title: Classe __ObjectProviderCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ObjectProviderCacheControl
- Root.__ObjectProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 53cfaa69afead4f436879f128a4d42e50d36fe67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781660"
---
# <a name="__objectprovidercachecontrol-class"></a><span data-ttu-id="c61c9-103">\_\_Classe ObjectProviderCacheControl</span><span class="sxs-lookup"><span data-stu-id="c61c9-103">\_\_ObjectProviderCacheControl class</span></span>

<span data-ttu-id="c61c9-104">A classe de sistema **\_ \_ ObjectProviderCacheControl** controla quando um provedor de classe ou instância é descarregado.</span><span class="sxs-lookup"><span data-stu-id="c61c9-104">The **\_\_ObjectProviderCacheControl** system class controls when a class or instance provider is unloaded.</span></span> <span data-ttu-id="c61c9-105">Ele está localizado somente no \\ namespace raiz.</span><span class="sxs-lookup"><span data-stu-id="c61c9-105">It is located only in the \\root namespace.</span></span>

<span data-ttu-id="c61c9-106">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c61c9-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c61c9-107">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="c61c9-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c61c9-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c61c9-108">Syntax</span></span>

``` syntax
[singleton]
class __ObjectProviderCacheControl : __CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="c61c9-109">Membros</span><span class="sxs-lookup"><span data-stu-id="c61c9-109">Members</span></span>

<span data-ttu-id="c61c9-110">A classe **\_ \_ ObjectProviderCacheControl** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c61c9-110">The **\_\_ObjectProviderCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="c61c9-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c61c9-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c61c9-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c61c9-112">Properties</span></span>

<span data-ttu-id="c61c9-113">A classe **\_ \_ ObjectProviderCacheControl** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c61c9-113">The **\_\_ObjectProviderCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c61c9-114">**ClearAfter**</span><span class="sxs-lookup"><span data-stu-id="c61c9-114">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c61c9-115">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c61c9-115">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c61c9-116">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c61c9-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c61c9-117">Intervalo de tempo após o qual o WMI libera uma instância, uma classe ou um provedor de métodos.</span><span class="sxs-lookup"><span data-stu-id="c61c9-117">Time interval after which WMI releases an instance, class, or method provider.</span></span> <span data-ttu-id="c61c9-118">A hora está no [formato de intervalo](interval-format.md).</span><span class="sxs-lookup"><span data-stu-id="c61c9-118">The time is in [interval format](interval-format.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c61c9-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="c61c9-119">Remarks</span></span>

<span data-ttu-id="c61c9-120">A classe **\_ \_ ObjectProviderCacheControl** é derivada de [**\_ \_ CacheControl**](--cachecontrol.md).</span><span class="sxs-lookup"><span data-stu-id="c61c9-120">The **\_\_ObjectProviderCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span> <span data-ttu-id="c61c9-121">Para obter mais informações sobre como usar essa classe, consulte [descarregando um provedor](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c61c9-121">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c61c9-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c61c9-122">Requirements</span></span>



| <span data-ttu-id="c61c9-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c61c9-123">Requirement</span></span> | <span data-ttu-id="c61c9-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c61c9-124">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="c61c9-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c61c9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c61c9-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c61c9-126">Windows Vista</span></span><br/>       |
| <span data-ttu-id="c61c9-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c61c9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c61c9-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c61c9-128">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="c61c9-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="c61c9-129">Namespace</span></span><br/>                | <span data-ttu-id="c61c9-130">Root</span><span class="sxs-lookup"><span data-stu-id="c61c9-130">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="c61c9-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="c61c9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c61c9-132">**\_\_CacheControl**</span><span class="sxs-lookup"><span data-stu-id="c61c9-132">**\_\_CacheControl**</span></span>](/windows/desktop/WmiSdk/--cachecontrol)
</dt> <dt>

[<span data-ttu-id="c61c9-133">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="c61c9-133">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="c61c9-134">Recebendo eventos em todos os momentos</span><span class="sxs-lookup"><span data-stu-id="c61c9-134">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> </dl>

 

