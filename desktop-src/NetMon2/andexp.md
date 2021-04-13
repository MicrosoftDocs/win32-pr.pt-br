---
description: A estrutura ANDEXP contém uma matriz de correspondências de padrão usada para avaliar dados de quadro.
ms.assetid: e5f4c030-eb2b-4cc9-9032-9ad4701b6503
title: Estrutura ANDEXP (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ANDEXP
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 1d27d5bdd51a45b31f518271053f44b45917cdeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297016"
---
# <a name="andexp-structure"></a><span data-ttu-id="21221-103">Estrutura ANDEXP</span><span class="sxs-lookup"><span data-stu-id="21221-103">ANDEXP structure</span></span>

<span data-ttu-id="21221-104">A estrutura **ANDEXP** contém uma matriz de correspondências de padrão usada para avaliar dados de quadro.</span><span class="sxs-lookup"><span data-stu-id="21221-104">The **ANDEXP** structure contains an array of pattern matches used to evaluate frame data.</span></span>

## <a name="syntax"></a><span data-ttu-id="21221-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="21221-105">Syntax</span></span>


```C++
typedef struct _ANDEXP {
  DWORD        nPatternMatches;
  PATTERNMATCH PatternMatch[MAX_PATTERNS];
} ANDEXP, *LPANDEXP;
```



## <a name="members"></a><span data-ttu-id="21221-106">Membros</span><span class="sxs-lookup"><span data-stu-id="21221-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="21221-107">**nPatternMatches**</span><span class="sxs-lookup"><span data-stu-id="21221-107">**nPatternMatches**</span></span>
</dt> <dd>

<span data-ttu-id="21221-108">Número de correspondências de padrão.</span><span class="sxs-lookup"><span data-stu-id="21221-108">Number of pattern matches.</span></span>

</dd> <dt>

<span data-ttu-id="21221-109">**PatternMatch**</span><span class="sxs-lookup"><span data-stu-id="21221-109">**PatternMatch**</span></span>
</dt> <dd>

<span data-ttu-id="21221-110">Matriz de elementos de correspondência de padrões.</span><span class="sxs-lookup"><span data-stu-id="21221-110">Array of pattern match elements.</span></span> <span data-ttu-id="21221-111">Observe que cada estrutura **ANDEXP** pode conter até quatro elementos de correspondência de padrões.</span><span class="sxs-lookup"><span data-stu-id="21221-111">Note that each **ANDEXP** structure can contain up to four pattern match elements.</span></span> <span data-ttu-id="21221-112">Para obter mais informações sobre esse membro, consulte [filtros de captura](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="21221-112">For more information about this member, see [Capture Filters](capture-filters.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="21221-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="21221-113">Remarks</span></span>

<span data-ttu-id="21221-114">Os padrões na matriz de padrões **PatternMatch** \[ Max \_ \] são Unidos como pares em instruções or lógicas no formato</span><span class="sxs-lookup"><span data-stu-id="21221-114">The patterns in the **PatternMatch**\[MAX\_PATTERNS\] array are joined as peers in logical OR statements in the format</span></span>

<span data-ttu-id="21221-115">(Padrão 1 \| \| Padrão 2 \| \| padrão 3).</span><span class="sxs-lookup"><span data-stu-id="21221-115">(Pattern 1 \|\| Pattern 2 \|\| Pattern 3).</span></span>

<span data-ttu-id="21221-116">Para obter mais informações sobre como implementar essa estrutura, consulte [filtros de captura](capture-filters.md) .</span><span class="sxs-lookup"><span data-stu-id="21221-116">For more information about implementing this structure, see [Capture Filters](capture-filters.md) .</span></span>

## <a name="requirements"></a><span data-ttu-id="21221-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21221-117">Requirements</span></span>



| <span data-ttu-id="21221-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="21221-118">Requirement</span></span> | <span data-ttu-id="21221-119">Valor</span><span class="sxs-lookup"><span data-stu-id="21221-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="21221-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21221-120">Minimum supported client</span></span><br/> | <span data-ttu-id="21221-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="21221-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="21221-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21221-122">Minimum supported server</span></span><br/> | <span data-ttu-id="21221-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="21221-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="21221-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="21221-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="21221-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="21221-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21221-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="21221-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21221-127">PATTERNMATCH</span><span class="sxs-lookup"><span data-stu-id="21221-127">PATTERNMATCH</span></span>](patternmatch.md)
</dt> </dl>

 

 




