---
description: 'Método CRenderedInputPin. EndFlush – o método EndFlush termina uma operação de liberação. Esse método implementa o método IPin:: EndFlush.'
ms.assetid: 5c27bf76-6886-431d-9958-5064c53909ec
title: Método CRenderedInputPin. EndFlush (Amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7be740df2b3b45d0b681a86b8f70bed8e1395e8f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098914"
---
# <a name="crenderedinputpinendflush-method"></a><span data-ttu-id="d51ca-104">Método CRenderedInputPin. EndFlush</span><span class="sxs-lookup"><span data-stu-id="d51ca-104">CRenderedInputPin.EndFlush method</span></span>

<span data-ttu-id="d51ca-105">O `EndFlush` método encerra uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="d51ca-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="d51ca-106">Esse método implementa o método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="d51ca-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d51ca-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d51ca-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="d51ca-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d51ca-108">Parameters</span></span>

<span data-ttu-id="d51ca-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d51ca-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d51ca-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d51ca-110">Return value</span></span>

<span data-ttu-id="d51ca-111">Retorna S \_ OK se for bem-sucedido ou um código de erro do contrário.</span><span class="sxs-lookup"><span data-stu-id="d51ca-111">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d51ca-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="d51ca-112">Remarks</span></span>

<span data-ttu-id="d51ca-113">Esse método limpa todos os eventos pendentes do [**EC \_ concluído**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="d51ca-113">This method clears any pending [**EC\_COMPLETE**](ec-complete.md) events.</span></span>

## <a name="requirements"></a><span data-ttu-id="d51ca-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d51ca-114">Requirements</span></span>



| <span data-ttu-id="d51ca-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d51ca-115">Requirement</span></span> | <span data-ttu-id="d51ca-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d51ca-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d51ca-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d51ca-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d51ca-118"><dt>Amextra. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d51ca-118"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d51ca-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d51ca-119">Library</span></span><br/> | <dl> <span data-ttu-id="d51ca-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d51ca-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d51ca-121">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d51ca-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d51ca-122">**Classe CRenderedInputPin**</span><span class="sxs-lookup"><span data-stu-id="d51ca-122">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




