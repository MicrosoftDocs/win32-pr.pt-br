---
description: O <dateCreated> elemento opcional identifica a data e a hora em que esse conector de pesquisa foi criado, usando o padrão ISO 8601. Ele não tem nenhum elemento filho e nenhum atributo.
ms.assetid: 96d8b067-b5ab-4d36-a8d7-1d084a9f661d
title: Elemento dateCreated (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6017c0555d464a49192c4fe8cb7e347bbab0e367
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646860"
---
# <a name="datecreated-element-search-connector-schema"></a><span data-ttu-id="89b89-104">Elemento dateCreated (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="89b89-104">dateCreated Element (Search Connector Schema)</span></span>

<span data-ttu-id="89b89-105">O <dateCreated> elemento opcional identifica a data e a hora em que esse conector de pesquisa foi criado, usando o padrão ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="89b89-105">The optional <dateCreated> element identifies the date and the time when this search connector was created, using the ISO 8601 standard.</span></span> <span data-ttu-id="89b89-106">Ele não tem nenhum elemento filho e nenhum atributo.</span><span class="sxs-lookup"><span data-stu-id="89b89-106">It has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="89b89-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="89b89-107">Syntax</span></span>


```
<!-- dateCreated -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="dateCreated" type="xs:dateTime" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="89b89-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="89b89-108">Element Information</span></span>



| <span data-ttu-id="89b89-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="89b89-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="89b89-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="89b89-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="89b89-111">Elemento searchConnectorDescriptionType (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="89b89-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="89b89-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="89b89-112">Remarks</span></span>

<span data-ttu-id="89b89-113">O formato do valor desse elemento segue o padrão ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="89b89-113">The format of the value of this element follows the ISO 8601 standard.</span></span> <span data-ttu-id="89b89-114">Um uso comum seria um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="89b89-114">A common use would be either of the following:</span></span>

-   <span data-ttu-id="89b89-115">\[Aaaa \] - \[ mm \] - \[ DD \] T \[ hh \] : \[ mm \] : \[ SS \] ± \[ hh \] : \[ mm \] ("1981-04-05T14:30:30-05:00")</span><span class="sxs-lookup"><span data-stu-id="89b89-115">\[YYYY\]-\[MM\]-\[DD\]T\[hh\]:\[mm\]:\[ss\]±\[hh\]:\[mm\] ("1981-04-05T14:30:30-05:00")</span></span>
-   <span data-ttu-id="89b89-116">\[AAAA \] \[ mm \] \[ DD \] T \[ hh \] \[ mm \] \[ SS \] Z ("19810405T193030Z")</span><span class="sxs-lookup"><span data-stu-id="89b89-116">\[YYYY\]\[MM\]\[DD\]T\[hh\]\[mm\]\[ss\]Z ("19810405T193030Z")</span></span>

## <a name="example"></a><span data-ttu-id="89b89-117">Exemplo</span><span class="sxs-lookup"><span data-stu-id="89b89-117">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <dateCreated>2009-04-05T12:00:00-05:00</dateCreated>
    ...
</searchConnectionDescription>
```



 

 



