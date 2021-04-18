---
description: O método Disconnect interrompe a conexão com o pino de saída.
ms.assetid: 6e362e32-7b74-4392-b46f-1ab47a30a07b
title: Método CPullPin. Disconnect (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec13a7f29a06bab4f79ddb58932796f8363adadc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756615"
---
# <a name="cpullpindisconnect-method"></a><span data-ttu-id="fbd2c-103">Método CPullPin. Disconnect</span><span class="sxs-lookup"><span data-stu-id="fbd2c-103">CPullPin.Disconnect method</span></span>

<span data-ttu-id="fbd2c-104">O `Disconnect` método interrompe a conexão com o pino de saída.</span><span class="sxs-lookup"><span data-stu-id="fbd2c-104">The `Disconnect` method breaks the connection with the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbd2c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fbd2c-105">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="fbd2c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fbd2c-106">Parameters</span></span>

<span data-ttu-id="fbd2c-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fbd2c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fbd2c-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fbd2c-108">Return value</span></span>

<span data-ttu-id="fbd2c-109">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fbd2c-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbd2c-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="fbd2c-110">Remarks</span></span>

<span data-ttu-id="fbd2c-111">Esse método interrompe qualquer conexão feita no método [**CPullPin:: Connect**](cpullpin-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="fbd2c-111">This method breaks any connection made in the [**CPullPin::Connect**](cpullpin-connect.md) method.</span></span> <span data-ttu-id="fbd2c-112">Chame esse método dentro de seu método [**IPin::D isconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) .</span><span class="sxs-lookup"><span data-stu-id="fbd2c-112">Call this method inside your [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) method.</span></span> <span data-ttu-id="fbd2c-113">(Se o PIN deriva de [**CBasePin**](cbasepin.md), substitua [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) para chamar esse método.)</span><span class="sxs-lookup"><span data-stu-id="fbd2c-113">(If your pin derives from [**CBasePin**](cbasepin.md), override [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) to call this method.)</span></span>

## <a name="requirements"></a><span data-ttu-id="fbd2c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbd2c-114">Requirements</span></span>



| <span data-ttu-id="fbd2c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbd2c-115">Requirement</span></span> | <span data-ttu-id="fbd2c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="fbd2c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbd2c-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fbd2c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="fbd2c-118"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbd2c-118"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="fbd2c-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fbd2c-119">Library</span></span><br/> | <dl> <span data-ttu-id="fbd2c-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="fbd2c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbd2c-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="fbd2c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbd2c-122">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="fbd2c-122">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




