---
description: Controla quando um provedor de eventos é descarregado.
ms.assetid: 7f11e521-d0f6-4c3c-8bfe-ceed2d106ed3
ms.tgt_platform: multiple
title: Classe __EventProviderCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventProviderCacheControl
- Root.__EventProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: c54ec47b1f67d96816cf24a6b6e0108ee0b1de70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170392"
---
# <a name="__eventprovidercachecontrol-class"></a><span data-ttu-id="08729-103">\_\_Classe EventProviderCacheControl</span><span class="sxs-lookup"><span data-stu-id="08729-103">\_\_EventProviderCacheControl class</span></span>

<span data-ttu-id="08729-104">A classe de sistema **\_ \_ EventProviderCacheControl** controla quando um provedor de eventos é descarregado.</span><span class="sxs-lookup"><span data-stu-id="08729-104">The **\_\_EventProviderCacheControl** system class controls when an event provider is unloaded.</span></span> <span data-ttu-id="08729-105">Ele está localizado somente no \\ namespace raiz.</span><span class="sxs-lookup"><span data-stu-id="08729-105">It is located only in the \\root namespace.</span></span>

<span data-ttu-id="08729-106">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="08729-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="08729-107">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="08729-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="08729-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="08729-108">Syntax</span></span>

``` syntax
[singleton]
class __EventProviderCacheControl : __CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="08729-109">Membros</span><span class="sxs-lookup"><span data-stu-id="08729-109">Members</span></span>

<span data-ttu-id="08729-110">A classe **\_ \_ EventProviderCacheControl** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="08729-110">The **\_\_EventProviderCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="08729-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="08729-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="08729-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="08729-112">Properties</span></span>

<span data-ttu-id="08729-113">A classe **\_ \_ EventProviderCacheControl** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="08729-113">The **\_\_EventProviderCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="08729-114">**ClearAfter**</span><span class="sxs-lookup"><span data-stu-id="08729-114">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08729-115">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="08729-115">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="08729-116">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="08729-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="08729-117">Intervalo de tempo após Instrumentação de Gerenciamento do Windows (WMI) libera um provedor de eventos.</span><span class="sxs-lookup"><span data-stu-id="08729-117">Time interval after Windows Management Instrumentation (WMI) releases an event provider.</span></span> <span data-ttu-id="08729-118">A hora está no [formato de intervalo](interval-format.md).</span><span class="sxs-lookup"><span data-stu-id="08729-118">The time is in [interval format](interval-format.md).</span></span> <span data-ttu-id="08729-119">Pode levar até duas vezes o intervalo especificado para descarregar o provedor.</span><span class="sxs-lookup"><span data-stu-id="08729-119">It may take up to twice the interval specified to unload the provider.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08729-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="08729-120">Remarks</span></span>

<span data-ttu-id="08729-121">A classe **\_ \_ EventProviderCacheControl** é derivada de [**\_ \_ CacheControl**](--cachecontrol.md).</span><span class="sxs-lookup"><span data-stu-id="08729-121">The **\_\_EventProviderCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span>

<span data-ttu-id="08729-122">Para obter mais informações sobre como usar essa classe, consulte [descarregando um provedor](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="08729-122">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="08729-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08729-123">Requirements</span></span>



| <span data-ttu-id="08729-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="08729-124">Requirement</span></span> | <span data-ttu-id="08729-125">Valor</span><span class="sxs-lookup"><span data-stu-id="08729-125">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="08729-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08729-126">Minimum supported client</span></span><br/> | <span data-ttu-id="08729-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08729-127">Windows Vista</span></span><br/>       |
| <span data-ttu-id="08729-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08729-128">Minimum supported server</span></span><br/> | <span data-ttu-id="08729-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="08729-129">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="08729-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="08729-130">Namespace</span></span><br/>                | <span data-ttu-id="08729-131">Root</span><span class="sxs-lookup"><span data-stu-id="08729-131">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="08729-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="08729-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08729-133">**\_\_CacheControl**</span><span class="sxs-lookup"><span data-stu-id="08729-133">**\_\_CacheControl**</span></span>](/windows/desktop/WmiSdk/--cachecontrol)
</dt> <dt>

[<span data-ttu-id="08729-134">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="08729-134">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

