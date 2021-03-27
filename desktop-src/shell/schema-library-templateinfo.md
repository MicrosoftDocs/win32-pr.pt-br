---
description: O <templateInfo> elemento é um contêiner para o elemento FolderType, que especifica um tipo de pasta para exibir os resultados de uma consulta nessa biblioteca. Esse elemento é opcional e não tem atributos.
ms.assetid: C555097A-E7B8-45ef-8CFA-19CFBC5E9D5A
title: Elemento templateInfo (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dae06a57a1b30407e2513e03f30ae6a4da13e849
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502073"
---
# <a name="templateinfo-element-library-schema"></a><span data-ttu-id="c4249-104">Elemento templateInfo (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="c4249-104">templateInfo Element (Library Schema)</span></span>

<span data-ttu-id="c4249-105">O <templateInfo> elemento é um contêiner para o elemento [FolderType](schema-library-foldertype.md) , que especifica um tipo de pasta para exibir os resultados de uma consulta nessa biblioteca.</span><span class="sxs-lookup"><span data-stu-id="c4249-105">The <templateInfo> element is a container for the [folderType](schema-library-foldertype.md) element, which specifies a folder type for displaying the results from a query over this library.</span></span> <span data-ttu-id="c4249-106">Esse elemento é opcional e não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="c4249-106">This element is optional and has no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4249-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4249-107">Syntax</span></span>

``` syntax
<!-- templateInfo -->
<xs:element name="templateInfo" minOccurs="0">
    <xs:complexType>
        <xs:all>
            <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a><span data-ttu-id="c4249-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="c4249-108">Element Information</span></span>



| <span data-ttu-id="c4249-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="c4249-109">Parent Element</span></span>                                                               | <span data-ttu-id="c4249-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="c4249-110">Child Elements</span></span>                                                             |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="c4249-111">Elemento libraryDescription (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="c4249-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) | [<span data-ttu-id="c4249-112">Elemento FolderType (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="c4249-112">folderType Element (Library Schema)</span></span>](schema-library-foldertype.md)       |
|                                                                              | [<span data-ttu-id="c4249-113">Elemento propertyStore (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="c4249-113">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md) |



 

## <a name="related-topics"></a><span data-ttu-id="c4249-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c4249-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4249-115">Esquema de descrição da biblioteca</span><span class="sxs-lookup"><span data-stu-id="c4249-115">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

<span data-ttu-id="c4249-116">[Esquema de descrição do conector de pesquisa](/previous-versions//dd743009(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c4249-116">[Search Connector Description Schema](/previous-versions//dd743009(v=vs.85))</span></span>
</dt> </dl>

 

 
