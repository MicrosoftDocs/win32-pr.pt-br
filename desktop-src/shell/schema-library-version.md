---
description: O <version> elemento Especifica a versão de conteúdo desta biblioteca. Este elemento não tem atributos nem elementos filho.
ms.assetid: 77FD5EF6-6B6F-48e1-973F-AC069F729613
title: Elemento Version (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7b16a6078a16f4ebbe5e995503114996572f1b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967474"
---
# <a name="version-element-library-schema"></a><span data-ttu-id="b2e19-104">Elemento Version (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="b2e19-104">version Element (Library Schema)</span></span>

<span data-ttu-id="b2e19-105">O <version> elemento Especifica a versão de conteúdo desta biblioteca.</span><span class="sxs-lookup"><span data-stu-id="b2e19-105">The <version> element specifies the content version of this library.</span></span> <span data-ttu-id="b2e19-106">Este elemento não tem atributos nem elementos filho.</span><span class="sxs-lookup"><span data-stu-id="b2e19-106">This element has no attributes and no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2e19-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2e19-107">Syntax</span></span>

``` syntax
<!-- version -->
<xs:element name="version" type="xs:int" minOccurs="0"/>
```

## <a name="element-information"></a><span data-ttu-id="b2e19-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="b2e19-108">Element Information</span></span>



| <span data-ttu-id="b2e19-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="b2e19-109">Parent Element</span></span>                                                               | <span data-ttu-id="b2e19-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="b2e19-110">Child Elements</span></span> |
|------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="b2e19-111">Elemento libraryDescription (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="b2e19-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) | <span data-ttu-id="b2e19-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b2e19-112">None</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="b2e19-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2e19-113">Remarks</span></span>

<span data-ttu-id="b2e19-114">A versão de conteúdo da biblioteca é diferente da versão do formato de arquivo da biblioteca ( \* . Library-MS).</span><span class="sxs-lookup"><span data-stu-id="b2e19-114">The content version of the library is different from the library's file format (\*.library-ms) version.</span></span> <span data-ttu-id="b2e19-115">A versão de formato de arquivo da biblioteca é especificada no [namespace](library-schema-entry.md).</span><span class="sxs-lookup"><span data-stu-id="b2e19-115">The library's file format version is specified in the [namespace](library-schema-entry.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2e19-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b2e19-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2e19-117">Esquema de descrição da biblioteca</span><span class="sxs-lookup"><span data-stu-id="b2e19-117">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="b2e19-118">Esquema de descrição do conector de pesquisa</span><span class="sxs-lookup"><span data-stu-id="b2e19-118">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
