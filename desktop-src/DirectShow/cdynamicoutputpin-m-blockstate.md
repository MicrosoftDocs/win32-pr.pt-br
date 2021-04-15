---
description: Estado de bloqueio.
ms.assetid: 55afd314-efd3-47bf-80e3-e17c1332a4cf
title: 'Membro CDynamicOutputPin:: m_BlockState (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_BlockState
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f02a59854b381db5e7b13a85ccca0754cc38f51d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747388"
---
# <a name="cdynamicoutputpinm_blockstate-member"></a><span data-ttu-id="461b4-103">Membro blockstate CDynamicOutputPin:: m \_</span><span class="sxs-lookup"><span data-stu-id="461b4-103">CDynamicOutputPin::m\_BlockState member</span></span>

<span data-ttu-id="461b4-104">Estado de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="461b4-104">Blocking state.</span></span>

## <a name="syntax"></a><span data-ttu-id="461b4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="461b4-105">Syntax</span></span>


```C++
BLOCK_STATE m_BlockState;
```



## <a name="remarks"></a><span data-ttu-id="461b4-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="461b4-106">Remarks</span></span>

<span data-ttu-id="461b4-107">Os seguintes Estados são definidos:</span><span class="sxs-lookup"><span data-stu-id="461b4-107">The following states are defined:</span></span>

-   <span data-ttu-id="461b4-108">Não \_ bloqueado</span><span class="sxs-lookup"><span data-stu-id="461b4-108">NOT\_BLOCKED</span></span>
-   <span data-ttu-id="461b4-109">PENDING</span><span class="sxs-lookup"><span data-stu-id="461b4-109">PENDING</span></span>
-   <span data-ttu-id="461b4-110">OBSTRUÍDO</span><span class="sxs-lookup"><span data-stu-id="461b4-110">BLOCKED</span></span>

<span data-ttu-id="461b4-111">Antes de acessar essa variável, mantenha a seção crítica [**CDynamicOutputPin:: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="461b4-111">Before accessing this variable, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="461b4-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="461b4-112">Requirements</span></span>



| <span data-ttu-id="461b4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="461b4-113">Requirement</span></span> | <span data-ttu-id="461b4-114">Valor</span><span class="sxs-lookup"><span data-stu-id="461b4-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="461b4-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="461b4-115">Header</span></span><br/>  | <dl> <span data-ttu-id="461b4-116"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="461b4-116"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="461b4-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="461b4-117">Library</span></span><br/> | <dl> <span data-ttu-id="461b4-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="461b4-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="461b4-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="461b4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="461b4-120">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="461b4-120">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




