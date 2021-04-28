---
description: Método CTransformInputPin. BreakConnect – o método BreakConnect libera o PIN de uma conexão.
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
ms.openlocfilehash: fe425ba617909dcfb1d66dbb4777b579139d436b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085014"
---
# <a name="ctransforminputpinbreakconnect-method"></a><span data-ttu-id="fa955-103">Método CTransformInputPin. BreakConnect</span><span class="sxs-lookup"><span data-stu-id="fa955-103">CTransformInputPin.BreakConnect method</span></span>

<span data-ttu-id="fa955-104">O `BreakConnect` método libera o PIN de uma conexão.</span><span class="sxs-lookup"><span data-stu-id="fa955-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa955-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa955-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="fa955-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa955-106">Parameters</span></span>

<span data-ttu-id="fa955-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fa955-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fa955-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="fa955-108">Return value</span></span>

<span data-ttu-id="fa955-109">Retorna S \_ OK ou outro valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fa955-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa955-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa955-110">Remarks</span></span>

<span data-ttu-id="fa955-111">Esse método substitui o método [**CBaseInputPin:: BreakConnect**](cbaseinputpin-breakconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="fa955-111">This method overrides the [**CBaseInputPin::BreakConnect**](cbaseinputpin-breakconnect.md) method.</span></span> <span data-ttu-id="fa955-112">Ele chama o método [**CTransformFilter:: BreakConnect**](ctransformfilter-breakconnect.md) do filtro, que retorna s \_ OK na classe base.</span><span class="sxs-lookup"><span data-stu-id="fa955-112">It calls the filter's [**CTransformFilter::BreakConnect**](ctransformfilter-breakconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="fa955-113">A classe derivada pode substituir o método **CTransformFilter:: BreakConnect** .</span><span class="sxs-lookup"><span data-stu-id="fa955-113">The derived class can override the **CTransformFilter::BreakConnect** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa955-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa955-114">Requirements</span></span>



| <span data-ttu-id="fa955-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa955-115">Requirement</span></span> | <span data-ttu-id="fa955-116">Valor</span><span class="sxs-lookup"><span data-stu-id="fa955-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa955-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fa955-117">Header</span></span><br/>  | <dl> <span data-ttu-id="fa955-118"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fa955-118"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fa955-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fa955-119">Library</span></span><br/> | <dl> <span data-ttu-id="fa955-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="fa955-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




