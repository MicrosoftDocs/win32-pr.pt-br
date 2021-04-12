---
description: Define o tipo que contém valores válidos para o atributo Type para o elemento Margin.
ms.assetid: 5448ead5-0249-4cc7-9f2a-d2181e2af734
title: Tipo simples de MarginTypeType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MarginTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4e8a09e98611fabc54a029c9cac9cb37dfc1373f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171532"
---
# <a name="margintypetype-simple-type"></a><span data-ttu-id="dbb73-103">Tipo simples de MarginTypeType</span><span class="sxs-lookup"><span data-stu-id="dbb73-103">MarginTypeType Simple Type</span></span>

<span data-ttu-id="dbb73-104">Define o tipo que contém valores válidos para o atributo **Type** para o [elemento Margin](margin-element.md).</span><span class="sxs-lookup"><span data-stu-id="dbb73-104">Defines the type that contains valid values for the **Type** attribute for the [Margin element](margin-element.md).</span></span>

``` syntax
<xs:simpleType name="MarginTypeType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="Left|Right"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="dbb73-105">Padrões</span><span class="sxs-lookup"><span data-stu-id="dbb73-105">Patterns</span></span>

<span data-ttu-id="dbb73-106">O tipo simples **MarginTypeType** é uma **cadeia de caracteres** que é restrita pelo seguinte padrão:</span><span class="sxs-lookup"><span data-stu-id="dbb73-106">The **MarginTypeType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `Left|Right`

## <a name="remarks"></a><span data-ttu-id="dbb73-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="dbb73-107">Remarks</span></span>

<span data-ttu-id="dbb73-108">Os valores válidos para o atributo **Type** para o [elemento Margin](margin-element.md) são "Left" e "Right".</span><span class="sxs-lookup"><span data-stu-id="dbb73-108">The valid values for the **Type** attribute for the [Margin element](margin-element.md) are "Left" and "Right".</span></span>

## <a name="requirements"></a><span data-ttu-id="dbb73-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbb73-109">Requirements</span></span>



| <span data-ttu-id="dbb73-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbb73-110">Requirement</span></span> | <span data-ttu-id="dbb73-111">Valor</span><span class="sxs-lookup"><span data-stu-id="dbb73-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="dbb73-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dbb73-112">Minimum supported client</span></span><br/> | <span data-ttu-id="dbb73-113">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="dbb73-113">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="dbb73-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dbb73-114">Minimum supported server</span></span><br/> | <span data-ttu-id="dbb73-115">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="dbb73-115">None supported</span></span><br/>                                     |



 

 




