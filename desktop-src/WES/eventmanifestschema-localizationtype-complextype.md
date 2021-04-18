---
title: Tipo complexo de corlocalizatype
description: Define um grupo de recursos localizados que você referencia em seu manifesto. | Tipo complexo de corlocalizatype
ms.assetid: fecab4e0-7136-4b13-8c24-bebbad0812e6
keywords:
- LogType tipo complexo EventLog
topic_type:
- apiref
api_name:
- LocalizationType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cbb6911ea606ea30d8e656f20b4c566d4f6d0e08
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105800192"
---
# <a name="localizationtype-complex-type"></a><span data-ttu-id="a89aa-105">Tipo complexo de corlocalizatype</span><span class="sxs-lookup"><span data-stu-id="a89aa-105">LocalizationType Complex Type</span></span>

<span data-ttu-id="a89aa-106">Define um grupo de recursos localizados que você referencia em seu manifesto.</span><span class="sxs-lookup"><span data-stu-id="a89aa-106">Defines a group of localized resources that you reference in your manifest.</span></span>

``` syntax
<xs:complexType name="LocalizationType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="resources">
            <xs:complexType>
                <xs:choice
                    minOccurs="0"
                    maxOccurs="unbounded"
                >
                    <xs:element name="stringTable"
                        type="StringTableType"
                     />
                </xs:choice>
                <xs:attribute name="culture"
                    type="string"
                    use="required"
                 />
                <xs:anyAttribute
                    processContents="lax"
                    namespace="##other"
                 />
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            namespace="##other"
         />
    </xs:choice>
    <xs:attribute name="fallbackCulture"
        type="string"
        default="en-us"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a89aa-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a89aa-107">Child elements</span></span>



| <span data-ttu-id="a89aa-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="a89aa-108">Element</span></span>                                                                         | <span data-ttu-id="a89aa-109">Type</span><span class="sxs-lookup"><span data-stu-id="a89aa-109">Type</span></span>                                                                       | <span data-ttu-id="a89aa-110">Description</span><span class="sxs-lookup"><span data-stu-id="a89aa-110">Description</span></span>                                                                                                         |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a89aa-111">**os**</span><span class="sxs-lookup"><span data-stu-id="a89aa-111">**resources**</span></span>](eventmanifestschema-resources-localizationtype-element.md)     |                                                                            | <span data-ttu-id="a89aa-112">Define um grupo de tabelas de cadeia que contém as cadeias de caracteres localizadas que você referencia em seu manifesto.</span><span class="sxs-lookup"><span data-stu-id="a89aa-112">Defines a group of string tables that contain the localized strings that you reference in your manifest.</span></span><br/> |
| [<span data-ttu-id="a89aa-113">**stringTable**</span><span class="sxs-lookup"><span data-stu-id="a89aa-113">**stringTable**</span></span>](eventmanifestschema-stringtable-localizationtype-element.md) | [<span data-ttu-id="a89aa-114">**StringTableType**</span><span class="sxs-lookup"><span data-stu-id="a89aa-114">**StringTableType**</span></span>](eventmanifestschema-stringtabletype-complextype.md) | <span data-ttu-id="a89aa-115">Define uma lista de cadeias de caracteres localizadas que você pode referenciar em seu manifesto.</span><span class="sxs-lookup"><span data-stu-id="a89aa-115">Defines a list of localized strings that you can reference in your manifest.</span></span><br/>                             |



## <a name="attributes"></a><span data-ttu-id="a89aa-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="a89aa-116">Attributes</span></span>



| <span data-ttu-id="a89aa-117">Nome</span><span class="sxs-lookup"><span data-stu-id="a89aa-117">Name</span></span>            | <span data-ttu-id="a89aa-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="a89aa-118">Type</span></span>   | <span data-ttu-id="a89aa-119">Description</span><span class="sxs-lookup"><span data-stu-id="a89aa-119">Description</span></span>                                                                                                                                            |
|-----------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a89aa-120">culture</span><span class="sxs-lookup"><span data-stu-id="a89aa-120">culture</span></span>         | <span data-ttu-id="a89aa-121">string</span><span class="sxs-lookup"><span data-stu-id="a89aa-121">string</span></span> | <span data-ttu-id="a89aa-122">Um nome de idioma que identifica a cultura das cadeias de caracteres localizadas na tabela de cadeias.</span><span class="sxs-lookup"><span data-stu-id="a89aa-122">A language name that identifies the culture of the localized strings in the string table.</span></span> <span data-ttu-id="a89aa-123">Por exemplo, "en-US" para inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="a89aa-123">For example, "en-US" for English (United States).</span></span><br/> |
| <span data-ttu-id="a89aa-124">fallbackCulture</span><span class="sxs-lookup"><span data-stu-id="a89aa-124">fallbackCulture</span></span> | <span data-ttu-id="a89aa-125">string</span><span class="sxs-lookup"><span data-stu-id="a89aa-125">string</span></span> | <span data-ttu-id="a89aa-126">Não usado.</span><span class="sxs-lookup"><span data-stu-id="a89aa-126">Not used.</span></span><br/>                                                                                                                                   |



## <a name="requirements"></a><span data-ttu-id="a89aa-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a89aa-127">Requirements</span></span>



| <span data-ttu-id="a89aa-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a89aa-128">Requirement</span></span> | <span data-ttu-id="a89aa-129">Valor</span><span class="sxs-lookup"><span data-stu-id="a89aa-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a89aa-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a89aa-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a89aa-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a89aa-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a89aa-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a89aa-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a89aa-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a89aa-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





