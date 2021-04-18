---
description: A interface IAMTimelineTrack fornece métodos para manipular objetos Track em serviços de edição do DirectShow (DES). Uma faixa contém uma lista de fontes que são processadas na saída final.
ms.assetid: 42ac88f2-1361-413a-a9b0-95f5c32a7c3c
title: Interface IAMTimelineTrack (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 71003694d33b33980fb262f06f6b2e7aa55a70d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767675"
---
# <a name="iamtimelinetrack-interface"></a><span data-ttu-id="850dc-103">Interface IAMTimelineTrack</span><span class="sxs-lookup"><span data-stu-id="850dc-103">IAMTimelineTrack interface</span></span>

> [!Note]  
> <span data-ttu-id="850dc-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="850dc-104">\[Deprecated.</span></span> <span data-ttu-id="850dc-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="850dc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="850dc-106">A `IAMTimelineTrack` interface fornece métodos para manipular objetos *Track* nos [serviços de edição do DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="850dc-106">The `IAMTimelineTrack` interface provides methods for manipulating *track* objects in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="850dc-107">Uma faixa contém uma lista de fontes que são processadas na saída final.</span><span class="sxs-lookup"><span data-stu-id="850dc-107">A track contains a list of sources that are rendered in the final output.</span></span> <span data-ttu-id="850dc-108">As fontes dentro da mesma faixa não podem se sobrepor.</span><span class="sxs-lookup"><span data-stu-id="850dc-108">Sources within the same track may not overlap.</span></span> <span data-ttu-id="850dc-109">As faixas de vídeo podem ter efeitos e transições.</span><span class="sxs-lookup"><span data-stu-id="850dc-109">Video tracks can have both effects and transitions.</span></span> <span data-ttu-id="850dc-110">O mecanismo de renderização aplica efeitos antes de aplicar transições.</span><span class="sxs-lookup"><span data-stu-id="850dc-110">The render engine applies effects before it applies transitions.</span></span> <span data-ttu-id="850dc-111">As faixas de áudio podem ter efeitos, mas não transições.</span><span class="sxs-lookup"><span data-stu-id="850dc-111">Audio tracks can have effects, but not transitions.</span></span> <span data-ttu-id="850dc-112">Para obter mais informações, consulte [o modelo de linha do tempo](the-timeline-model.md).</span><span class="sxs-lookup"><span data-stu-id="850dc-112">For more information, see [The Timeline Model](the-timeline-model.md).</span></span>

<span data-ttu-id="850dc-113">Para criar um objeto Track, chame [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) com o valor linha do tempo \_ Major \_ tipo \_ Track.</span><span class="sxs-lookup"><span data-stu-id="850dc-113">To create a track object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_TRACK.</span></span> <span data-ttu-id="850dc-114">Você pode consultar o ponteiro **IAMTimelineObj** retornado para a `IAMTimelineTrack` interface.</span><span class="sxs-lookup"><span data-stu-id="850dc-114">You can query the returned **IAMTimelineObj** pointer for the `IAMTimelineTrack` interface.</span></span>

## <a name="members"></a><span data-ttu-id="850dc-115">Membros</span><span class="sxs-lookup"><span data-stu-id="850dc-115">Members</span></span>

<span data-ttu-id="850dc-116">A interface **IAMTimelineTrack** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="850dc-116">The **IAMTimelineTrack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="850dc-117">**IAMTimelineTrack** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="850dc-117">**IAMTimelineTrack** also has these types of members:</span></span>

-   [<span data-ttu-id="850dc-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="850dc-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="850dc-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="850dc-119">Methods</span></span>

<span data-ttu-id="850dc-120">A interface **IAMTimelineTrack** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="850dc-120">The **IAMTimelineTrack** interface has these methods.</span></span>



| <span data-ttu-id="850dc-121">Método</span><span class="sxs-lookup"><span data-stu-id="850dc-121">Method</span></span>                                                          | <span data-ttu-id="850dc-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="850dc-122">Description</span></span>                                                                                                                                          |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="850dc-123">**AreYouBlank**</span><span class="sxs-lookup"><span data-stu-id="850dc-123">**AreYouBlank**</span></span>](iamtimelinetrack-areyoublank.md)             | <span data-ttu-id="850dc-124">Determina se a faixa está em branco (não contém nenhum objeto de origem).</span><span class="sxs-lookup"><span data-stu-id="850dc-124">Determines whether the track is blank (contains no source objects).</span></span><br/>                                                                       |
| [<span data-ttu-id="850dc-125">**GetNextSrc**</span><span class="sxs-lookup"><span data-stu-id="850dc-125">**GetNextSrc**</span></span>](iamtimelinetrack-getnextsrc.md)               | <span data-ttu-id="850dc-126">Pesquisa o roteiro da próxima fonte que aparece na hora especificada ou posteriormente.</span><span class="sxs-lookup"><span data-stu-id="850dc-126">Searches the track for the next source that appears at the specified time or later.</span></span><br/>                                                       |
| [<span data-ttu-id="850dc-127">**GetNextSrc2**</span><span class="sxs-lookup"><span data-stu-id="850dc-127">**GetNextSrc2**</span></span>](iamtimelinetrack-getnextsrc2.md)             | <span data-ttu-id="850dc-128">Pesquisa o roteiro da próxima fonte que aparece na hora especificada ou posteriormente, com o fornecido como um valor de [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="850dc-128">Searches the track for the next source that appears at the specified time or later, with the given as a [**REFTIME**](reftime.md) value.</span></span><br/> |
| [<span data-ttu-id="850dc-129">**GetNextSrcEx**</span><span class="sxs-lookup"><span data-stu-id="850dc-129">**GetNextSrcEx**</span></span>](iamtimelinetrack-getnextsrcex.md)           | <span data-ttu-id="850dc-130">Recupera a próxima fonte após a origem especificada.</span><span class="sxs-lookup"><span data-stu-id="850dc-130">Retrieves the next source after the specified source.</span></span><br/>                                                                                     |
| [<span data-ttu-id="850dc-131">**GetSourcesCount**</span><span class="sxs-lookup"><span data-stu-id="850dc-131">**GetSourcesCount**</span></span>](iamtimelinetrack-getsourcescount.md)     | <span data-ttu-id="850dc-132">Recupera o número de fontes no roteiro.</span><span class="sxs-lookup"><span data-stu-id="850dc-132">Retrieves the number of sources in the track.</span></span><br/>                                                                                             |
| [<span data-ttu-id="850dc-133">**GetSrcAtTime**</span><span class="sxs-lookup"><span data-stu-id="850dc-133">**GetSrcAtTime**</span></span>](iamtimelinetrack-getsrcattime.md)           | <span data-ttu-id="850dc-134">Recupera o objeto de origem mais próximo ao horário especificado, de acordo com as condições de limite especificadas.</span><span class="sxs-lookup"><span data-stu-id="850dc-134">Retrieves the source object nearest to the specified time, according to the specified boundary conditions.</span></span><br/>                                |
| [<span data-ttu-id="850dc-135">**GetSrcAtTime2**</span><span class="sxs-lookup"><span data-stu-id="850dc-135">**GetSrcAtTime2**</span></span>](iamtimelinetrack-getsrcattime2.md)         | <span data-ttu-id="850dc-136">Recupera o objeto de origem mais próximo ao tempo especificado, dado como um valor [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="850dc-136">Retrieves the source object nearest to the specified time, given as a [**REFTIME**](reftime.md) value.</span></span><br/>                                   |
| [<span data-ttu-id="850dc-137">**InsertSpace**</span><span class="sxs-lookup"><span data-stu-id="850dc-137">**InsertSpace**</span></span>](iamtimelinetrack-insertspace.md)             | <span data-ttu-id="850dc-138">Divide todos os objetos existentes na hora especificada e insere o espaço entre eles.</span><span class="sxs-lookup"><span data-stu-id="850dc-138">Splits any objects that exist at the specified time and inserts space between them.</span></span><br/>                                                       |
| [<span data-ttu-id="850dc-139">**InsertSpace2**</span><span class="sxs-lookup"><span data-stu-id="850dc-139">**InsertSpace2**</span></span>](iamtimelinetrack-insertspace2.md)           | <span data-ttu-id="850dc-140">Divide todos os objetos existentes na hora especificada e insere o espaço entre eles, usando valores de [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="850dc-140">Splits any objects that exist at the specified time and inserts space between them, using [**REFTIME**](reftime.md) values.</span></span><br/>              |
| [<span data-ttu-id="850dc-141">**MoveEverythingBy**</span><span class="sxs-lookup"><span data-stu-id="850dc-141">**MoveEverythingBy**</span></span>](iamtimelinetrack-moveeverythingby.md)   | <span data-ttu-id="850dc-142">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="850dc-142">Not supported.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="850dc-143">**MoveEverythingBy2**</span><span class="sxs-lookup"><span data-stu-id="850dc-143">**MoveEverythingBy2**</span></span>](iamtimelinetrack-moveeverythingby2.md) | <span data-ttu-id="850dc-144">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="850dc-144">Not supported.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="850dc-145">**SrcAdd**</span><span class="sxs-lookup"><span data-stu-id="850dc-145">**SrcAdd**</span></span>](iamtimelinetrack-srcadd.md)                       | <span data-ttu-id="850dc-146">Adiciona uma origem à faixa.</span><span class="sxs-lookup"><span data-stu-id="850dc-146">Adds a source to the track.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="850dc-147">**ZeroBetween**</span><span class="sxs-lookup"><span data-stu-id="850dc-147">**ZeroBetween**</span></span>](iamtimelinetrack-zerobetween.md)             | <span data-ttu-id="850dc-148">Remove tudo da faixa entre os horários especificados.</span><span class="sxs-lookup"><span data-stu-id="850dc-148">Removes everything from the track between the specified times.</span></span><br/>                                                                            |
| [<span data-ttu-id="850dc-149">**ZeroBetween2**</span><span class="sxs-lookup"><span data-stu-id="850dc-149">**ZeroBetween2**</span></span>](iamtimelinetrack-zerobetween2.md)           | <span data-ttu-id="850dc-150">Remove tudo da faixa entre os horários especificados, fornecidos como valores de [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="850dc-150">Removes everything from the track between the specified times, given as [**REFTIME**](reftime.md) values.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="850dc-151">Comentários</span><span class="sxs-lookup"><span data-stu-id="850dc-151">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="850dc-152">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="850dc-152">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="850dc-153">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="850dc-153">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="850dc-154">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="850dc-154">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="850dc-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="850dc-155">Requirements</span></span>



| <span data-ttu-id="850dc-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="850dc-156">Requirement</span></span> | <span data-ttu-id="850dc-157">Valor</span><span class="sxs-lookup"><span data-stu-id="850dc-157">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="850dc-158">parâmetro</span><span class="sxs-lookup"><span data-stu-id="850dc-158">Header</span></span><br/>  | <dl> <span data-ttu-id="850dc-159"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="850dc-159"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="850dc-160">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="850dc-160">Library</span></span><br/> | <dl> <span data-ttu-id="850dc-161"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="850dc-161"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
