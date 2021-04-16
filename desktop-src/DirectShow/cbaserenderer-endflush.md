---
description: O método EndFlush termina uma operação de liberação.
ms.assetid: 4c30abbf-7351-4eee-af9a-9330f6d1aa08
title: Método CBaseRenderer. EndFlush (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bd565bfa21edb9945b901d8e315f3e1d1cd054f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757434"
---
# <a name="cbaserendererendflush-method"></a><span data-ttu-id="15456-103">Método CBaseRenderer. EndFlush</span><span class="sxs-lookup"><span data-stu-id="15456-103">CBaseRenderer.EndFlush method</span></span>

<span data-ttu-id="15456-104">O `EndFlush` método encerra uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="15456-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="15456-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15456-105">Syntax</span></span>


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="15456-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15456-106">Parameters</span></span>

<span data-ttu-id="15456-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="15456-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="15456-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="15456-108">Return value</span></span>

<span data-ttu-id="15456-109">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="15456-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="15456-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="15456-110">Remarks</span></span>

<span data-ttu-id="15456-111">O pino de entrada do filtro chama esse método quando recebe uma chamada para o método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="15456-111">The filter's input pin calls this method when it receives a call to the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="15456-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15456-112">Requirements</span></span>



| <span data-ttu-id="15456-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="15456-113">Requirement</span></span> | <span data-ttu-id="15456-114">Valor</span><span class="sxs-lookup"><span data-stu-id="15456-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15456-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="15456-115">Header</span></span><br/>  | <dl> <span data-ttu-id="15456-116"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="15456-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="15456-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="15456-117">Library</span></span><br/> | <dl> <span data-ttu-id="15456-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="15456-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15456-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="15456-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15456-120">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="15456-120">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




