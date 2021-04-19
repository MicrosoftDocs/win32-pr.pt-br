---
description: 'O método GetDuration recupera a duração do fluxo. Esse método implementa o método IMediaSeeking:: getDuration.'
ms.assetid: 0552e7bb-4d7e-40a8-a8ad-89ae6fff8ccb
title: Método CPosPassThru. getDuration (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9b533537c36ac7ec4c76289307368539482aa47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748809"
---
# <a name="cpospassthrugetduration-method"></a><span data-ttu-id="5cabf-104">Método CPosPassThru. GetDuration</span><span class="sxs-lookup"><span data-stu-id="5cabf-104">CPosPassThru.GetDuration method</span></span>

<span data-ttu-id="5cabf-105">O `GetDuration` método recupera a duração do fluxo.</span><span class="sxs-lookup"><span data-stu-id="5cabf-105">The `GetDuration` method retrieves the duration of the stream.</span></span> <span data-ttu-id="5cabf-106">Esse método implementa o método [**IMediaSeeking:: getDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) .</span><span class="sxs-lookup"><span data-stu-id="5cabf-106">This method implements the [**IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cabf-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5cabf-107">Syntax</span></span>


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="5cabf-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5cabf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cabf-109">*pDuration*</span><span class="sxs-lookup"><span data-stu-id="5cabf-109">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="5cabf-110">Ponteiro para uma variável que recebe a duração, em unidades do formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="5cabf-110">Pointer to a variable that receives the duration, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cabf-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5cabf-111">Return value</span></span>

<span data-ttu-id="5cabf-112">Retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="5cabf-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cabf-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5cabf-113">Requirements</span></span>



| <span data-ttu-id="5cabf-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cabf-114">Requirement</span></span> | <span data-ttu-id="5cabf-115">Valor</span><span class="sxs-lookup"><span data-stu-id="5cabf-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cabf-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5cabf-116">Header</span></span><br/>  | <dl> <span data-ttu-id="5cabf-117"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5cabf-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5cabf-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5cabf-118">Library</span></span><br/> | <dl> <span data-ttu-id="5cabf-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5cabf-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cabf-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="5cabf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cabf-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="5cabf-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




