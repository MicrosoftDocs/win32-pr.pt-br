---
description: É usado no registro de consumidores de eventos permanentes para relacionar uma instância do \_ \_ EventConsumer a uma instância de \_ \_ EventFilter.
ms.assetid: e6a06161-0f1c-4754-ac34-263ccf7bf10d
ms.tgt_platform: multiple
title: Classe __FilterToConsumerBinding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __FilterToConsumerBinding
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
ms.openlocfilehash: 0fd9b7f3cf60d14d27fdf5b5014b57e6f599d67f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798266"
---
# <a name="__filtertoconsumerbinding-class"></a><span data-ttu-id="a61bf-103">\_\_Classe FilterToConsumerBinding</span><span class="sxs-lookup"><span data-stu-id="a61bf-103">\_\_FilterToConsumerBinding class</span></span>

<span data-ttu-id="a61bf-104">A classe de sistema **\_ \_ FilterToConsumerBinding** é usada no registro de consumidores de eventos permanentes para relacionar uma instância do [**\_ \_ EventConsumer**](--eventconsumer.md) a uma instância de [**\_ \_ EventFilter**](--eventfilter.md).**\_ \_ FilterToConsumerBinding** é uma classe de associação.</span><span class="sxs-lookup"><span data-stu-id="a61bf-104">The **\_\_FilterToConsumerBinding** system class is used in the registration of permanent event consumers to relate an instance of the [**\_\_EventConsumer**](--eventconsumer.md) to an instance of [**\_\_EventFilter**](--eventfilter.md).**\_\_FilterToConsumerBinding** is an association class.</span></span>

<span data-ttu-id="a61bf-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a61bf-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a61bf-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="a61bf-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a61bf-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a61bf-107">Syntax</span></span>

``` syntax
class __FilterToConsumerBinding : __IndicationRelated
{
  __EventConsumer REF Consumer;
  uint8               CreatorSID[];
  boolean             DeliverSynchronously = False;
  uint32              DeliveryQoS;
  __EventFilter   REF Filter;
  boolean             MaintainSecurityContext = False;
  boolean             SlowDownProviders = False;
};
```

## <a name="members"></a><span data-ttu-id="a61bf-108">Membros</span><span class="sxs-lookup"><span data-stu-id="a61bf-108">Members</span></span>

<span data-ttu-id="a61bf-109">A classe **\_ \_ FilterToConsumerBinding** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a61bf-109">The **\_\_FilterToConsumerBinding** class has these types of members:</span></span>

