---
description: Usado para determinar quando o WMI libera um ponteiro IWbemUnboundObjectSink de provedores de consumidor de eventos.
ms.assetid: f7b14efc-a2f7-4e99-8ec8-5b5af0743139
ms.tgt_platform: multiple
title: Classe __EventSinkCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventSinkCacheControl
- Root.__EventSinkCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 9d20e64fed1ee6ba5622d5e6a342a60485f53d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810728"
---
# <a name="__eventsinkcachecontrol-class"></a><span data-ttu-id="451b2-103">\_\_Classe EventSinkCacheControl</span><span class="sxs-lookup"><span data-stu-id="451b2-103">\_\_EventSinkCacheControl class</span></span>

<span data-ttu-id="451b2-104">A classe de sistema **\_ \_ EventSinkCacheControl** é usada para determinar quando o WMI libera o ponteiro [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) de um provedor de consumidor de evento.</span><span class="sxs-lookup"><span data-stu-id="451b2-104">The **\_\_EventSinkCacheControl** system class is used to determine when WMI releases an event consumer provider's [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) pointer.</span></span> <span data-ttu-id="451b2-105">A classe **\_ \_ EventSinkCacheControl** é uma classe singleton.</span><span class="sxs-lookup"><span data-stu-id="451b2-105">The **\_\_EventSinkCacheControl** class is a singleton class.</span></span> <span data-ttu-id="451b2-106">Ele está localizado somente no \\ namespace raiz.</span><span class="sxs-lookup"><span data-stu-id="451b2-106">It is located only in the \\root namespace.</span></span>

<span data-ttu-id="451b2-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="451b2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="451b2-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="451b2-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="451b2-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="451b2-109">Syntax</span></span>

``` syntax
[singleton]
class __EventSinkCacheControl : CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="451b2-110">Membros</span><span class="sxs-lookup"><span data-stu-id="451b2-110">Members</span></span>

<span data-ttu-id="451b2-111">A classe **\_ \_ EventSinkCacheControl** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="451b2-111">The **\_\_EventSinkCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="451b2-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="451b2-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="451b2-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="451b2-113">Properties</span></span>

<span data-ttu-id="451b2-114">A classe **\_ \_ EventSinkCacheControl** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="451b2-114">The **\_\_EventSinkCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="451b2-115">**ClearAfter**</span><span class="sxs-lookup"><span data-stu-id="451b2-115">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="451b2-116">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="451b2-116">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="451b2-117">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="451b2-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="451b2-118">Intervalo de tempo após o qual o WMI libera um provedor de eventos.</span><span class="sxs-lookup"><span data-stu-id="451b2-118">Time interval after which WMI releases an event provider.</span></span> <span data-ttu-id="451b2-119">Pode levar até duas vezes o intervalo especificado para descarregar o provedor.</span><span class="sxs-lookup"><span data-stu-id="451b2-119">It can take up to twice the interval specified to unload the provider.</span></span> <span data-ttu-id="451b2-120">A hora está no [formato de intervalo](interval-format.md).</span><span class="sxs-lookup"><span data-stu-id="451b2-120">The time is in [interval format](interval-format.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="451b2-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="451b2-121">Remarks</span></span>

<span data-ttu-id="451b2-122">A classe **\_ \_ EventSinkCacheControl** é derivada de [**\_ \_ CacheControl**](--cachecontrol.md).</span><span class="sxs-lookup"><span data-stu-id="451b2-122">The **\_\_EventSinkCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span> <span data-ttu-id="451b2-123">Para obter mais informações sobre como usar essa classe, consulte [descarregando um provedor](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="451b2-123">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="451b2-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="451b2-124">Requirements</span></span>



| <span data-ttu-id="451b2-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="451b2-125">Requirement</span></span> | <span data-ttu-id="451b2-126">Valor</span><span class="sxs-lookup"><span data-stu-id="451b2-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="451b2-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="451b2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="451b2-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="451b2-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="451b2-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="451b2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="451b2-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="451b2-130">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="451b2-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="451b2-131">Namespace</span></span><br/>                | <span data-ttu-id="451b2-132">Root</span><span class="sxs-lookup"><span data-stu-id="451b2-132">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="451b2-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="451b2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="451b2-134">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="451b2-134">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




