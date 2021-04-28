---
description: 'Método CPosPassThru. GetAvailable – o método GetAvailable recupera o intervalo de vezes em que a busca é eficiente. Esse método implementa o método IMediaSeeking:: GetAvailable.'
ms.assetid: 5f4af41a-eb7b-4caa-97e0-aaed78467723
title: Método CPosPassThru. GetAvailable (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0d56827a68f4c287e5808f0d8f64b8142c31b1f4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095284"
---
# <a name="cpospassthrugetavailable-method"></a><span data-ttu-id="15621-104">Método CPosPassThru. GetAvailable</span><span class="sxs-lookup"><span data-stu-id="15621-104">CPosPassThru.GetAvailable method</span></span>

<span data-ttu-id="15621-105">O `GetAvailable` método recupera o intervalo de vezes em que a busca é eficiente.</span><span class="sxs-lookup"><span data-stu-id="15621-105">The `GetAvailable` method retrieves the range of times in which seeking is efficient.</span></span> <span data-ttu-id="15621-106">Esse método implementa o método [**IMediaSeeking:: GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) .</span><span class="sxs-lookup"><span data-stu-id="15621-106">This method implements the [**IMediaSeeking::GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="15621-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15621-107">Syntax</span></span>


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a><span data-ttu-id="15621-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15621-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15621-109">*pEarliest*</span><span class="sxs-lookup"><span data-stu-id="15621-109">*pEarliest*</span></span> 
</dt> <dd>

<span data-ttu-id="15621-110">Ponteiro para uma variável que recebe a hora mais antiga para busca eficiente.</span><span class="sxs-lookup"><span data-stu-id="15621-110">Pointer to a variable that receives the earliest time for efficient seeking.</span></span>

</dd> <dt>

<span data-ttu-id="15621-111">*mais chapas*</span><span class="sxs-lookup"><span data-stu-id="15621-111">*pLatest*</span></span> 
</dt> <dd>

<span data-ttu-id="15621-112">Ponteiro para uma variável que recebe a hora mais recente para busca eficiente.</span><span class="sxs-lookup"><span data-stu-id="15621-112">Pointer to a variable that receives the latest time for efficient seeking.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15621-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="15621-113">Return value</span></span>

<span data-ttu-id="15621-114">Retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="15621-114">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="15621-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15621-115">Requirements</span></span>



| <span data-ttu-id="15621-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="15621-116">Requirement</span></span> | <span data-ttu-id="15621-117">Valor</span><span class="sxs-lookup"><span data-stu-id="15621-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15621-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="15621-118">Header</span></span><br/>  | <dl> <span data-ttu-id="15621-119"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="15621-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="15621-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="15621-120">Library</span></span><br/> | <dl> <span data-ttu-id="15621-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="15621-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15621-122">Consulte também</span><span class="sxs-lookup"><span data-stu-id="15621-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15621-123">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="15621-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




