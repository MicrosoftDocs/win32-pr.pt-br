---
description: O método GetMediaTime recupera os carimbos de data/hora no exemplo atual.
ms.assetid: 36f3b6d3-b884-4168-94f3-f334a5056c7d
title: Método CPosPassThru. GetMediaTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b2748d986f121a38041155dcd43f13a647916486
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760755"
---
# <a name="cpospassthrugetmediatime-method"></a><span data-ttu-id="80926-103">Método CPosPassThru. GetMediaTime</span><span class="sxs-lookup"><span data-stu-id="80926-103">CPosPassThru.GetMediaTime method</span></span>

<span data-ttu-id="80926-104">O `GetMediaTime` método recupera os carimbos de data/hora no exemplo atual.</span><span class="sxs-lookup"><span data-stu-id="80926-104">The `GetMediaTime` method retrieves the time stamps on the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="80926-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80926-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="80926-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="80926-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80926-107">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="80926-107">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="80926-108">Ponteiro para uma variável que recebe a hora de início, em unidades do formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="80926-108">Pointer to a variable that receives the start time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="80926-109">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="80926-109">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="80926-110">Ponteiro para uma variável que recebe a hora de término, em unidades do formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="80926-110">Pointer to a variable that receives the end time, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80926-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="80926-111">Return value</span></span>

<span data-ttu-id="80926-112">Retorna E \_ falha.</span><span class="sxs-lookup"><span data-stu-id="80926-112">Returns E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="80926-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="80926-113">Remarks</span></span>

<span data-ttu-id="80926-114">Substitua esse método se o filtro armazenar em cache os carimbos de data/hora nos exemplos que receber.</span><span class="sxs-lookup"><span data-stu-id="80926-114">Override this method if your filter caches the time stamps on the samples it receives.</span></span>

## <a name="requirements"></a><span data-ttu-id="80926-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80926-115">Requirements</span></span>



| <span data-ttu-id="80926-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="80926-116">Requirement</span></span> | <span data-ttu-id="80926-117">Valor</span><span class="sxs-lookup"><span data-stu-id="80926-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80926-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="80926-118">Header</span></span><br/>  | <dl> <span data-ttu-id="80926-119"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="80926-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="80926-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="80926-120">Library</span></span><br/> | <dl> <span data-ttu-id="80926-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="80926-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80926-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="80926-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80926-123">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="80926-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




