---
title: Elemento resources (Localizatype)
description: Define um grupo de tabelas de cadeia que contém as cadeias de caracteres localizadas que você referencia em seu manifesto.
ms.assetid: b984894a-0ae8-49be-af93-3acdcce53ee9
keywords:
- Log de elementos de recursos
topic_type:
- apiref
api_name:
- resources
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55bdfe504da08c754c18b790e282eba6787c3ee3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105789598"
---
# <a name="resources-localizationtype-element"></a><span data-ttu-id="cd80f-104">Elemento resources (Localizatype)</span><span class="sxs-lookup"><span data-stu-id="cd80f-104">resources (LocalizationType) Element</span></span>

<span data-ttu-id="cd80f-105">Define um grupo de tabelas de cadeia que contém as cadeias de caracteres localizadas que você referencia em seu manifesto.</span><span class="sxs-lookup"><span data-stu-id="cd80f-105">Defines a group of string tables that contain the localized strings that you reference in your manifest.</span></span>

``` syntax
<xs:element name="resources">
    <xs:complexType>
        <xs:choice
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:element name="stringTable"
                type="StringTableType"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                namespace="##other"
             />
        </xs:choice>
        <xs:attribute name="culture"
            type="string"
            default="##fallback"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="cd80f-106">O elemento **Resources** é definido pelo tipo complexo de [**corlocalizatype**](eventmanifestschema-localizationtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="cd80f-106">The **resources** element is defined by the [**LocalizationType**](eventmanifestschema-localizationtype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="cd80f-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="cd80f-107">Child elements</span></span>



| <span data-ttu-id="cd80f-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="cd80f-108">Element</span></span>                                                                  | <span data-ttu-id="cd80f-109">Type</span><span class="sxs-lookup"><span data-stu-id="cd80f-109">Type</span></span>                                                                       | <span data-ttu-id="cd80f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="cd80f-110">Description</span></span>                                                                             |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd80f-111">**stringTable**</span><span class="sxs-lookup"><span data-stu-id="cd80f-111">**stringTable**</span></span>](eventmanifestschema-stringtable-resources-element.md) | [<span data-ttu-id="cd80f-112">**StringTableType**</span><span class="sxs-lookup"><span data-stu-id="cd80f-112">**StringTableType**</span></span>](eventmanifestschema-stringtabletype-complextype.md) | <span data-ttu-id="cd80f-113">Define uma lista de cadeias de caracteres localizadas que você pode referenciar em seu manifesto.</span><span class="sxs-lookup"><span data-stu-id="cd80f-113">Defines a list of localized strings that you can reference in your manifest.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="cd80f-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="cd80f-114">Attributes</span></span>



| <span data-ttu-id="cd80f-115">Nome</span><span class="sxs-lookup"><span data-stu-id="cd80f-115">Name</span></span>    | <span data-ttu-id="cd80f-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd80f-116">Type</span></span>   | <span data-ttu-id="cd80f-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="cd80f-117">Description</span></span>                                                                                                                                            |
|---------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd80f-118">culture</span><span class="sxs-lookup"><span data-stu-id="cd80f-118">culture</span></span> | <span data-ttu-id="cd80f-119">string</span><span class="sxs-lookup"><span data-stu-id="cd80f-119">string</span></span> | <span data-ttu-id="cd80f-120">Um nome de idioma que identifica a cultura das cadeias de caracteres localizadas na tabela de cadeias.</span><span class="sxs-lookup"><span data-stu-id="cd80f-120">A language name that identifies the culture of the localized strings in the string table.</span></span> <span data-ttu-id="cd80f-121">Por exemplo, "en-US" para inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="cd80f-121">For example, "en-US" for English (United States).</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="cd80f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd80f-122">Requirements</span></span>



| <span data-ttu-id="cd80f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd80f-123">Requirement</span></span> | <span data-ttu-id="cd80f-124">Valor</span><span class="sxs-lookup"><span data-stu-id="cd80f-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cd80f-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd80f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cd80f-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cd80f-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cd80f-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd80f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cd80f-128">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cd80f-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cd80f-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd80f-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="cd80f-130">**Elemento pai**</span><span class="sxs-lookup"><span data-stu-id="cd80f-130">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="cd80f-131">**localização (instrumentationManifest)**</span><span class="sxs-lookup"><span data-stu-id="cd80f-131">**localization (instrumentationManifest)**</span></span>](eventmanifestschema-localization-instrumentationmanifest-element.md)
</dt> </dl>

 

 





