---
description: O método OnStartStreaming é chamado quando o filtro começa o streaming.
ms.assetid: 02a5b334-f6c4-4cba-8882-c6b36d97feb3
title: Método CBaseRenderer. OnStartStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnStartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 66433795b0674e1d2d5b7a7de5b1dcd1b50eb424
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752711"
---
# <a name="cbaserendereronstartstreaming-method"></a><span data-ttu-id="cb803-103">Método CBaseRenderer. OnStartStreaming</span><span class="sxs-lookup"><span data-stu-id="cb803-103">CBaseRenderer.OnStartStreaming method</span></span>

<span data-ttu-id="cb803-104">O `OnStartStreaming` método é chamado quando o filtro começa o streaming.</span><span class="sxs-lookup"><span data-stu-id="cb803-104">The `OnStartStreaming` method is called when the filter begins streaming.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb803-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cb803-105">Syntax</span></span>


```C++
virtual HRESULT OnStartStreaming();
```



## <a name="parameters"></a><span data-ttu-id="cb803-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cb803-106">Parameters</span></span>

<span data-ttu-id="cb803-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="cb803-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cb803-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cb803-108">Return value</span></span>

<span data-ttu-id="cb803-109">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cb803-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb803-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb803-110">Remarks</span></span>

<span data-ttu-id="cb803-111">O método [**CBaseRenderer:: StartStreaming**](cbaserenderer-startstreaming.md) chama esse método.</span><span class="sxs-lookup"><span data-stu-id="cb803-111">The [**CBaseRenderer::StartStreaming**](cbaserenderer-startstreaming.md) method calls this method.</span></span> <span data-ttu-id="cb803-112">Ele não faz nada na classe base, mas a classe derivada pode substituí-la.</span><span class="sxs-lookup"><span data-stu-id="cb803-112">It does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb803-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb803-113">Requirements</span></span>



| <span data-ttu-id="cb803-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb803-114">Requirement</span></span> | <span data-ttu-id="cb803-115">Valor</span><span class="sxs-lookup"><span data-stu-id="cb803-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb803-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cb803-116">Header</span></span><br/>  | <dl> <span data-ttu-id="cb803-117"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb803-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cb803-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cb803-118">Library</span></span><br/> | <dl> <span data-ttu-id="cb803-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="cb803-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb803-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb803-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb803-121">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="cb803-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




