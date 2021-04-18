---
title: Elemento binary (TemplateItemType)
description: Contém os dados binários fornecidos pela API do log de eventos.
ms.assetid: 3ad9c119-9395-49d3-b920-9a071bcc6a04
keywords:
- elemento Binary EventLog
topic_type:
- apiref
api_name:
- binary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c3e281da662b4cdd0ecacc81a88f1a5728f90da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105763141"
---
# <a name="binary-templateitemtype-element"></a><span data-ttu-id="69812-104">Elemento binary (TemplateItemType)</span><span class="sxs-lookup"><span data-stu-id="69812-104">binary (TemplateItemType) Element</span></span>

<span data-ttu-id="69812-105">Contém os dados binários fornecidos pela API do [log de eventos](/windows/desktop/EventLog/event-logging) .</span><span class="sxs-lookup"><span data-stu-id="69812-105">Contains the binary data that is supplied by the [Event Log](/windows/desktop/EventLog/event-logging) API.</span></span>

``` syntax
<xs:element name="binary">
    <xs:complexType>
        <xs:attribute name="name"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="69812-106">O elemento **Binary** é definido pelo tipo complexo [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="69812-106">The **binary** element is defined by the [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="69812-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="69812-107">Attributes</span></span>



| <span data-ttu-id="69812-108">Nome</span><span class="sxs-lookup"><span data-stu-id="69812-108">Name</span></span> | <span data-ttu-id="69812-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="69812-109">Type</span></span>   | <span data-ttu-id="69812-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="69812-110">Description</span></span>                                          |
|------|--------|------------------------------------------------------|
| <span data-ttu-id="69812-111">name</span><span class="sxs-lookup"><span data-stu-id="69812-111">name</span></span> | <span data-ttu-id="69812-112">string</span><span class="sxs-lookup"><span data-stu-id="69812-112">string</span></span> | <span data-ttu-id="69812-113">O nome associado aos dados binários.</span><span class="sxs-lookup"><span data-stu-id="69812-113">The name associated with the binary data.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="69812-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69812-114">Requirements</span></span>



| <span data-ttu-id="69812-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="69812-115">Requirement</span></span> | <span data-ttu-id="69812-116">Valor</span><span class="sxs-lookup"><span data-stu-id="69812-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="69812-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69812-117">Minimum supported client</span></span><br/> | <span data-ttu-id="69812-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="69812-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="69812-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69812-119">Minimum supported server</span></span><br/> | <span data-ttu-id="69812-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="69812-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="69812-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="69812-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="69812-122">**Elemento pai**</span><span class="sxs-lookup"><span data-stu-id="69812-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="69812-123">**modelo (TemplateListType)**</span><span class="sxs-lookup"><span data-stu-id="69812-123">**template (TemplateListType)**</span></span>](eventmanifestschema-template-templatelisttype-element.md)
</dt> </dl>

 

