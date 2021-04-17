---
description: 'O método BeginFlush inicia uma operação de liberação. Implementa o método IPin:: BeginFlush.'
ms.assetid: f16c8337-5b7f-47e8-810d-00ffb3b5a1b4
title: Método CBaseOutputPin. BeginFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0216f74094d0c024d9b354dc594ff8d65315efbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769247"
---
# <a name="cbaseoutputpinbeginflush-method"></a><span data-ttu-id="683d9-104">Método CBaseOutputPin. BeginFlush</span><span class="sxs-lookup"><span data-stu-id="683d9-104">CBaseOutputPin.BeginFlush method</span></span>

<span data-ttu-id="683d9-105">O `BeginFlush` método inicia uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="683d9-105">The `BeginFlush` method begins a flush operation.</span></span> <span data-ttu-id="683d9-106">Implementa o método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .</span><span class="sxs-lookup"><span data-stu-id="683d9-106">Implements the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="683d9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="683d9-107">Syntax</span></span>


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="683d9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="683d9-108">Parameters</span></span>

<span data-ttu-id="683d9-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="683d9-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="683d9-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="683d9-110">Return value</span></span>

<span data-ttu-id="683d9-111">Retorna E \_ inesperado.</span><span class="sxs-lookup"><span data-stu-id="683d9-111">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="683d9-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="683d9-112">Remarks</span></span>

<span data-ttu-id="683d9-113">Esse método só deve ser chamado em Pins de entrada, portanto a implementação de **CBaseOutputPin** retorna E \_ inesperada.</span><span class="sxs-lookup"><span data-stu-id="683d9-113">This method should only be called on input pins, so the **CBaseOutputPin** implementation returns E\_UNEXPECTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="683d9-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="683d9-114">Requirements</span></span>



| <span data-ttu-id="683d9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="683d9-115">Requirement</span></span> | <span data-ttu-id="683d9-116">Valor</span><span class="sxs-lookup"><span data-stu-id="683d9-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="683d9-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="683d9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="683d9-118"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="683d9-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="683d9-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="683d9-119">Library</span></span><br/> | <dl> <span data-ttu-id="683d9-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="683d9-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="683d9-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="683d9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="683d9-122">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="683d9-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




