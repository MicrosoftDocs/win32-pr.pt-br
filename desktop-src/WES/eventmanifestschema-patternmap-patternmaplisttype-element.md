---
title: Elemento patternMap (PatternMapListType)
description: Define um mapeamento entre duas expressões regulares. Uma expressão é usada para localizar uma cadeia de caracteres correspondente na cadeia de caracteres da mensagem e a outra é usada para alterar a cadeia de caracteres antes que o serviço a Coloque novamente na cadeia de caracteres da mensagem.
ms.assetid: 5cf28d38-4cc3-4a7b-a64b-3ad1cb42ebef
keywords:
- EventLog do elemento patternMap
topic_type:
- apiref
api_name:
- patternMap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3ae29d60e39515a7c4b4db334f947abc44df5ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008796"
---
# <a name="patternmap-patternmaplisttype-element"></a><span data-ttu-id="62589-105">Elemento patternMap (PatternMapListType)</span><span class="sxs-lookup"><span data-stu-id="62589-105">patternMap (PatternMapListType) Element</span></span>

<span data-ttu-id="62589-106">Define um mapeamento entre duas expressões regulares.</span><span class="sxs-lookup"><span data-stu-id="62589-106">Defines a mapping between two regular expressions.</span></span> <span data-ttu-id="62589-107">Uma expressão é usada para localizar uma cadeia de caracteres correspondente na cadeia de caracteres da mensagem e a outra é usada para alterar a cadeia de caracteres antes que o serviço a Coloque novamente na cadeia de caracteres da mensagem.</span><span class="sxs-lookup"><span data-stu-id="62589-107">One expression is used to find a matching string in the message string, and the other is used to alter the string before the service places it back in the message string.</span></span>

``` syntax
<xs:element name="patternMap"
    type="PatternMapType"
 />
```

<span data-ttu-id="62589-108">O elemento **patternMap** é definido pelo tipo complexo [**PatternMapListType**](eventmanifestschema-patternmaplisttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="62589-108">The **patternMap** element is defined by the [**PatternMapListType**](eventmanifestschema-patternmaplisttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="62589-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62589-109">Requirements</span></span>



| <span data-ttu-id="62589-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="62589-110">Requirement</span></span> | <span data-ttu-id="62589-111">Valor</span><span class="sxs-lookup"><span data-stu-id="62589-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="62589-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62589-112">Minimum supported client</span></span><br/> | <span data-ttu-id="62589-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="62589-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="62589-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62589-114">Minimum supported server</span></span><br/> | <span data-ttu-id="62589-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="62589-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="62589-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="62589-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="62589-117">**Elemento pai**</span><span class="sxs-lookup"><span data-stu-id="62589-117">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="62589-118">**patternMaps (NamedQueryType)**</span><span class="sxs-lookup"><span data-stu-id="62589-118">**patternMaps (NamedQueryType)**</span></span>](eventmanifestschema-patternmaps-namedquerytype-element.md)
</dt> </dl>

 

 





