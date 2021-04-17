---
description: O registro de um consumidor de evento permanente requer uma instância da \_ \_ classe de sistema EventFilter.
ms.assetid: 369d3c28-2b69-456f-9144-d7c73e3123bc
ms.tgt_platform: multiple
title: Classe __EventFilter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventFilter
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
ms.openlocfilehash: 0316e158eb2098f89106c64ba0057f8d9b4fc26b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763009"
---
# <a name="__eventfilter-class"></a><span data-ttu-id="23805-103">\_\_Classe EventFilter</span><span class="sxs-lookup"><span data-stu-id="23805-103">\_\_EventFilter class</span></span>

<span data-ttu-id="23805-104">O registro de um consumidor de evento permanente requer uma instância da classe de sistema **\_ \_ EventFilter** .</span><span class="sxs-lookup"><span data-stu-id="23805-104">The registration of a permanent event consumer requires an instance of the **\_\_EventFilter** system class.</span></span>

<span data-ttu-id="23805-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="23805-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="23805-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="23805-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="23805-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23805-107">Syntax</span></span>

``` syntax
class __EventFilter : __IndicationRelated
{
  uint8  CreatorSID[] = {1,1,0,0,0,0,0,5,18,0,0,0};
  string EventAccess;
  string EventNamespace;
  string Name;
  string Query;
  string QueryLanguage;
};
```

## <a name="members"></a><span data-ttu-id="23805-108">Membros</span><span class="sxs-lookup"><span data-stu-id="23805-108">Members</span></span>

<span data-ttu-id="23805-109">A classe **\_ \_ EventFilter** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="23805-109">The **\_\_EventFilter** class has these types of members:</span></span>

