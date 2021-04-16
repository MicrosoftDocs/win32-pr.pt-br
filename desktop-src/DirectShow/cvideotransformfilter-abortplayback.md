---
description: O método AbortPlayback é usado para sinalizar um erro de streaming. Ele envia um \_ evento ERRORABORT do EC para o Gerenciador do grafo de filtro e envia um downstream de notificação de fim de fluxo.
ms.assetid: b48ec72f-d220-4b27-98fc-88eaa4f663eb
title: Método CVideoTransformFilter. AbortPlayback (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.AbortPlayback
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 952987dec315408920e92d79003480a01640d14e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779497"
---
# <a name="cvideotransformfilterabortplayback-method"></a><span data-ttu-id="cb040-104">Método CVideoTransformFilter. AbortPlayback</span><span class="sxs-lookup"><span data-stu-id="cb040-104">CVideoTransformFilter.AbortPlayback method</span></span>

<span data-ttu-id="cb040-105">O `AbortPlayback` método é usado para sinalizar um erro de streaming.</span><span class="sxs-lookup"><span data-stu-id="cb040-105">The `AbortPlayback` method is used to signal a streaming error.</span></span> <span data-ttu-id="cb040-106">Ele envia um [**evento \_ ERRORABORT do EC**](ec-errorabort.md) para o Gerenciador do grafo de filtro e envia um downstream de notificação de fim de fluxo.</span><span class="sxs-lookup"><span data-stu-id="cb040-106">It sends an [**EC\_ERRORABORT**](ec-errorabort.md) event to the Filter Graph Manager, and sends an end-of-stream notification downstream.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb040-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cb040-107">Syntax</span></span>


```C++
HRESULT AbortPlayback(
   HRESULT hr
);
```



## <a name="parameters"></a><span data-ttu-id="cb040-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cb040-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb040-109">*h*</span><span class="sxs-lookup"><span data-stu-id="cb040-109">*hr*</span></span> 
</dt> <dd>

<span data-ttu-id="cb040-110">Valor **HRESULT** da operação que falhou.</span><span class="sxs-lookup"><span data-stu-id="cb040-110">**HRESULT** value of the operation that failed.</span></span> <span data-ttu-id="cb040-111">Esse valor é usado como o primeiro parâmetro de evento para o \_ evento ERRORABORT do EC.</span><span class="sxs-lookup"><span data-stu-id="cb040-111">This value is used as the first event parameter for the EC\_ERRORABORT event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb040-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cb040-112">Return value</span></span>

<span data-ttu-id="cb040-113">Retorna o valor do parâmetro *HR* .</span><span class="sxs-lookup"><span data-stu-id="cb040-113">Returns the value of the *hr* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb040-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb040-114">Requirements</span></span>



| <span data-ttu-id="cb040-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb040-115">Requirement</span></span> | <span data-ttu-id="cb040-116">Valor</span><span class="sxs-lookup"><span data-stu-id="cb040-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb040-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cb040-117">Header</span></span><br/>  | <dl> <span data-ttu-id="cb040-118"><dt>Vtrans. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb040-118"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="cb040-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cb040-119">Library</span></span><br/> | <dl> <span data-ttu-id="cb040-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="cb040-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb040-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb040-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb040-122">**Classe CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="cb040-122">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




