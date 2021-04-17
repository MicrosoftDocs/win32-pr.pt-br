---
description: Representa a ocorrência de algum outro evento que está sendo descartado devido à falha de um consumidor de evento.
ms.assetid: bb6a1ce9-72a2-4528-8bc8-71ac053b6b1d
ms.tgt_platform: multiple
title: Classe __ConsumerFailureEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ConsumerFailureEvent
- All
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 571785245c05d18678c10a65b192a25022fff8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791470"
---
# <a name="__consumerfailureevent-class"></a><span data-ttu-id="10ad6-103">\_\_Classe ConsumerFailureEvent</span><span class="sxs-lookup"><span data-stu-id="10ad6-103">\_\_ConsumerFailureEvent class</span></span>

<span data-ttu-id="10ad6-104">A classe de sistema **\_ \_ ConsumerFailureEvent** representa a ocorrência de algum outro evento que está sendo descartado devido à falha de um consumidor de evento.</span><span class="sxs-lookup"><span data-stu-id="10ad6-104">The **\_\_ConsumerFailureEvent** system class represents the occurrence of some other event that is being dropped because of the failure of an event consumer.</span></span>

<span data-ttu-id="10ad6-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="10ad6-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="10ad6-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="10ad6-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="10ad6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10ad6-107">Syntax</span></span>

``` syntax
class __ConsumerFailureEvent : __EventDroppedEvent
{
  uint32              ErrorCode;
  string              ErrorDescription;
  object              ErrorObject;
  object              Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="10ad6-108">Membros</span><span class="sxs-lookup"><span data-stu-id="10ad6-108">Members</span></span>

<span data-ttu-id="10ad6-109">A classe **\_ \_ ConsumerFailureEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="10ad6-109">The **\_\_ConsumerFailureEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="10ad6-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="10ad6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="10ad6-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="10ad6-111">Properties</span></span>

<span data-ttu-id="10ad6-112">A classe **\_ \_ ConsumerFailureEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="10ad6-112">The **\_\_ConsumerFailureEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="10ad6-113">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="10ad6-113">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ad6-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10ad6-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10ad6-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10ad6-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10ad6-116">Código de erro retornado pelo consumidor.</span><span class="sxs-lookup"><span data-stu-id="10ad6-116">Error code returned by the consumer.</span></span>

</dd> <dt>

<span data-ttu-id="10ad6-117">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="10ad6-117">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ad6-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="10ad6-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10ad6-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10ad6-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10ad6-120">Descrição do código de erro estendido, se disponível.</span><span class="sxs-lookup"><span data-stu-id="10ad6-120">Extended error code description, if available.</span></span>

</dd> <dt>

<span data-ttu-id="10ad6-121">**Erroobject**</span><span class="sxs-lookup"><span data-stu-id="10ad6-121">**ErrorObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ad6-122">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="10ad6-122">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="10ad6-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10ad6-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10ad6-124">Objeto com erro.</span><span class="sxs-lookup"><span data-stu-id="10ad6-124">Object in error.</span></span>

</dd> <dt>

<span data-ttu-id="10ad6-125">**Evento**</span><span class="sxs-lookup"><span data-stu-id="10ad6-125">**Event**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ad6-126">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="10ad6-126">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="10ad6-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10ad6-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10ad6-128">Evento em erro.</span><span class="sxs-lookup"><span data-stu-id="10ad6-128">Event in error.</span></span> <span data-ttu-id="10ad6-129">Essa propriedade é herdada de [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="10ad6-129">This property is inherited from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="10ad6-130">**IntendedConsumer**</span><span class="sxs-lookup"><span data-stu-id="10ad6-130">**IntendedConsumer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ad6-131">Tipo de dados: **\_ \_ EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="10ad6-131">Data type: **\_\_EventConsumer**</span></span>
</dt> <dt>

<span data-ttu-id="10ad6-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10ad6-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10ad6-133">Referência ao consumidor pretendido.</span><span class="sxs-lookup"><span data-stu-id="10ad6-133">Reference to the intended consumer.</span></span> <span data-ttu-id="10ad6-134">Essa propriedade é herdada de [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="10ad6-134">This property is inherited from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="10ad6-135">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="10ad6-135">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ad6-136">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="10ad6-136">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="10ad6-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10ad6-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10ad6-138">Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento.</span><span class="sxs-lookup"><span data-stu-id="10ad6-138">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="10ad6-139">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="10ad6-139">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="10ad6-140">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="10ad6-140">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ad6-141">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="10ad6-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="10ad6-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10ad6-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10ad6-143">Valor exclusivo que indica a hora em que o evento foi gerado.</span><span class="sxs-lookup"><span data-stu-id="10ad6-143">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="10ad6-144">Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="10ad6-144">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="10ad6-145">As informações estão no formato UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="10ad6-145">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="10ad6-146">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="10ad6-146">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="10ad6-147">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="10ad6-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10ad6-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="10ad6-148">Remarks</span></span>

<span data-ttu-id="10ad6-149">A classe **\_ \_ ConsumerFailureEvent** é derivada de [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="10ad6-149">The **\_\_ConsumerFailureEvent** class is derived from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="10ad6-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10ad6-150">Requirements</span></span>



| <span data-ttu-id="10ad6-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="10ad6-151">Requirement</span></span> | <span data-ttu-id="10ad6-152">Valor</span><span class="sxs-lookup"><span data-stu-id="10ad6-152">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="10ad6-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10ad6-153">Minimum supported client</span></span><br/> | <span data-ttu-id="10ad6-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10ad6-154">Windows Vista</span></span><br/>       |
| <span data-ttu-id="10ad6-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10ad6-155">Minimum supported server</span></span><br/> | <span data-ttu-id="10ad6-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10ad6-156">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="10ad6-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="10ad6-157">Namespace</span></span><br/>                | <span data-ttu-id="10ad6-158">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="10ad6-158">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="10ad6-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="10ad6-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10ad6-160">**\_\_EventDroppedEvent**</span><span class="sxs-lookup"><span data-stu-id="10ad6-160">**\_\_EventDroppedEvent**</span></span>](/windows/desktop/WmiSdk/--eventdroppedevent)
</dt> <dt>

[<span data-ttu-id="10ad6-161">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="10ad6-161">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

