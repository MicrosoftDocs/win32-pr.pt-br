---
description: 'O método ReceiveConnection aceita uma conexão de outro PIN. Esse método implementa o método IPin:: ReceiveConnection.'
ms.assetid: f17e7d93-ac45-4b8a-98c6-0c76ec7117c9
title: Método CBasePin. ReceiveConnection (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ReceiveConnection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d0a8134201af1d3c931121f59a20360020a53a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749632"
---
# <a name="cbasepinreceiveconnection-method"></a><span data-ttu-id="b8a3a-104">Método CBasePin. ReceiveConnection</span><span class="sxs-lookup"><span data-stu-id="b8a3a-104">CBasePin.ReceiveConnection method</span></span>

<span data-ttu-id="b8a3a-105">O `ReceiveConnection` método aceita uma conexão de outro PIN.</span><span class="sxs-lookup"><span data-stu-id="b8a3a-105">The `ReceiveConnection` method accepts a connection from another pin.</span></span> <span data-ttu-id="b8a3a-106">Esse método implementa o método [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) .</span><span class="sxs-lookup"><span data-stu-id="b8a3a-106">This method implements the [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8a3a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8a3a-107">Syntax</span></span>


```C++
HRESULT ReceiveConnection(
   IPin          *pConnector,
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="b8a3a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8a3a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8a3a-109">*pConnector*</span><span class="sxs-lookup"><span data-stu-id="b8a3a-109">*pConnector*</span></span> 
</dt> <dd>

<span data-ttu-id="b8a3a-110">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do PIN de conexão.</span><span class="sxs-lookup"><span data-stu-id="b8a3a-110">Pointer to the connecting pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="b8a3a-111">*PMT*</span><span class="sxs-lookup"><span data-stu-id="b8a3a-111">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="b8a3a-112">Ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="b8a3a-112">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8a3a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b8a3a-113">Return value</span></span>

<span data-ttu-id="b8a3a-114">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b8a3a-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b8a3a-115">Os valores possíveis incluem os da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b8a3a-115">Possible values include those in the following table.</span></span>



| <span data-ttu-id="b8a3a-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b8a3a-116">Return code</span></span>                                                                                                | <span data-ttu-id="b8a3a-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="b8a3a-117">Description</span></span>                                                                        |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b8a3a-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b8a3a-118"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="b8a3a-119">Êxito.</span><span class="sxs-lookup"><span data-stu-id="b8a3a-119">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="b8a3a-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="b8a3a-120"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="b8a3a-121">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="b8a3a-121">**NULL** pointer argument.</span></span><br/>                                              |
| <dl> <span data-ttu-id="b8a3a-122"><dt>**VFW \_ E \_ já \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="b8a3a-122"><dt>**VFW\_E\_ALREADY\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="b8a3a-123">O PIN já está conectado.</span><span class="sxs-lookup"><span data-stu-id="b8a3a-123">The pin is already connected.</span></span><br/>                                           |
| <dl> <span data-ttu-id="b8a3a-124"><dt>**VFW \_ E \_ não \_ parado**</dt></span><span class="sxs-lookup"><span data-stu-id="b8a3a-124"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl>        | <span data-ttu-id="b8a3a-125">O filtro está ativo e o PIN não dá suporte à reconexão dinâmica.</span><span class="sxs-lookup"><span data-stu-id="b8a3a-125">The filter is active and the pin does not support dynamic reconnection.</span></span><br/> |
| <dl> <span data-ttu-id="b8a3a-126"><dt>**\_tipo E \_ VFW \_ não \_ aceito**</dt></span><span class="sxs-lookup"><span data-stu-id="b8a3a-126"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="b8a3a-127">O tipo de mídia especificado não é aceitável.</span><span class="sxs-lookup"><span data-stu-id="b8a3a-127">The specified media type is not acceptable.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="b8a3a-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8a3a-128">Remarks</span></span>

<span data-ttu-id="b8a3a-129">O pino de saída chama esse método no pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="b8a3a-129">The output pin calls this method on the input pin.</span></span> <span data-ttu-id="b8a3a-130">Se o PIN de entrada retornar um código de erro, a conexão falhará.</span><span class="sxs-lookup"><span data-stu-id="b8a3a-130">If the input pin returns an error code, the connection fails.</span></span>

<span data-ttu-id="b8a3a-131">Na classe base, esse método executa as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="b8a3a-131">In the base class, this method performs the following steps:</span></span>

-   <span data-ttu-id="b8a3a-132">Verifica se o PIN já está conectado.</span><span class="sxs-lookup"><span data-stu-id="b8a3a-132">Checks whether the pin is already connected.</span></span>
-   <span data-ttu-id="b8a3a-133">Verifica se o filtro está parado.</span><span class="sxs-lookup"><span data-stu-id="b8a3a-133">Checks whether the filter is stopped.</span></span>
-   <span data-ttu-id="b8a3a-134">Chama o método [**CBasePin:: CheckConnect**](cbasepin-checkconnect.md) para testar se o PIN de conexão é adequado.</span><span class="sxs-lookup"><span data-stu-id="b8a3a-134">Calls the [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method to test whether the connecting pin is suitable.</span></span>
-   <span data-ttu-id="b8a3a-135">Chama o método [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) para testar se o tipo de mídia é aceitável.</span><span class="sxs-lookup"><span data-stu-id="b8a3a-135">Calls the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to test whether the media type is acceptable.</span></span>

<span data-ttu-id="b8a3a-136">Se todas essas etapas forem bem sucedidos, o método chamará os métodos [**CBasePin:: CompleteConnect**](cbasepin-completeconnect.md) e [**SetMediaType**](cbasepin-setmediatype.md) para concluir a conexão.</span><span class="sxs-lookup"><span data-stu-id="b8a3a-136">If all of these steps succeed, the method calls the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) and [**SetMediaType**](cbasepin-setmediatype.md) methods to complete the connection.</span></span> <span data-ttu-id="b8a3a-137">Esses métodos armazenam o tipo de mídia e um ponteiro para o pino de saída.</span><span class="sxs-lookup"><span data-stu-id="b8a3a-137">These methods store the media type and a pointer to the output pin.</span></span>

<span data-ttu-id="b8a3a-138">Se **CheckConnect** ou **CheckMediaType** falhar, a classe base chamará o método [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) para interromper a conexão e, em seguida, retornará um código de erro de `ReceiveConnection` .</span><span class="sxs-lookup"><span data-stu-id="b8a3a-138">If **CheckConnect** or **CheckMediaType** fail, the base class calls the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method to break the connection and then returns an error code from `ReceiveConnection`.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8a3a-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8a3a-139">Requirements</span></span>



| <span data-ttu-id="b8a3a-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8a3a-140">Requirement</span></span> | <span data-ttu-id="b8a3a-141">Valor</span><span class="sxs-lookup"><span data-stu-id="b8a3a-141">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8a3a-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b8a3a-142">Header</span></span><br/>  | <dl> <span data-ttu-id="b8a3a-143"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b8a3a-143"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b8a3a-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b8a3a-144">Library</span></span><br/> | <dl> <span data-ttu-id="b8a3a-145"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b8a3a-145"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8a3a-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8a3a-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8a3a-147">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="b8a3a-147">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




