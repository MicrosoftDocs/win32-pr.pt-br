---
description: O elemento booliano opcional <isDefaultSaveLocation> especifica se o local descrito no conector de pesquisa deve ser usado como o local de salvamento padrão. Este elemento não tem elementos filho e nenhum atributo.
ms.assetid: 4a33f411-d71e-41d3-b5fd-018a92dceeac
title: Elemento isDefaultSaveLocation (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b664e4cd6f7c88f1dfbeb44ba23faee5d24a43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296231"
---
# <a name="isdefaultsavelocation-element-search-connector-schema"></a><span data-ttu-id="e8cf7-104">Elemento isDefaultSaveLocation (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="e8cf7-104">isDefaultSaveLocation Element (Search Connector Schema)</span></span>

<span data-ttu-id="e8cf7-105">O elemento booliano opcional <isDefaultSaveLocation> especifica se o local descrito no conector de pesquisa deve ser usado como o local de salvamento padrão.</span><span class="sxs-lookup"><span data-stu-id="e8cf7-105">The optional Boolean <isDefaultSaveLocation> element specifies whether the location described in the search connector should be used as the default save location.</span></span> <span data-ttu-id="e8cf7-106">Este elemento não tem elementos filho e nenhum atributo.</span><span class="sxs-lookup"><span data-stu-id="e8cf7-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8cf7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8cf7-107">Syntax</span></span>


```
<!-- isDefaultSaveLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isDefaultSaveLocation" type="xs:boolean" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="e8cf7-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="e8cf7-108">Element Information</span></span>



| <span data-ttu-id="e8cf7-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="e8cf7-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="e8cf7-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="e8cf7-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="e8cf7-111">Elemento searchConnectorDescriptionType (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="e8cf7-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="e8cf7-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8cf7-112">Remarks</span></span>

<span data-ttu-id="e8cf7-113">Quando um usuário opta por salvar um item, o Windows Explorer salva o item no local especificado no <simpleLocation> elemento.</span><span class="sxs-lookup"><span data-stu-id="e8cf7-113">When a user chooses to save an item, Windows Explorer saves the item to the location specified in the <simpleLocation> element.</span></span> <span data-ttu-id="e8cf7-114">Os usuários podem alterar essa configuração usando a caixa de diálogo Propriedades do conector de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="e8cf7-114">Users can change this setting using the Properties dialog for the search connector.</span></span>

## <a name="example"></a><span data-ttu-id="e8cf7-115">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e8cf7-115">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultSaveLocation>true</isDefaultSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



