---
title: Tipo complexo do EventType
description: Define o nó raiz do esquema de evento.
ms.assetid: 1ff9299b-71ee-4bb3-8a9a-fb9880dbf577
keywords:
- Log de eventos do tipo complexo do EventType
topic_type:
- apiref
api_name:
- EventType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1103570b6c1d9f51a8cbe8fe5628460690fb32cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369290"
---
# <a name="eventtype-complex-type"></a><span data-ttu-id="1d1b6-104">Tipo complexo do EventType</span><span class="sxs-lookup"><span data-stu-id="1d1b6-104">EventType Complex Type</span></span>

<span data-ttu-id="1d1b6-105">Define o nó raiz do esquema de evento.</span><span class="sxs-lookup"><span data-stu-id="1d1b6-105">Defines the root node of the Event schema.</span></span>

``` syntax
<xs:complexType name="EventType">
    <xs:sequence>
        <xs:element name="System"
            type="SystemPropertiesType"
         />
        <xs:choice>
            <xs:element name="EventData"
                type="EventDataType"
                minOccurs="0"
             />
            <xs:element name="UserData"
                type="UserDataType"
                minOccurs="0"
             />
            <xs:element name="DebugData"
                type="DebugDataType"
                minOccurs="0"
             />
            <xs:element name="BinaryEventData"
                type="hexBinary"
                minOccurs="0"
             />
            <xs:element name="ProcessingErrorData"
                type="ProcessingErrorDataType"
                minOccurs="0"
             />
        </xs:choice>
        <xs:element name="RenderingInfo"
            type="RenderingInfoType"
            minOccurs="0"
         />
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="1d1b6-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1d1b6-106">Child elements</span></span>



| <span data-ttu-id="1d1b6-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="1d1b6-107">Element</span></span>                                                                          | <span data-ttu-id="1d1b6-108">Type</span><span class="sxs-lookup"><span data-stu-id="1d1b6-108">Type</span></span>                                                                               | <span data-ttu-id="1d1b6-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="1d1b6-109">Description</span></span>                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1d1b6-110">**BinaryEventData**</span><span class="sxs-lookup"><span data-stu-id="1d1b6-110">**BinaryEventData**</span></span>](eventschema-binaryeventdata-eventtype-element.md)         | <span data-ttu-id="1d1b6-111">hexBinary</span><span class="sxs-lookup"><span data-stu-id="1d1b6-111">hexBinary</span></span>                                                                          | <span data-ttu-id="1d1b6-112">Contém os dados de evento como um blob binário.</span><span class="sxs-lookup"><span data-stu-id="1d1b6-112">Contains the event data as a binary blob.</span></span> <span data-ttu-id="1d1b6-113">Os dados do evento são renderizados como um blob binário se a função de renderização não puder localizar os metadados usados para decodificar o evento.</span><span class="sxs-lookup"><span data-stu-id="1d1b6-113">The event data is rendered as a binary blob if the rendering function cannot find the metadata used to decode the event.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="1d1b6-114">**DebugData**</span><span class="sxs-lookup"><span data-stu-id="1d1b6-114">**DebugData**</span></span>](eventschema-debugdata-eventtype-element.md)                     | [<span data-ttu-id="1d1b6-115">**DebugDataType**</span><span class="sxs-lookup"><span data-stu-id="1d1b6-115">**DebugDataType**</span></span>](eventschema-debugdatatype-complextype.md)                     | <span data-ttu-id="1d1b6-116">Contém os dados que podem ser registrados para eventos de pré-processamento (pré-processador de rastreamento de software) do Windows.</span><span class="sxs-lookup"><span data-stu-id="1d1b6-116">Contains the data that can be logged for Windows software trace preprocessor (WPP) events.</span></span><br/>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="1d1b6-117">**EventData**</span><span class="sxs-lookup"><span data-stu-id="1d1b6-117">**EventData**</span></span>](eventschema-eventdata-eventtype-element.md)                     | [<span data-ttu-id="1d1b6-118">**EventDataType**</span><span class="sxs-lookup"><span data-stu-id="1d1b6-118">**EventDataType**</span></span>](eventschema-eventdatatype-complextype.md)                     | <span data-ttu-id="1d1b6-119">Contém os dados do evento.</span><span class="sxs-lookup"><span data-stu-id="1d1b6-119">Contains the event data.</span></span> <span data-ttu-id="1d1b6-120">A ordem dos itens de dados no modelo determina o layout dos dados do evento.</span><span class="sxs-lookup"><span data-stu-id="1d1b6-120">The order of the data items in the template determines the layout of the event data.</span></span><br/>                                                                                                                                                                                                                 |
| [<span data-ttu-id="1d1b6-121">**ProcessingErrorData**</span><span class="sxs-lookup"><span data-stu-id="1d1b6-121">**ProcessingErrorData**</span></span>](eventschema-processingerrordata-eventtype-element.md) | [<span data-ttu-id="1d1b6-122">**ProcessingErrorDataType**</span><span class="sxs-lookup"><span data-stu-id="1d1b6-122">**ProcessingErrorDataType**</span></span>](eventschema-processingerrordatatype-complextype.md) | <span data-ttu-id="1d1b6-123">Contém detalhes do erro que ocorreu ao tentar renderizar o evento.</span><span class="sxs-lookup"><span data-stu-id="1d1b6-123">Contains details of the error that occurred while trying to render the event.</span></span> <span data-ttu-id="1d1b6-124">Isso pode ocorrer se os dados do evento não corresponderem à definição de dados do evento no manifesto.</span><span class="sxs-lookup"><span data-stu-id="1d1b6-124">This can occur if the event data does not match the event data definition in the manifest.</span></span> <span data-ttu-id="1d1b6-125">Os dados do evento são incluídos como um blob binário.</span><span class="sxs-lookup"><span data-stu-id="1d1b6-125">The event data is included as a binary blob.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="1d1b6-126">**RenderingInfo**</span><span class="sxs-lookup"><span data-stu-id="1d1b6-126">**RenderingInfo**</span></span>](eventschema-renderinginfo-eventtype-element.md)             | [<span data-ttu-id="1d1b6-127">**RenderingInfoType**</span><span class="sxs-lookup"><span data-stu-id="1d1b6-127">**RenderingInfoType**</span></span>](eventschema-renderingtype-complextype.md)                 | <span data-ttu-id="1d1b6-128">Contém as cadeias de caracteres de mensagem renderizadas para o evento (inclui a cadeia de mensagem do evento e as cadeias de mensagens para qualquer uma das propriedades do evento, como nível, tarefa e opcode).</span><span class="sxs-lookup"><span data-stu-id="1d1b6-128">Contains the rendered message strings for the event (includes the event's message string and the message strings for any of the event's properties such as level, task, and opcode).</span></span> <span data-ttu-id="1d1b6-129">Somente os eventos que foram coletados usando o serviço [coletor de eventos do Windows](/windows/desktop/WEC/windows-event-collector) conterão esta seção.</span><span class="sxs-lookup"><span data-stu-id="1d1b6-129">Only events that have been collected using the [Windows Event Collector](/windows/desktop/WEC/windows-event-collector) service will contain this section.</span></span><br/> |
| [<span data-ttu-id="1d1b6-130">**Sistema**</span><span class="sxs-lookup"><span data-stu-id="1d1b6-130">**System**</span></span>](eventschema-system-eventtype-element.md)                           | [<span data-ttu-id="1d1b6-131">**SystemPropertiesType**</span><span class="sxs-lookup"><span data-stu-id="1d1b6-131">**SystemPropertiesType**</span></span>](eventschema-systempropertiestype-complextype.md)       | <span data-ttu-id="1d1b6-132">Contém informações que identificam o provedor e como ele foi habilitado, o evento, o canal no qual o evento foi gravado e informações do sistema, como as IDs de processo e thread.</span><span class="sxs-lookup"><span data-stu-id="1d1b6-132">Contains information that identifies the provider and how it was enabled, the event, the channel to which the event was written, and system information such as the process and thread IDs.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="1d1b6-133">**UserData**</span><span class="sxs-lookup"><span data-stu-id="1d1b6-133">**UserData**</span></span>](eventschema-userdata-eventtype-element.md)                       | [<span data-ttu-id="1d1b6-134">**UserDataType**</span><span class="sxs-lookup"><span data-stu-id="1d1b6-134">**UserDataType**</span></span>](eventschema-userdatatype-complextype.md)                       | <span data-ttu-id="1d1b6-135">Contém os dados do evento.</span><span class="sxs-lookup"><span data-stu-id="1d1b6-135">Contains the event data.</span></span> <span data-ttu-id="1d1b6-136">A seção de dados do usuário do modelo determina o layout dos dados do evento.</span><span class="sxs-lookup"><span data-stu-id="1d1b6-136">The user data section of the template determines the layout of the event data.</span></span><br/>                                                                                                                                                                                                                       |



## <a name="remarks"></a><span data-ttu-id="1d1b6-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d1b6-137">Remarks</span></span>

<span data-ttu-id="1d1b6-138">Normalmente, esta seção conterá com a seção **EVENTDATA** ou **UserData** .</span><span class="sxs-lookup"><span data-stu-id="1d1b6-138">Typically, this section will contain with the **EventData** or **UserData** section.</span></span> <span data-ttu-id="1d1b6-139">A seção **EVENTDATA** será usada se o modelo não contiver uma seção **UserData** .</span><span class="sxs-lookup"><span data-stu-id="1d1b6-139">The **EventData** section is used if the template does not contain a **UserData** section.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d1b6-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d1b6-140">Requirements</span></span>



| <span data-ttu-id="1d1b6-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d1b6-141">Requirement</span></span> | <span data-ttu-id="1d1b6-142">Valor</span><span class="sxs-lookup"><span data-stu-id="1d1b6-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1d1b6-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d1b6-143">Minimum supported client</span></span><br/> | <span data-ttu-id="1d1b6-144">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1d1b6-144">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1d1b6-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d1b6-145">Minimum supported server</span></span><br/> | <span data-ttu-id="1d1b6-146">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1d1b6-146">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

