---
description: 'O \_ método obter taxa recupera a taxa de reprodução. Esse método implementa o método de taxa IMediaPosition:: get \_ .'
ms.assetid: 216cbcef-4874-4565-abb0-8c8bf67fe23c
title: Método de CPosPassThru.get_Rate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_Rate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 46e565f51d7c549f524f9e478b2a8326daf690a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754256"
---
# <a name="cpospassthruget_rate-method"></a><span data-ttu-id="43452-104">Método de taxa CPosPassThru. get \_</span><span class="sxs-lookup"><span data-stu-id="43452-104">CPosPassThru.get\_Rate method</span></span>

<span data-ttu-id="43452-105">O `get_Rate` método recupera a taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="43452-105">The `get_Rate` method retrieves the playback rate.</span></span> <span data-ttu-id="43452-106">Esse método implementa o método de [**\_ taxa IMediaPosition:: Get**](/windows/desktop/api/Control/nf-control-imediaposition-get_rate) .</span><span class="sxs-lookup"><span data-stu-id="43452-106">This method implements the [**IMediaPosition::get\_Rate**](/windows/desktop/api/Control/nf-control-imediaposition-get_rate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="43452-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43452-107">Syntax</span></span>


```C++
HRESULT get_Rate(
   double *pdRate
);
```



## <a name="parameters"></a><span data-ttu-id="43452-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43452-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43452-109">*pdRate*</span><span class="sxs-lookup"><span data-stu-id="43452-109">*pdRate*</span></span> 
</dt> <dd>

<span data-ttu-id="43452-110">Ponteiro para uma variável que recebe a taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="43452-110">Pointer to a variable that receives the playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43452-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="43452-111">Return value</span></span>

<span data-ttu-id="43452-112">Retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="43452-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="43452-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43452-113">Requirements</span></span>



| <span data-ttu-id="43452-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="43452-114">Requirement</span></span> | <span data-ttu-id="43452-115">Valor</span><span class="sxs-lookup"><span data-stu-id="43452-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43452-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="43452-116">Header</span></span><br/>  | <dl> <span data-ttu-id="43452-117"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="43452-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="43452-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="43452-118">Library</span></span><br/> | <dl> <span data-ttu-id="43452-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="43452-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43452-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="43452-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43452-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="43452-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




