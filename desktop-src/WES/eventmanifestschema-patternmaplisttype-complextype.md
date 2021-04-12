---
title: Tipo complexo PatternMapListType
description: Não usado. Define uma lista de pares de expressões regulares que são usados para alterar a cadeia de caracteres da mensagem.
ms.assetid: f7b92821-a959-4b91-9e7e-47d0136ee61f
keywords:
- Log de eventos do tipo complexo PatternMapListType
topic_type:
- apiref
api_name:
- PatternMapListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5d1bb655dcf13c70fb989756cb9f5716301934c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294745"
---
# <a name="patternmaplisttype-complex-type"></a><span data-ttu-id="f757d-105">Tipo complexo PatternMapListType</span><span class="sxs-lookup"><span data-stu-id="f757d-105">PatternMapListType Complex Type</span></span>

<span data-ttu-id="f757d-106">Não usado.</span><span class="sxs-lookup"><span data-stu-id="f757d-106">Not used.</span></span> <span data-ttu-id="f757d-107">Define uma lista de pares de expressões regulares que são usados para alterar a cadeia de caracteres da mensagem.</span><span class="sxs-lookup"><span data-stu-id="f757d-107">Defines a list of regular expression pairs that are used to alter the message string.</span></span>

``` syntax
<xs:complexType name="PatternMapListType">
    <xs:sequence>
        <xs:element name="patternMap"
            type="PatternMapType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="f757d-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f757d-108">Child elements</span></span>



| <span data-ttu-id="f757d-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="f757d-109">Element</span></span>                                                                         | <span data-ttu-id="f757d-110">Type</span><span class="sxs-lookup"><span data-stu-id="f757d-110">Type</span></span>                                                                     | <span data-ttu-id="f757d-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="f757d-111">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f757d-112">**patternMap**</span><span class="sxs-lookup"><span data-stu-id="f757d-112">**patternMap**</span></span>](eventmanifestschema-patternmap-patternmaplisttype-element.md) | [<span data-ttu-id="f757d-113">**PatternMapType**</span><span class="sxs-lookup"><span data-stu-id="f757d-113">**PatternMapType**</span></span>](eventmanifestschema-patternmaptype-complextype.md) | <span data-ttu-id="f757d-114">Define um mapeamento entre duas expressões regulares.</span><span class="sxs-lookup"><span data-stu-id="f757d-114">Defines a mapping between two regular expressions.</span></span> <span data-ttu-id="f757d-115">Uma expressão é usada para localizar uma cadeia de caracteres correspondente na cadeia de caracteres de mensagem e a outra é usada para alterar a cadeia de caracteres antes que o serviço a Coloque novamente na cadeia de caracteres de mensagem.</span><span class="sxs-lookup"><span data-stu-id="f757d-115">One expression is used to find a matching string in the message string and the other is used to alter the string before the service places it back in the message string.</span></span> <span data-ttu-id="f757d-116">O primeiro mapeamento de padrão que corresponde a é usado e outros padrões não são tentados.</span><span class="sxs-lookup"><span data-stu-id="f757d-116">The first pattern mapping that matches is used and other patterns are not tried.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f757d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f757d-117">Requirements</span></span>



| <span data-ttu-id="f757d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f757d-118">Requirement</span></span> | <span data-ttu-id="f757d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f757d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f757d-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f757d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f757d-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f757d-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f757d-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f757d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f757d-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f757d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





