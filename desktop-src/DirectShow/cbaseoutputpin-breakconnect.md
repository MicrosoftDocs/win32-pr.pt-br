---
description: Método CBaseOutputPin. BreakConnect – o método BreakConnect libera o PIN de uma conexão.
ms.assetid: 0dec3c9d-1adf-4fa3-ab5a-c351053f8054
title: Método CBaseOutputPin. BreakConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 746783a73892bc34273da4b020446f2668a19cd9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096214"
---
# <a name="cbaseoutputpinbreakconnect-method"></a><span data-ttu-id="ee593-103">Método CBaseOutputPin. BreakConnect</span><span class="sxs-lookup"><span data-stu-id="ee593-103">CBaseOutputPin.BreakConnect method</span></span>

<span data-ttu-id="ee593-104">O `BreakConnect` método libera o PIN de uma conexão.</span><span class="sxs-lookup"><span data-stu-id="ee593-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee593-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee593-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="ee593-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee593-106">Parameters</span></span>

<span data-ttu-id="ee593-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ee593-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ee593-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ee593-108">Return value</span></span>

<span data-ttu-id="ee593-109">Retorna S \_ OK se bem-sucedido ou um valor **HRESULT** que indica a causa do erro.</span><span class="sxs-lookup"><span data-stu-id="ee593-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee593-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee593-110">Remarks</span></span>

<span data-ttu-id="ee593-111">Esse método substitui o método [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="ee593-111">This method overrides the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="ee593-112">Ele desconfirma o alocador e libera as interfaces [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) e [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="ee593-112">It decommits the allocator and releases the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) and [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interfaces.</span></span>

<span data-ttu-id="ee593-113">Se você substituir esse método, chame o método de classe base do seu método de substituição.</span><span class="sxs-lookup"><span data-stu-id="ee593-113">If you override this method, call the base-class method from your overriding method.</span></span> <span data-ttu-id="ee593-114">Caso contrário, você pode causar vazamentos de memória.</span><span class="sxs-lookup"><span data-stu-id="ee593-114">Otherwise, you might cause memory leaks.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee593-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee593-115">Requirements</span></span>



| <span data-ttu-id="ee593-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee593-116">Requirement</span></span> | <span data-ttu-id="ee593-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ee593-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee593-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ee593-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ee593-119"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee593-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ee593-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ee593-120">Library</span></span><br/> | <dl> <span data-ttu-id="ee593-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ee593-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee593-122">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ee593-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee593-123">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="ee593-123">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




