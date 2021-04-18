---
description: 'O identificador do thread que chamou por último o método IPinFlowControl:: Block neste PIN. Esta variável de membro só é válida enquanto o PIN está bloqueado.'
ms.assetid: 7f8429c5-7e58-49a1-9f36-01088379a193
title: 'Membro CDynamicOutputPin:: m_dwBlockCallerThreadID (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwBlockCallerThreadID
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9aa2de66f1afe690715ab658483c01cdfeb3f451
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750049"
---
# <a name="cdynamicoutputpinm_dwblockcallerthreadid-member"></a><span data-ttu-id="dde10-104">Membro de CDynamicOutputPin:: m \_ dwBlockCallerThreadID</span><span class="sxs-lookup"><span data-stu-id="dde10-104">CDynamicOutputPin::m\_dwBlockCallerThreadID member</span></span>

<span data-ttu-id="dde10-105">O identificador do thread que chamou por último o método [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) neste PIN.</span><span class="sxs-lookup"><span data-stu-id="dde10-105">The identifier of the thread that last called the [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) method on this pin.</span></span> <span data-ttu-id="dde10-106">Esta variável de membro só é válida enquanto o PIN está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="dde10-106">This member variable is only valid while the pin is blocked.</span></span>

## <a name="syntax"></a><span data-ttu-id="dde10-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dde10-107">Syntax</span></span>


```C++
DWORD m_dwBlockCallerThreadID;
```



## <a name="remarks"></a><span data-ttu-id="dde10-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="dde10-108">Remarks</span></span>

<span data-ttu-id="dde10-109">Antes de acessar essa variável, mantenha a seção crítica [**CDynamicOutputPin:: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="dde10-109">Before accessing this variable, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="dde10-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dde10-110">Requirements</span></span>



| <span data-ttu-id="dde10-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="dde10-111">Requirement</span></span> | <span data-ttu-id="dde10-112">Valor</span><span class="sxs-lookup"><span data-stu-id="dde10-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dde10-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dde10-113">Header</span></span><br/>  | <dl> <span data-ttu-id="dde10-114"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dde10-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="dde10-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dde10-115">Library</span></span><br/> | <dl> <span data-ttu-id="dde10-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="dde10-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dde10-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="dde10-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dde10-118">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="dde10-118">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




