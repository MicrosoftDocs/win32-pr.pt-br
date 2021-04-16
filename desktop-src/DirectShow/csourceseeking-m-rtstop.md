---
description: Hora de parada. Por padrão, o valor é definido como um número muito grande. A classe derivada pode redefinir o valor em seu construtor ou quando o filtro é inicializado.
ms.assetid: 1fddcf84-fd9a-4dad-892c-1b0abbb0ca55
title: 'Membro CSourceSeeking:: m_rtStop (Ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtStop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 28031f245ef877eca38129df2a86210f90093db4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751240"
---
# <a name="csourceseekingm_rtstop-member"></a><span data-ttu-id="d91e9-105">Membro de CSourceSeeking:: m \_ rtStop</span><span class="sxs-lookup"><span data-stu-id="d91e9-105">CSourceSeeking::m\_rtStop member</span></span>

<span data-ttu-id="d91e9-106">Hora de parada.</span><span class="sxs-lookup"><span data-stu-id="d91e9-106">Stop time.</span></span> <span data-ttu-id="d91e9-107">Por padrão, o valor é definido como um número muito grande.</span><span class="sxs-lookup"><span data-stu-id="d91e9-107">By default, the value is set to a very large number.</span></span> <span data-ttu-id="d91e9-108">A classe derivada pode redefinir o valor em seu construtor ou quando o filtro é inicializado.</span><span class="sxs-lookup"><span data-stu-id="d91e9-108">The derived class can reset the value in its constructor, or when the filter is initialized.</span></span>

## <a name="syntax"></a><span data-ttu-id="d91e9-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d91e9-109">Syntax</span></span>


```C++
CRefTime m_rtStop;
```



## <a name="remarks"></a><span data-ttu-id="d91e9-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d91e9-110">Remarks</span></span>

<span data-ttu-id="d91e9-111">Mantenha a seção crítica **m \_ pLock** antes de acessar essa variável.</span><span class="sxs-lookup"><span data-stu-id="d91e9-111">Hold the **m\_pLock** critical section before accessing this variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="d91e9-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d91e9-112">Requirements</span></span>



| <span data-ttu-id="d91e9-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d91e9-113">Requirement</span></span> | <span data-ttu-id="d91e9-114">Valor</span><span class="sxs-lookup"><span data-stu-id="d91e9-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d91e9-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d91e9-115">Header</span></span><br/>  | <dl> <span data-ttu-id="d91e9-116"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d91e9-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d91e9-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d91e9-117">Library</span></span><br/> | <dl> <span data-ttu-id="d91e9-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d91e9-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d91e9-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="d91e9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d91e9-120">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="d91e9-120">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




