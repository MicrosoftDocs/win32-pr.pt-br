---
description: 'O método FindPin recupera o PIN com o identificador especificado. Esse método implementa o método IBaseFilter:: FindPin.'
ms.assetid: 152e4ff3-2809-4c57-b9c8-f51fc50b3703
title: Método CBaseFilter. FindPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98b49c547ec59a74185f7f719da660220de8480f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748831"
---
# <a name="cbasefilterfindpin-method"></a><span data-ttu-id="d09b8-104">Método CBaseFilter. FindPin</span><span class="sxs-lookup"><span data-stu-id="d09b8-104">CBaseFilter.FindPin method</span></span>

<span data-ttu-id="d09b8-105">O `FindPin` método recupera o PIN com o identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="d09b8-105">The `FindPin` method retrieves the pin with the specified identifier.</span></span> <span data-ttu-id="d09b8-106">Esse método implementa o método [**IBaseFilter:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) .</span><span class="sxs-lookup"><span data-stu-id="d09b8-106">This method implements the [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d09b8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d09b8-107">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="d09b8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d09b8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d09b8-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="d09b8-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="d09b8-110">Ponteiro para uma constante, Cadeia de caracteres Unicode terminada em nulo que identifica o PIN.</span><span class="sxs-lookup"><span data-stu-id="d09b8-110">Pointer to a constant, null-terminated Unicode string that identifies the pin.</span></span>

</dd> <dt>

<span data-ttu-id="d09b8-111">*ppPin*</span><span class="sxs-lookup"><span data-stu-id="d09b8-111">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="d09b8-112">Endereço de uma variável que recebe um ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do PIN.</span><span class="sxs-lookup"><span data-stu-id="d09b8-112">Address of a variable that receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d09b8-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d09b8-113">Return value</span></span>

<span data-ttu-id="d09b8-114">Retorna um dos valores de **HRESULT** a seguir.</span><span class="sxs-lookup"><span data-stu-id="d09b8-114">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="d09b8-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d09b8-115">Return code</span></span>                                                                                       | <span data-ttu-id="d09b8-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="d09b8-116">Description</span></span>                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="d09b8-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d09b8-117"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="d09b8-118">Êxito.</span><span class="sxs-lookup"><span data-stu-id="d09b8-118">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="d09b8-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="d09b8-119"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="d09b8-120">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="d09b8-120">**NULL** pointer argument.</span></span><br/>     |
| <dl> <span data-ttu-id="d09b8-121"><dt>**VFW \_ E \_ não \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="d09b8-121"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="d09b8-122">Não foi possível localizar um PIN correspondente.</span><span class="sxs-lookup"><span data-stu-id="d09b8-122">Could not find a matching pin.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d09b8-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="d09b8-123">Remarks</span></span>

<span data-ttu-id="d09b8-124">Esse método chama o método [**CBasePin:: Name**](cbasepin-name.md) para comparar o nome de cada PIN com a cadeia de caracteres especificada pelo parâmetro *ID* .</span><span class="sxs-lookup"><span data-stu-id="d09b8-124">This method calls the [**CBasePin::Name**](cbasepin-name.md) method to compare each pin's name against the string specified by the *Id* parameter.</span></span>

<span data-ttu-id="d09b8-125">Se o método tiver sucesso, a interface **IPin** terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="d09b8-125">If the method succeeds, the **IPin** interface has an outstanding reference count.</span></span> <span data-ttu-id="d09b8-126">Certifique-se de liberá-lo quando terminar.</span><span class="sxs-lookup"><span data-stu-id="d09b8-126">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="d09b8-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d09b8-127">Requirements</span></span>



| <span data-ttu-id="d09b8-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d09b8-128">Requirement</span></span> | <span data-ttu-id="d09b8-129">Valor</span><span class="sxs-lookup"><span data-stu-id="d09b8-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d09b8-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d09b8-130">Header</span></span><br/>  | <dl> <span data-ttu-id="d09b8-131"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d09b8-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d09b8-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d09b8-132">Library</span></span><br/> | <dl> <span data-ttu-id="d09b8-133"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d09b8-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d09b8-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="d09b8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d09b8-135">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="d09b8-135">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