-   [<span data-ttu-id="23805-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="23805-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="23805-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="23805-111">Properties</span></span>

<span data-ttu-id="23805-112">A classe **\_ \_ EventFilter** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="23805-112">The **\_\_EventFilter** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="23805-113">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="23805-113">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23805-114">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="23805-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="23805-115">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="23805-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="23805-116">SID (identificador de segurança) que identifica exclusivamente o usuário que cria esse filtro.</span><span class="sxs-lookup"><span data-stu-id="23805-116">Security identifier (SID) that uniquely identifies the user who creates this filter.</span></span> <span data-ttu-id="23805-117">Instrumentação de gerenciamento do Windows (WMI) armazena o SID do usuário que cria uma instância de **\_ \_ EventFilter** ou o SID do administrador, dependendo do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="23805-117">Windows Management Instrumentation (WMI) stores the SID of the user that creates an instance of **\_\_EventFilter** or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="23805-118">Para obter mais informações, consulte [associando um filtro de eventos a um consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md) e [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="23805-118">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

</dd> <dt>

<span data-ttu-id="23805-119">**EventAccess**</span><span class="sxs-lookup"><span data-stu-id="23805-119">**EventAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23805-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="23805-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23805-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="23805-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="23805-122">Descritor de segurança (SD) na linguagem de definição de descritor de segurança (SDDL) que controla o acesso a eventos entregues ao filtro.</span><span class="sxs-lookup"><span data-stu-id="23805-122">Security descriptor (SD) in Security Descriptor Definition Language (SDDL) that controls access for events delivered to the filter.</span></span> <span data-ttu-id="23805-123">Use essa propriedade para especificar que somente os eventos no contexto de segurança de contas específicas podem ser entregues a esse filtro.</span><span class="sxs-lookup"><span data-stu-id="23805-123">Use this property to specify that only events in the security context of specific accounts can be delivered to this filter.</span></span> <span data-ttu-id="23805-124">Por exemplo, um consumidor de evento permanente pode limpar os logs de segurança somente quando um evento específico é gerado por um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="23805-124">For example, a permanent event consumer may clear the security logs only when a specific event is generated by a specific user.</span></span> <span data-ttu-id="23805-125">Para especificar quem pode publicar eventos nesse filtro, use a máscara **de \_ \_ publicação do WBEM direito** na ACE (entrada de controle de acesso) para a propriedade do [**\_ descritor de segurança**](--event.md) .</span><span class="sxs-lookup"><span data-stu-id="23805-125">To specify who can publish events to this filter, use the **WBEM\_RIGHT\_PUBLISH** mask in the Access Control Entry (ACE) for the [**SECURITY\_DESCRIPTOR**](--event.md) property.</span></span> <span data-ttu-id="23805-126">Para obter mais informações, consulte [linguagem de definição do descritor de segurança](/windows/desktop/SecAuthZ/security-descriptor-definition-language).</span><span class="sxs-lookup"><span data-stu-id="23805-126">For more information, see [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language).</span></span> <span data-ttu-id="23805-127">Para obter mais informações sobre constantes usadas para definir esse descritor de segurança, consulte [constantes de segurança do WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="23805-127">For more information about constants used to set this security descriptor, see [WMI Security Constants](wmi-security-constants.md).</span></span> <span data-ttu-id="23805-128">Para obter mais informações e exemplos, consulte replace:[recebendo eventos com segurança](receiving-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="23805-128">For more information and examples, see replace:[Receiving Events Securely](receiving-events-securely.md).</span></span>

<span data-ttu-id="23805-129">Você pode configurar um descritor de segurança de acesso de evento para permitir que um evento seja entregue somente quando a conta do sistema local gerar o evento.</span><span class="sxs-lookup"><span data-stu-id="23805-129">You can configure an event access security descriptor to allow an event to be delivered only when the local system account generates the event.</span></span> <span data-ttu-id="23805-130">Para obter mais informações sobre como criar um descritor de segurança e autorizar o acesso, consulte [controle de acesso](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="23805-130">For more information about creating security descriptor and authorizing access, see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

<span data-ttu-id="23805-131">Exemplo: a cadeia de caracteres SDDL a seguir permite que somente administradores forneçam eventos para o filtro.</span><span class="sxs-lookup"><span data-stu-id="23805-131">Example: The following SDDL string allows only administrators to provide events to the filter.</span></span> <span data-ttu-id="23805-132">O direito necessário para fornecer eventos é **a \_ \_ publicação do WBEM à direita** (x80).</span><span class="sxs-lookup"><span data-stu-id="23805-132">The right required to provide events is **WBEM\_RIGHT\_PUBLISH** (x80).</span></span>


```VB
O:BAG:BAD:(A;;0x80;;;BA)
```



</dd> <dt>

<span data-ttu-id="23805-133">**EventNamespace**</span><span class="sxs-lookup"><span data-stu-id="23805-133">**EventNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23805-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="23805-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23805-135">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="23805-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="23805-136">Namespace da instância de evento usada para assinaturas de namespace cruzado.</span><span class="sxs-lookup"><span data-stu-id="23805-136">Namespace of the event instance used for cross-namespace subscriptions.</span></span>

</dd> <dt>

<span data-ttu-id="23805-137">**Nome**</span><span class="sxs-lookup"><span data-stu-id="23805-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23805-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="23805-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23805-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="23805-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="23805-140">Qualificadores: [ **chave**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="23805-140">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="23805-141">Identificador exclusivo de um filtro de eventos.</span><span class="sxs-lookup"><span data-stu-id="23805-141">Unique identifier of an event filter.</span></span> <span data-ttu-id="23805-142">Como um filtro de eventos é usado apenas internamente pelo WMI, é recomendável que você defina essa propriedade como um **GUID**(identificador global exclusivo) convertido em uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="23805-142">Because an event filter is only used internally by WMI, it is recommended that you set this property to a globally unique identifier (**GUID**) converted to a string.</span></span> <span data-ttu-id="23805-143">No entanto, os consumidores podem usar qualquer esquema privado para um nome de filtro, contanto que não haja um conflito com outros filtros.</span><span class="sxs-lookup"><span data-stu-id="23805-143">However, consumers can use any private scheme for a filter name as long as there is not a conflict with other filters.</span></span>

</dd> <dt>

<span data-ttu-id="23805-144">**Consulta**</span><span class="sxs-lookup"><span data-stu-id="23805-144">**Query**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23805-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="23805-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23805-146">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="23805-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="23805-147">Consulta de evento WQL (linguagem de consulta Instrumentação de Gerenciamento do Windows) que especifica o conjunto de eventos para notificação do consumidor e as condições específicas para notificação.</span><span class="sxs-lookup"><span data-stu-id="23805-147">Windows Management Instrumentation Query Language (WQL) event query that specifies the set of events for consumer notification, and the specific conditions for notification.</span></span>

</dd> <dt>

<span data-ttu-id="23805-148">**QueryLanguage**</span><span class="sxs-lookup"><span data-stu-id="23805-148">**QueryLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23805-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="23805-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23805-150">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="23805-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="23805-151">Idioma usado para a consulta.</span><span class="sxs-lookup"><span data-stu-id="23805-151">Language used for the query.</span></span> <span data-ttu-id="23805-152">Como o WMI atualmente suporta apenas linguagem WQL (WQL) como uma linguagem de consulta, essa propriedade deve ser definida como "WQL".</span><span class="sxs-lookup"><span data-stu-id="23805-152">Because WMI currently supports only WMI Query Language (WQL) as a query language, this property must be set to "WQL".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23805-153">Comentários</span><span class="sxs-lookup"><span data-stu-id="23805-153">Remarks</span></span>

<span data-ttu-id="23805-154">A classe **\_ \_ EventFilter** é derivada de [**\_ \_ IndicationRelated**](--indicationrelated.md).</span><span class="sxs-lookup"><span data-stu-id="23805-154">The **\_\_EventFilter** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md).</span></span>

## <a name="examples"></a><span data-ttu-id="23805-155">Exemplos</span><span class="sxs-lookup"><span data-stu-id="23805-155">Examples</span></span>

<span data-ttu-id="23805-156">O exemplo de [criar registro de evento WMI permanente para monitorar arquivos](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) no PowerShell na galeria do TechNet usa **\_ \_ EventFilter** como parte de um script complexo para configurar um registro de evento do WMI permanente.</span><span class="sxs-lookup"><span data-stu-id="23805-156">The [Create Permanent WMI Event registration to monitor files](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell example on TechNet Gallery uses **\_\_EventFilter** as part of a complex script to set up a permanent WMI event registration.</span></span>

## <a name="requirements"></a><span data-ttu-id="23805-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23805-157">Requirements</span></span>



| <span data-ttu-id="23805-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="23805-158">Requirement</span></span> | <span data-ttu-id="23805-159">Valor</span><span class="sxs-lookup"><span data-stu-id="23805-159">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="23805-160">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23805-160">Minimum supported client</span></span><br/> | <span data-ttu-id="23805-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="23805-161">Windows Vista</span></span><br/>       |
| <span data-ttu-id="23805-162">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23805-162">Minimum supported server</span></span><br/> | <span data-ttu-id="23805-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="23805-163">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="23805-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="23805-164">Namespace</span></span><br/>                | <span data-ttu-id="23805-165">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="23805-165">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="23805-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="23805-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23805-167">**\_\_IndicationRelated**</span><span class="sxs-lookup"><span data-stu-id="23805-167">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="23805-168">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="23805-168">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="23805-169">Criando um filtro de eventos</span><span class="sxs-lookup"><span data-stu-id="23805-169">Creating an Event Filter</span></span>](creating-an-event-filter.md)
</dt> <dt>

[<span data-ttu-id="23805-170">Recebendo eventos em todos os momentos</span><span class="sxs-lookup"><span data-stu-id="23805-170">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="23805-171">Monitorando e respondendo a eventos com consumidores padrão</span><span class="sxs-lookup"><span data-stu-id="23805-171">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[<span data-ttu-id="23805-172">Eventos de monitoramento</span><span class="sxs-lookup"><span data-stu-id="23805-172">Monitoring Events</span></span>](monitoring-events.md)
</dt> <dt>

[<span data-ttu-id="23805-173">Classes de consumidor padrão</span><span class="sxs-lookup"><span data-stu-id="23805-173">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="23805-174">Protegendo eventos WMI</span><span class="sxs-lookup"><span data-stu-id="23805-174">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> </dl>

 

