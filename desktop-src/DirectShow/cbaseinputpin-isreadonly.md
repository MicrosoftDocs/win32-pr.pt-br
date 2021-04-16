---
description: Consulta se o alocador usa amostras de mídia somente leitura.
ms.assetid: 2cb692da-f030-4265-afe4-b1608b51fd47
title: Método CBaseInputPin. IsReadOnly (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.IsReadOnly
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93d1e7930631328a277ce7332f483ee264b2d525
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750071"
---
# <a name="cbaseinputpinisreadonly-method"></a><span data-ttu-id="ea7ee-103">Método CBaseInputPin. IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="ea7ee-103">CBaseInputPin.IsReadOnly method</span></span>

<span data-ttu-id="ea7ee-104">Consulta se o alocador usa amostras de mídia somente leitura.</span><span class="sxs-lookup"><span data-stu-id="ea7ee-104">Queries whether the allocator uses read-only media samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea7ee-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea7ee-105">Syntax</span></span>


```C++
BOOL IsReadOnly();
```



## <a name="parameters"></a><span data-ttu-id="ea7ee-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea7ee-106">Parameters</span></span>

<span data-ttu-id="ea7ee-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ea7ee-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ea7ee-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ea7ee-108">Return value</span></span>

<span data-ttu-id="ea7ee-109">Retorna o valor da variável de membro [**CBaseInputPin:: m \_ bReadOnly**](cbaseinputpin-m-breadonly.md) .</span><span class="sxs-lookup"><span data-stu-id="ea7ee-109">Returns the value of the [**CBaseInputPin::m\_bReadOnly**](cbaseinputpin-m-breadonly.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea7ee-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea7ee-110">Requirements</span></span>



| <span data-ttu-id="ea7ee-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea7ee-111">Requirement</span></span> | <span data-ttu-id="ea7ee-112">Valor</span><span class="sxs-lookup"><span data-stu-id="ea7ee-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea7ee-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ea7ee-113">Header</span></span><br/>  | <dl> <span data-ttu-id="ea7ee-114"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea7ee-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ea7ee-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ea7ee-115">Library</span></span><br/> | <dl> <span data-ttu-id="ea7ee-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ea7ee-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea7ee-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea7ee-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea7ee-118">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="ea7ee-118">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




