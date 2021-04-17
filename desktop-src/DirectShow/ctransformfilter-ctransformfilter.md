---
description: Método de construtor.
ms.assetid: a64c3e29-91f2-455f-aac1-1e4ecce6958d
title: Construtor CTransformFilter. CTransformFilter (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CTransformFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39569dff69c2ab1ebb635cb69a4c71602a7400d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752485"
---
# <a name="ctransformfilterctransformfilter-constructor"></a><span data-ttu-id="9f41c-103">Construtor CTransformFilter. CTransformFilter</span><span class="sxs-lookup"><span data-stu-id="9f41c-103">CTransformFilter.CTransformFilter constructor</span></span>

<span data-ttu-id="9f41c-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="9f41c-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f41c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f41c-105">Syntax</span></span>


```C++
CTransformFilter(
   TCHAR     *pObjectName,
   LPUNKNOWN lpUnk,
   CLSID     clsid
);
```



## <a name="parameters"></a><span data-ttu-id="9f41c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f41c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f41c-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="9f41c-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="9f41c-108">Cadeia de caracteres que contém o nome de depuração do filtro.</span><span class="sxs-lookup"><span data-stu-id="9f41c-108">String containing the debug name of the filter.</span></span> <span data-ttu-id="9f41c-109">Para obter mais informações, consulte [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="9f41c-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f41c-110">*lpUnk*</span><span class="sxs-lookup"><span data-stu-id="9f41c-110">*lpUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="9f41c-111">Ponteiro para o proprietário deste objeto.</span><span class="sxs-lookup"><span data-stu-id="9f41c-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="9f41c-112">Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação.</span><span class="sxs-lookup"><span data-stu-id="9f41c-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="9f41c-113">Caso contrário, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9f41c-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9f41c-114">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="9f41c-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="9f41c-115">Identificador de classe do filtro.</span><span class="sxs-lookup"><span data-stu-id="9f41c-115">Class identifier of the filter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f41c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f41c-116">Remarks</span></span>

<span data-ttu-id="9f41c-117">O construtor não cria os Pins do filtro.</span><span class="sxs-lookup"><span data-stu-id="9f41c-117">The constructor does not create the filter's pins.</span></span> <span data-ttu-id="9f41c-118">Isso ocorre durante a primeira chamada para o método [**GetPin**](ctransformfilter-getpin.md) .</span><span class="sxs-lookup"><span data-stu-id="9f41c-118">That happens during the first call to the [**GetPin**](ctransformfilter-getpin.md) method.</span></span> <span data-ttu-id="9f41c-119">O construtor inicializa as variáveis de membro [**m \_ pInput**](ctransformfilter-m-pinput.md) e [**m \_ pOutput**](ctransformfilter-m-poutput.md) como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9f41c-119">The constructor initializes the [**m\_pInput**](ctransformfilter-m-pinput.md) and [**m\_pOutput**](ctransformfilter-m-poutput.md) member variables to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f41c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f41c-120">Requirements</span></span>



| <span data-ttu-id="9f41c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f41c-121">Requirement</span></span> | <span data-ttu-id="9f41c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9f41c-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f41c-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9f41c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9f41c-124"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f41c-124"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9f41c-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9f41c-125">Library</span></span><br/> | <dl> <span data-ttu-id="9f41c-126"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="9f41c-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f41c-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f41c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f41c-128">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="9f41c-128">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




