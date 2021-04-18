---
title: Tipo complexo NamedQueryType
description: Não usado. Define uma lista de consultas nomeadas que consultam a cadeia de caracteres de mensagem de evento para um valor e executam uma ação especificada, se encontradas. | Tipo complexo NamedQueryType
ms.assetid: 2606094d-ae1b-4a3f-a78f-30659fa141ab
keywords:
- Log de eventos do tipo complexo NamedQueryType
topic_type:
- apiref
api_name:
- NamedQueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e296847cbed635d88f4fa58efa53fda030affffe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105759767"
---
# <a name="namedquerytype-complex-type"></a><span data-ttu-id="5c7a2-106">Tipo complexo NamedQueryType</span><span class="sxs-lookup"><span data-stu-id="5c7a2-106">NamedQueryType Complex Type</span></span>

<span data-ttu-id="5c7a2-107">Não usado.</span><span class="sxs-lookup"><span data-stu-id="5c7a2-107">Not used.</span></span> <span data-ttu-id="5c7a2-108">Define uma lista de consultas nomeadas que consultam a cadeia de caracteres de mensagem de evento para um valor e executam uma ação especificada, se encontradas.</span><span class="sxs-lookup"><span data-stu-id="5c7a2-108">Defines a list of named queries that query the event message string for a value and perform a specified action if found.</span></span>

``` syntax
<xs:complexType name="NamedQueryType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="patternMaps"
            type="PatternMapListType"
         />
        <xs:any
            processContents="lax"
            maxOccurs="unbounded"
            minOccurs="0"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="5c7a2-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5c7a2-109">Child elements</span></span>



| <span data-ttu-id="5c7a2-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="5c7a2-110">Element</span></span>                                                                       | <span data-ttu-id="5c7a2-111">Type</span><span class="sxs-lookup"><span data-stu-id="5c7a2-111">Type</span></span>                                                                             | <span data-ttu-id="5c7a2-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="5c7a2-112">Description</span></span>                                                                                      |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c7a2-113">**patternMaps**</span><span class="sxs-lookup"><span data-stu-id="5c7a2-113">**patternMaps**</span></span>](eventmanifestschema-patternmaps-namedquerytype-element.md) | [<span data-ttu-id="5c7a2-114">**PatternMapListType**</span><span class="sxs-lookup"><span data-stu-id="5c7a2-114">**PatternMapListType**</span></span>](eventmanifestschema-patternmaplisttype-complextype.md) | <span data-ttu-id="5c7a2-115">Define uma lista de pares de expressões regulares que são usados para alterar a cadeia de caracteres da mensagem.</span><span class="sxs-lookup"><span data-stu-id="5c7a2-115">Defines a list of regular expression pairs that are used to alter the message string.</span></span><br/> |



## <a name="examples"></a><span data-ttu-id="5c7a2-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5c7a2-116">Examples</span></span>

<span data-ttu-id="5c7a2-117">O exemplo a seguir mostra como usar o elemento [**namedQueries**](eventmanifestschema-namedqueries-metadatatype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5c7a2-117">The following example shows how to use the [**namedQueries**](eventmanifestschema-namedqueries-metadatatype-element.md) element.</span></span> <span data-ttu-id="5c7a2-118">Este exemplo usa o conteúdo da cadeia de caracteres de mensagem e o insere na cadeia de caracteres https://www .*. com.*</span><span class="sxs-lookup"><span data-stu-id="5c7a2-118">This example takes the contents of the message string and inserts it into the string https://www.*messagestring*.com.</span></span> <span data-ttu-id="5c7a2-119">Em seguida, ele substitui a cadeia de caracteres da mensagem pelo resultado.</span><span class="sxs-lookup"><span data-stu-id="5c7a2-119">It then replaces the message string with the result.</span></span> <span data-ttu-id="5c7a2-120">Por exemplo, se a cadeia de caracteres de mensagem contiver a Microsoft, a consulta substituiria a cadeia de caracteres de mensagem da Microsoft por https://www.Microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="5c7a2-120">For example, if the message string contained Microsoft, the query would replace the Microsoft message string with https://www.Microsoft.com.</span></span>


```XML
<namedqueries>
   <patternmap name="SearchStrings" format="winrxv1">
       <map name="/${1}/" value="/http:\/\/www\.*\.com\/"/>
   </patternmap>
</namedqueries>
```



## <a name="requirements"></a><span data-ttu-id="5c7a2-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c7a2-121">Requirements</span></span>



| <span data-ttu-id="5c7a2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c7a2-122">Requirement</span></span> | <span data-ttu-id="5c7a2-123">Valor</span><span class="sxs-lookup"><span data-stu-id="5c7a2-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5c7a2-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c7a2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5c7a2-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5c7a2-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5c7a2-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c7a2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5c7a2-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5c7a2-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





