---
description: O método streamtime recupera a hora atual do fluxo.
ms.assetid: 2e1ff6f1-9815-4ee6-97e8-a5ab5f472b27
title: Método CBaseMediaFilter. streamtime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.StreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27ccc9c721c97742c09d043af4cca5d287747597
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747833"
---
# <a name="cbasemediafilterstreamtime-method"></a><span data-ttu-id="233b5-103">Método CBaseMediaFilter. streamtime</span><span class="sxs-lookup"><span data-stu-id="233b5-103">CBaseMediaFilter.StreamTime method</span></span>

<span data-ttu-id="233b5-104">O `StreamTime` método recupera a hora atual do fluxo.</span><span class="sxs-lookup"><span data-stu-id="233b5-104">The `StreamTime` method retrieves the current stream time.</span></span>

## <a name="syntax"></a><span data-ttu-id="233b5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="233b5-105">Syntax</span></span>


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a><span data-ttu-id="233b5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="233b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="233b5-107">*rtStream* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="233b5-107">*rtStream* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="233b5-108">Referência a um objeto [**CRefTime**](creftime.md) que recebe a hora atual do fluxo.</span><span class="sxs-lookup"><span data-stu-id="233b5-108">Reference to a [**CRefTime**](creftime.md) object that receives the current stream time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="233b5-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="233b5-109">Return value</span></span>

<span data-ttu-id="233b5-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="233b5-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="233b5-111">Os valores possíveis incluem os listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="233b5-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="233b5-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="233b5-112">Return code</span></span>                                                                                      | <span data-ttu-id="233b5-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="233b5-113">Description</span></span>                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="233b5-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="233b5-114"><dt>**S\_OK**</dt></span></span> </dl>             | <span data-ttu-id="233b5-115">Êxito.</span><span class="sxs-lookup"><span data-stu-id="233b5-115">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="233b5-116"><dt>**VFW \_ E \_ sem \_ relógio**</dt></span><span class="sxs-lookup"><span data-stu-id="233b5-116"><dt>**VFW\_E\_NO\_CLOCK**</dt></span></span> </dl> | <span data-ttu-id="233b5-117">Nenhum relógio de referência está disponível.</span><span class="sxs-lookup"><span data-stu-id="233b5-117">No reference clock is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="233b5-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="233b5-118">Remarks</span></span>

<span data-ttu-id="233b5-119">O tempo de transmissão é definido como o tempo de referência atual (conforme fornecido pelo relógio de referência) menos a hora de início (especificada por [**CBaseMediaFilter:: m \_ tStart**](cbasemediafilter-m-tstart.md)).</span><span class="sxs-lookup"><span data-stu-id="233b5-119">Stream time is defined as the current reference time (as given by the reference clock) minus the start time (specified by [**CBaseMediaFilter::m\_tStart**](cbasemediafilter-m-tstart.md)).</span></span> <span data-ttu-id="233b5-120">Um carimbo de data/hora de um exemplo de mídia especifica o tempo de transmissão quando ele deve ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="233b5-120">A media sample's time stamp specifies the stream time when it should be rendered.</span></span> <span data-ttu-id="233b5-121">Se um exemplo com um carimbo de data/hora menor que o tempo atual do fluxo ainda não tiver sido renderizado, ele será atrasado.</span><span class="sxs-lookup"><span data-stu-id="233b5-121">If a sample with a time stamp less than the current stream time has not yet been rendered, it is late.</span></span>

## <a name="requirements"></a><span data-ttu-id="233b5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="233b5-122">Requirements</span></span>



| <span data-ttu-id="233b5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="233b5-123">Requirement</span></span> | <span data-ttu-id="233b5-124">Valor</span><span class="sxs-lookup"><span data-stu-id="233b5-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="233b5-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="233b5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="233b5-126"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="233b5-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="233b5-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="233b5-127">Library</span></span><br/> | <dl> <span data-ttu-id="233b5-128"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="233b5-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="233b5-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="233b5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="233b5-130">**Classe CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="233b5-130">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




