---
description: O método IncrementTypeVersion incrementa o número de versão no conjunto de tipos de mídia preferenciais.
ms.assetid: 30cad0ae-58e7-47f6-94ee-75e24ce0a7e9
title: Método CBasePin. IncrementTypeVersion (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.IncrementTypeVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6db3c08972bebbaf1172c44412ae9c8652100da8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748823"
---
# <a name="cbasepinincrementtypeversion-method"></a><span data-ttu-id="2f62c-103">Método CBasePin. IncrementTypeVersion</span><span class="sxs-lookup"><span data-stu-id="2f62c-103">CBasePin.IncrementTypeVersion method</span></span>

<span data-ttu-id="2f62c-104">O `IncrementTypeVersion` método incrementa o número de versão no conjunto de tipos de mídia preferenciais.</span><span class="sxs-lookup"><span data-stu-id="2f62c-104">The `IncrementTypeVersion` method increments the version number on the set of preferred media types.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f62c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f62c-105">Syntax</span></span>


```C++
void IncrementTypeVersion();
```



## <a name="parameters"></a><span data-ttu-id="2f62c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f62c-106">Parameters</span></span>

<span data-ttu-id="2f62c-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2f62c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2f62c-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2f62c-108">Return value</span></span>

<span data-ttu-id="2f62c-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="2f62c-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f62c-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f62c-110">Remarks</span></span>

<span data-ttu-id="2f62c-111">Esse método incrementa a variável de membro [**CBasePin:: m \_ TypeVersion**](cbasepin-m-typeversion.md) .</span><span class="sxs-lookup"><span data-stu-id="2f62c-111">This method increments the [**CBasePin::m\_TypeVersion**](cbasepin-m-typeversion.md) member variable.</span></span> <span data-ttu-id="2f62c-112">Se o PIN alterar dinamicamente a lista de tipos de mídia preferenciais, chame esse método sempre que a lista for alterada.</span><span class="sxs-lookup"><span data-stu-id="2f62c-112">If the pin dynamically changes the list of preferred media types, call this method whenever the list changes.</span></span> <span data-ttu-id="2f62c-113">Para obter mais informações, consulte [**CBasePin:: GetMediaTypeVersion**](cbasepin-getmediatypeversion.md).</span><span class="sxs-lookup"><span data-stu-id="2f62c-113">For more information, see [**CBasePin::GetMediaTypeVersion**](cbasepin-getmediatypeversion.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f62c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f62c-114">Requirements</span></span>



| <span data-ttu-id="2f62c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f62c-115">Requirement</span></span> | <span data-ttu-id="2f62c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="2f62c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f62c-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2f62c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="2f62c-118"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f62c-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2f62c-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2f62c-119">Library</span></span><br/> | <dl> <span data-ttu-id="2f62c-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="2f62c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f62c-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f62c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f62c-122">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="2f62c-122">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




