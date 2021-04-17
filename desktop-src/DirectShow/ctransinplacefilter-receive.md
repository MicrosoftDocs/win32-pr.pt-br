---
description: O método Receive recebe um exemplo de mídia, processa-o e o entrega para o filtro downstream.
ms.assetid: 87126353-b73a-45f5-a8e7-b719efdf9d76
title: Método CTransInPlaceFilter. Receive (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e7a1f87617b59c31139cb3d857c83d4470fd709
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748012"
---
# <a name="ctransinplacefilterreceive-method"></a><span data-ttu-id="1d7bf-103">Método CTransInPlaceFilter. Receive</span><span class="sxs-lookup"><span data-stu-id="1d7bf-103">CTransInPlaceFilter.Receive method</span></span>

<span data-ttu-id="1d7bf-104">O `Receive` método recebe um exemplo de mídia, processa-o e o entrega para o filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="1d7bf-104">The `Receive` method receives a media sample, processes it, and delivers it to the downstream filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d7bf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d7bf-105">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="1d7bf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1d7bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d7bf-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="1d7bf-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="1d7bf-108">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) no exemplo.</span><span class="sxs-lookup"><span data-stu-id="1d7bf-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface on the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d7bf-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1d7bf-109">Return value</span></span>

<span data-ttu-id="1d7bf-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1d7bf-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1d7bf-111">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1d7bf-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="1d7bf-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1d7bf-112">Return code</span></span>                                                                                  | <span data-ttu-id="1d7bf-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="1d7bf-113">Description</span></span>                 |
|----------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <span data-ttu-id="1d7bf-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1d7bf-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="1d7bf-115">Sucesso</span><span class="sxs-lookup"><span data-stu-id="1d7bf-115">Success</span></span><br/>          |
| <dl> <span data-ttu-id="1d7bf-116"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="1d7bf-116"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="1d7bf-117">Erro inesperado</span><span class="sxs-lookup"><span data-stu-id="1d7bf-117">Unexpected error</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1d7bf-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d7bf-118">Remarks</span></span>

<span data-ttu-id="1d7bf-119">O pino de entrada do filtro chama esse método quando recebe um exemplo.</span><span class="sxs-lookup"><span data-stu-id="1d7bf-119">The filter's input pin calls this method when it receives a sample.</span></span> <span data-ttu-id="1d7bf-120">O filtro chama o método [**Transform**](ctransinplacefilter-transform.md) , que a classe derivada deve implementar.</span><span class="sxs-lookup"><span data-stu-id="1d7bf-120">The filter calls the [**Transform**](ctransinplacefilter-transform.md) method, which the derived class must implement.</span></span> <span data-ttu-id="1d7bf-121">O método **Transform** processa os dados.</span><span class="sxs-lookup"><span data-stu-id="1d7bf-121">The **Transform** method processes the data.</span></span> <span data-ttu-id="1d7bf-122">Se o filtro estiver usando apenas um alocador, ele passará *pSample* diretamente para o método **Transform** .</span><span class="sxs-lookup"><span data-stu-id="1d7bf-122">If the filter is using only one allocator, it passes *pSample* directly to the **Transform** method.</span></span> <span data-ttu-id="1d7bf-123">Caso contrário, ele copiará *pSample* e passará a cópia.</span><span class="sxs-lookup"><span data-stu-id="1d7bf-123">Otherwise, it copies *pSample* and passes the copy.</span></span>

<span data-ttu-id="1d7bf-124">Se o método **Transform** retornar S \_ false, o `Receive` método descartará o exemplo.</span><span class="sxs-lookup"><span data-stu-id="1d7bf-124">If the **Transform** method returns S\_FALSE, the `Receive` method drops the sample.</span></span> <span data-ttu-id="1d7bf-125">Na primeira amostra descartada, o filtro envia um evento de [**\_ \_ alteração de qualidade do EC**](ec-quality-change.md) para o Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="1d7bf-125">On the first dropped sample, the filter sends an [**EC\_QUALITY\_CHANGE**](ec-quality-change.md) event to the filter graph manager.</span></span> <span data-ttu-id="1d7bf-126">Caso contrário, se o método **Transform** retornar S \_ OK, o filtro entregará o exemplo de saída.</span><span class="sxs-lookup"><span data-stu-id="1d7bf-126">Otherwise, if the **Transform** method returns S\_OK, the filter delivers the output sample.</span></span> <span data-ttu-id="1d7bf-127">Para fazer isso, ele chama o método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) no pino de entrada downstream.</span><span class="sxs-lookup"><span data-stu-id="1d7bf-127">To do so, it calls the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d7bf-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d7bf-128">Requirements</span></span>



| <span data-ttu-id="1d7bf-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d7bf-129">Requirement</span></span> | <span data-ttu-id="1d7bf-130">Valor</span><span class="sxs-lookup"><span data-stu-id="1d7bf-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d7bf-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1d7bf-131">Header</span></span><br/>  | <dl> <span data-ttu-id="1d7bf-132"><dt>TRANSip. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d7bf-132"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1d7bf-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1d7bf-133">Library</span></span><br/> | <dl> <span data-ttu-id="1d7bf-134"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="1d7bf-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d7bf-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d7bf-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d7bf-136">**Classe CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="1d7bf-136">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




