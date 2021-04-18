---
description: Representa informações sobre o histórico de pixel.
MS-HAID: vspixengine.PixelHistoryOperation
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estrutura PixelHistoryOperation
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 59DC72FC-3865-48D3-9F92-9BE93DCA093B
api_name:
- PixelHistoryOperation
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c02a6725f588aaa4c7d72c48d03d921503d4e6a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105771538"
---
# <a name="span-idvspixenginepixelhistoryoperationspanpixelhistoryoperation-structure"></a><span data-ttu-id="fe1a8-103"><span id="vspixengine.pixelhistoryoperation"></span>Estrutura PixelHistoryOperation</span><span class="sxs-lookup"><span data-stu-id="fe1a8-103"><span id="vspixengine.pixelhistoryoperation"></span>PixelHistoryOperation structure</span></span>

<span data-ttu-id="fe1a8-104">Representa informações sobre o histórico de pixel.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-104">Represents information about pixel history.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe1a8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fe1a8-105">Syntax</span></span>


```C++
} PixelHistoryOperation;
```

## <a name="members"></a><span data-ttu-id="fe1a8-106">Membros</span><span class="sxs-lookup"><span data-stu-id="fe1a8-106">Members</span></span>

<span data-ttu-id="fe1a8-107">**Eid**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-107">**eid**</span></span>  
<span data-ttu-id="fe1a8-108">A ID do evento de gráficos associado a esta operação.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-108">The ID of the graphics event associated with this operation.</span></span>

<span data-ttu-id="fe1a8-109">**PCP**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-109">**PCP**</span></span>  
<span data-ttu-id="fe1a8-110">Chamadas empacotadas associadas a esta operação.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-110">Packed calls associated with this operation.</span></span>

<span data-ttu-id="fe1a8-111">**renderTargetPtr**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-111">**renderTargetPtr**</span></span>  
<span data-ttu-id="fe1a8-112">O destino de renderização originalmente associado (dentro do aplicativo capturado) com esta operação.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-112">The render target originally associated (inside the captured application) with this operation.</span></span>

<span data-ttu-id="fe1a8-113">**iPrim**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-113">**iPrim**</span></span>  
<span data-ttu-id="fe1a8-114">O índice da primitiva real associada à sua operação.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-114">The index of the actual primitive associated witht his operation.</span></span>

<span data-ttu-id="fe1a8-115">**numPrims**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-115">**numPrims**</span></span>  
<span data-ttu-id="fe1a8-116">O número total de primitivos associados a esta operação.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-116">The total number of primitives associated with this operation.</span></span>

<span data-ttu-id="fe1a8-117">**numVertsPerPrim**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-117">**numVertsPerPrim**</span></span>  
<span data-ttu-id="fe1a8-118">O número de vértices por primitivo.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-118">The number of vertices per primitive.</span></span>

<span data-ttu-id="fe1a8-119">**iInstance**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-119">**iInstance**</span></span>  
<span data-ttu-id="fe1a8-120">Ao renderizar instâncias, o número de instância da instância real associada a essa operação.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-120">When rendering instances, the instance number of the actual instance associated with this operation.</span></span>

<span data-ttu-id="fe1a8-121">**iInstanceCount**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-121">**iInstanceCount**</span></span>  
<span data-ttu-id="fe1a8-122">Ao renderizar instâncias, o número total de instâncias associadas a essa operação.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-122">When rendering instances, the total number of instances associated with this operation.</span></span>

<span data-ttu-id="fe1a8-123">**bAssemblerStageGeneratesInstanceID**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-123">**bAssemblerStageGeneratesInstanceID**</span></span>  
<span data-ttu-id="fe1a8-124">true se o montador de entrada gerar IDs de instância; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-124">true if the input assembler generates instance IDs; otherwise false.</span></span>

<span data-ttu-id="fe1a8-125">**sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-125">**flags**</span></span>  
<span data-ttu-id="fe1a8-126">Uma combinação de valores PIXELHISTORYFLAGS.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-126">A combination of PIXELHISTORYFLAGS values.</span></span> <span data-ttu-id="fe1a8-127">Para obter mais informações, consulte a enumeração PIXELHISTORYFLAGS.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-127">For more information, see the PIXELHISTORYFLAGS enumeration.</span></span>

