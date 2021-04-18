---
title: Elemento opcode (TaskEventDefinitionType)
description: Contém um opcode específico da tarefa para um evento. Todas as definições de opcode são consideradas específicas da tarefa que contém as definições de evento.
ms.assetid: c7192772-401b-4602-918d-0e0bc4b65ca7
keywords:
- EventLog do elemento opcode
topic_type:
- apiref
api_name:
- opcode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d9f3b58353163e1ee5b9abeb04007a4a9d449e5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810608"
---
# <a name="opcode-taskeventdefinitiontype-element"></a><span data-ttu-id="80695-105">Elemento opcode (TaskEventDefinitionType)</span><span class="sxs-lookup"><span data-stu-id="80695-105">opcode (TaskEventDefinitionType) Element</span></span>

<span data-ttu-id="80695-106">\[A partir do compilador de mensagens fornecido com a versão do Windows 7 do SDK do Windows, esse elemento não estará mais disponível.\]</span><span class="sxs-lookup"><span data-stu-id="80695-106">\[Beginning with the message compiler that ships with the Windows 7 version of the Windows SDK, this element is no longer available.\]</span></span>

<span data-ttu-id="80695-107">Contém um opcode específico da tarefa para um evento.</span><span class="sxs-lookup"><span data-stu-id="80695-107">Contains a task-specific opcode for an event.</span></span> <span data-ttu-id="80695-108">Todas as definições de opcode são consideradas específicas da tarefa que contém as definições de evento.</span><span class="sxs-lookup"><span data-stu-id="80695-108">All of the opcode definitions are assumed to be task-specific for the task that contains the event definitions.</span></span>

``` syntax
<xs:element name="opcode">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="event"
                type="EventDefinitionType"
                maxOccurs="unbounded"
             />
        </xs:sequence>
        <xs:attribute name="name"
            type="QName"
            use="required"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="80695-109">O elemento **opcode** é definido pelo tipo complexo [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="80695-109">The **opcode** element is defined by the [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="80695-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="80695-110">Child elements</span></span>



| <span data-ttu-id="80695-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="80695-111">Element</span></span>                                                   | <span data-ttu-id="80695-112">Type</span><span class="sxs-lookup"><span data-stu-id="80695-112">Type</span></span>                                                                               | <span data-ttu-id="80695-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="80695-113">Description</span></span>                                        |
|-----------------------------------------------------------|------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="80695-114">**circunstância**</span><span class="sxs-lookup"><span data-stu-id="80695-114">**event**</span></span>](eventmanifestschema-event-opcode-element.md) | [<span data-ttu-id="80695-115">**EventDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="80695-115">**EventDefinitionType**</span></span>](eventmanifestschema-eventdefinitiontype-complextype.md) | <span data-ttu-id="80695-116">Um evento que é publicado com uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="80695-116">An event that is published with a task.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="80695-117">Atributos</span><span class="sxs-lookup"><span data-stu-id="80695-117">Attributes</span></span>



| <span data-ttu-id="80695-118">Nome</span><span class="sxs-lookup"><span data-stu-id="80695-118">Name</span></span> | <span data-ttu-id="80695-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="80695-119">Type</span></span>      | <span data-ttu-id="80695-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="80695-120">Description</span></span>                                      |
|------|-----------|--------------------------------------------------|
| <span data-ttu-id="80695-121">name</span><span class="sxs-lookup"><span data-stu-id="80695-121">name</span></span> | <span data-ttu-id="80695-122">**QName**</span><span class="sxs-lookup"><span data-stu-id="80695-122">**QName**</span></span> | <span data-ttu-id="80695-123">O nome do opcode específico da tarefa.</span><span class="sxs-lookup"><span data-stu-id="80695-123">The name of the task-specific opcode.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="80695-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80695-124">Requirements</span></span>



| <span data-ttu-id="80695-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="80695-125">Requirement</span></span> | <span data-ttu-id="80695-126">Valor</span><span class="sxs-lookup"><span data-stu-id="80695-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="80695-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80695-127">Minimum supported client</span></span><br/> | <span data-ttu-id="80695-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="80695-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="80695-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80695-129">Minimum supported server</span></span><br/> | <span data-ttu-id="80695-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="80695-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="80695-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="80695-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="80695-132">**Elemento pai**</span><span class="sxs-lookup"><span data-stu-id="80695-132">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="80695-133">**tarefa (Definitiontype)**</span><span class="sxs-lookup"><span data-stu-id="80695-133">**task (DefinitionType)**</span></span>](eventmanifestschema-task-definitiontype-element.md)
</dt> </dl>

 

 





