---
description: Class é a classe base abstrata para classes que são usadas para determinar quando o WMI deve liberar um objeto COM (Component Object Model).
ms.assetid: 32631610-8c0e-4f04-b0b2-62e5f8e23ef4
ms.tgt_platform: multiple
title: Classe __CacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __CacheControl
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: fe5358630a7ac5eb48751135d39c2fd998196bf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105779262"
---
# <a name="__cachecontrol-class"></a><span data-ttu-id="842aa-103">\_\_Classe CacheControl</span><span class="sxs-lookup"><span data-stu-id="842aa-103">\_\_CacheControl class</span></span>

<span data-ttu-id="842aa-104">A classe de sistema **\_ \_ CacheControl** é a classe base abstrata para classes que são usadas para determinar quando o WMI deve liberar um objeto com (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="842aa-104">The **\_\_CacheControl** system class is the abstract base class for classes that are used to determine when WMI should release a Component Object Model (COM) object.</span></span> <span data-ttu-id="842aa-105">As instâncias dessa classe nunca são criadas.</span><span class="sxs-lookup"><span data-stu-id="842aa-105">Instances of this class are never created.</span></span> <span data-ttu-id="842aa-106">A classe **\_ \_ CacheControl** está localizada somente no namespace raiz.</span><span class="sxs-lookup"><span data-stu-id="842aa-106">The **\_\_CacheControl** class is located only in the root namespace.</span></span> <span data-ttu-id="842aa-107">Para obter mais informações sobre como usar essa classe, consulte [descarregando um provedor](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="842aa-107">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

<span data-ttu-id="842aa-108">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="842aa-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="842aa-109">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="842aa-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="842aa-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="842aa-110">Syntax</span></span>

``` syntax
[abstract]
class __CacheControl : __SystemClass
{
};
```

## <a name="members"></a><span data-ttu-id="842aa-111">Membros</span><span class="sxs-lookup"><span data-stu-id="842aa-111">Members</span></span>

<span data-ttu-id="842aa-112">A classe **\_ \_ CacheControl** não define nenhum membro.</span><span class="sxs-lookup"><span data-stu-id="842aa-112">The **\_\_CacheControl** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="842aa-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="842aa-113">Remarks</span></span>

<span data-ttu-id="842aa-114">A classe **\_ \_ CacheControl** é derivada de [**\_ \_ SystemClass**](--systemclass.md).</span><span class="sxs-lookup"><span data-stu-id="842aa-114">The **\_\_CacheControl** class is derived from [**\_\_SystemClass**](--systemclass.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="842aa-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="842aa-115">Requirements</span></span>



| <span data-ttu-id="842aa-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="842aa-116">Requirement</span></span> | <span data-ttu-id="842aa-117">Valor</span><span class="sxs-lookup"><span data-stu-id="842aa-117">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="842aa-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="842aa-118">Minimum supported client</span></span><br/> | <span data-ttu-id="842aa-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="842aa-119">Windows Vista</span></span><br/>       |
| <span data-ttu-id="842aa-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="842aa-120">Minimum supported server</span></span><br/> | <span data-ttu-id="842aa-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="842aa-121">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="842aa-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="842aa-122">Namespace</span></span><br/>                | <span data-ttu-id="842aa-123">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="842aa-123">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="842aa-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="842aa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="842aa-125">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="842aa-125">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="842aa-126">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="842aa-126">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="842aa-127">**\_\_EventConsumerProviderCacheControl**</span><span class="sxs-lookup"><span data-stu-id="842aa-127">**\_\_EventConsumerProviderCacheControl**</span></span>](--eventconsumerprovidercachecontrol.md)
</dt> <dt>

[<span data-ttu-id="842aa-128">**\_\_EventProviderCacheControl**</span><span class="sxs-lookup"><span data-stu-id="842aa-128">**\_\_EventProviderCacheControl**</span></span>](--eventprovidercachecontrol.md)
</dt> <dt>

[<span data-ttu-id="842aa-129">**\_\_EventSinkCacheControl**</span><span class="sxs-lookup"><span data-stu-id="842aa-129">**\_\_EventSinkCacheControl**</span></span>](--eventsinkcachecontrol.md)
</dt> <dt>

[<span data-ttu-id="842aa-130">**\_\_ObjectProviderCacheControl**</span><span class="sxs-lookup"><span data-stu-id="842aa-130">**\_\_ObjectProviderCacheControl**</span></span>](--objectprovidercachecontrol.md)
</dt> <dt>

[<span data-ttu-id="842aa-131">\_\_PropertyProviderCacheControl</span><span class="sxs-lookup"><span data-stu-id="842aa-131">\_\_PropertyProviderCacheControl</span></span>](--propertyprovidercachecontrol.md)
</dt> <dt>

[<span data-ttu-id="842aa-132">Descarregando um provedor</span><span class="sxs-lookup"><span data-stu-id="842aa-132">Unloading a Provider</span></span>](unloading-a-provider.md)
</dt> </dl>

 

