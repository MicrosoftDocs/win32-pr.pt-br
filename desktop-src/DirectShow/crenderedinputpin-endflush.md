---
description: 'O método EndFlush termina uma operação de liberação. Esse método implementa o método IPin:: EndFlush.'
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
ms.openlocfilehash: 3d80f6cbc31a8bc5bf797847465a218f32631c1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756611"
---
# <a name="crenderedinputpinendflush-method"></a><span data-ttu-id="74cbb-104">Método CRenderedInputPin. EndFlush</span><span class="sxs-lookup"><span data-stu-id="74cbb-104">CRenderedInputPin.EndFlush method</span></span>

<span data-ttu-id="74cbb-105">O `EndFlush` método encerra uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="74cbb-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="74cbb-106">Esse método implementa o método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="74cbb-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="74cbb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="74cbb-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="74cbb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74cbb-108">Parameters</span></span>

<span data-ttu-id="74cbb-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="74cbb-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="74cbb-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="74cbb-110">Return value</span></span>

<span data-ttu-id="74cbb-111">Retorna S \_ OK se for bem-sucedido ou um código de erro do contrário.</span><span class="sxs-lookup"><span data-stu-id="74cbb-111">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="74cbb-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="74cbb-112">Remarks</span></span>

<span data-ttu-id="74cbb-113">Esse método limpa todos os eventos pendentes do [**EC \_ concluído**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="74cbb-113">This method clears any pending [**EC\_COMPLETE**](ec-complete.md) events.</span></span>

## <a name="requirements"></a><span data-ttu-id="74cbb-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74cbb-114">Requirements</span></span>



| <span data-ttu-id="74cbb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="74cbb-115">Requirement</span></span> | <span data-ttu-id="74cbb-116">Valor</span><span class="sxs-lookup"><span data-stu-id="74cbb-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74cbb-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="74cbb-117">Header</span></span><br/>  | <dl> <span data-ttu-id="74cbb-118"><dt>Amextra. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="74cbb-118"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="74cbb-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="74cbb-119">Library</span></span><br/> | <dl> <span data-ttu-id="74cbb-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="74cbb-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74cbb-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="74cbb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74cbb-122">**Classe CRenderedInputPin**</span><span class="sxs-lookup"><span data-stu-id="74cbb-122">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




