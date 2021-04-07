---
description: A classe NTEventLogEventConsumer registra uma mensagem específica no log de eventos do sistema operacional quando um evento é entregue a ele.
ms.assetid: cf986812-f09a-4f32-ba76-db76a23e2e4c
ms.tgt_platform: multiple
title: Classe NTEventLogEventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NTEventLogEventConsumer
- NTEventLogEventConsumer.CreatorSID
- NTEventLogEventConsumer.MachineName
- NTEventLogEventConsumer.MaximumQueueSize
- NTEventLogEventConsumer.Category
- NTEventLogEventConsumer.NameOfRawDataProperty
- NTEventLogEventConsumer.EventID
- NTEventLogEventConsumer.EventType
- NTEventLogEventConsumer.InsertionStringTemplates
- NTEventLogEventConsumer.Name
- NTEventLogEventConsumer.NumberOfInsertionStrings
- NTEventLogEventConsumer.NameOfUserSidProperty
- NTEventLogEventConsumer.SourceName
- NTEventLogEventConsumer.UNCServerName
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: e98948688b0fee37316102b2c37039de1c139310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827491"
---
# <a name="nteventlogeventconsumer-class"></a><span data-ttu-id="daf50-103">Classe NTEventLogEventConsumer</span><span class="sxs-lookup"><span data-stu-id="daf50-103">NTEventLogEventConsumer class</span></span>

