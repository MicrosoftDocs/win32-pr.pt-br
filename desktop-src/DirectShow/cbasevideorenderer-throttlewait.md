---
description: O método ThrottleWait insere um período de espera após cada quadro.
ms.assetid: 69306093-f5db-4170-b30f-e33cfa448e9f
title: Método CBaseVideoRenderer. ThrottleWait (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ThrottleWait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7408cfb011fa0fbbb223b6757ddb10ff9cbd357b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778511"
---
# <a name="cbasevideorendererthrottlewait-method"></a><span data-ttu-id="835bc-103">Método CBaseVideoRenderer. ThrottleWait</span><span class="sxs-lookup"><span data-stu-id="835bc-103">CBaseVideoRenderer.ThrottleWait method</span></span>

<span data-ttu-id="835bc-104">O `ThrottleWait` método insere um período de espera após cada quadro.</span><span class="sxs-lookup"><span data-stu-id="835bc-104">The `ThrottleWait` method inserts a wait period after each frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="835bc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="835bc-105">Syntax</span></span>


```C++
void ThrottleWait();
```



## <a name="parameters"></a><span data-ttu-id="835bc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="835bc-106">Parameters</span></span>

<span data-ttu-id="835bc-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="835bc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="835bc-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="835bc-108">Return value</span></span>

<span data-ttu-id="835bc-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="835bc-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="835bc-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="835bc-110">Remarks</span></span>

<span data-ttu-id="835bc-111">Essa função de membro aguarda um período de tempo obtido do membro de dados **m \_ trThrottle** .</span><span class="sxs-lookup"><span data-stu-id="835bc-111">This member function waits for a time period obtained from the **m\_trThrottle** data member.</span></span>

## <a name="requirements"></a><span data-ttu-id="835bc-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="835bc-112">Requirements</span></span>



| <span data-ttu-id="835bc-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="835bc-113">Requirement</span></span> | <span data-ttu-id="835bc-114">Valor</span><span class="sxs-lookup"><span data-stu-id="835bc-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="835bc-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="835bc-115">Header</span></span><br/>  | <dl> <span data-ttu-id="835bc-116"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="835bc-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="835bc-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="835bc-117">Library</span></span><br/> | <dl> <span data-ttu-id="835bc-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="835bc-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="835bc-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="835bc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="835bc-120">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="835bc-120">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




