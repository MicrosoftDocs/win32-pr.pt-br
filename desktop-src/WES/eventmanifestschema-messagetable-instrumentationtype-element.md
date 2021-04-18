---
title: Elemento messagetable (EventType)
description: Contém uma referência a uma cadeia de caracteres na seção de localização do manifesto. | Elemento messagetable (EventType)
ms.assetid: 4dcc1afe-8f2b-4baf-b40b-406f60368575
keywords:
- EventLog do elemento messagetable
topic_type:
- apiref
api_name:
- messageTable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 85ce478fb30389ba911ef9dd76473a6261974f55
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105788819"
---
# <a name="messagetable-eventstype-element"></a><span data-ttu-id="0ae1f-105">Elemento messagetable (EventType)</span><span class="sxs-lookup"><span data-stu-id="0ae1f-105">messageTable (EventsType) Element</span></span>

<span data-ttu-id="0ae1f-106">Contém uma referência a uma cadeia de caracteres na seção de localização do manifesto.</span><span class="sxs-lookup"><span data-stu-id="0ae1f-106">Contains a reference to a string in the localization section of the manifest.</span></span>

``` syntax
<xs:element name="messageTable">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="message"
                minOccurs="0"
                maxOccurs="unbounded"
            >
                <xs:complexType>
                    <xs:attribute name="value"
                        type="string"
                        use="required"
                     />
                    <xs:attribute name="mid"
                        type="string"
                        use="optional"
                     />
                    <xs:attribute name="message"
                        type="string"
                        use="required"
                     />
                    <xs:attribute name="symbol"
                        type="string"
                        use="optional"
                     />
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="0ae1f-107">O elemento **messagetable** é definido pelo tipo complexo [**EventType**](eventmanifestschema-eventstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="0ae1f-107">The **messageTable** element is defined by the [**EventsType**](eventmanifestschema-eventstype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0ae1f-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="0ae1f-108">Child elements</span></span>



| <span data-ttu-id="0ae1f-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="0ae1f-109">Element</span></span>                                                             | <span data-ttu-id="0ae1f-110">Type</span><span class="sxs-lookup"><span data-stu-id="0ae1f-110">Type</span></span> | <span data-ttu-id="0ae1f-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="0ae1f-111">Description</span></span>                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0ae1f-112">**message**</span><span class="sxs-lookup"><span data-stu-id="0ae1f-112">**message**</span></span>](eventmanifestschema-message-messagetable-element.md) |      | <span data-ttu-id="0ae1f-113">Especifica uma referência a uma cadeia de caracteres na seção de localização do manifesto.</span><span class="sxs-lookup"><span data-stu-id="0ae1f-113">Specifies a reference to a string in the localization section of the manifest.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="0ae1f-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="0ae1f-114">Attributes</span></span>



| <span data-ttu-id="0ae1f-115">Nome</span><span class="sxs-lookup"><span data-stu-id="0ae1f-115">Name</span></span>    | <span data-ttu-id="0ae1f-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ae1f-116">Type</span></span>   | <span data-ttu-id="0ae1f-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="0ae1f-117">Description</span></span>                                                                                        |
|---------|--------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ae1f-118">message</span><span class="sxs-lookup"><span data-stu-id="0ae1f-118">message</span></span> | <span data-ttu-id="0ae1f-119">string</span><span class="sxs-lookup"><span data-stu-id="0ae1f-119">string</span></span> | <span data-ttu-id="0ae1f-120">Uma referência à cadeia de caracteres localizada na tabela de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="0ae1f-120">A reference to the localized string in the string table.</span></span><br/>                                |
| <span data-ttu-id="0ae1f-121">mid</span><span class="sxs-lookup"><span data-stu-id="0ae1f-121">mid</span></span>     | <span data-ttu-id="0ae1f-122">string</span><span class="sxs-lookup"><span data-stu-id="0ae1f-122">string</span></span> | <span data-ttu-id="0ae1f-123">Não usado.</span><span class="sxs-lookup"><span data-stu-id="0ae1f-123">Not used.</span></span><br/>                                                                               |
| <span data-ttu-id="0ae1f-124">símbolo</span><span class="sxs-lookup"><span data-stu-id="0ae1f-124">symbol</span></span>  | <span data-ttu-id="0ae1f-125">string</span><span class="sxs-lookup"><span data-stu-id="0ae1f-125">string</span></span> | <span data-ttu-id="0ae1f-126">O nome simbólico que você deseja que o compilador de mensagem crie para essa cadeia de caracteres de mensagem.</span><span class="sxs-lookup"><span data-stu-id="0ae1f-126">The symbolic name that you want the message compiler to create for this message string.</span></span><br/> |
| <span data-ttu-id="0ae1f-127">value</span><span class="sxs-lookup"><span data-stu-id="0ae1f-127">value</span></span>   | <span data-ttu-id="0ae1f-128">string</span><span class="sxs-lookup"><span data-stu-id="0ae1f-128">string</span></span> | <span data-ttu-id="0ae1f-129">O número a ser usado como o identificador da mensagem para esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="0ae1f-129">The number to use as the message identifier for this message.</span></span><br/>                           |



## <a name="requirements"></a><span data-ttu-id="0ae1f-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ae1f-130">Requirements</span></span>



| <span data-ttu-id="0ae1f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ae1f-131">Requirement</span></span> | <span data-ttu-id="0ae1f-132">Valor</span><span class="sxs-lookup"><span data-stu-id="0ae1f-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0ae1f-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ae1f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0ae1f-134">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0ae1f-134">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0ae1f-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ae1f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0ae1f-136">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0ae1f-136">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0ae1f-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ae1f-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="0ae1f-138">**Elementos pai**</span><span class="sxs-lookup"><span data-stu-id="0ae1f-138">**Parent elements**</span></span>
</dt> <dt>

[<span data-ttu-id="0ae1f-139">**Elemento Events (InstrumentationType)**</span><span class="sxs-lookup"><span data-stu-id="0ae1f-139">**events (InstrumentationType) Element**</span></span>](eventmanifestschema-events-instrumentationtype-element.md)
</dt> </dl>

 

 





