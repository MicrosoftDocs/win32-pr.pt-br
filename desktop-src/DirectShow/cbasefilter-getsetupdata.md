---
description: O método GetSetupData recupera os dados de registro para o filtro.
ms.assetid: 93582c75-4f40-492c-919c-c8a06dce7715
title: Método CBaseFilter. GetSetupData (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetSetupData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40223a22f4de4a078ce84f8ebe49bddd5ab13575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756201"
---
# <a name="cbasefiltergetsetupdata-method"></a><span data-ttu-id="a14da-103">Método CBaseFilter. GetSetupData</span><span class="sxs-lookup"><span data-stu-id="a14da-103">CBaseFilter.GetSetupData method</span></span>

<span data-ttu-id="a14da-104">O `GetSetupData` método recupera os dados de registro para o filtro.</span><span class="sxs-lookup"><span data-stu-id="a14da-104">The `GetSetupData` method retrieves the registration data for the filter.</span></span>

> [!Note]  
> <span data-ttu-id="a14da-105">Esse método é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="a14da-105">This method is obsolete.</span></span> <span data-ttu-id="a14da-106">Ele é chamado pelos métodos [**CBaseFilter:: Register**](cbasefilter-register.md) e [**CBaseFilter:: Unregister**](cbasefilter-unregister.md) .</span><span class="sxs-lookup"><span data-stu-id="a14da-106">It is called by the [**CBaseFilter::Register**](cbasefilter-register.md) and [**CBaseFilter::Unregister**](cbasefilter-unregister.md) methods.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a14da-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a14da-107">Syntax</span></span>


```C++
virtual LPAMOVIESETUP_FILTER GetSetupData();
```



## <a name="parameters"></a><span data-ttu-id="a14da-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a14da-108">Parameters</span></span>

<span data-ttu-id="a14da-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a14da-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a14da-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a14da-110">Return value</span></span>

<span data-ttu-id="a14da-111">Retorna um ponteiro para uma estrutura de [**\_ filtro AMOVIESETUP**](amoviesetup-filter.md) que contém informações de registro para o filtro.</span><span class="sxs-lookup"><span data-stu-id="a14da-111">Returns a pointer to an [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) structure containing registration information for the filter.</span></span>

## <a name="remarks"></a><span data-ttu-id="a14da-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="a14da-112">Remarks</span></span>

<span data-ttu-id="a14da-113">A classe base retorna **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a14da-113">The base class returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a14da-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a14da-114">Requirements</span></span>



| <span data-ttu-id="a14da-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a14da-115">Requirement</span></span> | <span data-ttu-id="a14da-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a14da-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a14da-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a14da-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a14da-118"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a14da-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a14da-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a14da-119">Library</span></span><br/> | <dl> <span data-ttu-id="a14da-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a14da-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a14da-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="a14da-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a14da-122">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="a14da-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




