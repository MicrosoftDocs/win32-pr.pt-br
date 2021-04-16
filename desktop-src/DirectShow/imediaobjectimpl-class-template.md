---
description: O modelo de classe IMediaObjectImpl fornece uma implementação base para a interface IMediaObject. Para obter mais informações sobre como usar esse modelo, consulte usando o modelo de classe DMO.
ms.assetid: 81d45b8d-8373-4e42-b768-f6126feb935d
title: Modelo de classe IMediaObjectImpl (Dmoimpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ecfa1be82ffeaa9e05eb6460249e0c40bb2989c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759497"
---
# <a name="imediaobjectimpl-class-template"></a><span data-ttu-id="bbf4b-104">Modelo de classe IMediaObjectImpl</span><span class="sxs-lookup"><span data-stu-id="bbf4b-104">IMediaObjectImpl Class Template</span></span>

<span data-ttu-id="bbf4b-105">O `IMediaObjectImpl` modelo de classe fornece uma implementação base para a interface [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) .</span><span class="sxs-lookup"><span data-stu-id="bbf4b-105">The `IMediaObjectImpl` class template provides a base implementation for the [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) interface.</span></span> <span data-ttu-id="bbf4b-106">Para obter mais informações sobre como usar esse modelo, consulte [usando o modelo de classe DMO](using-the-dmo-class-template.md).</span><span class="sxs-lookup"><span data-stu-id="bbf4b-106">For more information on using this template, see [Using the DMO Class Template](using-the-dmo-class-template.md).</span></span>

<span data-ttu-id="bbf4b-107">Este `IMediaObjectImpl` modelo expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="bbf4b-107">This `IMediaObjectImpl` template exposes the following members.</span></span>



| <span data-ttu-id="bbf4b-108">Classe aninhada</span><span class="sxs-lookup"><span data-stu-id="bbf4b-108">Nested Class</span></span>                              | <span data-ttu-id="bbf4b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="bbf4b-109">Description</span></span>                                  |
|-------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="bbf4b-110">**LockIt**</span><span class="sxs-lookup"><span data-stu-id="bbf4b-110">**LockIt**</span></span>](imediaobjectimpl-lockit.md) | <span data-ttu-id="bbf4b-111">Classe auxiliar que bloqueia e desbloqueia o DMO.</span><span class="sxs-lookup"><span data-stu-id="bbf4b-111">Helper class that locks and unlocks the DMO.</span></span> |



 