-   [<span data-ttu-id="a61bf-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a61bf-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a61bf-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a61bf-111">Properties</span></span>

<span data-ttu-id="a61bf-112">A classe **\_ \_ FilterToConsumerBinding** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a61bf-112">The **\_\_FilterToConsumerBinding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a61bf-113">**Consumidor**</span><span class="sxs-lookup"><span data-stu-id="a61bf-113">**Consumer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a61bf-114">Tipo de dados: **\_ \_ EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="a61bf-114">Data type: **\_\_EventConsumer**</span></span>
</dt> <dt>

<span data-ttu-id="a61bf-115">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a61bf-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a61bf-116">Qualificadores: [ **chave**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="a61bf-116">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="a61bf-117">Referência a uma instância de [**\_ \_ EventConsumer**](--eventconsumer.md) que representa o caminho do objeto para um consumidor lógico, o destinatário de um evento.</span><span class="sxs-lookup"><span data-stu-id="a61bf-117">Reference to an instance of [**\_\_EventConsumer**](--eventconsumer.md) that represents the object path to a logical consumer, the recipient of an event.</span></span> <span data-ttu-id="a61bf-118">Um consumidor lógico é uma instância de uma classe derivada de **\_ \_ EventConsumer**.</span><span class="sxs-lookup"><span data-stu-id="a61bf-118">A logical consumer is an instance of a class derived from **\_\_EventConsumer**.</span></span>

</dd> <dt>

<span data-ttu-id="a61bf-119">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="a61bf-119">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a61bf-120">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="a61bf-120">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="a61bf-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a61bf-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a61bf-122">SID (identificador de segurança) que identifica exclusivamente o usuário que criou a associação.</span><span class="sxs-lookup"><span data-stu-id="a61bf-122">Security identifier (SID) that uniquely identifies the user who created the binding.</span></span> <span data-ttu-id="a61bf-123">Dependendo do sistema operacional, o WMI armazena o SID do administrador ou o SID do usuário que cria uma instância do **\_ \_ FilterToConsumerBinding**.</span><span class="sxs-lookup"><span data-stu-id="a61bf-123">Depending on the operating system, WMI stores the Administrator SID or the SID of the user that creates an instance of **\_\_FilterToConsumerBinding**.</span></span> <span data-ttu-id="a61bf-124">Para obter mais informações, consulte [associando um filtro de eventos a um consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md) e [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="a61bf-124">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

</dd> <dt>

<span data-ttu-id="a61bf-125">**DeliverSynchronously**</span><span class="sxs-lookup"><span data-stu-id="a61bf-125">**DeliverSynchronously**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a61bf-126">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a61bf-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a61bf-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a61bf-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a61bf-128">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="a61bf-128">Obsolete.</span></span> <span data-ttu-id="a61bf-129">Em vez disso, use a propriedade **DeliveryQoS** no lugar dessa propriedade, porque se **DeliverSynchronously** for definido como **true** , ele substituirá a configuração da propriedade **DeliveryQoS** .</span><span class="sxs-lookup"><span data-stu-id="a61bf-129">Instead use the **DeliveryQoS** property in place of this property, because if **DeliverSynchronously** is set to **True** it overrides the setting of the **DeliveryQoS** property.</span></span>

</dd> <dt>

<span data-ttu-id="a61bf-130">**DeliveryQoS**</span><span class="sxs-lookup"><span data-stu-id="a61bf-130">**DeliveryQoS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a61bf-131">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a61bf-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a61bf-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a61bf-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a61bf-133">Qualidade de serviço para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="a61bf-133">Quality of service for a subscription.</span></span> <span data-ttu-id="a61bf-134">Se a propriedade **DeliverSynchronously** for definida como **true**, ela substituirá a configuração da propriedade **DeliveryQoS** .</span><span class="sxs-lookup"><span data-stu-id="a61bf-134">If the **DeliverSynchronously** property is set to **True**, it overrides the setting of the **DeliveryQoS** property.</span></span>

<dt>

<span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>

<span data-ttu-id="a61bf-135"><span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>**WMIMSG \_ SINALIZAr \_ QoS \_ síncrono** (0)</span><span class="sxs-lookup"><span data-stu-id="a61bf-135"><span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>**WMIMSG\_FLAG\_QOS\_SYNCHRONOUS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="a61bf-136">Entrega síncrona</span><span class="sxs-lookup"><span data-stu-id="a61bf-136">Synchronous delivery</span></span>

<span data-ttu-id="a61bf-137">**False**.</span><span class="sxs-lookup"><span data-stu-id="a61bf-137">**False**.</span></span> <span data-ttu-id="a61bf-138">O evento é entregue ao consumidor lógico de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="a61bf-138">The event is delivered to the logical consumer synchronously.</span></span>

</dd> <dt>

<span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>

<span data-ttu-id="a61bf-139"><span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>**WMIMSG \_ SINALIZAr \_ QoS \_ Express** (1)</span><span class="sxs-lookup"><span data-stu-id="a61bf-139"><span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>**WMIMSG\_FLAG\_QOS\_EXPRESS** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a61bf-140">Entrega expressa</span><span class="sxs-lookup"><span data-stu-id="a61bf-140">Express delivery</span></span>

<span data-ttu-id="a61bf-141">**True**.</span><span class="sxs-lookup"><span data-stu-id="a61bf-141">**True**.</span></span> <span data-ttu-id="a61bf-142">O evento é entregue ao consumidor lógico de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="a61bf-142">The event is delivered to the logical consumer asynchronously.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a61bf-143">**Filter**</span><span class="sxs-lookup"><span data-stu-id="a61bf-143">**Filter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a61bf-144">Tipo de dados: **\_ \_ EventFilter**</span><span class="sxs-lookup"><span data-stu-id="a61bf-144">Data type: **\_\_EventFilter**</span></span>
</dt> <dt>

<span data-ttu-id="a61bf-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a61bf-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a61bf-146">Qualificadores: [ **chave**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="a61bf-146">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="a61bf-147">Referência a uma instância de [**\_ \_ EventFilter**](--eventfilter.md) que representa o caminho do objeto para um filtro de eventos que é uma consulta que especifica o tipo de evento a ser recebido.</span><span class="sxs-lookup"><span data-stu-id="a61bf-147">Reference to an instance of [**\_\_EventFilter**](--eventfilter.md) that represents the object path to an event filter which is a query that specifies the type of event to be received.</span></span>

</dd> <dt>

<span data-ttu-id="a61bf-148">**MaintainSecurityContext**</span><span class="sxs-lookup"><span data-stu-id="a61bf-148">**MaintainSecurityContext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a61bf-149">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a61bf-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a61bf-150">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a61bf-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a61bf-151">Se **for true**, os eventos serão entregues no mesmo contexto de segurança em que o provedor estava quando os forneceu.</span><span class="sxs-lookup"><span data-stu-id="a61bf-151">If **True**, the events are delivered in the same security context that the provider was in when it provided them.</span></span>

> [!Note]  
> <span data-ttu-id="a61bf-152">Somente um consumidor implementado como uma DLL (um consumidor em processo) pode receber eventos no contexto de segurança do provedor.</span><span class="sxs-lookup"><span data-stu-id="a61bf-152">Only a consumer implemented as a DLL (an in-process consumer) can receive events in the security context of the provider.</span></span> <span data-ttu-id="a61bf-153">Para obter mais informações sobre provedores em processo e segurança, consulte [hospedagem e segurança do provedor](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="a61bf-153">For more information about in-process providers and security, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span> <span data-ttu-id="a61bf-154">Para obter mais informações e exemplos, consulte replace:[recebendo eventos com segurança](receiving-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="a61bf-154">For more information and examples, see replace:[Receiving Events Securely](receiving-events-securely.md).</span></span>

 

</dd> <dt>

<span data-ttu-id="a61bf-155">**SlowDownProviders**</span><span class="sxs-lookup"><span data-stu-id="a61bf-155">**SlowDownProviders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a61bf-156">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a61bf-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a61bf-157">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a61bf-157">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a61bf-158">Se **for true**, os provedores serão reduzidos se este consumidor não puder acompanhar.</span><span class="sxs-lookup"><span data-stu-id="a61bf-158">If **True**, providers are slowed down if this consumer cannot keep up.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a61bf-159">Comentários</span><span class="sxs-lookup"><span data-stu-id="a61bf-159">Remarks</span></span>

<span data-ttu-id="a61bf-160">A classe **\_ \_ FilterToConsumerBinding** é derivada de [**\_ \_ IndicationRelated**](--indicationrelated.md), que não tem propriedades.</span><span class="sxs-lookup"><span data-stu-id="a61bf-160">The **\_\_FilterToConsumerBinding** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which has no properties.</span></span>

<span data-ttu-id="a61bf-161">Os consumidores de eventos permanentes usam a classe de sistema **\_ \_ FilterToConsumerBinding** para associar filtros de eventos aos consumidores finais.</span><span class="sxs-lookup"><span data-stu-id="a61bf-161">Permanent event consumers use the **\_\_FilterToConsumerBinding** system class to bind event filters to final consumers.</span></span> <span data-ttu-id="a61bf-162">Depois que o filtro e o consumidor são associados, o WMI pode encaminhar eventos que correspondam ao filtro para o consumidor correspondente.</span><span class="sxs-lookup"><span data-stu-id="a61bf-162">After the filter and consumer are bound together, WMI can forward events that match the filter to the corresponding consumer.</span></span>

## <a name="examples"></a><span data-ttu-id="a61bf-163">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a61bf-163">Examples</span></span>

<span data-ttu-id="a61bf-164">O exemplo de [criar registro de evento WMI permanente para monitorar arquivos](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) no PowerShell na galeria do TechNet usa **\_ \_ FilterToConsumerBinding** como parte de um script complexo para configurar um registro de evento do WMI permanente.</span><span class="sxs-lookup"><span data-stu-id="a61bf-164">The [Create Permanent WMI Event registration to monitor files](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell example on TechNet Gallery uses **\_\_FilterToConsumerBinding** as part of a complex script to set up a permanent WMI event registration.</span></span>

## <a name="requirements"></a><span data-ttu-id="a61bf-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a61bf-165">Requirements</span></span>



| <span data-ttu-id="a61bf-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="a61bf-166">Requirement</span></span> | <span data-ttu-id="a61bf-167">Valor</span><span class="sxs-lookup"><span data-stu-id="a61bf-167">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="a61bf-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a61bf-168">Minimum supported client</span></span><br/> | <span data-ttu-id="a61bf-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a61bf-169">Windows Vista</span></span><br/>       |
| <span data-ttu-id="a61bf-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a61bf-170">Minimum supported server</span></span><br/> | <span data-ttu-id="a61bf-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a61bf-171">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="a61bf-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="a61bf-172">Namespace</span></span><br/>                | <span data-ttu-id="a61bf-173">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="a61bf-173">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="a61bf-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="a61bf-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a61bf-175">**\_\_IndicationRelated**</span><span class="sxs-lookup"><span data-stu-id="a61bf-175">**\_\_IndicationRelated**</span></span>](--indicationrelated.md)
</dt> <dt>

[<span data-ttu-id="a61bf-176">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="a61bf-176">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="a61bf-177">Monitorando e respondendo a eventos com consumidores padrão</span><span class="sxs-lookup"><span data-stu-id="a61bf-177">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[<span data-ttu-id="a61bf-178">Eventos de monitoramento</span><span class="sxs-lookup"><span data-stu-id="a61bf-178">Monitoring Events</span></span>](monitoring-events.md)
</dt> <dt>

[<span data-ttu-id="a61bf-179">Criando um filtro de eventos</span><span class="sxs-lookup"><span data-stu-id="a61bf-179">Creating an Event Filter</span></span>](creating-an-event-filter.md)
</dt> <dt>

[<span data-ttu-id="a61bf-180">Protegendo eventos WMI</span><span class="sxs-lookup"><span data-stu-id="a61bf-180">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> </dl>

 

 




