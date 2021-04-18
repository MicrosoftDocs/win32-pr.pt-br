---
description: Contêiner para um ou vários elementos propertyDescription individuais.
ms.assetid: b54aaa85-6928-470e-9630-44b094205106
title: propertyDescriptionList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cd0beaf4dbbd8b71c7f4b3335c169754c704d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751531"
---
# <a name="propertydescriptionlist"></a><span data-ttu-id="c2af2-103">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="c2af2-103">propertyDescriptionList</span></span>

<span data-ttu-id="c2af2-104">Contêiner para um ou vários elementos [propertyDescription](./propdesc-schema-propertydescription.md) individuais.</span><span class="sxs-lookup"><span data-stu-id="c2af2-104">Container for one or many individual [propertyDescription](./propdesc-schema-propertydescription.md) elements.</span></span> <span data-ttu-id="c2af2-105">Um arquivo de esquema de descrição da propriedade. propDesc deve conter pelo menos um elemento [propertyDescriptionList]() .</span><span class="sxs-lookup"><span data-stu-id="c2af2-105">A .propdesc property description schema file should contain at least one [propertyDescriptionList]() element.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2af2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2af2-106">Syntax</span></span>


```
<!-- propertyDescriptionList -->
<xs:element name="propertyDescriptionList">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="s:propertyDescription" minOccurs="1" maxOccurs="unbounded"/>
        </xs:sequence>
        <xs:attribute name="publisher" type="xs:string" use="required"/>
        <xs:attribute name="product"   type="xs:string" use="required"/>
    </xs:complexType>

    <xs:unique name="No_two_propertyDescriptions_can_have_the_same_formatid_and_propid">
        <xs:selector xpath="s:propertyDescription"/>
        <xs:field    xpath="@formatID"/>
        <xs:field    xpath="@propID"/>
    </xs:unique>

    <xs:unique name="No_two_propertyDescriptions_can_have_the_same_canonical_name">
        <xs:selector xpath="s:propertyDescription"/>
        <xs:field    xpath="@name"/>
    </xs:unique>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="c2af2-107">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="c2af2-107">Element Information</span></span>



| <span data-ttu-id="c2af2-108">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="c2af2-108">Parent Element</span></span>                        | <span data-ttu-id="c2af2-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="c2af2-109">Child Elements</span></span>                                                   |
|---------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="c2af2-110">schema</span><span class="sxs-lookup"><span data-stu-id="c2af2-110">schema</span></span>](./propdesc-schema-entry.md) | [<span data-ttu-id="c2af2-111">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="c2af2-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) |



 

## <a name="attributes"></a><span data-ttu-id="c2af2-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="c2af2-112">Attributes</span></span>



| <span data-ttu-id="c2af2-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="c2af2-113">Attribute</span></span> | <span data-ttu-id="c2af2-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2af2-114">Description</span></span>                                                               |
|-----------|---------------------------------------------------------------------------|
| <span data-ttu-id="c2af2-115">editor</span><span class="sxs-lookup"><span data-stu-id="c2af2-115">publisher</span></span> | <span data-ttu-id="c2af2-116">Público.</span><span class="sxs-lookup"><span data-stu-id="c2af2-116">Public.</span></span> <span data-ttu-id="c2af2-117">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="c2af2-117">Required.</span></span> <span data-ttu-id="c2af2-118">O nome de exibição do Publicador que fornece o esquema.</span><span class="sxs-lookup"><span data-stu-id="c2af2-118">The display name of the publisher providing the schema.</span></span> |
| <span data-ttu-id="c2af2-119">product</span><span class="sxs-lookup"><span data-stu-id="c2af2-119">product</span></span>   | <span data-ttu-id="c2af2-120">Público.</span><span class="sxs-lookup"><span data-stu-id="c2af2-120">Public.</span></span> <span data-ttu-id="c2af2-121">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="c2af2-121">Required.</span></span> <span data-ttu-id="c2af2-122">O nome de exibição do produto que fornece o esquema.</span><span class="sxs-lookup"><span data-stu-id="c2af2-122">The display name of the product providing the schema.</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="c2af2-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2af2-123">Remarks</span></span>

<span data-ttu-id="c2af2-124">O [propertyDescriptionList]() não deve ser confundido com "listas de propriedades" e [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), que são completamente separadas.</span><span class="sxs-lookup"><span data-stu-id="c2af2-124">The [propertyDescriptionList]() should not be confused with "property lists" and [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), which are completely separate.</span></span>

 

 
