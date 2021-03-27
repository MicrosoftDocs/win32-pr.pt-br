---
description: O <folderType> elemento especifica um GUID para o tipo de pasta. Esse elemento será necessário se o <templateInfo> elemento existir, caso contrário, será opcional. Este elemento não tem atributos nem elementos filho.
title: Elemento FolderType (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 240550F0-B6AC-470e-8BF1-DB5A4068226B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c6d94906fa8c0debfa1ee49d95f5acd47aea2526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967477"
---
# <a name="foldertype-element-library-schema"></a><span data-ttu-id="8a9c6-105">Elemento FolderType (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="8a9c6-105">folderType Element (Library Schema)</span></span>

<span data-ttu-id="8a9c6-106">O <folderType> elemento especifica um GUID para o tipo de pasta.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-106">The <folderType> element specifies a GUID for the folder type.</span></span> <span data-ttu-id="8a9c6-107">Esse elemento será necessário se o <templateInfo> elemento existir, caso contrário, será opcional.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-107">This element is required if the <templateInfo> element exists, otherwise it is optional.</span></span> <span data-ttu-id="8a9c6-108">Este elemento não tem atributos nem elementos filho.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-108">This element has no attributes and no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a9c6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a9c6-109">Syntax</span></span>


```
<!-- folderType -->
    <xs:element name="templateInfo" minOccurs="0">
      <xs:complexType>
        <xs:all>
          <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
      </xs:complexType>
    </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="8a9c6-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="8a9c6-110">Element Information</span></span>



| <span data-ttu-id="8a9c6-111">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="8a9c6-111">Parent Element</span></span>                                                           | <span data-ttu-id="8a9c6-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="8a9c6-112">Child Elements</span></span> |
|--------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="8a9c6-113">Elemento templateInfo (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="8a9c6-113">templateInfo Element (Library Schema)</span></span>](schema-library-templateinfo.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="8a9c6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a9c6-114">Remarks</span></span>

<span data-ttu-id="8a9c6-115">A configuração de um tipo de pasta determina as colunas e os detalhes que aparecem no Windows Explorer por padrão.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-115">Setting a folder type determines the columns and details that appear in Windows Explorer by default.</span></span> <span data-ttu-id="8a9c6-116">Os identificadores de tipo de pasta ([**FOLDERTYPEID**](foldertypeid.md)) são GUIDs definidos em Shlguid. h.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-116">Folder type identifiers ([**FOLDERTYPEID**](foldertypeid.md)) are GUIDs defined in Shlguid.h.</span></span> <span data-ttu-id="8a9c6-117">A tabela a seguir lista os GUIDs de tipos de pasta comuns.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-117">The following table lists the GUIDs of common folder types.</span></span>



| <span data-ttu-id="8a9c6-118">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="8a9c6-118">Folder Type</span></span>      | <span data-ttu-id="8a9c6-119">GUID</span><span class="sxs-lookup"><span data-stu-id="8a9c6-119">GUID</span></span>                                   |
|------------------|----------------------------------------|
| <span data-ttu-id="8a9c6-120">Biblioteca genérica</span><span class="sxs-lookup"><span data-stu-id="8a9c6-120">Generic Library</span></span>  | <span data-ttu-id="8a9c6-121">{5f4eab9a-6833-4f61-899d-31cf46979d49}</span><span class="sxs-lookup"><span data-stu-id="8a9c6-121">{5f4eab9a-6833-4f61-899d-31cf46979d49}</span></span> |
| <span data-ttu-id="8a9c6-122">Bibliotecas de usuários</span><span class="sxs-lookup"><span data-stu-id="8a9c6-122">Users Libraries</span></span>  | <span data-ttu-id="8a9c6-123">{C4D98F09-6124-4fe0-9942-826416082DA9}</span><span class="sxs-lookup"><span data-stu-id="8a9c6-123">{C4D98F09-6124-4fe0-9942-826416082DA9}</span></span> |
| <span data-ttu-id="8a9c6-124">Pasta de documentos</span><span class="sxs-lookup"><span data-stu-id="8a9c6-124">Documents Folder</span></span> | <span data-ttu-id="8a9c6-125">{7D49D726-3C21-4F05-99AA-FDC2C9474656}</span><span class="sxs-lookup"><span data-stu-id="8a9c6-125">{7D49D726-3C21-4F05-99AA-FDC2C9474656}</span></span> |
| <span data-ttu-id="8a9c6-126">Pasta imagens</span><span class="sxs-lookup"><span data-stu-id="8a9c6-126">Pictures Folder</span></span>  | <span data-ttu-id="8a9c6-127">{B3690E58-E961-423B-B687-386EBFD83239}</span><span class="sxs-lookup"><span data-stu-id="8a9c6-127">{B3690E58-E961-423B-B687-386EBFD83239}</span></span> |
| <span data-ttu-id="8a9c6-128">Pasta vídeos</span><span class="sxs-lookup"><span data-stu-id="8a9c6-128">Videos Folder</span></span>    | <span data-ttu-id="8a9c6-129">{5fa96407-7e77-483c-ac93-691d05850de8}</span><span class="sxs-lookup"><span data-stu-id="8a9c6-129">{5fa96407-7e77-483c-ac93-691d05850de8}</span></span> |
| <span data-ttu-id="8a9c6-130">Pasta jogos</span><span class="sxs-lookup"><span data-stu-id="8a9c6-130">Games Folder</span></span>     | <span data-ttu-id="8a9c6-131">{b689b0d0-76d3-4cbb-87f7-585d0e0ce070}</span><span class="sxs-lookup"><span data-stu-id="8a9c6-131">{b689b0d0-76d3-4cbb-87f7-585d0e0ce070}</span></span> |
| <span data-ttu-id="8a9c6-132">Pasta de música</span><span class="sxs-lookup"><span data-stu-id="8a9c6-132">Music Folder</span></span>     | <span data-ttu-id="8a9c6-133">{94d6ddcc-4a68-4175-a374-bd584a510b78}</span><span class="sxs-lookup"><span data-stu-id="8a9c6-133">{94d6ddcc-4a68-4175-a374-bd584a510b78}</span></span> |
| <span data-ttu-id="8a9c6-134">Contatos</span><span class="sxs-lookup"><span data-stu-id="8a9c6-134">Contacts</span></span>         | <span data-ttu-id="8a9c6-135">{DE2B70EC-9BF7-4A93-BD3D-243F7881D492}</span><span class="sxs-lookup"><span data-stu-id="8a9c6-135">{DE2B70EC-9BF7-4A93-BD3D-243F7881D492}</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8a9c6-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8a9c6-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a9c6-137">Elemento iconReference (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="8a9c6-137">iconReference Element (Library Schema)</span></span>](schema-library-iconreference.md)
</dt> <dt>

[<span data-ttu-id="8a9c6-138">Elemento isLibraryPinned (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="8a9c6-138">isLibraryPinned Element (Library Schema)</span></span>](schema-library-islibrarypinned.md)
</dt> <dt>

[<span data-ttu-id="8a9c6-139">Elemento libraryDescription (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="8a9c6-139">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md)
</dt> <dt>

[<span data-ttu-id="8a9c6-140">Elemento Name (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="8a9c6-140">name Element (Library Schema)</span></span>](schema-library-name.md)
</dt> <dt>

[<span data-ttu-id="8a9c6-141">Elemento OwnerId (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="8a9c6-141">ownerSID Element (Library Schema)</span></span>](schema-library-ownersid.md)
</dt> <dt>

[<span data-ttu-id="8a9c6-142">Elemento propertyStore (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="8a9c6-142">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md)
</dt> <dt>

[<span data-ttu-id="8a9c6-143">Elemento searchConnectorDescription (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="8a9c6-143">searchConnectorDescription Element (Library Schema)</span></span>](schema-library-searchconnectordescription.md)
</dt> <dt>

[<span data-ttu-id="8a9c6-144">Elemento searchConnectorDescriptionList (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="8a9c6-144">searchConnectorDescriptionList Element (Library Schema)</span></span>](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="8a9c6-145">Elemento templateInfo (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="8a9c6-145">templateInfo Element (Library Schema)</span></span>](schema-library-templateinfo.md)
</dt> <dt>

[<span data-ttu-id="8a9c6-146">Elemento Version (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="8a9c6-146">version Element (Library Schema)</span></span>](schema-library-version.md)
</dt> </dl>

 

 



