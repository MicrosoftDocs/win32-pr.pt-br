---
description: 'O método GetRate recupera a taxa de reprodução. Esse método implementa o método IMediaSeeking:: GetRate.'
ms.assetid: 19de3ea3-280e-4320-9cce-2c29801bd84b
title: Método CPosPassThru. GetRate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13e96bb231eb3e5c41f8cdf18c649f20955ba5cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752084"
---
# <a name="cpospassthrugetrate-method"></a><span data-ttu-id="a4415-104">Método CPosPassThru. GetRate</span><span class="sxs-lookup"><span data-stu-id="a4415-104">CPosPassThru.GetRate method</span></span>

<span data-ttu-id="a4415-105">O `GetRate` método recupera a taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="a4415-105">The `GetRate` method retrieves the playback rate.</span></span> <span data-ttu-id="a4415-106">Esse método implementa o método [**IMediaSeeking:: GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) .</span><span class="sxs-lookup"><span data-stu-id="a4415-106">This method implements the [**IMediaSeeking::GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4415-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4415-107">Syntax</span></span>


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a><span data-ttu-id="a4415-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4415-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4415-109">*pdRate*</span><span class="sxs-lookup"><span data-stu-id="a4415-109">*pdRate*</span></span> 
</dt> <dd>

<span data-ttu-id="a4415-110">Ponteiro para uma variável que recebe a taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="a4415-110">Pointer to a variable that receives the playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4415-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a4415-111">Return value</span></span>

<span data-ttu-id="a4415-112">Retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="a4415-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4415-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4415-113">Requirements</span></span>



| <span data-ttu-id="a4415-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4415-114">Requirement</span></span> | <span data-ttu-id="a4415-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a4415-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4415-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a4415-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a4415-117"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a4415-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a4415-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a4415-118">Library</span></span><br/> | <dl> <span data-ttu-id="a4415-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a4415-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4415-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4415-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4415-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="a4415-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




