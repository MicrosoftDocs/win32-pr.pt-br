---
description: O método checktime determina se um tempo especificado é devido.
ms.assetid: 522bc7ae-f998-4a7d-8bc3-caf09b4108a6
title: Método CCmdQueue. checktime (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.CheckTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 17fd67973e122830e53d93d1d8db17046f716507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775638"
---
# <a name="ccmdqueuechecktime-method"></a><span data-ttu-id="426a1-103">Método CCmdQueue. checktime</span><span class="sxs-lookup"><span data-stu-id="426a1-103">CCmdQueue.CheckTime method</span></span>

<span data-ttu-id="426a1-104">O `CheckTime` método determina se um tempo especificado é devido.</span><span class="sxs-lookup"><span data-stu-id="426a1-104">The `CheckTime` method determines if a specified time is due.</span></span>

## <a name="syntax"></a><span data-ttu-id="426a1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="426a1-105">Syntax</span></span>


```C++
BOOL CheckTime(
   CRefTime time,
   BOOL     bStream
);
```



## <a name="parameters"></a><span data-ttu-id="426a1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="426a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="426a1-107">*time*</span><span class="sxs-lookup"><span data-stu-id="426a1-107">*time*</span></span> 
</dt> <dd>

<span data-ttu-id="426a1-108">Tempo para verificar.</span><span class="sxs-lookup"><span data-stu-id="426a1-108">Time to check.</span></span>

</dd> <dt>

<span data-ttu-id="426a1-109">*bStream*</span><span class="sxs-lookup"><span data-stu-id="426a1-109">*bStream*</span></span> 
</dt> <dd>

<span data-ttu-id="426a1-110">**True** se o parâmetro *time* for um valor de tempo de fluxo; **False** se o *tempo* for um valor de tempo de apresentação.</span><span class="sxs-lookup"><span data-stu-id="426a1-110">**TRUE** if the *time* parameter is a stream-time value; **FALSE** if *time* is a presentation-time value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="426a1-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="426a1-111">Return value</span></span>

<span data-ttu-id="426a1-112">Retornará **true** se o tempo especificado ainda não tiver passado.</span><span class="sxs-lookup"><span data-stu-id="426a1-112">Returns **TRUE** if the specified time has not yet passed.</span></span>

## <a name="requirements"></a><span data-ttu-id="426a1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="426a1-113">Requirements</span></span>



| <span data-ttu-id="426a1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="426a1-114">Requirement</span></span> | <span data-ttu-id="426a1-115">Valor</span><span class="sxs-lookup"><span data-stu-id="426a1-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="426a1-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="426a1-116">Header</span></span><br/>  | <dl> <span data-ttu-id="426a1-117"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="426a1-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="426a1-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="426a1-118">Library</span></span><br/> | <dl> <span data-ttu-id="426a1-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="426a1-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="426a1-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="426a1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="426a1-121">**Classe CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="426a1-121">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




