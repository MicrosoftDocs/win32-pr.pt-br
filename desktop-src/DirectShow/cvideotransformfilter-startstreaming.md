---
description: 'O método StartStreaming é chamado quando o filtro alterna para o estado pausado. Esse método substitui o método CTransformFilter:: StartStreaming.'
ms.assetid: fa05f88f-fed8-479d-b0b4-d9df982d51e7
title: Método CVideoTransformFilter. StartStreaming (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5ae8d49401389830f9d5dbf0ec91e7f390c51ca6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758476"
---
# <a name="cvideotransformfilterstartstreaming-method"></a><span data-ttu-id="da63b-104">Método CVideoTransformFilter. StartStreaming</span><span class="sxs-lookup"><span data-stu-id="da63b-104">CVideoTransformFilter.StartStreaming method</span></span>

<span data-ttu-id="da63b-105">O `StartStreaming` método é chamado quando o filtro alterna para o estado pausado.</span><span class="sxs-lookup"><span data-stu-id="da63b-105">The `StartStreaming` method is called when the filter switches to the paused state.</span></span> <span data-ttu-id="da63b-106">Esse método substitui o método [**CTransformFilter:: StartStreaming**](ctransformfilter-startstreaming.md) .</span><span class="sxs-lookup"><span data-stu-id="da63b-106">This method overrides the [**CTransformFilter::StartStreaming**](ctransformfilter-startstreaming.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="da63b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="da63b-107">Syntax</span></span>


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a><span data-ttu-id="da63b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="da63b-108">Parameters</span></span>

<span data-ttu-id="da63b-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="da63b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="da63b-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="da63b-110">Return value</span></span>

<span data-ttu-id="da63b-111">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="da63b-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="da63b-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="da63b-112">Remarks</span></span>

<span data-ttu-id="da63b-113">Esse método redefine todas as estatísticas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="da63b-113">This method resets all of the performance statistics.</span></span>

## <a name="requirements"></a><span data-ttu-id="da63b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da63b-114">Requirements</span></span>



| <span data-ttu-id="da63b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="da63b-115">Requirement</span></span> | <span data-ttu-id="da63b-116">Valor</span><span class="sxs-lookup"><span data-stu-id="da63b-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da63b-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="da63b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="da63b-118"><dt>Vtrans. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da63b-118"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="da63b-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="da63b-119">Library</span></span><br/> | <dl> <span data-ttu-id="da63b-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="da63b-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da63b-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="da63b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da63b-122">**Classe CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="da63b-122">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




