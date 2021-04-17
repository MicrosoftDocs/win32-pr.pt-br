---
description: 'O método EndFlush termina uma operação de liberação. Esse método substitui o método CTransformFilter:: EndFlush.'
ms.assetid: e7dfc6f9-1630-426b-95b2-9814331b5e61
title: Método CVideoTransformFilter. EndFlush (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca160bd2e3e66df3bcf6f293abe6f828309172c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749009"
---
# <a name="cvideotransformfilterendflush-method"></a><span data-ttu-id="c3abb-104">Método CVideoTransformFilter. EndFlush</span><span class="sxs-lookup"><span data-stu-id="c3abb-104">CVideoTransformFilter.EndFlush method</span></span>

<span data-ttu-id="c3abb-105">O `EndFlush` método encerra uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="c3abb-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="c3abb-106">Esse método substitui o método [**CTransformFilter:: EndFlush**](ctransformfilter-endflush.md) .</span><span class="sxs-lookup"><span data-stu-id="c3abb-106">This method overrides the [**CTransformFilter::EndFlush**](ctransformfilter-endflush.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3abb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3abb-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="c3abb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3abb-108">Parameters</span></span>

<span data-ttu-id="c3abb-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c3abb-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c3abb-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c3abb-110">Return value</span></span>

<span data-ttu-id="c3abb-111">Retorna S \_ OK se for bem-sucedido ou um código de erro.</span><span class="sxs-lookup"><span data-stu-id="c3abb-111">Returns S\_OK if successful, or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3abb-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3abb-112">Remarks</span></span>

<span data-ttu-id="c3abb-113">Esse método redefine todas as medidas de desempenho internas do filtro.</span><span class="sxs-lookup"><span data-stu-id="c3abb-113">This method resets all of the filter's internal performance measurements.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3abb-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3abb-114">Requirements</span></span>



| <span data-ttu-id="c3abb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3abb-115">Requirement</span></span> | <span data-ttu-id="c3abb-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c3abb-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3abb-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3abb-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c3abb-118"><dt>Vtrans. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3abb-118"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c3abb-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c3abb-119">Library</span></span><br/> | <dl> <span data-ttu-id="c3abb-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c3abb-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3abb-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3abb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3abb-122">**Classe CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="c3abb-122">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




