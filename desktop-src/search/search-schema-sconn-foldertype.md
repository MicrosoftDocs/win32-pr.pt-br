---
description: O <folderType> elemento Especifica o GUID para o tipo de pasta. Esse elemento será necessário se o <templateInfo> elemento existir. Ele não tem nenhum atributo e nenhum elemento filho.
ms.assetid: 2361bbf5-adeb-4189-a8ff-5fdd1c9b0ec6
title: Elemento FolderType (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7d2a9e7f83dbe225427a8370cd8f5e948a46cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104460980"
---
# <a name="foldertype-element-search-connector-schema"></a><span data-ttu-id="1ba72-105">Elemento FolderType (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="1ba72-105">folderType Element (Search Connector Schema)</span></span>

<span data-ttu-id="1ba72-106">O <folderType> elemento Especifica o GUID para o tipo de pasta.</span><span class="sxs-lookup"><span data-stu-id="1ba72-106">The <folderType> element specifies GUID for the folder type.</span></span> <span data-ttu-id="1ba72-107">Esse elemento será necessário se o <templateInfo> elemento existir.</span><span class="sxs-lookup"><span data-stu-id="1ba72-107">This element is required if the <templateInfo> element exists.</span></span> <span data-ttu-id="1ba72-108">Ele não tem nenhum atributo e nenhum elemento filho.</span><span class="sxs-lookup"><span data-stu-id="1ba72-108">It has no attributes and no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ba72-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ba72-109">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="1ba72-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="1ba72-110">Element Information</span></span>



| <span data-ttu-id="1ba72-111">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="1ba72-111">Parent Element</span></span>                                                                         | <span data-ttu-id="1ba72-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1ba72-112">Child Elements</span></span> |
|----------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="1ba72-113">Elemento templateInfo (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="1ba72-113">templateInfo Element (Search Connector Schema)</span></span>](search-schema-sconn-templateinfo.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="1ba72-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ba72-114">Remarks</span></span>

<span data-ttu-id="1ba72-115">O GUID padrão é {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}, um tipo de pasta geral para conectores de pesquisa federada (OpenSearch).</span><span class="sxs-lookup"><span data-stu-id="1ba72-115">The default GUID is {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}, a general folder type for federated search (OpenSearch) connectors.</span></span>

## <a name="example-of-a-foldertype-element"></a><span data-ttu-id="1ba72-116">Exemplo de um elemento FolderType</span><span class="sxs-lookup"><span data-stu-id="1ba72-116">Example of a folderType Element</span></span>


```
<!-- templateInfo and folderType -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



