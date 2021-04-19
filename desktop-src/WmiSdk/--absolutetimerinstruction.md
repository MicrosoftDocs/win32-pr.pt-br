---
description: Faz com que um evento seja gerado em uma data específica em um momento específico.
ms.assetid: bcb64c81-3b40-4665-a880-a100629656e0
ms.tgt_platform: multiple
title: Classe __AbsoluteTimerInstruction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __AbsoluteTimerInstruction
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5f4f55e635e42ec34e9b3558a0784d319e4d91ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807182"
---
# <a name="__absolutetimerinstruction-class"></a><span data-ttu-id="259a1-103">\_\_Classe AbsoluteTimerInstruction</span><span class="sxs-lookup"><span data-stu-id="259a1-103">\_\_AbsoluteTimerInstruction class</span></span>

<span data-ttu-id="259a1-104">A classe de sistema **\_ \_ AbsoluteTimerInstruction** faz com que um evento seja gerado em uma data específica em um momento específico.</span><span class="sxs-lookup"><span data-stu-id="259a1-104">The **\_\_AbsoluteTimerInstruction** system class causes an event to be generated on a specific date at a specific time.</span></span> <span data-ttu-id="259a1-105">Um consumidor de eventos registra-se para receber um evento de timer absoluto criando uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="259a1-105">An event consumer registers to receive an absolute timer event by creating an instance of this class.</span></span> <span data-ttu-id="259a1-106">O evento é gerado uma vez.</span><span class="sxs-lookup"><span data-stu-id="259a1-106">The event is generated one time.</span></span>

<span data-ttu-id="259a1-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="259a1-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="259a1-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="259a1-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="259a1-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="259a1-109">Syntax</span></span>

``` syntax
class __AbsoluteTimerInstruction : __TimerInstruction
{
  datetime EventDateTime;
  boolean  SkipIfPassed = FALSE;
  string   TimerId;
};
```

## <a name="members"></a><span data-ttu-id="259a1-110">Membros</span><span class="sxs-lookup"><span data-stu-id="259a1-110">Members</span></span>

<span data-ttu-id="259a1-111">A classe **\_ \_ AbsoluteTimerInstruction** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="259a1-111">The **\_\_AbsoluteTimerInstruction** class has these types of members:</span></span>

