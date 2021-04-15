---
description: Relata um evento de exclusão de namespace, que é um tipo de evento intrínseco que é gerado quando um subnamespace é removido do namespace atual.
ms.assetid: f7160a90-562d-40d9-9189-32aaabcd81d0
ms.tgt_platform: multiple
title: Classe __NamespaceDeletionEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceDeletionEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 6e23f909718167760c02bbdb38e2a075d04bc516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747252"
---
# <a name="__namespacedeletionevent-class"></a><span data-ttu-id="69d9d-103">\_\_Classe NamespaceDeletionEvent</span><span class="sxs-lookup"><span data-stu-id="69d9d-103">\_\_NamespaceDeletionEvent class</span></span>

<span data-ttu-id="69d9d-104">A classe de sistema **\_ \_ NamespaceDeletionEvent** relata um evento de exclusão de namespace, que é um tipo de [evento intrínseco](determining-the-type-of-event-to-receive.md) que é gerado quando um subnamespace é removido do namespace atual.</span><span class="sxs-lookup"><span data-stu-id="69d9d-104">The **\_\_NamespaceDeletionEvent** system class reports a namespace deletion event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) that is generated when a sub-namespace is removed from the current namespace.</span></span>

<span data-ttu-id="69d9d-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="69d9d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="69d9d-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="69d9d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="69d9d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="69d9d-107">Syntax</span></span>

``` syntax
class __NamespaceDeletionEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="69d9d-108">Membros</span><span class="sxs-lookup"><span data-stu-id="69d9d-108">Members</span></span>

<span data-ttu-id="69d9d-109">A classe **\_ \_ NamespaceDeletionEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="69d9d-109">The **\_\_NamespaceDeletionEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="69d9d-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="69d9d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="69d9d-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="69d9d-111">Properties</span></span>

<span data-ttu-id="69d9d-112">A classe **\_ \_ NamespaceDeletionEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="69d9d-112">The **\_\_NamespaceDeletionEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="69d9d-113">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="69d9d-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69d9d-114">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="69d9d-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="69d9d-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="69d9d-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="69d9d-116">Descritor que o provedor de eventos usa para determinar os usuários que podem receber um evento.</span><span class="sxs-lookup"><span data-stu-id="69d9d-116">Descriptor that the event provider uses to determine the users that can receive an event.</span></span> <span data-ttu-id="69d9d-117">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="69d9d-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="69d9d-118">**TargetNamespace**</span><span class="sxs-lookup"><span data-stu-id="69d9d-118">**TargetNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69d9d-119">Tipo de dados: **\_ \_ namespace**</span><span class="sxs-lookup"><span data-stu-id="69d9d-119">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="69d9d-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="69d9d-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="69d9d-121">Cópia da instância de [**\_ \_ namespace**](--namespace.md) que é excluída.</span><span class="sxs-lookup"><span data-stu-id="69d9d-121">Copy of the [**\_\_Namespace**](--namespace.md) instance that is deleted.</span></span> <span data-ttu-id="69d9d-122">A propriedade **Name** da instância do **\_ \_ namespace** identifica o namespace que é excluído.</span><span class="sxs-lookup"><span data-stu-id="69d9d-122">The **Name** property of the **\_\_Namespace** instance identifies the namespace that is deleted.</span></span> <span data-ttu-id="69d9d-123">Essa propriedade é herdada de [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="69d9d-123">This property is inherited from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="69d9d-124">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="69d9d-124">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69d9d-125">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="69d9d-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="69d9d-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="69d9d-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="69d9d-127">Valor exclusivo que indica a hora em que um evento é gerado.</span><span class="sxs-lookup"><span data-stu-id="69d9d-127">Unique value that indicates the time an event is generated.</span></span> <span data-ttu-id="69d9d-128">Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="69d9d-128">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="69d9d-129">As informações estão no formato UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="69d9d-129">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="69d9d-130">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="69d9d-130">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="69d9d-131">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="69d9d-131">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69d9d-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="69d9d-132">Remarks</span></span>

<span data-ttu-id="69d9d-133">A classe **\_ \_ NamespaceDeletionEvent** é derivada de [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="69d9d-133">The **\_\_NamespaceDeletionEvent** class is derived from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="69d9d-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69d9d-134">Requirements</span></span>



| <span data-ttu-id="69d9d-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="69d9d-135">Requirement</span></span> | <span data-ttu-id="69d9d-136">Valor</span><span class="sxs-lookup"><span data-stu-id="69d9d-136">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="69d9d-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69d9d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="69d9d-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="69d9d-138">Windows Vista</span></span><br/>       |
| <span data-ttu-id="69d9d-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69d9d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="69d9d-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69d9d-140">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="69d9d-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="69d9d-141">Namespace</span></span><br/>                | <span data-ttu-id="69d9d-142">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="69d9d-142">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="69d9d-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="69d9d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69d9d-144">**\_\_NamespaceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="69d9d-144">**\_\_NamespaceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--namespaceoperationevent)
</dt> <dt>

[<span data-ttu-id="69d9d-145">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="69d9d-145">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

