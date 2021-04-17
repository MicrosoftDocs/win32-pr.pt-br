---
description: O método SampleProps recupera as propriedades da amostra mais recente, em uma estrutura de \_ Propriedades am SAMPLE2 \_ .
ms.assetid: d4c98c35-f8b2-4111-bae9-4e0f58a0cc8a
title: Método CBaseInputPin. SampleProps (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.SampleProps
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 45663cfd221c7a31abe5f85a494869b24d1ddd8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752908"
---
# <a name="cbaseinputpinsampleprops-method"></a><span data-ttu-id="f5edb-103">Método CBaseInputPin. SampleProps</span><span class="sxs-lookup"><span data-stu-id="f5edb-103">CBaseInputPin.SampleProps method</span></span>

<span data-ttu-id="f5edb-104">O `SampleProps` método recupera as propriedades da amostra mais recente, em uma estrutura [**de \_ \_ Propriedades SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .</span><span class="sxs-lookup"><span data-stu-id="f5edb-104">The `SampleProps` method retrieves the properties of the most recent sample, in an [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5edb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5edb-105">Syntax</span></span>


```C++
AM_SAMPLE2_PROPERTIES* SampleProps();
```



## <a name="parameters"></a><span data-ttu-id="f5edb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5edb-106">Parameters</span></span>

<span data-ttu-id="f5edb-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f5edb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f5edb-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f5edb-108">Return value</span></span>

<span data-ttu-id="f5edb-109">Retorna o endereço da variável de membro [**CBaseInputPin:: m \_ SampleProps**](cbaseinputpin-m-sampleprops.md) .</span><span class="sxs-lookup"><span data-stu-id="f5edb-109">Returns the address of the [**CBaseInputPin::m\_SampleProps**](cbaseinputpin-m-sampleprops.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5edb-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5edb-110">Requirements</span></span>



| <span data-ttu-id="f5edb-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5edb-111">Requirement</span></span> | <span data-ttu-id="f5edb-112">Valor</span><span class="sxs-lookup"><span data-stu-id="f5edb-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5edb-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f5edb-113">Header</span></span><br/>  | <dl> <span data-ttu-id="f5edb-114"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f5edb-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f5edb-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f5edb-115">Library</span></span><br/> | <dl> <span data-ttu-id="f5edb-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f5edb-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5edb-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5edb-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5edb-118">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="f5edb-118">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




