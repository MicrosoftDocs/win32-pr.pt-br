---
description: O método FindPinNumber recupera o número de um PIN especificado no filtro.
ms.assetid: c9366fcc-7b13-4e43-883e-6003c32fadec
title: Método CSource. FindPinNumber (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.FindPinNumber
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6a71c65efd97c48eed58fb7d0b5aa8fcc2f178e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779241"
---
# <a name="csourcefindpinnumber-method"></a><span data-ttu-id="9f754-103">Método CSource. FindPinNumber</span><span class="sxs-lookup"><span data-stu-id="9f754-103">CSource.FindPinNumber method</span></span>

<span data-ttu-id="9f754-104">O `FindPinNumber` método recupera o número de um PIN especificado no filtro.</span><span class="sxs-lookup"><span data-stu-id="9f754-104">The `FindPinNumber` method retrieves the number of a specified pin on the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f754-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f754-105">Syntax</span></span>


```C++
int FindPinNumber(
   IPin *iPin
);
```



## <a name="parameters"></a><span data-ttu-id="9f754-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f754-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f754-107">*iPin*</span><span class="sxs-lookup"><span data-stu-id="9f754-107">*iPin*</span></span> 
</dt> <dd>

<span data-ttu-id="9f754-108">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do PIN.</span><span class="sxs-lookup"><span data-stu-id="9f754-108">Pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f754-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9f754-109">Return value</span></span>

<span data-ttu-id="9f754-110">Retorna o número do PIN ou 1 se o PIN não for encontrado neste filtro.</span><span class="sxs-lookup"><span data-stu-id="9f754-110">Returns the pin number, or  1 if the pin is not found on this filter.</span></span> <span data-ttu-id="9f754-111">O primeiro PIN é numerado como zero.</span><span class="sxs-lookup"><span data-stu-id="9f754-111">The first pin is numbered zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f754-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f754-112">Requirements</span></span>



| <span data-ttu-id="9f754-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f754-113">Requirement</span></span> | <span data-ttu-id="9f754-114">Valor</span><span class="sxs-lookup"><span data-stu-id="9f754-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f754-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9f754-115">Header</span></span><br/>  | <dl> <span data-ttu-id="9f754-116"><dt>Source. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f754-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="9f754-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9f754-117">Library</span></span><br/> | <dl> <span data-ttu-id="9f754-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="9f754-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f754-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f754-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f754-120">**Classe CSource**</span><span class="sxs-lookup"><span data-stu-id="9f754-120">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




