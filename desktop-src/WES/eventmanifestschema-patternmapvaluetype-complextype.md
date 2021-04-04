---
title: Tipo complexo PatternMapValueType
description: Não usado. Define as expressões regulares usadas para localizar uma cadeia de caracteres correspondente na cadeia de caracteres da mensagem e alterá-la.
ms.assetid: 2ae8a268-64c0-45d1-8339-988b13d884a3
keywords:
- Log de eventos do tipo complexo PatternMapValueType
topic_type:
- apiref
api_name:
- PatternMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55b57b63f3e5c9e5a5c4cd15974c89f6d28439f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644207"
---
# <a name="patternmapvaluetype-complex-type"></a><span data-ttu-id="e3777-105">Tipo complexo PatternMapValueType</span><span class="sxs-lookup"><span data-stu-id="e3777-105">PatternMapValueType Complex Type</span></span>

<span data-ttu-id="e3777-106">Não usado.</span><span class="sxs-lookup"><span data-stu-id="e3777-106">Not used.</span></span> <span data-ttu-id="e3777-107">Define as expressões regulares usadas para localizar uma cadeia de caracteres correspondente na cadeia de caracteres da mensagem e alterá-la.</span><span class="sxs-lookup"><span data-stu-id="e3777-107">Defines the regular expressions used to find a matching string in the message string and alter it.</span></span>

``` syntax
<xs:complexType name="PatternMapValueType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="string"
                use="required"
             />
            <xs:attribute name="value"
                type="string"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="e3777-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e3777-108">Attributes</span></span>



| <span data-ttu-id="e3777-109">Nome</span><span class="sxs-lookup"><span data-stu-id="e3777-109">Name</span></span>  | <span data-ttu-id="e3777-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3777-110">Type</span></span>   | <span data-ttu-id="e3777-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3777-111">Description</span></span>                                                                                               |
|-------|--------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3777-112">name</span><span class="sxs-lookup"><span data-stu-id="e3777-112">name</span></span>  | <span data-ttu-id="e3777-113">string</span><span class="sxs-lookup"><span data-stu-id="e3777-113">string</span></span> | <span data-ttu-id="e3777-114">A expressão regular usada para localizar uma cadeia de caracteres correspondente na cadeia de caracteres da mensagem.</span><span class="sxs-lookup"><span data-stu-id="e3777-114">The regular expression used to find a matching string in the message string.</span></span><br/>                   |
| <span data-ttu-id="e3777-115">value</span><span class="sxs-lookup"><span data-stu-id="e3777-115">value</span></span> | <span data-ttu-id="e3777-116">string</span><span class="sxs-lookup"><span data-stu-id="e3777-116">string</span></span> | <span data-ttu-id="e3777-117">A expressão regular usada para alterar a cadeia de caracteres correspondente encontrada na cadeia de caracteres da mensagem.</span><span class="sxs-lookup"><span data-stu-id="e3777-117">The regular expression used to alter the matching string that was found in the message string.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e3777-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3777-118">Requirements</span></span>



| <span data-ttu-id="e3777-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3777-119">Requirement</span></span> | <span data-ttu-id="e3777-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e3777-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e3777-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3777-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e3777-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e3777-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e3777-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3777-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e3777-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e3777-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





