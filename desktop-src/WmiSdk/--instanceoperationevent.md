---
description: Serve como uma classe base para todos os eventos intrínsecos relacionados a uma instância.
ms.assetid: f6d2b6e5-0dca-4cb5-95a5-33b45cd76807
ms.tgt_platform: multiple
title: Classe __InstanceOperationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 1d3111b74c876cc7ffedb959eca7f46812ed92e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807876"
---
# <a name="__instanceoperationevent-class"></a><span data-ttu-id="d52f5-103">\_\_Classe InstanceOperationEvent</span><span class="sxs-lookup"><span data-stu-id="d52f5-103">\_\_InstanceOperationEvent class</span></span>

<span data-ttu-id="d52f5-104">A classe de sistema **\_ \_ InstanceOperationEvent** serve como uma classe base para todos os eventos intrínsecos relacionados a uma instância.</span><span class="sxs-lookup"><span data-stu-id="d52f5-104">The **\_\_InstanceOperationEvent** system class serves as a base class for all intrinsic events that relate to an instance.</span></span>

<span data-ttu-id="d52f5-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d52f5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d52f5-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="d52f5-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d52f5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d52f5-107">Syntax</span></span>

``` syntax
class __InstanceOperationEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="d52f5-108">Membros</span><span class="sxs-lookup"><span data-stu-id="d52f5-108">Members</span></span>

<span data-ttu-id="d52f5-109">A classe **\_ \_ InstanceOperationEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d52f5-109">The **\_\_InstanceOperationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="d52f5-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d52f5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d52f5-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d52f5-111">Properties</span></span>

<span data-ttu-id="d52f5-112">A classe **\_ \_ InstanceOperationEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d52f5-112">The **\_\_InstanceOperationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d52f5-113">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="d52f5-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d52f5-114">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="d52f5-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="d52f5-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d52f5-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d52f5-116">Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento.</span><span class="sxs-lookup"><span data-stu-id="d52f5-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="d52f5-117">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="d52f5-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="d52f5-118">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="d52f5-118">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d52f5-119">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="d52f5-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="d52f5-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d52f5-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d52f5-121">Instância afetada pelo evento.</span><span class="sxs-lookup"><span data-stu-id="d52f5-121">Instance affected by the event.</span></span> <span data-ttu-id="d52f5-122">Para eventos de criação, essa é a instância recém-criada.</span><span class="sxs-lookup"><span data-stu-id="d52f5-122">For creation events, this is the newly created instance.</span></span> <span data-ttu-id="d52f5-123">Para eventos de modificação, esta é a nova versão da instância alterada.</span><span class="sxs-lookup"><span data-stu-id="d52f5-123">For modification events, this is the new version of the changed instance.</span></span> <span data-ttu-id="d52f5-124">Para eventos de exclusão, essa é a instância excluída.</span><span class="sxs-lookup"><span data-stu-id="d52f5-124">For deletion events, this is the deleted instance.</span></span>

</dd> <dt>

<span data-ttu-id="d52f5-125">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="d52f5-125">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d52f5-126">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d52f5-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d52f5-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d52f5-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d52f5-128">Valor exclusivo que indica a hora em que o evento foi gerado.</span><span class="sxs-lookup"><span data-stu-id="d52f5-128">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="d52f5-129">Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="d52f5-129">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="d52f5-130">As informações estão no formato UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="d52f5-130">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="d52f5-131">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="d52f5-131">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="d52f5-132">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d52f5-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d52f5-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="d52f5-133">Remarks</span></span>

<span data-ttu-id="d52f5-134">A classe **\_ \_ InstanceOperationEvent** é derivada de [**\_ \_ Event**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="d52f5-134">The **\_\_InstanceOperationEvent** class is derived from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="d52f5-135">As instâncias de **\_ \_ InstanceOperationEvent** não são criadas; apenas instâncias de suas subclasses são criadas.</span><span class="sxs-lookup"><span data-stu-id="d52f5-135">Instances of **\_\_InstanceOperationEvent** are not created; only instances of its subclasses are created.</span></span> <span data-ttu-id="d52f5-136">As classes a seguir derivam de **\_ \_ InstanceOperationEvent**:</span><span class="sxs-lookup"><span data-stu-id="d52f5-136">The following classes derive from **\_\_InstanceOperationEvent**:</span></span>

[<span data-ttu-id="d52f5-137">**\_\_InstanceCreationEvent**</span><span class="sxs-lookup"><span data-stu-id="d52f5-137">**\_\_InstanceCreationEvent**</span></span>](--instancecreationevent.md)

[<span data-ttu-id="d52f5-138">**\_\_InstanceModificationEvent**</span><span class="sxs-lookup"><span data-stu-id="d52f5-138">**\_\_InstanceModificationEvent**</span></span>](--instancemodificationevent.md)

[<span data-ttu-id="d52f5-139">**\_\_InstanceDeletionEvent**</span><span class="sxs-lookup"><span data-stu-id="d52f5-139">**\_\_InstanceDeletionEvent**</span></span>](--instancedeletionevent.md)

<span data-ttu-id="d52f5-140">**Visão geral**</span><span class="sxs-lookup"><span data-stu-id="d52f5-140">**Overview**</span></span>

<span data-ttu-id="d52f5-141">Assim como há uma classe WMI que representa cada tipo de recurso do sistema que pode ser gerenciado usando o WMI, há uma classe WMI que representa cada tipo de evento WMI.</span><span class="sxs-lookup"><span data-stu-id="d52f5-141">Just as there is a WMI class that represents each type of system resource that can be managed using WMI, there is a WMI class that represents each type of WMI event.</span></span> <span data-ttu-id="d52f5-142">Quando ocorre um evento que pode ser monitorado pelo WMI, uma instância da classe de evento WMI correspondente é criada.</span><span class="sxs-lookup"><span data-stu-id="d52f5-142">When an event that can be monitored by WMI occurs, an instance of the corresponding WMI event class is created.</span></span> <span data-ttu-id="d52f5-143">Um evento WMI ocorre quando essa instância é criada.</span><span class="sxs-lookup"><span data-stu-id="d52f5-143">A WMI event occurs when that instance is created.</span></span>

<span data-ttu-id="d52f5-144">Há três tipos principais de classes de evento WMI, todas derivadas da classe WMI de [**\_ \_ evento**](--event.md) : eventos intrínsecos, eventos extrínsecos e eventos de temporizador.</span><span class="sxs-lookup"><span data-stu-id="d52f5-144">There are three major types of WMI event classes, all of which are derived from the [**\_\_Event**](--event.md) WMI class: Intrinsic Events, Extrinsic Events, and Timer Events.</span></span> <span data-ttu-id="d52f5-145">Os eventos intrínsecos, por sua vez, são representados por três classes distintas derivadas da classe de **\_ \_ evento** : [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md), **\_ \_ InstanceOperationEvent** e [**\_ \_ ClassOperationEvent**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="d52f5-145">Intrinsic Events, in turn, are represented by three distinct classes derived from the **\_\_Event** class: [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md), **\_\_InstanceOperationEvent**, and [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

<span data-ttu-id="d52f5-146">Eventos intrínsecos</span><span class="sxs-lookup"><span data-stu-id="d52f5-146">Intrinsic Events</span></span>

<span data-ttu-id="d52f5-147">Os eventos intrínsecos são usados para monitorar um recurso representado por uma classe no repositório CIM.</span><span class="sxs-lookup"><span data-stu-id="d52f5-147">Intrinsic events are used to monitor a resource represented by a class in the CIM repository.</span></span> <span data-ttu-id="d52f5-148">Cada recurso é representado por uma instância de uma classe.</span><span class="sxs-lookup"><span data-stu-id="d52f5-148">Each resource is represented by an instance of a class.</span></span> <span data-ttu-id="d52f5-149">Isso significa que o monitoramento de um recurso usando o WMI, na verdade, envolve o monitoramento das instâncias que correspondem ao recurso.</span><span class="sxs-lookup"><span data-stu-id="d52f5-149">This means that monitoring a resource using WMI actually involves monitoring the instances that correspond to the resource.</span></span>

<span data-ttu-id="d52f5-150">Eventos intrínsecos também podem ser usados para monitorar alterações em um namespace ou classe no repositório.</span><span class="sxs-lookup"><span data-stu-id="d52f5-150">Intrinsic events can also be used to monitor changes to a namespace or class in the repository.</span></span> <span data-ttu-id="d52f5-151">No entanto, o monitoramento de alterações em namespaces ou classes é de valor limitado para administradores do sistema.</span><span class="sxs-lookup"><span data-stu-id="d52f5-151">However, monitoring changes to namespaces or classes is of limited value to system administrators.</span></span>

<span data-ttu-id="d52f5-152">Um evento intrínseco é representado por uma instância de uma classe derivada de \_ \_ InstanceOperationEvent, \_ \_ NamespaceOperationEvent ou \_ \_ ClassOperationEvent.</span><span class="sxs-lookup"><span data-stu-id="d52f5-152">An intrinsic event is represented by an instance of a class derived from \_\_InstanceOperationEvent, \_\_NamespaceOperationEvent, or \_\_ClassOperationEvent.</span></span> <span data-ttu-id="d52f5-153">As alterações nas instâncias no WMI são representadas pela \_ \_ classe InstanceOperationEvent e pelas classes derivadas dela: \_ \_ InstanceCreationEvent, \_ \_ InstanceModificationEvent e \_ \_ InstanceDeletionEvent.</span><span class="sxs-lookup"><span data-stu-id="d52f5-153">Any changes to instances in WMI are represented by the \_\_InstanceOperationEvent class and the classes derived from it: \_\_InstanceCreationEvent, \_\_InstanceModificationEvent, and \_\_InstanceDeletionEvent.</span></span>

<span data-ttu-id="d52f5-154">Os recursos de monitoramento usando o WMI envolvem instâncias de monitoramento e todas as alterações feitas em instâncias são representadas por \_ \_ InstanceOperationEvent e pelas classes derivadas dela.</span><span class="sxs-lookup"><span data-stu-id="d52f5-154">Monitoring resources using WMI involves monitoring instances and all changes to instances are represented by \_\_InstanceOperationEvent and the classes derived from it.</span></span> <span data-ttu-id="d52f5-155">Isso significa que os recursos de monitoramento em última instância envolvem o monitoramento de instâncias de \_ \_ classes derivadas de InstanceOperationEvent.</span><span class="sxs-lookup"><span data-stu-id="d52f5-155">This means that monitoring resources ultimately involves monitoring instances of \_\_InstanceOperationEvent-derived classes.</span></span>

<span data-ttu-id="d52f5-156">Você registra o interesse em instâncias de uma dessas classes emitindo uma consulta de notificação expressa na WQL.</span><span class="sxs-lookup"><span data-stu-id="d52f5-156">You register interest in instances of one of these classes by issuing a notification query expressed in WQL.</span></span> <span data-ttu-id="d52f5-157">A consulta usa sintaxe semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="d52f5-157">The query uses syntax similar to the following:</span></span>

`SELECT * FROM __InstanceOperationEventOrDerivedClass WITHIN PollingInterval WHERE TargetInstance ISA WMIClassName AND TargetInstance.WMIClassPropertyName = Value`

<span data-ttu-id="d52f5-158">Para obter uma discussão mais demorada sobre como usar os eventos da instância WMI para monitorar a atividade do computador, consulte [como posso monitorar diferentes tipos de eventos com apenas um script?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/04/04/how-can-i-monitor-for-different-types-of-events-with-just-one-script.aspx)</span><span class="sxs-lookup"><span data-stu-id="d52f5-158">For a longer discussion of using the WMI instance events to monitor computer activity, see [How Can I Monitor for Different Types of Events With Just One Script?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/04/04/how-can-i-monitor-for-different-types-of-events-with-just-one-script.aspx)</span></span>

## <a name="examples"></a><span data-ttu-id="d52f5-159">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d52f5-159">Examples</span></span>

<span data-ttu-id="d52f5-160">O exemplo de código do [evento monitor Process](https://Gallery.TechNet.Microsoft.Com/94c7dc4c-813a-411d-aa3f-f98982cd2a2f) VBScript na galeria do TechNet usa **\_ \_ InstanceOperationEvent** para monitorar o primeiro evento de instância WMI para o [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="d52f5-160">The [Monitor process event](https://Gallery.TechNet.Microsoft.Com/94c7dc4c-813a-411d-aa3f-f98982cd2a2f) VBScript code sample on TechNet Gallery uses **\_\_InstanceOperationEvent** to monitors the first WMI instance event for [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>

## <a name="requirements"></a><span data-ttu-id="d52f5-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d52f5-161">Requirements</span></span>



| <span data-ttu-id="d52f5-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="d52f5-162">Requirement</span></span> | <span data-ttu-id="d52f5-163">Valor</span><span class="sxs-lookup"><span data-stu-id="d52f5-163">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="d52f5-164">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d52f5-164">Minimum supported client</span></span><br/> | <span data-ttu-id="d52f5-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d52f5-165">Windows Vista</span></span><br/>       |
| <span data-ttu-id="d52f5-166">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d52f5-166">Minimum supported server</span></span><br/> | <span data-ttu-id="d52f5-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d52f5-167">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="d52f5-168">Namespace</span><span class="sxs-lookup"><span data-stu-id="d52f5-168">Namespace</span></span><br/>                | <span data-ttu-id="d52f5-169">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="d52f5-169">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="d52f5-170">Confira também</span><span class="sxs-lookup"><span data-stu-id="d52f5-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d52f5-171">**\_\_Evento**</span><span class="sxs-lookup"><span data-stu-id="d52f5-171">**\_\_Event**</span></span>](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[<span data-ttu-id="d52f5-172">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="d52f5-172">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="d52f5-173">Determinando o tipo de evento a ser recebido</span><span class="sxs-lookup"><span data-stu-id="d52f5-173">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[<span data-ttu-id="d52f5-174">Gravando em um arquivo de log baseado em um evento</span><span class="sxs-lookup"><span data-stu-id="d52f5-174">Writing to a Log File Based on an Event</span></span>](writing-to-a-log-file-based-on-an-event.md)
</dt> </dl>

 

