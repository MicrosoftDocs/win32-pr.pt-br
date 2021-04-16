---
description: O método OnThreadStartPlay é chamado no início do método CSourceStream::D oBufferProcessingLoop.
ms.assetid: 16d3b28f-bfae-49af-b8e4-8cc8cb15ecab
title: Método CSourceStream. OnThreadStartPlay (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadStartPlay
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 857f27ad39fb9169e1ef67253d5232c7cbc3dbb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779239"
---
# <a name="csourcestreamonthreadstartplay-method"></a><span data-ttu-id="43a48-103">Método CSourceStream. OnThreadStartPlay</span><span class="sxs-lookup"><span data-stu-id="43a48-103">CSourceStream.OnThreadStartPlay method</span></span>

<span data-ttu-id="43a48-104">O `OnThreadStartPlay` método é chamado no início do método [**CSourceStream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) .</span><span class="sxs-lookup"><span data-stu-id="43a48-104">The `OnThreadStartPlay` method is called at the start of the [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="43a48-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43a48-105">Syntax</span></span>


```C++
virtual HRESULT OnThreadStartPlay();
```



## <a name="parameters"></a><span data-ttu-id="43a48-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43a48-106">Parameters</span></span>

<span data-ttu-id="43a48-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="43a48-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="43a48-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="43a48-108">Return value</span></span>

<span data-ttu-id="43a48-109">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="43a48-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="43a48-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="43a48-110">Remarks</span></span>

<span data-ttu-id="43a48-111">Esse método não faz nada na classe base; Ele está disponível para a classe derivada substituir.</span><span class="sxs-lookup"><span data-stu-id="43a48-111">This method does nothing in the base class; it is available for the derived class to override.</span></span>

## <a name="requirements"></a><span data-ttu-id="43a48-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43a48-112">Requirements</span></span>



| <span data-ttu-id="43a48-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="43a48-113">Requirement</span></span> | <span data-ttu-id="43a48-114">Valor</span><span class="sxs-lookup"><span data-stu-id="43a48-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43a48-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="43a48-115">Header</span></span><br/>  | <dl> <span data-ttu-id="43a48-116"><dt>Source. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="43a48-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="43a48-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="43a48-117">Library</span></span><br/> | <dl> <span data-ttu-id="43a48-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="43a48-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43a48-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="43a48-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43a48-120">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="43a48-120">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




