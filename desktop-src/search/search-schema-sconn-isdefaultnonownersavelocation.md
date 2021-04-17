---
description: O elemento booliano opcional <isDefaultNonOwnerSaveLocation> especifica se o local descrito no conector de pesquisa deve ser usado como o local de salvamento padrão quando um usuário de outro computador em um grupo doméstico opta por salvar um item.
ms.assetid: 4286b122-2454-4dc3-9c06-9967b7a763dd
title: Elemento isDefaultNonOwnerSaveLocation (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edd39ab76ae1b99d6518ca40407d328f5da9778c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790491"
---
# <a name="isdefaultnonownersavelocation-element-search-connector-schema"></a><span data-ttu-id="eefb9-103">Elemento isDefaultNonOwnerSaveLocation (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="eefb9-103">isDefaultNonOwnerSaveLocation Element (Search Connector Schema)</span></span>

<span data-ttu-id="eefb9-104">O elemento booliano opcional <isDefaultNonOwnerSaveLocation> especifica se o local descrito no conector de pesquisa deve ser usado como o local de salvamento padrão quando um usuário de outro computador em um grupo doméstico opta por salvar um item.</span><span class="sxs-lookup"><span data-stu-id="eefb9-104">The optional Boolean <isDefaultNonOwnerSaveLocation> element specifies whether the location described in the search connector should be used as the default save location when a user from another computer in a Homegroup chooses to save an item.</span></span> <span data-ttu-id="eefb9-105">Este elemento não tem elementos filho e nenhum atributo.</span><span class="sxs-lookup"><span data-stu-id="eefb9-105">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="eefb9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="eefb9-106">Syntax</span></span>


```
<!-- isDefaultNonOwnerSaveLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isDefaultNonOwnerSaveLocation" type="xs:boolean" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="eefb9-107">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="eefb9-107">Element Information</span></span>



| <span data-ttu-id="eefb9-108">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="eefb9-108">Parent Element</span></span>                                                                                                   | <span data-ttu-id="eefb9-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="eefb9-109">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="eefb9-110">Elemento searchConnectorDescriptionType (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="eefb9-110">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="eefb9-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="eefb9-111">Remarks</span></span>

<span data-ttu-id="eefb9-112">Se for true, quando um usuário de outro computador em um grupo doméstico optar por salvar um item, o Windows Explorer salvará o item no local especificado no <simpleLocation> elemento.</span><span class="sxs-lookup"><span data-stu-id="eefb9-112">If true, when a user from another computer in a Homegroup chooses to save an item, Windows Explorer saves the item to the location specified in the <simpleLocation> element.</span></span>

## <a name="example"></a><span data-ttu-id="eefb9-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="eefb9-113">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