-   [<span data-ttu-id="259a1-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="259a1-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="259a1-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="259a1-113">Properties</span></span>

<span data-ttu-id="259a1-114">A classe **\_ \_ AbsoluteTimerInstruction** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="259a1-114">The **\_\_AbsoluteTimerInstruction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="259a1-115">**EventDateTime**</span><span class="sxs-lookup"><span data-stu-id="259a1-115">**EventDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="259a1-116">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="259a1-116">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="259a1-117">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="259a1-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="259a1-118">Cadeia de caracteres de comprimento fixo no [formato DMTF](date-and-time-format.md) que especifica quando o temporizador é acionado.</span><span class="sxs-lookup"><span data-stu-id="259a1-118">Fixed-length string in [DMTF format](date-and-time-format.md) that specifies when the timer fires.</span></span>

</dd> <dt>

<span data-ttu-id="259a1-119">**SkipIfPassed**</span><span class="sxs-lookup"><span data-stu-id="259a1-119">**SkipIfPassed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="259a1-120">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="259a1-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="259a1-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="259a1-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="259a1-122">Se **for true**, o evento timer ocorrerá se o WMI não puder gerá-lo no intervalo de tempo correto ou se o consumidor solicitando receber o evento não estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="259a1-122">If **TRUE**, the timer event occurs if WMI cannot generate it at the correct time interval, or the consumer requesting to receive the event is unavailable.</span></span> <span data-ttu-id="259a1-123">Se **for true**, o evento não ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="259a1-123">If **TRUE**, the event will not occur.</span></span> <span data-ttu-id="259a1-124">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="259a1-124">The default is **FALSE**.</span></span> <span data-ttu-id="259a1-125">Quando o WMI ou o consumidor se torna disponível, um evento de notificação é gerado e recebido.</span><span class="sxs-lookup"><span data-stu-id="259a1-125">When WMI or the consumer becomes available, a notification event is generated and received.</span></span> <span data-ttu-id="259a1-126">Essa propriedade é herdada de [**\_ \_ TimerInstruction**](--timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="259a1-126">This property is inherited from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

<dt>

<span data-ttu-id="259a1-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="259a1-127">FALSE</span></span>
</dt> <dd>

<span data-ttu-id="259a1-128">Quando o WMI ou o consumidor se tornar disponível novamente, um evento de notificação será gerado e recebido.</span><span class="sxs-lookup"><span data-stu-id="259a1-128">When WMI or the consumer becomes available again, a notification event will be generated and received.</span></span>

</dd> <dt>

<span data-ttu-id="259a1-129">TRUE</span><span class="sxs-lookup"><span data-stu-id="259a1-129">TRUE</span></span>
</dt> <dd>

<span data-ttu-id="259a1-130">O evento de timer não ocorrerá se o WMI não estiver disponível para gerá-lo no intervalo de tempo apropriado ou se o consumidor solicitando receber o evento não estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="259a1-130">The timer event does not occur if WMI is unavailable to generate it at the appropriate time interval, or the consumer requesting to receive the event is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="259a1-131">**TimerId**</span><span class="sxs-lookup"><span data-stu-id="259a1-131">**TimerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="259a1-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="259a1-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="259a1-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="259a1-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="259a1-134">Qualificadores: [ **chave**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="259a1-134">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="259a1-135">Cadeia de caracteres exclusiva atribuída pelo usuário que identifica um evento de temporizador específico.</span><span class="sxs-lookup"><span data-stu-id="259a1-135">Unique user-assigned string that identifies a specific timer event.</span></span> <span data-ttu-id="259a1-136">Para evitar conflitos de nomenclatura com outros identificadores de temporizador, a forma de cadeia de caracteres de um GUID de estilo de ambiente de computador distribuído pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="259a1-136">To avoid naming conflicts with other timer identifiers, the string form of a distributed computer environment style GUID can be used.</span></span> <span data-ttu-id="259a1-137">Essa propriedade é herdada de [**\_ \_ TimerInstruction**](--timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="259a1-137">This property is inherited from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="259a1-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="259a1-138">Remarks</span></span>

<span data-ttu-id="259a1-139">A classe **\_ \_ AbsoluteTimerInstruction** é derivada de [**\_ \_ TimerInstruction**](--timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="259a1-139">The **\_\_AbsoluteTimerInstruction** class is derived from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

<span data-ttu-id="259a1-140">O WMI gera o evento de timer absoluto criando uma instância da classe [**\_ \_ TimerEvent**](--timerevent.md) .</span><span class="sxs-lookup"><span data-stu-id="259a1-140">WMI generates the absolute timer event by creating an instance of the [**\_\_TimerEvent**](--timerevent.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="259a1-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="259a1-141">Requirements</span></span>



| <span data-ttu-id="259a1-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="259a1-142">Requirement</span></span> | <span data-ttu-id="259a1-143">Valor</span><span class="sxs-lookup"><span data-stu-id="259a1-143">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="259a1-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="259a1-144">Minimum supported client</span></span><br/> | <span data-ttu-id="259a1-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="259a1-145">Windows Vista</span></span><br/>       |
| <span data-ttu-id="259a1-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="259a1-146">Minimum supported server</span></span><br/> | <span data-ttu-id="259a1-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="259a1-147">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="259a1-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="259a1-148">Namespace</span></span><br/>                | <span data-ttu-id="259a1-149">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="259a1-149">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="259a1-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="259a1-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="259a1-151">**\_\_TimerInstruction**</span><span class="sxs-lookup"><span data-stu-id="259a1-151">**\_\_TimerInstruction**</span></span>](/windows/desktop/WmiSdk/--timerinstruction)
</dt> <dt>

[<span data-ttu-id="259a1-152">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="259a1-152">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="259a1-153">Recebendo eventos cronometrados ou repetidos</span><span class="sxs-lookup"><span data-stu-id="259a1-153">Receiving Timed or Repeating Events</span></span>](receiving-a-timed-or-repeating-event.md)
</dt> <dt>

[<span data-ttu-id="259a1-154">Recebendo eventos em todos os momentos</span><span class="sxs-lookup"><span data-stu-id="259a1-154">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="259a1-155">Recebendo eventos para a duração do seu aplicativo</span><span class="sxs-lookup"><span data-stu-id="259a1-155">Receiving Events for the Duration of Your Application</span></span>](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

