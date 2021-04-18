---
description: O método GetMediaTypeVersion recupera um número de versão para o conjunto de tipos de mídia preferenciais.
ms.assetid: bd7b8070-eac5-458c-ada0-7fb0d789dd54
title: Método CBasePin. GetMediaTypeVersion (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetMediaTypeVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe01d33d7a7c1cb65bc0e2391af63e3519d9cce3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749031"
---
# <a name="cbasepingetmediatypeversion-method"></a><span data-ttu-id="1344f-103">Método CBasePin. GetMediaTypeVersion</span><span class="sxs-lookup"><span data-stu-id="1344f-103">CBasePin.GetMediaTypeVersion method</span></span>

<span data-ttu-id="1344f-104">O `GetMediaTypeVersion` método recupera um número de versão para o conjunto de tipos de mídia preferenciais.</span><span class="sxs-lookup"><span data-stu-id="1344f-104">The `GetMediaTypeVersion` method retrieves a version number for the set of preferred media types.</span></span>

## <a name="syntax"></a><span data-ttu-id="1344f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1344f-105">Syntax</span></span>


```C++
virtual LONG GetMediaTypeVersion();
```



## <a name="parameters"></a><span data-ttu-id="1344f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1344f-106">Parameters</span></span>

<span data-ttu-id="1344f-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1344f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1344f-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1344f-108">Return value</span></span>

<span data-ttu-id="1344f-109">Retorna a variável de membro [**CBasePin:: m \_ TypeVersion**](cbasepin-m-typeversion.md) .</span><span class="sxs-lookup"><span data-stu-id="1344f-109">Returns the [**CBasePin::m\_TypeVersion**](cbasepin-m-typeversion.md) member variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="1344f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="1344f-110">Remarks</span></span>

<span data-ttu-id="1344f-111">O construtor **CBasePin** Inicializa o número de versão para 1.</span><span class="sxs-lookup"><span data-stu-id="1344f-111">The **CBasePin** constructor initializes the version number to 1.</span></span> <span data-ttu-id="1344f-112">Na classe base, esse número nunca é alterado.</span><span class="sxs-lookup"><span data-stu-id="1344f-112">In the base class, this number never changes.</span></span> <span data-ttu-id="1344f-113">Se o PIN alterar dinamicamente sua lista de tipos de mídia preferenciais, ele deverá incrementar o número de versão sempre que a lista for alterada.</span><span class="sxs-lookup"><span data-stu-id="1344f-113">If the pin dynamically changes its list of preferred media types, it should increment the version number whenever the list changes.</span></span> <span data-ttu-id="1344f-114">Para incrementar o número de versão, chame o método [**CBasePin:: IncrementTypeVersion**](cbasepin-incrementtypeversion.md) .</span><span class="sxs-lookup"><span data-stu-id="1344f-114">To increment the version number, call the [**CBasePin::IncrementTypeVersion**](cbasepin-incrementtypeversion.md) method.</span></span>

<span data-ttu-id="1344f-115">O enumerador de tipo de mídia, que é implementado pela classe [**CEnumMediaTypes**](cenummediatypes.md) , usa o número de versão para manter-se sincronizado com o PIN.</span><span class="sxs-lookup"><span data-stu-id="1344f-115">The media type enumerator, which is implemented by the [**CEnumMediaTypes**](cenummediatypes.md) class, uses the version number to keep itself synchronized with the pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="1344f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1344f-116">Requirements</span></span>



| <span data-ttu-id="1344f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1344f-117">Requirement</span></span> | <span data-ttu-id="1344f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="1344f-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1344f-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1344f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="1344f-120"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1344f-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1344f-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1344f-121">Library</span></span><br/> | <dl> <span data-ttu-id="1344f-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="1344f-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1344f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="1344f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1344f-124">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="1344f-124">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




