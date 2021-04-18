---
description: O método AttemptConnection se conecta a outro PIN usando um tipo de mídia especificado.
ms.assetid: b80cf2c0-7266-4dac-8633-d30a871c57d9
title: Método CBasePin. AttemptConnection (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.AttemptConnection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72f80d81b5f105f528292a23f8b58257066b425e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751266"
---
# <a name="cbasepinattemptconnection-method"></a><span data-ttu-id="97a62-103">Método CBasePin. AttemptConnection</span><span class="sxs-lookup"><span data-stu-id="97a62-103">CBasePin.AttemptConnection method</span></span>

<span data-ttu-id="97a62-104">O `AttemptConnection` método se conecta a outro PIN usando um tipo de mídia especificado.</span><span class="sxs-lookup"><span data-stu-id="97a62-104">The `AttemptConnection` method connects to another pin using a specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="97a62-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="97a62-105">Syntax</span></span>


```C++
virtual HRESULT AttemptConnection(
         IPin       *pReceivePin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="97a62-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97a62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97a62-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="97a62-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="97a62-108">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de recebimento.</span><span class="sxs-lookup"><span data-stu-id="97a62-108">Pointer to the receiving pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="97a62-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="97a62-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="97a62-110">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que especifica o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="97a62-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97a62-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="97a62-111">Return value</span></span>

<span data-ttu-id="97a62-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="97a62-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="97a62-113">Os valores possíveis incluem os da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="97a62-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="97a62-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="97a62-114">Return code</span></span>                                                                                                | <span data-ttu-id="97a62-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="97a62-115">Description</span></span>                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="97a62-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="97a62-116"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="97a62-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="97a62-117">Success.</span></span><br/>                          |
| <dl> <span data-ttu-id="97a62-118"><dt>**\_tipo E \_ VFW \_ não \_ aceito**</dt></span><span class="sxs-lookup"><span data-stu-id="97a62-118"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="97a62-119">O tipo de mídia não é aceitável.</span><span class="sxs-lookup"><span data-stu-id="97a62-119">The media type is not acceptable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="97a62-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="97a62-120">Remarks</span></span>

<span data-ttu-id="97a62-121">Esse método tenta conectar os dois Pins com um tipo de mídia específico.</span><span class="sxs-lookup"><span data-stu-id="97a62-121">This method attempts to connect the two pins with a specific media type.</span></span> <span data-ttu-id="97a62-122">Se o tipo não for aceitável, o método falhará sem tentar outros tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="97a62-122">If the type is not acceptable, the method fails without trying other media types.</span></span>

<span data-ttu-id="97a62-123">Se o tipo de mídia for aceitável, esse método chamará o método [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) do pino de recebimento.</span><span class="sxs-lookup"><span data-stu-id="97a62-123">If the media type is acceptable, this method calls the receiving pin's [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) method.</span></span> <span data-ttu-id="97a62-124">Em seguida, ele chama o método [**CBasePin:: CompleteConnect**](cbasepin-completeconnect.md) para concluir a conexão.</span><span class="sxs-lookup"><span data-stu-id="97a62-124">Then it calls the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method to complete the connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="97a62-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97a62-125">Requirements</span></span>



| <span data-ttu-id="97a62-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="97a62-126">Requirement</span></span> | <span data-ttu-id="97a62-127">Valor</span><span class="sxs-lookup"><span data-stu-id="97a62-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97a62-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="97a62-128">Header</span></span><br/>  | <dl> <span data-ttu-id="97a62-129"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="97a62-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="97a62-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="97a62-130">Library</span></span><br/> | <dl> <span data-ttu-id="97a62-131"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="97a62-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97a62-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="97a62-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97a62-133">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="97a62-133">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




