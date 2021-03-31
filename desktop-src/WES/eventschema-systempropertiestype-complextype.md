---
title: Tipo complexo SystemPropertiesType
description: Define as informações que identificam o provedor e como elas foram habilitadas, o evento, o canal no qual o evento foi gravado e informações do sistema, como as IDs de processo e thread.
ms.assetid: f86f7940-86cf-49ba-8f09-bf6f473d60fd
keywords:
- Log de eventos do tipo complexo SystemPropertiesType
topic_type:
- apiref
api_name:
- SystemPropertiesType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce78a804c52ed492bd4b2a42332f8eda36b4c3be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644955"
---
# <a name="systempropertiestype-complex-type"></a><span data-ttu-id="5e8e4-104">Tipo complexo SystemPropertiesType</span><span class="sxs-lookup"><span data-stu-id="5e8e4-104">SystemPropertiesType Complex Type</span></span>

<span data-ttu-id="5e8e4-105">Define as informações que identificam o provedor e como elas foram habilitadas, o evento, o canal no qual o evento foi gravado e informações do sistema, como as IDs de processo e thread.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-105">Defines the information that identifies the provider and how it was enabled, the event, the channel to which the event was written, and system information such as the process and thread IDs.</span></span>

``` syntax
<xs:complexType name="SystemPropertiesType">
    <xs:sequence>
        <xs:element name="Provider">
            <xs:complexType>
                <xs:attribute name="Name"
                    type="anyURI"
                    use="optional"
                 />
                <xs:attribute name="Guid"
                    type="GUIDType"
                    use="optional"
                 />
                <xs:attribute name="EventSourceName"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="EventID">
            <xs:complexType>
                <xs:simpleContent>
                    <xs:extension
                        base="unsignedShort"
                    >
                        <xs:attribute name="Qualifiers"
                            type="unsignedShort"
                            use="optional"
                         />
                    </xs:extension>
                </xs:simpleContent>
            </xs:complexType>
        </xs:element>
        <xs:element name="Version"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Level"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Task"
            type="unsignedShort"
            minOccurs="0"
         />
        <xs:element name="Opcode"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Keywords"
            type="HexInt64Type"
            minOccurs="0"
         />
        <xs:element name="TimeCreated"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="SystemTime"
                    type="dateTime"
                    use="optional"
                 />
                <xs:attribute name="RawTime"
                    type="unsignedLong"
                    use="optional"
                 />
            </xs:complexType>
            <xs:key name="uniqueAtt">
                <xs:selector
                    xpath="."
                 />
                <xs:field
                    xpath="@SystemTime|@RawTime"
                 />
            </xs:key>
        </xs:element>
        <xs:element name="EventRecordID"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:simpleContent>
                    <xs:extension
                        base="unsignedLong"
                     />
                </xs:simpleContent>
            </xs:complexType>
        </xs:element>
        <xs:element name="Correlation"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="ActivityID"
                    type="GUIDType"
                    use="optional"
                 />
                <xs:attribute name="RelatedActivityID"
                    type="GUIDType"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Execution"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="ProcessID"
                    type="unsignedInt"
                    use="required"
                 />
                <xs:attribute name="ThreadID"
                    type="unsignedInt"
                    use="required"
                 />
                <xs:attribute name="ProcessorID"
                    type="unsignedByte"
                    use="optional"
                 />
                <xs:attribute name="SessionID"
                    type="unsignedInt"
                    use="optional"
                 />
                <xs:attribute name="KernelTime"
                    type="unsignedInt"
                    use="optional"
                 />
                <xs:attribute name="UserTime"
                    type="unsignedInt"
                    use="optional"
                 />
                <xs:attribute name="ProcessorTime"
                    type="unsignedInt"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Channel"
            type="anyURI"
            minOccurs="0"
         />
        <xs:element name="Computer"
            type="string"
         />
        <xs:element name="Security"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="UserID"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="5e8e4-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5e8e4-106">Child elements</span></span>



| <span data-ttu-id="5e8e4-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="5e8e4-107">Element</span></span>                                                                         | <span data-ttu-id="5e8e4-108">Type</span><span class="sxs-lookup"><span data-stu-id="5e8e4-108">Type</span></span>                                                        | <span data-ttu-id="5e8e4-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e8e4-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e8e4-110">**Canal**</span><span class="sxs-lookup"><span data-stu-id="5e8e4-110">**Channel**</span></span>](eventschema-channel-systempropertiestype-element.md)             | <span data-ttu-id="5e8e4-111">anyURI</span><span class="sxs-lookup"><span data-stu-id="5e8e4-111">anyURI</span></span>                                                      | <span data-ttu-id="5e8e4-112">O canal no qual o evento foi registrado.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-112">The channel to which the event was logged.</span></span><br/>                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="5e8e4-113">**Computador**</span><span class="sxs-lookup"><span data-stu-id="5e8e4-113">**Computer**</span></span>](eventschema-computer-systempropertiestype-element.md)           | <span data-ttu-id="5e8e4-114">string</span><span class="sxs-lookup"><span data-stu-id="5e8e4-114">string</span></span>                                                      | <span data-ttu-id="5e8e4-115">O nome do computador no qual o evento ocorreu.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-115">The name of the computer on which the event occurred.</span></span><br/>                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="5e8e4-116">**Correlação**</span><span class="sxs-lookup"><span data-stu-id="5e8e4-116">**Correlation**</span></span>](eventschema-correlation-systempropertiestype-element.md)     |                                                             | <span data-ttu-id="5e8e4-117">Os identificadores de atividade que os consumidores podem usar para agrupar eventos relacionados.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-117">The activity identifiers that consumers can use to group related events together.</span></span><br/>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="5e8e4-118">**1008**</span><span class="sxs-lookup"><span data-stu-id="5e8e4-118">**EventID**</span></span>](eventschema-eventid-systempropertiestype-element.md)             |                                                             | <span data-ttu-id="5e8e4-119">O identificador que o provedor usou para identificar o evento.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-119">The identifier that the provider used to identify the event.</span></span><br/>                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="5e8e4-120">**EventRecordID**</span><span class="sxs-lookup"><span data-stu-id="5e8e4-120">**EventRecordID**</span></span>](eventschema-eventrecordid-systempropertiestype-element.md) |                                                             | <span data-ttu-id="5e8e4-121">O número de registro atribuído ao evento quando ele foi registrado.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-121">The record number assigned to the event when it was logged.</span></span><br/>                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="5e8e4-122">**Execução**</span><span class="sxs-lookup"><span data-stu-id="5e8e4-122">**Execution**</span></span>](eventschema-execution-systempropertiestype-element.md)         |                                                             | <span data-ttu-id="5e8e4-123">Contém informações sobre o processo e o thread que registrou o evento.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-123">Contains information about the process and thread that logged the event.</span></span><br/>                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="5e8e4-124">**Palavras-chave**</span><span class="sxs-lookup"><span data-stu-id="5e8e4-124">**Keywords**</span></span>](eventschema-keywords-systempropertiestype-element.md)           | [<span data-ttu-id="5e8e4-125">**HexInt64Type**</span><span class="sxs-lookup"><span data-stu-id="5e8e4-125">**HexInt64Type**</span></span>](eventschema-hexint64type-simpletype.md) | <span data-ttu-id="5e8e4-126">Um bitmask das palavras-chave definidas no evento.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-126">A bitmask of the keywords defined in the event.</span></span> <span data-ttu-id="5e8e4-127">As palavras-chave são usadas para classificar tipos de eventos (por exemplo, eventos associados à leitura de dados).</span><span class="sxs-lookup"><span data-stu-id="5e8e4-127">Keywords are used to classify types of events (for example, events associated with reading data).</span></span><br/>                                                                                                                                                                                 |
| [<span data-ttu-id="5e8e4-128">**Geral**</span><span class="sxs-lookup"><span data-stu-id="5e8e4-128">**Level**</span></span>](eventschema-level-systempropertiestype-element.md)                 | <span data-ttu-id="5e8e4-129">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="5e8e4-129">unsignedByte</span></span>                                                | <span data-ttu-id="5e8e4-130">O nível de severidade definido no evento.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-130">The severity level defined in the event.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="5e8e4-131">**Opcode**</span><span class="sxs-lookup"><span data-stu-id="5e8e4-131">**Opcode**</span></span>](eventschema-opcode-systempropertiestype-element.md)               | <span data-ttu-id="5e8e4-132">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="5e8e4-132">unsignedByte</span></span>                                                | <span data-ttu-id="5e8e4-133">O opcode definido no evento.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-133">The opcode defined in the event.</span></span> <span data-ttu-id="5e8e4-134">Task e opcode são typcially usados para identificar o local no aplicativo de onde o evento foi registrado.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-134">Task and opcode are typcially used to identify the location in the application from where the event was logged.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="5e8e4-135">**Provedor**</span><span class="sxs-lookup"><span data-stu-id="5e8e4-135">**Provider**</span></span>](eventschema-provider-systempropertiestype-element.md)           |                                                             | <span data-ttu-id="5e8e4-136">Identifica o provedor que registrou o evento.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-136">Identifies the provider that logged the event.</span></span> <span data-ttu-id="5e8e4-137">Os atributos **Name** e **GUID** serão incluídos se o provedor tiver usado um manifesto de instrumentação para definir seus eventos; caso contrário, o atributo **eventSourceName** será incluído se um provedor de eventos herdado (usando a API de [log de eventos](/windows/desktop/EventLog/event-logging) ) tiver registrado o evento.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-137">The **Name** and **Guid** attributes are included if the provider used an instrumentation manifest to define its events; otherwise, the **EventSourceName** attribute is included if a legacy event provider (using the [Event Logging](/windows/desktop/EventLog/event-logging) API) logged the event.</span></span><br/> |
| [<span data-ttu-id="5e8e4-138">**Segurança**</span><span class="sxs-lookup"><span data-stu-id="5e8e4-138">**Security**</span></span>](eventschema-security-systempropertiestype-element.md)           |                                                             | <span data-ttu-id="5e8e4-139">Identifica o usuário que registrou o evento.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-139">Identifies the user that logged the event.</span></span><br/>                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="5e8e4-140">**Tarefa**</span><span class="sxs-lookup"><span data-stu-id="5e8e4-140">**Task**</span></span>](eventschema-task-systempropertiestype-element.md)                   | <span data-ttu-id="5e8e4-141">unsignedShort</span><span class="sxs-lookup"><span data-stu-id="5e8e4-141">unsignedShort</span></span>                                               | <span data-ttu-id="5e8e4-142">A tarefa definida no evento.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-142">The task defined in the event.</span></span> <span data-ttu-id="5e8e4-143">A tarefa e o opcode são normalmente usados para identificar o local no aplicativo de onde o evento foi registrado.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-143">Task and opcode are typically used to identify the location in the application from where the event was logged.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="5e8e4-144">**TimeCreated**</span><span class="sxs-lookup"><span data-stu-id="5e8e4-144">**TimeCreated**</span></span>](eventschema-timecreated-systempropertiestype-element.md)     |                                                             | <span data-ttu-id="5e8e4-145">O carimbo de data/hora que identifica quando o evento foi registrado.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-145">The time stamp that identifies when the event was logged.</span></span> <span data-ttu-id="5e8e4-146">O carimbo de data/hora incluirá o atributo **SYSTEMTIME** ou o atributo **RawTime** .</span><span class="sxs-lookup"><span data-stu-id="5e8e4-146">The time stamp will include either the **SystemTime** attribute or the **RawTime** attribute.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="5e8e4-147">**Versão**</span><span class="sxs-lookup"><span data-stu-id="5e8e4-147">**Version**</span></span>](schema-version-systempropertiestype-element.md)                  | <span data-ttu-id="5e8e4-148">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="5e8e4-148">unsignedByte</span></span>                                                | <span data-ttu-id="5e8e4-149">O número de versão da definição do evento.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-149">The version number of the event's definition.</span></span><br/>                                                                                                                                                                                                                                                                                     |



## <a name="attributes"></a><span data-ttu-id="5e8e4-150">Atributos</span><span class="sxs-lookup"><span data-stu-id="5e8e4-150">Attributes</span></span>



| <span data-ttu-id="5e8e4-151">Nome</span><span class="sxs-lookup"><span data-stu-id="5e8e4-151">Name</span></span>              | <span data-ttu-id="5e8e4-152">Type</span><span class="sxs-lookup"><span data-stu-id="5e8e4-152">Type</span></span>                                                | <span data-ttu-id="5e8e4-153">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e8e4-153">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e8e4-154">ActivityID</span><span class="sxs-lookup"><span data-stu-id="5e8e4-154">ActivityID</span></span>        | [<span data-ttu-id="5e8e4-155">**GUIDtype**</span><span class="sxs-lookup"><span data-stu-id="5e8e4-155">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="5e8e4-156">Um identificador global exclusivo que identifica a atividade atual.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-156">A globally unique identifier that identifies the current activity.</span></span> <span data-ttu-id="5e8e4-157">Os eventos que são publicados com esse identificador fazem parte da mesma atividade.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-157">The events that are published with this identifier are part of the same activity.</span></span><br/>                                                                                                                                         |
| <span data-ttu-id="5e8e4-158">EventSourcename</span><span class="sxs-lookup"><span data-stu-id="5e8e4-158">EventSourceName</span></span>   | <span data-ttu-id="5e8e4-159">string</span><span class="sxs-lookup"><span data-stu-id="5e8e4-159">string</span></span>                                              | <span data-ttu-id="5e8e4-160">O nome da origem do evento que publicou o evento (se a origem do evento for da API de [log de eventos](/windows/desktop/EventLog/event-logging) herdados).</span><span class="sxs-lookup"><span data-stu-id="5e8e4-160">The name of the event source that published the event (if the event source is from the legacy [Event Logging](/windows/desktop/EventLog/event-logging) API).</span></span><br/>                                                                                                                                                      |
| <span data-ttu-id="5e8e4-161">Guid</span><span class="sxs-lookup"><span data-stu-id="5e8e4-161">Guid</span></span>              | [<span data-ttu-id="5e8e4-162">**GUIDtype**</span><span class="sxs-lookup"><span data-stu-id="5e8e4-162">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="5e8e4-163">O identificador global exclusivo que identifica exclusivamente o provedor.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-163">The globally unique identifier that uniquely identifies the provider.</span></span><br/>                                                                                                                                                                                                                        |
| <span data-ttu-id="5e8e4-164">Kerneltime</span><span class="sxs-lookup"><span data-stu-id="5e8e4-164">KernelTime</span></span>        | <span data-ttu-id="5e8e4-165">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5e8e4-165">unsignedInt</span></span>                                         | <span data-ttu-id="5e8e4-166">Tempo de execução decorrido para instruções do modo kernel, em unidades de tempo de CPU.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-166">Elapsed execution time for kernel-mode instructions, in CPU time units.</span></span> <span data-ttu-id="5e8e4-167">Se você estiver usando uma sessão particular do ETW, use o valor no membro Processortime em vez disso.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-167">If you are using an ETW private session, use the value in the ProcessorTime member instead.</span></span> <span data-ttu-id="5e8e4-168">Disponível somente para eventos registrados em um arquivo de log de rastreamento de eventos (arquivo. ETL).</span><span class="sxs-lookup"><span data-stu-id="5e8e4-168">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                               |
| <span data-ttu-id="5e8e4-169">Nome</span><span class="sxs-lookup"><span data-stu-id="5e8e4-169">Name</span></span>              | <span data-ttu-id="5e8e4-170">anyURI</span><span class="sxs-lookup"><span data-stu-id="5e8e4-170">anyURI</span></span>                                              | <span data-ttu-id="5e8e4-171">O nome do provedor.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-171">The name of the provider.</span></span><br/>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="5e8e4-172">ProcessID</span><span class="sxs-lookup"><span data-stu-id="5e8e4-172">ProcessID</span></span>         | <span data-ttu-id="5e8e4-173">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5e8e4-173">unsignedInt</span></span>                                         | <span data-ttu-id="5e8e4-174">Identifica o processo que gerou o evento.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-174">Identifies the process that generated the event.</span></span><br/>                                                                                                                                                                                                                                             |
| <span data-ttu-id="5e8e4-175">Processador</span><span class="sxs-lookup"><span data-stu-id="5e8e4-175">ProcessorID</span></span>       | <span data-ttu-id="5e8e4-176">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="5e8e4-176">unsignedByte</span></span>                                        | <span data-ttu-id="5e8e4-177">O número de identificação do processador que processou o evento.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-177">The identification number for the processor that processed the event.</span></span> <span data-ttu-id="5e8e4-178">Disponível somente para eventos registrados em um arquivo de log de rastreamento de eventos (arquivo. ETL).</span><span class="sxs-lookup"><span data-stu-id="5e8e4-178">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                                                                                                                             |
| <span data-ttu-id="5e8e4-179">Processadortime</span><span class="sxs-lookup"><span data-stu-id="5e8e4-179">ProcessorTime</span></span>     | <span data-ttu-id="5e8e4-180">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5e8e4-180">unsignedInt</span></span>                                         | <span data-ttu-id="5e8e4-181">Para sessões privadas do ETW, o tempo de execução decorrido para as instruções do modo de usuário, em tiques de CPU.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-181">For ETW private sessions, the elapsed execution time for user-mode instructions, in CPU ticks.</span></span> <span data-ttu-id="5e8e4-182">Disponível somente para eventos registrados em um arquivo de log de rastreamento de eventos (arquivo. ETL).</span><span class="sxs-lookup"><span data-stu-id="5e8e4-182">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                                                                                                    |
| <span data-ttu-id="5e8e4-183">Qualificadores</span><span class="sxs-lookup"><span data-stu-id="5e8e4-183">Qualifiers</span></span>        | <span data-ttu-id="5e8e4-184">**unsignedShort**</span><span class="sxs-lookup"><span data-stu-id="5e8e4-184">**unsignedShort**</span></span>                                   | <span data-ttu-id="5e8e4-185">Um provedor herdado usa um número de 32 bits para identificar seus eventos.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-185">A legacy provider uses a 32-bit number to identify its events.</span></span> <span data-ttu-id="5e8e4-186">Se o evento for registrado por um provedor herdado, o valor do elemento **EventID** conterá os 16 bits de ordem inferior do identificador de evento e o atributo **Qualifier** conterá os 16 bits de ordem superior do identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-186">If the event is logged by a legacy provider, the value of **EventID** element contains the low-order 16 bits of the event identifier and the **Qualifier** attribute contains the high-order 16 bits of the event identifier.</span></span><br/> |
| <span data-ttu-id="5e8e4-187">RawTime</span><span class="sxs-lookup"><span data-stu-id="5e8e4-187">RawTime</span></span>           | <span data-ttu-id="5e8e4-188">unsignedLong</span><span class="sxs-lookup"><span data-stu-id="5e8e4-188">unsignedLong</span></span>                                        | <span data-ttu-id="5e8e4-189">O valor do carimbo de data/hora bruto; o formato do carimbo de data/hora depende da fonte de tempo usada para coletar o rastreamento.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-189">The raw time stamp value; the format of the time stamp depends on the time source used to collect the trace.</span></span> <span data-ttu-id="5e8e4-190">O carimbo de data/hora bruto oferece mais precisão do que o tempo do sistema.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-190">The raw time stamp offers higher precision than system time.</span></span> <span data-ttu-id="5e8e4-191">A saída do evento renderizado só conterá tempo bruto se você usar TraceRpt.exe com a opção-RTS.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-191">The rendered event output will only contain raw time if you use TraceRpt.exe with the -rts switch.</span></span><br/>                 |
| <span data-ttu-id="5e8e4-192">RelatedActivityID</span><span class="sxs-lookup"><span data-stu-id="5e8e4-192">RelatedActivityID</span></span> | [<span data-ttu-id="5e8e4-193">**GUIDtype**</span><span class="sxs-lookup"><span data-stu-id="5e8e4-193">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="5e8e4-194">Um identificador global exclusivo que identifica a atividade para a qual o controle foi transferido.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-194">A globally unique identifier that identifies the activity to which control was transferred to.</span></span> <span data-ttu-id="5e8e4-195">Em seguida, os eventos relacionados teriam esse identificador como seu identificador de ActivityId.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-195">The related events would then have this identifier as their ActivityID identifier.</span></span><br/>                                                                                                            |
| <span data-ttu-id="5e8e4-196">SessionID</span><span class="sxs-lookup"><span data-stu-id="5e8e4-196">SessionID</span></span>         | <span data-ttu-id="5e8e4-197">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5e8e4-197">unsignedInt</span></span>                                         | <span data-ttu-id="5e8e4-198">O número de identificação da sessão do Terminal Server na qual o evento ocorreu.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-198">The identification number for the terminal server session in which the event occurred.</span></span> <span data-ttu-id="5e8e4-199">Disponível somente para eventos registrados em um arquivo de log de rastreamento de eventos (arquivo. ETL).</span><span class="sxs-lookup"><span data-stu-id="5e8e4-199">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                                                                                                            |
| <span data-ttu-id="5e8e4-200">SystemTime</span><span class="sxs-lookup"><span data-stu-id="5e8e4-200">SystemTime</span></span>        | <span data-ttu-id="5e8e4-201">dateTime</span><span class="sxs-lookup"><span data-stu-id="5e8e4-201">dateTime</span></span>                                            | <span data-ttu-id="5e8e4-202">A hora do sistema de quando o evento foi registrado.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-202">The system time of when the event was logged.</span></span><br/>                                                                                                                                                                                                                                                |
| <span data-ttu-id="5e8e4-203">ThreadID</span><span class="sxs-lookup"><span data-stu-id="5e8e4-203">ThreadID</span></span>          | <span data-ttu-id="5e8e4-204">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5e8e4-204">unsignedInt</span></span>                                         | <span data-ttu-id="5e8e4-205">Identifica o thread que gerou o evento.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-205">Identifies the thread that generated the event.</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="5e8e4-206">UserID</span><span class="sxs-lookup"><span data-stu-id="5e8e4-206">UserID</span></span>            | <span data-ttu-id="5e8e4-207">string</span><span class="sxs-lookup"><span data-stu-id="5e8e4-207">string</span></span>                                              | <span data-ttu-id="5e8e4-208">O SID (identificador de segurança) do usuário no formulário de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-208">The security identifier (SID) of the user in string form.</span></span><br/>                                                                                                                                                                                                                                    |
| <span data-ttu-id="5e8e4-209">Usertime</span><span class="sxs-lookup"><span data-stu-id="5e8e4-209">UserTime</span></span>          | <span data-ttu-id="5e8e4-210">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5e8e4-210">unsignedInt</span></span>                                         | <span data-ttu-id="5e8e4-211">Tempo de execução decorrido para instruções do modo de usuário, em unidades de tempo de CPU.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-211">Elapsed execution time for user-mode instructions, in CPU time units.</span></span> <span data-ttu-id="5e8e4-212">Se você estiver usando uma sessão particular do ETW, use o valor no membro Processortime em vez disso.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-212">If you are using an ETW private session, use the value in the ProcessorTime member instead.</span></span> <span data-ttu-id="5e8e4-213">Disponível somente para eventos registrados em um arquivo de log de rastreamento de eventos (arquivo. ETL).</span><span class="sxs-lookup"><span data-stu-id="5e8e4-213">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                                 |



## <a name="remarks"></a><span data-ttu-id="5e8e4-214">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e8e4-214">Remarks</span></span>

<span data-ttu-id="5e8e4-215">Por padrão, o evento contém o FQDN (nome de domínio totalmente qualificado) de um computador.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-215">By default, the event contains the fully qualified domain name (FQDN) of a computer.</span></span> <span data-ttu-id="5e8e4-216">Para usar o nome NETBIOS em vez do FQDN, você deve criar um valor do Registro DWORD chamado CompatFlags na seguinte chave do registro e definir o valor de CompatFlags como 0x2.</span><span class="sxs-lookup"><span data-stu-id="5e8e4-216">To use the NETBIOS name rather than the FQDN, you must create a DWORD registry value named CompatFlags under the following registry key, and set the value of CompatFlags to 0x2.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               WINEVT
```

## <a name="requirements"></a><span data-ttu-id="5e8e4-217">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e8e4-217">Requirements</span></span>



| <span data-ttu-id="5e8e4-218">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e8e4-218">Requirement</span></span> | <span data-ttu-id="5e8e4-219">Valor</span><span class="sxs-lookup"><span data-stu-id="5e8e4-219">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5e8e4-220">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e8e4-220">Minimum supported client</span></span><br/> | <span data-ttu-id="5e8e4-221">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5e8e4-221">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5e8e4-222">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e8e4-222">Minimum supported server</span></span><br/> | <span data-ttu-id="5e8e4-223">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5e8e4-223">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

