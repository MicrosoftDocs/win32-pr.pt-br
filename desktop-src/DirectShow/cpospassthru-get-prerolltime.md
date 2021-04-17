---
description: 'O \_ método Get preverttime recupera a quantidade de dados que serão enfileirados antes da posição inicial. Esse método implementa o \_ método preverttime IMediaPosition:: Get.'
ms.assetid: 37c12798-eb0d-4859-8b2e-52d6ae147863
title: Método de CPosPassThru.get_PrerollTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_PrerollTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55cb2cc37a18c9ea00b4eb7115590f472b8d467e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749618"
---
# <a name="cpospassthruget_prerolltime-method"></a><span data-ttu-id="1d0f5-104">\_Método preverttime CPosPassThru. Get</span><span class="sxs-lookup"><span data-stu-id="1d0f5-104">CPosPassThru.get\_PrerollTime method</span></span>

<span data-ttu-id="1d0f5-105">O `get_PrerollTime` método recupera a quantidade de dados que serão enfileirados antes da posição inicial.</span><span class="sxs-lookup"><span data-stu-id="1d0f5-105">The `get_PrerollTime` method retrieves the amount of data that will be queued before the start position.</span></span> <span data-ttu-id="1d0f5-106">Esse método implementa o método [**\_ preverttime IMediaPosition:: Get**](/windows/desktop/api/Control/nf-control-imediaposition-get_prerolltime) .</span><span class="sxs-lookup"><span data-stu-id="1d0f5-106">This method implements the [**IMediaPosition::get\_PrerollTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_prerolltime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d0f5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d0f5-107">Syntax</span></span>


```C++
HRESULT get_PrerollTime(
   REFTIME *pllTime
);
```



## <a name="parameters"></a><span data-ttu-id="1d0f5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1d0f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d0f5-109">*pllTime*</span><span class="sxs-lookup"><span data-stu-id="1d0f5-109">*pllTime*</span></span> 
</dt> <dd>

<span data-ttu-id="1d0f5-110">Ponteiro para uma variável que recebe o tempo de preversão, em segundos.</span><span class="sxs-lookup"><span data-stu-id="1d0f5-110">Pointer to a variable that receives the preroll time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d0f5-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1d0f5-111">Return value</span></span>

<span data-ttu-id="1d0f5-112">Retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="1d0f5-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d0f5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d0f5-113">Requirements</span></span>



| <span data-ttu-id="1d0f5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d0f5-114">Requirement</span></span> | <span data-ttu-id="1d0f5-115">Valor</span><span class="sxs-lookup"><span data-stu-id="1d0f5-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d0f5-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1d0f5-116">Header</span></span><br/>  | <dl> <span data-ttu-id="1d0f5-117"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d0f5-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1d0f5-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1d0f5-118">Library</span></span><br/> | <dl> <span data-ttu-id="1d0f5-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="1d0f5-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d0f5-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d0f5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d0f5-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="1d0f5-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




