---
description: O método Init Inicializa o thread de streaming.
ms.assetid: c746e595-de97-478c-8b22-5c4dd5594a8f
title: Método t CSourceStream.Ini(Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Init
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a3abf2b4637385616862c0613f72afd676f5b79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812989"
---
# <a name="csourcestreaminit-method"></a><span data-ttu-id="0fe0d-103">Método t CSourceStream.Ini</span><span class="sxs-lookup"><span data-stu-id="0fe0d-103">CSourceStream.Init method</span></span>

<span data-ttu-id="0fe0d-104">O `Init` método inicializa o thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="0fe0d-104">The `Init` method initializes the streaming thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fe0d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0fe0d-105">Syntax</span></span>


```C++
HRESULT Init();
```



## <a name="parameters"></a><span data-ttu-id="0fe0d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0fe0d-106">Parameters</span></span>

<span data-ttu-id="0fe0d-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0fe0d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0fe0d-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0fe0d-108">Return value</span></span>

<span data-ttu-id="0fe0d-109">Retorna S \_ OK ou outro valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0fe0d-109">Returns S\_OK, or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fe0d-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="0fe0d-110">Remarks</span></span>

<span data-ttu-id="0fe0d-111">Esse método deve ser a primeira solicitação de thread enviada ao método [**CSourceStream:: ThreadProc**](csourcestream-threadproc.md) .</span><span class="sxs-lookup"><span data-stu-id="0fe0d-111">This method must be the first thread request sent to the [**CSourceStream::ThreadProc**](csourcestream-threadproc.md) method.</span></span> <span data-ttu-id="0fe0d-112">O método [**CSourceStream:: active**](csourcestream-active.md) chama esse método.</span><span class="sxs-lookup"><span data-stu-id="0fe0d-112">The [**CSourceStream::Active**](csourcestream-active.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fe0d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fe0d-113">Requirements</span></span>



| <span data-ttu-id="0fe0d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fe0d-114">Requirement</span></span> | <span data-ttu-id="0fe0d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="0fe0d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fe0d-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0fe0d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="0fe0d-117"><dt>Source. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe0d-117"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="0fe0d-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0fe0d-118">Library</span></span><br/> | <dl> <span data-ttu-id="0fe0d-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe0d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fe0d-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="0fe0d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fe0d-121">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="0fe0d-121">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




