---
description: O método FindPin recupera o PIN com o identificador especificado.
ms.assetid: d07a298f-ddb0-44eb-85ca-81735875cdf3
title: Método CBaseRenderer. FindPin (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6e6789a91f34d95933ae7869e1588eeb14b6006
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758863"
---
# <a name="cbaserendererfindpin-method"></a><span data-ttu-id="f83dc-103">Método CBaseRenderer. FindPin</span><span class="sxs-lookup"><span data-stu-id="f83dc-103">CBaseRenderer.FindPin method</span></span>

<span data-ttu-id="f83dc-104">O `FindPin` método recupera o PIN com o identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="f83dc-104">The `FindPin` method retrieves the pin with the specified identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="f83dc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f83dc-105">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="f83dc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f83dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f83dc-107">*Id*</span><span class="sxs-lookup"><span data-stu-id="f83dc-107">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="f83dc-108">Ponteiro para uma constante, Cadeia de caracteres largo terminada em nulo que identifica o PIN.</span><span class="sxs-lookup"><span data-stu-id="f83dc-108">Pointer to a constant, null-terminated wide-character string that identifies the pin.</span></span> <span data-ttu-id="f83dc-109">Deve ser L "in".</span><span class="sxs-lookup"><span data-stu-id="f83dc-109">Must be L"In".</span></span>

</dd> <dt>

<span data-ttu-id="f83dc-110">*ppPin*</span><span class="sxs-lookup"><span data-stu-id="f83dc-110">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="f83dc-111">Endereço de uma variável que recebe um ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do PIN.</span><span class="sxs-lookup"><span data-stu-id="f83dc-111">Address of a variable that receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span> <span data-ttu-id="f83dc-112">Se o método falhar, *\* ppPin* será definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="f83dc-112">If the method fails, *\*ppPin* is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f83dc-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f83dc-113">Return value</span></span>

<span data-ttu-id="f83dc-114">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f83dc-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="f83dc-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f83dc-115">Return code</span></span>                                                                                       | <span data-ttu-id="f83dc-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="f83dc-116">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="f83dc-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f83dc-117"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="f83dc-118">Êxito.</span><span class="sxs-lookup"><span data-stu-id="f83dc-118">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="f83dc-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="f83dc-119"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="f83dc-120">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="f83dc-120">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="f83dc-121"><dt>**VFW \_ E \_ não \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="f83dc-121"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="f83dc-122">Não encontrado.</span><span class="sxs-lookup"><span data-stu-id="f83dc-122">Not found.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="f83dc-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="f83dc-123">Remarks</span></span>

<span data-ttu-id="f83dc-124">Esse método substitui o método [**CBaseFilter:: FindPin**](cbasefilter-findpin.md) .</span><span class="sxs-lookup"><span data-stu-id="f83dc-124">This method overrides the [**CBaseFilter::FindPin**](cbasefilter-findpin.md) method.</span></span> <span data-ttu-id="f83dc-125">O único PIN do filtro (o PIN de entrada) é denominado "in".</span><span class="sxs-lookup"><span data-stu-id="f83dc-125">The filter's only pin (the input pin) is named "In".</span></span>

## <a name="requirements"></a><span data-ttu-id="f83dc-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f83dc-126">Requirements</span></span>



| <span data-ttu-id="f83dc-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f83dc-127">Requirement</span></span> | <span data-ttu-id="f83dc-128">Valor</span><span class="sxs-lookup"><span data-stu-id="f83dc-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f83dc-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f83dc-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f83dc-130"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f83dc-130"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f83dc-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f83dc-131">Library</span></span><br/> | <dl> <span data-ttu-id="f83dc-132"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f83dc-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f83dc-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="f83dc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f83dc-134">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="f83dc-134">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




