---
description: 'O método GetAvailable recupera o intervalo de vezes em que a busca é eficiente. Esse método implementa o método IMediaSeeking:: GetAvailable.'
ms.assetid: 2a7b6cdb-47c3-4aeb-89ff-ea968c6a809b
title: Método CSourceSeeking. GetAvailable (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bc661d81c49798b6fe06dc569b680e5f9839e5a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758850"
---
# <a name="csourceseekinggetavailable-method"></a><span data-ttu-id="34fdf-104">Método CSourceSeeking. GetAvailable</span><span class="sxs-lookup"><span data-stu-id="34fdf-104">CSourceSeeking.GetAvailable method</span></span>

<span data-ttu-id="34fdf-105">O `GetAvailable` método recupera o intervalo de vezes em que a busca é eficiente.</span><span class="sxs-lookup"><span data-stu-id="34fdf-105">The `GetAvailable` method retrieves the range of times in which seeking is efficient.</span></span> <span data-ttu-id="34fdf-106">Esse método implementa o método [**IMediaSeeking:: GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) .</span><span class="sxs-lookup"><span data-stu-id="34fdf-106">This method implements the [**IMediaSeeking::GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="34fdf-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="34fdf-107">Syntax</span></span>


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a><span data-ttu-id="34fdf-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34fdf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34fdf-109">*pEarliest*</span><span class="sxs-lookup"><span data-stu-id="34fdf-109">*pEarliest*</span></span> 
</dt> <dd>

<span data-ttu-id="34fdf-110">Ponteiro para uma variável que recebe a hora mais antiga para busca eficiente.</span><span class="sxs-lookup"><span data-stu-id="34fdf-110">Pointer to a variable that receives the earliest time for efficient seeking.</span></span> <span data-ttu-id="34fdf-111">A variável é definida como zero.</span><span class="sxs-lookup"><span data-stu-id="34fdf-111">The variable is set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="34fdf-112">*mais chapas*</span><span class="sxs-lookup"><span data-stu-id="34fdf-112">*pLatest*</span></span> 
</dt> <dd>

<span data-ttu-id="34fdf-113">Ponteiro para uma variável que recebe a hora mais recente para busca eficiente.</span><span class="sxs-lookup"><span data-stu-id="34fdf-113">Pointer to a variable that receives the latest time for efficient seeking.</span></span> <span data-ttu-id="34fdf-114">A variável é definida como o valor da variável de membro [**CSourceSeeking:: m \_ rtDuration**](csourceseeking-m-rtduration.md) .</span><span class="sxs-lookup"><span data-stu-id="34fdf-114">The variable is set to the value of the [**CSourceSeeking::m\_rtDuration**](csourceseeking-m-rtduration.md) member variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34fdf-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="34fdf-115">Return value</span></span>

<span data-ttu-id="34fdf-116">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="34fdf-116">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="34fdf-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34fdf-117">Requirements</span></span>



| <span data-ttu-id="34fdf-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="34fdf-118">Requirement</span></span> | <span data-ttu-id="34fdf-119">Valor</span><span class="sxs-lookup"><span data-stu-id="34fdf-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34fdf-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="34fdf-120">Header</span></span><br/>  | <dl> <span data-ttu-id="34fdf-121"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34fdf-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="34fdf-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="34fdf-122">Library</span></span><br/> | <dl> <span data-ttu-id="34fdf-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="34fdf-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34fdf-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="34fdf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34fdf-125">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="34fdf-125">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




