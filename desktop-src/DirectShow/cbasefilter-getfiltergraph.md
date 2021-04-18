---
description: O método GetFilterGraph recupera um ponteiro para o Gerenciador do grafo de filtro.
ms.assetid: 80b41272-2ca1-40db-8624-0d99d66f3c34
title: Método CBaseFilter. GetFilterGraph (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c0843c7789afc1500565d2737d863cbc8af114d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752519"
---
# <a name="cbasefiltergetfiltergraph-method"></a><span data-ttu-id="02acc-103">Método CBaseFilter. GetFilterGraph</span><span class="sxs-lookup"><span data-stu-id="02acc-103">CBaseFilter.GetFilterGraph method</span></span>

<span data-ttu-id="02acc-104">O `GetFilterGraph` método recupera um ponteiro para o Gerenciador de gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="02acc-104">The `GetFilterGraph` method retrieves a pointer to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="02acc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02acc-105">Syntax</span></span>


```C++
IFilterGraph* GetFilterGraph();
```



## <a name="parameters"></a><span data-ttu-id="02acc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02acc-106">Parameters</span></span>

<span data-ttu-id="02acc-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="02acc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="02acc-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="02acc-108">Return value</span></span>

<span data-ttu-id="02acc-109">Retorna o valor de [**CBaseFilter:: m \_ pGraph**](cbasefilter-m-pgraph.md).</span><span class="sxs-lookup"><span data-stu-id="02acc-109">Returns the value of [**CBaseFilter::m\_pGraph**](cbasefilter-m-pgraph.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="02acc-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02acc-110">Requirements</span></span>



| <span data-ttu-id="02acc-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="02acc-111">Requirement</span></span> | <span data-ttu-id="02acc-112">Valor</span><span class="sxs-lookup"><span data-stu-id="02acc-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02acc-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="02acc-113">Header</span></span><br/>  | <dl> <span data-ttu-id="02acc-114"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="02acc-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="02acc-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="02acc-115">Library</span></span><br/> | <dl> <span data-ttu-id="02acc-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="02acc-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02acc-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="02acc-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02acc-118">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="02acc-118">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




