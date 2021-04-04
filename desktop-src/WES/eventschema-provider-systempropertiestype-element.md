---
title: Elemento Provider (SystemPropertiesType)
description: Identifica o provedor que registrou o evento.
ms.assetid: 4560c938-4e2a-40d5-97f9-85a38141ac8f
keywords:
- O elemento do provedor EventLog
topic_type:
- apiref
api_name:
- Provider
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c3dc6ae072ed6491915067bea4395a1a84369b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009021"
---
# <a name="provider-systempropertiestype-element"></a><span data-ttu-id="589a4-104">Elemento Provider (SystemPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="589a4-104">Provider (SystemPropertiesType) Element</span></span>

<span data-ttu-id="589a4-105">Identifica o provedor que registrou o evento.</span><span class="sxs-lookup"><span data-stu-id="589a4-105">Identifies the provider that logged the event.</span></span>

``` syntax
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
```

<span data-ttu-id="589a4-106">O elemento **Provider** é definido pelo tipo complexo [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="589a4-106">The **Provider** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="589a4-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="589a4-107">Attributes</span></span>



| <span data-ttu-id="589a4-108">Nome</span><span class="sxs-lookup"><span data-stu-id="589a4-108">Name</span></span>            | <span data-ttu-id="589a4-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="589a4-109">Type</span></span>                                                | <span data-ttu-id="589a4-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="589a4-110">Description</span></span>                                                                                                                                        |
|-----------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="589a4-111">EventSourcename</span><span class="sxs-lookup"><span data-stu-id="589a4-111">EventSourceName</span></span> | <span data-ttu-id="589a4-112">string</span><span class="sxs-lookup"><span data-stu-id="589a4-112">string</span></span>                                              | <span data-ttu-id="589a4-113">O nome da origem do evento que publicou o evento (se a origem do evento for da API de [log de eventos](/windows/desktop/EventLog/event-logging) herdados).</span><span class="sxs-lookup"><span data-stu-id="589a4-113">The name of the event source that published the event (if the event source is from the legacy [Event Logging](/windows/desktop/EventLog/event-logging) API).</span></span><br/> |
| <span data-ttu-id="589a4-114">Guid</span><span class="sxs-lookup"><span data-stu-id="589a4-114">Guid</span></span>            | [<span data-ttu-id="589a4-115">**GUIDtype**</span><span class="sxs-lookup"><span data-stu-id="589a4-115">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="589a4-116">O identificador global exclusivo que identifica exclusivamente o provedor.</span><span class="sxs-lookup"><span data-stu-id="589a4-116">The globally unique identifier that uniquely identifies the provider.</span></span><br/>                                                                   |
| <span data-ttu-id="589a4-117">Nome</span><span class="sxs-lookup"><span data-stu-id="589a4-117">Name</span></span>            | <span data-ttu-id="589a4-118">anyURI</span><span class="sxs-lookup"><span data-stu-id="589a4-118">anyURI</span></span>                                              | <span data-ttu-id="589a4-119">O nome do provedor de eventos que registrou o evento.</span><span class="sxs-lookup"><span data-stu-id="589a4-119">The name of the event provider that logged the event.</span></span><br/>                                                                                   |



## <a name="requirements"></a><span data-ttu-id="589a4-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="589a4-120">Requirements</span></span>



| <span data-ttu-id="589a4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="589a4-121">Requirement</span></span> | <span data-ttu-id="589a4-122">Valor</span><span class="sxs-lookup"><span data-stu-id="589a4-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="589a4-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="589a4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="589a4-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="589a4-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="589a4-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="589a4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="589a4-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="589a4-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="589a4-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="589a4-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="589a4-128">**Elemento pai**</span><span class="sxs-lookup"><span data-stu-id="589a4-128">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="589a4-129">**Sistema (EventType)**</span><span class="sxs-lookup"><span data-stu-id="589a4-129">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

