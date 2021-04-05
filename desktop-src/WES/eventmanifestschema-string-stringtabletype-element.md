---
title: Elemento String (StringTableType)
description: Define uma cadeia de caracteres localizada.
ms.assetid: 845476a9-bcf4-4821-824c-06c9a9f64649
keywords:
- elemento string EventLog
topic_type:
- apiref
api_name:
- string
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c46fc43366d6472e8047b529d847eefd5369c263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918636"
---
# <a name="string-stringtabletype-element"></a><span data-ttu-id="922e5-104">Elemento String (StringTableType)</span><span class="sxs-lookup"><span data-stu-id="922e5-104">string (StringTableType) Element</span></span>

<span data-ttu-id="922e5-105">Define uma cadeia de caracteres localizada.</span><span class="sxs-lookup"><span data-stu-id="922e5-105">Defines a localized string.</span></span>

``` syntax
<xs:element name="string">
    <xs:complexType>
        <xs:attribute name="id"
            type="string"
            use="required"
         />
        <xs:attribute name="value"
            type="string"
            use="required"
         />
        <xs:attribute name="stringType"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="922e5-106">O elemento **String** é definido pelo tipo complexo [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="922e5-106">The **string** element is defined by the [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="922e5-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="922e5-107">Attributes</span></span>



| <span data-ttu-id="922e5-108">Nome</span><span class="sxs-lookup"><span data-stu-id="922e5-108">Name</span></span>       | <span data-ttu-id="922e5-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="922e5-109">Type</span></span>   | <span data-ttu-id="922e5-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="922e5-110">Description</span></span>                                                                           |
|------------|--------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="922e5-111">id</span><span class="sxs-lookup"><span data-stu-id="922e5-111">id</span></span>         | <span data-ttu-id="922e5-112">string</span><span class="sxs-lookup"><span data-stu-id="922e5-112">string</span></span> | <span data-ttu-id="922e5-113">Um identificador que identifica exclusivamente a cadeia de caracteres na tabela de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="922e5-113">An identifier that uniquely identifies the string within the string table.</span></span><br/> |
| <span data-ttu-id="922e5-114">StringType</span><span class="sxs-lookup"><span data-stu-id="922e5-114">stringType</span></span> | <span data-ttu-id="922e5-115">string</span><span class="sxs-lookup"><span data-stu-id="922e5-115">string</span></span> | <span data-ttu-id="922e5-116">Não usado.</span><span class="sxs-lookup"><span data-stu-id="922e5-116">Not used.</span></span><br/>                                                                  |
| <span data-ttu-id="922e5-117">value</span><span class="sxs-lookup"><span data-stu-id="922e5-117">value</span></span>      | <span data-ttu-id="922e5-118">string</span><span class="sxs-lookup"><span data-stu-id="922e5-118">string</span></span> | <span data-ttu-id="922e5-119">A cadeia de caracteres localizada.</span><span class="sxs-lookup"><span data-stu-id="922e5-119">The localized string.</span></span><br/>                                                      |



## <a name="requirements"></a><span data-ttu-id="922e5-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="922e5-120">Requirements</span></span>



| <span data-ttu-id="922e5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="922e5-121">Requirement</span></span> | <span data-ttu-id="922e5-122">Valor</span><span class="sxs-lookup"><span data-stu-id="922e5-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="922e5-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="922e5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="922e5-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="922e5-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="922e5-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="922e5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="922e5-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="922e5-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="922e5-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="922e5-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="922e5-128">**Elemento pai**</span><span class="sxs-lookup"><span data-stu-id="922e5-128">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="922e5-129">**stringTable (corlocalizatype)**</span><span class="sxs-lookup"><span data-stu-id="922e5-129">**stringTable (LocalizationType)**</span></span>](eventmanifestschema-stringtable-localizationtype-element.md)
</dt> </dl>

 

 





