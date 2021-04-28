---
description: 'Método CBaseOutputPin. EndFlush – o método EndFlush termina uma operação de liberação. Esse método implementa o método IPin:: EndFlush.'
ms.assetid: c5c76cf8-1ca1-4fef-8776-7f4dcca32939
title: Método CBaseOutputPin. EndFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 53153c6dbd941390c7ef616ee36c56e01214c341
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099504"
---
# <a name="cbaseoutputpinendflush-method"></a><span data-ttu-id="97ace-104">Método CBaseOutputPin. EndFlush</span><span class="sxs-lookup"><span data-stu-id="97ace-104">CBaseOutputPin.EndFlush method</span></span>

<span data-ttu-id="97ace-105">O `EndFlush` método encerra uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="97ace-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="97ace-106">Esse método implementa o método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="97ace-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="97ace-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="97ace-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="97ace-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97ace-108">Parameters</span></span>

<span data-ttu-id="97ace-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="97ace-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="97ace-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="97ace-110">Return value</span></span>

<span data-ttu-id="97ace-111">Retorna E \_ inesperado.</span><span class="sxs-lookup"><span data-stu-id="97ace-111">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="97ace-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="97ace-112">Remarks</span></span>

<span data-ttu-id="97ace-113">Esse método só deve ser chamado em Pins de entrada, portanto a implementação de **CBaseOutputPin** retorna E \_ inesperada.</span><span class="sxs-lookup"><span data-stu-id="97ace-113">This method should only be called on input pins, so the **CBaseOutputPin** implementation returns E\_UNEXPECTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="97ace-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97ace-114">Requirements</span></span>



| <span data-ttu-id="97ace-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="97ace-115">Requirement</span></span> | <span data-ttu-id="97ace-116">Valor</span><span class="sxs-lookup"><span data-stu-id="97ace-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97ace-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="97ace-117">Header</span></span><br/>  | <dl> <span data-ttu-id="97ace-118"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="97ace-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="97ace-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="97ace-119">Library</span></span><br/> | <dl> <span data-ttu-id="97ace-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="97ace-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97ace-121">Consulte também</span><span class="sxs-lookup"><span data-stu-id="97ace-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97ace-122">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="97ace-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




