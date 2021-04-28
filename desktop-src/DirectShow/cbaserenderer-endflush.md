---
description: Método CBaseRenderer. EndFlush – o método EndFlush termina uma operação de liberação.
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
ms.openlocfilehash: 87e29f405430ca87943773d19793ffc1941ec42c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095904"
---
# <a name="cbaserendererendflush-method"></a><span data-ttu-id="52c39-103">Método CBaseRenderer. EndFlush</span><span class="sxs-lookup"><span data-stu-id="52c39-103">CBaseRenderer.EndFlush method</span></span>

<span data-ttu-id="52c39-104">O `EndFlush` método encerra uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="52c39-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="52c39-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52c39-105">Syntax</span></span>


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="52c39-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52c39-106">Parameters</span></span>

<span data-ttu-id="52c39-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="52c39-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="52c39-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="52c39-108">Return value</span></span>

<span data-ttu-id="52c39-109">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="52c39-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="52c39-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="52c39-110">Remarks</span></span>

<span data-ttu-id="52c39-111">O pino de entrada do filtro chama esse método quando recebe uma chamada para o método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="52c39-111">The filter's input pin calls this method when it receives a call to the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="52c39-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52c39-112">Requirements</span></span>



| <span data-ttu-id="52c39-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="52c39-113">Requirement</span></span> | <span data-ttu-id="52c39-114">Valor</span><span class="sxs-lookup"><span data-stu-id="52c39-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52c39-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="52c39-115">Header</span></span><br/>  | <dl> <span data-ttu-id="52c39-116"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="52c39-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="52c39-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="52c39-117">Library</span></span><br/> | <dl> <span data-ttu-id="52c39-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="52c39-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52c39-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="52c39-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52c39-120">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="52c39-120">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




