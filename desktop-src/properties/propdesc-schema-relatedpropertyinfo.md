---
description: Novo no Windows 7. Elemento contêiner para elementos relatedproperty.
ms.assetid: F8BAAE5C-A7EA-487a-B829-91A27E24B58D
title: relatedPropertyInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 442de657bed7e97f74064c39cc0934c65a6f520d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783321"
---
# <a name="relatedpropertyinfo"></a><span data-ttu-id="baadb-104">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="baadb-104">relatedPropertyInfo</span></span>

<span data-ttu-id="baadb-105">Novo no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="baadb-105">New for Windows 7.</span></span> <span data-ttu-id="baadb-106">Elemento contêiner para elementos [relatedproperty](./propdesc-schema-relatedproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="baadb-106">Container element for [relatedProperty](./propdesc-schema-relatedproperty.md) elements.</span></span> <span data-ttu-id="baadb-107">Deve haver apenas um elemento [relatedPropertyInfo]() para cada elemento [propertyDescription](./propdesc-schema-propertydescription.md) .</span><span class="sxs-lookup"><span data-stu-id="baadb-107">There should be only one [relatedPropertyInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md) element.</span></span>

## <a name="syntax"></a><span data-ttu-id="baadb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="baadb-108">Syntax</span></span>


```
<!-- relatedPropertyInfo -->
<xs:element name="relatedPropertyInfo">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="relatedProperty" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="relationshipName" type="canonical-name" use="required"/>
                    <xs:attribute name="propertyName" type="canonical-name" use="required"/>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>

    <xs:unique name="No_two_relatedProperties_can_have_the_same_relationship_name">
        <xs:selector xpath="s:relatedProperty"/>
        <xs:field    xpath="@relationshipName"/>
    </xs:unique>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="baadb-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="baadb-109">Element Information</span></span>



| <span data-ttu-id="baadb-110">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="baadb-110">Parent Element</span></span>                                                   | <span data-ttu-id="baadb-111">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="baadb-111">Child Elements</span></span>                                           |
|------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="baadb-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="baadb-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | [<span data-ttu-id="baadb-113">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="baadb-113">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md) |



 

## <a name="attributes"></a><span data-ttu-id="baadb-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="baadb-114">Attributes</span></span>

<span data-ttu-id="baadb-115">Esse elemento não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="baadb-115">This element has no attributes.</span></span>

 

 
