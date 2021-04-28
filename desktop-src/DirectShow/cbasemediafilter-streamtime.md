---
description: Método CBaseMediaFilter. streamtime – o método streamtime recupera a hora atual do fluxo.
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
ms.openlocfilehash: a90bb7d97825c14f11c75dd42d696fa302f8e3d4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096244"
---
# <a name="cbasemediafilterstreamtime-method"></a><span data-ttu-id="e2bdf-103">Método CBaseMediaFilter. streamtime</span><span class="sxs-lookup"><span data-stu-id="e2bdf-103">CBaseMediaFilter.StreamTime method</span></span>

<span data-ttu-id="e2bdf-104">O `StreamTime` método recupera a hora atual do fluxo.</span><span class="sxs-lookup"><span data-stu-id="e2bdf-104">The `StreamTime` method retrieves the current stream time.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2bdf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e2bdf-105">Syntax</span></span>


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a><span data-ttu-id="e2bdf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2bdf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2bdf-107">*rtStream* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="e2bdf-107">*rtStream* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e2bdf-108">Referência a um objeto [**CRefTime**](creftime.md) que recebe a hora atual do fluxo.</span><span class="sxs-lookup"><span data-stu-id="e2bdf-108">Reference to a [**CRefTime**](creftime.md) object that receives the current stream time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2bdf-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e2bdf-109">Return value</span></span>

<span data-ttu-id="e2bdf-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e2bdf-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e2bdf-111">Os valores possíveis incluem os listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e2bdf-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="e2bdf-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e2bdf-112">Return code</span></span>                                                                                      | <span data-ttu-id="e2bdf-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="e2bdf-113">Description</span></span>                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="e2bdf-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e2bdf-114"><dt>**S\_OK**</dt></span></span> </dl>             | <span data-ttu-id="e2bdf-115">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="e2bdf-115">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="e2bdf-116"><dt>**VFW \_ E \_ sem \_ relógio**</dt></span><span class="sxs-lookup"><span data-stu-id="e2bdf-116"><dt>**VFW\_E\_NO\_CLOCK**</dt></span></span> </dl> | <span data-ttu-id="e2bdf-117">Nenhum relógio de referência está disponível.</span><span class="sxs-lookup"><span data-stu-id="e2bdf-117">No reference clock is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e2bdf-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2bdf-118">Remarks</span></span>

<span data-ttu-id="e2bdf-119">O tempo de transmissão é definido como o tempo de referência atual (conforme fornecido pelo relógio de referência) menos a hora de início (especificada por [**CBaseMediaFilter:: m \_ tStart**](cbasemediafilter-m-tstart.md)).</span><span class="sxs-lookup"><span data-stu-id="e2bdf-119">Stream time is defined as the current reference time (as given by the reference clock) minus the start time (specified by [**CBaseMediaFilter::m\_tStart**](cbasemediafilter-m-tstart.md)).</span></span> <span data-ttu-id="e2bdf-120">Um carimbo de data/hora de um exemplo de mídia especifica o tempo de transmissão quando ele deve ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="e2bdf-120">A media sample's time stamp specifies the stream time when it should be rendered.</span></span> <span data-ttu-id="e2bdf-121">Se um exemplo com um carimbo de data/hora menor que o tempo atual do fluxo ainda não tiver sido renderizado, ele será atrasado.</span><span class="sxs-lookup"><span data-stu-id="e2bdf-121">If a sample with a time stamp less than the current stream time has not yet been rendered, it is late.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2bdf-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2bdf-122">Requirements</span></span>



| <span data-ttu-id="e2bdf-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2bdf-123">Requirement</span></span> | <span data-ttu-id="e2bdf-124">Valor</span><span class="sxs-lookup"><span data-stu-id="e2bdf-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2bdf-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e2bdf-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e2bdf-126"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2bdf-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e2bdf-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e2bdf-127">Library</span></span><br/> | <dl> <span data-ttu-id="e2bdf-128"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e2bdf-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2bdf-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e2bdf-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2bdf-130">**Classe CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="e2bdf-130">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




