---
title: Elemento messagetable (MetadataType)
description: Contém referências a cadeias de caracteres que são usadas na seção de metadados do manifesto de instrumentação de eventos. As cadeias de caracteres são armazenadas em um grupo de elementos de mensagem e IDs emparelhados juntos.
ms.assetid: 868af191-0f9c-435b-878f-ef0584e097d1
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
ms.openlocfilehash: eb5efc261a2c055a95f71ba556c9acbc0ad45373
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085264"
---
# <a name="messagetable-metadatatype-element"></a><span data-ttu-id="4f803-105">Elemento messagetable (MetadataType)</span><span class="sxs-lookup"><span data-stu-id="4f803-105">messageTable (MetadataType) Element</span></span>

<span data-ttu-id="4f803-106">Contém referências a cadeias de caracteres que são usadas na seção de metadados do manifesto de instrumentação de eventos.</span><span class="sxs-lookup"><span data-stu-id="4f803-106">Contains references to strings that are used in the event instrumentation manifest metadata section.</span></span> <span data-ttu-id="4f803-107">As cadeias de caracteres são armazenadas em um grupo de elementos de [**mensagem**](eventmanifestschema-message-messagetable-element.md) e IDs emparelhados juntos.</span><span class="sxs-lookup"><span data-stu-id="4f803-107">The strings are stored in a group of [**message**](eventmanifestschema-message-messagetable-element.md) elements and IDs paired together.</span></span>

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

<span data-ttu-id="4f803-108">O elemento **messagetable** é definido pelo tipo complexo [**MetadataType**](eventmanifestschema-metadatatype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="4f803-108">The **messageTable** element is defined by the [**MetadataType**](eventmanifestschema-metadatatype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="4f803-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="4f803-109">Child elements</span></span>



| <span data-ttu-id="4f803-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="4f803-110">Element</span></span>                                                             | <span data-ttu-id="4f803-111">Type</span><span class="sxs-lookup"><span data-stu-id="4f803-111">Type</span></span> | <span data-ttu-id="4f803-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="4f803-112">Description</span></span>                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4f803-113">**message**</span><span class="sxs-lookup"><span data-stu-id="4f803-113">**message**</span></span>](eventmanifestschema-message-messagetable-element.md) |      | <span data-ttu-id="4f803-114">Especifica uma referência a uma cadeia de caracteres na seção de localização do manifesto.</span><span class="sxs-lookup"><span data-stu-id="4f803-114">Specifies a reference to a string in the localization section of the manifest.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="4f803-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="4f803-115">Attributes</span></span>



| <span data-ttu-id="4f803-116">Nome</span><span class="sxs-lookup"><span data-stu-id="4f803-116">Name</span></span>    | <span data-ttu-id="4f803-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="4f803-117">Type</span></span>   | <span data-ttu-id="4f803-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="4f803-118">Description</span></span>                                                              |
|---------|--------|--------------------------------------------------------------------------|
| <span data-ttu-id="4f803-119">message</span><span class="sxs-lookup"><span data-stu-id="4f803-119">message</span></span> | <span data-ttu-id="4f803-120">string</span><span class="sxs-lookup"><span data-stu-id="4f803-120">string</span></span> | <span data-ttu-id="4f803-121">Uma referência à cadeia de caracteres localizada na tabela de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4f803-121">A reference to the localized string in the string table.</span></span><br/>      |
| <span data-ttu-id="4f803-122">mid</span><span class="sxs-lookup"><span data-stu-id="4f803-122">mid</span></span>     | <span data-ttu-id="4f803-123">string</span><span class="sxs-lookup"><span data-stu-id="4f803-123">string</span></span> | <span data-ttu-id="4f803-124">Não usado.</span><span class="sxs-lookup"><span data-stu-id="4f803-124">Not used.</span></span><br/>                                                     |
| <span data-ttu-id="4f803-125">símbolo</span><span class="sxs-lookup"><span data-stu-id="4f803-125">symbol</span></span>  | <span data-ttu-id="4f803-126">string</span><span class="sxs-lookup"><span data-stu-id="4f803-126">string</span></span> | <span data-ttu-id="4f803-127">O símbolo usado para fazer referência à mensagem.</span><span class="sxs-lookup"><span data-stu-id="4f803-127">The symbol used to reference the message.</span></span><br/>                     |
| <span data-ttu-id="4f803-128">value</span><span class="sxs-lookup"><span data-stu-id="4f803-128">value</span></span>   | <span data-ttu-id="4f803-129">string</span><span class="sxs-lookup"><span data-stu-id="4f803-129">string</span></span> | <span data-ttu-id="4f803-130">O número a ser usado como o identificador da mensagem para esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="4f803-130">The number to use as the message identifier for this message.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4f803-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f803-131">Requirements</span></span>



| <span data-ttu-id="4f803-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f803-132">Requirement</span></span> | <span data-ttu-id="4f803-133">Valor</span><span class="sxs-lookup"><span data-stu-id="4f803-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4f803-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f803-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4f803-135">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4f803-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4f803-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f803-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4f803-137">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4f803-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4f803-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f803-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="4f803-139">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="4f803-139">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="4f803-140">**MetadataType**</span><span class="sxs-lookup"><span data-stu-id="4f803-140">**MetadataType**</span></span>](eventmanifestschema-metadatatype-complextype.md)
</dt> <dt>

<span data-ttu-id="4f803-141">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="4f803-141">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="4f803-142">**metadados (instrumentationManifest)**</span><span class="sxs-lookup"><span data-stu-id="4f803-142">**metadata (instrumentationManifest)**</span></span>](eventmanifestschema-metadata-instrumentationmanifest-element.md)
</dt> </dl>

 

 





