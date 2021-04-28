---
description: Método CBaseInputPin. BreakConnect – o método BreakConnect libera o PIN de uma conexão.
ms.assetid: 73b228a9-0a59-4647-b400-c33fa06c7e34
title: Método CBaseInputPin. BreakConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5398f675e056da2c60747c0b4eb17c475771bdc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099734"
---
# <a name="cbaseinputpinbreakconnect-method"></a><span data-ttu-id="41e9e-103">Método CBaseInputPin. BreakConnect</span><span class="sxs-lookup"><span data-stu-id="41e9e-103">CBaseInputPin.BreakConnect method</span></span>

<span data-ttu-id="41e9e-104">O `BreakConnect` método libera o PIN de uma conexão.</span><span class="sxs-lookup"><span data-stu-id="41e9e-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="41e9e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="41e9e-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="41e9e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="41e9e-106">Parameters</span></span>

<span data-ttu-id="41e9e-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="41e9e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="41e9e-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="41e9e-108">Return value</span></span>

<span data-ttu-id="41e9e-109">Retorna S \_ OK se bem-sucedido ou um valor **HRESULT** que indica a causa do erro.</span><span class="sxs-lookup"><span data-stu-id="41e9e-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="41e9e-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="41e9e-110">Remarks</span></span>

<span data-ttu-id="41e9e-111">Esse método substitui o método [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="41e9e-111">This method overrides the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="41e9e-112">Ele desconfirma o alocador e libera a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .</span><span class="sxs-lookup"><span data-stu-id="41e9e-112">It decommits the allocator and releases the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

<span data-ttu-id="41e9e-113">Se você substituir esse método, chame o método de classe base do seu método de substituição.</span><span class="sxs-lookup"><span data-stu-id="41e9e-113">If you override this method, call the base-class method from your overriding method.</span></span> <span data-ttu-id="41e9e-114">Caso contrário, você pode causar vazamentos de memória.</span><span class="sxs-lookup"><span data-stu-id="41e9e-114">Otherwise, you might cause memory leaks.</span></span>

## <a name="requirements"></a><span data-ttu-id="41e9e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41e9e-115">Requirements</span></span>



| <span data-ttu-id="41e9e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="41e9e-116">Requirement</span></span> | <span data-ttu-id="41e9e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="41e9e-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41e9e-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="41e9e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="41e9e-119"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="41e9e-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="41e9e-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="41e9e-120">Library</span></span><br/> | <dl> <span data-ttu-id="41e9e-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="41e9e-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41e9e-122">Consulte também</span><span class="sxs-lookup"><span data-stu-id="41e9e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41e9e-123">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="41e9e-123">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




