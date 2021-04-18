---
description: Um bloco de estado pode ser usado para capturar somente o estado de vértice (consulte estado de salvamento e restauração de blocos de estado (Direct3D 9)).
ms.assetid: cb898228-dc45-4a2a-a82e-8d64523e9b85
title: Salvando Estados de vértice com um StateBlock (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81c6bc7fd291a2609ef60709f05a04fe8d27f8eb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105796068"
---
# <a name="saving-vertex-states-with-a-stateblock-direct3d-9"></a><span data-ttu-id="f53ee-103">Salvando Estados de vértice com um StateBlock (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f53ee-103">Saving Vertex States With a StateBlock (Direct3D 9)</span></span>

<span data-ttu-id="f53ee-104">Um bloco de estado pode ser usado para capturar somente o estado de vértice (consulte [estado de salvamento e restauração de blocos de estado (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="f53ee-104">A state block can be used to capture only vertex state (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span> <span data-ttu-id="f53ee-105">O estado a seguir é o estado do vértice:</span><span class="sxs-lookup"><span data-stu-id="f53ee-105">The following state is vertex state:</span></span>

-   <span data-ttu-id="f53ee-106">Estado de renderização de vértice (consulte [pipeline de vértice: renderizar estado](#vertex-pipeline-render-state)).</span><span class="sxs-lookup"><span data-stu-id="f53ee-106">Vertex render state (see [Vertex Pipeline: Render State](#vertex-pipeline-render-state)).</span></span>
-   <span data-ttu-id="f53ee-107">Estado de amostra de vértice (consulte [pipeline de vértice: estado de amostra](#vertex-pipeline-sampler-state)).</span><span class="sxs-lookup"><span data-stu-id="f53ee-107">Vertex sampler state (see [Vertex Pipeline: Sampler State](#vertex-pipeline-sampler-state)).</span></span>
-   <span data-ttu-id="f53ee-108">Estado de textura de vértice (consulte [pipeline de vértice: estado de textura](#vertex-pipeline-texture-state)).</span><span class="sxs-lookup"><span data-stu-id="f53ee-108">Vertex texture state (see [Vertex Pipeline: Texture State](#vertex-pipeline-texture-state)).</span></span>
-   <span data-ttu-id="f53ee-109">Os segmentos do modo NPatch de [**IDirect3DDevice9:: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span><span class="sxs-lookup"><span data-stu-id="f53ee-109">The NPatch mode segments from [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span></span>
-   <span data-ttu-id="f53ee-110">Cada luz de [**IDirect3DDevice9:: SetLight**](/windows/desktop/api), bem como se a luz está habilitada com [**IDirect3DDevice9:: clarear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span><span class="sxs-lookup"><span data-stu-id="f53ee-110">Each light from [**IDirect3DDevice9::SetLight**](/windows/desktop/api), as well as whether or not the light is enabled with [**IDirect3DDevice9::LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span></span>
-   <span data-ttu-id="f53ee-111">O sombreador de vértice atual e cada uma das constantes de sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="f53ee-111">The current vertex shader and each of the vertex shader constants.</span></span>
-   <span data-ttu-id="f53ee-112">Para cada fluxo de vértice, armazene o valor de divisor de [**IDirect3DDevice9:: SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).</span><span class="sxs-lookup"><span data-stu-id="f53ee-112">For each vertex stream, store the divider value from [**IDirect3DDevice9::SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).</span></span>
-   <span data-ttu-id="f53ee-113">A declaração de vértice atual.</span><span class="sxs-lookup"><span data-stu-id="f53ee-113">The current vertex declaration.</span></span>

<span data-ttu-id="f53ee-114">Para capturar o estado de vértice com um bloco de estado, especifique D3DSBT \_ vertexstate ao chamar [**IDirect3DDevice9:: CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).</span><span class="sxs-lookup"><span data-stu-id="f53ee-114">To capture vertex state with a state block, specify D3DSBT\_VERTEXSTATE when calling [**IDirect3DDevice9::CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).</span></span>

## <a name="vertex-pipeline-render-state"></a><span data-ttu-id="f53ee-115">Pipeline de vértice: estado de renderização</span><span class="sxs-lookup"><span data-stu-id="f53ee-115">Vertex Pipeline: Render State</span></span>

<span data-ttu-id="f53ee-116">Os Estados de renderização do dispositivo afetam o comportamento de quase todas as partes do pipeline.</span><span class="sxs-lookup"><span data-stu-id="f53ee-116">Device render states affect the behavior of almost every part of the pipeline.</span></span> <span data-ttu-id="f53ee-117">Os Estados de renderização são definidos chamando [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span><span class="sxs-lookup"><span data-stu-id="f53ee-117">Render states are set by calling [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span></span>

<span data-ttu-id="f53ee-118">A tabela a seguir inclui todos os Estados de renderização que configuram o estado de vértice:</span><span class="sxs-lookup"><span data-stu-id="f53ee-118">The following table includes all render states that set-up vertex state:</span></span>



| <span data-ttu-id="f53ee-119">Processar Estados</span><span class="sxs-lookup"><span data-stu-id="f53ee-119">Render States</span></span>                           | <span data-ttu-id="f53ee-120">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="f53ee-120">Default Value</span></span>          |
|-----------------------------------------|------------------------|
| <span data-ttu-id="f53ee-121">D3DRS de \_ seleção</span><span class="sxs-lookup"><span data-stu-id="f53ee-121">D3DRS\_CULLMODE</span></span>                         | <span data-ttu-id="f53ee-122">\_CCW D3DCULL</span><span class="sxs-lookup"><span data-stu-id="f53ee-122">D3DCULL\_CCW</span></span>           |
| <span data-ttu-id="f53ee-123">D3DRS \_ FOGCOLOR</span><span class="sxs-lookup"><span data-stu-id="f53ee-123">D3DRS\_FOGCOLOR</span></span>                         | <span data-ttu-id="f53ee-124">0</span><span class="sxs-lookup"><span data-stu-id="f53ee-124">0</span></span>                      |
| <span data-ttu-id="f53ee-125">D3DRS \_ FOGTABLEMODE</span><span class="sxs-lookup"><span data-stu-id="f53ee-125">D3DRS\_FOGTABLEMODE</span></span>                     | <span data-ttu-id="f53ee-126">D3DFOG \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="f53ee-126">D3DFOG\_NONE</span></span>           |
| <span data-ttu-id="f53ee-127">D3DRS \_ FOGSTART</span><span class="sxs-lookup"><span data-stu-id="f53ee-127">D3DRS\_FOGSTART</span></span>                         | <span data-ttu-id="f53ee-128">0</span><span class="sxs-lookup"><span data-stu-id="f53ee-128">0</span></span>                      |
| <span data-ttu-id="f53ee-129">D3DRS \_ FOGEND</span><span class="sxs-lookup"><span data-stu-id="f53ee-129">D3DRS\_FOGEND</span></span>                           | <span data-ttu-id="f53ee-130">1</span><span class="sxs-lookup"><span data-stu-id="f53ee-130">1</span></span>                      |
| <span data-ttu-id="f53ee-131">D3DRS \_ FOGDENSITY</span><span class="sxs-lookup"><span data-stu-id="f53ee-131">D3DRS\_FOGDENSITY</span></span>                       | <span data-ttu-id="f53ee-132">1</span><span class="sxs-lookup"><span data-stu-id="f53ee-132">1</span></span>                      |
| <span data-ttu-id="f53ee-133">D3DRS \_ RANGEFOGENABLE</span><span class="sxs-lookup"><span data-stu-id="f53ee-133">D3DRS\_RANGEFOGENABLE</span></span>                   | <span data-ttu-id="f53ee-134">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="f53ee-134">**FALSE**</span></span>              |
| <span data-ttu-id="f53ee-135">\_Ambiente D3DRS</span><span class="sxs-lookup"><span data-stu-id="f53ee-135">D3DRS\_AMBIENT</span></span>                          | <span data-ttu-id="f53ee-136">0</span><span class="sxs-lookup"><span data-stu-id="f53ee-136">0</span></span>                      |
| <span data-ttu-id="f53ee-137">D3DRS \_ COLORVERTEX</span><span class="sxs-lookup"><span data-stu-id="f53ee-137">D3DRS\_COLORVERTEX</span></span>                      | <span data-ttu-id="f53ee-138">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="f53ee-138">**TRUE**</span></span>               |
| <span data-ttu-id="f53ee-139">D3DRS \_ FOGVERTEXMODE</span><span class="sxs-lookup"><span data-stu-id="f53ee-139">D3DRS\_FOGVERTEXMODE</span></span>                    | <span data-ttu-id="f53ee-140">D3DFOG \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="f53ee-140">D3DFOG\_NONE</span></span>           |
| <span data-ttu-id="f53ee-141">Recorte de D3DRS \_</span><span class="sxs-lookup"><span data-stu-id="f53ee-141">D3DRS\_CLIPPING</span></span>                         | <span data-ttu-id="f53ee-142">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="f53ee-142">**TRUE**</span></span>               |
| <span data-ttu-id="f53ee-143">\_Iluminação D3DRS</span><span class="sxs-lookup"><span data-stu-id="f53ee-143">D3DRS\_LIGHTING</span></span>                         | <span data-ttu-id="f53ee-144">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="f53ee-144">**TRUE**</span></span>               |
| <span data-ttu-id="f53ee-145">D3DRS \_ LOCALVIEWER</span><span class="sxs-lookup"><span data-stu-id="f53ee-145">D3DRS\_LOCALVIEWER</span></span>                      | <span data-ttu-id="f53ee-146">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="f53ee-146">**TRUE**</span></span>               |
| <span data-ttu-id="f53ee-147">D3DRS \_ EMISSIVEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="f53ee-147">D3DRS\_EMISSIVEMATERIALSOURCE</span></span>           | <span data-ttu-id="f53ee-148">MATERIAL de D3DMCS \_</span><span class="sxs-lookup"><span data-stu-id="f53ee-148">D3DMCS\_MATERIAL</span></span>       |
| <span data-ttu-id="f53ee-149">D3DRS \_ AMBIENTMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="f53ee-149">D3DRS\_AMBIENTMATERIALSOURCE</span></span>            | <span data-ttu-id="f53ee-150">MATERIAL de D3DMCS \_</span><span class="sxs-lookup"><span data-stu-id="f53ee-150">D3DMCS\_MATERIAL</span></span>       |
| <span data-ttu-id="f53ee-151">D3DRS \_ DiffuseMaterialSource</span><span class="sxs-lookup"><span data-stu-id="f53ee-151">D3DRS\_DIFFUSEMATERIALSOURCE</span></span>            | <span data-ttu-id="f53ee-152">D3DMCS \_ COLOR1</span><span class="sxs-lookup"><span data-stu-id="f53ee-152">D3DMCS\_COLOR1</span></span>         |
| <span data-ttu-id="f53ee-153">D3DRS \_ SPECULARMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="f53ee-153">D3DRS\_SPECULARMATERIALSOURCE</span></span>           | <span data-ttu-id="f53ee-154">D3DMCS \_ COLOR2</span><span class="sxs-lookup"><span data-stu-id="f53ee-154">D3DMCS\_COLOR2</span></span>         |
| <span data-ttu-id="f53ee-155">D3DRS \_ VERTEXBLEND</span><span class="sxs-lookup"><span data-stu-id="f53ee-155">D3DRS\_VERTEXBLEND</span></span>                      | <span data-ttu-id="f53ee-156">D3DVBF \_ desabilitar</span><span class="sxs-lookup"><span data-stu-id="f53ee-156">D3DVBF\_DISABLE</span></span>        |
| <span data-ttu-id="f53ee-157">D3DRS \_ CLIPPLANEENABLE</span><span class="sxs-lookup"><span data-stu-id="f53ee-157">D3DRS\_CLIPPLANEENABLE</span></span>                  | <span data-ttu-id="f53ee-158">0</span><span class="sxs-lookup"><span data-stu-id="f53ee-158">0</span></span>                      |
| <span data-ttu-id="f53ee-159">Pontos de D3DRS \_</span><span class="sxs-lookup"><span data-stu-id="f53ee-159">D3DRS\_POINTSIZE</span></span>                        | <span data-ttu-id="f53ee-160">Dependente do driver</span><span class="sxs-lookup"><span data-stu-id="f53ee-160">Driver dependent</span></span>       |
| <span data-ttu-id="f53ee-161">D3DRS \_ pontos \_ mínimos</span><span class="sxs-lookup"><span data-stu-id="f53ee-161">D3DRS\_POINTSIZE\_MIN</span></span>                   | <span data-ttu-id="f53ee-162">1</span><span class="sxs-lookup"><span data-stu-id="f53ee-162">1</span></span>                      |
| <span data-ttu-id="f53ee-163">D3DRS \_ POINTSPRITEENABLE</span><span class="sxs-lookup"><span data-stu-id="f53ee-163">D3DRS\_POINTSPRITEENABLE</span></span>                | <span data-ttu-id="f53ee-164">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="f53ee-164">**FALSE**</span></span>              |
| <span data-ttu-id="f53ee-165">D3DRS \_ POINTSCALEENABLE</span><span class="sxs-lookup"><span data-stu-id="f53ee-165">D3DRS\_POINTSCALEENABLE</span></span>                 | <span data-ttu-id="f53ee-166">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="f53ee-166">**FALSE**</span></span>              |
| <span data-ttu-id="f53ee-167">D3DRS \_ POINTSCALE \_ A</span><span class="sxs-lookup"><span data-stu-id="f53ee-167">D3DRS\_POINTSCALE\_A</span></span>                    | <span data-ttu-id="f53ee-168">1</span><span class="sxs-lookup"><span data-stu-id="f53ee-168">1</span></span>                      |
| <span data-ttu-id="f53ee-169">D3DRS \_ POINTSCALE \_ B</span><span class="sxs-lookup"><span data-stu-id="f53ee-169">D3DRS\_POINTSCALE\_B</span></span>                    | <span data-ttu-id="f53ee-170">0</span><span class="sxs-lookup"><span data-stu-id="f53ee-170">0</span></span>                      |
| <span data-ttu-id="f53ee-171">D3DRS \_ POINTSCALE \_ C</span><span class="sxs-lookup"><span data-stu-id="f53ee-171">D3DRS\_POINTSCALE\_C</span></span>                    | <span data-ttu-id="f53ee-172">0</span><span class="sxs-lookup"><span data-stu-id="f53ee-172">0</span></span>                      |
| <span data-ttu-id="f53ee-173">D3DRS \_ MULTISAMPLEANTIALIAS</span><span class="sxs-lookup"><span data-stu-id="f53ee-173">D3DRS\_MULTISAMPLEANTIALIAS</span></span>             | <span data-ttu-id="f53ee-174">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="f53ee-174">**TRUE**</span></span>               |
| <span data-ttu-id="f53ee-175">D3DRS \_ MULTISAMPLEMASK</span><span class="sxs-lookup"><span data-stu-id="f53ee-175">D3DRS\_MULTISAMPLEMASK</span></span>                  | <span data-ttu-id="f53ee-176">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="f53ee-176">0xffffffff</span></span>             |
| <span data-ttu-id="f53ee-177">D3DRS \_ PATCHEDGESTYLE</span><span class="sxs-lookup"><span data-stu-id="f53ee-177">D3DRS\_PATCHEDGESTYLE</span></span>                   | <span data-ttu-id="f53ee-178">D3DPATCHEDGE \_ discreto</span><span class="sxs-lookup"><span data-stu-id="f53ee-178">D3DPATCHEDGE\_DISCRETE</span></span> |
| <span data-ttu-id="f53ee-179">D3DRS \_ pontos \_ máximos</span><span class="sxs-lookup"><span data-stu-id="f53ee-179">D3DRS\_POINTSIZE\_MAX</span></span>                   | <span data-ttu-id="f53ee-180">1</span><span class="sxs-lookup"><span data-stu-id="f53ee-180">1</span></span>                      |
| <span data-ttu-id="f53ee-181">D3DRS \_ INDEXEDVERTEXBLENDENABLE</span><span class="sxs-lookup"><span data-stu-id="f53ee-181">D3DRS\_INDEXEDVERTEXBLENDENABLE</span></span>         | <span data-ttu-id="f53ee-182">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="f53ee-182">**FALSE**</span></span>              |
| <span data-ttu-id="f53ee-183">D3DRS \_ TWEENFACTOR</span><span class="sxs-lookup"><span data-stu-id="f53ee-183">D3DRS\_TWEENFACTOR</span></span>                      | <span data-ttu-id="f53ee-184">0</span><span class="sxs-lookup"><span data-stu-id="f53ee-184">0</span></span>                      |
| <span data-ttu-id="f53ee-185">D3DRS \_ POSITIONDEGREE</span><span class="sxs-lookup"><span data-stu-id="f53ee-185">D3DRS\_POSITIONDEGREE</span></span>                   | <span data-ttu-id="f53ee-186">D3DDEGREE \_ cúbico</span><span class="sxs-lookup"><span data-stu-id="f53ee-186">D3DDEGREE\_CUBIC</span></span>       |
| <span data-ttu-id="f53ee-187">D3DRS \_ NORMALDEGREE</span><span class="sxs-lookup"><span data-stu-id="f53ee-187">D3DRS\_NORMALDEGREE</span></span>                     | <span data-ttu-id="f53ee-188">D3DDEGREE \_ linear</span><span class="sxs-lookup"><span data-stu-id="f53ee-188">D3DDEGREE\_LINEAR</span></span>      |
| <span data-ttu-id="f53ee-189">D3DRS \_ MINTESSELLATIONLEVEL</span><span class="sxs-lookup"><span data-stu-id="f53ee-189">D3DRS\_MINTESSELLATIONLEVEL</span></span>             | <span data-ttu-id="f53ee-190">1</span><span class="sxs-lookup"><span data-stu-id="f53ee-190">1</span></span>                      |
| <span data-ttu-id="f53ee-191">D3DRS \_ MAXTESSELLATIONLEVEL</span><span class="sxs-lookup"><span data-stu-id="f53ee-191">D3DRS\_MAXTESSELLATIONLEVEL</span></span>             | <span data-ttu-id="f53ee-192">1</span><span class="sxs-lookup"><span data-stu-id="f53ee-192">1</span></span>                      |
| <span data-ttu-id="f53ee-193">D3DRS \_ ADAPTIVETESS \_ X</span><span class="sxs-lookup"><span data-stu-id="f53ee-193">D3DRS\_ADAPTIVETESS\_X</span></span>                  | <span data-ttu-id="f53ee-194">0</span><span class="sxs-lookup"><span data-stu-id="f53ee-194">0</span></span>                      |
| <span data-ttu-id="f53ee-195">D3DRS \_ ADAPTIVETESS \_ Y</span><span class="sxs-lookup"><span data-stu-id="f53ee-195">D3DRS\_ADAPTIVETESS\_Y</span></span>                  | <span data-ttu-id="f53ee-196">0</span><span class="sxs-lookup"><span data-stu-id="f53ee-196">0</span></span>                      |
| <span data-ttu-id="f53ee-197">D3DRS \_ ADAPTIVETESS \_ Z</span><span class="sxs-lookup"><span data-stu-id="f53ee-197">D3DRS\_ADAPTIVETESS\_Z</span></span>                  | <span data-ttu-id="f53ee-198">1</span><span class="sxs-lookup"><span data-stu-id="f53ee-198">1</span></span>                      |
| <span data-ttu-id="f53ee-199">D3DRS \_ ADAPTIVETESS \_ W</span><span class="sxs-lookup"><span data-stu-id="f53ee-199">D3DRS\_ADAPTIVETESS\_W</span></span>                  | <span data-ttu-id="f53ee-200">0</span><span class="sxs-lookup"><span data-stu-id="f53ee-200">0</span></span>                      |
| <span data-ttu-id="f53ee-201">D3DRS \_ ENABLEADAPTIVETESSELLATION "/></span><span class="sxs-lookup"><span data-stu-id="f53ee-201">D3DRS\_ENABLEADAPTIVETESSELLATION"/></span></span> | <span data-ttu-id="f53ee-202">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="f53ee-202">**FALSE**</span></span>              |



 

## <a name="vertex-pipeline-sampler-state"></a><span data-ttu-id="f53ee-203">Pipeline de vértice: estado de amostra</span><span class="sxs-lookup"><span data-stu-id="f53ee-203">Vertex Pipeline: Sampler State</span></span>

<span data-ttu-id="f53ee-204">Os Estados de amostra controlam tópicos relacionados à amostragem, como filtragem, divisão e modos de endereço de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="f53ee-204">Sampler states control sampling related topics such as filtering, tiling, and texture coordinate address modes.</span></span> <span data-ttu-id="f53ee-205">Use [**IDirect3DDevice9:: Setamostrastate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) para configurar o estado de amostra (incluindo aquele usado na unidade Tessellator para mapas de deslocamento de exemplo).</span><span class="sxs-lookup"><span data-stu-id="f53ee-205">Use [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) to set up the sampler state (including the one used in the tessellator unit to sample displacement maps).</span></span> <span data-ttu-id="f53ee-206">Os Estados de amostra foram renomeados com um prefixo "D3DSAMP \_ " para habilitar a detecção de erros de tempo de compilação ao portar do DirectX 8.</span><span class="sxs-lookup"><span data-stu-id="f53ee-206">The sampler states have been renamed with a "D3DSAMP\_" prefix to enable compile time error detection when porting from DirectX 8.</span></span>

<span data-ttu-id="f53ee-207">A tabela a seguir inclui todos os Estados de amostra que definem o estado do vértice:</span><span class="sxs-lookup"><span data-stu-id="f53ee-207">The following table includes all sampler states that set-up vertex state:</span></span>



| <span data-ttu-id="f53ee-208">Estados de amostra</span><span class="sxs-lookup"><span data-stu-id="f53ee-208">Sampler States</span></span>      | <span data-ttu-id="f53ee-209">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="f53ee-209">Default Value</span></span> |
|---------------------|---------------|
| <span data-ttu-id="f53ee-210">D3DSAMP \_ DMAPOFFSET</span><span class="sxs-lookup"><span data-stu-id="f53ee-210">D3DSAMP\_DMAPOFFSET</span></span> | <span data-ttu-id="f53ee-211">256</span><span class="sxs-lookup"><span data-stu-id="f53ee-211">256</span></span>           |



 

## <a name="vertex-pipeline-texture-state"></a><span data-ttu-id="f53ee-212">Pipeline de vértice: estado de textura</span><span class="sxs-lookup"><span data-stu-id="f53ee-212">Vertex Pipeline: Texture State</span></span>

<span data-ttu-id="f53ee-213">Os Estados de textura controlam as operações de mesclagem de textura do misturador de várias texturas.</span><span class="sxs-lookup"><span data-stu-id="f53ee-213">Texture states control texture blending operations of the multi-texture blender.</span></span> <span data-ttu-id="f53ee-214">Use [**IDirect3DDevice9:: SetTextureStageState**](/windows/desktop/api) para configurar Estados de textura.</span><span class="sxs-lookup"><span data-stu-id="f53ee-214">Use [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api) to set-up texture states.</span></span> <span data-ttu-id="f53ee-215">Use [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) para associar uma textura a um estágio de amostra.</span><span class="sxs-lookup"><span data-stu-id="f53ee-215">Use [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) to associate a texture with a sampler stage.</span></span>

<span data-ttu-id="f53ee-216">A tabela a seguir inclui todos os Estados de textura que configuram o estado de vértice:</span><span class="sxs-lookup"><span data-stu-id="f53ee-216">The following table includes all the texture states that set-up vertex state:</span></span>



| <span data-ttu-id="f53ee-217">Estados de textura</span><span class="sxs-lookup"><span data-stu-id="f53ee-217">Texture States</span></span>                | <span data-ttu-id="f53ee-218">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="f53ee-218">Default Value</span></span>    |
|-------------------------------|------------------|
| <span data-ttu-id="f53ee-219">D3DTSS \_ TEXCOORDINDEX</span><span class="sxs-lookup"><span data-stu-id="f53ee-219">D3DTSS\_TEXCOORDINDEX</span></span>         | <span data-ttu-id="f53ee-220">0</span><span class="sxs-lookup"><span data-stu-id="f53ee-220">0</span></span>                |
| <span data-ttu-id="f53ee-221">D3DTSS \_ TEXTURETRANSFORMFLAGS</span><span class="sxs-lookup"><span data-stu-id="f53ee-221">D3DTSS\_TEXTURETRANSFORMFLAGS</span></span> | <span data-ttu-id="f53ee-222">D3DTTFF \_ desabilitar</span><span class="sxs-lookup"><span data-stu-id="f53ee-222">D3DTTFF\_DISABLE</span></span> |



 

<span data-ttu-id="f53ee-223">D3DTSS \_ TEXCOORDINDEX é um estado de processamento de vértice de função fixo.</span><span class="sxs-lookup"><span data-stu-id="f53ee-223">D3DTSS\_TEXCOORDINDEX is a fixed function vertex processing state.</span></span> <span data-ttu-id="f53ee-224">Se um sombreador de vértice programável for usado, esse Estado será ignorado.</span><span class="sxs-lookup"><span data-stu-id="f53ee-224">If a programmable vertex shader is used, this state is ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f53ee-225">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f53ee-225">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f53ee-226">Estado de salvamento e restauração de blocos de estado</span><span class="sxs-lookup"><span data-stu-id="f53ee-226">State Blocks Save and Restore State</span></span>](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
