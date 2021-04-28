---
description: Método CBaseFilter. streamtime – o método streamtime recupera a hora atual do fluxo.
ms.assetid: 88a2939d-fb51-49fd-af71-21c99511de43
title: Método CBaseFilter. streamtime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.StreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f3334ac273a733c3f0591b76af7e76460997a199
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120064"
---
# <a name="cbasefilterstreamtime-method"></a><span data-ttu-id="94d72-103">Método CBaseFilter. streamtime</span><span class="sxs-lookup"><span data-stu-id="94d72-103">CBaseFilter.StreamTime method</span></span>

<span data-ttu-id="94d72-104">O método **streamtime** recupera a hora atual do fluxo.</span><span class="sxs-lookup"><span data-stu-id="94d72-104">The **StreamTime** method retrieves the current stream time.</span></span>

## <a name="syntax"></a><span data-ttu-id="94d72-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="94d72-105">Syntax</span></span>


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a><span data-ttu-id="94d72-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="94d72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94d72-107">*rtStream* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="94d72-107">*rtStream* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="94d72-108">Referência a um objeto [**CRefTime**](creftime.md) que recebe a hora atual do fluxo.</span><span class="sxs-lookup"><span data-stu-id="94d72-108">Reference to a [**CRefTime**](creftime.md) object that receives the current stream time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94d72-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="94d72-109">Return value</span></span>

<span data-ttu-id="94d72-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="94d72-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="94d72-111">Os valores possíveis incluem os listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="94d72-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="94d72-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="94d72-112">Return code</span></span>                                                                                      | <span data-ttu-id="94d72-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="94d72-113">Description</span></span>                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="94d72-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="94d72-114"><dt>**S\_OK**</dt></span></span> </dl>             | <span data-ttu-id="94d72-115">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="94d72-115">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="94d72-116"><dt>**VFW \_ E \_ sem \_ relógio**</dt></span><span class="sxs-lookup"><span data-stu-id="94d72-116"><dt>**VFW\_E\_NO\_CLOCK**</dt></span></span> </dl> | <span data-ttu-id="94d72-117">Nenhum relógio de referência está disponível.</span><span class="sxs-lookup"><span data-stu-id="94d72-117">No reference clock is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="94d72-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="94d72-118">Remarks</span></span>

<span data-ttu-id="94d72-119">O tempo de transmissão é definido como o tempo de referência atual (conforme fornecido pelo relógio de referência) menos a hora de início (especificada por [**CBaseFilter:: m \_ tStart**](cbasefilter-m-tstart.md)).</span><span class="sxs-lookup"><span data-stu-id="94d72-119">Stream time is defined as the current reference time (as given by the reference clock) minus the start time (specified by [**CBaseFilter::m\_tStart**](cbasefilter-m-tstart.md)).</span></span> <span data-ttu-id="94d72-120">Um *carimbo de data/hora* de um exemplo de mídia especifica o tempo de transmissão quando ele deve ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="94d72-120">A media sample's *time stamp* specifies the stream time when it should be rendered.</span></span> <span data-ttu-id="94d72-121">Se um exemplo com um carimbo de data/hora menor que o tempo atual do fluxo ainda não tiver sido renderizado, ele será atrasado.</span><span class="sxs-lookup"><span data-stu-id="94d72-121">If a sample with a time stamp less than the current stream time has not yet been rendered, it is late.</span></span>

<span data-ttu-id="94d72-122">Esse método obtém o tempo de transmissão chamando [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) para obter o tempo de referência atual e subtraindo a hora de início inicial.</span><span class="sxs-lookup"><span data-stu-id="94d72-122">This method gets the stream time by calling [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) to get the current reference time, and then subtracting the initial start time.</span></span>

## <a name="requirements"></a><span data-ttu-id="94d72-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94d72-123">Requirements</span></span>



| <span data-ttu-id="94d72-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="94d72-124">Requirement</span></span> | <span data-ttu-id="94d72-125">Valor</span><span class="sxs-lookup"><span data-stu-id="94d72-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94d72-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="94d72-126">Header</span></span><br/>  | <dl> <span data-ttu-id="94d72-127"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="94d72-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="94d72-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="94d72-128">Library</span></span><br/> | <dl> <span data-ttu-id="94d72-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="94d72-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94d72-130">Consulte também</span><span class="sxs-lookup"><span data-stu-id="94d72-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94d72-131">Tempo e relógios no DirectShow</span><span class="sxs-lookup"><span data-stu-id="94d72-131">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="94d72-132">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="94d72-132">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




