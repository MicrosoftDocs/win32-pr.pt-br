---
description: Uma classe base para todos os eventos intrínsecos relacionados a um namespace.
ms.assetid: 168637b1-217e-4b6d-bd07-25127b9e9f6c
ms.tgt_platform: multiple
title: Classe __NamespaceOperationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: d263af0eab5fc3899b45659bc8409a5e68776fe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752563"
---
# <a name="__namespaceoperationevent-class"></a><span data-ttu-id="b32e0-103">\_\_Classe NamespaceOperationEvent</span><span class="sxs-lookup"><span data-stu-id="b32e0-103">\_\_NamespaceOperationEvent class</span></span>

<span data-ttu-id="b32e0-104">A classe de sistema **\_ \_ NamespaceOperationEvent** é uma classe base para todos os eventos intrínsecos relacionados a um namespace.</span><span class="sxs-lookup"><span data-stu-id="b32e0-104">The **\_\_NamespaceOperationEvent** system class is a base class for all intrinsic events that relate to a namespace.</span></span>

<span data-ttu-id="b32e0-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b32e0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b32e0-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="b32e0-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b32e0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b32e0-107">Syntax</span></span>

``` syntax
class __NamespaceOperationEvent : __Event
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="b32e0-108">Membros</span><span class="sxs-lookup"><span data-stu-id="b32e0-108">Members</span></span>

<span data-ttu-id="b32e0-109">A classe **\_ \_ NamespaceOperationEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b32e0-109">The **\_\_NamespaceOperationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="b32e0-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b32e0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b32e0-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b32e0-111">Properties</span></span>

<span data-ttu-id="b32e0-112">A classe **\_ \_ NamespaceOperationEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b32e0-112">The **\_\_NamespaceOperationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b32e0-113">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="b32e0-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32e0-114">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="b32e0-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="b32e0-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b32e0-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b32e0-116">Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento.</span><span class="sxs-lookup"><span data-stu-id="b32e0-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="b32e0-117">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="b32e0-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="b32e0-118">**TargetNamespace**</span><span class="sxs-lookup"><span data-stu-id="b32e0-118">**TargetNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32e0-119">Tipo de dados: **\_ \_ namespace**</span><span class="sxs-lookup"><span data-stu-id="b32e0-119">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="b32e0-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b32e0-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b32e0-121">Namespace afetado pelo evento.</span><span class="sxs-lookup"><span data-stu-id="b32e0-121">Namespace affected by the event.</span></span> <span data-ttu-id="b32e0-122">Para eventos de criação, esse é o namespace recém-criado.</span><span class="sxs-lookup"><span data-stu-id="b32e0-122">For creation events, this is the newly created namespace.</span></span> <span data-ttu-id="b32e0-123">Para eventos de modificação, este é o namespace alterado.</span><span class="sxs-lookup"><span data-stu-id="b32e0-123">For modification events, this is the changed namespace.</span></span> <span data-ttu-id="b32e0-124">Para eventos de exclusão, esse é o namespace excluído.</span><span class="sxs-lookup"><span data-stu-id="b32e0-124">For deletion events, this is the deleted namespace.</span></span>

</dd> <dt>

<span data-ttu-id="b32e0-125">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="b32e0-125">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32e0-126">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b32e0-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b32e0-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b32e0-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b32e0-128">Valor exclusivo que indica a hora em que o evento foi gerado.</span><span class="sxs-lookup"><span data-stu-id="b32e0-128">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="b32e0-129">Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="b32e0-129">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="b32e0-130">As informações estão no formato UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="b32e0-130">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="b32e0-131">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="b32e0-131">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="b32e0-132">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b32e0-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b32e0-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="b32e0-133">Remarks</span></span>

<span data-ttu-id="b32e0-134">A classe **\_ \_ NamespaceOperationEvent** é derivada de [**\_ \_ Event**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="b32e0-134">The **\_\_NamespaceOperationEvent** class is derived from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="b32e0-135">As instâncias dessa classe não são criadas.</span><span class="sxs-lookup"><span data-stu-id="b32e0-135">Instances of this class are not created.</span></span> <span data-ttu-id="b32e0-136">O WMI cria instâncias de uma das seguintes classes derivadas desta classe:</span><span class="sxs-lookup"><span data-stu-id="b32e0-136">WMI creates instances of one of the following classes derived from this class:</span></span>

[<span data-ttu-id="b32e0-137">**\_\_NamespaceCreationEvent**</span><span class="sxs-lookup"><span data-stu-id="b32e0-137">**\_\_NamespaceCreationEvent**</span></span>](--namespacecreationevent.md)

[<span data-ttu-id="b32e0-138">**\_\_NamespaceModificationEvent**</span><span class="sxs-lookup"><span data-stu-id="b32e0-138">**\_\_NamespaceModificationEvent**</span></span>](--namespacemodificationevent.md)

[<span data-ttu-id="b32e0-139">**\_\_NamespaceDeletionEvent**</span><span class="sxs-lookup"><span data-stu-id="b32e0-139">**\_\_NamespaceDeletionEvent**</span></span>](--namespacedeletionevent.md)

## <a name="requirements"></a><span data-ttu-id="b32e0-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b32e0-140">Requirements</span></span>



| <span data-ttu-id="b32e0-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="b32e0-141">Requirement</span></span> | <span data-ttu-id="b32e0-142">Valor</span><span class="sxs-lookup"><span data-stu-id="b32e0-142">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b32e0-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b32e0-143">Minimum supported client</span></span><br/> | <span data-ttu-id="b32e0-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b32e0-144">Windows Vista</span></span><br/>       |
| <span data-ttu-id="b32e0-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b32e0-145">Minimum supported server</span></span><br/> | <span data-ttu-id="b32e0-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b32e0-146">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="b32e0-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="b32e0-147">Namespace</span></span><br/>                | <span data-ttu-id="b32e0-148">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="b32e0-148">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="b32e0-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="b32e0-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b32e0-150">**\_\_Evento**</span><span class="sxs-lookup"><span data-stu-id="b32e0-150">**\_\_Event**</span></span>](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[<span data-ttu-id="b32e0-151">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="b32e0-151">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="b32e0-152">Determinando o tipo de evento a ser recebido</span><span class="sxs-lookup"><span data-stu-id="b32e0-152">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 

