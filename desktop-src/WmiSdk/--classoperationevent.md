---
description: É uma classe base para todos os eventos intrínsecos relacionados a uma classe.
ms.assetid: 554bbabd-2639-40f5-8786-6df2188db0ec
ms.tgt_platform: multiple
title: Classe __ClassOperationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 0c7a78219cec5c014e289dad4bf1cc29f0466a06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782673"
---
# <a name="__classoperationevent-class"></a><span data-ttu-id="13997-103">\_\_Classe ClassOperationEvent</span><span class="sxs-lookup"><span data-stu-id="13997-103">\_\_ClassOperationEvent class</span></span>

<span data-ttu-id="13997-104">A classe de sistema **\_ \_ ClassOperationEvent** é uma classe base para todos os eventos intrínsecos relacionados a uma classe.</span><span class="sxs-lookup"><span data-stu-id="13997-104">The **\_\_ClassOperationEvent** system class is a base class for all intrinsic events that relate to a class.</span></span>

<span data-ttu-id="13997-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="13997-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="13997-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="13997-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="13997-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="13997-107">Syntax</span></span>

``` syntax
class __ClassOperationEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="13997-108">Membros</span><span class="sxs-lookup"><span data-stu-id="13997-108">Members</span></span>

<span data-ttu-id="13997-109">A classe **\_ \_ ClassOperationEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="13997-109">The **\_\_ClassOperationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="13997-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="13997-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="13997-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="13997-111">Properties</span></span>

<span data-ttu-id="13997-112">A classe **\_ \_ ClassOperationEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="13997-112">The **\_\_ClassOperationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="13997-113">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="13997-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13997-114">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="13997-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="13997-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13997-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13997-116">Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento.</span><span class="sxs-lookup"><span data-stu-id="13997-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="13997-117">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="13997-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="13997-118">**TargetClass**</span><span class="sxs-lookup"><span data-stu-id="13997-118">**TargetClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13997-119">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="13997-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="13997-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13997-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13997-121">Classe afetada pelo evento.</span><span class="sxs-lookup"><span data-stu-id="13997-121">Class affected by the event.</span></span> <span data-ttu-id="13997-122">Para eventos de criação, essa é a classe recém-criada.</span><span class="sxs-lookup"><span data-stu-id="13997-122">For creation events, this is the newly created class.</span></span> <span data-ttu-id="13997-123">Para eventos de modificação, esta é a nova versão da classe alterada.</span><span class="sxs-lookup"><span data-stu-id="13997-123">For modification events, this is the new version of the changed class.</span></span> <span data-ttu-id="13997-124">Para eventos de exclusão, essa é a classe excluída.</span><span class="sxs-lookup"><span data-stu-id="13997-124">For deletion events, this is the deleted class.</span></span>

</dd> <dt>

<span data-ttu-id="13997-125">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="13997-125">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13997-126">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="13997-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="13997-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13997-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13997-128">Valor exclusivo que indica a hora em que o evento foi gerado.</span><span class="sxs-lookup"><span data-stu-id="13997-128">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="13997-129">Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="13997-129">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="13997-130">As informações estão no formato UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="13997-130">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="13997-131">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="13997-131">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="13997-132">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="13997-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="13997-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="13997-133">Remarks</span></span>

<span data-ttu-id="13997-134">A classe **\_ \_ ClassOperationEvent** é derivada de [**\_ \_ Event**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="13997-134">The **\_\_ClassOperationEvent** class is derived from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="13997-135">As instâncias de **\_ \_ ClassOperationEvent** não são criadas; apenas instâncias de suas subclasses são criadas.</span><span class="sxs-lookup"><span data-stu-id="13997-135">Instances of **\_\_ClassOperationEvent** are not created; only instances of its subclasses are created.</span></span> <span data-ttu-id="13997-136">As classes a seguir derivam de **\_ \_ ClassOperationEvent**:</span><span class="sxs-lookup"><span data-stu-id="13997-136">The following classes derive from **\_\_ClassOperationEvent**:</span></span>

[<span data-ttu-id="13997-137">**\_\_ClassCreationEvent**</span><span class="sxs-lookup"><span data-stu-id="13997-137">**\_\_ClassCreationEvent**</span></span>](--classcreationevent.md)

[<span data-ttu-id="13997-138">**\_\_ClassModificationEvent**</span><span class="sxs-lookup"><span data-stu-id="13997-138">**\_\_ClassModificationEvent**</span></span>](--classmodificationevent.md)

[<span data-ttu-id="13997-139">**\_\_ClassDeletionEvent**</span><span class="sxs-lookup"><span data-stu-id="13997-139">**\_\_ClassDeletionEvent**</span></span>](--classdeletionevent.md)

## <a name="requirements"></a><span data-ttu-id="13997-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13997-140">Requirements</span></span>



| <span data-ttu-id="13997-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="13997-141">Requirement</span></span> | <span data-ttu-id="13997-142">Valor</span><span class="sxs-lookup"><span data-stu-id="13997-142">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="13997-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13997-143">Minimum supported client</span></span><br/> | <span data-ttu-id="13997-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13997-144">Windows Vista</span></span><br/>       |
| <span data-ttu-id="13997-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13997-145">Minimum supported server</span></span><br/> | <span data-ttu-id="13997-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13997-146">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="13997-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="13997-147">Namespace</span></span><br/>                | <span data-ttu-id="13997-148">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="13997-148">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="13997-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="13997-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13997-150">**\_\_Evento**</span><span class="sxs-lookup"><span data-stu-id="13997-150">**\_\_Event**</span></span>](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[<span data-ttu-id="13997-151">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="13997-151">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="13997-152">Determinando o tipo de evento a ser recebido</span><span class="sxs-lookup"><span data-stu-id="13997-152">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 

