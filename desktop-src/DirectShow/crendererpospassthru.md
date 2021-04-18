---
description: A classe CRendererPosPassThru manipula comandos de busca para filtros de processador, passando-os upstream para o próximo filtro.
ms.assetid: 7b532177-939c-4cb7-a6fa-c0133f65c768
title: Classe CRendererPosPassThru (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7154dde8adefdb3292107e9c33d7b6a2b54f6af0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757020"
---
# <a name="crendererpospassthru-class"></a><span data-ttu-id="8d91e-103">Classe CRendererPosPassThru</span><span class="sxs-lookup"><span data-stu-id="8d91e-103">CRendererPosPassThru class</span></span>

![hierarquia de classe CRendererPosPassThru](images/cutil14.png)

<span data-ttu-id="8d91e-105">A `CRendererPosPassThru` classe lida com os comandos de busca para filtros de processador, passando-os upstream para o próximo filtro.</span><span class="sxs-lookup"><span data-stu-id="8d91e-105">The `CRendererPosPassThru` class handles seek commands for renderer filters, by passing them upstream to the next filter.</span></span>

<span data-ttu-id="8d91e-106">Essa classe deriva da classe [**CPosPassThru**](cpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="8d91e-106">This class derives from the [**CPosPassThru**](cpospassthru.md) class.</span></span> <span data-ttu-id="8d91e-107">Ele adiciona suporte para armazenar em cache os carimbos de data/hora de exemplos à medida que eles chegam.</span><span class="sxs-lookup"><span data-stu-id="8d91e-107">It adds support for caching the time stamps from samples as they arrive.</span></span> <span data-ttu-id="8d91e-108">Use essa classe da mesma maneira que a classe **CPosPassThru** .</span><span class="sxs-lookup"><span data-stu-id="8d91e-108">Use this class in the same way as the **CPosPassThru** class.</span></span> <span data-ttu-id="8d91e-109">Consulte a documentação do **CPosPassThru** para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="8d91e-109">Refer to the **CPosPassThru** documentation for details.</span></span>

<span data-ttu-id="8d91e-110">O filtro de renderizador deve atualizar os `CRendererPosPassThru` carimbos de data/hora em cache do objeto, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="8d91e-110">The renderer filter must update the `CRendererPosPassThru` object's cached time stamps, as follows:</span></span>

-   <span data-ttu-id="8d91e-111">Para cada exemplo que o filtro recebe, chame o método [**CRendererPosPassThru:: RegisterMediaTime**](crendererpospassthru-registermediatime.md) .</span><span class="sxs-lookup"><span data-stu-id="8d91e-111">For each sample the filter receives, call the [**CRendererPosPassThru::RegisterMediaTime**](crendererpospassthru-registermediatime.md) method.</span></span>
-   <span data-ttu-id="8d91e-112">Quando o filtro é interrompido ou recebe uma chamada **EndFlush** , chame o método [**CRendererPosPassThru:: ResetMediaTime**](crendererpospassthru-resetmediatime.md) .</span><span class="sxs-lookup"><span data-stu-id="8d91e-112">When the filter is stopped or receives an **EndFlush** call, call the [**CRendererPosPassThru::ResetMediaTime**](crendererpospassthru-resetmediatime.md) method.</span></span>
-   <span data-ttu-id="8d91e-113">Quando o filtro recebe uma notificação de fim de fluxo, chame o método [**CRendererPosPassThru:: EOS**](crendererpospassthru-eos.md) .</span><span class="sxs-lookup"><span data-stu-id="8d91e-113">When the filter receives an end-of-stream notification, call the [**CRendererPosPassThru::EOS**](crendererpospassthru-eos.md) method.</span></span>

<span data-ttu-id="8d91e-114">Para obter um exemplo de como usar essa classe, consulte o código-fonte [**CBaseRenderer**](cbaserenderer.md) .</span><span class="sxs-lookup"><span data-stu-id="8d91e-114">For an example of how to use this class, refer to the [**CBaseRenderer**](cbaserenderer.md) source code.</span></span>



| <span data-ttu-id="8d91e-115">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="8d91e-115">Public Methods</span></span>                                                            | <span data-ttu-id="8d91e-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="8d91e-116">Description</span></span>                                                         |
|---------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="8d91e-117">**CRendererPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="8d91e-117">**CRendererPosPassThru**</span></span>](crendererpospassthru-crendererpospassthru.md) | <span data-ttu-id="8d91e-118">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="8d91e-118">Constructor method.</span></span>                                                 |
| [<span data-ttu-id="8d91e-119">**GetMediaTime**</span><span class="sxs-lookup"><span data-stu-id="8d91e-119">**GetMediaTime**</span></span>](crendererpospassthru-getmediatime.md)                 | <span data-ttu-id="8d91e-120">Recupera os carimbos de data/hora no exemplo atual.</span><span class="sxs-lookup"><span data-stu-id="8d91e-120">Retrieves the time stamps on the current sample.</span></span>                    |
| [<span data-ttu-id="8d91e-121">**RegisterMediaTime**</span><span class="sxs-lookup"><span data-stu-id="8d91e-121">**RegisterMediaTime**</span></span>](crendererpospassthru-registermediatime.md)       | <span data-ttu-id="8d91e-122">Armazena em cache os carimbos de data/hora do exemplo atual.</span><span class="sxs-lookup"><span data-stu-id="8d91e-122">Caches the time stamps from the current sample.</span></span>                     |
| [<span data-ttu-id="8d91e-123">**ResetMediaTime**</span><span class="sxs-lookup"><span data-stu-id="8d91e-123">**ResetMediaTime**</span></span>](crendererpospassthru-resetmediatime.md)             | <span data-ttu-id="8d91e-124">Redefine os carimbos de data/hora em cache como zero.</span><span class="sxs-lookup"><span data-stu-id="8d91e-124">Resets the cached time stamps to zero.</span></span>                              |
| [<span data-ttu-id="8d91e-125">**Electric**</span><span class="sxs-lookup"><span data-stu-id="8d91e-125">**EOS**</span></span>](crendererpospassthru-eos.md)                                   | <span data-ttu-id="8d91e-126">Atualiza os carimbos de data/hora em cache após uma notificação de fim de fluxo.</span><span class="sxs-lookup"><span data-stu-id="8d91e-126">Updates the cached time stamps after an end-of-stream notification.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="8d91e-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d91e-127">Requirements</span></span>



| <span data-ttu-id="8d91e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d91e-128">Requirement</span></span> | <span data-ttu-id="8d91e-129">Valor</span><span class="sxs-lookup"><span data-stu-id="8d91e-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d91e-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8d91e-130">Header</span></span><br/>  | <dl> <span data-ttu-id="8d91e-131"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8d91e-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8d91e-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8d91e-132">Library</span></span><br/> | <dl> <span data-ttu-id="8d91e-133"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="8d91e-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




