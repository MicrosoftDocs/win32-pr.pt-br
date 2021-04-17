---
description: O \_ método Put preverttime define a quantidade de dados que serão enfileirados antes da posição inicial. Esse método implementa o método IMediaPosition::p UT \_ preverttime.
ms.assetid: 5c35fb1d-2296-493f-8104-601127d7dd9f
title: Método de CPosPassThru.put_PrerollTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_PrerollTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60bd4eddc7688373386147ea7999fdbd17f9af6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752287"
---
# <a name="cpospassthruput_prerolltime-method"></a><span data-ttu-id="2d47c-104">CPosPassThru. put \_ método preverttime</span><span class="sxs-lookup"><span data-stu-id="2d47c-104">CPosPassThru.put\_PrerollTime method</span></span>

<span data-ttu-id="2d47c-105">O `put_PrerollTime` método define a quantidade de dados que serão enfileirados antes da posição inicial.</span><span class="sxs-lookup"><span data-stu-id="2d47c-105">The `put_PrerollTime` method sets the amount of data that will be queued before the start position.</span></span> <span data-ttu-id="2d47c-106">Esse método implementa o método [**IMediaPosition::p UT \_ preverttime**](/windows/desktop/api/Control/nf-control-imediaposition-put_prerolltime) .</span><span class="sxs-lookup"><span data-stu-id="2d47c-106">This method implements the [**IMediaPosition::put\_PrerollTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_prerolltime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d47c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d47c-107">Syntax</span></span>


```C++
HRESULT put_PrerollTime(
   REFTIME llTime
);
```



## <a name="parameters"></a><span data-ttu-id="2d47c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d47c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d47c-109">*llTime*</span><span class="sxs-lookup"><span data-stu-id="2d47c-109">*llTime*</span></span> 
</dt> <dd>

<span data-ttu-id="2d47c-110">Tempo de preversão, em segundos.</span><span class="sxs-lookup"><span data-stu-id="2d47c-110">Preroll time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d47c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2d47c-111">Return value</span></span>

<span data-ttu-id="2d47c-112">Retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="2d47c-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d47c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d47c-113">Requirements</span></span>



| <span data-ttu-id="2d47c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d47c-114">Requirement</span></span> | <span data-ttu-id="2d47c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="2d47c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d47c-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2d47c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2d47c-117"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2d47c-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2d47c-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2d47c-118">Library</span></span><br/> | <dl> <span data-ttu-id="2d47c-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="2d47c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d47c-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d47c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d47c-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="2d47c-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




