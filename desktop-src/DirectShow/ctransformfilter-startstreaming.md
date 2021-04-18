---
description: O método StartStreaming é chamado quando o filtro alterna para o estado pausado.
ms.assetid: 1e3bbca7-b5b1-41fd-8f70-b7ef39c9491b
title: Método CTransformFilter. StartStreaming (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 50df2db2aada7f96744af5e553f474818594d399
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748617"
---
# <a name="ctransformfilterstartstreaming-method"></a><span data-ttu-id="dfb89-103">Método CTransformFilter. StartStreaming</span><span class="sxs-lookup"><span data-stu-id="dfb89-103">CTransformFilter.StartStreaming method</span></span>

<span data-ttu-id="dfb89-104">O `StartStreaming` método é chamado quando o filtro alterna para o estado pausado.</span><span class="sxs-lookup"><span data-stu-id="dfb89-104">The `StartStreaming` method is called when the filter switches to the paused state.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfb89-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dfb89-105">Syntax</span></span>


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a><span data-ttu-id="dfb89-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dfb89-106">Parameters</span></span>

<span data-ttu-id="dfb89-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="dfb89-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dfb89-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dfb89-108">Return value</span></span>

<span data-ttu-id="dfb89-109">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dfb89-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfb89-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="dfb89-110">Remarks</span></span>

<span data-ttu-id="dfb89-111">Esse método não faz nada na classe base, mas a classe derivada pode substituí-la.</span><span class="sxs-lookup"><span data-stu-id="dfb89-111">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfb89-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfb89-112">Requirements</span></span>



| <span data-ttu-id="dfb89-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfb89-113">Requirement</span></span> | <span data-ttu-id="dfb89-114">Valor</span><span class="sxs-lookup"><span data-stu-id="dfb89-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfb89-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dfb89-115">Header</span></span><br/>  | <dl> <span data-ttu-id="dfb89-116"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dfb89-116"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="dfb89-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dfb89-117">Library</span></span><br/> | <dl> <span data-ttu-id="dfb89-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="dfb89-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfb89-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="dfb89-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfb89-120">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="dfb89-120">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




