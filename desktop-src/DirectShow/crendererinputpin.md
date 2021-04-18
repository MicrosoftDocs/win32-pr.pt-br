---
description: A classe CBaseRendererInputPin implementa um pino de entrada para a classe CBaseRenderer. Exceto quando indicado, os métodos nesta classe delegam os métodos correspondentes na classe CBaseRenderer.
ms.assetid: da3e6aba-c2cc-4fd4-b382-fc4bc7fef774
title: Classe CRendererInputPin (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ec48b31170b2233f211e7e72de81d8792ae9160
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752488"
---
# <a name="crendererinputpin-class"></a><span data-ttu-id="10234-104">Classe CRendererInputPin</span><span class="sxs-lookup"><span data-stu-id="10234-104">CRendererInputPin class</span></span>

![hierarquia de classe crendererinput PIN](images/rbase01.png)

<span data-ttu-id="10234-106">A classe **CBaseRendererInputPin** implementa um pino de entrada para a classe [**CBaseRenderer**](cbaserenderer.md) .</span><span class="sxs-lookup"><span data-stu-id="10234-106">The **CBaseRendererInputPin** class implements an input pin for the [**CBaseRenderer**](cbaserenderer.md) class.</span></span> <span data-ttu-id="10234-107">Exceto quando indicado, os métodos nesta classe delegam os métodos correspondentes na classe **CBaseRenderer** .</span><span class="sxs-lookup"><span data-stu-id="10234-107">Except where noted, the methods in this class delegate to corresponding methods on the **CBaseRenderer** class.</span></span>



| <span data-ttu-id="10234-108">Variáveis de membro protegido</span><span class="sxs-lookup"><span data-stu-id="10234-108">Protected Member Variables</span></span>                                       | <span data-ttu-id="10234-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="10234-109">Description</span></span>                                                                            |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="10234-110">**\_pRenderer m**</span><span class="sxs-lookup"><span data-stu-id="10234-110">**m\_pRenderer**</span></span>](crendererinputpin-m-prenderer.md)            | <span data-ttu-id="10234-111">Ponteiro para o filtro.</span><span class="sxs-lookup"><span data-stu-id="10234-111">Pointer to the filter.</span></span>                                                                 |
| <span data-ttu-id="10234-112">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="10234-112">Public Methods</span></span>                                                   | <span data-ttu-id="10234-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="10234-113">Description</span></span>                                                                            |
| [<span data-ttu-id="10234-114">**CRendererInputPin**</span><span class="sxs-lookup"><span data-stu-id="10234-114">**CRendererInputPin**</span></span>](crendererinputpin-crendererinputpin.md) | <span data-ttu-id="10234-115">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="10234-115">Constructor method.</span></span>                                                                    |
| [<span data-ttu-id="10234-116">**BreakConnect**</span><span class="sxs-lookup"><span data-stu-id="10234-116">**BreakConnect**</span></span>](crendererinputpin-breakconnect.md)           | <span data-ttu-id="10234-117">Adiciona código personalizado na interrupção de uma conexão.</span><span class="sxs-lookup"><span data-stu-id="10234-117">Adds customized code upon breaking a connection.</span></span>                                       |
| [<span data-ttu-id="10234-118">**CompleteConnect**</span><span class="sxs-lookup"><span data-stu-id="10234-118">**CompleteConnect**</span></span>](crendererinputpin-completeconnect.md)     | <span data-ttu-id="10234-119">Conclui a conexão.</span><span class="sxs-lookup"><span data-stu-id="10234-119">Completes the connection.</span></span>                                                              |
| [<span data-ttu-id="10234-120">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="10234-120">**CheckMediaType**</span></span>](crendererinputpin-checkmediatype.md)       | <span data-ttu-id="10234-121">Determina se o PIN pode dar suporte a um tipo de mídia específico.</span><span class="sxs-lookup"><span data-stu-id="10234-121">Determines if the pin can support a specific media type.</span></span>                               |
| [<span data-ttu-id="10234-122">**Activo**</span><span class="sxs-lookup"><span data-stu-id="10234-122">**Active**</span></span>](crendererinputpin-active.md)                       | <span data-ttu-id="10234-123">Alterna o PIN para o modo ativo (em pausa ou em execução).</span><span class="sxs-lookup"><span data-stu-id="10234-123">Switches the pin to the active (paused or running) mode.</span></span>                               |
| [<span data-ttu-id="10234-124">**Inativo**</span><span class="sxs-lookup"><span data-stu-id="10234-124">**Inactive**</span></span>](crendererinputpin-inactive.md)                   | <span data-ttu-id="10234-125">Alterna o PIN para um estado inativo e libera a memória do alocador.</span><span class="sxs-lookup"><span data-stu-id="10234-125">Switches the pin to an inactive state and releases the memory of the allocator.</span></span>        |
| [<span data-ttu-id="10234-126">**SetMediaType**</span><span class="sxs-lookup"><span data-stu-id="10234-126">**SetMediaType**</span></span>](crendererinputpin-setmediatype.md)           | <span data-ttu-id="10234-127">Define o tipo de mídia do PIN.</span><span class="sxs-lookup"><span data-stu-id="10234-127">Sets the media type of the pin.</span></span>                                                        |
| [<span data-ttu-id="10234-128">**Alocador**</span><span class="sxs-lookup"><span data-stu-id="10234-128">**Allocator**</span></span>](crendererinputpin-allocator.md)                 | <span data-ttu-id="10234-129">Recupera um ponteiro para o alocador de memória padrão.</span><span class="sxs-lookup"><span data-stu-id="10234-129">Retrieves a pointer to the default memory allocator.</span></span>                                   |
| <span data-ttu-id="10234-130">Métodos IPin</span><span class="sxs-lookup"><span data-stu-id="10234-130">IPin Methods</span></span>                                                     | <span data-ttu-id="10234-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="10234-131">Description</span></span>                                                                            |
| [<span data-ttu-id="10234-132">**QueryId**</span><span class="sxs-lookup"><span data-stu-id="10234-132">**QueryId**</span></span>](crendererinputpin-queryid.md)                     | <span data-ttu-id="10234-133">Recupera um identificador para o PIN.</span><span class="sxs-lookup"><span data-stu-id="10234-133">Retrieves an identifier for the pin.</span></span>                                                   |
| [<span data-ttu-id="10234-134">**EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="10234-134">**EndOfStream**</span></span>](crendererinputpin-endofstream.md)             | <span data-ttu-id="10234-135">Informa ao PIN que nenhum dado adicional é esperado até que um novo comando de execução seja emitido.</span><span class="sxs-lookup"><span data-stu-id="10234-135">Informs the pin that no additional data is expected until a new run command is issued.</span></span> |
| [<span data-ttu-id="10234-136">**BeginFlush**</span><span class="sxs-lookup"><span data-stu-id="10234-136">**BeginFlush**</span></span>](crendererinputpin-beginflush.md)               | <span data-ttu-id="10234-137">Informa o PIN para iniciar uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="10234-137">Informs the pin to begin a flush operation.</span></span>                                            |
| [<span data-ttu-id="10234-138">**EndFlush**</span><span class="sxs-lookup"><span data-stu-id="10234-138">**EndFlush**</span></span>](crendererinputpin-endflush.md)                   | <span data-ttu-id="10234-139">Informa o PIN para finalizar uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="10234-139">Informs the pin to end a flush operation.</span></span>                                              |
| <span data-ttu-id="10234-140">Métodos IMemInputPin</span><span class="sxs-lookup"><span data-stu-id="10234-140">IMemInputPin Methods</span></span>                                             | <span data-ttu-id="10234-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="10234-141">Description</span></span>                                                                            |
| [<span data-ttu-id="10234-142">**Recebe**</span><span class="sxs-lookup"><span data-stu-id="10234-142">**Receive**</span></span>](crendererinputpin-receive.md)                     | <span data-ttu-id="10234-143">Recupera o próximo bloco de dados do fluxo.</span><span class="sxs-lookup"><span data-stu-id="10234-143">Retrieves the next block of data from the stream.</span></span>                                      |



 

## <a name="requirements"></a><span data-ttu-id="10234-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10234-144">Requirements</span></span>



| <span data-ttu-id="10234-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="10234-145">Requirement</span></span> | <span data-ttu-id="10234-146">Valor</span><span class="sxs-lookup"><span data-stu-id="10234-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10234-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="10234-147">Header</span></span><br/>  | <dl> <span data-ttu-id="10234-148"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="10234-148"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="10234-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="10234-149">Library</span></span><br/> | <dl> <span data-ttu-id="10234-150"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="10234-150"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