<span data-ttu-id="fe1a8-128">**pVSFile**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-128">**pVSFile**</span></span>  
<span data-ttu-id="fe1a8-129">Um FILEPTR para o fluxo de bytes do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-129">A FILEPTR for the pixel shader byte stream.</span></span> <span data-ttu-id="fe1a8-130">Isso é passado de volta para depurar.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-130">This is passed back in order to debug.</span></span>

<span data-ttu-id="fe1a8-131">**pGSFile**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-131">**pGSFile**</span></span>  
<span data-ttu-id="fe1a8-132">Um FILEPTR para o fluxo de bytes do sombreador de geometria.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-132">A FILEPTR for the geometry shader byte stream.</span></span> <span data-ttu-id="fe1a8-133">Isso é passado de volta para depurar.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-133">This is passed back in order to debug.</span></span>

<span data-ttu-id="fe1a8-134">**pPSFile**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-134">**pPSFile**</span></span>  
<span data-ttu-id="fe1a8-135">Um FILEPTR para o fluxo de bytes do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-135">A FILEPTR for the pixel shader byte stream.</span></span> <span data-ttu-id="fe1a8-136">Isso é passado de volta para depurar.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-136">This is passed back in order to debug.</span></span>

<span data-ttu-id="fe1a8-137">**pHSFile**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-137">**pHSFile**</span></span>  
<span data-ttu-id="fe1a8-138">Um FILEPTR para o fluxo de bytes do sombreador envoltória.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-138">A FILEPTR for the hull shader byte stream.</span></span> <span data-ttu-id="fe1a8-139">Isso é passado de volta para depurar.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-139">This is passed back in order to debug.</span></span>

<span data-ttu-id="fe1a8-140">**pDSFile**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-140">**pDSFile**</span></span>  
<span data-ttu-id="fe1a8-141">Um FILEPTR para o fluxo de bytes do sombreador de domínio.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-141">A FILEPTR for the domain shader byte stream.</span></span> <span data-ttu-id="fe1a8-142">Isso é passado de volta para depurar.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-142">This is passed back in order to debug.</span></span>

<span data-ttu-id="fe1a8-143">**pCSFile**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-143">**pCSFile**</span></span>  
<span data-ttu-id="fe1a8-144">Um FILEPTR para o fluxo de bytes do sombreador de computação.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-144">A FILEPTR for the compute shader byte stream.</span></span> <span data-ttu-id="fe1a8-145">Isso é passado de volta para depurar.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-145">This is passed back in order to debug.</span></span>

<span data-ttu-id="fe1a8-146">**VertexShaderFile**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-146">**VertexShaderFile**</span></span>  
<span data-ttu-id="fe1a8-147">Uma cadeia de caracteres COM que contém o FilePath do arquivo de origem do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-147">A COM string containing the filepath of the vertex shader source file.</span></span>

<span data-ttu-id="fe1a8-148">**PixelShaderFile**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-148">**PixelShaderFile**</span></span>  
<span data-ttu-id="fe1a8-149">Uma cadeia de caracteres COM que contém o caminho de arquivo de origem do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-149">A COM string containing the filepath of the pixel shader source file.</span></span>

<span data-ttu-id="fe1a8-150">**GeometryShaderFile**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-150">**GeometryShaderFile**</span></span>  
<span data-ttu-id="fe1a8-151">Uma cadeia de caracteres COM que contém o FilePath do arquivo de origem do sombreador de geometria.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-151">A COM string containing the filepath of the geometry shader source file.</span></span>

<span data-ttu-id="fe1a8-152">**HullShaderFile**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-152">**HullShaderFile**</span></span>  
<span data-ttu-id="fe1a8-153">Uma cadeia de caracteres COM que contém o FilePath do arquivo de origem do sombreador envoltória.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-153">A COM string containing the filepath of the hull shader source file.</span></span>