| <span data-ttu-id="bbf4b-112">Método</span><span class="sxs-lookup"><span data-stu-id="bbf4b-112">Method</span></span>                                                                      | <span data-ttu-id="bbf4b-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="bbf4b-113">Description</span></span>                                                          |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="bbf4b-114">[**CheckTypesSet**](/previous-versions/ms807621(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="bbf4b-114">[**CheckTypesSet**](/previous-versions/ms807621(v=msdn.10))</span></span>                     | <span data-ttu-id="bbf4b-115">Determina se todos os fluxos não opcionais têm tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="bbf4b-115">Determines whether all of the non-optional streams have media types.</span></span> |
| <span data-ttu-id="bbf4b-116">[**InputType**](/previous-versions/ms807633(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="bbf4b-116">[**InputType**](/previous-versions/ms807633(v=msdn.10))</span></span>                             | <span data-ttu-id="bbf4b-117">Recupera o tipo de mídia atual para um fluxo de entrada especificado.</span><span class="sxs-lookup"><span data-stu-id="bbf4b-117">Retrieves the current media type for a specified input stream.</span></span>       |
| <span data-ttu-id="bbf4b-118">[**InputTypeSet**](/previous-versions/ms807638(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="bbf4b-118">[**InputTypeSet**](/previous-versions/ms807638(v=msdn.10))</span></span>                       | <span data-ttu-id="bbf4b-119">Consulta se o tipo de mídia foi definido em um fluxo de entrada.</span><span class="sxs-lookup"><span data-stu-id="bbf4b-119">Queries whether the media type was set on an input stream.</span></span>           |
| <span data-ttu-id="bbf4b-120">[**InternalAcceptingInput**](/previous-versions/ms809095(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="bbf4b-120">[**InternalAcceptingInput**](/previous-versions/ms809095(v=msdn.10))</span></span>   | <span data-ttu-id="bbf4b-121">Consulta se um fluxo de entrada pode aceitar mais entradas.</span><span class="sxs-lookup"><span data-stu-id="bbf4b-121">Queries whether an input stream can accept more input.</span></span>               |
| <span data-ttu-id="bbf4b-122">[**InternalCheckInputType**](/previous-versions/ms809096(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="bbf4b-122">[**InternalCheckInputType**](/previous-versions/ms809096(v=msdn.10))</span></span>   | <span data-ttu-id="bbf4b-123">Consulta se um fluxo de entrada pode aceitar um determinado tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="bbf4b-123">Queries whether an input stream can accept a given media type.</span></span>       |
| <span data-ttu-id="bbf4b-124">[**InternalCheckOutputType**](/previous-versions/ms809098(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="bbf4b-124">[**InternalCheckOutputType**](/previous-versions/ms809098(v=msdn.10))</span></span> | <span data-ttu-id="bbf4b-125">Consulta se um fluxo de saída pode aceitar um determinado tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="bbf4b-125">Queries whether an output stream can accept a given media type.</span></span>      |
| <span data-ttu-id="bbf4b-126">[**Bloquear**](/previous-versions/ms809100(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="bbf4b-126">[**Lock**](/previous-versions/ms809100(v=msdn.10))</span></span>                                       | <span data-ttu-id="bbf4b-127">Bloqueia o DMO</span><span class="sxs-lookup"><span data-stu-id="bbf4b-127">Locks the DMO</span></span>                                                        |
| <span data-ttu-id="bbf4b-128">[**OutputType**](/previous-versions/ms807644(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="bbf4b-128">[**OutputType**](/previous-versions/ms807644(v=msdn.10))</span></span>                           | <span data-ttu-id="bbf4b-129">Recupera o tipo de mídia atual para um fluxo de saída especificado.</span><span class="sxs-lookup"><span data-stu-id="bbf4b-129">Retrieves the current media type for a specified output stream.</span></span>      |
| <span data-ttu-id="bbf4b-130">[**OutputTypeSet**](/previous-versions/ms807649(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="bbf4b-130">[**OutputTypeSet**](/previous-versions/ms807649(v=msdn.10))</span></span>                     | <span data-ttu-id="bbf4b-131">Consulta se o tipo de mídia foi definido em um fluxo de saída.</span><span class="sxs-lookup"><span data-stu-id="bbf4b-131">Queries whether the media type was set on an output stream.</span></span>          |
| <span data-ttu-id="bbf4b-132">[**Unlock**](/previous-versions/ms809101(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="bbf4b-132">[**Unlock**](/previous-versions/ms809101(v=msdn.10))</span></span>                                   | <span data-ttu-id="bbf4b-133">Desbloqueia o DMO</span><span class="sxs-lookup"><span data-stu-id="bbf4b-133">Unlocks the DMO</span></span>                                                      |



 

## <a name="requirements"></a><span data-ttu-id="bbf4b-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbf4b-134">Requirements</span></span>



| <span data-ttu-id="bbf4b-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbf4b-135">Requirement</span></span> | <span data-ttu-id="bbf4b-136">Valor</span><span class="sxs-lookup"><span data-stu-id="bbf4b-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbf4b-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bbf4b-137">Header</span></span><br/>  | <dl> <span data-ttu-id="bbf4b-138"><dt>Dmoimpl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbf4b-138"><dt>Dmoimpl.h</dt></span></span> </dl>                                                                     |
| <span data-ttu-id="bbf4b-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bbf4b-139">Library</span></span><br/> | <dl> <span data-ttu-id="bbf4b-140"><dt>Dmoguids. lib; </dt> <dt>Msdmo. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bbf4b-140"><dt>Dmoguids.lib; </dt> <dt>Msdmo.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbf4b-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="bbf4b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbf4b-142">Referência de DMO</span><span class="sxs-lookup"><span data-stu-id="bbf4b-142">DMO Reference</span></span>](dmo-reference.md)
</dt> <dt>

[<span data-ttu-id="bbf4b-143">Usando o modelo de classe DMO</span><span class="sxs-lookup"><span data-stu-id="bbf4b-143">Using the DMO Class Template</span></span>](using-the-dmo-class-template.md)
</dt> </dl>

 

 
