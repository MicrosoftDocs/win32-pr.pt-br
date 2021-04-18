---
description: O elemento booliano opcional <includeInStartMenuScope> especifica se esse conector de pesquisa deve ser incluído no escopo de pesquisa do menu iniciar.
ms.assetid: 934a3834-9ddc-4c15-b738-68ea74adc24c
title: Elemento includeInStartMenuScope (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 126d10a2b69dcec5057e732679c8531fd6e82bca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810686"
---
# <a name="includeinstartmenuscope-element-search-connector-schema"></a><span data-ttu-id="5f423-103">Elemento includeInStartMenuScope (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="5f423-103">includeInStartMenuScope Element (Search Connector Schema)</span></span>

<span data-ttu-id="5f423-104">O elemento booliano opcional <includeInStartMenuScope> especifica se esse conector de pesquisa deve ser incluído no escopo de pesquisa do menu iniciar.</span><span class="sxs-lookup"><span data-stu-id="5f423-104">The optional Boolean <includeInStartMenuScope> element specifies whether this search connector should be included in the Start menu search scope.</span></span> <span data-ttu-id="5f423-105">O valor padrão é true para conectores de pesquisa usando o sistema de arquivos como uma fonte de dados e false para conectores de pesquisa usados por manipuladores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="5f423-105">The default value is true for search connectors using the file system as a data source, and false for search connectors used by property handlers.</span></span> <span data-ttu-id="5f423-106">Este elemento não tem elementos filho e nenhum atributo.</span><span class="sxs-lookup"><span data-stu-id="5f423-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f423-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f423-107">Syntax</span></span>


```
<!-- includeInStartMenuScope -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="includeInStartMenuScope" type="xs:boolean" default="false" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="5f423-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="5f423-108">Element Information</span></span>



| <span data-ttu-id="5f423-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="5f423-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="5f423-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5f423-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="5f423-111">Elemento searchConnectorDescriptionType (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="5f423-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="5f423-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f423-112">Remarks</span></span>

<span data-ttu-id="5f423-113">Se você incluir o conector de pesquisa no escopo do menu Iniciar, os usuários poderão pesquisar seu local na caixa de pesquisa no menu iniciar.</span><span class="sxs-lookup"><span data-stu-id="5f423-113">If you include the search connector in the Start menu scope, users can search your location from the search box in the Start menu.</span></span>

## <a name="example"></a><span data-ttu-id="5f423-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="5f423-114">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <includeinStartMenuScope>true</includeinStartMenuScope>
    ...
</searchConnectionDescription>
```



 

 



