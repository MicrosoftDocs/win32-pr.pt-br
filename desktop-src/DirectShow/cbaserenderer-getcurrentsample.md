---
description: O método GetCurrentSample recupera o exemplo atual.
ms.assetid: cfdc66e3-7d32-47b7-87f6-99dd9513c93b
title: Método CBaseRenderer. GetCurrentSample (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetCurrentSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 48c42ff02b22d30138fcad7d1e8af5e57a391b99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752508"
---
# <a name="cbaserenderergetcurrentsample-method"></a><span data-ttu-id="30ae0-103">Método CBaseRenderer. GetCurrentSample</span><span class="sxs-lookup"><span data-stu-id="30ae0-103">CBaseRenderer.GetCurrentSample method</span></span>

<span data-ttu-id="30ae0-104">O `GetCurrentSample` método recupera o exemplo atual.</span><span class="sxs-lookup"><span data-stu-id="30ae0-104">The `GetCurrentSample` method retrieves the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="30ae0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30ae0-105">Syntax</span></span>


```C++
virtual IMediaSample* GetCurrentSample();
```



## <a name="parameters"></a><span data-ttu-id="30ae0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30ae0-106">Parameters</span></span>

<span data-ttu-id="30ae0-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="30ae0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="30ae0-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="30ae0-108">Return value</span></span>

<span data-ttu-id="30ae0-109">Retorna um ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo, ou **NULL** se nenhum exemplo estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="30ae0-109">Returns a pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface, or **NULL** if no sample is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="30ae0-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="30ae0-110">Remarks</span></span>

<span data-ttu-id="30ae0-111">A menos que o método retorne **NULL**, o método chama **AddRef** no ponteiro [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) antes de retorná-lo.</span><span class="sxs-lookup"><span data-stu-id="30ae0-111">Unless the method returns **NULL**, the method calls **AddRef** on the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) pointer before returning it.</span></span> <span data-ttu-id="30ae0-112">O chamador deve liberar o ponteiro.</span><span class="sxs-lookup"><span data-stu-id="30ae0-112">The caller must release the pointer.</span></span> <span data-ttu-id="30ae0-113">(Por implicação, você deve atribuir o valor de retorno a uma variável, para que você possa liberá-lo mais tarde.)</span><span class="sxs-lookup"><span data-stu-id="30ae0-113">(By implication, you must assign the return value to a variable, so that you can release it later.)</span></span>

## <a name="requirements"></a><span data-ttu-id="30ae0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30ae0-114">Requirements</span></span>



| <span data-ttu-id="30ae0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="30ae0-115">Requirement</span></span> | <span data-ttu-id="30ae0-116">Valor</span><span class="sxs-lookup"><span data-stu-id="30ae0-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30ae0-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="30ae0-117">Header</span></span><br/>  | <dl> <span data-ttu-id="30ae0-118"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="30ae0-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="30ae0-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="30ae0-119">Library</span></span><br/> | <dl> <span data-ttu-id="30ae0-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="30ae0-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30ae0-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="30ae0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30ae0-122">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="30ae0-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




