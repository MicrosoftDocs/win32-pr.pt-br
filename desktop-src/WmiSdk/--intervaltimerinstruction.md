---
description: Gera eventos em intervalos, semelhantes a uma \_ mensagem de temporizador do WM na programação do Windows.
ms.assetid: 0895a743-a0dd-4833-a2bf-0196369e18b9
ms.tgt_platform: multiple
title: Classe __IntervalTimerInstruction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __IntervalTimerInstruction
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 20dd1c9fb2d009de4d8d957b4d5980cc6d6ff45e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797948"
---
# <a name="__intervaltimerinstruction-class"></a><span data-ttu-id="4ca1b-103">\_\_Classe IntervalTimerInstruction</span><span class="sxs-lookup"><span data-stu-id="4ca1b-103">\_\_IntervalTimerInstruction class</span></span>

<span data-ttu-id="4ca1b-104">A classe de sistema **\_ \_ IntervalTimerInstruction** gera eventos em intervalos, semelhante a uma \_ mensagem de temporizador do WM na programação do Windows.</span><span class="sxs-lookup"><span data-stu-id="4ca1b-104">The **\_\_IntervalTimerInstruction** system class generates events at intervals, similar to a WM\_TIMER message in Windows programming.</span></span> <span data-ttu-id="4ca1b-105">Um consumidor de eventos registra-se para receber eventos de temporizador de intervalo criando uma consulta de evento que faz referência a essa classe.</span><span class="sxs-lookup"><span data-stu-id="4ca1b-105">An event consumer registers to receive interval timer events by creating an event query that references this class.</span></span> <span data-ttu-id="4ca1b-106">Devido ao comportamento do sistema operacional, não há nenhuma garantia de que os eventos serão entregues exatamente no intervalo solicitado.</span><span class="sxs-lookup"><span data-stu-id="4ca1b-106">Due to operating system behavior, there are no guarantees that events will be delivered at precisely the requested interval.</span></span>

<span data-ttu-id="4ca1b-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="4ca1b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4ca1b-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="4ca1b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ca1b-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ca1b-109">Syntax</span></span>

``` syntax
class __IntervalTimerInstruction : __TimerInstruction
{
  uint32  IntervalBetweenEvents;
  boolean SkipIfPassed = FALSE;
  string  TimerId;
};
```

## <a name="members"></a><span data-ttu-id="4ca1b-110">Membros</span><span class="sxs-lookup"><span data-stu-id="4ca1b-110">Members</span></span>

<span data-ttu-id="4ca1b-111">A classe **\_ \_ IntervalTimerInstruction** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4ca1b-111">The **\_\_IntervalTimerInstruction** class has these types of members:</span></span>

