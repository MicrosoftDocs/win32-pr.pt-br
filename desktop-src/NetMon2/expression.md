---
description: Contém um grupo de matrizes ANDEXP avaliadas como pares.
ms.assetid: 14fa568c-9535-4415-923d-7e93ba4d2e80
title: Estrutura de expressão (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPRESSION
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b6565c294c0d8e0a7a277769404cb8b1b206380e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753429"
---
# <a name="expression-structure"></a><span data-ttu-id="3f655-103">Estrutura de expressão</span><span class="sxs-lookup"><span data-stu-id="3f655-103">EXPRESSION structure</span></span>

<span data-ttu-id="3f655-104">A estrutura de **expressão** contém um grupo de matrizes **ANDEXP** avaliadas como pares em expressões lógicas e, que têm o formato</span><span class="sxs-lookup"><span data-stu-id="3f655-104">The **EXPRESSION** structure contains a group of **ANDEXP** arrays evaluated as peers in logical AND expressions, which have the format</span></span>

<span data-ttu-id="3f655-105">(ANDEXP 1 && ANDEXP 2 && ANDEXP 3).</span><span class="sxs-lookup"><span data-stu-id="3f655-105">(ANDEXP 1 && ANDEXP 2 && ANDEXP 3).</span></span>

## <a name="syntax"></a><span data-ttu-id="3f655-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f655-106">Syntax</span></span>


```C++
typedef struct _EXPRESSION {
  DWORD  nAndExps;
  ANDEXP AndExp[MAX_PATTERNS];
} EXPRESSION, *LPEXPRESSION;
```



## <a name="members"></a><span data-ttu-id="3f655-107">Membros</span><span class="sxs-lookup"><span data-stu-id="3f655-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3f655-108">**nAndExps**</span><span class="sxs-lookup"><span data-stu-id="3f655-108">**nAndExps**</span></span>
</dt> <dd>

<span data-ttu-id="3f655-109">Número de padrões de **ANDEXP** .</span><span class="sxs-lookup"><span data-stu-id="3f655-109">Number of **ANDEXP** patterns.</span></span>

</dd> <dt>

<span data-ttu-id="3f655-110">**AndExp**</span><span class="sxs-lookup"><span data-stu-id="3f655-110">**AndExp**</span></span>
</dt> <dd>

<span data-ttu-id="3f655-111">Matriz de padrões de **ANDEXP** .</span><span class="sxs-lookup"><span data-stu-id="3f655-111">Array of **ANDEXP** patterns.</span></span> <span data-ttu-id="3f655-112">O filtro de captura organiza todas as linhas dessa matriz como lógica e instruções.</span><span class="sxs-lookup"><span data-stu-id="3f655-112">The capture filter arranges all rows of this array as logical AND statements.</span></span> <span data-ttu-id="3f655-113">Lembre-se de que cada estrutura de expressão pode conter um máximo de quatro padrões de **ANDEXP** .</span><span class="sxs-lookup"><span data-stu-id="3f655-113">Be aware that each EXPRESSION structure can contain a maximum of four **ANDEXP** patterns.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3f655-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3f655-114">Remarks</span></span>

<span data-ttu-id="3f655-115">Para obter mais informações sobre como implementar essa estrutura como parte de um filtro de captura, consulte [filtros de captura](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="3f655-115">For more information about implementing this structure as part of a capture filter, see [Capture Filters](capture-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3f655-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f655-116">Requirements</span></span>



| <span data-ttu-id="3f655-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f655-117">Requirement</span></span> | <span data-ttu-id="3f655-118">Valor</span><span class="sxs-lookup"><span data-stu-id="3f655-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3f655-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f655-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3f655-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3f655-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3f655-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f655-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3f655-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3f655-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3f655-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3f655-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f655-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f655-124"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f655-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f655-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f655-126">ANDEXP</span><span class="sxs-lookup"><span data-stu-id="3f655-126">ANDEXP</span></span>](andexp.md)
</dt> <dt>

[<span data-ttu-id="3f655-127">CAPTUREFILTER</span><span class="sxs-lookup"><span data-stu-id="3f655-127">CAPTUREFILTER</span></span>](capturefilter.md)
</dt> </dl>

 

 




