---
description: 'A interface IRenderEngine renderiza um projeto de serviços de edição do DirectShow (DES) construindo um grafo de filtro de uma linha do tempo. O DES fornece dois componentes que implementam essa interface: o mecanismo de renderização básico cria uma saída não compactada.'
ms.assetid: e2a91b34-ee4d-405e-81bf-29d15ea6342a
title: Interface IRenderEngine (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d8c57e976fac877a02c3f3993fb3fe4d27f9033b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760737"
---
# <a name="irenderengine-interface"></a><span data-ttu-id="6892f-103">Interface IRenderEngine</span><span class="sxs-lookup"><span data-stu-id="6892f-103">IRenderEngine interface</span></span>

> [!Note]  
> <span data-ttu-id="6892f-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="6892f-104">\[Deprecated.</span></span> <span data-ttu-id="6892f-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6892f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6892f-106">A `IRenderEngine` interface renderiza um projeto de [serviços de edição do DirectShow](directshow-editing-services.md) (des) construindo um grafo de filtro de uma linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="6892f-106">The `IRenderEngine` interface renders a [DirectShow Editing Services](directshow-editing-services.md) (DES) project by constructing a filter graph from a timeline.</span></span>

<span data-ttu-id="6892f-107">O DES fornece dois componentes que implementam essa interface:</span><span class="sxs-lookup"><span data-stu-id="6892f-107">DES provides two components that implement this interface:</span></span>

-   <span data-ttu-id="6892f-108">O *mecanismo de renderização básico* cria uma saída não compactada.</span><span class="sxs-lookup"><span data-stu-id="6892f-108">The *basic render engine* creates uncompressed output.</span></span> <span data-ttu-id="6892f-109">Você pode usar a saída para visualização ou circulá-la por meio de filtros de compactação e gravá-la em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="6892f-109">You can use the output for preview, or route it through compression filters and write it to a file.</span></span>
-   <span data-ttu-id="6892f-110">O *mecanismo de processamento inteligente* cria uma saída compactada, usando a *recompactação inteligente*.</span><span class="sxs-lookup"><span data-stu-id="6892f-110">The *smart render engine* creates compressed output, using *smart recompression*.</span></span> <span data-ttu-id="6892f-111">Com a recompactação inteligente, um arquivo de origem será recompactado somente se seu formato for diferente do formato de saída.</span><span class="sxs-lookup"><span data-stu-id="6892f-111">With smart recompression, a source file is recompressed only if its format differs from the output format.</span></span> <span data-ttu-id="6892f-112">Uma fonte com um formato correspondente é gravada diretamente no arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="6892f-112">A source with a matching format is written directly to the output file.</span></span> <span data-ttu-id="6892f-113">Dependendo do cenário, a recompactação inteligente pode melhorar muito o tempo de renderização.</span><span class="sxs-lookup"><span data-stu-id="6892f-113">Depending on the scenario, smart recompression can greatly improve rendering time.</span></span>

<span data-ttu-id="6892f-114">O mecanismo de processamento inteligente também dá suporte à interface [**ISmartRenderEngine**](ismartrenderengine.md) .</span><span class="sxs-lookup"><span data-stu-id="6892f-114">The smart render engine also supports the [**ISmartRenderEngine**](ismartrenderengine.md) interface.</span></span>

<span data-ttu-id="6892f-115">Embora um aplicativo possa criar um gráfico de filtro e passá-lo para um mecanismo de renderização, o cenário típico é que o mecanismo de renderização crie o gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="6892f-115">Although an application can create a filter graph and pass it to a render engine, the typical scenario is for the render engine to create the filter graph.</span></span> <span data-ttu-id="6892f-116">Criar o grafo é um processo de duas etapas.</span><span class="sxs-lookup"><span data-stu-id="6892f-116">Building the graph is a two-stage process.</span></span> <span data-ttu-id="6892f-117">Primeiro, compile o front-end chamando o método [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) .</span><span class="sxs-lookup"><span data-stu-id="6892f-117">First, build the front end by calling the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method.</span></span> <span data-ttu-id="6892f-118">Em seguida, conecte os Pins de saída no front-end aos filtros de renderização desejados:</span><span class="sxs-lookup"><span data-stu-id="6892f-118">Then connect the output pins on the front end to the desired rendering filters:</span></span>

-   <span data-ttu-id="6892f-119">Renderizadores de vídeo e áudio para visualização ou</span><span class="sxs-lookup"><span data-stu-id="6892f-119">Video and audio renderers for preview, or</span></span>
-   <span data-ttu-id="6892f-120">Compactadores, multiplexadores e gravadores de arquivo para gerar a saída final.</span><span class="sxs-lookup"><span data-stu-id="6892f-120">Compressors, multiplexers, and file writers to generate the final output.</span></span>

## <a name="members"></a><span data-ttu-id="6892f-121">Membros</span><span class="sxs-lookup"><span data-stu-id="6892f-121">Members</span></span>

<span data-ttu-id="6892f-122">A interface **IRenderEngine** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6892f-122">The **IRenderEngine** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6892f-123">**IRenderEngine** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6892f-123">**IRenderEngine** also has these types of members:</span></span>

-   [<span data-ttu-id="6892f-124">Métodos</span><span class="sxs-lookup"><span data-stu-id="6892f-124">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6892f-125">Métodos</span><span class="sxs-lookup"><span data-stu-id="6892f-125">Methods</span></span>

<span data-ttu-id="6892f-126">A interface **IRenderEngine** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="6892f-126">The **IRenderEngine** interface has these methods.</span></span>



| <span data-ttu-id="6892f-127">Método</span><span class="sxs-lookup"><span data-stu-id="6892f-127">Method</span></span>                                                                             | <span data-ttu-id="6892f-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="6892f-128">Description</span></span>                                                                           |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="6892f-129">**Compromisso**</span><span class="sxs-lookup"><span data-stu-id="6892f-129">**Commit**</span></span>](irenderengine-commit.md)                                             | <span data-ttu-id="6892f-130">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="6892f-130">Not implemented.</span></span><br/>                                                           |
| [<span data-ttu-id="6892f-131">**ConnectFrontEnd**</span><span class="sxs-lookup"><span data-stu-id="6892f-131">**ConnectFrontEnd**</span></span>](irenderengine-connectfrontend.md)                           | <span data-ttu-id="6892f-132">Cria o front-end do grafo de filtro a partir da linha do tempo atual.</span><span class="sxs-lookup"><span data-stu-id="6892f-132">Builds the front end of the filter graph from the current timeline.</span></span><br/>        |
| [<span data-ttu-id="6892f-133">**Anulação confirmação**</span><span class="sxs-lookup"><span data-stu-id="6892f-133">**Decommit**</span></span>](irenderengine-decommit.md)                                         | <span data-ttu-id="6892f-134">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="6892f-134">Not implemented.</span></span><br/>                                                           |
| [<span data-ttu-id="6892f-135">**DoSmartRecompression**</span><span class="sxs-lookup"><span data-stu-id="6892f-135">**DoSmartRecompression**</span></span>](irenderengine-dosmartrecompression.md)                 | <span data-ttu-id="6892f-136">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="6892f-136">Not supported.</span></span><br/>                                                             |
| [<span data-ttu-id="6892f-137">**GetCaps**</span><span class="sxs-lookup"><span data-stu-id="6892f-137">**GetCaps**</span></span>](irenderengine-getcaps.md)                                           | <span data-ttu-id="6892f-138">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="6892f-138">Not implemented.</span></span><br/>                                                           |
| [<span data-ttu-id="6892f-139">**GetFilterGraph**</span><span class="sxs-lookup"><span data-stu-id="6892f-139">**GetFilterGraph**</span></span>](irenderengine-getfiltergraph.md)                             | <span data-ttu-id="6892f-140">Recupera o gráfico de filtro que o mecanismo de processamento construiu, se houver.</span><span class="sxs-lookup"><span data-stu-id="6892f-140">Retrieves the filter graph that the render engine has constructed, if any.</span></span><br/> |
| [<span data-ttu-id="6892f-141">**GetGroupOutputPin**</span><span class="sxs-lookup"><span data-stu-id="6892f-141">**GetGroupOutputPin**</span></span>](irenderengine-getgroupoutputpin.md)                       | <span data-ttu-id="6892f-142">Recupera o pino de saída para o grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="6892f-142">Retrieves the output pin for the specified group.</span></span><br/>                          |
| [<span data-ttu-id="6892f-143">**Gettimelineobject**</span><span class="sxs-lookup"><span data-stu-id="6892f-143">**GetTimelineObject**</span></span>](irenderengine-gettimelineobject.md)                       | <span data-ttu-id="6892f-144">Recupera a linha do tempo que o mecanismo de processamento está usando no momento.</span><span class="sxs-lookup"><span data-stu-id="6892f-144">Retrieves the timeline that the render engine is currently using.</span></span><br/>          |
| [<span data-ttu-id="6892f-145">**Getvendor**</span><span class="sxs-lookup"><span data-stu-id="6892f-145">**GetVendorString**</span></span>](irenderengine-getvendorstring.md)                           | <span data-ttu-id="6892f-146">Recupera a cadeia de caracteres do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="6892f-146">Retrieves the vendor string.</span></span><br/>                                               |
| [<span data-ttu-id="6892f-147">**RenderOutputPins**</span><span class="sxs-lookup"><span data-stu-id="6892f-147">**RenderOutputPins**</span></span>](irenderengine-renderoutputpins.md)                         | <span data-ttu-id="6892f-148">Cria a parte de visualização do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="6892f-148">Creates the previewing portion of the filter graph.</span></span><br/>                        |
| [<span data-ttu-id="6892f-149">**ScrapIt**</span><span class="sxs-lookup"><span data-stu-id="6892f-149">**ScrapIt**</span></span>](irenderengine-scrapit.md)                                           | <span data-ttu-id="6892f-150">Descarta o grafo de filtro do mecanismo de processamento e todos os objetos associados.</span><span class="sxs-lookup"><span data-stu-id="6892f-150">Discards the render engine's filter graph and all associated objects.</span></span><br/>      |
| [<span data-ttu-id="6892f-151">**SetDynamicReconnectLevel**</span><span class="sxs-lookup"><span data-stu-id="6892f-151">**SetDynamicReconnectLevel**</span></span>](irenderengine-setdynamicreconnectlevel.md)         | <span data-ttu-id="6892f-152">Define o nível de reconexão dinâmica durante a renderização.</span><span class="sxs-lookup"><span data-stu-id="6892f-152">Sets the level of dynamic reconnection during rendering.</span></span><br/>                   |
| [<span data-ttu-id="6892f-153">**SetFilterGraph**</span><span class="sxs-lookup"><span data-stu-id="6892f-153">**SetFilterGraph**</span></span>](irenderengine-setfiltergraph.md)                             | <span data-ttu-id="6892f-154">Especifica um grafo de filtro para o mecanismo de renderização usar.</span><span class="sxs-lookup"><span data-stu-id="6892f-154">Specifies a filter graph for the render engine to use.</span></span><br/>                     |
| [<span data-ttu-id="6892f-155">**SetInterestRange**</span><span class="sxs-lookup"><span data-stu-id="6892f-155">**SetInterestRange**</span></span>](irenderengine-setinterestrange.md)                         | <span data-ttu-id="6892f-156">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="6892f-156">Not supported.</span></span><br/>                                                             |
| [<span data-ttu-id="6892f-157">**SetInterestRange2**</span><span class="sxs-lookup"><span data-stu-id="6892f-157">**SetInterestRange2**</span></span>](irenderengine-setinterestrange2.md)                       | <span data-ttu-id="6892f-158">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="6892f-158">Not supported.</span></span><br/>                                                             |
| [<span data-ttu-id="6892f-159">**SetRenderRange**</span><span class="sxs-lookup"><span data-stu-id="6892f-159">**SetRenderRange**</span></span>](irenderengine-setrenderrange.md)                             | <span data-ttu-id="6892f-160">Define o intervalo de tempo a ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="6892f-160">Sets the range of time to be rendered.</span></span><br/>                                     |
| [<span data-ttu-id="6892f-161">**SetRenderRange2**</span><span class="sxs-lookup"><span data-stu-id="6892f-161">**SetRenderRange2**</span></span>](irenderengine-setrenderrange2.md)                           | <span data-ttu-id="6892f-162">Define o intervalo de tempo a ser renderizado, como um **duplo**.</span><span class="sxs-lookup"><span data-stu-id="6892f-162">Sets the range of time to be rendered, as a **double**.</span></span><br/>                    |
| [<span data-ttu-id="6892f-163">**SetSourceConnectCallback**</span><span class="sxs-lookup"><span data-stu-id="6892f-163">**SetSourceConnectCallback**</span></span>](irenderengine-setsourceconnectcallback.md)         | <span data-ttu-id="6892f-164">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="6892f-164">Not supported.</span></span><br/>                                                             |
| [<span data-ttu-id="6892f-165">**SetSourceNameValidation**</span><span class="sxs-lookup"><span data-stu-id="6892f-165">**SetSourceNameValidation**</span></span>](irenderengine-setsourcenamevalidation.md)           | <span data-ttu-id="6892f-166">Especifica como o mecanismo de renderização valida nomes de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6892f-166">Specifies how the render engine validates file names.</span></span><br/>                      |
| [<span data-ttu-id="6892f-167">**Settimelineobject**</span><span class="sxs-lookup"><span data-stu-id="6892f-167">**SetTimelineObject**</span></span>](irenderengine-settimelineobject.md)                       | <span data-ttu-id="6892f-168">Define a linha do tempo para o mecanismo de renderização usar.</span><span class="sxs-lookup"><span data-stu-id="6892f-168">Sets the timeline for the render engine to use.</span></span><br/>                            |
| [<span data-ttu-id="6892f-169">**UseInSmartRecompressionGraph**</span><span class="sxs-lookup"><span data-stu-id="6892f-169">**UseInSmartRecompressionGraph**</span></span>](irenderengine-useinsmartrecompressiongraph.md) | <span data-ttu-id="6892f-170">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="6892f-170">Not supported.</span></span><br/>                                                             |



 

## <a name="remarks"></a><span data-ttu-id="6892f-171">Comentários</span><span class="sxs-lookup"><span data-stu-id="6892f-171">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6892f-172">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="6892f-172">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6892f-173">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6892f-173">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6892f-174">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6892f-174">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6892f-175">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6892f-175">Requirements</span></span>



| <span data-ttu-id="6892f-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="6892f-176">Requirement</span></span> | <span data-ttu-id="6892f-177">Valor</span><span class="sxs-lookup"><span data-stu-id="6892f-177">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6892f-178">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6892f-178">Header</span></span><br/>  | <dl> <span data-ttu-id="6892f-179"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6892f-179"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6892f-180">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6892f-180">Library</span></span><br/> | <dl> <span data-ttu-id="6892f-181"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6892f-181"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6892f-182">Confira também</span><span class="sxs-lookup"><span data-stu-id="6892f-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6892f-183">Renderizando um projeto</span><span class="sxs-lookup"><span data-stu-id="6892f-183">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 
