---
description: Método CTransformOutputPin. BreakConnect – o método BreakConnect libera o PIN de uma conexão.
ms.assetid: bf68aca3-93e5-4f9d-9980-1a5eed1513f5
title: Método CTransformOutputPin. BreakConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 92854041e1d553945d0a1ab1755ef3557bd4a8b2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084954"
---
# <a name="ctransformoutputpinbreakconnect-method"></a><span data-ttu-id="70e28-103">Método CTransformOutputPin. BreakConnect</span><span class="sxs-lookup"><span data-stu-id="70e28-103">CTransformOutputPin.BreakConnect method</span></span>

<span data-ttu-id="70e28-104">O `BreakConnect` método libera o PIN de uma conexão.</span><span class="sxs-lookup"><span data-stu-id="70e28-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="70e28-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="70e28-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="70e28-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="70e28-106">Parameters</span></span>

<span data-ttu-id="70e28-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="70e28-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="70e28-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="70e28-108">Return value</span></span>

<span data-ttu-id="70e28-109">Retorna S \_ OK ou outro valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="70e28-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="70e28-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="70e28-110">Remarks</span></span>

<span data-ttu-id="70e28-111">Esse método substitui o método [**CBaseOutputPin:: BreakConnect**](cbaseoutputpin-breakconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="70e28-111">This method overrides the [**CBaseOutputPin::BreakConnect**](cbaseoutputpin-breakconnect.md) method.</span></span> <span data-ttu-id="70e28-112">Ele chama o método [**CTransformFilter:: BreakConnect**](ctransformfilter-breakconnect.md) do filtro, que retorna s \_ OK na classe base.</span><span class="sxs-lookup"><span data-stu-id="70e28-112">It calls the filter's [**CTransformFilter::BreakConnect**](ctransformfilter-breakconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="70e28-113">A classe derivada pode substituir o método **CTransformFilter:: BreakConnect** .</span><span class="sxs-lookup"><span data-stu-id="70e28-113">The derived class can override the **CTransformFilter::BreakConnect** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="70e28-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70e28-114">Requirements</span></span>



| <span data-ttu-id="70e28-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="70e28-115">Requirement</span></span> | <span data-ttu-id="70e28-116">Valor</span><span class="sxs-lookup"><span data-stu-id="70e28-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70e28-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="70e28-117">Header</span></span><br/>  | <dl> <span data-ttu-id="70e28-118"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="70e28-118"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="70e28-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="70e28-119">Library</span></span><br/> | <dl> <span data-ttu-id="70e28-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="70e28-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




