---
description: O <iconReference> elemento especifica um ícone personalizado para esta biblioteca. Esse elemento é opcional e não tem atributos ou elementos filho.
title: Elemento iconReference (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 7A35B014-1E01-4da2-AA64-4CFC3436C6D9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1f307ecd4fa523cc28881164869dca3329dfd698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988850"
---
# <a name="iconreference-element-library-schema"></a><span data-ttu-id="43e9b-104">Elemento iconReference (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="43e9b-104">iconReference Element (Library Schema)</span></span>

<span data-ttu-id="43e9b-105">O <iconReference> elemento especifica um ícone personalizado para esta biblioteca.</span><span class="sxs-lookup"><span data-stu-id="43e9b-105">The <iconReference> element specifies a custom icon for this library.</span></span> <span data-ttu-id="43e9b-106">Esse elemento é opcional e não tem atributos ou elementos filho.</span><span class="sxs-lookup"><span data-stu-id="43e9b-106">This element is optional and has no attributes or child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="43e9b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="43e9b-107">Syntax</span></span>


```
<!-- iconReference -->
    <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
```



## <a name="element-information"></a><span data-ttu-id="43e9b-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="43e9b-108">Element Information</span></span>



| <span data-ttu-id="43e9b-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="43e9b-109">Parent Element</span></span>                                                               | <span data-ttu-id="43e9b-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="43e9b-110">Child Elements</span></span> |
|------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="43e9b-111">Elemento libraryDescription (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="43e9b-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="43e9b-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="43e9b-112">Remarks</span></span>

<span data-ttu-id="43e9b-113">A referência do ícone deve ser especificada em um formato adequado para a função [**PathParseIconLocation**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa) .</span><span class="sxs-lookup"><span data-stu-id="43e9b-113">The icon reference must be specified in a form suitable for the [**PathParseIconLocation**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa) function.</span></span> <span data-ttu-id="43e9b-114">Por exemplo: `ModuleFileName,IconResourceIndex`.</span><span class="sxs-lookup"><span data-stu-id="43e9b-114">For example: `ModuleFileName,IconResourceIndex`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43e9b-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="43e9b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43e9b-116">Elemento FolderType (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="43e9b-116">folderType Element (Library Schema)</span></span>](schema-library-foldertype.md)
</dt> <dt>

[<span data-ttu-id="43e9b-117">Elemento isLibraryPinned (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="43e9b-117">isLibraryPinned Element (Library Schema)</span></span>](schema-library-islibrarypinned.md)
</dt> <dt>

[<span data-ttu-id="43e9b-118">Elemento libraryDescription (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="43e9b-118">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md)
</dt> <dt>

[<span data-ttu-id="43e9b-119">Elemento Name (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="43e9b-119">name Element (Library Schema)</span></span>](schema-library-name.md)
</dt> <dt>

[<span data-ttu-id="43e9b-120">Elemento OwnerId (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="43e9b-120">ownerSID Element (Library Schema)</span></span>](schema-library-ownersid.md)
</dt> <dt>

[<span data-ttu-id="43e9b-121">Elemento propertyStore (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="43e9b-121">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md)
</dt> <dt>

[<span data-ttu-id="43e9b-122">Elemento searchConnectorDescription (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="43e9b-122">searchConnectorDescription Element (Library Schema)</span></span>](schema-library-searchconnectordescription.md)
</dt> <dt>

[<span data-ttu-id="43e9b-123">Elemento searchConnectorDescriptionList (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="43e9b-123">searchConnectorDescriptionList Element (Library Schema)</span></span>](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="43e9b-124">Elemento templateInfo (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="43e9b-124">templateInfo Element (Library Schema)</span></span>](schema-library-templateinfo.md)
</dt> <dt>

[<span data-ttu-id="43e9b-125">Elemento Version (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="43e9b-125">version Element (Library Schema)</span></span>](schema-library-version.md)
</dt> </dl>

 

 



