---
description: O método Stop sinaliza o thread de streaming para parar.
ms.assetid: 79bc528a-cf53-43f3-aa17-c459063c99ab
title: Método CSourceStream. Stop (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 44c9f845c092280ef5fafa808036654bd868a796
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779546"
---
# <a name="csourcestreamstop-method"></a><span data-ttu-id="0bb48-103">Método CSourceStream. Stop</span><span class="sxs-lookup"><span data-stu-id="0bb48-103">CSourceStream.Stop method</span></span>

<span data-ttu-id="0bb48-104">O `Stop` método sinaliza o thread de streaming para parar.</span><span class="sxs-lookup"><span data-stu-id="0bb48-104">The `Stop` method signals the streaming thread to stop.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bb48-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0bb48-105">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="0bb48-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0bb48-106">Parameters</span></span>

<span data-ttu-id="0bb48-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0bb48-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0bb48-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0bb48-108">Return value</span></span>

<span data-ttu-id="0bb48-109">Retorna S \_ OK ou E \_ inesperado.</span><span class="sxs-lookup"><span data-stu-id="0bb48-109">Returns S\_OK or E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bb48-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="0bb48-110">Remarks</span></span>

<span data-ttu-id="0bb48-111">O método [**CSourceStream:: Inactive**](csourcestream-inactive.md) chama esse método.</span><span class="sxs-lookup"><span data-stu-id="0bb48-111">The [**CSourceStream::Inactive**](csourcestream-inactive.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bb48-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bb48-112">Requirements</span></span>



| <span data-ttu-id="0bb48-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bb48-113">Requirement</span></span> | <span data-ttu-id="0bb48-114">Valor</span><span class="sxs-lookup"><span data-stu-id="0bb48-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bb48-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0bb48-115">Header</span></span><br/>  | <dl> <span data-ttu-id="0bb48-116"><dt>Source. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0bb48-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="0bb48-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0bb48-117">Library</span></span><br/> | <dl> <span data-ttu-id="0bb48-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0bb48-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bb48-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="0bb48-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bb48-120">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="0bb48-120">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




