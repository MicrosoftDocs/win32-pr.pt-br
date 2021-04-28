---
description: 'Método CTransformInputPin. Receive – o método Receive recebe o próximo exemplo de mídia no fluxo. Esse método implementa o método IMemInputPin:: Receive.'
ms.assetid: 65e4f8f5-2aa2-435b-84b4-e65af3f51afc
title: Método CTransformInputPin. Receive (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2a6a3c5dd4c9f11d45e1b719498d515a536e5ef8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084964"
---
# <a name="ctransforminputpinreceive-method"></a><span data-ttu-id="0734b-104">Método CTransformInputPin. Receive</span><span class="sxs-lookup"><span data-stu-id="0734b-104">CTransformInputPin.Receive method</span></span>

<span data-ttu-id="0734b-105">O `Receive` método recebe o próximo exemplo de mídia no fluxo.</span><span class="sxs-lookup"><span data-stu-id="0734b-105">The `Receive` method receives the next media sample in the stream.</span></span> <span data-ttu-id="0734b-106">Esse método implementa o método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .</span><span class="sxs-lookup"><span data-stu-id="0734b-106">This method implements the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0734b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0734b-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="0734b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0734b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0734b-109">*pSample*</span><span class="sxs-lookup"><span data-stu-id="0734b-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="0734b-110">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.</span><span class="sxs-lookup"><span data-stu-id="0734b-110">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0734b-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0734b-111">Return value</span></span>

<span data-ttu-id="0734b-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0734b-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0734b-113">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0734b-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="0734b-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0734b-114">Return code</span></span>                                                                             | <span data-ttu-id="0734b-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="0734b-115">Description</span></span>                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="0734b-116"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="0734b-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="0734b-117">O PIN está sendo liberado no momento; o exemplo foi rejeitado.</span><span class="sxs-lookup"><span data-stu-id="0734b-117">Pin is currently flushing; sample was rejected.</span></span><br/> |
| <dl> <span data-ttu-id="0734b-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0734b-118"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="0734b-119">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="0734b-119">Success.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="0734b-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="0734b-120">Remarks</span></span>

<span data-ttu-id="0734b-121">Esse método chama o método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) do PIN, que verifica o estado de streaming do PIN e verifica se há alterações de formato no tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="0734b-121">This method calls the pin's [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method, which checks the pin's streaming state and checks for format changes in the media type.</span></span> <span data-ttu-id="0734b-122">Em seguida, ele chama o método [**CTransformFilter:: Receive**](ctransformfilter-receive.md) do filtro, que processa o exemplo e o entrega downstream.</span><span class="sxs-lookup"><span data-stu-id="0734b-122">Then it calls the filter's [**CTransformFilter::Receive**](ctransformfilter-receive.md) method, which processes the sample and delivers it downstream.</span></span>

<span data-ttu-id="0734b-123">Se o filtro precisar acessar o exemplo depois que esse método retornar, ele deverá conter uma contagem de referência chamando o método **IUnknown:: AddRef** no exemplo.</span><span class="sxs-lookup"><span data-stu-id="0734b-123">If the filter needs to access the sample after this method returns, it should hold a reference count by calling the **IUnknown::AddRef** method on the sample.</span></span> <span data-ttu-id="0734b-124">Por exemplo, alguns filtros de decodificador precisam do exemplo atual para decodificar a próxima amostra.</span><span class="sxs-lookup"><span data-stu-id="0734b-124">For example, some decoder filters need the current sample in order to decode the next sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="0734b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0734b-125">Requirements</span></span>



| <span data-ttu-id="0734b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0734b-126">Requirement</span></span> | <span data-ttu-id="0734b-127">Valor</span><span class="sxs-lookup"><span data-stu-id="0734b-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0734b-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0734b-128">Header</span></span><br/>  | <dl> <span data-ttu-id="0734b-129"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0734b-129"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0734b-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0734b-130">Library</span></span><br/> | <dl> <span data-ttu-id="0734b-131"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0734b-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




