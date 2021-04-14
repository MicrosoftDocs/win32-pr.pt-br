---
title: Tipo simples de nonEmptyStringType
description: Define os valores usados para uma cadeia de caracteres não vazia de texto.
ms.assetid: cb3b1ca6-4531-467c-a27a-b27a62233514
keywords:
- tipo simples não vazio Agendador de Tarefas
topic_type:
- apiref
api_name:
- nonEmptyString
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab9c9fa84c510fc4e67f6f63664a58d6d4093709
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369741"
---
# <a name="nonemptystringtype-simple-type"></a><span data-ttu-id="c2941-104">Tipo simples de nonEmptyStringType</span><span class="sxs-lookup"><span data-stu-id="c2941-104">nonEmptyStringType Simple Type</span></span>

<span data-ttu-id="c2941-105">Define os valores usados para uma cadeia de caracteres não vazia de texto.</span><span class="sxs-lookup"><span data-stu-id="c2941-105">Defines the values used for a non-empty string of text.</span></span>

``` syntax
<xs:simpleType name="nonEmptyString">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="c2941-106">Valores de enumeração</span><span class="sxs-lookup"><span data-stu-id="c2941-106">Enumeration values</span></span>

<span data-ttu-id="c2941-107">O tipo simples **Nonemptytype** define o valor a seguir.</span><span class="sxs-lookup"><span data-stu-id="c2941-107">The **nonEmptyString** simple type defines the following value.</span></span>



| <span data-ttu-id="c2941-108">Valor</span><span class="sxs-lookup"><span data-stu-id="c2941-108">Value</span></span> | <span data-ttu-id="c2941-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2941-109">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="c2941-110">1</span><span class="sxs-lookup"><span data-stu-id="c2941-110">1</span></span>     | <span data-ttu-id="c2941-111">A cadeia de caracteres contém pelo menos um caractere.</span><span class="sxs-lookup"><span data-stu-id="c2941-111">The string contains at least one character.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c2941-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2941-112">Requirements</span></span>



| <span data-ttu-id="c2941-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2941-113">Requirement</span></span> | <span data-ttu-id="c2941-114">Valor</span><span class="sxs-lookup"><span data-stu-id="c2941-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c2941-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2941-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c2941-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c2941-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c2941-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2941-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c2941-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c2941-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





