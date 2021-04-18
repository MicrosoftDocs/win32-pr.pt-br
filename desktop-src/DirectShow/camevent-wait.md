---
description: O método Wait é bloqueado até que o evento seja sinalizado ou até que ocorra um tempo limite.
ms.assetid: bcc13723-a59b-4e8a-bfc8-eadb6facf116
title: Método CAMEvent. Wait (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Wait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ab5bc2aabf77fb73739528e99cda7961ae87e9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752116"
---
# <a name="cameventwait-method"></a><span data-ttu-id="f4dfe-103">Método CAMEvent. Wait</span><span class="sxs-lookup"><span data-stu-id="f4dfe-103">CAMEvent.Wait method</span></span>

<span data-ttu-id="f4dfe-104">O `Wait` método é bloqueado até que o evento seja sinalizado ou até que ocorra um tempo limite.</span><span class="sxs-lookup"><span data-stu-id="f4dfe-104">The `Wait` method blocks until the event is signaled, or until a time-out occurs.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4dfe-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f4dfe-105">Syntax</span></span>


```C++
BOOL Wait(
   DWORD dwTimeout = INFINITE
);
```



## <a name="parameters"></a><span data-ttu-id="f4dfe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4dfe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4dfe-107">*dwTimeout*</span><span class="sxs-lookup"><span data-stu-id="f4dfe-107">*dwTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="f4dfe-108">Valor de tempo limite opcional, representado em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="f4dfe-108">Optional time-out value, represented in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4dfe-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f4dfe-109">Return value</span></span>

<span data-ttu-id="f4dfe-110">Retornará **true** se o evento for sinalizado.</span><span class="sxs-lookup"><span data-stu-id="f4dfe-110">Returns **TRUE** if the event is signaled.</span></span> <span data-ttu-id="f4dfe-111">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="f4dfe-111">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4dfe-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4dfe-112">Remarks</span></span>

<span data-ttu-id="f4dfe-113">Para eventos de redefinição automática, o evento é redefinido para um estado não sinalizado quando esse método retorna.</span><span class="sxs-lookup"><span data-stu-id="f4dfe-113">For auto-reset events, the event is reset to a nonsignaled state when this method returns.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4dfe-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4dfe-114">Requirements</span></span>



| <span data-ttu-id="f4dfe-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4dfe-115">Requirement</span></span> | <span data-ttu-id="f4dfe-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f4dfe-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4dfe-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f4dfe-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f4dfe-118"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f4dfe-118"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f4dfe-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f4dfe-119">Library</span></span><br/> | <dl> <span data-ttu-id="f4dfe-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f4dfe-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4dfe-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4dfe-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4dfe-122">**Classe CAMEvent**</span><span class="sxs-lookup"><span data-stu-id="f4dfe-122">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




