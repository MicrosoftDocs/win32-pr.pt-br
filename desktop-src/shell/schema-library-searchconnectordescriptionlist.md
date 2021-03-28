---
description: Esse <searchConnectorDescriptionList> elemento contém uma lista de conectores de pesquisa que são mapeados para locais incluídos nesta biblioteca. Cada conector de pesquisa é definido por um <searchConnectorDescription> elemento. Esse elemento é opcional e não tem atributos.
ms.assetid: 58A7BC21-0EB8-4bcf-98EE-31A56A4BC58C
title: Elemento searchConnectorDescriptionList (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d7295796f205ca0d20f220ba827abfd5470bdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968128"
---
# <a name="searchconnectordescriptionlist-element-library-schema"></a><span data-ttu-id="db8d5-105">Elemento searchConnectorDescriptionList (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="db8d5-105">searchConnectorDescriptionList Element (Library Schema)</span></span>

<span data-ttu-id="db8d5-106">Esse <searchConnectorDescriptionList> elemento contém uma lista de conectores de pesquisa que são mapeados para locais incluídos nesta biblioteca.</span><span class="sxs-lookup"><span data-stu-id="db8d5-106">This <searchConnectorDescriptionList> element contains a list of search connectors that map to locations included in this library.</span></span> <span data-ttu-id="db8d5-107">Cada conector de pesquisa é definido por um <searchConnectorDescription> elemento.</span><span class="sxs-lookup"><span data-stu-id="db8d5-107">Each search connector is defined by a <searchConnectorDescription> element.</span></span> <span data-ttu-id="db8d5-108">Esse elemento é opcional e não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="db8d5-108">This element is optional and has no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="db8d5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="db8d5-109">Syntax</span></span>

``` syntax
<!-- searchConnectorDescriptionList -->
    <xs:element name="searchConnectorDescriptionList" minOccurs="0">
          <xs:complexType>
            <xs:sequence minOccurs="0">
              <xs:element name="searchConnectorDescription" type="searchConnectorDescriptionType" minOccurs="0" maxOccurs="unbounded"/>
            </xs:sequence>
          </xs:complexType>
        </xs:element>
```

## <a name="element-information"></a><span data-ttu-id="db8d5-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="db8d5-110">Element Information</span></span>



| <span data-ttu-id="db8d5-111">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="db8d5-111">Parent Element</span></span>                                                               | <span data-ttu-id="db8d5-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="db8d5-112">Child Elements</span></span>                                                                                       |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="db8d5-113">Elemento libraryDescription (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="db8d5-113">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) | [<span data-ttu-id="db8d5-114">Elemento searchConnectorDescription (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="db8d5-114">searchConnectorDescription Element (Library Schema)</span></span>](schema-library-searchconnectordescription.md) |



 

## <a name="remarks"></a><span data-ttu-id="db8d5-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="db8d5-115">Remarks</span></span>

<span data-ttu-id="db8d5-116">Os conectores de pesquisa para a pesquisa federada do Windows e os escopos do manipulador de protocolo não podem ser incluídos em uma biblioteca.</span><span class="sxs-lookup"><span data-stu-id="db8d5-116">Search connectors for Windows Federated Search and protocol handler scopes cannot be included in a library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db8d5-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="db8d5-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db8d5-118">Esquema de descrição da biblioteca</span><span class="sxs-lookup"><span data-stu-id="db8d5-118">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

<span data-ttu-id="db8d5-119">[Esquema de descrição do conector de pesquisa](/previous-versions//dd743009(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="db8d5-119">[Search Connector Description Schema](/previous-versions//dd743009(v=vs.85))</span></span>
</dt> </dl>

 

 
