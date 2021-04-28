---
description: 'Método CPosPassThru. GetRate – o método GetRate recupera a taxa de reprodução. Esse método implementa o método IMediaSeeking:: GetRate.'
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
ms.openlocfilehash: 997323ca2089a0b381b85c3730cb364d0883b1bf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085554"
---
# <a name="cpospassthrugetrate-method"></a><span data-ttu-id="cc726-104">Método CPosPassThru. GetRate</span><span class="sxs-lookup"><span data-stu-id="cc726-104">CPosPassThru.GetRate method</span></span>

<span data-ttu-id="cc726-105">O `GetRate` método recupera a taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="cc726-105">The `GetRate` method retrieves the playback rate.</span></span> <span data-ttu-id="cc726-106">Esse método implementa o método [**IMediaSeeking:: GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) .</span><span class="sxs-lookup"><span data-stu-id="cc726-106">This method implements the [**IMediaSeeking::GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc726-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc726-107">Syntax</span></span>


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a><span data-ttu-id="cc726-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc726-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc726-109">*pdRate*</span><span class="sxs-lookup"><span data-stu-id="cc726-109">*pdRate*</span></span> 
</dt> <dd>

<span data-ttu-id="cc726-110">Ponteiro para uma variável que recebe a taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="cc726-110">Pointer to a variable that receives the playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc726-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="cc726-111">Return value</span></span>

<span data-ttu-id="cc726-112">Retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="cc726-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc726-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc726-113">Requirements</span></span>



| <span data-ttu-id="cc726-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc726-114">Requirement</span></span> | <span data-ttu-id="cc726-115">Valor</span><span class="sxs-lookup"><span data-stu-id="cc726-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc726-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cc726-116">Header</span></span><br/>  | <dl> <span data-ttu-id="cc726-117"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc726-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cc726-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cc726-118">Library</span></span><br/> | <dl> <span data-ttu-id="cc726-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="cc726-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc726-120">Consulte também</span><span class="sxs-lookup"><span data-stu-id="cc726-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc726-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="cc726-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




