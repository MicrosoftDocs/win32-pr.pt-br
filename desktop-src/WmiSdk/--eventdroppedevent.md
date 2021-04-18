---
description: Representa a ocorrência de um evento que é Descartado. Um evento removido é um evento que não é entregue a um consumidor de evento.
ms.assetid: fae267a9-e0ec-43fa-a3c3-d50345775a1d
ms.tgt_platform: multiple
title: Classe __EventDroppedEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventDroppedEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 4e9f68328a3c5c455c98e85a65d53156da6eeada
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763010"
---
# <a name="__eventdroppedevent-class"></a><span data-ttu-id="ebd56-104">\_\_Classe EventDroppedEvent</span><span class="sxs-lookup"><span data-stu-id="ebd56-104">\_\_EventDroppedEvent class</span></span>

<span data-ttu-id="ebd56-105">A classe de sistema **\_ \_ EventDroppedEvent** representa a ocorrência de um evento que é Descartado.</span><span class="sxs-lookup"><span data-stu-id="ebd56-105">The **\_\_EventDroppedEvent** system class represents the occurrence of an event that is dropped.</span></span> <span data-ttu-id="ebd56-106">Um evento removido é um evento que não é entregue a um consumidor de evento.</span><span class="sxs-lookup"><span data-stu-id="ebd56-106">A dropped event is an event that is not delivered to an event consumer.</span></span>

<span data-ttu-id="ebd56-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="ebd56-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ebd56-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="ebd56-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebd56-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ebd56-109">Syntax</span></span>

``` syntax
class __EventDroppedEvent : __SystemEvent
{
  __Event             Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="ebd56-110">Membros</span><span class="sxs-lookup"><span data-stu-id="ebd56-110">Members</span></span>

<span data-ttu-id="ebd56-111">A classe **\_ \_ EventDroppedEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ebd56-111">The **\_\_EventDroppedEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="ebd56-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ebd56-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ebd56-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ebd56-113">Properties</span></span>

<span data-ttu-id="ebd56-114">A classe **\_ \_ EventDroppedEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ebd56-114">The **\_\_EventDroppedEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ebd56-115">**Evento**</span><span class="sxs-lookup"><span data-stu-id="ebd56-115">**Event**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebd56-116">Tipo de dados: **\_ \_ evento**</span><span class="sxs-lookup"><span data-stu-id="ebd56-116">Data type: **\_\_Event**</span></span>
</dt> <dt>

<span data-ttu-id="ebd56-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ebd56-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ebd56-118">Evento Descartado.</span><span class="sxs-lookup"><span data-stu-id="ebd56-118">Event that is dropped.</span></span>

</dd> <dt>

<span data-ttu-id="ebd56-119">**IntendedConsumer**</span><span class="sxs-lookup"><span data-stu-id="ebd56-119">**IntendedConsumer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebd56-120">Tipo de dados: **\_ \_ EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="ebd56-120">Data type: **\_\_EventConsumer**</span></span>
</dt> <dt>

<span data-ttu-id="ebd56-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ebd56-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ebd56-122">Referência a uma instância de [**\_ \_ EventConsumer**](--eventconsumer.md) que representa o consumidor permanente que você identifica para receber um evento.</span><span class="sxs-lookup"><span data-stu-id="ebd56-122">Reference to an instance of [**\_\_EventConsumer**](--eventconsumer.md) that represents the permanent consumer you identify to receive an event.</span></span> <span data-ttu-id="ebd56-123">Diferentes consumidores permanentes que assinam um evento podem continuar a receber o evento.</span><span class="sxs-lookup"><span data-stu-id="ebd56-123">Different permanent consumers that subscribe to an event can continue to receive the event.</span></span>

</dd> <dt>

<span data-ttu-id="ebd56-124">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="ebd56-124">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebd56-125">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="ebd56-125">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="ebd56-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ebd56-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ebd56-127">Descritor que um provedor de eventos usa para determinar os usuários que podem receber um evento.</span><span class="sxs-lookup"><span data-stu-id="ebd56-127">Descriptor that an event provider uses to determine the users who can receive an event.</span></span> <span data-ttu-id="ebd56-128">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="ebd56-128">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="ebd56-129">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="ebd56-129">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebd56-130">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ebd56-130">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ebd56-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ebd56-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ebd56-132">Valor exclusivo que indica a hora em que um evento é gerado.</span><span class="sxs-lookup"><span data-stu-id="ebd56-132">Unique value that indicates the time when an event is generated.</span></span> <span data-ttu-id="ebd56-133">Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="ebd56-133">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="ebd56-134">As informações estão no formato UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="ebd56-134">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="ebd56-135">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="ebd56-135">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="ebd56-136">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="ebd56-136">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ebd56-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="ebd56-137">Remarks</span></span>

<span data-ttu-id="ebd56-138">A classe **\_ \_ EventDroppedEvent** é derivada de [**\_ \_ SystemEvent**](--systemevent.md).</span><span class="sxs-lookup"><span data-stu-id="ebd56-138">The **\_\_EventDroppedEvent** class is derived from [**\_\_SystemEvent**](--systemevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ebd56-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebd56-139">Requirements</span></span>



| <span data-ttu-id="ebd56-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebd56-140">Requirement</span></span> | <span data-ttu-id="ebd56-141">Valor</span><span class="sxs-lookup"><span data-stu-id="ebd56-141">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="ebd56-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ebd56-142">Minimum supported client</span></span><br/> | <span data-ttu-id="ebd56-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ebd56-143">Windows Vista</span></span><br/>       |
| <span data-ttu-id="ebd56-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ebd56-144">Minimum supported server</span></span><br/> | <span data-ttu-id="ebd56-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ebd56-145">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="ebd56-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="ebd56-146">Namespace</span></span><br/>                | <span data-ttu-id="ebd56-147">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="ebd56-147">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="ebd56-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="ebd56-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebd56-149">**\_\_SystemEvent**</span><span class="sxs-lookup"><span data-stu-id="ebd56-149">**\_\_SystemEvent**</span></span>](/windows/desktop/WmiSdk/--systemevent)
</dt> <dt>

[<span data-ttu-id="ebd56-150">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="ebd56-150">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

