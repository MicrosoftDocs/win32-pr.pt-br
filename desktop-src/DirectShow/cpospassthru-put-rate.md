---
description: O \_ método de taxa Put define a taxa de reprodução. Esse método implementa o método de taxa IMediaPosition::p UT \_ .
ms.assetid: c077f344-de34-4f8a-8e08-6d7086a5a4f1
title: Método de CPosPassThru.put_Rate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_Rate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21e7e654233f78adcda2addf73b87a178654872e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778490"
---
# <a name="cpospassthruput_rate-method"></a><span data-ttu-id="f944a-104">Método de taxa CPosPassThru. put \_</span><span class="sxs-lookup"><span data-stu-id="f944a-104">CPosPassThru.put\_Rate method</span></span>

<span data-ttu-id="f944a-105">O `put_Rate` método define a taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="f944a-105">The `put_Rate` method sets the playback rate.</span></span> <span data-ttu-id="f944a-106">Esse método implementa o método de [**\_ taxa IMediaPosition::p UT**](/windows/desktop/api/Control/nf-control-imediaposition-put_rate) .</span><span class="sxs-lookup"><span data-stu-id="f944a-106">This method implements the [**IMediaPosition::put\_Rate**](/windows/desktop/api/Control/nf-control-imediaposition-put_rate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f944a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f944a-107">Syntax</span></span>


```C++
HRESULT put_Rate(
   double dRate
);
```



## <a name="parameters"></a><span data-ttu-id="f944a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f944a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f944a-109">*dRate*</span><span class="sxs-lookup"><span data-stu-id="f944a-109">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="f944a-110">Taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="f944a-110">Playback rate.</span></span> <span data-ttu-id="f944a-111">Não deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f944a-111">Must not be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f944a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f944a-112">Return value</span></span>

<span data-ttu-id="f944a-113">Retorna E \_ INVALIDARG se *drate* for zero.</span><span class="sxs-lookup"><span data-stu-id="f944a-113">Returns E\_INVALIDARG if *dRate* is zero.</span></span> <span data-ttu-id="f944a-114">Caso contrário, retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="f944a-114">Otherwise, returns the **HRESULT** value from the connected pin.</span></span>

## <a name="remarks"></a><span data-ttu-id="f944a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f944a-115">Remarks</span></span>

<span data-ttu-id="f944a-116">As taxas negativas indicam a reprodução reversa.</span><span class="sxs-lookup"><span data-stu-id="f944a-116">Negative rates indicate reverse play.</span></span> <span data-ttu-id="f944a-117">Nem toda mídia dará suporte à reprodução inversa.</span><span class="sxs-lookup"><span data-stu-id="f944a-117">Not all media will support reverse play.</span></span>

## <a name="requirements"></a><span data-ttu-id="f944a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f944a-118">Requirements</span></span>



| <span data-ttu-id="f944a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f944a-119">Requirement</span></span> | <span data-ttu-id="f944a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f944a-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f944a-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f944a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f944a-122"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f944a-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f944a-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f944a-123">Library</span></span><br/> | <dl> <span data-ttu-id="f944a-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f944a-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f944a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="f944a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f944a-126">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="f944a-126">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




