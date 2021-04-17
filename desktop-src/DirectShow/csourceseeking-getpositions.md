---
description: 'O método getpositiones recupera a posição atual e a posição de parada. Esse método implementa o método IMediaSeeking:: getposicionations.'
ms.assetid: f577b052-669b-457d-beab-94f574fef08d
title: Método CSourceSeeking. GetPositions (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8d95013b12d1ee41867ac73920ca1f9b1ca0bdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748016"
---
# <a name="csourceseekinggetpositions-method"></a><span data-ttu-id="6ac71-104">Método CSourceSeeking. getpositiones</span><span class="sxs-lookup"><span data-stu-id="6ac71-104">CSourceSeeking.GetPositions method</span></span>

<span data-ttu-id="6ac71-105">O `GetPositions` método recupera a posição atual e a posição de parada.</span><span class="sxs-lookup"><span data-stu-id="6ac71-105">The `GetPositions` method retrieves the current position and the stop position.</span></span> <span data-ttu-id="6ac71-106">Esse método implementa o método [**IMediaSeeking:: Getposicionations**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) .</span><span class="sxs-lookup"><span data-stu-id="6ac71-106">This method implements the [**IMediaSeeking::GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ac71-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6ac71-107">Syntax</span></span>


```C++
HRESULT GetPositions(
   LONGLONG *pCurrent,
   LONGLONG *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="6ac71-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ac71-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ac71-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="6ac71-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="6ac71-110">Ponteiro para uma variável que recebe a posição inicial.</span><span class="sxs-lookup"><span data-stu-id="6ac71-110">Pointer to a variable that receives the start position.</span></span>

</dd> <dt>

<span data-ttu-id="6ac71-111">*pStop*</span><span class="sxs-lookup"><span data-stu-id="6ac71-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="6ac71-112">Ponteiro para uma variável que recebe a posição de parada.</span><span class="sxs-lookup"><span data-stu-id="6ac71-112">Pointer to a variable that receives the stop position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ac71-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6ac71-113">Return value</span></span>

<span data-ttu-id="6ac71-114">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6ac71-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ac71-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ac71-115">Remarks</span></span>

<span data-ttu-id="6ac71-116">Para o parâmetro *pCurrent* , esse método retorna o valor da variável de membro [**CSourceSeeking:: m \_ rtStart**](csourceseeking-m-rtstart.md) , que representa a hora de busca mais recente, não a posição de streaming atual.</span><span class="sxs-lookup"><span data-stu-id="6ac71-116">For the *pCurrent* parameter, this method returns the value of the [**CSourceSeeking::m\_rtStart**](csourceseeking-m-rtstart.md) member variable, which represents the latest seek time, not the current streaming position.</span></span> <span data-ttu-id="6ac71-117">No entanto, quando um aplicativo chama **IMediaSeeking:: getposições** por meio do Gerenciador de gráfico de filtro, os valores normalmente são provenientes de um filtro de processador, não de um filtro de origem.</span><span class="sxs-lookup"><span data-stu-id="6ac71-117">However, when an application calls **IMediaSeeking::GetPositions** through the filter graph manager, the values typically come from a renderer filter, not a source filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ac71-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ac71-118">Requirements</span></span>



| <span data-ttu-id="6ac71-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ac71-119">Requirement</span></span> | <span data-ttu-id="6ac71-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6ac71-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ac71-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6ac71-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6ac71-122"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ac71-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6ac71-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6ac71-123">Library</span></span><br/> | <dl> <span data-ttu-id="6ac71-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="6ac71-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ac71-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ac71-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ac71-126">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="6ac71-126">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




