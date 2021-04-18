---
title: Tipo complexo
description: Define uma lista de palavras-chave que categorizam eventos. | Tipo complexo
ms.assetid: 7aeb5ca1-b23f-40f5-a77b-894deaf9c6bb
keywords:
- Log de tipos de tipo complexo de
topic_type:
- apiref
api_name:
- KeywordListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7132e2e85015aaf9d38adbd6278ea4d3e1296446
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105781479"
---
# <a name="keywordlisttype-complex-type"></a><span data-ttu-id="d0b55-105">Tipo complexo</span><span class="sxs-lookup"><span data-stu-id="d0b55-105">KeywordListType Complex Type</span></span>

<span data-ttu-id="d0b55-106">Define uma lista de palavras-chave que categorizam eventos.</span><span class="sxs-lookup"><span data-stu-id="d0b55-106">Defines a list of keywords that categorize events.</span></span>

``` syntax
<xs:complexType name="KeywordListType">
    <xs:sequence>
        <xs:element name="keyword"
            type="KeywordType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="d0b55-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d0b55-107">Child elements</span></span>



| <span data-ttu-id="d0b55-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="d0b55-108">Element</span></span>                                                                | <span data-ttu-id="d0b55-109">Type</span><span class="sxs-lookup"><span data-stu-id="d0b55-109">Type</span></span>                                                               | <span data-ttu-id="d0b55-110">Description</span><span class="sxs-lookup"><span data-stu-id="d0b55-110">Description</span></span>                                                                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d0b55-111">**chaves**</span><span class="sxs-lookup"><span data-stu-id="d0b55-111">**keyword**</span></span>](eventmanifestschema-keyword-keywordlisttype-element.md) | [<span data-ttu-id="d0b55-112">**Keywordtype**</span><span class="sxs-lookup"><span data-stu-id="d0b55-112">**KeywordType**</span></span>](eventmanifestschema-keywordtype-complextype.md) | <span data-ttu-id="d0b55-113">Define uma palavra-chave que identifica uma categoria de eventos.</span><span class="sxs-lookup"><span data-stu-id="d0b55-113">Defines a keyword that identifies a category of events.</span></span> <span data-ttu-id="d0b55-114">Você pode especificar um máximo de 48 palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="d0b55-114">You can specify a maximum of 48 keywords.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d0b55-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0b55-115">Requirements</span></span>



| <span data-ttu-id="d0b55-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0b55-116">Requirement</span></span> | <span data-ttu-id="d0b55-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d0b55-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d0b55-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0b55-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d0b55-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d0b55-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d0b55-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0b55-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d0b55-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d0b55-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





