---
description: Construtor de CTransformFilter. CTransformFilter-método de construtor.
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
ms.openlocfilehash: fce67bbe22361bdbae0cd3e51768e0cf0743d97d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098714"
---
# <a name="ctransformfilterctransformfilter-constructor"></a><span data-ttu-id="a333a-103">Construtor CTransformFilter. CTransformFilter</span><span class="sxs-lookup"><span data-stu-id="a333a-103">CTransformFilter.CTransformFilter constructor</span></span>

<span data-ttu-id="a333a-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="a333a-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a333a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a333a-105">Syntax</span></span>


```C++
CTransformFilter(
   TCHAR     *pObjectName,
   LPUNKNOWN lpUnk,
   CLSID     clsid
);
```



## <a name="parameters"></a><span data-ttu-id="a333a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a333a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a333a-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="a333a-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="a333a-108">Cadeia de caracteres que contém o nome de depuração do filtro.</span><span class="sxs-lookup"><span data-stu-id="a333a-108">String containing the debug name of the filter.</span></span> <span data-ttu-id="a333a-109">Para obter mais informações, consulte [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="a333a-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="a333a-110">*lpUnk*</span><span class="sxs-lookup"><span data-stu-id="a333a-110">*lpUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="a333a-111">Ponteiro para o proprietário deste objeto.</span><span class="sxs-lookup"><span data-stu-id="a333a-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="a333a-112">Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação.</span><span class="sxs-lookup"><span data-stu-id="a333a-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="a333a-113">Caso contrário, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a333a-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a333a-114">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="a333a-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="a333a-115">Identificador de classe do filtro.</span><span class="sxs-lookup"><span data-stu-id="a333a-115">Class identifier of the filter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a333a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a333a-116">Remarks</span></span>

<span data-ttu-id="a333a-117">O construtor não cria os Pins do filtro.</span><span class="sxs-lookup"><span data-stu-id="a333a-117">The constructor does not create the filter's pins.</span></span> <span data-ttu-id="a333a-118">Isso ocorre durante a primeira chamada para o método [**GetPin**](ctransformfilter-getpin.md) .</span><span class="sxs-lookup"><span data-stu-id="a333a-118">That happens during the first call to the [**GetPin**](ctransformfilter-getpin.md) method.</span></span> <span data-ttu-id="a333a-119">O construtor inicializa as variáveis de membro [**m \_ pInput**](ctransformfilter-m-pinput.md) e [**m \_ pOutput**](ctransformfilter-m-poutput.md) como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a333a-119">The constructor initializes the [**m\_pInput**](ctransformfilter-m-pinput.md) and [**m\_pOutput**](ctransformfilter-m-poutput.md) member variables to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a333a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a333a-120">Requirements</span></span>



| <span data-ttu-id="a333a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a333a-121">Requirement</span></span> | <span data-ttu-id="a333a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a333a-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a333a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a333a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a333a-124"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a333a-124"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a333a-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a333a-125">Library</span></span><br/> | <dl> <span data-ttu-id="a333a-126"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a333a-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a333a-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a333a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a333a-128">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="a333a-128">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




