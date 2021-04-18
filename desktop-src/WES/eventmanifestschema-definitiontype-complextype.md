---
title: Tipo complexo definitiontype
description: Define uma lista de eventos que seu provedor pode registrar.
ms.assetid: 6d401ced-be1a-409a-8f4d-2d977a33ff8d
keywords:
- EventLog de tipo complexo de definitiontype
topic_type:
- apiref
api_name:
- DefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 82fbf7ec7db6f64f1bac9776376fa8fe89659d9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105800196"
---
# <a name="definitiontype-complex-type"></a><span data-ttu-id="cb19b-104">Tipo complexo definitiontype</span><span class="sxs-lookup"><span data-stu-id="cb19b-104">DefinitionType Complex Type</span></span>

<span data-ttu-id="cb19b-105">Define uma lista de eventos que seu provedor pode registrar.</span><span class="sxs-lookup"><span data-stu-id="cb19b-105">Defines a list of events that your provider can log.</span></span>

``` syntax
<xs:complexType name="DefinitionType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="event"
            type="EventDefinitionType"
         />
        <xs:element name="task"
            type="TaskEventDefinitionType"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="cb19b-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="cb19b-106">Child elements</span></span>



| <span data-ttu-id="cb19b-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="cb19b-107">Element</span></span>                                                           | <span data-ttu-id="cb19b-108">Type</span><span class="sxs-lookup"><span data-stu-id="cb19b-108">Type</span></span>                                                                                       | <span data-ttu-id="cb19b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="cb19b-109">Description</span></span>                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb19b-110">**circunstância**</span><span class="sxs-lookup"><span data-stu-id="cb19b-110">**event**</span></span>](eventmanifestschema-event-definitiontype-element.md) | [<span data-ttu-id="cb19b-111">**EventDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="cb19b-111">**EventDefinitionType**</span></span>](eventmanifestschema-eventdefinitiontype-complextype.md)         | <span data-ttu-id="cb19b-112">Define um evento que seu provedor pode registrar.</span><span class="sxs-lookup"><span data-stu-id="cb19b-112">Defines an event that your provider can log.</span></span><br/>                                                                                                                                                                                                                                 |
| [<span data-ttu-id="cb19b-113">**agenda**</span><span class="sxs-lookup"><span data-stu-id="cb19b-113">**task**</span></span>](eventmanifestschema-task-definitiontype-element.md)   | [<span data-ttu-id="cb19b-114">**TaskEventDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="cb19b-114">**TaskEventDefinitionType**</span></span>](eventmanifestschema-taskeventdefinitiontype-complextype.md) | <span data-ttu-id="cb19b-115">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="cb19b-115">Not supported.</span></span><br/> <span data-ttu-id="cb19b-116">**Windows Server 2008 e Windows Vista:** Define um evento específico de tarefa que seu provedor pode registrar.</span><span class="sxs-lookup"><span data-stu-id="cb19b-116">**Windows Server 2008 and Windows Vista:** Defines a task-specific event that your provider can log.</span></span> <span data-ttu-id="cb19b-117">(Começando com o compilador de mensagem que acompanha a versão do Windows 7 do SDK do Windows, não há mais suporte para eventos específicos da tarefa.)</span><span class="sxs-lookup"><span data-stu-id="cb19b-117">(Beginning with the message compiler that ships with the Windows 7 version of the Windows SDK, task-specific events are no longer supported.)</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="cb19b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb19b-118">Requirements</span></span>



| <span data-ttu-id="cb19b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb19b-119">Requirement</span></span> | <span data-ttu-id="cb19b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="cb19b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cb19b-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb19b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cb19b-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cb19b-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cb19b-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb19b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cb19b-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cb19b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





