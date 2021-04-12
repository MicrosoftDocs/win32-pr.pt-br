---
title: Tipo complexo RenderingInfoType
description: Define as mensagens renderizadas para o evento.
ms.assetid: 85a4cfc6-6277-4af8-af4e-cae3bd3aac13
keywords:
- Log de eventos do tipo complexo RenderingInfoType
topic_type:
- apiref
api_name:
- RenderingInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d0e4224ec9b90e84cbacbf5ede852763edd8e4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455838"
---
# <a name="renderinginfotype-complex-type"></a><span data-ttu-id="ec830-104">Tipo complexo RenderingInfoType</span><span class="sxs-lookup"><span data-stu-id="ec830-104">RenderingInfoType Complex Type</span></span>

<span data-ttu-id="ec830-105">Define as mensagens renderizadas para o evento.</span><span class="sxs-lookup"><span data-stu-id="ec830-105">Defines the rendered messages for the event.</span></span>

``` syntax
<xs:complexType name="RenderingInfoType">
    <xs:sequence>
        <xs:element name="Message"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Level"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Opcode"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Task"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Channel"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Provider"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Keywords"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="Keyword"
                        type="string"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
            namespace="##other"
         />
    </xs:sequence>
    <xs:attribute name="Culture"
        type="language"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="ec830-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ec830-106">Child elements</span></span>



| <span data-ttu-id="ec830-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="ec830-107">Element</span></span>                                                             | <span data-ttu-id="ec830-108">Type</span><span class="sxs-lookup"><span data-stu-id="ec830-108">Type</span></span>   | <span data-ttu-id="ec830-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="ec830-109">Description</span></span>                                                                   |
|---------------------------------------------------------------------|--------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="ec830-110">**Canal**</span><span class="sxs-lookup"><span data-stu-id="ec830-110">**Channel**</span></span>](eventschema-task-renderingtype-element.md)           | <span data-ttu-id="ec830-111">string</span><span class="sxs-lookup"><span data-stu-id="ec830-111">string</span></span> | <span data-ttu-id="ec830-112">A cadeia de caracteres de mensagem renderizada do canal especificado no evento.</span><span class="sxs-lookup"><span data-stu-id="ec830-112">The rendered message string of the channel specified in the event.</span></span><br/> |
| [<span data-ttu-id="ec830-113">**Palavra-chave**</span><span class="sxs-lookup"><span data-stu-id="ec830-113">**Keyword**</span></span>](eventschema-keyword-keywords-element.md)             | <span data-ttu-id="ec830-114">string</span><span class="sxs-lookup"><span data-stu-id="ec830-114">string</span></span> | <span data-ttu-id="ec830-115">A cadeia de caracteres de mensagem renderizada de uma palavra-chave especificada no evento.</span><span class="sxs-lookup"><span data-stu-id="ec830-115">The rendered message string of a keyword specified in the event.</span></span><br/>   |
| [<span data-ttu-id="ec830-116">**Palavras-chave**</span><span class="sxs-lookup"><span data-stu-id="ec830-116">**Keywords**</span></span>](eventschema-keywords-renderingtype-element.md)      |        | <span data-ttu-id="ec830-117">Uma lista de palavras-chave renderizadas.</span><span class="sxs-lookup"><span data-stu-id="ec830-117">A list of rendered keywords.</span></span><br/>                                       |
| [<span data-ttu-id="ec830-118">**Geral**</span><span class="sxs-lookup"><span data-stu-id="ec830-118">**Level**</span></span>](eventschema-level-renderingtype-element.md)            | <span data-ttu-id="ec830-119">string</span><span class="sxs-lookup"><span data-stu-id="ec830-119">string</span></span> | <span data-ttu-id="ec830-120">A cadeia de caracteres de mensagem renderizada do nível especificado no evento.</span><span class="sxs-lookup"><span data-stu-id="ec830-120">The rendered message string of the level specified in the event.</span></span><br/>   |
| [<span data-ttu-id="ec830-121">**Mensagem**</span><span class="sxs-lookup"><span data-stu-id="ec830-121">**Message**</span></span>](eventschema-message-renderingtype-element.md)        | <span data-ttu-id="ec830-122">string</span><span class="sxs-lookup"><span data-stu-id="ec830-122">string</span></span> | <span data-ttu-id="ec830-123">A cadeia de caracteres de mensagem renderizada do evento.</span><span class="sxs-lookup"><span data-stu-id="ec830-123">The rendered message string of the event.</span></span><br/>                          |
| [<span data-ttu-id="ec830-124">**Opcode**</span><span class="sxs-lookup"><span data-stu-id="ec830-124">**Opcode**</span></span>](eventschema-opcode-renderingtype-element.md)          | <span data-ttu-id="ec830-125">string</span><span class="sxs-lookup"><span data-stu-id="ec830-125">string</span></span> | <span data-ttu-id="ec830-126">A cadeia de caracteres de mensagem renderizada do opcode especificado no evento.</span><span class="sxs-lookup"><span data-stu-id="ec830-126">The rendered message string of the opcode specified in the event.</span></span><br/>  |
| [<span data-ttu-id="ec830-127">**Provedor**</span><span class="sxs-lookup"><span data-stu-id="ec830-127">**Provider**</span></span>](eventschema-publisher-renderinginfotype-element.md) | <span data-ttu-id="ec830-128">string</span><span class="sxs-lookup"><span data-stu-id="ec830-128">string</span></span> | <span data-ttu-id="ec830-129">A cadeia de caracteres de mensagem renderizada para o provedor.</span><span class="sxs-lookup"><span data-stu-id="ec830-129">The rendered message string for the provider.</span></span><br/>                      |
| [<span data-ttu-id="ec830-130">**Tarefa**</span><span class="sxs-lookup"><span data-stu-id="ec830-130">**Task**</span></span>](eventschema-task-renderingtype-element.md)              | <span data-ttu-id="ec830-131">string</span><span class="sxs-lookup"><span data-stu-id="ec830-131">string</span></span> | <span data-ttu-id="ec830-132">A cadeia de caracteres de mensagem renderizada da tarefa especificada no evento.</span><span class="sxs-lookup"><span data-stu-id="ec830-132">The rendered message string of the task specified in the event.</span></span><br/>    |



## <a name="attributes"></a><span data-ttu-id="ec830-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="ec830-133">Attributes</span></span>



| <span data-ttu-id="ec830-134">Nome</span><span class="sxs-lookup"><span data-stu-id="ec830-134">Name</span></span>    | <span data-ttu-id="ec830-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="ec830-135">Type</span></span>     | <span data-ttu-id="ec830-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="ec830-136">Description</span></span>                                                                                                      |
|---------|----------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec830-137">Cultura</span><span class="sxs-lookup"><span data-stu-id="ec830-137">Culture</span></span> | <span data-ttu-id="ec830-138">Linguagem</span><span class="sxs-lookup"><span data-stu-id="ec830-138">language</span></span> | <span data-ttu-id="ec830-139">O nome do idioma (por exemplo, en-US) que identifica a localidade usada para renderizar as cadeias de caracteres de mensagem.</span><span class="sxs-lookup"><span data-stu-id="ec830-139">The language name (for example, en-US) that identifies the locale used to render the message strings.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ec830-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec830-140">Remarks</span></span>

<span data-ttu-id="ec830-141">Somente os eventos que foram coletados usando o serviço [coletor de eventos do Windows](/windows/desktop/WEC/windows-event-collector) conterão esta seção.</span><span class="sxs-lookup"><span data-stu-id="ec830-141">Only events that have been collected using the [Windows Event Collector](/windows/desktop/WEC/windows-event-collector) service will contain this section.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec830-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec830-142">Requirements</span></span>



| <span data-ttu-id="ec830-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec830-143">Requirement</span></span> | <span data-ttu-id="ec830-144">Valor</span><span class="sxs-lookup"><span data-stu-id="ec830-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ec830-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec830-145">Minimum supported client</span></span><br/> | <span data-ttu-id="ec830-146">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ec830-146">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ec830-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec830-147">Minimum supported server</span></span><br/> | <span data-ttu-id="ec830-148">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ec830-148">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

