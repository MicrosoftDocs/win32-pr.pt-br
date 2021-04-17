---
description: O método GetPinVersion recupera um número de versão para o conjunto de Pins neste filtro.
ms.assetid: 6cc186b2-4d9f-4d1c-a8b3-975e9c248df7
title: Método CBaseFilter. GetPinVersion (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPinVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d8cb2e67f88ef7a02958cc851dd9b8c0c751096
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748231"
---
# <a name="cbasefiltergetpinversion-method"></a><span data-ttu-id="5c8f7-103">Método CBaseFilter. GetPinVersion</span><span class="sxs-lookup"><span data-stu-id="5c8f7-103">CBaseFilter.GetPinVersion method</span></span>

<span data-ttu-id="5c8f7-104">O `GetPinVersion` método recupera um número de versão para o conjunto de Pins neste filtro.</span><span class="sxs-lookup"><span data-stu-id="5c8f7-104">The `GetPinVersion` method retrieves a version number for the set of pins on this filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c8f7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5c8f7-105">Syntax</span></span>


```C++
virtual long GetPinVersion();
```



## <a name="parameters"></a><span data-ttu-id="5c8f7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5c8f7-106">Parameters</span></span>

<span data-ttu-id="5c8f7-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5c8f7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5c8f7-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5c8f7-108">Return value</span></span>

<span data-ttu-id="5c8f7-109">Retorna a variável de membro [**CBaseFilter:: m \_ PinVersion**](cbasefilter-m-pinversion.md) .</span><span class="sxs-lookup"><span data-stu-id="5c8f7-109">Returns the [**CBaseFilter::m\_PinVersion**](cbasefilter-m-pinversion.md) member variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c8f7-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="5c8f7-110">Remarks</span></span>

<span data-ttu-id="5c8f7-111">O construtor **CBaseFilter** Inicializa a versão do PIN como 1.</span><span class="sxs-lookup"><span data-stu-id="5c8f7-111">The **CBaseFilter** constructor initializes the pin version to 1.</span></span> <span data-ttu-id="5c8f7-112">Na classe base, esse número nunca é alterado.</span><span class="sxs-lookup"><span data-stu-id="5c8f7-112">In the base class, this number never changes.</span></span> <span data-ttu-id="5c8f7-113">Se o filtro cria ou destrói Pins dinamicamente, ele deve incrementar a versão do PIN sempre que os Pins forem alterados.</span><span class="sxs-lookup"><span data-stu-id="5c8f7-113">If the filter dynamically creates or destroys pins, it should increment the pin version whenever the pins change.</span></span> <span data-ttu-id="5c8f7-114">Para incrementar o número de versão, chame o método [**CBaseFilter:: IncrementPinVersion**](cbasefilter-incrementpinversion.md) .</span><span class="sxs-lookup"><span data-stu-id="5c8f7-114">To increment the version number, call the [**CBaseFilter::IncrementPinVersion**](cbasefilter-incrementpinversion.md) method.</span></span>

<span data-ttu-id="5c8f7-115">O objeto enumerador de PIN, que é implementado pela classe [**CEnumPins**](cenumpins.md) , usa a versão do PIN para manter-se sincronizado com o filtro.</span><span class="sxs-lookup"><span data-stu-id="5c8f7-115">The pin enumerator object, which is implemented by the [**CEnumPins**](cenumpins.md) class, uses the pin version to keep itself synchronized with the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c8f7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c8f7-116">Requirements</span></span>



| <span data-ttu-id="5c8f7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c8f7-117">Requirement</span></span> | <span data-ttu-id="5c8f7-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5c8f7-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c8f7-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5c8f7-119">Header</span></span><br/>  | <dl> <span data-ttu-id="5c8f7-120"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5c8f7-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5c8f7-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5c8f7-121">Library</span></span><br/> | <dl> <span data-ttu-id="5c8f7-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5c8f7-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c8f7-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c8f7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c8f7-124">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="5c8f7-124">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




