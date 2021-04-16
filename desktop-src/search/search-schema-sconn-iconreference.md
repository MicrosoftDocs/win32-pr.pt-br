---
description: O <iconReference> elemento opcional especifica um ícone personalizado para esse local. Este elemento não tem atributos nem elementos filho.
ms.assetid: c2fa5e99-a7fd-423e-9952-5233e8c83619
title: Elemento iconReference (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c181efe3bb8ac04f08d4fa16016d3468af6f10c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501459"
---
# <a name="iconreference-element-search-connector-schema"></a><span data-ttu-id="a8893-104">Elemento iconReference (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="a8893-104">iconReference Element (Search Connector Schema)</span></span>

<span data-ttu-id="a8893-105">O <iconReference> elemento opcional especifica um ícone personalizado para esse local.</span><span class="sxs-lookup"><span data-stu-id="a8893-105">The optional <iconReference> element specifies a custom icon for this location.</span></span> <span data-ttu-id="a8893-106">Este elemento não tem atributos nem elementos filho.</span><span class="sxs-lookup"><span data-stu-id="a8893-106">This element has no attributes and no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8893-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8893-107">Syntax</span></span>


```
<!-- iconReference -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
            <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="a8893-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a8893-108">Element Information</span></span>



| <span data-ttu-id="a8893-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="a8893-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="a8893-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a8893-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="a8893-111">Elemento searchConnectorDescriptionType (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="a8893-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="a8893-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8893-112">Remarks</span></span>

<span data-ttu-id="a8893-113">O formato da referência deve ser especificado em um formato adequado para a função [PathParseIconLocation](/windows/desktop/api/shlwapi/nf-shlwapi-pathparseiconlocationa) : (por exemplo, <dll file name> <icon index> ).</span><span class="sxs-lookup"><span data-stu-id="a8893-113">The format of the reference must be specified in a form suitable for the [PathParseIconLocation](/windows/desktop/api/shlwapi/nf-shlwapi-pathparseiconlocationa) function: (for example, <dll file name>,<icon index>).</span></span>

## <a name="example"></a><span data-ttu-id="a8893-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a8893-114">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <iconReference>example.dll,-1002</iconReference>
    ...
</searchConnectionDescription>
```



 

 
