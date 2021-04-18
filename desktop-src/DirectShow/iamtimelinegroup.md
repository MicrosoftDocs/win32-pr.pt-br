---
description: 'A interface IAMTimelineGroup define e recupera propriedades em grupos nos serviços de edição do DirectShow (DES). Um grupo contém uma ou mais faixas e, possivelmente, uma ou mais composições que, por sua vez, contêm clipes de origem de um tipo uniforme, como vídeo ou áudio. Os grupos são as composições mais altas em uma linha do tempo e também expõem a interface IAMTimelineComp. Uma linha do tempo pode conter vários grupos. Cada grupo tem os seguintes atributos. Um tipo de mídia associado. A taxa de quadros na qual o grupo é renderizado, em quadros por segundo (FPS). Todas as edições ocorrem em um tempo arredondado para o limite de quadro mais próximo, conforme definido pela configuração de FPS do grupo. Um nível de prioridade, para gravar arquivos com vários fluxos do mesmo tipo de mídia (por exemplo, um arquivo AVI de dois vídeos). Para criar um objeto de grupo, chame IAMTimeline:: CreateEmptyNode com o valor TIMELINE \_ principal \_ tipo \_ grupo. Você pode consultar o ponteiro IAMTimelineObj retornado para a interface IAMTimelineGroup.'
ms.assetid: c24e5e0a-43a5-4ba7-ac28-6e2ebb341a38
title: Interface IAMTimelineGroup (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e82a11db65183e343048f594a7457c0a8febf8bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810399"
---
# <a name="iamtimelinegroup-interface"></a><span data-ttu-id="f36ad-107">Interface IAMTimelineGroup</span><span class="sxs-lookup"><span data-stu-id="f36ad-107">IAMTimelineGroup interface</span></span>

> [!Note]  
> <span data-ttu-id="f36ad-108">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="f36ad-108">\[Deprecated.</span></span> <span data-ttu-id="f36ad-109">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f36ad-109">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f36ad-110">A `IAMTimelineGroup` interface define e recupera propriedades em grupos nos [serviços de edição do DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="f36ad-110">The `IAMTimelineGroup` interface sets and retrieves properties on groups in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="f36ad-111">Um grupo contém uma ou mais faixas e, possivelmente, uma ou mais composições que, por sua vez, contêm clipes de origem de um tipo uniforme, como vídeo ou áudio.</span><span class="sxs-lookup"><span data-stu-id="f36ad-111">A group contains one or more tracks, and possibly one or more compositions, which in turn contain source clips of a uniform type, such as video or audio.</span></span> <span data-ttu-id="f36ad-112">Os grupos são as composições mais altas em uma linha do tempo e também expõem a interface [**IAMTimelineComp**](iamtimelinecomp.md) .</span><span class="sxs-lookup"><span data-stu-id="f36ad-112">Groups are the topmost compositions in a timeline, and also expose the [**IAMTimelineComp**](iamtimelinecomp.md) interface.</span></span> <span data-ttu-id="f36ad-113">Uma linha do tempo pode conter vários grupos.</span><span class="sxs-lookup"><span data-stu-id="f36ad-113">A timeline can contain multiple groups.</span></span>

<span data-ttu-id="f36ad-114">Cada grupo tem os seguintes atributos.</span><span class="sxs-lookup"><span data-stu-id="f36ad-114">Each group has the following attributes.</span></span>

-   <span data-ttu-id="f36ad-115">Um tipo de mídia associado.</span><span class="sxs-lookup"><span data-stu-id="f36ad-115">An associated media type.</span></span>
-   <span data-ttu-id="f36ad-116">A taxa de quadros na qual o grupo é renderizado, em quadros por segundo (FPS).</span><span class="sxs-lookup"><span data-stu-id="f36ad-116">The frame rate at which the group renders, in frames per second (FPS).</span></span> <span data-ttu-id="f36ad-117">Todas as edições ocorrem em um tempo arredondado para o limite de quadro mais próximo, conforme definido pela configuração de FPS do grupo.</span><span class="sxs-lookup"><span data-stu-id="f36ad-117">All edits occur at a time rounded to the nearest frame boundary, as defined by the group's FPS setting.</span></span>
-   <span data-ttu-id="f36ad-118">Um nível de prioridade, para gravar arquivos com vários fluxos do mesmo tipo de mídia (por exemplo, um arquivo AVI de dois vídeos).</span><span class="sxs-lookup"><span data-stu-id="f36ad-118">A priority level, for writing files with multiple streams of the same media type (for example, a two-video-stream AVI file).</span></span>

<span data-ttu-id="f36ad-119">Para criar um objeto de grupo, chame [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) com o valor Timeline \_ principal \_ tipo \_ grupo.</span><span class="sxs-lookup"><span data-stu-id="f36ad-119">To create a group object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_GROUP.</span></span> <span data-ttu-id="f36ad-120">Você pode consultar o ponteiro [**IAMTimelineObj**](iamtimelineobj.md) retornado para a interface **IAMTimelineGroup** .</span><span class="sxs-lookup"><span data-stu-id="f36ad-120">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the **IAMTimelineGroup** interface.</span></span>

## <a name="members"></a><span data-ttu-id="f36ad-121">Membros</span><span class="sxs-lookup"><span data-stu-id="f36ad-121">Members</span></span>

<span data-ttu-id="f36ad-122">A interface **IAMTimelineGroup** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f36ad-122">The **IAMTimelineGroup** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f36ad-123">**IAMTimelineGroup** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f36ad-123">**IAMTimelineGroup** also has these types of members:</span></span>

-   [<span data-ttu-id="f36ad-124">Métodos</span><span class="sxs-lookup"><span data-stu-id="f36ad-124">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f36ad-125">Métodos</span><span class="sxs-lookup"><span data-stu-id="f36ad-125">Methods</span></span>

<span data-ttu-id="f36ad-126">A interface **IAMTimelineGroup** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f36ad-126">The **IAMTimelineGroup** interface has these methods.</span></span>



| <span data-ttu-id="f36ad-127">Método</span><span class="sxs-lookup"><span data-stu-id="f36ad-127">Method</span></span>                                                                            | <span data-ttu-id="f36ad-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="f36ad-128">Description</span></span>                                                                                     |
|:----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f36ad-129">**ClearRecompressFormatDirty**</span><span class="sxs-lookup"><span data-stu-id="f36ad-129">**ClearRecompressFormatDirty**</span></span>](iamtimelinegroup-clearrecompressformatdirty.md) | <span data-ttu-id="f36ad-130">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="f36ad-130">Not supported.</span></span><br/>                                                                       |
| [<span data-ttu-id="f36ad-131">**Getgroupname**</span><span class="sxs-lookup"><span data-stu-id="f36ad-131">**GetGroupName**</span></span>](iamtimelinegroup-getgroupname.md)                             | <span data-ttu-id="f36ad-132">Recupera o nome definido pelo aplicativo do grupo.</span><span class="sxs-lookup"><span data-stu-id="f36ad-132">Retrieves the application-defined name of the group.</span></span><br/>                                 |
| [<span data-ttu-id="f36ad-133">**GetMediaType**</span><span class="sxs-lookup"><span data-stu-id="f36ad-133">**GetMediaType**</span></span>](iamtimelinegroup-getmediatype.md)                             | <span data-ttu-id="f36ad-134">Recupera o tipo de mídia descompactado para o grupo.</span><span class="sxs-lookup"><span data-stu-id="f36ad-134">Retrieves the uncompressed media type for the group.</span></span><br/>                                 |
| [<span data-ttu-id="f36ad-135">**GetOutputBuffering**</span><span class="sxs-lookup"><span data-stu-id="f36ad-135">**GetOutputBuffering**</span></span>](iamtimelinegroup-getoutputbuffering.md)                 | <span data-ttu-id="f36ad-136">Recupera o número de quadros renderizados antecipadamente durante a visualização.</span><span class="sxs-lookup"><span data-stu-id="f36ad-136">Retrieves the number of frames rendered in advance during preview.</span></span><br/>                   |
| [<span data-ttu-id="f36ad-137">**GetOutputFPS**</span><span class="sxs-lookup"><span data-stu-id="f36ad-137">**GetOutputFPS**</span></span>](iamtimelinegroup-getoutputfps.md)                             | <span data-ttu-id="f36ad-138">Recupera a taxa de quadros de saída deste grupo.</span><span class="sxs-lookup"><span data-stu-id="f36ad-138">Retrieves the output frame rate of this group.</span></span><br/>                                       |
| [<span data-ttu-id="f36ad-139">**Getpreviewmode**</span><span class="sxs-lookup"><span data-stu-id="f36ad-139">**GetPreviewMode**</span></span>](iamtimelinegroup-getpreviewmode.md)                         | <span data-ttu-id="f36ad-140">Recupera o modo de visualização do grupo.</span><span class="sxs-lookup"><span data-stu-id="f36ad-140">Retrieves the preview mode for the group.</span></span><br/>                                            |
| [<span data-ttu-id="f36ad-141">**Getanteriority**</span><span class="sxs-lookup"><span data-stu-id="f36ad-141">**GetPriority**</span></span>](iamtimelinegroup-getpriority.md)                               | <span data-ttu-id="f36ad-142">Recupera a prioridade do grupo.</span><span class="sxs-lookup"><span data-stu-id="f36ad-142">Retrieves the group's priority.</span></span><br/>                                                      |
| [<span data-ttu-id="f36ad-143">**GetSmartRecompressFormat**</span><span class="sxs-lookup"><span data-stu-id="f36ad-143">**GetSmartRecompressFormat**</span></span>](iamtimelinegroup-getsmartrecompressformat.md)     | <span data-ttu-id="f36ad-144">Recupera o formato de compactação atual para a recompactação inteligente.</span><span class="sxs-lookup"><span data-stu-id="f36ad-144">Retrieves the current compression format for smart recompression.</span></span><br/>                    |
| [<span data-ttu-id="f36ad-145">**GetTimer**</span><span class="sxs-lookup"><span data-stu-id="f36ad-145">**GetTimeline**</span></span>](iamtimelinegroup-gettimeline.md)                               | <span data-ttu-id="f36ad-146">Recupera a linha do tempo à qual este grupo pertence.</span><span class="sxs-lookup"><span data-stu-id="f36ad-146">Retrieves the timeline to which this group belongs.</span></span><br/>                                  |
| [<span data-ttu-id="f36ad-147">**IsRecompressFormatDirty**</span><span class="sxs-lookup"><span data-stu-id="f36ad-147">**IsRecompressFormatDirty**</span></span>](iamtimelinegroup-isrecompressformatdirty.md)       | <span data-ttu-id="f36ad-148">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="f36ad-148">Not supported.</span></span><br/>                                                                       |
| [<span data-ttu-id="f36ad-149">**IsSmartRecompressFormatSet**</span><span class="sxs-lookup"><span data-stu-id="f36ad-149">**IsSmartRecompressFormatSet**</span></span>](iamtimelinegroup-issmartrecompressformatset.md) | <span data-ttu-id="f36ad-150">Determina se um formato de compactação inteligente foi definido para o grupo.</span><span class="sxs-lookup"><span data-stu-id="f36ad-150">Determines whether a smart compression format was set for the group.</span></span><br/>                 |
| [<span data-ttu-id="f36ad-151">**Setgroupname**</span><span class="sxs-lookup"><span data-stu-id="f36ad-151">**SetGroupName**</span></span>](iamtimelinegroup-setgroupname.md)                             | <span data-ttu-id="f36ad-152">Define o nome definido pelo aplicativo do grupo.</span><span class="sxs-lookup"><span data-stu-id="f36ad-152">Sets the application-defined name of the group.</span></span><br/>                                      |
| [<span data-ttu-id="f36ad-153">**SetMediaType**</span><span class="sxs-lookup"><span data-stu-id="f36ad-153">**SetMediaType**</span></span>](iamtimelinegroup-setmediatype.md)                             | <span data-ttu-id="f36ad-154">Define o tipo de mídia descompactado para o grupo.</span><span class="sxs-lookup"><span data-stu-id="f36ad-154">Sets the uncompressed media type for the group.</span></span><br/>                                      |
| [<span data-ttu-id="f36ad-155">**SetMediaTypeForVB**</span><span class="sxs-lookup"><span data-stu-id="f36ad-155">**SetMediaTypeForVB**</span></span>](iamtimelinegroup-setmediatypeforvb.md)                   | <span data-ttu-id="f36ad-156">Especifica o tipo de mídia do grupo, para clientes de automação.</span><span class="sxs-lookup"><span data-stu-id="f36ad-156">Specifies the group media type, for Automation clients.</span></span><br/>                              |
| [<span data-ttu-id="f36ad-157">**SetOutputBuffering**</span><span class="sxs-lookup"><span data-stu-id="f36ad-157">**SetOutputBuffering**</span></span>](iamtimelinegroup-setoutputbuffering.md)                 | <span data-ttu-id="f36ad-158">Especifica o número de quadros renderizados antecipadamente durante a visualização.</span><span class="sxs-lookup"><span data-stu-id="f36ad-158">Specifies the number of frames rendered in advance during preview.</span></span><br/>                   |
| [<span data-ttu-id="f36ad-159">**SetOutputFPS**</span><span class="sxs-lookup"><span data-stu-id="f36ad-159">**SetOutputFPS**</span></span>](iamtimelinegroup-setoutputfps.md)                             | <span data-ttu-id="f36ad-160">Define a taxa de quadros de saída não compactados para esse grupo.</span><span class="sxs-lookup"><span data-stu-id="f36ad-160">Sets the uncompressed output frame rate for this group.</span></span><br/>                              |
| [<span data-ttu-id="f36ad-161">**SetPreviewMode**</span><span class="sxs-lookup"><span data-stu-id="f36ad-161">**SetPreviewMode**</span></span>](iamtimelinegroup-setpreviewmode.md)                         | <span data-ttu-id="f36ad-162">Define o modo de visualização para o grupo.</span><span class="sxs-lookup"><span data-stu-id="f36ad-162">Sets the preview mode for the group.</span></span><br/>                                                 |
| [<span data-ttu-id="f36ad-163">**SetRecompFormatFromSource**</span><span class="sxs-lookup"><span data-stu-id="f36ad-163">**SetRecompFormatFromSource**</span></span>](iamtimelinegroup-setrecompformatfromsource.md)   | <span data-ttu-id="f36ad-164">Define o formato de recompactação de vídeo usando o formato de compactação de um arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="f36ad-164">Sets the video recompression format using the compression format from a source file.</span></span><br/> |
| [<span data-ttu-id="f36ad-165">**SetSmartRecompressFormat**</span><span class="sxs-lookup"><span data-stu-id="f36ad-165">**SetSmartRecompressFormat**</span></span>](iamtimelinegroup-setsmartrecompressformat.md)     | <span data-ttu-id="f36ad-166">Especifica um formato de compactação a ser usado para a recompactação inteligente.</span><span class="sxs-lookup"><span data-stu-id="f36ad-166">Specifies a compression format to use for smart recompression.</span></span><br/>                       |
| [<span data-ttu-id="f36ad-167">**SetTimer**</span><span class="sxs-lookup"><span data-stu-id="f36ad-167">**SetTimeline**</span></span>](iamtimelinegroup-settimeline.md)                               | <span data-ttu-id="f36ad-168">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="f36ad-168">Not supported.</span></span><br/>                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="f36ad-169">Comentários</span><span class="sxs-lookup"><span data-stu-id="f36ad-169">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f36ad-170">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="f36ad-170">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f36ad-171">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f36ad-171">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f36ad-172">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f36ad-172">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f36ad-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f36ad-173">Requirements</span></span>



| <span data-ttu-id="f36ad-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="f36ad-174">Requirement</span></span> | <span data-ttu-id="f36ad-175">Valor</span><span class="sxs-lookup"><span data-stu-id="f36ad-175">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f36ad-176">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f36ad-176">Header</span></span><br/>  | <dl> <span data-ttu-id="f36ad-177"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f36ad-177"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f36ad-178">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f36ad-178">Library</span></span><br/> | <dl> <span data-ttu-id="f36ad-179"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f36ad-179"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