<span data-ttu-id="fe1a8-154">**DomainShaderFile**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-154">**DomainShaderFile**</span></span>  
<span data-ttu-id="fe1a8-155">Uma cadeia de caracteres COM que contém o caminho de arquivo de origem do sombreador de domínio.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-155">A COM string containing the filepath of the domain shader source file.</span></span>

<span data-ttu-id="fe1a8-156">**psRed**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-156">**psRed**</span></span>  
<span data-ttu-id="fe1a8-157">Saída do sombreador de pixel: valor do componente de cor vermelha.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-157">Pixel shader output: value of red color component.</span></span>

<span data-ttu-id="fe1a8-158">**psGreen**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-158">**psGreen**</span></span>  
<span data-ttu-id="fe1a8-159">Saída do sombreador de pixel: valor do componente de cor verde.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-159">Pixel shader output: value of green color component.</span></span>

<span data-ttu-id="fe1a8-160">**psBlue**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-160">**psBlue**</span></span>  
<span data-ttu-id="fe1a8-161">Saída do sombreador de pixel: valor do componente de cor azul</span><span class="sxs-lookup"><span data-stu-id="fe1a8-161">Pixel shader output: value of blue color component</span></span>

<span data-ttu-id="fe1a8-162">**psAlpha**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-162">**psAlpha**</span></span>  
<span data-ttu-id="fe1a8-163">Saída do sombreador de pixel: valor do componente de cor alfa</span><span class="sxs-lookup"><span data-stu-id="fe1a8-163">Pixel shader output: value of alpha color component</span></span>

<span data-ttu-id="fe1a8-164">**LabelPSRed**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-164">**LabelPSRed**</span></span>  
<span data-ttu-id="fe1a8-165">Uma cadeia COM que contém o nome do rótulo associado ao componente de cor vermelha da saída do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-165">A COM string containing the name of the label associated with the red color component of the pixel shader output.</span></span>

<span data-ttu-id="fe1a8-166">**LabelPSGreen**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-166">**LabelPSGreen**</span></span>  
<span data-ttu-id="fe1a8-167">Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor verde da saída do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-167">A COM string containing the name of the label associated with the green color component of the pixel shader output.</span></span>

<span data-ttu-id="fe1a8-168">**LabelPSBlue**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-168">**LabelPSBlue**</span></span>  
<span data-ttu-id="fe1a8-169">Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor azul da saída do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-169">A COM string containing the name of the label associated with the blue color component of the pixel shader output.</span></span>

<span data-ttu-id="fe1a8-170">**LabelPSAlpha**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-170">**LabelPSAlpha**</span></span>  
<span data-ttu-id="fe1a8-171">Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor alfa da saída do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-171">A COM string containing the name of the label associated with the alpha color component of the pixel shader output.</span></span>

<span data-ttu-id="fe1a8-172">**pixelKillReason**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-172">**pixelKillReason**</span></span>  
<span data-ttu-id="fe1a8-173">Saída do sombreador de pixel: motivo pelo qual a saída de pixel foi eliminada.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-173">Pixel shader output: reason the pixel output was killed.</span></span>

<span data-ttu-id="fe1a8-174">**pixelOccluded**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-174">**pixelOccluded**</span></span>  
<span data-ttu-id="fe1a8-175">true se o pixel for obstruído; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-175">true if the pixel is occluded; otherwise, false.</span></span>

<span data-ttu-id="fe1a8-176">**fbRed**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-176">**fbRed**</span></span>  
<span data-ttu-id="fe1a8-177">Framebuffer: valor do componente de cor vermelha de framebuffer antes da saída do sombreador de pixel ser mesclada.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-177">Framebuffer: value of red color component of framebuffer before pixel shader output is merged.</span></span>

<span data-ttu-id="fe1a8-178">**fbGreen**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-178">**fbGreen**</span></span>  
<span data-ttu-id="fe1a8-179">Framebuffer: valor do componente de cor verde de framebuffer antes da saída do sombreador de pixel ser mesclada.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-179">Framebuffer: value of green color component of framebuffer before pixel shader output is merged.</span></span>

