---
description: 'Método CBaseFilter. FindPin – o método FindPin recupera o PIN com o identificador especificado. Esse método implementa o método IBaseFilter:: FindPin.'
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
ms.openlocfilehash: 2bbef9b051a42597b2585a432f544eead4e2e0a1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099814"
---
# <a name="cbasefilterfindpin-method"></a><span data-ttu-id="88b6b-104">Método CBaseFilter. FindPin</span><span class="sxs-lookup"><span data-stu-id="88b6b-104">CBaseFilter.FindPin method</span></span>

<span data-ttu-id="88b6b-105">O `FindPin` método recupera o PIN com o identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="88b6b-105">The `FindPin` method retrieves the pin with the specified identifier.</span></span> <span data-ttu-id="88b6b-106">Esse método implementa o método [**IBaseFilter:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) .</span><span class="sxs-lookup"><span data-stu-id="88b6b-106">This method implements the [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="88b6b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88b6b-107">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="88b6b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88b6b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88b6b-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="88b6b-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="88b6b-110">Ponteiro para uma constante, Cadeia de caracteres Unicode terminada em nulo que identifica o PIN.</span><span class="sxs-lookup"><span data-stu-id="88b6b-110">Pointer to a constant, null-terminated Unicode string that identifies the pin.</span></span>

</dd> <dt>

<span data-ttu-id="88b6b-111">*ppPin*</span><span class="sxs-lookup"><span data-stu-id="88b6b-111">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="88b6b-112">Endereço de uma variável que recebe um ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do PIN.</span><span class="sxs-lookup"><span data-stu-id="88b6b-112">Address of a variable that receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88b6b-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="88b6b-113">Return value</span></span>

<span data-ttu-id="88b6b-114">Retorna um dos valores de **HRESULT** a seguir.</span><span class="sxs-lookup"><span data-stu-id="88b6b-114">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="88b6b-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="88b6b-115">Return code</span></span>                                                                                       | <span data-ttu-id="88b6b-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="88b6b-116">Description</span></span>                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="88b6b-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="88b6b-117"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="88b6b-118">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="88b6b-118">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="88b6b-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="88b6b-119"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="88b6b-120">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="88b6b-120">**NULL** pointer argument.</span></span><br/>     |
| <dl> <span data-ttu-id="88b6b-121"><dt>**VFW \_ E \_ não \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="88b6b-121"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="88b6b-122">Não foi possível localizar um PIN correspondente.</span><span class="sxs-lookup"><span data-stu-id="88b6b-122">Could not find a matching pin.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="88b6b-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="88b6b-123">Remarks</span></span>

<span data-ttu-id="88b6b-124">Esse método chama o método [**CBasePin:: Name**](cbasepin-name.md) para comparar o nome de cada PIN com a cadeia de caracteres especificada pelo parâmetro *ID* .</span><span class="sxs-lookup"><span data-stu-id="88b6b-124">This method calls the [**CBasePin::Name**](cbasepin-name.md) method to compare each pin's name against the string specified by the *Id* parameter.</span></span>

<span data-ttu-id="88b6b-125">Se o método tiver sucesso, a interface **IPin** terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="88b6b-125">If the method succeeds, the **IPin** interface has an outstanding reference count.</span></span> <span data-ttu-id="88b6b-126">Certifique-se de liberá-lo quando terminar.</span><span class="sxs-lookup"><span data-stu-id="88b6b-126">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="88b6b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88b6b-127">Requirements</span></span>



| <span data-ttu-id="88b6b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="88b6b-128">Requirement</span></span> | <span data-ttu-id="88b6b-129">Valor</span><span class="sxs-lookup"><span data-stu-id="88b6b-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88b6b-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="88b6b-130">Header</span></span><br/>  | <dl> <span data-ttu-id="88b6b-131"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88b6b-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="88b6b-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="88b6b-132">Library</span></span><br/> | <dl> <span data-ttu-id="88b6b-133"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="88b6b-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88b6b-134">Consulte também</span><span class="sxs-lookup"><span data-stu-id="88b6b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88b6b-135">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="88b6b-135">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




