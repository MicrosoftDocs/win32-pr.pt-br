---
description: 'O método ReceiveCanBlock determina se as chamadas para o método IMemInputPin:: Receive podem ser bloqueadas. Esse método implementa o método IMemInputPin:: ReceiveCanBlock.'
ms.assetid: db96e389-e1bc-4b38-8d0a-a20f0d3a4460
title: Método CBaseInputPin. ReceiveCanBlock (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.ReceiveCanBlock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93c80d6c8f834b45381b89e80d2e0acc392bf25a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751272"
---
# <a name="cbaseinputpinreceivecanblock-method"></a><span data-ttu-id="d8877-104">Método CBaseInputPin. ReceiveCanBlock</span><span class="sxs-lookup"><span data-stu-id="d8877-104">CBaseInputPin.ReceiveCanBlock method</span></span>

<span data-ttu-id="d8877-105">O `ReceiveCanBlock` método determina se as chamadas para o método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) podem ser bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="d8877-105">The `ReceiveCanBlock` method determines whether calls to the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method might block.</span></span> <span data-ttu-id="d8877-106">Esse método implementa o método [**IMemInputPin:: ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) .</span><span class="sxs-lookup"><span data-stu-id="d8877-106">This method implements the [**IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8877-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8877-107">Syntax</span></span>


```C++
HRESULT ReceiveCanBlock();
```



## <a name="parameters"></a><span data-ttu-id="d8877-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8877-108">Parameters</span></span>

<span data-ttu-id="d8877-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d8877-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d8877-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d8877-110">Return value</span></span>

<span data-ttu-id="d8877-111">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d8877-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d8877-112">O valor possível incluem os listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d8877-112">Possible value include those listed in the following table.</span></span>



| <span data-ttu-id="d8877-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d8877-113">Return code</span></span>                                                                             | <span data-ttu-id="d8877-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="d8877-114">Description</span></span>                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="d8877-115"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="d8877-115"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="d8877-116">O PIN não será bloqueado em uma chamada para **Receive**.</span><span class="sxs-lookup"><span data-stu-id="d8877-116">The pin will not block on a call to **Receive**.</span></span><br/> |
| <dl> <span data-ttu-id="d8877-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d8877-117"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="d8877-118">O PIN pode ser bloqueado em uma chamada para **Receive**.</span><span class="sxs-lookup"><span data-stu-id="d8877-118">The pin might block on a call to **Receive**.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="d8877-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8877-119">Remarks</span></span>

<span data-ttu-id="d8877-120">Retorna S \_ false se as chamadas para o método **Receive** estiverem garantidas por não bloquear.</span><span class="sxs-lookup"><span data-stu-id="d8877-120">Return S\_FALSE if calls to the **Receive** method are guaranteed not to block.</span></span> <span data-ttu-id="d8877-121">Caso contrário, retorne S \_ OK ou um código de erro.</span><span class="sxs-lookup"><span data-stu-id="d8877-121">Otherwise, return S\_OK or an error code.</span></span> <span data-ttu-id="d8877-122">Se o método **Receive** chamar **Receive** em um PIN downstream, o PIN downstream poderá ser bloqueado; `ReceiveCanBlock` deve levar esse fator em conta.</span><span class="sxs-lookup"><span data-stu-id="d8877-122">If the **Receive** method calls **Receive** on a downstream pin, the downstream pin might block; `ReceiveCanBlock` must take that factor into account.</span></span>

<span data-ttu-id="d8877-123">Um filtro upstream pode usar esse método para determinar sua estratégia de Threading.</span><span class="sxs-lookup"><span data-stu-id="d8877-123">An upstream filter can use this method to determine its threading strategy.</span></span> <span data-ttu-id="d8877-124">Se o método **Receive** puder ser bloqueado, o filtro upstream poderá decidir usar um thread de trabalho que armazena os dados em buffer.</span><span class="sxs-lookup"><span data-stu-id="d8877-124">If the **Receive** method might block, the upstream filter might decide to use a worker thread that buffers data.</span></span> <span data-ttu-id="d8877-125">Consulte a classe [**COutputQueue**](coutputqueue.md) para uma implementação dessa estratégia.</span><span class="sxs-lookup"><span data-stu-id="d8877-125">See the [**COutputQueue**](coutputqueue.md) class for an implementation of this strategy.</span></span>

<span data-ttu-id="d8877-126">Na classe base, esse método retorna S \_ OK quando qualquer uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="d8877-126">In the base class, this method returns S\_OK when any of the following are true:</span></span>

-   <span data-ttu-id="d8877-127">O filtro não tem nenhum pino de saída.</span><span class="sxs-lookup"><span data-stu-id="d8877-127">The filter has no output pins.</span></span>
-   <span data-ttu-id="d8877-128">Um PIN de entrada conectado a esse filtro sinaliza que ele pode bloquear.</span><span class="sxs-lookup"><span data-stu-id="d8877-128">An input pin connected to this filter signals that it might block.</span></span>
-   <span data-ttu-id="d8877-129">Um PIN de entrada conectado a este filtro não oferece suporte à interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="d8877-129">An input pin connected to this filter does not support the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8877-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8877-130">Requirements</span></span>



| <span data-ttu-id="d8877-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8877-131">Requirement</span></span> | <span data-ttu-id="d8877-132">Valor</span><span class="sxs-lookup"><span data-stu-id="d8877-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8877-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d8877-133">Header</span></span><br/>  | <dl> <span data-ttu-id="d8877-134"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8877-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d8877-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d8877-135">Library</span></span><br/> | <dl> <span data-ttu-id="d8877-136"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d8877-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8877-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8877-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8877-138">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="d8877-138">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




