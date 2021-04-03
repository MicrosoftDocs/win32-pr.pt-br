---
title: Tipo complexo EventDataType
description: Define os itens de dados do evento e as estruturas que contêm os dados do evento.
ms.assetid: 9531163f-34ce-4673-b2d8-636042915c73
keywords:
- Log de eventos do tipo complexo EventDataType
topic_type:
- apiref
api_name:
- EventDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a93695db477ebb0c7b5652419198f8f5c6370dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644368"
---
# <a name="eventdatatype-complex-type"></a><span data-ttu-id="5b03a-104">Tipo complexo EventDataType</span><span class="sxs-lookup"><span data-stu-id="5b03a-104">EventDataType Complex Type</span></span>

<span data-ttu-id="5b03a-105">Define os itens de dados do evento e as estruturas que contêm os dados do evento.</span><span class="sxs-lookup"><span data-stu-id="5b03a-105">Defines the event data items and structures that contains the event data.</span></span>

``` syntax
<xs:complexType name="EventDataType">
    <xs:sequence>
        <xs:choice
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:element name="Data"
                type="DataType"
             />
            <xs:element name="ComplexData"
                type="ComplexDataType"
             />
        </xs:choice>
        <xs:element name="Binary"
            type="hexBinary"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="Name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="5b03a-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5b03a-106">Child elements</span></span>



| <span data-ttu-id="5b03a-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="5b03a-107">Element</span></span>                                                              | <span data-ttu-id="5b03a-108">Type</span><span class="sxs-lookup"><span data-stu-id="5b03a-108">Type</span></span>                                                               | <span data-ttu-id="5b03a-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="5b03a-109">Description</span></span>                                                                                          |
|----------------------------------------------------------------------|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5b03a-110">**Binário**</span><span class="sxs-lookup"><span data-stu-id="5b03a-110">**Binary**</span></span>](eventschema-binary-eventdatatype-element.md)           | <span data-ttu-id="5b03a-111">hexBinary</span><span class="sxs-lookup"><span data-stu-id="5b03a-111">hexBinary</span></span>                                                          | <span data-ttu-id="5b03a-112">Um blob de dados binários para eventos que são gravados usando o [log de eventos](/windows/desktop/EventLog/event-logging).</span><span class="sxs-lookup"><span data-stu-id="5b03a-112">A binary data blob for events that are written using [Event Logging](/windows/desktop/EventLog/event-logging).</span></span><br/> |
| [<span data-ttu-id="5b03a-113">**ComplexData**</span><span class="sxs-lookup"><span data-stu-id="5b03a-113">**ComplexData**</span></span>](eventschema-complexdata-eventdatatype-element.md) | [<span data-ttu-id="5b03a-114">**ComplexDataType**</span><span class="sxs-lookup"><span data-stu-id="5b03a-114">**ComplexDataType**</span></span>](eventschema-complexdatatype-complextype.md) | <span data-ttu-id="5b03a-115">Uma estrutura que é definida no modelo para o evento.</span><span class="sxs-lookup"><span data-stu-id="5b03a-115">A structure that is defined in the template for the event.</span></span><br/>                                |
| [<span data-ttu-id="5b03a-116">**Dados**</span><span class="sxs-lookup"><span data-stu-id="5b03a-116">**Data**</span></span>](eventschema-data-eventdatatype-element.md)               | [<span data-ttu-id="5b03a-117">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="5b03a-117">**DataType**</span></span>](eventschema-datafieldtype-complextype.md)          | <span data-ttu-id="5b03a-118">Um item de dados de nível superior que é definido no modelo para o evento.</span><span class="sxs-lookup"><span data-stu-id="5b03a-118">A top-level data item that is defined in the template for the event.</span></span><br/>                      |



## <a name="attributes"></a><span data-ttu-id="5b03a-119">Atributos</span><span class="sxs-lookup"><span data-stu-id="5b03a-119">Attributes</span></span>



| <span data-ttu-id="5b03a-120">Nome</span><span class="sxs-lookup"><span data-stu-id="5b03a-120">Name</span></span> | <span data-ttu-id="5b03a-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="5b03a-121">Type</span></span>   | <span data-ttu-id="5b03a-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="5b03a-122">Description</span></span>                                                       |
|------|--------|-------------------------------------------------------------------|
| <span data-ttu-id="5b03a-123">Nome</span><span class="sxs-lookup"><span data-stu-id="5b03a-123">Name</span></span> | <span data-ttu-id="5b03a-124">cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="5b03a-124">string</span></span> | <span data-ttu-id="5b03a-125">O nome do modelo que contém os itens de dados.</span><span class="sxs-lookup"><span data-stu-id="5b03a-125">The name of the template that contains the data items.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5b03a-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b03a-126">Remarks</span></span>

<span data-ttu-id="5b03a-127">A função [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) renderiza matrizes e estruturas como blobs binários.</span><span class="sxs-lookup"><span data-stu-id="5b03a-127">The [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) function renders arrays and structures as binary blobs.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b03a-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b03a-128">Requirements</span></span>



| <span data-ttu-id="5b03a-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b03a-129">Requirement</span></span> | <span data-ttu-id="5b03a-130">Valor</span><span class="sxs-lookup"><span data-stu-id="5b03a-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5b03a-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b03a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5b03a-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5b03a-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5b03a-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b03a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5b03a-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5b03a-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

