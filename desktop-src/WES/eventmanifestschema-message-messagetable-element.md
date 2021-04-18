---
title: Elemento de mensagem (messagetable)
description: Contém uma referência a uma cadeia de caracteres na seção de localização do manifesto. | Elemento de mensagem (messagetable)
ms.assetid: 0988cf99-c7e1-446b-869e-9ac4a0976ac5
keywords:
- EventLog de elemento de mensagem
topic_type:
- apiref
api_name:
- message
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e1165e3a613434fb76befb87cd1a83ed3af95d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105781300"
---
# <a name="message-messagetable-element"></a><span data-ttu-id="8c8ef-105">Elemento de mensagem (messagetable)</span><span class="sxs-lookup"><span data-stu-id="8c8ef-105">message (messageTable) Element</span></span>

<span data-ttu-id="8c8ef-106">Contém uma referência a uma cadeia de caracteres na seção de localização do manifesto.</span><span class="sxs-lookup"><span data-stu-id="8c8ef-106">Contains a reference to a string in the localization section of the manifest.</span></span>

``` syntax
<xs:element name="message">
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
```

<span data-ttu-id="8c8ef-107">O elemento **Message** é definido pelo elemento [**messagetable**](eventmanifestschema-messagetable-instrumentationtype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8c8ef-107">The **message** element is defined by the [**messageTable**](eventmanifestschema-messagetable-instrumentationtype-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="8c8ef-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="8c8ef-108">Attributes</span></span>



| <span data-ttu-id="8c8ef-109">Nome</span><span class="sxs-lookup"><span data-stu-id="8c8ef-109">Name</span></span>    | <span data-ttu-id="8c8ef-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="8c8ef-110">Type</span></span>   | <span data-ttu-id="8c8ef-111">Description</span><span class="sxs-lookup"><span data-stu-id="8c8ef-111">Description</span></span>                                                                                        |
|---------|--------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c8ef-112">message</span><span class="sxs-lookup"><span data-stu-id="8c8ef-112">message</span></span> | <span data-ttu-id="8c8ef-113">string</span><span class="sxs-lookup"><span data-stu-id="8c8ef-113">string</span></span> | <span data-ttu-id="8c8ef-114">Uma referência à cadeia de caracteres localizada na tabela de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8c8ef-114">A reference to the localized string in the string table.</span></span><br/>                                |
| <span data-ttu-id="8c8ef-115">mid</span><span class="sxs-lookup"><span data-stu-id="8c8ef-115">mid</span></span>     | <span data-ttu-id="8c8ef-116">string</span><span class="sxs-lookup"><span data-stu-id="8c8ef-116">string</span></span> | <span data-ttu-id="8c8ef-117">Não usado.</span><span class="sxs-lookup"><span data-stu-id="8c8ef-117">Not used.</span></span><br/>                                                                               |
| <span data-ttu-id="8c8ef-118">símbolo</span><span class="sxs-lookup"><span data-stu-id="8c8ef-118">symbol</span></span>  | <span data-ttu-id="8c8ef-119">string</span><span class="sxs-lookup"><span data-stu-id="8c8ef-119">string</span></span> | <span data-ttu-id="8c8ef-120">O nome simbólico que você deseja que o compilador de mensagem crie para essa cadeia de caracteres de mensagem.</span><span class="sxs-lookup"><span data-stu-id="8c8ef-120">The symbolic name that you want the message compiler to create for this message string.</span></span><br/> |
| <span data-ttu-id="8c8ef-121">value</span><span class="sxs-lookup"><span data-stu-id="8c8ef-121">value</span></span>   | <span data-ttu-id="8c8ef-122">string</span><span class="sxs-lookup"><span data-stu-id="8c8ef-122">string</span></span> | <span data-ttu-id="8c8ef-123">O número a ser usado como o identificador da mensagem para esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="8c8ef-123">The number to use as the message identifier for this message.</span></span><br/>                           |



## <a name="requirements"></a><span data-ttu-id="8c8ef-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c8ef-124">Requirements</span></span>



| <span data-ttu-id="8c8ef-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c8ef-125">Requirement</span></span> | <span data-ttu-id="8c8ef-126">Valor</span><span class="sxs-lookup"><span data-stu-id="8c8ef-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8c8ef-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c8ef-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8c8ef-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8c8ef-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8c8ef-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c8ef-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8c8ef-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8c8ef-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8c8ef-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c8ef-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="8c8ef-132">**Elementos pai**</span><span class="sxs-lookup"><span data-stu-id="8c8ef-132">**Parent elements**</span></span>
</dt> <dt>

[<span data-ttu-id="8c8ef-133">**messagetable (EventType)**</span><span class="sxs-lookup"><span data-stu-id="8c8ef-133">**messageTable (EventsType)**</span></span>](eventmanifestschema-messagetable-instrumentationtype-element.md)
</dt> <dt>

[<span data-ttu-id="8c8ef-134">**mensagens (MetadataType)**</span><span class="sxs-lookup"><span data-stu-id="8c8ef-134">**messageTable (MetadataType)**</span></span>](eventmanifestschema-messagetable-metadatatype-element.md)
</dt> </dl>

 

 





