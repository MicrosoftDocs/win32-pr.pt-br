---
description: O método Run sinaliza o thread de streaming para execução.
ms.assetid: 9aef7801-dcfb-4597-bccb-5ba19327b2d5
title: Método CSourceStream. Run (origem. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39093654677ab4828f8a1d5a01a8cf7deaf42507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779547"
---
# <a name="csourcestreamrun-method"></a><span data-ttu-id="e1d2c-103">Método CSourceStream. Run</span><span class="sxs-lookup"><span data-stu-id="e1d2c-103">CSourceStream.Run method</span></span>

<span data-ttu-id="e1d2c-104">O `Run` método sinaliza o thread de streaming a ser executado.</span><span class="sxs-lookup"><span data-stu-id="e1d2c-104">The `Run` method signals the streaming thread to run.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1d2c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e1d2c-105">Syntax</span></span>


```C++
HRESULT Run();
```



## <a name="parameters"></a><span data-ttu-id="e1d2c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1d2c-106">Parameters</span></span>

<span data-ttu-id="e1d2c-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e1d2c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e1d2c-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e1d2c-108">Return value</span></span>

<span data-ttu-id="e1d2c-109">Retorna S \_ OK ou E \_ inesperado.</span><span class="sxs-lookup"><span data-stu-id="e1d2c-109">Returns S\_OK or E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1d2c-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1d2c-110">Remarks</span></span>

<span data-ttu-id="e1d2c-111">Na classe base, esse método tem o mesmo efeito que a solicitação [**CSourceStream::P ause**](csourcestream-pause.md) e não é usado.</span><span class="sxs-lookup"><span data-stu-id="e1d2c-111">In the base class, this method has the same effect as the [**CSourceStream::Pause**](csourcestream-pause.md) request, and is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1d2c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1d2c-112">Requirements</span></span>



| <span data-ttu-id="e1d2c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1d2c-113">Requirement</span></span> | <span data-ttu-id="e1d2c-114">Valor</span><span class="sxs-lookup"><span data-stu-id="e1d2c-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1d2c-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e1d2c-115">Header</span></span><br/>  | <dl> <span data-ttu-id="e1d2c-116"><dt>Source. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e1d2c-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="e1d2c-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e1d2c-117">Library</span></span><br/> | <dl> <span data-ttu-id="e1d2c-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e1d2c-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1d2c-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1d2c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1d2c-120">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="e1d2c-120">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