<span data-ttu-id="daf50-104">A classe **NTEventLogEventConsumer** registra uma mensagem específica no log de eventos do sistema operacional quando um evento é entregue a ele.</span><span class="sxs-lookup"><span data-stu-id="daf50-104">The **NTEventLogEventConsumer** class logs a specific message to the operating system event log when an event is delivered to it.</span></span> <span data-ttu-id="daf50-105">Essa classe é um dos consumidores de eventos padrão que o WMI fornece.</span><span class="sxs-lookup"><span data-stu-id="daf50-105">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="daf50-106">Para obter mais informações, consulte [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="daf50-106">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="daf50-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="daf50-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class NTEventLogEventConsumer : __EventConsumer
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
  uint16 Category;
  string NameOfRawDataProperty;
  uint32 EventID;
  uint32 EventType = 1;
  string InsertionStringTemplates[] = {""};
  string Name;
  uint32 NumberOfInsertionStrings = 0;
  string NameOfUserSidProperty;
  string SourceName;
  string UNCServerName;
};
```

## <a name="members"></a><span data-ttu-id="daf50-108">Membros</span><span class="sxs-lookup"><span data-stu-id="daf50-108">Members</span></span>

<span data-ttu-id="daf50-109">A classe **NTEventLogEventConsumer** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="daf50-109">The **NTEventLogEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="daf50-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="daf50-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="daf50-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="daf50-111">Properties</span></span>

<span data-ttu-id="daf50-112">A classe **NTEventLogEventConsumer** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="daf50-112">The **NTEventLogEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="daf50-113">**Categoria**</span><span class="sxs-lookup"><span data-stu-id="daf50-113">**Category**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="daf50-114">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="daf50-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="daf50-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="daf50-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="daf50-116">Categoria de evento.</span><span class="sxs-lookup"><span data-stu-id="daf50-116">Event category.</span></span> <span data-ttu-id="daf50-117">Essas são informações específicas de origem e podem ter qualquer valor.</span><span class="sxs-lookup"><span data-stu-id="daf50-117">This is source-specific information and can have any value.</span></span>

</dd> <dt>

<span data-ttu-id="daf50-118">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="daf50-118">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="daf50-119">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="daf50-119">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="daf50-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="daf50-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="daf50-121">SID (identificador de segurança) que identifica exclusivamente o usuário que cria um filtro.</span><span class="sxs-lookup"><span data-stu-id="daf50-121">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="daf50-122">O WMI armazena o SID do usuário que cria uma instância de [**\_ \_ EventConsumer**](--eventconsumer.md) ou o SID do administrador, dependendo do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="daf50-122">WMI stores the SID of the user who creates an instance of [**\_\_EventConsumer**](--eventconsumer.md) or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="daf50-123">Para obter mais informações, consulte [associando um filtro de eventos a um consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md) e [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="daf50-123">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="daf50-124">Essa propriedade é herdada de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="daf50-124">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="daf50-125">**EventID**</span><span class="sxs-lookup"><span data-stu-id="daf50-125">**EventID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="daf50-126">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="daf50-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="daf50-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="daf50-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="daf50-128">Mensagem de evento na DLL de mensagem.</span><span class="sxs-lookup"><span data-stu-id="daf50-128">Event message in the message DLL.</span></span> <span data-ttu-id="daf50-129">Esta propriedade não pode ser **nula**.</span><span class="sxs-lookup"><span data-stu-id="daf50-129">This property cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="daf50-130">**EventType**</span><span class="sxs-lookup"><span data-stu-id="daf50-130">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="daf50-131">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="daf50-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="daf50-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="daf50-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="daf50-133">Tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="daf50-133">Type of event.</span></span> <span data-ttu-id="daf50-134">Esse parâmetro pode ter um dos valores listados na lista a seguir, que são definidos em Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="daf50-134">This parameter can have one of the values listed in the following list, which are defined in Winnt.h.</span></span>

<dt>

<span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>

<span data-ttu-id="daf50-135"><span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>**Log de eventos \_ ÊXITO** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="daf50-135"><span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>**EVENTLOG\_SUCCESS** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="daf50-136">Evento bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="daf50-136">Successful event</span></span>

</dd> <dt>

<span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>

<span data-ttu-id="daf50-137"><span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>**Log de eventos \_ ERRO \_ TPYE** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="daf50-137"><span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>**EVENTLOG\_ERROR\_TPYE** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="daf50-138">Evento de erro</span><span class="sxs-lookup"><span data-stu-id="daf50-138">Error event</span></span>

</dd> <dt>

<span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>

<span data-ttu-id="daf50-139"><span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>**Log de eventos \_ \_Tipo de aviso** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="daf50-139"><span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>**EVENTLOG\_WARNING\_TYPE** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="daf50-140">Evento de aviso</span><span class="sxs-lookup"><span data-stu-id="daf50-140">Warning event</span></span>

</dd> <dt>

<span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>

<span data-ttu-id="daf50-141"><span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>**Log de eventos \_ \_Tipo de informação** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="daf50-141"><span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>**EVENTLOG\_INFORMATION\_TYPE** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="daf50-142">Evento de informações</span><span class="sxs-lookup"><span data-stu-id="daf50-142">Information event</span></span>

</dd> <dt>

<span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>

<span data-ttu-id="daf50-143"><span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>**Log de eventos \_ \_Êxito na auditoria** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="daf50-143"><span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>**EVENTLOG\_AUDIT\_SUCCESS** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="daf50-144">Tipo de auditoria com êxito</span><span class="sxs-lookup"><span data-stu-id="daf50-144">Success audit type</span></span>

</dd> <dt>

<span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>

<span data-ttu-id="daf50-145"><span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>**Log de eventos \_ \_Falha de auditoria** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="daf50-145"><span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>**EVENTLOG\_AUDIT\_FAILURE** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="daf50-146">Tipo de auditoria de falha</span><span class="sxs-lookup"><span data-stu-id="daf50-146">Failure audit type</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="daf50-147">**InsertionStringTemplates**</span><span class="sxs-lookup"><span data-stu-id="daf50-147">**InsertionStringTemplates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="daf50-148">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="daf50-148">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="daf50-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="daf50-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="daf50-150">Matriz de modelos de cadeia de caracteres padrão que é usada como a cadeia de caracteres de inserção para um registro de log de eventos.</span><span class="sxs-lookup"><span data-stu-id="daf50-150">Array of standard string templates that is used as the insertion string for an event log record.</span></span>

</dd> <dt>

<span data-ttu-id="daf50-151">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="daf50-151">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="daf50-152">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="daf50-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="daf50-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="daf50-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="daf50-154">Nome do computador ao qual Instrumentação de Gerenciamento do Windows (WMI) envia eventos.</span><span class="sxs-lookup"><span data-stu-id="daf50-154">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

<span data-ttu-id="daf50-155">Essa propriedade é herdada de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="daf50-155">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="daf50-156">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="daf50-156">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="daf50-157">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="daf50-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="daf50-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="daf50-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="daf50-159">Fila máxima para um consumidor específico, em bytes.</span><span class="sxs-lookup"><span data-stu-id="daf50-159">Maximum queue for a specific consumer, in bytes.</span></span>

<span data-ttu-id="daf50-160">Essa propriedade é herdada de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="daf50-160">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="daf50-161">**Nome**</span><span class="sxs-lookup"><span data-stu-id="daf50-161">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="daf50-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="daf50-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="daf50-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="daf50-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="daf50-164">Qualificadores: [ **chave**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="daf50-164">Qualifiers: [**key**](key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="daf50-165">Nome exclusivo de um consumidor.</span><span class="sxs-lookup"><span data-stu-id="daf50-165">Unique name of a consumer.</span></span>

</dd> <dt>

<span data-ttu-id="daf50-166">**NameOfRawDataProperty**</span><span class="sxs-lookup"><span data-stu-id="daf50-166">**NameOfRawDataProperty**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="daf50-167">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="daf50-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="daf50-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="daf50-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="daf50-169">Nome da propriedade de evento que contém os dados a serem passados para o parâmetro *lpRawData* da função [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) .</span><span class="sxs-lookup"><span data-stu-id="daf50-169">Name of the event property that contains data to be passed to the [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) function *lpRawData* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="daf50-170">**NameOfUserSidProperty**</span><span class="sxs-lookup"><span data-stu-id="daf50-170">**NameOfUserSidProperty**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="daf50-171">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="daf50-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="daf50-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="daf50-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="daf50-173">Nome da propriedade de evento que contém um SID (identificador de segurança) a ser passado para o parâmetro *lpUserSid* da função [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) .</span><span class="sxs-lookup"><span data-stu-id="daf50-173">Name of the event property that contains a security identifier (SID) to be passed to the [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) function *lpUserSid* parameter.</span></span> <span data-ttu-id="daf50-174">A propriedade deve ser uma matriz de bytes (**uint8**) ou uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="daf50-174">The property must be either an array of bytes (**uint8**) or a string.</span></span> <span data-ttu-id="daf50-175">Se for uma matriz de bytes, supõe-se que seja um SID.</span><span class="sxs-lookup"><span data-stu-id="daf50-175">If it is an array of bytes, it is assumed to be a SID.</span></span> <span data-ttu-id="daf50-176">Se for uma cadeia de caracteres, é um SID de cadeia de caracteres que é convertido em um SID.</span><span class="sxs-lookup"><span data-stu-id="daf50-176">If it is a string, it is a string SID that is converted into a SID.</span></span>

</dd> <dt>

<span data-ttu-id="daf50-177">**NumberOfInsertionStrings**</span><span class="sxs-lookup"><span data-stu-id="daf50-177">**NumberOfInsertionStrings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="daf50-178">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="daf50-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="daf50-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="daf50-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="daf50-180">Número de elementos na matriz **InsertionStringTemplates** .</span><span class="sxs-lookup"><span data-stu-id="daf50-180">Number of elements in the **InsertionStringTemplates** array.</span></span>

</dd> <dt>

<span data-ttu-id="daf50-181">**SourceName**</span><span class="sxs-lookup"><span data-stu-id="daf50-181">**SourceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="daf50-182">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="daf50-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="daf50-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="daf50-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="daf50-184">Nome de origem em que uma mensagem está localizada.</span><span class="sxs-lookup"><span data-stu-id="daf50-184">Source name where a message is located.</span></span> <span data-ttu-id="daf50-185">Supõe-se que o cliente tenha registrado uma DLL com as mensagens necessárias.</span><span class="sxs-lookup"><span data-stu-id="daf50-185">The customer is assumed to have registered a DLL with the necessary messages.</span></span>

> [!Note]  
> <span data-ttu-id="daf50-186">O valor desse parâmetro não deve incluir dois-pontos (:) espaço.</span><span class="sxs-lookup"><span data-stu-id="daf50-186">The value of this parameter must not include a colon (:) character.</span></span>

 

</dd> <dt>

<span data-ttu-id="daf50-187">**UNCServerName**</span><span class="sxs-lookup"><span data-stu-id="daf50-187">**UNCServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="daf50-188">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="daf50-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="daf50-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="daf50-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="daf50-190">Nome do computador no qual registrar um evento ou **nulo** se o evento for registrado em um servidor local.</span><span class="sxs-lookup"><span data-stu-id="daf50-190">Name of the computer on which to log an event, or **NULL** if the event is to be logged on a local server.</span></span>

<span data-ttu-id="daf50-191">Os usuários autenticados não podem, por padrão, registrar eventos no log do aplicativo em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="daf50-191">Authenticated users cannot, by default, log events to the Application log on a remote computer.</span></span> <span data-ttu-id="daf50-192">Como resultado, o uso dessa propriedade para especificar um computador remoto não funcionará.</span><span class="sxs-lookup"><span data-stu-id="daf50-192">As a result, using this property to specify a remote computer will not work.</span></span> <span data-ttu-id="daf50-193">Para saber como alterar a segurança do log de eventos, consulte este [artigo da base de conhecimento](https://support.microsoft.com/kb/323076).</span><span class="sxs-lookup"><span data-stu-id="daf50-193">To learn how to change event log security, consult this [KB article](https://support.microsoft.com/kb/323076).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="daf50-194">Comentários</span><span class="sxs-lookup"><span data-stu-id="daf50-194">Remarks</span></span>

<span data-ttu-id="daf50-195">A classe **NTEventLogEventConsumer** é derivada da classe abstrata [**\_ \_ EventConsumer**](--eventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="daf50-195">The **NTEventLogEventConsumer** class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span>

## <a name="examples"></a><span data-ttu-id="daf50-196">Exemplos</span><span class="sxs-lookup"><span data-stu-id="daf50-196">Examples</span></span>

<span data-ttu-id="daf50-197">Para obter um exemplo de como usar o **NTEventLogEventConsumer** para criar um consumidor, consulte [log no log de eventos NT com base em um evento](logging-to-nt-event-log-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="daf50-197">For an example of using **NTEventLogEventConsumer** to create a consumer, see [Logging to NT Event Log Based on an Event](logging-to-nt-event-log-based-on-an-event.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="daf50-198">Requisitos</span><span class="sxs-lookup"><span data-stu-id="daf50-198">Requirements</span></span>



| <span data-ttu-id="daf50-199">Requisito</span><span class="sxs-lookup"><span data-stu-id="daf50-199">Requirement</span></span> | <span data-ttu-id="daf50-200">Valor</span><span class="sxs-lookup"><span data-stu-id="daf50-200">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="daf50-201">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="daf50-201">Minimum supported client</span></span><br/> | <span data-ttu-id="daf50-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="daf50-202">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="daf50-203">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="daf50-203">Minimum supported server</span></span><br/> | <span data-ttu-id="daf50-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="daf50-204">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="daf50-205">Namespace</span><span class="sxs-lookup"><span data-stu-id="daf50-205">Namespace</span></span><br/>                | <span data-ttu-id="daf50-206">\\Assinatura raiz</span><span class="sxs-lookup"><span data-stu-id="daf50-206">Root\\subscription</span></span><br/>                                                           |
| <span data-ttu-id="daf50-207">MOF</span><span class="sxs-lookup"><span data-stu-id="daf50-207">MOF</span></span><br/>                      | <dl> <span data-ttu-id="daf50-208"><dt>Wbemcons. mof</dt></span><span class="sxs-lookup"><span data-stu-id="daf50-208"><dt>Wbemcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="daf50-209">DLL</span><span class="sxs-lookup"><span data-stu-id="daf50-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="daf50-210"><dt>Wbemcons.dll</dt></span><span class="sxs-lookup"><span data-stu-id="daf50-210"><dt>Wbemcons.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="daf50-211">Confira também</span><span class="sxs-lookup"><span data-stu-id="daf50-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daf50-212">Classes de consumidor padrão</span><span class="sxs-lookup"><span data-stu-id="daf50-212">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="daf50-213">Criando um consumidor lógico</span><span class="sxs-lookup"><span data-stu-id="daf50-213">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="daf50-214">Recebendo eventos em todos os momentos</span><span class="sxs-lookup"><span data-stu-id="daf50-214">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="daf50-215">**\_\_EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="daf50-215">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> </dl>

 

