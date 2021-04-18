---
description: 'O método inativo notifica o PIN de que o filtro não está mais ativo. Esse método substitui o método CBasePin:: Inactive. Se o thread de streaming estiver ativo, esse método o interromperá e aguardará a saída do thread.'
ms.assetid: 82cf0f13-e563-4a0b-b2e1-25ab19f7ed78
title: Método CSourceStream. Inactive (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c4fab336f5f06d932189ee991fd190d1ae42b27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767682"
---
# <a name="csourcestreaminactive-method"></a><span data-ttu-id="4f765-105">Método CSourceStream. Inactive</span><span class="sxs-lookup"><span data-stu-id="4f765-105">CSourceStream.Inactive method</span></span>

<span data-ttu-id="4f765-106">O `Inactive` método notifica o PIN de que o filtro não está mais ativo.</span><span class="sxs-lookup"><span data-stu-id="4f765-106">The `Inactive` method notifies the pin that the filter is no longer active.</span></span> <span data-ttu-id="4f765-107">Esse método substitui o método [**CBasePin:: Inactive**](cbasepin-inactive.md) .</span><span class="sxs-lookup"><span data-stu-id="4f765-107">This method overrides the [**CBasePin::Inactive**](cbasepin-inactive.md) method.</span></span> <span data-ttu-id="4f765-108">Se o thread de streaming estiver ativo, esse método o interromperá e aguardará a saída do thread.</span><span class="sxs-lookup"><span data-stu-id="4f765-108">If the streaming thread is active, this method stops it and waits for the thread to exit.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f765-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f765-109">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="4f765-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f765-110">Parameters</span></span>

<span data-ttu-id="4f765-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4f765-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4f765-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4f765-112">Return value</span></span>

<span data-ttu-id="4f765-113">Retorna S \_ OK ou outro valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4f765-113">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f765-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f765-114">Requirements</span></span>



| <span data-ttu-id="4f765-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f765-115">Requirement</span></span> | <span data-ttu-id="4f765-116">Valor</span><span class="sxs-lookup"><span data-stu-id="4f765-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f765-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4f765-117">Header</span></span><br/>  | <dl> <span data-ttu-id="4f765-118"><dt>Source. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f765-118"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4f765-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4f765-119">Library</span></span><br/> | <dl> <span data-ttu-id="4f765-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4f765-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f765-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f765-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f765-122">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="4f765-122">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




