---
description: Determina quando o WMI deve liberar um provedor de consumidor de eventos.
ms.assetid: 93246826-8070-4e05-96f0-f773041ed1d4
ms.tgt_platform: multiple
title: Classe __EventConsumerProviderCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumerProviderCacheControl
- Root.__EventConsumerProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: f769427c77f6efdf9a521a63f7334d5d27416c04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765708"
---
# <a name="__eventconsumerprovidercachecontrol-class"></a><span data-ttu-id="0207a-103">\_\_Classe EventConsumerProviderCacheControl</span><span class="sxs-lookup"><span data-stu-id="0207a-103">\_\_EventConsumerProviderCacheControl class</span></span>

<span data-ttu-id="0207a-104">A classe de sistema **\_ \_ EventConsumerProviderCacheControl** determina quando o WMI deve liberar um provedor de consumidor de eventos.</span><span class="sxs-lookup"><span data-stu-id="0207a-104">The **\_\_EventConsumerProviderCacheControl** system class determines when WMI should release an event consumer provider.</span></span> <span data-ttu-id="0207a-105">A classe **\_ \_ EventConsumerProviderCacheControl** é uma classe singleton.</span><span class="sxs-lookup"><span data-stu-id="0207a-105">The **\_\_EventConsumerProviderCacheControl** class is a singleton class.</span></span> <span data-ttu-id="0207a-106">Ele está localizado somente no \\ namespace raiz.</span><span class="sxs-lookup"><span data-stu-id="0207a-106">It is located only in the \\root namespace.</span></span>

<span data-ttu-id="0207a-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0207a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0207a-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="0207a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0207a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0207a-109">Syntax</span></span>

``` syntax
[singleton]
class __EventConsumerProviderCacheControl : CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="0207a-110">Membros</span><span class="sxs-lookup"><span data-stu-id="0207a-110">Members</span></span>

<span data-ttu-id="0207a-111">A classe **\_ \_ EventConsumerProviderCacheControl** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0207a-111">The **\_\_EventConsumerProviderCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="0207a-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0207a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0207a-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0207a-113">Properties</span></span>

<span data-ttu-id="0207a-114">A classe **\_ \_ EventConsumerProviderCacheControl** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0207a-114">The **\_\_EventConsumerProviderCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0207a-115">**ClearAfter**</span><span class="sxs-lookup"><span data-stu-id="0207a-115">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0207a-116">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0207a-116">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0207a-117">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0207a-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0207a-118">Intervalo de tempo após o qual o WMI libera um provedor de consumidor de eventos.</span><span class="sxs-lookup"><span data-stu-id="0207a-118">Time interval after which WMI releases an event consumer provider.</span></span> <span data-ttu-id="0207a-119">Pode levar até duas vezes o intervalo especificado para descarregar o provedor.</span><span class="sxs-lookup"><span data-stu-id="0207a-119">It may take up to twice the interval specified to unload the provider.</span></span> <span data-ttu-id="0207a-120">A hora está no [formato de intervalo](interval-format.md).</span><span class="sxs-lookup"><span data-stu-id="0207a-120">The time is in [interval format](interval-format.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0207a-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="0207a-121">Remarks</span></span>

<span data-ttu-id="0207a-122">A classe **\_ \_ EventConsumerProviderCacheControl** é derivada de [**\_ \_ CacheControl**](--cachecontrol.md).</span><span class="sxs-lookup"><span data-stu-id="0207a-122">The **\_\_EventConsumerProviderCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span> <span data-ttu-id="0207a-123">Para obter mais informações sobre como usar essa classe, consulte [descarregando um provedor](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0207a-123">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0207a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0207a-124">Requirements</span></span>



| <span data-ttu-id="0207a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0207a-125">Requirement</span></span> | <span data-ttu-id="0207a-126">Valor</span><span class="sxs-lookup"><span data-stu-id="0207a-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="0207a-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0207a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0207a-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0207a-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="0207a-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0207a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0207a-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0207a-130">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="0207a-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="0207a-131">Namespace</span></span><br/>                | <span data-ttu-id="0207a-132">Root</span><span class="sxs-lookup"><span data-stu-id="0207a-132">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="0207a-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="0207a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0207a-134">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="0207a-134">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




