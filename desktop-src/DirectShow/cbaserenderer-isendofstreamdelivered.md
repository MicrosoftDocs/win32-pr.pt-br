---
description: O método IsEndOfStreamDelivered consulta se o \_ evento EC Complete foi entregue ao Gerenciador do grafo de filtro.
ms.assetid: 13138626-35b0-4da1-9c7e-5d22d86ad2e3
title: Método CBaseRenderer. IsEndOfStreamDelivered (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.IsEndOfStreamDelivered
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f60216afc6481411010fb2f2b0618c36a7d7acf4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755357"
---
# <a name="cbaserendererisendofstreamdelivered-method"></a><span data-ttu-id="1b871-103">Método CBaseRenderer. IsEndOfStreamDelivered</span><span class="sxs-lookup"><span data-stu-id="1b871-103">CBaseRenderer.IsEndOfStreamDelivered method</span></span>

<span data-ttu-id="1b871-104">O `IsEndOfStreamDelivered` método consulta se o \_ evento EC Complete foi entregue ao Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="1b871-104">The `IsEndOfStreamDelivered` method queries whether the EC\_COMPLETE event has been delivered to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b871-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1b871-105">Syntax</span></span>


```C++
BOOL IsEndOfStreamDelivered();
```



## <a name="parameters"></a><span data-ttu-id="1b871-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1b871-106">Parameters</span></span>

<span data-ttu-id="1b871-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1b871-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1b871-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1b871-108">Return value</span></span>

<span data-ttu-id="1b871-109">Retorna o sinalizador [**\_ bEOSDelivered CBaseRenderer:: m**](cbaserenderer-m-beosdelivered.md) .</span><span class="sxs-lookup"><span data-stu-id="1b871-109">Returns the [**CBaseRenderer::m\_bEOSDelivered**](cbaserenderer-m-beosdelivered.md) flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b871-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b871-110">Requirements</span></span>



| <span data-ttu-id="1b871-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b871-111">Requirement</span></span> | <span data-ttu-id="1b871-112">Valor</span><span class="sxs-lookup"><span data-stu-id="1b871-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b871-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1b871-113">Header</span></span><br/>  | <dl> <span data-ttu-id="1b871-114"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1b871-114"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1b871-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1b871-115">Library</span></span><br/> | <dl> <span data-ttu-id="1b871-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="1b871-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b871-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b871-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b871-118">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="1b871-118">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




