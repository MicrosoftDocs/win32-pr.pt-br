---
description: Descreve uma única propriedade canônica exclusiva.
ms.assetid: 1a36ec83-5d8a-4fc5-be3d-a8c2f0983057
title: propertyDescription
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233f6d9b1242a9f02b2edbb2bb29cefaef625c7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921338"
---
# <a name="propertydescription"></a><span data-ttu-id="1eb15-103">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="1eb15-103">propertyDescription</span></span>

<span data-ttu-id="1eb15-104">Descreve uma única propriedade canônica exclusiva.</span><span class="sxs-lookup"><span data-stu-id="1eb15-104">Describes a single unique canonical property.</span></span> <span data-ttu-id="1eb15-105">Cada propriedade desse tipo deveria estar disponível no sistema deve ter um elemento [propertyDescription]() correspondente.</span><span class="sxs-lookup"><span data-stu-id="1eb15-105">Every such property intended to be available in the system must have a corresponding [propertyDescription]() element.</span></span>

## <a name="syntax-for-windows-7"></a><span data-ttu-id="1eb15-106">Sintaxe do Windows 7</span><span class="sxs-lookup"><span data-stu-id="1eb15-106">Syntax for Windows 7</span></span>


```
<!-- propertyDescription for Windows 7-->
<xs:element name="propertyDescription">
    <xs:complexType>
        <xs:all>
            <xs:element ref="searchInfo"          minOccurs="0" maxOccurs="1"/>
            <xs:element ref="labelInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="typeInfo"            minOccurs="0" maxOccurs="1"/>
            <xs:element ref="aliasInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="displayInfo"         minOccurs="0" maxOccurs="1"/>
            <xs:element ref="relatedPropertyInfo" minOccurs="0" maxOccurs="1"/>
        </xs:all>

        <xs:attribute name="formatID"  type="uuid" use="required"/>
        <xs:attribute name="propID"    type="propid" use="required"/>
        <xs:attribute name="name"      type="canonical-name"        use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="syntax-for-vista"></a><span data-ttu-id="1eb15-107">Sintaxe do vista</span><span class="sxs-lookup"><span data-stu-id="1eb15-107">Syntax for Vista</span></span>


```
<!-- propertyDescription for Windows Vista-->
<xs:element name="propertyDescription">
    <xs:complexType>
        <xs:all>
            <xs:element ref="searchInfo"          minOccurs="0" maxOccurs="1"/>
            <xs:element ref="labelInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="typeInfo"            minOccurs="0" maxOccurs="1"/>
            <xs:element ref="aliasInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="displayInfo"         minOccurs="0" maxOccurs="1"/>
        </xs:all>

        <xs:attribute name="formatID"  type="uuid" use="required"/>
        <xs:attribute name="propID"    type="xs:nonNegativeInteger" use="required"/>
        <xs:attribute name="name"      type="canonical-name"        use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="1eb15-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="1eb15-108">Element Information</span></span>



