---
title: Tipo complexo TaskEventDefinitionType
description: Define um evento específico de tarefa que seu provedor pode registrar. | Tipo complexo TaskEventDefinitionType
ms.assetid: f0329728-e7b5-4161-a30f-78b81a7b6812
keywords:
- Log de eventos do tipo complexo TaskEventDefinitionType
topic_type:
- apiref
api_name:
- TaskEventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2ebf752dbaf97ceced84b6bd9698faf7b191c07e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105794543"
---
# <a name="taskeventdefinitiontype-complex-type"></a><span data-ttu-id="77281-105">Tipo complexo TaskEventDefinitionType</span><span class="sxs-lookup"><span data-stu-id="77281-105">TaskEventDefinitionType Complex Type</span></span>

<span data-ttu-id="77281-106">\[Começando com o compilador de mensagem que acompanha a versão do Windows 7 do SDK do Windows, o tipo complexo TaskEventDefinitionType não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="77281-106">\[Beginning with the message compiler that ships with the Windows 7 version of the Windows SDK, the TaskEventDefinitionType complex type is no longer available.</span></span> <span data-ttu-id="77281-107">Em vez disso, use opcodes específicos da tarefa para fornecer a mesma funcionalidade.\]</span><span class="sxs-lookup"><span data-stu-id="77281-107">Instead use task-specific opcodes to provide the same functionality.\]</span></span>

<span data-ttu-id="77281-108">Define um evento específico de tarefa que seu provedor pode registrar.</span><span class="sxs-lookup"><span data-stu-id="77281-108">Defines a task-specific event that your provider can log.</span></span>

``` syntax
<xs:complexType name="TaskEventDefinitionType">
    <xs:sequence>
        <xs:element name="opcode"
            maxOccurs="unbounded"
        >
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
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="77281-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="77281-109">Child elements</span></span>



| <span data-ttu-id="77281-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="77281-110">Element</span></span>                                                                      | <span data-ttu-id="77281-111">Type</span><span class="sxs-lookup"><span data-stu-id="77281-111">Type</span></span>                                                                               | <span data-ttu-id="77281-112">Description</span><span class="sxs-lookup"><span data-stu-id="77281-112">Description</span></span>                                             |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="77281-113">**event**</span><span class="sxs-lookup"><span data-stu-id="77281-113">**event**</span></span>                                                                    | [<span data-ttu-id="77281-114">**EventDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="77281-114">**EventDefinitionType**</span></span>](eventmanifestschema-eventdefinitiontype-complextype.md) | <span data-ttu-id="77281-115">Um evento específico da tarefa publicado com uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="77281-115">A task-specific event published with a task.</span></span><br/> |
| [<span data-ttu-id="77281-116">**opcode**</span><span class="sxs-lookup"><span data-stu-id="77281-116">**opcode**</span></span>](eventmanifestschema-opcode-taskeventdefinitiontype-element.md) |                                                                                    | <span data-ttu-id="77281-117">Um opcode específico da tarefa que para um evento.</span><span class="sxs-lookup"><span data-stu-id="77281-117">A task-specific opcode that for an event.</span></span> <br/>   |



## <a name="attributes"></a><span data-ttu-id="77281-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="77281-118">Attributes</span></span>



| <span data-ttu-id="77281-119">Nome</span><span class="sxs-lookup"><span data-stu-id="77281-119">Name</span></span> | <span data-ttu-id="77281-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="77281-120">Type</span></span>      | <span data-ttu-id="77281-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="77281-121">Description</span></span>                                      |
|------|-----------|--------------------------------------------------|
| <span data-ttu-id="77281-122">name</span><span class="sxs-lookup"><span data-stu-id="77281-122">name</span></span> | <span data-ttu-id="77281-123">**QName**</span><span class="sxs-lookup"><span data-stu-id="77281-123">**QName**</span></span> | <span data-ttu-id="77281-124">O nome do opcode específico da tarefa.</span><span class="sxs-lookup"><span data-stu-id="77281-124">The name of the task-specific opcode.</span></span><br/> |
| <span data-ttu-id="77281-125">name</span><span class="sxs-lookup"><span data-stu-id="77281-125">name</span></span> | <span data-ttu-id="77281-126">anyURI</span><span class="sxs-lookup"><span data-stu-id="77281-126">anyURI</span></span>    | <span data-ttu-id="77281-127">O nome da tarefa.</span><span class="sxs-lookup"><span data-stu-id="77281-127">The name of the task.</span></span><br/>                 |



## <a name="requirements"></a><span data-ttu-id="77281-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77281-128">Requirements</span></span>



| <span data-ttu-id="77281-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="77281-129">Requirement</span></span> | <span data-ttu-id="77281-130">Valor</span><span class="sxs-lookup"><span data-stu-id="77281-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="77281-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77281-131">Minimum supported client</span></span><br/> | <span data-ttu-id="77281-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="77281-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="77281-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77281-133">Minimum supported server</span></span><br/> | <span data-ttu-id="77281-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="77281-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





