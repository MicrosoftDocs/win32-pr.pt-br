---
description: Especifica instruções sobre como os eventos de temporizador devem ser gerados para os consumidores.
ms.assetid: b08edb25-bedf-4014-a835-4050f5749479
ms.tgt_platform: multiple
title: Classe __TimerInstruction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __TimerInstruction
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5c6bbbf905a141fb7e9e3621c78709fd78999393
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297668"
---
# <a name="__timerinstruction-class"></a><span data-ttu-id="57797-103">\_\_Classe TimerInstruction</span><span class="sxs-lookup"><span data-stu-id="57797-103">\_\_TimerInstruction class</span></span>

<span data-ttu-id="57797-104">A classe de sistema abstrata **\_ \_ TimerInstruction** especifica instruções sobre como os [eventos de temporizador](receiving-a-timed-or-repeating-event.md) devem ser gerados para os consumidores.</span><span class="sxs-lookup"><span data-stu-id="57797-104">The **\_\_TimerInstruction** abstract system class specifies instructions on how [timer events](receiving-a-timed-or-repeating-event.md) should be generated for consumers.</span></span>

<span data-ttu-id="57797-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="57797-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="57797-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="57797-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="57797-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="57797-107">Syntax</span></span>

``` syntax
[abstract]
class __TimerInstruction : __EventGenerator
{
  boolean SkipIfPassed = FALSE;
  string  TimerId;
};
```

## <a name="members"></a><span data-ttu-id="57797-108">Membros</span><span class="sxs-lookup"><span data-stu-id="57797-108">Members</span></span>

<span data-ttu-id="57797-109">A classe **\_ \_ TimerInstruction** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="57797-109">The **\_\_TimerInstruction** class has these types of members:</span></span>

-   [<span data-ttu-id="57797-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="57797-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="57797-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="57797-111">Properties</span></span>

<span data-ttu-id="57797-112">A classe **\_ \_ TimerInstruction** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="57797-112">The **\_\_TimerInstruction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="57797-113">**SkipIfPassed**</span><span class="sxs-lookup"><span data-stu-id="57797-113">**SkipIfPassed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57797-114">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="57797-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="57797-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57797-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57797-116">Descreve se um evento de notificação será gerado e receberá quando um consumidor ficar disponível.</span><span class="sxs-lookup"><span data-stu-id="57797-116">Describes whether a notification event will be generated and receive when a consumer becomes available.</span></span>

<dt>

<span data-ttu-id="57797-117">FALSE</span><span class="sxs-lookup"><span data-stu-id="57797-117">FALSE</span></span>
</dt> <dd>

<span data-ttu-id="57797-118">Quando o WMI ou o consumidor se tornar disponível novamente, um evento de notificação será gerado e recebido.</span><span class="sxs-lookup"><span data-stu-id="57797-118">When WMI or the consumer becomes available again, a notification event will be generated and received.</span></span>

</dd> <dt>

<span data-ttu-id="57797-119">TRUE</span><span class="sxs-lookup"><span data-stu-id="57797-119">TRUE</span></span>
</dt> <dd>

<span data-ttu-id="57797-120">O evento de timer não ocorrerá se o WMI não estiver disponível para gerá-lo no intervalo de tempo apropriado ou se o consumidor solicitando receber o evento não estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="57797-120">The timer event does not occur if WMI is unavailable to generate it at the appropriate time interval, or the consumer requesting to receive the event is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="57797-121">**TimerId**</span><span class="sxs-lookup"><span data-stu-id="57797-121">**TimerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57797-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="57797-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57797-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57797-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57797-124">Qualificadores: [ **chave**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="57797-124">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="57797-125">Cadeia de caracteres exclusiva atribuída pelo usuário que identifica esse evento de temporizador específico.</span><span class="sxs-lookup"><span data-stu-id="57797-125">Unique user-assigned string that identifies this particular timer event.</span></span> <span data-ttu-id="57797-126">Para evitar conflitos de nomenclatura com outros identificadores de temporizador, a forma de cadeia de caracteres de um GUID do estilo de ambiente de computador distribuído (DCE) pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="57797-126">To avoid naming conflicts with other timer identifiers, the string form of a distributed computer environment (DCE)-style GUID can be used.</span></span> <span data-ttu-id="57797-127">Essa propriedade faz parte da instância de [**\_ \_ TimerEvent**](--timerevent.md) que representa o evento.</span><span class="sxs-lookup"><span data-stu-id="57797-127">This property is part of the [**\_\_TimerEvent**](--timerevent.md) instance that represents the event.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="57797-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="57797-128">Remarks</span></span>

<span data-ttu-id="57797-129">A classe **\_ \_ TimerInstruction** é derivada de [**\_ \_ EventGenerator**](--eventgenerator.md).</span><span class="sxs-lookup"><span data-stu-id="57797-129">The **\_\_TimerInstruction** class is derived from [**\_\_EventGenerator**](--eventgenerator.md).</span></span>

<span data-ttu-id="57797-130">As subclasses **\_ \_ TimerInstruction** são [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md), usadas pelos consumidores para se registrar em um evento de timer absoluto e [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md), usadas para se registrar em um evento de timer de intervalo.</span><span class="sxs-lookup"><span data-stu-id="57797-130">The **\_\_TimerInstruction** subclasses are [**\_\_AbsoluteTimerInstruction**](--absolutetimerinstruction.md), used by consumers to register for an absolute timer event, and [**\_\_IntervalTimerInstruction**](--intervaltimerinstruction.md), used to register for an interval timer event.</span></span>

## <a name="requirements"></a><span data-ttu-id="57797-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57797-131">Requirements</span></span>



| <span data-ttu-id="57797-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="57797-132">Requirement</span></span> | <span data-ttu-id="57797-133">Valor</span><span class="sxs-lookup"><span data-stu-id="57797-133">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="57797-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57797-134">Minimum supported client</span></span><br/> | <span data-ttu-id="57797-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57797-135">Windows Vista</span></span><br/>       |
| <span data-ttu-id="57797-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57797-136">Minimum supported server</span></span><br/> | <span data-ttu-id="57797-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="57797-137">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="57797-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="57797-138">Namespace</span></span><br/>                | <span data-ttu-id="57797-139">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="57797-139">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="57797-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="57797-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57797-141">**\_\_EventGenerator**</span><span class="sxs-lookup"><span data-stu-id="57797-141">**\_\_EventGenerator**</span></span>](/windows/desktop/WmiSdk/--eventgenerator)
</dt> <dt>

[<span data-ttu-id="57797-142">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="57797-142">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

