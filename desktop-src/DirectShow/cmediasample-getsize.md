---
description: 'O método GetSize recupera o tamanho do buffer. Esse método implementa o método IMediaSample:: GetSize.'
ms.assetid: 14562ef4-f554-4d5a-83d3-1a29abae08a4
title: Método CMediaSample. GetSize (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff4146b66ca62905fe54eeb88d1e38ccf56ceea9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757702"
---
# <a name="cmediasamplegetsize-method"></a><span data-ttu-id="a0ca4-104">Método CMediaSample. GetSize</span><span class="sxs-lookup"><span data-stu-id="a0ca4-104">CMediaSample.GetSize method</span></span>

<span data-ttu-id="a0ca4-105">O `GetSize` método recupera o tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="a0ca4-105">The `GetSize` method retrieves the size of the buffer.</span></span> <span data-ttu-id="a0ca4-106">Esse método implementa o método [**IMediaSample:: GetSize**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getsize) .</span><span class="sxs-lookup"><span data-stu-id="a0ca4-106">This method implements the [**IMediaSample::GetSize**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getsize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0ca4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a0ca4-107">Syntax</span></span>


```C++
LONG GetSize();
```



## <a name="parameters"></a><span data-ttu-id="a0ca4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0ca4-108">Parameters</span></span>

<span data-ttu-id="a0ca4-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a0ca4-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a0ca4-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a0ca4-110">Return value</span></span>

<span data-ttu-id="a0ca4-111">Retorna o tamanho do buffer, em bytes.</span><span class="sxs-lookup"><span data-stu-id="a0ca4-111">Returns the size of the buffer, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0ca4-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0ca4-112">Requirements</span></span>



| <span data-ttu-id="a0ca4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0ca4-113">Requirement</span></span> | <span data-ttu-id="a0ca4-114">Valor</span><span class="sxs-lookup"><span data-stu-id="a0ca4-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ca4-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a0ca4-115">Header</span></span><br/>  | <dl> <span data-ttu-id="a0ca4-116"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0ca4-116"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a0ca4-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a0ca4-117">Library</span></span><br/> | <dl> <span data-ttu-id="a0ca4-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a0ca4-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0ca4-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="a0ca4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0ca4-120">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="a0ca4-120">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




