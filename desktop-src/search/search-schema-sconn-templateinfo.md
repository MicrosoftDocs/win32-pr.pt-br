---
description: Esse <templateInfo> elemento opcional especifica um tipo de pasta para exibir os resultados de uma consulta nesse conector de pesquisa. Este elemento não tem atributos e apenas um filho obrigatório.
ms.assetid: fe42f589-5c47-4629-94eb-78dbaffa4112
title: Elemento templateInfo (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fd28780689b4d544f251bbaf1542bc379ecdaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763970"
---
# <a name="templateinfo-element-search-connector-schema"></a><span data-ttu-id="20347-104">Elemento templateInfo (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="20347-104">templateInfo Element (Search Connector Schema)</span></span>

<span data-ttu-id="20347-105">Esse <templateInfo> elemento opcional especifica um tipo de pasta para exibir os resultados de uma consulta nesse conector de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="20347-105">This optional <templateInfo> element specifies a folder type for displaying the results from a query over this search connector.</span></span> <span data-ttu-id="20347-106">Este elemento não tem atributos e apenas um filho obrigatório.</span><span class="sxs-lookup"><span data-stu-id="20347-106">This element has no attributes and only one mandatory child.</span></span>

## <a name="syntax"></a><span data-ttu-id="20347-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="20347-107">Syntax</span></span>


```
<!-- templateInfo -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="templateInfo" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="folderType" minOccurs="0"/>
                    </xs:all>
                </xs:complexType>
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="20347-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="20347-108">Element Information</span></span>



| <span data-ttu-id="20347-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="20347-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="20347-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="20347-110">Child Elements</span></span>                                                                     |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="20347-111">Elemento searchConnectorDescriptionType (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="20347-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="20347-112">Elemento FolderType (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="20347-112">folderType Element (Search Connector Schema)</span></span>](search-schema-sconn-foldertype.md) |



 

## <a name="remarks"></a><span data-ttu-id="20347-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="20347-113">Remarks</span></span>

<span data-ttu-id="20347-114">Se você não especificar um tipo de pasta específico no <templateInfo> elemento, o Windows usará o tipo de pasta do conector de pesquisa geral {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}.</span><span class="sxs-lookup"><span data-stu-id="20347-114">If you don't specify a particular folder type in the <templateInfo> element, Windows uses the general search connector folder type {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}.</span></span>

## <a name="example-of-a-templateinfo-element"></a><span data-ttu-id="20347-115">Exemplo de um elemento templateInfo</span><span class="sxs-lookup"><span data-stu-id="20347-115">Example of a templateInfo Element</span></span>


```
<!-- templateInfo -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



