---
description: Novo no Windows 7. Identifica uma propriedade que está relacionada à propriedade definida no arquivo de descrição da propriedade.
ms.assetid: 30167942-141A-4f37-B019-0811BA654124
title: relatedProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cabde093a47a25834598659d3ad38e0847c1351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296609"
---
# <a name="relatedproperty"></a><span data-ttu-id="97a99-104">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="97a99-104">relatedProperty</span></span>

<span data-ttu-id="97a99-105">Novo no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="97a99-105">New for Windows 7.</span></span> <span data-ttu-id="97a99-106">Identifica uma propriedade que está relacionada à propriedade definida no arquivo de descrição da propriedade.</span><span class="sxs-lookup"><span data-stu-id="97a99-106">Identifies a property that is related to the property defined in the property description file.</span></span> <span data-ttu-id="97a99-107">Pode haver tantos elementos [relatedproperty]() dentro de um [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) , conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="97a99-107">There can be as many [relatedProperty]() elements within a [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) as needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="97a99-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="97a99-108">Syntax</span></span>


```
<!-- relatedPropertyInfo -->
<xs:element name="relatedProperty" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:attribute name="relationshipName" type="canonical-name" use="required"/>
        <xs:attribute name="propertyName" type="canonical-name" use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="97a99-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="97a99-109">Element Information</span></span>



| <span data-ttu-id="97a99-110">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="97a99-110">Parent Element</span></span>                                                   | <span data-ttu-id="97a99-111">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="97a99-111">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="97a99-112">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="97a99-112">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md) | <span data-ttu-id="97a99-113">Nenhum</span><span class="sxs-lookup"><span data-stu-id="97a99-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="97a99-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="97a99-114">Attributes</span></span>



| <span data-ttu-id="97a99-115">Atributo</span><span class="sxs-lookup"><span data-stu-id="97a99-115">Attribute</span></span>        | <span data-ttu-id="97a99-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="97a99-116">Description</span></span>                                                        |
|------------------|--------------------------------------------------------------------|
| <span data-ttu-id="97a99-117">relationshipName</span><span class="sxs-lookup"><span data-stu-id="97a99-117">relationshipName</span></span> | <span data-ttu-id="97a99-118">Público.</span><span class="sxs-lookup"><span data-stu-id="97a99-118">Public.</span></span> <span data-ttu-id="97a99-119">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="97a99-119">Required.</span></span> <span data-ttu-id="97a99-120">O nome canônico da relação de propriedade.</span><span class="sxs-lookup"><span data-stu-id="97a99-120">The canonical name of the property relationship.</span></span> |
| <span data-ttu-id="97a99-121">propertyName</span><span class="sxs-lookup"><span data-stu-id="97a99-121">propertyName</span></span>     | <span data-ttu-id="97a99-122">Público.</span><span class="sxs-lookup"><span data-stu-id="97a99-122">Public.</span></span> <span data-ttu-id="97a99-123">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="97a99-123">Required.</span></span> <span data-ttu-id="97a99-124">O nome canônico da propriedade relacionada.</span><span class="sxs-lookup"><span data-stu-id="97a99-124">The canonical name of the related property.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="97a99-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="97a99-125">Remarks</span></span>

<span data-ttu-id="97a99-126">Esse elemento permite mapear uma propriedade para outra.</span><span class="sxs-lookup"><span data-stu-id="97a99-126">This element enables you to map one property to another.</span></span> <span data-ttu-id="97a99-127">Por exemplo, você pode mapear o texto da propriedade personalizada, fabrikam. StorageCapacity, para System. Capacity:</span><span class="sxs-lookup"><span data-stu-id="97a99-127">For example, you can map the text of your custom property, Fabrikam.StorageCapacity, to System.Capacity:</span></span>


```
<!-- relatedPropertyInfo -->
<propertyDescription name="Fabrikam.StorageCapacity" ... >
    ...
    <relatedPropertyInfo>
        <relatedProperty relationshipName="System.RelatedProperty.Text" propertyName="System.Capacity"/>
    </relatedPropertyInfo>
</propertyDescription>
```



 

 
