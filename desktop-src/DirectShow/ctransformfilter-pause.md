---
description: Método CTransformFilter. Pause – o método pause pausa o filtro. Esse método implementa o método IMediaFilter::P ause.
ms.assetid: 3e3afd14-1c92-4f2b-a367-e10caaeb3b63
title: Método CTransformFilter. PAUSE (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 903522b63754ff7972e4cdcf5221946442497896
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095094"
---
# <a name="ctransformfilterpause-method"></a><span data-ttu-id="22627-104">Método CTransformFilter. Pause</span><span class="sxs-lookup"><span data-stu-id="22627-104">CTransformFilter.Pause method</span></span>

<span data-ttu-id="22627-105">O `Pause` método pausa o filtro.</span><span class="sxs-lookup"><span data-stu-id="22627-105">The `Pause` method pauses the filter.</span></span> <span data-ttu-id="22627-106">Esse método implementa o método [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) .</span><span class="sxs-lookup"><span data-stu-id="22627-106">This method implements the [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="22627-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="22627-107">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="22627-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="22627-108">Parameters</span></span>

<span data-ttu-id="22627-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="22627-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="22627-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="22627-110">Return value</span></span>

<span data-ttu-id="22627-111">Retorna S \_ OK ou outro valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="22627-111">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="22627-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="22627-112">Remarks</span></span>

<span data-ttu-id="22627-113">Esse método chama o método [**StartStreaming**](ctransformfilter-startstreaming.md) .</span><span class="sxs-lookup"><span data-stu-id="22627-113">This method calls the [**StartStreaming**](ctransformfilter-startstreaming.md) method.</span></span> <span data-ttu-id="22627-114">O método **StartStreaming** não faz nada na classe base, mas a classe derivada pode substituí-la.</span><span class="sxs-lookup"><span data-stu-id="22627-114">The **StartStreaming** method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="22627-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22627-115">Requirements</span></span>



| <span data-ttu-id="22627-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="22627-116">Requirement</span></span> | <span data-ttu-id="22627-117">Valor</span><span class="sxs-lookup"><span data-stu-id="22627-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22627-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="22627-118">Header</span></span><br/>  | <dl> <span data-ttu-id="22627-119"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="22627-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="22627-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="22627-120">Library</span></span><br/> | <dl> <span data-ttu-id="22627-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="22627-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22627-122">Consulte também</span><span class="sxs-lookup"><span data-stu-id="22627-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22627-123">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="22627-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




