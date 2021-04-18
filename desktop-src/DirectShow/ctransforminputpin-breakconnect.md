---
description: O método BreakConnect libera o PIN de uma conexão.
ms.assetid: 9874717d-f4d8-426d-a717-9f5d83b4683c
title: Método CTransformInputPin. BreakConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2274b71b67a54ecacb291d77d2eef4ad8a110fa2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751238"
---
# <a name="ctransforminputpinbreakconnect-method"></a><span data-ttu-id="5543a-103">Método CTransformInputPin. BreakConnect</span><span class="sxs-lookup"><span data-stu-id="5543a-103">CTransformInputPin.BreakConnect method</span></span>

<span data-ttu-id="5543a-104">O `BreakConnect` método libera o PIN de uma conexão.</span><span class="sxs-lookup"><span data-stu-id="5543a-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5543a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5543a-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="5543a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5543a-106">Parameters</span></span>

<span data-ttu-id="5543a-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5543a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5543a-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5543a-108">Return value</span></span>

<span data-ttu-id="5543a-109">Retorna S \_ OK ou outro valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5543a-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5543a-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="5543a-110">Remarks</span></span>

<span data-ttu-id="5543a-111">Esse método substitui o método [**CBaseInputPin:: BreakConnect**](cbaseinputpin-breakconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="5543a-111">This method overrides the [**CBaseInputPin::BreakConnect**](cbaseinputpin-breakconnect.md) method.</span></span> <span data-ttu-id="5543a-112">Ele chama o método [**CTransformFilter:: BreakConnect**](ctransformfilter-breakconnect.md) do filtro, que retorna s \_ OK na classe base.</span><span class="sxs-lookup"><span data-stu-id="5543a-112">It calls the filter's [**CTransformFilter::BreakConnect**](ctransformfilter-breakconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="5543a-113">A classe derivada pode substituir o método **CTransformFilter:: BreakConnect** .</span><span class="sxs-lookup"><span data-stu-id="5543a-113">The derived class can override the **CTransformFilter::BreakConnect** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5543a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5543a-114">Requirements</span></span>



| <span data-ttu-id="5543a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5543a-115">Requirement</span></span> | <span data-ttu-id="5543a-116">Valor</span><span class="sxs-lookup"><span data-stu-id="5543a-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5543a-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5543a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5543a-118"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5543a-118"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5543a-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5543a-119">Library</span></span><br/> | <dl> <span data-ttu-id="5543a-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5543a-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




