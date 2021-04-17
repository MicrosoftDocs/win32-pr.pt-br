---
description: 'O \_ método Get Duration recupera a duração do fluxo. Esse método implementa o método de duração IMediaPosition:: get \_ .'
ms.assetid: 326a8cd3-d05f-49d0-941d-08f9778e9a06
title: Método de CPosPassThru.get_Duration (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_Duration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df518a0691a4fe1a6c0443ba93a83e65577efe21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789961"
---
# <a name="cpospassthruget_duration-method"></a><span data-ttu-id="75129-104">Método Duration de CPosPassThru. get \_</span><span class="sxs-lookup"><span data-stu-id="75129-104">CPosPassThru.get\_Duration method</span></span>

<span data-ttu-id="75129-105">O `get_Duration` método recupera a duração do fluxo.</span><span class="sxs-lookup"><span data-stu-id="75129-105">The `get_Duration` method retrieves the duration of the stream.</span></span> <span data-ttu-id="75129-106">Esse método implementa o método de [**\_ duração IMediaPosition:: Get**](/windows/desktop/api/Control/nf-control-imediaposition-get_duration) .</span><span class="sxs-lookup"><span data-stu-id="75129-106">This method implements the [**IMediaPosition::get\_Duration**](/windows/desktop/api/Control/nf-control-imediaposition-get_duration) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="75129-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75129-107">Syntax</span></span>


```C++
HRESULT get_Duration(
   REFTIME *plength
);
```



## <a name="parameters"></a><span data-ttu-id="75129-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75129-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75129-109">*plength*</span><span class="sxs-lookup"><span data-stu-id="75129-109">*plength*</span></span> 
</dt> <dd>

<span data-ttu-id="75129-110">Ponteiro para uma variável que recebe o tamanho total do fluxo, em segundos.</span><span class="sxs-lookup"><span data-stu-id="75129-110">Pointer to a variable that receives the total stream length, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75129-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="75129-111">Return value</span></span>

<span data-ttu-id="75129-112">Retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="75129-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="75129-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75129-113">Requirements</span></span>



| <span data-ttu-id="75129-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="75129-114">Requirement</span></span> | <span data-ttu-id="75129-115">Valor</span><span class="sxs-lookup"><span data-stu-id="75129-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75129-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="75129-116">Header</span></span><br/>  | <dl> <span data-ttu-id="75129-117"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75129-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="75129-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="75129-118">Library</span></span><br/> | <dl> <span data-ttu-id="75129-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="75129-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75129-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="75129-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75129-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="75129-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




