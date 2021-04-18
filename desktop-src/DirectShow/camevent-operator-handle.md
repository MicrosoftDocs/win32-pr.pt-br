---
description: Recupera o identificador de evento. Não há suporte para esse operador como um L-Value.
ms.assetid: 9000d6d1-bbca-44ac-8808-0b3b827086c5
title: Método de identificador CAMEvent. Operator (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.operator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72193e89f415aabebfea4288fcdb986ccf8d73bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750716"
---
# <a name="cameventoperator-handle-method"></a><span data-ttu-id="15129-104">Método de identificador CAMEvent. Operator</span><span class="sxs-lookup"><span data-stu-id="15129-104">CAMEvent.operator HANDLE method</span></span>

<span data-ttu-id="15129-105">Recupera o identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="15129-105">Retrieves the event handle.</span></span> <span data-ttu-id="15129-106">Não há suporte para esse operador como um L-Value.</span><span class="sxs-lookup"><span data-stu-id="15129-106">This operator is not supported as an L-value.</span></span>

## <a name="syntax"></a><span data-ttu-id="15129-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15129-107">Syntax</span></span>


```C++
 operator HANDLE() const;
```



## <a name="parameters"></a><span data-ttu-id="15129-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15129-108">Parameters</span></span>

<span data-ttu-id="15129-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="15129-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="15129-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="15129-110">Return value</span></span>

<span data-ttu-id="15129-111">Retorna a variável de membro [**CAMEvent:: m \_ hEvent**](camevent-m-hevent.md) .</span><span class="sxs-lookup"><span data-stu-id="15129-111">Returns the [**CAMEvent::m\_hEvent**](camevent-m-hevent.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="15129-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15129-112">Requirements</span></span>



| <span data-ttu-id="15129-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="15129-113">Requirement</span></span> | <span data-ttu-id="15129-114">Valor</span><span class="sxs-lookup"><span data-stu-id="15129-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15129-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="15129-115">Header</span></span><br/>  | <dl> <span data-ttu-id="15129-116"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="15129-116"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="15129-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="15129-117">Library</span></span><br/> | <dl> <span data-ttu-id="15129-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="15129-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15129-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="15129-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15129-120">**Classe CAMEvent**</span><span class="sxs-lookup"><span data-stu-id="15129-120">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




