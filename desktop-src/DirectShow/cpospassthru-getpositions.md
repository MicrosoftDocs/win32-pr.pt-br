---
description: 'O método getpositiones recupera a posição atual e a posição de parada, em relação à duração total do fluxo. Esse método implementa o método IMediaSeeking:: getposicionations.'
ms.assetid: 51e45bc3-ae30-4b05-b9d9-684c1b028f51
title: Método CPosPassThru. GetPositions (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0852199e8e143ce5b0348c3b79afd495a5a47627
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748019"
---
# <a name="cpospassthrugetpositions-method"></a><span data-ttu-id="ff812-104">Método CPosPassThru. getpositiones</span><span class="sxs-lookup"><span data-stu-id="ff812-104">CPosPassThru.GetPositions method</span></span>

<span data-ttu-id="ff812-105">O `GetPositions` método recupera a posição atual e a posição de parada, em relação à duração total do fluxo.</span><span class="sxs-lookup"><span data-stu-id="ff812-105">The `GetPositions` method retrieves the current position and the stop position, relative to the total duration of the stream.</span></span> <span data-ttu-id="ff812-106">Esse método implementa o método [**IMediaSeeking:: Getposicionations**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) .</span><span class="sxs-lookup"><span data-stu-id="ff812-106">This method implements the [**IMediaSeeking::GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff812-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff812-107">Syntax</span></span>


```C++
HRESULT GetPositions(
   LONGLONG *pCurrent,
   LONGLONG *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="ff812-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff812-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff812-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="ff812-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="ff812-110">Ponteiro para uma variável que recebe a posição atual, em unidades do formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="ff812-110">Pointer to a variable that receives the current position, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="ff812-111">*pStop*</span><span class="sxs-lookup"><span data-stu-id="ff812-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="ff812-112">Ponteiro para uma variável que recebe a posição de parada, em unidades do formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="ff812-112">Pointer to a variable that receives the stop position, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff812-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ff812-113">Return value</span></span>

<span data-ttu-id="ff812-114">Retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="ff812-114">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff812-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff812-115">Requirements</span></span>



| <span data-ttu-id="ff812-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff812-116">Requirement</span></span> | <span data-ttu-id="ff812-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ff812-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff812-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ff812-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ff812-119"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ff812-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ff812-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ff812-120">Library</span></span><br/> | <dl> <span data-ttu-id="ff812-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ff812-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff812-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff812-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff812-123">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="ff812-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




