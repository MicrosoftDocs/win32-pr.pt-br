---
description: 'O método Connect conecta o PIN a outro PIN. Esse método implementa o método IPin:: connect.'
ms.assetid: 8ea99d2f-09da-4b15-a3b0-04ceb7888bc1
title: Método CBasePin. Connect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Connect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ed8bcdab7e0909e59e7d9ec00645786f8ce48c02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752714"
---
# <a name="cbasepinconnect-method"></a><span data-ttu-id="6a7ee-104">Método CBasePin. Connect</span><span class="sxs-lookup"><span data-stu-id="6a7ee-104">CBasePin.Connect method</span></span>

<span data-ttu-id="6a7ee-105">O `Connect` método conecta o PIN a outro PIN.</span><span class="sxs-lookup"><span data-stu-id="6a7ee-105">The `Connect` method connects the pin to another pin.</span></span> <span data-ttu-id="6a7ee-106">Esse método implementa o método [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) .</span><span class="sxs-lookup"><span data-stu-id="6a7ee-106">This method implements the [**IPin::Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a7ee-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a7ee-107">Syntax</span></span>


```C++
HRESULT Connect(
         IPin          *pReceivePin,
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="6a7ee-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a7ee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a7ee-109">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="6a7ee-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="6a7ee-110">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de recebimento.</span><span class="sxs-lookup"><span data-stu-id="6a7ee-110">Pointer to the receiving pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="6a7ee-111">*PMT*</span><span class="sxs-lookup"><span data-stu-id="6a7ee-111">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="6a7ee-112">Ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica o tipo de mídia para a conexão.</span><span class="sxs-lookup"><span data-stu-id="6a7ee-112">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type for the connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a7ee-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6a7ee-113">Return value</span></span>

<span data-ttu-id="6a7ee-114">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6a7ee-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6a7ee-115">Os valores possíveis incluem os da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="6a7ee-115">Possible values include those in the following table.</span></span>



| <span data-ttu-id="6a7ee-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6a7ee-116">Return code</span></span>                                                                                                  | <span data-ttu-id="6a7ee-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="6a7ee-117">Description</span></span>                                                                        |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6a7ee-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6a7ee-118"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="6a7ee-119">Êxito.</span><span class="sxs-lookup"><span data-stu-id="6a7ee-119">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="6a7ee-120"><dt>**VFW \_ E \_ já \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="6a7ee-120"><dt>**VFW\_E\_ALREADY\_CONNECTED**</dt></span></span> </dl>    | <span data-ttu-id="6a7ee-121">O PIN já está conectado.</span><span class="sxs-lookup"><span data-stu-id="6a7ee-121">The pin is already connected.</span></span><br/>                                           |
| <dl> <span data-ttu-id="6a7ee-122"><dt>**VFW \_ E \_ nenhum \_ \_ tipo aceitável**</dt></span><span class="sxs-lookup"><span data-stu-id="6a7ee-122"><dt>**VFW\_E\_NO\_ACCEPTABLE\_TYPES**</dt></span></span> </dl> | <span data-ttu-id="6a7ee-123">Não foi possível encontrar um tipo de mídia aceitável.</span><span class="sxs-lookup"><span data-stu-id="6a7ee-123">Could not find an acceptable media type.</span></span><br/>                                |
| <dl> <span data-ttu-id="6a7ee-124"><dt>**VFW \_ E \_ não \_ parado**</dt></span><span class="sxs-lookup"><span data-stu-id="6a7ee-124"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl>          | <span data-ttu-id="6a7ee-125">O filtro está ativo e o PIN não dá suporte à reconexão dinâmica.</span><span class="sxs-lookup"><span data-stu-id="6a7ee-125">The filter is active and the pin does not support dynamic reconnection.</span></span><br/> |
| <dl> <span data-ttu-id="6a7ee-126"><dt>**\_tipo E \_ VFW \_ não \_ aceito**</dt></span><span class="sxs-lookup"><span data-stu-id="6a7ee-126"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl>   | <span data-ttu-id="6a7ee-127">O tipo de mídia especificado não é aceitável.</span><span class="sxs-lookup"><span data-stu-id="6a7ee-127">The specified media type is not acceptable.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="6a7ee-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a7ee-128">Remarks</span></span>

<span data-ttu-id="6a7ee-129">O parâmetro *PGTO* pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="6a7ee-129">The *pmt* parameter can be **NULL**.</span></span> <span data-ttu-id="6a7ee-130">Ele também pode especificar um tipo de mídia parcial, com um valor de GUID \_ NULL para o tipo, subtipo ou formato principal.</span><span class="sxs-lookup"><span data-stu-id="6a7ee-130">It can also specify a partial media type, with a value of GUID\_NULL for the major type, subtype, or format.</span></span>

<span data-ttu-id="6a7ee-131">Na classe base, esse método testa se o PIN já está conectado e se o filtro está parado.</span><span class="sxs-lookup"><span data-stu-id="6a7ee-131">In the base class, this method tests whether the pin is already connected and whether the filter is stopped.</span></span> <span data-ttu-id="6a7ee-132">Ele delega o restante do processo de conexão para o método [**CBasePin:: AgreeMediaType**](cbasepin-agreemediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="6a7ee-132">It delegates the rest of the connection process to the [**CBasePin::AgreeMediaType**](cbasepin-agreemediatype.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a7ee-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a7ee-133">Requirements</span></span>



| <span data-ttu-id="6a7ee-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a7ee-134">Requirement</span></span> | <span data-ttu-id="6a7ee-135">Valor</span><span class="sxs-lookup"><span data-stu-id="6a7ee-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a7ee-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6a7ee-136">Header</span></span><br/>  | <dl> <span data-ttu-id="6a7ee-137"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6a7ee-137"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6a7ee-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6a7ee-138">Library</span></span><br/> | <dl> <span data-ttu-id="6a7ee-139"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="6a7ee-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a7ee-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a7ee-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a7ee-141">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="6a7ee-141">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




