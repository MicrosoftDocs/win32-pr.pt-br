---
description: Define os valores válidos para o atributo style do elemento LineLayout.
ms.assetid: b257f0da-1bee-4d1b-9829-70f91cdcabe0
title: Tipo simples de LineLayoutStyleType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LineLayoutStyleType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 67b07d9de51e16148905768d7a6f268038bb1afa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811468"
---
# <a name="linelayoutstyletype-simple-type"></a><span data-ttu-id="be33e-103">Tipo simples de LineLayoutStyleType</span><span class="sxs-lookup"><span data-stu-id="be33e-103">LineLayoutStyleType Simple Type</span></span>

<span data-ttu-id="be33e-104">Define os valores válidos para o atributo **Style** do [elemento LineLayout](linelayout-element.md).</span><span class="sxs-lookup"><span data-stu-id="be33e-104">Defines the valid values for the **Style** attribute of the [LineLayout element](linelayout-element.md).</span></span>

``` syntax
<xs:simpleType name="LineLayoutStyleType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="None|Solid|Dash|Dot|DashDot|DashDotDot|Double"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="be33e-105">Padrões</span><span class="sxs-lookup"><span data-stu-id="be33e-105">Patterns</span></span>

<span data-ttu-id="be33e-106">O tipo simples **LineLayoutStyleType** é uma cadeia de caracteres que é restrita pelo seguinte padrão:</span><span class="sxs-lookup"><span data-stu-id="be33e-106">The **LineLayoutStyleType** simple type is a string that is restricted by the following pattern:</span></span>

-   `None|Solid|Dash|Dot|DashDot|DashDotDot|Double`

## <a name="remarks"></a><span data-ttu-id="be33e-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="be33e-107">Remarks</span></span>

<span data-ttu-id="be33e-108">Os valores válidos para o atributo **Style** do [elemento LineLayout](linelayout-element.md) são:</span><span class="sxs-lookup"><span data-stu-id="be33e-108">Valid values for the **Style** attribute of the [LineLayout element](linelayout-element.md) are:</span></span>

-   <span data-ttu-id="be33e-109">Nenhum</span><span class="sxs-lookup"><span data-stu-id="be33e-109">None</span></span>
-   <span data-ttu-id="be33e-110">Sólido</span><span class="sxs-lookup"><span data-stu-id="be33e-110">Solid</span></span>
-   <span data-ttu-id="be33e-111">Traço</span><span class="sxs-lookup"><span data-stu-id="be33e-111">Dash</span></span>
-   <span data-ttu-id="be33e-112">Ponto</span><span class="sxs-lookup"><span data-stu-id="be33e-112">Dot</span></span>
-   <span data-ttu-id="be33e-113">DashDot</span><span class="sxs-lookup"><span data-stu-id="be33e-113">DashDot</span></span>
-   <span data-ttu-id="be33e-114">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="be33e-114">DashDotDot</span></span>
-   <span data-ttu-id="be33e-115">Double</span><span class="sxs-lookup"><span data-stu-id="be33e-115">Double</span></span>

## <a name="requirements"></a><span data-ttu-id="be33e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be33e-116">Requirements</span></span>



| <span data-ttu-id="be33e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="be33e-117">Requirement</span></span> | <span data-ttu-id="be33e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="be33e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="be33e-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be33e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="be33e-120">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="be33e-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="be33e-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be33e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="be33e-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="be33e-122">None supported</span></span><br/>                                     |



 

 




