---
description: Método CTransInPlaceFilter. CompleteConnect – o método CompleteConnect conclui uma conexão de PIN.
ms.assetid: 0c02c455-dbd0-4606-b1b1-f965c2a5805b
title: Método CTransInPlaceFilter. CompleteConnect (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d9cc0bc839a4e35c4ce896acdf50da10f0c2bb0c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084784"
---
# <a name="ctransinplacefiltercompleteconnect-method"></a><span data-ttu-id="e1a19-103">Método CTransInPlaceFilter. CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="e1a19-103">CTransInPlaceFilter.CompleteConnect method</span></span>

<span data-ttu-id="e1a19-104">O `CompleteConnect` método conclui uma conexão de PIN.</span><span class="sxs-lookup"><span data-stu-id="e1a19-104">The `CompleteConnect` method completes a pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1a19-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e1a19-105">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="e1a19-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1a19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1a19-107">*direction*</span><span class="sxs-lookup"><span data-stu-id="e1a19-107">*direction*</span></span> 
</dt> <dd>

<span data-ttu-id="e1a19-108">Membro do tipo enumerado de [**\_ direção do PIN**](/windows/win32/api/strmif/ne-strmif-pin_direction) , especificando qual Pin no filtro está fazendo a conexão.</span><span class="sxs-lookup"><span data-stu-id="e1a19-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="e1a19-109">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="e1a19-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="e1a19-110">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do outro PIN nesta tentativa de conexão.</span><span class="sxs-lookup"><span data-stu-id="e1a19-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1a19-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e1a19-111">Return value</span></span>

<span data-ttu-id="e1a19-112">Retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e1a19-112">Returns an **HRESULT**.</span></span> <span data-ttu-id="e1a19-113">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e1a19-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="e1a19-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e1a19-114">Return code</span></span>                                                                                           | <span data-ttu-id="e1a19-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1a19-115">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="e1a19-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e1a19-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="e1a19-117">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="e1a19-117">Success.</span></span><br/>                             |
| <dl> <span data-ttu-id="e1a19-118"><dt>**VFW \_ E \_ não \_ no \_ grafo**</dt></span><span class="sxs-lookup"><span data-stu-id="e1a19-118"><dt>**VFW\_E\_NOT\_IN\_GRAPH**</dt></span></span> </dl> | <span data-ttu-id="e1a19-119">O filtro não está em um grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="e1a19-119">The filter is not in a filter graph.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e1a19-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1a19-120">Remarks</span></span>

<span data-ttu-id="e1a19-121">Esse método substitui o método [**CTransformFilter:: CompleteConnect**](ctransformfilter-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="e1a19-121">This method overrides the [**CTransformFilter::CompleteConnect**](ctransformfilter-completeconnect.md) method.</span></span>

<span data-ttu-id="e1a19-122">O comportamento do filtro depende da ordem das conexões do PIN:</span><span class="sxs-lookup"><span data-stu-id="e1a19-122">The behavior of the filter depends on the order of the pin connections:</span></span>

-   <span data-ttu-id="e1a19-123">Se o PIN de entrada for conectado primeiro, a conexão usará um alocador temporário.</span><span class="sxs-lookup"><span data-stu-id="e1a19-123">If the input pin is connected first, the connection uses a temporary allocator.</span></span> <span data-ttu-id="e1a19-124">Quando o pino de saída é conectado, o filtro reconecta o PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="e1a19-124">When the output pin is connected, the filter reconnects the input pin.</span></span> <span data-ttu-id="e1a19-125">Reconectar o PIN de entrada faz com que o filtro upstream renegocie o alocador.</span><span class="sxs-lookup"><span data-stu-id="e1a19-125">Reconnecting the input pin causes the upstream filter to renegotiate the allocator.</span></span> <span data-ttu-id="e1a19-126">Nesse ponto, o PIN de entrada propõe um alocador do filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="e1a19-126">At that point, the input pin proposes an allocator from the downstream filter.</span></span> <span data-ttu-id="e1a19-127">Para obter mais informações, consulte [**CTransInPlaceInputPin:: Getalocador**](ctransinplaceinputpin-getallocator.md).</span><span class="sxs-lookup"><span data-stu-id="e1a19-127">For more information, see [**CTransInPlaceInputPin::GetAllocator**](ctransinplaceinputpin-getallocator.md).</span></span>
-   <span data-ttu-id="e1a19-128">Se o pino de saída for conectado primeiro, o pino de saída não selecionará um alocador.</span><span class="sxs-lookup"><span data-stu-id="e1a19-128">If the output pin is connected first, the output pin does not select an allocator.</span></span> <span data-ttu-id="e1a19-129">Quando o pino de entrada é conectado, ele negocia um alocador para ambas as conexões.</span><span class="sxs-lookup"><span data-stu-id="e1a19-129">When the input pin is connected, it negotiates an allocator for both connections.</span></span> <span data-ttu-id="e1a19-130">Se os tipos de mídia de entrada e saída não forem iguais, o filtro reconectará o pino de saída usando o tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="e1a19-130">If the input and output media types are not the same, the filter reconnects the output pin using the input type.</span></span>

<span data-ttu-id="e1a19-131">O filtro executa todas as reconexões de PIN chamando o método [**CBaseFilter:: ReconnectPin**](cbasefilter-reconnectpin.md) .</span><span class="sxs-lookup"><span data-stu-id="e1a19-131">The filter performs all pin reconnections by calling the [**CBaseFilter::ReconnectPin**](cbasefilter-reconnectpin.md) method.</span></span> <span data-ttu-id="e1a19-132">O método **ReconnectPin** , por sua vez, chama o método [**IFilterGraph2:: ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) no Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="e1a19-132">The **ReconnectPin** method, in turn, calls the [**IFilterGraph2::ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) method on the filter graph manager.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1a19-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1a19-133">Requirements</span></span>



| <span data-ttu-id="e1a19-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1a19-134">Requirement</span></span> | <span data-ttu-id="e1a19-135">Valor</span><span class="sxs-lookup"><span data-stu-id="e1a19-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1a19-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e1a19-136">Header</span></span><br/>  | <dl> <span data-ttu-id="e1a19-137"><dt>TRANSip. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e1a19-137"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e1a19-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e1a19-138">Library</span></span><br/> | <dl> <span data-ttu-id="e1a19-139"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e1a19-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1a19-140">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e1a19-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1a19-141">**Classe CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="e1a19-141">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




