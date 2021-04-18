---
description: Relata quando um evento é Descartado como resultado do estouro da fila de entrega.
ms.assetid: 7cb1ef3b-3b0a-4f72-96de-862022fd6db8
ms.tgt_platform: multiple
title: Classe __EventQueueOverflowEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventQueueOverflowEvent
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 058b03b8a3311aad805f47a04d20e9f1fa8c2477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788627"
---
# <a name="__eventqueueoverflowevent-class"></a><span data-ttu-id="cf8a5-103">\_\_Classe EventQueueOverflowEvent</span><span class="sxs-lookup"><span data-stu-id="cf8a5-103">\_\_EventQueueOverflowEvent class</span></span>

<span data-ttu-id="cf8a5-104">A classe de sistema **\_ \_ EventQueueOverflowEvent** relata quando um evento é Descartado como resultado do estouro da fila de entrega.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-104">The **\_\_EventQueueOverflowEvent** system class reports when an event is dropped as a result of delivery queue overflow.</span></span>

<span data-ttu-id="cf8a5-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="cf8a5-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf8a5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cf8a5-107">Syntax</span></span>

``` syntax
class __EventQueueOverflowEvent : __EventDroppedEvent
{
  uint32              CurrentQueueSize;
  object              Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="cf8a5-108">Membros</span><span class="sxs-lookup"><span data-stu-id="cf8a5-108">Members</span></span>

<span data-ttu-id="cf8a5-109">A classe **\_ \_ EventQueueOverflowEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="cf8a5-109">The **\_\_EventQueueOverflowEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="cf8a5-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cf8a5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cf8a5-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cf8a5-111">Properties</span></span>

<span data-ttu-id="cf8a5-112">A classe **\_ \_ EventQueueOverflowEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-112">The **\_\_EventQueueOverflowEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cf8a5-113">**CurrentQueueSize**</span><span class="sxs-lookup"><span data-stu-id="cf8a5-113">**CurrentQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8a5-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cf8a5-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cf8a5-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf8a5-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8a5-116">Tamanho da fila atual, em bytes.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-116">Current queue size, in bytes.</span></span> <span data-ttu-id="cf8a5-117">Essa propriedade usa como padrão 10 MB para todas as filas combinadas.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-117">This property defaults to 10 MB for all queues combined.</span></span>

</dd> <dt>

<span data-ttu-id="cf8a5-118">**Evento**</span><span class="sxs-lookup"><span data-stu-id="cf8a5-118">**Event**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8a5-119">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="cf8a5-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="cf8a5-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf8a5-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8a5-121">Evento de interesse.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-121">Event of interest.</span></span> <span data-ttu-id="cf8a5-122">Essa propriedade é herdada de [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="cf8a5-122">This property is inherited from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf8a5-123">**IntendedConsumer**</span><span class="sxs-lookup"><span data-stu-id="cf8a5-123">**IntendedConsumer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8a5-124">Tipo de dados: **\_ \_ EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="cf8a5-124">Data type: **\_\_EventConsumer**</span></span>
</dt> <dt>

<span data-ttu-id="cf8a5-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf8a5-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8a5-126">Referência ao consumidor pretendido.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-126">Reference to the intended consumer.</span></span> <span data-ttu-id="cf8a5-127">Essa propriedade é herdada de [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="cf8a5-127">This property is inherited from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf8a5-128">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="cf8a5-128">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8a5-129">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="cf8a5-129">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="cf8a5-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf8a5-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8a5-131">Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-131">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="cf8a5-132">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="cf8a5-132">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf8a5-133">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="cf8a5-133">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8a5-134">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cf8a5-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cf8a5-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf8a5-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8a5-136">Valor exclusivo que indica a hora em que o evento foi gerado.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-136">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="cf8a5-137">Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-137">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="cf8a5-138">As informações estão no formato UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="cf8a5-138">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="cf8a5-139">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="cf8a5-139">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="cf8a5-140">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="cf8a5-140">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf8a5-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf8a5-141">Remarks</span></span>

<span data-ttu-id="cf8a5-142">Somente os usuários com privilégios de administrador podem receber esse evento.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-142">Only users with administrator privileges are able to receive this event.</span></span> <span data-ttu-id="cf8a5-143">A classe **\_ \_ EventQueueOverflowEvent** é derivada de [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="cf8a5-143">The **\_\_EventQueueOverflowEvent** class is derived from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

<span data-ttu-id="cf8a5-144">Para obter mais informações, consulte a propriedade [**MaximumQueueSize**](--eventconsumer.md) na classe [**\_ \_ EventConsumer**](--eventconsumer.md) e a propriedade [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) na classe **Win32 \_ WMISetting** .</span><span class="sxs-lookup"><span data-stu-id="cf8a5-144">For more information, see the [**MaximumQueueSize**](--eventconsumer.md) property in the [**\_\_EventConsumer**](--eventconsumer.md) class and the [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) property in the **Win32\_WMISetting** class.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf8a5-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf8a5-145">Requirements</span></span>



| <span data-ttu-id="cf8a5-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf8a5-146">Requirement</span></span> | <span data-ttu-id="cf8a5-147">Valor</span><span class="sxs-lookup"><span data-stu-id="cf8a5-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="cf8a5-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf8a5-148">Minimum supported client</span></span><br/> | <span data-ttu-id="cf8a5-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cf8a5-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="cf8a5-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf8a5-150">Minimum supported server</span></span><br/> | <span data-ttu-id="cf8a5-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf8a5-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="cf8a5-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="cf8a5-152">Namespace</span></span><br/>                | <span data-ttu-id="cf8a5-153">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="cf8a5-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="cf8a5-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf8a5-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf8a5-155">**\_\_EventDroppedEvent**</span><span class="sxs-lookup"><span data-stu-id="cf8a5-155">**\_\_EventDroppedEvent**</span></span>](/windows/desktop/WmiSdk/--eventdroppedevent)
</dt> <dt>

[<span data-ttu-id="cf8a5-156">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="cf8a5-156">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