| <span data-ttu-id="1eb15-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="1eb15-109">Parent Element</span></span>                                                           | <span data-ttu-id="1eb15-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1eb15-110">Child Elements</span></span>                                                   |
|--------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="1eb15-111">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="1eb15-111">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md) | [<span data-ttu-id="1eb15-112">searchInfo</span><span class="sxs-lookup"><span data-stu-id="1eb15-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)                   |
|                                                                          | [<span data-ttu-id="1eb15-113">labelInfo</span><span class="sxs-lookup"><span data-stu-id="1eb15-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)                     |
|                                                                          | [<span data-ttu-id="1eb15-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="1eb15-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)                       |
|                                                                          | [<span data-ttu-id="1eb15-115">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="1eb15-115">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)                     |
|                                                                          | [<span data-ttu-id="1eb15-116">displayInfo</span><span class="sxs-lookup"><span data-stu-id="1eb15-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)                 |
|                                                                          | [<span data-ttu-id="1eb15-117">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="1eb15-117">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md) |



 

## <a name="attributes"></a><span data-ttu-id="1eb15-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="1eb15-118">Attributes</span></span>



| <span data-ttu-id="1eb15-119">Atributo</span><span class="sxs-lookup"><span data-stu-id="1eb15-119">Attribute</span></span> | <span data-ttu-id="1eb15-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="1eb15-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                         |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1eb15-121">name</span><span class="sxs-lookup"><span data-stu-id="1eb15-121">name</span></span>      | <span data-ttu-id="1eb15-122">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="1eb15-122">Required.</span></span> <span data-ttu-id="1eb15-123">O nome da propriedade canônica, exclusivo para o sistema; por exemplo, `System.Rating` .</span><span class="sxs-lookup"><span data-stu-id="1eb15-123">The canonical property name, unique to the system; for example, `System.Rating`.</span></span> <span data-ttu-id="1eb15-124">Essa cadeia de caracteres é do tipo canônico e é limitada a 64 caracteres.</span><span class="sxs-lookup"><span data-stu-id="1eb15-124">This string is of type canonical-type and is limited to 64 characters.</span></span> <span data-ttu-id="1eb15-125">O nome diferencia maiúsculas de minúsculas e deve usar a seguinte sintaxe: Publisher. Application. PropertyName.</span><span class="sxs-lookup"><span data-stu-id="1eb15-125">The name is case-sensitive and should use the following syntax: Publisher.Application.PropertyName.</span></span> <span data-ttu-id="1eb15-126">[**IPropertyDescription:: Getcanônicaname**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname) retorna esse valor.</span><span class="sxs-lookup"><span data-stu-id="1eb15-126">[**IPropertyDescription::GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname) returns this value.</span></span> |
| <span data-ttu-id="1eb15-127">FormatID</span><span class="sxs-lookup"><span data-stu-id="1eb15-127">formatID</span></span>  | <span data-ttu-id="1eb15-128">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="1eb15-128">Required.</span></span> <span data-ttu-id="1eb15-129">O identificador de formato da propriedade (FMTID).</span><span class="sxs-lookup"><span data-stu-id="1eb15-129">The property's format identifier (FMTID).</span></span> <span data-ttu-id="1eb15-130">O valor deve incluir chaves de circunscrição; por exemplo, `{64440492-4C8B-11D1-8B70-080036B11A03}` .</span><span class="sxs-lookup"><span data-stu-id="1eb15-130">The value must include enclosing braces; for example, `{64440492-4C8B-11D1-8B70-080036B11A03}`.</span></span> <span data-ttu-id="1eb15-131">[**IPropertyDescription:: GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) retorna esse valor.</span><span class="sxs-lookup"><span data-stu-id="1eb15-131">[**IPropertyDescription::GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) returns this value.</span></span>                                                                                                                       |
| <span data-ttu-id="1eb15-132">propID</span><span class="sxs-lookup"><span data-stu-id="1eb15-132">propID</span></span>    | <span data-ttu-id="1eb15-133">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="1eb15-133">Required.</span></span> <span data-ttu-id="1eb15-134">O identificador de propriedade (PID); por exemplo, `9` .</span><span class="sxs-lookup"><span data-stu-id="1eb15-134">The property identifier (PID); for example, `9`.</span></span> <span data-ttu-id="1eb15-135">[**IPropertyDescription:: GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) retorna esse valor.</span><span class="sxs-lookup"><span data-stu-id="1eb15-135">[**IPropertyDescription::GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) returns this value.</span></span> <span data-ttu-id="1eb15-136">Esse valor deve ser maior ou igual a 2.</span><span class="sxs-lookup"><span data-stu-id="1eb15-136">This value must be greater than or equal to 2.</span></span> <span data-ttu-id="1eb15-137">Os valores 0 e 1 são reservados pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="1eb15-137">The values 0 and 1 are reserved by the system.</span></span>                                                                                                                  |



 

 

 