-   [<span data-ttu-id="4ca1b-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4ca1b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4ca1b-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4ca1b-113">Properties</span></span>

<span data-ttu-id="4ca1b-114">A classe **\_ \_ IntervalTimerInstruction** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4ca1b-114">The **\_\_IntervalTimerInstruction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4ca1b-115">**IntervalBetweenEvents**</span><span class="sxs-lookup"><span data-stu-id="4ca1b-115">**IntervalBetweenEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ca1b-116">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4ca1b-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ca1b-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4ca1b-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ca1b-118">Qualificadores: [**unidades**](standard-qualifiers.md) (milissegundos)</span><span class="sxs-lookup"><span data-stu-id="4ca1b-118">Qualifiers: [**Units**](standard-qualifiers.md) (milliseconds)</span></span>
</dt> </dl>

<span data-ttu-id="4ca1b-119">Número de milissegundos entre acionamentos de evento.</span><span class="sxs-lookup"><span data-stu-id="4ca1b-119">Number of milliseconds between event firings.</span></span>

</dd> <dt>

<span data-ttu-id="4ca1b-120">**SkipIfPassed**</span><span class="sxs-lookup"><span data-stu-id="4ca1b-120">**SkipIfPassed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ca1b-121">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="4ca1b-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4ca1b-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4ca1b-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ca1b-123">Se **for true**, esse evento será ignorado se o intervalo já for passado.</span><span class="sxs-lookup"><span data-stu-id="4ca1b-123">If **TRUE**, this event is to be skipped if the interval is already passed.</span></span> <span data-ttu-id="4ca1b-124">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="4ca1b-124">The default is **FALSE**.</span></span> <span data-ttu-id="4ca1b-125">Essa propriedade é herdada de [**\_ \_ TimerInstruction**](--timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="4ca1b-125">This property is inherited from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

<dt>

<span data-ttu-id="4ca1b-126">FALSE</span><span class="sxs-lookup"><span data-stu-id="4ca1b-126">FALSE</span></span>
</dt> <dd>

<span data-ttu-id="4ca1b-127">Quando o WMI ou o consumidor se tornar disponível novamente, um evento de notificação será gerado e recebido.</span><span class="sxs-lookup"><span data-stu-id="4ca1b-127">When WMI or the consumer becomes available again, a notification event will be generated and received.</span></span>

</dd> <dt>

<span data-ttu-id="4ca1b-128">TRUE</span><span class="sxs-lookup"><span data-stu-id="4ca1b-128">TRUE</span></span>
</dt> <dd>

<span data-ttu-id="4ca1b-129">O evento de timer não ocorrerá se o WMI não estiver disponível para gerá-lo no intervalo de tempo apropriado ou se o consumidor solicitando receber o evento não estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="4ca1b-129">The timer event does not occur if WMI is unavailable to generate it at the appropriate time interval, or the consumer requesting to receive the event is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4ca1b-130">**TimerId**</span><span class="sxs-lookup"><span data-stu-id="4ca1b-130">**TimerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ca1b-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4ca1b-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ca1b-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4ca1b-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ca1b-133">Qualificadores: [ **chave**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="4ca1b-133">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="4ca1b-134">Identificador exclusivo deste objeto **\_ \_ IntervalTimerInstruction** .</span><span class="sxs-lookup"><span data-stu-id="4ca1b-134">Unique identifier for this **\_\_IntervalTimerInstruction** object.</span></span> <span data-ttu-id="4ca1b-135">Essa propriedade é herdada de [**\_ \_ TimerInstruction**](--timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="4ca1b-135">This property is inherited from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ca1b-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ca1b-136">Remarks</span></span>

<span data-ttu-id="4ca1b-137">A classe **\_ \_ IntervalTimerInstruction** é derivada de [**\_ \_ TimerInstruction**](--timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="4ca1b-137">The **\_\_IntervalTimerInstruction** class is derived from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

<span data-ttu-id="4ca1b-138">A consulta de evento inserida para se registrar em um evento de timer de intervalo geralmente é baseada na propriedade **timerId** .</span><span class="sxs-lookup"><span data-stu-id="4ca1b-138">The event query entered to register for an interval timer event is usually based on the **TimerId** property.</span></span> <span data-ttu-id="4ca1b-139">Eventos de notificação gerados a partir de um evento de temporizador de intervalo contêm a propriedade **NumFirings** que contém dados que refletem quantos eventos foram acionados durante o tempo em que os eventos não puderam ser recebidos.</span><span class="sxs-lookup"><span data-stu-id="4ca1b-139">Notification events generated from an interval timer event contain the property **NumFirings** which contains data reflecting how many events fired during the time the events were unable to be received.</span></span> <span data-ttu-id="4ca1b-140">Se **SkipIfPassed** for definido como **true**, essas informações serão descartadas.</span><span class="sxs-lookup"><span data-stu-id="4ca1b-140">If **SkipIfPassed** is set to **TRUE**, that information is discarded.</span></span>

<span data-ttu-id="4ca1b-141">O valor da propriedade **IntervalBetweenEvents** deve ser razoavelmente grande.</span><span class="sxs-lookup"><span data-stu-id="4ca1b-141">The value for the **IntervalBetweenEvents** property should be reasonably large.</span></span> <span data-ttu-id="4ca1b-142">Se for muito pequeno, o WMI poderá ignorá-lo e não gerar o evento devido a limitações em alguns sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="4ca1b-142">If it is too small, WMI may ignore it and not generate the event due to limitations in some operating systems.</span></span>

<span data-ttu-id="4ca1b-143">O WMI gera o evento de timer de intervalo criando uma instância da classe [**\_ \_ TimerEvent**](--timerevent.md) .</span><span class="sxs-lookup"><span data-stu-id="4ca1b-143">WMI generates the interval timer event by creating an instance of the [**\_\_TimerEvent**](--timerevent.md) class.</span></span>

<span data-ttu-id="4ca1b-144">Para receber esses eventos de timer em um consumidor de evento temporário, execute [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) com a seguinte cadeia de caracteres de consulta de evento:</span><span class="sxs-lookup"><span data-stu-id="4ca1b-144">To receive these timer events in a temporary event consumer, execute [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) with the following event query string:</span></span>


```sql
SELECT * FROM __TimerEvent WHERE TimerID = "MyEvent"
```



<span data-ttu-id="4ca1b-145">Para receber esses eventos de temporizador em um consumidor de evento permanente, você deve carregar a consulta anterior em um filtro de evento, definir um consumidor lógico e criar uma associação de filtro para consumidor para o filtro e o consumidor.</span><span class="sxs-lookup"><span data-stu-id="4ca1b-145">To receive these timer events in a permanent event consumer, you must load the previous query into an event filter, define a logical consumer, and create a filter-to-consumer binding for the filter and consumer.</span></span> <span data-ttu-id="4ca1b-146">Para obter mais informações, consulte [recebendo eventos em todos os momentos](receiving-events-at-all-times.md).</span><span class="sxs-lookup"><span data-stu-id="4ca1b-146">For more information, see [Receiving Events at All Times](receiving-events-at-all-times.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4ca1b-147">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4ca1b-147">Examples</span></span>

<span data-ttu-id="4ca1b-148">A declaração MOF a seguir mostra como gerar um evento de timer de intervalo com a propriedade de chave definida como "MyEvent" a cada 10 segundos:</span><span class="sxs-lookup"><span data-stu-id="4ca1b-148">The following MOF declaration shows how to generate an interval timer event with the key property set to "MyEvent" every 10 seconds:</span></span>


```mof
instance of __IntervalTimerInstruction
{
  TimerId = "MyEvent";     // inherited from __TimerInstruction
  SkipIfPassed = FALSE;    // also inherited
  IntervalBetweenEvents = 10000;
};
```



## <a name="requirements"></a><span data-ttu-id="4ca1b-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ca1b-149">Requirements</span></span>



| <span data-ttu-id="4ca1b-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ca1b-150">Requirement</span></span> | <span data-ttu-id="4ca1b-151">Valor</span><span class="sxs-lookup"><span data-stu-id="4ca1b-151">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="4ca1b-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ca1b-152">Minimum supported client</span></span><br/> | <span data-ttu-id="4ca1b-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4ca1b-153">Windows Vista</span></span><br/>       |
| <span data-ttu-id="4ca1b-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ca1b-154">Minimum supported server</span></span><br/> | <span data-ttu-id="4ca1b-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ca1b-155">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="4ca1b-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="4ca1b-156">Namespace</span></span><br/>                | <span data-ttu-id="4ca1b-157">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="4ca1b-157">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="4ca1b-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ca1b-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ca1b-159">**\_\_TimerInstruction**</span><span class="sxs-lookup"><span data-stu-id="4ca1b-159">**\_\_TimerInstruction**</span></span>](/windows/desktop/WmiSdk/--timerinstruction)
</dt> <dt>

[<span data-ttu-id="4ca1b-160">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="4ca1b-160">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="4ca1b-161">Recebendo eventos cronometrados ou repetidos</span><span class="sxs-lookup"><span data-stu-id="4ca1b-161">Receiving Timed or Repeating Events</span></span>](receiving-a-timed-or-repeating-event.md)
</dt> </dl>

 