<span data-ttu-id="fe1a8-180">**fbBlue**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-180">**fbBlue**</span></span>  
<span data-ttu-id="fe1a8-181">Framebuffer: valor do componente de cor azul de framebuffer antes da saída do sombreador de pixel ser mesclada.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-181">Framebuffer: value of blue color component of framebuffer before pixel shader output is merged.</span></span>

<span data-ttu-id="fe1a8-182">**fbAlpha**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-182">**fbAlpha**</span></span>  
<span data-ttu-id="fe1a8-183">Framebuffer: valor do componente de cor alfa de framebuffer antes da saída do sombreador de pixel ser mesclada.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-183">Framebuffer: value of alpha color component of framebuffer before pixel shader output is merged.</span></span>

<span data-ttu-id="fe1a8-184">**LabelFBRed**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-184">**LabelFBRed**</span></span>  
<span data-ttu-id="fe1a8-185">Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor vermelha do framebuffer.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-185">A COM string containing the name of the label associated with the red color component of the framebuffer.</span></span>

<span data-ttu-id="fe1a8-186">**LabelFBGreen**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-186">**LabelFBGreen**</span></span>  
<span data-ttu-id="fe1a8-187">Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor verde do framebuffer.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-187">A COM string containing the name of the label associated with the green color component of the framebuffer.</span></span>

<span data-ttu-id="fe1a8-188">**LabelFBBlue**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-188">**LabelFBBlue**</span></span>  
<span data-ttu-id="fe1a8-189">Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor azul do framebuffer.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-189">A COM string containing the name of the label associated with the blue color component of the framebuffer.</span></span>

<span data-ttu-id="fe1a8-190">**LabelFBAlpha**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-190">**LabelFBAlpha**</span></span>  
<span data-ttu-id="fe1a8-191">Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor alfa do framebuffer.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-191">A COM string containing the name of the label associated with the alpha color component of the framebuffer.</span></span>

<span data-ttu-id="fe1a8-192">**visualização**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-192">**topology**</span></span>  
<span data-ttu-id="fe1a8-193">A topologia de vértice das chamadas de desenho (lista de triângulo, faixa de triângulo, etc.).</span><span class="sxs-lookup"><span data-stu-id="fe1a8-193">The vertex topology of the draw calls (triangle list, triangle strip, etc).</span></span>

<span data-ttu-id="fe1a8-194">**vértices**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-194">**vertices**</span></span>  
<span data-ttu-id="fe1a8-195">Uma cadeia de caracteres COM que contém o buffer de vértice começando nesse primitivo.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-195">A COM string containing the vertex buffer starting at this primitive.</span></span> <span data-ttu-id="fe1a8-196">O buffer de vértice segue o formato de layout de entrada especificado no estágio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-196">The vertex buffer follows the input layout format specified in the pipeline stage.</span></span>

<span data-ttu-id="fe1a8-197">**vertexSize**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-197">**vertexSize**</span></span>  
<span data-ttu-id="fe1a8-198">O tamanho de um único vértice em bytes.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-198">The size of a single vertex in bytes.</span></span>

<span data-ttu-id="fe1a8-199">**InputLayout**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-199">**InputLayout**</span></span>  
<span data-ttu-id="fe1a8-200">Uma cadeia de caracteres COM que contém uma sequência de estruturas InputLayoutStruct associadas à chamada de desenho.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-200">A COM string containing a sequence of InputLayoutStruct structures associated with the draw call.</span></span>

<span data-ttu-id="fe1a8-201">**Resultado**</span><span class="sxs-lookup"><span data-stu-id="fe1a8-201">**HResult**</span></span>  
<span data-ttu-id="fe1a8-202">O DirectX HRESULT.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-202">The DirectX Hresult.</span></span> <span data-ttu-id="fe1a8-203">No caso de um problema, isso pode ser usado para exibir o erro.</span><span class="sxs-lookup"><span data-stu-id="fe1a8-203">In the event of a problem this can be used to display the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe1a8-204">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe1a8-204">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="fe1a8-205">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fe1a8-205">Header</span></span></p></td><td><span data-ttu-id="fe1a8-206">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="fe1a8-206">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



