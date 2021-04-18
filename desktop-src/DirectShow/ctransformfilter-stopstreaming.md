---
description: O método StopStreaming é chamado quando o filtro alterna para o estado parado.
ms.assetid: cfebfed2-4105-4dea-8d47-60d6160ee337
title: Método CTransformFilter. StopStreaming (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.StopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4990b55ad87a4eb754af7101e762ce227a090993
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747371"
---
# <a name="ctransformfilterstopstreaming-method"></a><span data-ttu-id="fe090-103">Método CTransformFilter. StopStreaming</span><span class="sxs-lookup"><span data-stu-id="fe090-103">CTransformFilter.StopStreaming method</span></span>

<span data-ttu-id="fe090-104">O `StopStreaming` método é chamado quando o filtro alterna para o estado parado.</span><span class="sxs-lookup"><span data-stu-id="fe090-104">The `StopStreaming` method is called when the filter switches to the stopped state.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe090-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fe090-105">Syntax</span></span>


```C++
virtual HRESULT StopStreaming();
```



## <a name="parameters"></a><span data-ttu-id="fe090-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe090-106">Parameters</span></span>

<span data-ttu-id="fe090-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fe090-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fe090-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fe090-108">Return value</span></span>

<span data-ttu-id="fe090-109">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fe090-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe090-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe090-110">Remarks</span></span>

<span data-ttu-id="fe090-111">Esse método não faz nada na classe base, mas a classe derivada pode substituí-la.</span><span class="sxs-lookup"><span data-stu-id="fe090-111">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe090-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe090-112">Requirements</span></span>



| <span data-ttu-id="fe090-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe090-113">Requirement</span></span> | <span data-ttu-id="fe090-114">Valor</span><span class="sxs-lookup"><span data-stu-id="fe090-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe090-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fe090-115">Header</span></span><br/>  | <dl> <span data-ttu-id="fe090-116"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe090-116"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fe090-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fe090-117">Library</span></span><br/> | <dl> <span data-ttu-id="fe090-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="fe090-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe090-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe090-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe090-120">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="fe090-120">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




