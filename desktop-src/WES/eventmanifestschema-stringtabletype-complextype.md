---
title: Tipo complexo StringTableType
description: Define uma lista de cadeias de caracteres localizadas que você pode referenciar em seu manifesto. | Tipo complexo StringTableType
ms.assetid: 47a59ff7-aaf6-4200-805b-0a8b5f57f101
keywords:
- Log de eventos do tipo complexo StringTableType
topic_type:
- apiref
api_name:
- StringTableType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9964c51524f7401afdfdd8a2da10cf43326bcae
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105763401"
---
# <a name="stringtabletype-complex-type"></a><span data-ttu-id="f3642-105">Tipo complexo StringTableType</span><span class="sxs-lookup"><span data-stu-id="f3642-105">StringTableType Complex Type</span></span>

<span data-ttu-id="f3642-106">Define uma lista de cadeias de caracteres localizadas que você pode referenciar em seu manifesto.</span><span class="sxs-lookup"><span data-stu-id="f3642-106">Defines a list of localized strings that you can reference in your manifest.</span></span>

``` syntax
<xs:complexType name="StringTableType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="string">
            <xs:complexType
                mixed="true"
            >
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
    </xs:choice>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="f3642-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f3642-107">Child elements</span></span>



| <span data-ttu-id="f3642-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="f3642-108">Element</span></span>                                                              | <span data-ttu-id="f3642-109">Type</span><span class="sxs-lookup"><span data-stu-id="f3642-109">Type</span></span> | <span data-ttu-id="f3642-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f3642-110">Description</span></span>                            |
|----------------------------------------------------------------------|------|----------------------------------------|
| [<span data-ttu-id="f3642-111">**string**</span><span class="sxs-lookup"><span data-stu-id="f3642-111">**string**</span></span>](eventmanifestschema-string-stringtabletype-element.md) |      | <span data-ttu-id="f3642-112">Define uma cadeia de caracteres localizada.</span><span class="sxs-lookup"><span data-stu-id="f3642-112">Defines a localized string.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="f3642-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="f3642-113">Attributes</span></span>



| <span data-ttu-id="f3642-114">Nome</span><span class="sxs-lookup"><span data-stu-id="f3642-114">Name</span></span>       | <span data-ttu-id="f3642-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="f3642-115">Type</span></span>   | <span data-ttu-id="f3642-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="f3642-116">Description</span></span>                                                                                                              |
|------------|--------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3642-117">id</span><span class="sxs-lookup"><span data-stu-id="f3642-117">id</span></span>         | <span data-ttu-id="f3642-118">string</span><span class="sxs-lookup"><span data-stu-id="f3642-118">string</span></span> | <span data-ttu-id="f3642-119">Um identificador que identifica exclusivamente a cadeia de caracteres na tabela de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f3642-119">An identifier that uniquely identifies the string within the string table.</span></span> <span data-ttu-id="f3642-120">Por exemplo, "Printer. Connection".</span><span class="sxs-lookup"><span data-stu-id="f3642-120">For example, "Printer.Connection".</span></span><br/> |
| <span data-ttu-id="f3642-121">StringType</span><span class="sxs-lookup"><span data-stu-id="f3642-121">stringType</span></span> | <span data-ttu-id="f3642-122">string</span><span class="sxs-lookup"><span data-stu-id="f3642-122">string</span></span> | <span data-ttu-id="f3642-123">Não usado.</span><span class="sxs-lookup"><span data-stu-id="f3642-123">Not used.</span></span><br/>                                                                                                     |
| <span data-ttu-id="f3642-124">value</span><span class="sxs-lookup"><span data-stu-id="f3642-124">value</span></span>      | <span data-ttu-id="f3642-125">string</span><span class="sxs-lookup"><span data-stu-id="f3642-125">string</span></span> | <span data-ttu-id="f3642-126">A cadeia de caracteres localizada.</span><span class="sxs-lookup"><span data-stu-id="f3642-126">The localized string.</span></span><br/>                                                                                         |



## <a name="remarks"></a><span data-ttu-id="f3642-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="f3642-127">Remarks</span></span>

<span data-ttu-id="f3642-128">Você pode fazer referência às cadeias de caracteres de qualquer tipo de manifesto que contenha o atributo Message.</span><span class="sxs-lookup"><span data-stu-id="f3642-128">You can reference the strings from any manifest type that contains the message attribute.</span></span> <span data-ttu-id="f3642-129">Para fazer referência a uma cadeia de caracteres com um StringType de "String" e uma ID de "Printer. Connection", use $ (String. Printer. Connection) como o valor do atributo Message.</span><span class="sxs-lookup"><span data-stu-id="f3642-129">To reference a string with a stringType of "string" and an id of "Printer.Connection", use $(string.Printer.Connection) as the value of the message attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3642-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3642-130">Requirements</span></span>



| <span data-ttu-id="f3642-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3642-131">Requirement</span></span> | <span data-ttu-id="f3642-132">Valor</span><span class="sxs-lookup"><span data-stu-id="f3642-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f3642-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3642-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f3642-134">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f3642-134">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f3642-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3642-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f3642-136">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f3642-136">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





