---
description: A classe CBaseMediaFilter implementa a interface IMediaFilter.
ms.assetid: 45c8973b-d0b3-4aeb-96e7-be47f8d7f4a7
title: Classe CBaseMediaFilter (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e594fd941fffecc836af26bd3d70cced82ddcaa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756644"
---
# <a name="cbasemediafilter-class"></a><span data-ttu-id="e3931-103">Classe CBaseMediaFilter</span><span class="sxs-lookup"><span data-stu-id="e3931-103">CBaseMediaFilter class</span></span>

![cbasemediafilter](images/filter05.png)

<span data-ttu-id="e3931-105">A `CBaseMediaFilter` classe implementa a interface [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) .</span><span class="sxs-lookup"><span data-stu-id="e3931-105">The `CBaseMediaFilter` class implements the [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) interface.</span></span> <span data-ttu-id="e3931-106">Use essa classe para distribuidores de plug-in ou outros objetos que precisam dar suporte a **IMediaFilter** sem dar suporte à interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .</span><span class="sxs-lookup"><span data-stu-id="e3931-106">Use this class for plug-in distributors or other objects that need to support **IMediaFilter** without supporting the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="e3931-107">Não use essa classe para filtros.</span><span class="sxs-lookup"><span data-stu-id="e3931-107">Do not use this class for filters.</span></span> <span data-ttu-id="e3931-108">Em vez disso, use a classe [**CBaseFilter**](cbasefilter.md) ou uma classe base derivada de **CBaseFilter**.</span><span class="sxs-lookup"><span data-stu-id="e3931-108">Instead, use the [**CBaseFilter**](cbasefilter.md) class, or a base class derived from **CBaseFilter**.</span></span>



| <span data-ttu-id="e3931-109">Variáveis de membro protegido</span><span class="sxs-lookup"><span data-stu-id="e3931-109">Protected Member Variables</span></span>                                       | <span data-ttu-id="e3931-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3931-110">Description</span></span>                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="e3931-111">**\_estado m**</span><span class="sxs-lookup"><span data-stu-id="e3931-111">**m\_State**</span></span>](cbasemediafilter-m-state.md)                     | <span data-ttu-id="e3931-112">Estado atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="e3931-112">Current state of the object.</span></span>                                 |
| [<span data-ttu-id="e3931-113">**\_pClock m**</span><span class="sxs-lookup"><span data-stu-id="e3931-113">**m\_pClock**</span></span>](cbasemediafilter-m-pclock.md)                   | <span data-ttu-id="e3931-114">Ponteiro para o relógio de referência do objeto.</span><span class="sxs-lookup"><span data-stu-id="e3931-114">Pointer to the object's reference clock.</span></span>                     |
| [<span data-ttu-id="e3931-115">**\_tStart m**</span><span class="sxs-lookup"><span data-stu-id="e3931-115">**m\_tStart**</span></span>](cbasemediafilter-m-tstart.md)                   | <span data-ttu-id="e3931-116">Tempo de referência que corresponde ao tempo de fluxo 0.</span><span class="sxs-lookup"><span data-stu-id="e3931-116">Reference time that corresponds to stream time 0.</span></span>            |
| [<span data-ttu-id="e3931-117">**CLSID do m \_**</span><span class="sxs-lookup"><span data-stu-id="e3931-117">**m\_clsid**</span></span>](cbasemediafilter-m-clsid.md)                     | <span data-ttu-id="e3931-118">Identificador de classe (CLSID) do objeto.</span><span class="sxs-lookup"><span data-stu-id="e3931-118">Class identifier (CLSID) of the object.</span></span>                      |
| [<span data-ttu-id="e3931-119">**\_pLock m**</span><span class="sxs-lookup"><span data-stu-id="e3931-119">**m\_pLock**</span></span>](cbasemediafilter-m-plock.md)                     | <span data-ttu-id="e3931-120">Ponteiro para uma seção crítica.</span><span class="sxs-lookup"><span data-stu-id="e3931-120">Pointer to a critical section.</span></span>                               |
| <span data-ttu-id="e3931-121">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="e3931-121">Public Methods</span></span>                                                   | <span data-ttu-id="e3931-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3931-122">Description</span></span>                                                  |
| [<span data-ttu-id="e3931-123">**CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="e3931-123">**CBaseMediaFilter**</span></span>](cbasemediafilter-cbasemediafilter.md)    | <span data-ttu-id="e3931-124">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="e3931-124">Constructor method.</span></span>                                          |
| [<span data-ttu-id="e3931-125">**~ CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="e3931-125">**~ CBaseMediaFilter**</span></span>](cbasemediafilter--cbasemediafilter.md) | <span data-ttu-id="e3931-126">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="e3931-126">Destructor method.</span></span> <span data-ttu-id="e3931-127">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="e3931-127">Virtual.</span></span>                                  |
| [<span data-ttu-id="e3931-128">**Fluxo de transmissão**</span><span class="sxs-lookup"><span data-stu-id="e3931-128">**StreamTime**</span></span>](cbasemediafilter-streamtime.md)                | <span data-ttu-id="e3931-129">Recupera a hora atual do fluxo.</span><span class="sxs-lookup"><span data-stu-id="e3931-129">Retrieves the current stream time.</span></span> <span data-ttu-id="e3931-130">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="e3931-130">Virtual.</span></span>                  |
| [<span data-ttu-id="e3931-131">**IsActive**</span><span class="sxs-lookup"><span data-stu-id="e3931-131">**IsActive**</span></span>](cbasemediafilter-isactive.md)                    | <span data-ttu-id="e3931-132">Determina se o objeto está ativo (em execução ou em pausa).</span><span class="sxs-lookup"><span data-stu-id="e3931-132">Determines whether the object is active (running or paused).</span></span> |
| <span data-ttu-id="e3931-133">Métodos IPersist</span><span class="sxs-lookup"><span data-stu-id="e3931-133">IPersist Methods</span></span>                                                 | <span data-ttu-id="e3931-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3931-134">Description</span></span>                                                  |
| [<span data-ttu-id="e3931-135">**GetClassID**</span><span class="sxs-lookup"><span data-stu-id="e3931-135">**GetClassID**</span></span>](cbasemediafilter-getclassid.md)                | <span data-ttu-id="e3931-136">Recupera o identificador de classe.</span><span class="sxs-lookup"><span data-stu-id="e3931-136">Retrieves the class identifier.</span></span>                              |
| <span data-ttu-id="e3931-137">Métodos IMediaFilter</span><span class="sxs-lookup"><span data-stu-id="e3931-137">IMediaFilter Methods</span></span>                                             | <span data-ttu-id="e3931-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3931-138">Description</span></span>                                                  |
| [<span data-ttu-id="e3931-139">**GetState**</span><span class="sxs-lookup"><span data-stu-id="e3931-139">**GetState**</span></span>](cbasemediafilter-getstate.md)                    | <span data-ttu-id="e3931-140">Recupera o estado do objeto (em execução, parado ou pausado).</span><span class="sxs-lookup"><span data-stu-id="e3931-140">Retrieves the object's state (running, stopped, or paused).</span></span>  |
| [<span data-ttu-id="e3931-141">**Setsynce**</span><span class="sxs-lookup"><span data-stu-id="e3931-141">**SetSyncSource**</span></span>](cbasemediafilter-setsyncsource.md)          | <span data-ttu-id="e3931-142">Define um relógio de referência para o objeto.</span><span class="sxs-lookup"><span data-stu-id="e3931-142">Sets a reference clock for the object.</span></span>                       |
| [<span data-ttu-id="e3931-143">**Getsync**</span><span class="sxs-lookup"><span data-stu-id="e3931-143">**GetSyncSource**</span></span>](cbasemediafilter-getsyncsource.md)          | <span data-ttu-id="e3931-144">Recupera o relógio de referência que o objeto está usando.</span><span class="sxs-lookup"><span data-stu-id="e3931-144">Retrieves the reference clock that the object is using.</span></span>      |
| [<span data-ttu-id="e3931-145">**Stop**</span><span class="sxs-lookup"><span data-stu-id="e3931-145">**Stop**</span></span>](cbasemediafilter-stop.md)                            | <span data-ttu-id="e3931-146">Interrompe o objeto.</span><span class="sxs-lookup"><span data-stu-id="e3931-146">Stops the object.</span></span>                                            |
| [<span data-ttu-id="e3931-147">**Pausar**</span><span class="sxs-lookup"><span data-stu-id="e3931-147">**Pause**</span></span>](cbasemediafilter-pause.md)                          | <span data-ttu-id="e3931-148">Pausa o objeto.</span><span class="sxs-lookup"><span data-stu-id="e3931-148">Pauses the object.</span></span>                                           |
| [<span data-ttu-id="e3931-149">**Executar**</span><span class="sxs-lookup"><span data-stu-id="e3931-149">**Run**</span></span>](cbasemediafilter-run.md)                              | <span data-ttu-id="e3931-150">Executa o objeto.</span><span class="sxs-lookup"><span data-stu-id="e3931-150">Runs the object.</span></span>                                             |



 

## <a name="requirements"></a><span data-ttu-id="e3931-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3931-151">Requirements</span></span>



| <span data-ttu-id="e3931-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3931-152">Requirement</span></span> | <span data-ttu-id="e3931-153">Valor</span><span class="sxs-lookup"><span data-stu-id="e3931-153">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3931-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e3931-154">Header</span></span><br/>  | <dl> <span data-ttu-id="e3931-155"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e3931-155"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e3931-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e3931-156">Library</span></span><br/> | <dl> <span data-ttu-id="e3931-157"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e3931-157"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




