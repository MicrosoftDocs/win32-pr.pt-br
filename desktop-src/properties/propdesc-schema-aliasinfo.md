---
description: Especifica um alias de classificação ou uma lista de aliases de classificação especificando um elemento que contém uma propriedade de classificação ou uma lista de propriedades de classificação.
ms.assetid: 4c514197-0df0-49c6-b39e-8a2a7cefa93d
title: aliasInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 052409864617bdaba7acbf9ae561752c83d18395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814504"
---
# <a name="aliasinfo"></a><span data-ttu-id="64e36-103">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="64e36-103">aliasInfo</span></span>

<span data-ttu-id="64e36-104">Especifica um alias de classificação ou uma lista de aliases de classificação especificando um elemento que contém uma propriedade de classificação ou uma lista de propriedades de classificação.</span><span class="sxs-lookup"><span data-stu-id="64e36-104">Specifies a sort alias or list of sort aliases by specifying an element that contains a sort property or list of sort properties.</span></span> <span data-ttu-id="64e36-105">Deve haver apenas um elemento [aliasInfo]() para cada elemento [propertyDescription](./propdesc-schema-propertydescription.md) .</span><span class="sxs-lookup"><span data-stu-id="64e36-105">There should be only one [aliasInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md) element.</span></span> <span data-ttu-id="64e36-106">Para propriedades que definem cangroupby = true, a menos que uma propriedade de classificação secundária seja especificada ( aliasInfo/@additionalSortByAliases = prop: example), o usuário pode experimentar um comportamento inesperado ao alterar a ordem de classificação em uma exibição que é agrupada pela propriedade.</span><span class="sxs-lookup"><span data-stu-id="64e36-106">For properties that set canGroupBy=true, unless a secondary sort property is specified (aliasInfo/@additionalSortByAliases=prop:example), the user may experience unexpected behavior when changing the sort order in a view that is grouped by the property.</span></span> <span data-ttu-id="64e36-107">Especificamente, a ordem dos grupos será alterada, mas a ordem dos itens nos grupos não será.</span><span class="sxs-lookup"><span data-stu-id="64e36-107">Specifically, the order of the groups will change, but the order of items within the groups will not.</span></span>

## <a name="syntax"></a><span data-ttu-id="64e36-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="64e36-108">Syntax</span></span>


```
<!-- aliasInfo -->
<xs:element name="aliasInfo">
    <xs:complexType>
        <xs:attribute name="sortByAlias" type="canonical-name"/>
        <xs:attribute name="additionalSortByAliases" type="proplist"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="64e36-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="64e36-109">Element Information</span></span>



| <span data-ttu-id="64e36-110">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="64e36-110">Parent Element</span></span>                                                   | <span data-ttu-id="64e36-111">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="64e36-111">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="64e36-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="64e36-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | <span data-ttu-id="64e36-113">Nenhum</span><span class="sxs-lookup"><span data-stu-id="64e36-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="64e36-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="64e36-114">Attributes</span></span>



| <span data-ttu-id="64e36-115">Atributo</span><span class="sxs-lookup"><span data-stu-id="64e36-115">Attribute</span></span>               | <span data-ttu-id="64e36-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="64e36-116">Description</span></span>                                                                                                                                                            |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64e36-117">sortByAlias</span><span class="sxs-lookup"><span data-stu-id="64e36-117">sortByAlias</span></span>             | <span data-ttu-id="64e36-118">Público.</span><span class="sxs-lookup"><span data-stu-id="64e36-118">Public.</span></span> <span data-ttu-id="64e36-119">Opcional.</span><span class="sxs-lookup"><span data-stu-id="64e36-119">Optional.</span></span> <span data-ttu-id="64e36-120">O nome canônico da propriedade que deve ser usada para classificar.</span><span class="sxs-lookup"><span data-stu-id="64e36-120">The canonical name of the property that should be used to sort by.</span></span> <span data-ttu-id="64e36-121">Essa cadeia de caracteres é do tipo canônico.</span><span class="sxs-lookup"><span data-stu-id="64e36-121">This string is of type canonical-type.</span></span>                                            |
| <span data-ttu-id="64e36-122">additionalSortByAliases</span><span class="sxs-lookup"><span data-stu-id="64e36-122">additionalSortByAliases</span></span> | <span data-ttu-id="64e36-123">Público.</span><span class="sxs-lookup"><span data-stu-id="64e36-123">Public.</span></span> <span data-ttu-id="64e36-124">Opcional.</span><span class="sxs-lookup"><span data-stu-id="64e36-124">Optional.</span></span> <span data-ttu-id="64e36-125">Uma lista delimitada por ponto e vírgula de propriedades adicionais a serem usadas durante a classificação.</span><span class="sxs-lookup"><span data-stu-id="64e36-125">A semi-colon delimited list of additional properties to be used when sorting.</span></span> <span data-ttu-id="64e36-126">As propriedades são aplicadas à classificação na sequência em que são dadas.</span><span class="sxs-lookup"><span data-stu-id="64e36-126">The properties are applied to the sort in the sequence they are given.</span></span> |



 

 

 
