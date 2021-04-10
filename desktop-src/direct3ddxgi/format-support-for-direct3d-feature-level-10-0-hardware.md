---
description: Esta seção especifica os formatos ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valores) que têm suporte no hardware do nível de recurso do Direct3D 10,0.
ms.assetid: 3C1CCA7D-9F2F-4B1B-8424-BA9C6DED4974
title: Suporte de formato para hardware 10.0 do Nível de Recursos do Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f298460330feb2143b20da37ae82c3a6d63790
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163733"
---
# <a name="format-support-for-direct3d-feature-level-100-hardware"></a><span data-ttu-id="5baf9-103">Suporte de formato para hardware 10.0 do Nível de Recursos do Direct3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-103">Format support for Direct3D Feature Level 10.0 hardware</span></span>

<span data-ttu-id="5baf9-104">Esta seção especifica os formatos ([_\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valores) que têm suporte no hardware do nível de recurso do Direct3D 10,0.</span><span class="sxs-lookup"><span data-stu-id="5baf9-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature Level 10.0 hardware.</span></span>

<span data-ttu-id="5baf9-105">A tabela resume o suporte a recursos, usando a chave a seguir.</span><span class="sxs-lookup"><span data-stu-id="5baf9-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="5baf9-106">Símbolo</span><span class="sxs-lookup"><span data-stu-id="5baf9-106">Symbol</span></span>                            | <span data-ttu-id="5baf9-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="5baf9-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="5baf9-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="5baf9-108">_ *-*\*</span></span>                             | <span data-ttu-id="5baf9-109">Não permitido ou não disponível.</span><span class="sxs-lookup"><span data-stu-id="5baf9-109">Disallowed or not available.</span></span>                                                  |
| ![exigido](images/letter-r.jpg)  | <span data-ttu-id="5baf9-111">O suporte a hardware é necessário.</span><span class="sxs-lookup"><span data-stu-id="5baf9-111">Hardware support is required.</span></span>                                                 |
| ![opcionais](images/letter-o.jpg)  | <span data-ttu-id="5baf9-113">Suporte a hardware opcional, o formato pode ou não ser acelerado por hardware.</span><span class="sxs-lookup"><span data-stu-id="5baf9-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![dependentes](images/letter-d.jpg) | <span data-ttu-id="5baf9-115">Necessário se houver suporte para o recurso opcional relacionado.</span><span class="sxs-lookup"><span data-stu-id="5baf9-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="5baf9-116">Este tópico contém uma seção por formato.</span><span class="sxs-lookup"><span data-stu-id="5baf9-116">This topic contains a section per format.</span></span> <span data-ttu-id="5baf9-117">Um *destino* de formato (as tabelas contêm uma linha por destino) pode ser um tipo de recurso, uma função intrínseca HLSL ou uma funcionalidade específica que depende de um formato específico.</span><span class="sxs-lookup"><span data-stu-id="5baf9-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="5baf9-118">Para verificar programaticamente o suporte a Format em D3D11 e D3D12, consulte [verificando o suporte a recursos de hardware](checking-hardware-feature-support.md).</span><span class="sxs-lookup"><span data-stu-id="5baf9-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="5baf9-119">Os números dos formatos são principalmente, mas nem todos, em ordem numérica crescente &mdash; alguns estão fora de ordem numérica e listados junto com outros formatos relevantes.</span><span class="sxs-lookup"><span data-stu-id="5baf9-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="5baf9-120">Observe também que sem *tipo* em um nome de formato pode significar digitação *parcial* e não estritamente tipado (consulte a seção [observações de formato](#format-notes) no final do tópico).</span><span class="sxs-lookup"><span data-stu-id="5baf9-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>
 
## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="5baf9-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span><span class="sxs-lookup"><span data-stu-id="5baf9-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="5baf9-122">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-122">Target</span></span> | <span data-ttu-id="5baf9-123">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-123">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-124">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-125">0</span><span class="sxs-lookup"><span data-stu-id="5baf9-125">0</span></span> |
| <span data-ttu-id="5baf9-126">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-126">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-128">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-128">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-130">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-130">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-131">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-131">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-132">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-132">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-133">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-134">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-134">Texture2D</span></span> | \- |
| <span data-ttu-id="5baf9-135">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-135">Texture3D</span></span> | \- |
| <span data-ttu-id="5baf9-136">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-136">TextureCube</span></span> | \- |
| <span data-ttu-id="5baf9-137">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-137">Shader ld</span></span> | \- |
| <span data-ttu-id="5baf9-138">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-138">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-139">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-139">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-140">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-140">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-141">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-141">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-142">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-142">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-143">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-143">Mipmap</span></span> | \- |
| <span data-ttu-id="5baf9-144">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-144">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-145">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-145">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-146">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-146">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-147">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-147">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-148">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-148">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-149">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-149">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-150">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-150">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-151">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-151">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-152">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-152">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-153">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-153">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-154">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-154">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-155">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-155">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-156">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-156">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-157">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-157">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-158">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-158">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-159">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-159">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-160">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-160">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-162">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-162">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-163">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-163">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-164">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-164">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-165">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-165">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-166">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-166">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-167">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-167">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-168">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-168">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="5baf9-169">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-169">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-170">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-170">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-171">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-171">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-172">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-172">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-173">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-173">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="5baf9-174">DXGI_FORMAT_R32G32B32A32 \_ <sup>PCs</sup> não tipados (1)</span><span class="sxs-lookup"><span data-stu-id="5baf9-174">DXGI_FORMAT_R32G32B32A32\_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="5baf9-175">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-175">Target</span></span> | <span data-ttu-id="5baf9-176">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-176">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-177">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-177">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-178">128</span><span class="sxs-lookup"><span data-stu-id="5baf9-178">128</span></span> |
| <span data-ttu-id="5baf9-179">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-179">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-181">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-181">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-182">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-182">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-183">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-183">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-184">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-184">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-185">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-185">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-187">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-187">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-189">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-189">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-191">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-191">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-193">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-193">Shader ld</span></span> | \- |
| <span data-ttu-id="5baf9-194">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-194">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-195">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-195">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-196">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-196">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-197">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-197">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-198">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-198">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-199">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-199">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-201">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-201">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-202">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-202">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-203">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-203">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-204">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-204">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-205">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-205">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-206">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-206">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-207">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-207">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-208">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-208">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-209">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-209">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-210">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-210">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-211">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-211">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-212">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-212">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-213">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-213">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-214">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-214">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-215">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-215">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-216">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-216">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-217">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-217">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-219">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-219">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-220">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-220">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-221">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-221">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-222">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-222">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-223">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-223">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-224">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-224">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-225">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-225">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-227">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-227">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-228">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-228">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-229">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-229">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-230">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-230">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-232">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-232">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfcssup-2"></a><span data-ttu-id="5baf9-233">\_<sup>FCS</sup> de DXGI_FORMAT_R32G32B32A32 float (2)</span><span class="sxs-lookup"><span data-stu-id="5baf9-233">DXGI_FORMAT_R32G32B32A32\_FLOAT<sup>FCS</sup> (2)</span></span>
| <span data-ttu-id="5baf9-234">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-234">Target</span></span> | <span data-ttu-id="5baf9-235">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-235">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-236">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-236">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-237">128</span><span class="sxs-lookup"><span data-stu-id="5baf9-237">128</span></span> |
| <span data-ttu-id="5baf9-238">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-238">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-240">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-240">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-242">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-242">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-244">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-244">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-245">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-245">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-247">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-247">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-249">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-249">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-251">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-251">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-253">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-253">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-255">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-255">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-257">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-257">Shader sample (any filter)</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-259">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-259">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-260">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-260">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-261">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-261">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-262">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-262">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-263">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-263">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-265">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-265">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-267">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-267">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-269">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-269">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-271">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-271">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-272">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-272">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-273">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-273">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-274">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-274">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-275">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-275">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-276">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-276">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-277">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-277">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-278">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-278">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-279">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-279">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-280">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-280">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-281">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-281">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-282">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-282">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-283">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-283">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-284">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-284">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-286">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-286">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-288">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-288">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-290">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-290">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-292">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-292">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-294">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-294">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-296">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-296">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-297">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-297">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-299">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-299">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-300">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-300">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-301">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-301">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-302">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-302">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-304">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-304">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfcssup-3"></a><span data-ttu-id="5baf9-305">\_<sup>FCS</sup> DXGI_FORMAT_R32G32B32A32 uint (3)</span><span class="sxs-lookup"><span data-stu-id="5baf9-305">DXGI_FORMAT_R32G32B32A32\_UINT<sup>FCS</sup> (3)</span></span>
| <span data-ttu-id="5baf9-306">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-306">Target</span></span> | <span data-ttu-id="5baf9-307">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-307">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-308">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-308">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-309">128</span><span class="sxs-lookup"><span data-stu-id="5baf9-309">128</span></span> |
| <span data-ttu-id="5baf9-310">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-310">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-312">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-312">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-314">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-314">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-316">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-316">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-317">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-317">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-319">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-319">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-321">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-321">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-323">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-323">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-325">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-325">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-327">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-327">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-329">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-329">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-330">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-330">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-331">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-331">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-332">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-332">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-333">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-333">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-334">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-334">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-336">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-336">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-337">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-337">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-339">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-339">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-340">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-340">Output Merger Logic Op</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-342">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-342">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-343">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-343">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-344">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-344">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-345">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-345">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-346">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-346">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-347">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-347">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-348">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-348">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-349">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-349">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-350">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-350">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-351">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-351">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-352">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-352">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-353">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-353">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-354">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-354">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-356">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-356">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-358">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-358">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-360">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-360">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-362">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-362">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-363">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-363">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-365">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-365">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-366">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-366">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-368">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-368">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-369">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-369">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-370">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-370">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-371">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-371">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-373">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-373">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfcssup-4"></a><span data-ttu-id="5baf9-374">DXGI_FORMAT_R32G32B32A32 \_ Santo<sup>FCS</sup> (4)</span><span class="sxs-lookup"><span data-stu-id="5baf9-374">DXGI_FORMAT_R32G32B32A32\_SINT<sup>FCS</sup> (4)</span></span>
| <span data-ttu-id="5baf9-375">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-375">Target</span></span> | <span data-ttu-id="5baf9-376">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-376">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-377">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-377">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-378">128</span><span class="sxs-lookup"><span data-stu-id="5baf9-378">128</span></span> |
| <span data-ttu-id="5baf9-379">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-379">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-381">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-381">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-383">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-383">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-385">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-385">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-386">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-386">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-388">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-388">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-390">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-390">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-392">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-392">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-394">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-394">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-396">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-396">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-398">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-398">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-399">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-399">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-400">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-400">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-401">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-401">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-402">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-402">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-403">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-403">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-405">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-405">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-406">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-406">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-408">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-408">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-409">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-409">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-410">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-410">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-411">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-411">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-412">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-412">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-413">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-413">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-414">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-414">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-415">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-415">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-416">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-416">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-417">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-417">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-418">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-418">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-419">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-419">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-420">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-420">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-421">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-421">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-422">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-422">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-424">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-424">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-426">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-426">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-428">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-428">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-430">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-430">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-431">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-431">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-433">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-433">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-434">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-434">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-436">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-436">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-437">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-437">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-438">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-438">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-439">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-439">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-441">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-441">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="5baf9-442">DXGI_FORMAT_R32G32B32 \_ <sup>PCs</sup> não tipados (5)</span><span class="sxs-lookup"><span data-stu-id="5baf9-442">DXGI_FORMAT_R32G32B32\_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="5baf9-443">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-443">Target</span></span> | <span data-ttu-id="5baf9-444">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-444">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-445">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-445">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-446">96</span><span class="sxs-lookup"><span data-stu-id="5baf9-446">96</span></span> |
| <span data-ttu-id="5baf9-447">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-447">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-449">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-449">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-450">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-450">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-451">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-451">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-452">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-452">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-453">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-453">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-455">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-455">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-457">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-457">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-459">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-459">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-461">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-461">Shader ld</span></span> | \- |
| <span data-ttu-id="5baf9-462">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-462">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-463">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-463">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-464">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-464">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-465">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-465">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-466">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-466">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-467">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-467">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-469">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-469">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-470">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-470">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-471">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-471">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-472">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-472">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-473">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-473">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-474">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-474">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-475">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-475">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-476">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-476">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-477">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-477">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-478">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-478">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-479">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-479">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-480">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-480">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-481">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-481">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-482">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-482">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-483">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-483">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-484">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-484">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-485">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-485">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-487">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-487">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-488">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-488">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-489">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-489">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-490">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-490">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-491">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-491">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-492">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-492">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-493">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-493">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-495">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-495">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-496">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-496">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-497">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-497">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-498">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-498">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-499">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-499">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfcssup-6"></a><span data-ttu-id="5baf9-500">\_<sup>FCS</sup> de DXGI_FORMAT_R32G32B32 float (6)</span><span class="sxs-lookup"><span data-stu-id="5baf9-500">DXGI_FORMAT_R32G32B32\_FLOAT<sup>FCS</sup> (6)</span></span>
| <span data-ttu-id="5baf9-501">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-501">Target</span></span> | <span data-ttu-id="5baf9-502">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-502">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-503">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-503">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-504">96</span><span class="sxs-lookup"><span data-stu-id="5baf9-504">96</span></span> |
| <span data-ttu-id="5baf9-505">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-505">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-507">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-507">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-509">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-509">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-511">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-511">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-512">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-512">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-514">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-514">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-516">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-516">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-518">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-518">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-520">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-520">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-522">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-522">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-524">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-524">Shader sample (any filter)</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-526">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-526">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-527">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-527">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-528">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-528">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-529">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-529">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-530">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-530">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-532">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-532">Mipmap Auto-Generation</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-534">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-534">RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-536">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-536">Blendable RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="5baf9-538">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-538">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-539">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-539">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-540">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-540">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-541">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-541">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-542">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-542">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-543">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-543">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-544">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-544">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-545">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-545">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-546">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-546">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-547">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-547">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-548">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-548">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-549">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-549">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-550">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-550">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-551">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-551">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-553">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-553">4x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="5baf9-555">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-555">8x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="5baf9-557">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-557">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-559">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-559">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-561">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-561">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-563">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-563">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-564">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-564">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-566">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-566">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-567">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-567">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-568">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-568">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-569">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-569">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-570">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-570">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfcssup-7"></a><span data-ttu-id="5baf9-571">\_<sup>FCS</sup> DXGI_FORMAT_R32G32B32 uint (7)</span><span class="sxs-lookup"><span data-stu-id="5baf9-571">DXGI_FORMAT_R32G32B32\_UINT<sup>FCS</sup> (7)</span></span>
| <span data-ttu-id="5baf9-572">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-572">Target</span></span> | <span data-ttu-id="5baf9-573">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-573">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-574">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-574">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-575">96</span><span class="sxs-lookup"><span data-stu-id="5baf9-575">96</span></span> |
| <span data-ttu-id="5baf9-576">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-576">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-578">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-578">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-580">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-580">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-582">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-582">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-583">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-583">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-585">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-585">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-587">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-587">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-589">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-589">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-591">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-591">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-593">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-593">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-595">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-595">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-596">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-596">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-597">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-597">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-598">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-598">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-599">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-599">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-600">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-600">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-602">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-602">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-603">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-603">RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-605">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-605">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-606">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-606">Output Merger Logic Op</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-608">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-608">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-609">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-609">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-610">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-610">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-611">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-611">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-612">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-612">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-613">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-613">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-614">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-614">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-615">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-615">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-616">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-616">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-617">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-617">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-618">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-618">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-619">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-619">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-620">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-620">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-622">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-622">4x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="5baf9-624">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-624">8x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="5baf9-626">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-626">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-628">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-628">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-629">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-629">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-631">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-631">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-632">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-632">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-634">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-634">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-635">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-635">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-636">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-636">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-637">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-637">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-638">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-638">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfcssup-8"></a><span data-ttu-id="5baf9-639">DXGI_FORMAT_R32G32B32 \_ Santo<sup>FCS</sup> (8)</span><span class="sxs-lookup"><span data-stu-id="5baf9-639">DXGI_FORMAT_R32G32B32\_SINT<sup>FCS</sup> (8)</span></span>
| <span data-ttu-id="5baf9-640">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-640">Target</span></span> | <span data-ttu-id="5baf9-641">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-641">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-642">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-642">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-643">96</span><span class="sxs-lookup"><span data-stu-id="5baf9-643">96</span></span> |
| <span data-ttu-id="5baf9-644">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-644">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-646">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-646">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-648">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-648">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-650">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-650">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-651">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-651">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-653">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-653">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-655">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-655">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-657">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-657">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-659">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-659">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-661">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-661">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-663">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-663">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-664">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-664">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-665">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-665">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-666">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-666">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-667">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-667">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-668">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-668">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-670">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-670">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-671">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-671">RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-673">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-673">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-674">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-674">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-675">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-675">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-676">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-676">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-677">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-677">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-678">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-678">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-679">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-679">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-680">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-680">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-681">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-681">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-682">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-682">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-683">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-683">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-684">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-684">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-685">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-685">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-686">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-686">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-687">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-687">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-689">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-689">4x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="5baf9-691">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-691">8x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="5baf9-693">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-693">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-695">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-695">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-696">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-696">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-698">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-698">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-699">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-699">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-701">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-701">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-702">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-702">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-703">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-703">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-704">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-704">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-705">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-705">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="5baf9-706">DXGI_FORMAT_R16G16B16A16 \_ <sup>PCs</sup> não tipados (9)</span><span class="sxs-lookup"><span data-stu-id="5baf9-706">DXGI_FORMAT_R16G16B16A16\_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="5baf9-707">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-707">Target</span></span> | <span data-ttu-id="5baf9-708">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-708">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-709">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-709">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-710">64</span><span class="sxs-lookup"><span data-stu-id="5baf9-710">64</span></span> |
| <span data-ttu-id="5baf9-711">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-711">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-713">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-713">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-714">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-714">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-715">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-715">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-716">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-716">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-717">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-717">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-719">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-719">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-721">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-721">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-723">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-723">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-725">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-725">Shader ld</span></span> | \- |
| <span data-ttu-id="5baf9-726">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-726">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-727">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-727">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-728">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-728">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-729">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-729">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-730">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-730">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-731">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-731">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-733">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-733">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-734">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-734">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-735">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-735">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-736">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-736">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-737">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-737">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-738">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-738">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-739">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-739">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-740">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-740">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-741">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-741">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-742">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-742">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-743">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-743">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-744">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-744">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-745">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-745">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-746">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-746">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-747">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-747">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-748">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-748">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-749">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-749">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-751">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-751">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-752">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-752">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-753">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-753">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-754">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-754">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-755">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-755">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-756">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-756">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-757">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-757">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-759">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-759">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-760">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-760">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-761">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-761">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-762">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-762">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-764">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-764">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfcssup-10"></a><span data-ttu-id="5baf9-765">\_<sup>FCS</sup> de DXGI_FORMAT_R16G16B16A16 float (10)</span><span class="sxs-lookup"><span data-stu-id="5baf9-765">DXGI_FORMAT_R16G16B16A16\_FLOAT<sup>FCS</sup> (10)</span></span>
| <span data-ttu-id="5baf9-766">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-766">Target</span></span> | <span data-ttu-id="5baf9-767">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-767">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-768">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-768">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-769">64</span><span class="sxs-lookup"><span data-stu-id="5baf9-769">64</span></span> |
| <span data-ttu-id="5baf9-770">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-770">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-772">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-772">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-774">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-774">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-776">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-776">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-777">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-777">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-778">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-778">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-780">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-780">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-782">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-782">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-784">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-784">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-786">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-786">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-788">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-788">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-790">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-790">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-791">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-791">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-792">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-792">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-793">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-793">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-794">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-794">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-796">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-796">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-798">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-798">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-800">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-800">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-802">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-802">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-803">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-803">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-804">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-804">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-805">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-805">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-806">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-806">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-807">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-807">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-808">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-808">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-809">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-809">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-810">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-810">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-811">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-811">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-812">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-812">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-813">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-813">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-814">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-814">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-815">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-815">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-817">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-817">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-819">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-819">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-821">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-821">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-823">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-823">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-825">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-825">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-827">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-827">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-829">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-829">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-831">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-831">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-832">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-832">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-834">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-834">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-836">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-836">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-838">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-838">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfcssup-11"></a><span data-ttu-id="5baf9-839">\_<sup>FCS</sup> DXGI_FORMAT_R16G16B16A16 UNORM (11)</span><span class="sxs-lookup"><span data-stu-id="5baf9-839">DXGI_FORMAT_R16G16B16A16\_UNORM<sup>FCS</sup> (11)</span></span>
| <span data-ttu-id="5baf9-840">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-840">Target</span></span> | <span data-ttu-id="5baf9-841">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-841">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-842">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-842">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-843">64</span><span class="sxs-lookup"><span data-stu-id="5baf9-843">64</span></span> |
| <span data-ttu-id="5baf9-844">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-844">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-846">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-846">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-848">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-848">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-850">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-850">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-851">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-851">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-852">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-852">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-854">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-854">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-856">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-856">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-858">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-858">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-860">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-860">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-862">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-862">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-864">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-864">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-865">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-865">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-866">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-866">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-867">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-867">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-868">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-868">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-870">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-870">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-872">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-872">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-874">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-874">Blendable RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-876">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-876">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-877">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-877">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-878">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-878">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-879">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-879">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-880">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-880">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-881">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-881">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-882">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-882">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-883">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-883">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-884">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-884">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-885">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-885">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-886">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-886">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-887">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-887">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-888">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-888">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-889">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-889">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-891">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-891">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-893">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-893">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-895">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-895">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-897">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-897">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-899">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-899">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-901">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-901">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-902">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-902">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-904">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-904">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-905">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-905">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-906">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-906">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-907">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-907">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-909">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-909">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfcssup-12"></a><span data-ttu-id="5baf9-910">\_<sup>FCS</sup> DXGI_FORMAT_R16G16B16A16 uint (12)</span><span class="sxs-lookup"><span data-stu-id="5baf9-910">DXGI_FORMAT_R16G16B16A16\_UINT<sup>FCS</sup> (12)</span></span>
| <span data-ttu-id="5baf9-911">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-911">Target</span></span> | <span data-ttu-id="5baf9-912">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-912">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-913">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-913">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-914">64</span><span class="sxs-lookup"><span data-stu-id="5baf9-914">64</span></span> |
| <span data-ttu-id="5baf9-915">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-915">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-917">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-917">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-919">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-919">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-921">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-921">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-922">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-922">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-923">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-923">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-925">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-925">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-927">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-927">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-929">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-929">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-931">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-931">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-933">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-933">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-934">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-934">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-935">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-935">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-936">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-936">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-937">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-937">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-938">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-938">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-940">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-940">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-941">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-941">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-943">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-943">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-944">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-944">Output Merger Logic Op</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-946">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-946">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-947">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-947">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-948">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-948">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-949">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-949">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-950">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-950">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-951">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-951">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-952">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-952">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-953">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-953">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-954">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-954">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-955">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-955">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-956">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-956">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-957">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-957">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-958">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-958">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-960">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-960">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-962">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-962">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-964">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-964">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-966">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-966">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-967">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-967">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-969">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-969">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-970">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-970">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-972">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-972">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-973">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-973">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-974">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-974">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-975">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-975">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-977">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-977">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfcssup-13"></a><span data-ttu-id="5baf9-978">\_SNORM<sup>FCS</sup> de DXGI_FORMAT_R16G16B16A16 (13)</span><span class="sxs-lookup"><span data-stu-id="5baf9-978">DXGI_FORMAT_R16G16B16A16\_SNORM<sup>FCS</sup> (13)</span></span>
| <span data-ttu-id="5baf9-979">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-979">Target</span></span> | <span data-ttu-id="5baf9-980">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-980">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-981">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-981">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-982">64</span><span class="sxs-lookup"><span data-stu-id="5baf9-982">64</span></span> |
| <span data-ttu-id="5baf9-983">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-983">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-985">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-985">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-987">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-987">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-989">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-989">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-990">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-990">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-991">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-991">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-993">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-993">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-995">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-995">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-997">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-997">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-999">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-999">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1001">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1001">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1003">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1003">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1004">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1004">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1005">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-1005">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-1006">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-1006">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-1007">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1007">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1009">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1009">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1011">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1011">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1013">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-1013">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1014">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-1014">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-1015">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-1015">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-1016">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-1016">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1017">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1017">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1018">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1018">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-1019">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1019">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-1020">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1020">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-1021">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1021">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-1022">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-1022">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-1023">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-1023">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-1024">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1024">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-1025">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-1025">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1026">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1026">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1027">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-1027">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1029">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1029">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1031">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-1031">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1033">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-1033">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1035">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-1035">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1037">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-1037">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1039">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-1039">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-1040">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-1040">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1042">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1042">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-1043">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1043">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-1044">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1044">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-1045">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1045">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1047">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-1047">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfcssup-14"></a><span data-ttu-id="5baf9-1048">DXGI_FORMAT_R16G16B16A16 \_ Santo<sup>FCS</sup> (14)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1048">DXGI_FORMAT_R16G16B16A16\_SINT<sup>FCS</sup> (14)</span></span>
| <span data-ttu-id="5baf9-1049">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-1049">Target</span></span> | <span data-ttu-id="5baf9-1050">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-1050">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-1051">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1051">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-1052">64</span><span class="sxs-lookup"><span data-stu-id="5baf9-1052">64</span></span> |
| <span data-ttu-id="5baf9-1053">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-1053">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1055">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-1055">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1057">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-1057">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1059">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-1059">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1060">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1060">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1061">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1061">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1063">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1063">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1065">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1065">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1067">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-1067">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1069">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-1069">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1071">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1071">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1072">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1072">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1073">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1073">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1074">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-1074">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-1075">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-1075">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-1076">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1076">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1078">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1078">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-1079">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1079">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1081">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-1081">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1082">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-1082">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-1083">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-1083">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-1084">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-1084">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1085">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1085">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1086">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1086">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-1087">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1087">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-1088">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1088">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-1089">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1089">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-1090">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-1090">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-1091">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-1091">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-1092">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1092">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-1093">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-1093">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1094">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1094">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1095">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-1095">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1097">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1097">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1099">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-1099">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1101">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-1101">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1103">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-1103">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-1104">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-1104">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1106">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-1106">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-1107">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-1107">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1109">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1109">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-1110">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1110">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-1111">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1111">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-1112">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1112">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1114">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-1114">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="5baf9-1115">DXGI_FORMAT_R32G32 \_ <sup>PCs</sup> não tipados (15)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1115">DXGI_FORMAT_R32G32\_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="5baf9-1116">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-1116">Target</span></span> | <span data-ttu-id="5baf9-1117">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-1117">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-1118">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1118">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-1119">64</span><span class="sxs-lookup"><span data-stu-id="5baf9-1119">64</span></span> |
| <span data-ttu-id="5baf9-1120">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-1120">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1122">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-1122">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1123">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-1123">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1124">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-1124">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1125">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1125">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1126">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1126">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1128">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1128">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1130">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1130">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1132">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-1132">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1134">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-1134">Shader ld</span></span> | \- |
| <span data-ttu-id="5baf9-1135">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1135">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1136">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1136">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1137">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1137">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1138">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-1138">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-1139">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-1139">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-1140">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1140">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1142">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1142">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-1143">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1143">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1144">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-1144">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1145">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-1145">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-1146">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-1146">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-1147">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-1147">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1148">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1148">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1149">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1149">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-1150">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1150">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-1151">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1151">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-1152">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1152">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-1153">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-1153">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-1154">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-1154">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-1155">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1155">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-1156">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-1156">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1157">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1157">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1158">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-1158">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1160">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1160">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1161">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-1161">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1162">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-1162">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-1163">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-1163">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-1164">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-1164">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-1165">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-1165">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-1166">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-1166">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1168">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1168">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-1169">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1169">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-1170">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1170">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-1171">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1171">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-1172">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-1172">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_floatsupfcssup-16"></a><span data-ttu-id="5baf9-1173">\_<sup>FCS</sup> de DXGI_FORMAT_R32G32 float (16)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1173">DXGI_FORMAT_R32G32\_FLOAT<sup>FCS</sup> (16)</span></span>
| <span data-ttu-id="5baf9-1174">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-1174">Target</span></span> | <span data-ttu-id="5baf9-1175">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-1175">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-1176">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1176">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-1177">64</span><span class="sxs-lookup"><span data-stu-id="5baf9-1177">64</span></span> |
| <span data-ttu-id="5baf9-1178">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-1178">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1180">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-1180">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1182">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-1182">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1184">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-1184">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1185">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1185">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1187">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1187">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1189">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1189">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1191">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1191">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1193">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-1193">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1195">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-1195">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1197">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1197">Shader sample (any filter)</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1199">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1199">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1200">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1200">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1201">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-1201">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-1202">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-1202">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-1203">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1203">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1205">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1205">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1207">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1207">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1209">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-1209">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1211">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-1211">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-1212">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-1212">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-1213">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-1213">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1214">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1214">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1215">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1215">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-1216">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1216">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-1217">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1217">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-1218">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1218">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-1219">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-1219">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-1220">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-1220">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-1221">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1221">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-1222">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-1222">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1223">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1223">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1224">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-1224">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1226">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1226">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1228">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-1228">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1230">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-1230">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1232">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-1232">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1234">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-1234">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1236">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-1236">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-1237">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-1237">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1239">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1239">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-1240">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1240">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-1241">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1241">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-1242">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1242">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-1243">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-1243">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_uintsupfcssup-17"></a><span data-ttu-id="5baf9-1244">\_<sup>FCS</sup> DXGI_FORMAT_R32G32 uint (17)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1244">DXGI_FORMAT_R32G32\_UINT<sup>FCS</sup> (17)</span></span>
| <span data-ttu-id="5baf9-1245">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-1245">Target</span></span> | <span data-ttu-id="5baf9-1246">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-1246">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-1247">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1247">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-1248">64</span><span class="sxs-lookup"><span data-stu-id="5baf9-1248">64</span></span> |
| <span data-ttu-id="5baf9-1249">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-1249">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1251">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-1251">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1253">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-1253">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1255">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-1255">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1256">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1256">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1258">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1258">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1260">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1260">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1262">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1262">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1264">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-1264">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1266">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-1266">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1268">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1268">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1269">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1269">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1270">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1270">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1271">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-1271">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-1272">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-1272">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-1273">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1273">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1275">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1275">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-1276">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1276">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1278">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-1278">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1279">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-1279">Output Merger Logic Op</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1281">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-1281">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-1282">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-1282">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1283">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1283">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1284">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1284">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-1285">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1285">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-1286">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1286">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-1287">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1287">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-1288">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-1288">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-1289">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-1289">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-1290">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1290">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-1291">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-1291">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1292">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1292">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1293">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-1293">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1295">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1295">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1297">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-1297">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1299">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-1299">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1301">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-1301">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-1302">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-1302">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1304">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-1304">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-1305">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-1305">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1307">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1307">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-1308">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1308">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-1309">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1309">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-1310">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1310">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-1311">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-1311">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_sintsupfcssup-18"></a><span data-ttu-id="5baf9-1312">DXGI_FORMAT_R32G32 \_ Santo<sup>FCS</sup> (18)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1312">DXGI_FORMAT_R32G32\_SINT<sup>FCS</sup> (18)</span></span>
| <span data-ttu-id="5baf9-1313">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-1313">Target</span></span> | <span data-ttu-id="5baf9-1314">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-1314">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-1315">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1315">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-1316">64</span><span class="sxs-lookup"><span data-stu-id="5baf9-1316">64</span></span> |
| <span data-ttu-id="5baf9-1317">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-1317">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1319">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-1319">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1321">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-1321">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1323">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-1323">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1324">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1324">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1326">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1326">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1328">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1328">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1330">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1330">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1332">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-1332">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1334">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-1334">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1336">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1336">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1337">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1337">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1338">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1338">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1339">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-1339">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-1340">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-1340">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-1341">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1341">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1343">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1343">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-1344">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1344">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1346">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-1346">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1347">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-1347">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-1348">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-1348">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-1349">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-1349">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1350">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1350">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1351">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1351">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-1352">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1352">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-1353">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1353">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-1354">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1354">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-1355">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-1355">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-1356">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-1356">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-1357">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1357">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-1358">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-1358">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1359">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1359">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1360">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-1360">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1362">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1362">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1364">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-1364">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1366">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-1366">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1368">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-1368">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-1369">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-1369">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1371">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-1371">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-1372">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-1372">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1374">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1374">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-1375">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1375">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-1376">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1376">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-1377">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1377">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-1378">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-1378">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a><span data-ttu-id="5baf9-1379">DXGI_FORMAT_R32G8X24 \_ <sup>PCs</sup> não tipados (19)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1379">DXGI_FORMAT_R32G8X24\_TYPELESS<sup>PCS</sup> (19)</span></span>
| <span data-ttu-id="5baf9-1380">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-1380">Target</span></span> | <span data-ttu-id="5baf9-1381">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-1381">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-1382">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1382">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-1383">64</span><span class="sxs-lookup"><span data-stu-id="5baf9-1383">64</span></span> |
| <span data-ttu-id="5baf9-1384">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-1384">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1386">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-1386">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1387">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-1387">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1388">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-1388">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1389">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1389">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1390">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1390">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1392">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1392">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1394">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1394">Texture3D</span></span> | \- |
| <span data-ttu-id="5baf9-1395">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-1395">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1397">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-1397">Shader ld</span></span> | \- |
| <span data-ttu-id="5baf9-1398">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1398">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1399">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1399">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1400">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1400">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1401">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-1401">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-1402">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-1402">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-1403">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1403">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1405">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1405">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-1406">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1406">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1407">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-1407">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1408">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-1408">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-1409">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-1409">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-1410">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-1410">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1411">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1411">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1412">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1412">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-1413">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1413">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-1414">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1414">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-1415">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1415">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-1416">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-1416">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-1417">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-1417">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-1418">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1418">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-1419">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-1419">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1420">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1420">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1421">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-1421">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1423">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1423">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1424">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-1424">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1425">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-1425">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-1426">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-1426">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-1427">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-1427">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-1428">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-1428">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-1429">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-1429">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1431">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1431">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-1432">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1432">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-1433">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1433">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-1434">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1434">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-1435">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-1435">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfcssup-20"></a><span data-ttu-id="5baf9-1436">DXGI_FORMAT_D32 \_ float \_ S8X24 \_ uint do<sup>FCS</sup> (20)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1436">DXGI_FORMAT_D32\_FLOAT\_S8X24\_UINT<sup>FCS</sup> (20)</span></span>
| <span data-ttu-id="5baf9-1437">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-1437">Target</span></span> | <span data-ttu-id="5baf9-1438">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-1438">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-1439">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1439">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-1440">64</span><span class="sxs-lookup"><span data-stu-id="5baf9-1440">64</span></span> |
| <span data-ttu-id="5baf9-1441">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-1441">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1443">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-1443">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1444">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-1444">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1445">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-1445">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1446">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1446">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1447">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1447">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1449">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1449">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1451">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1451">Texture3D</span></span> | \- |
| <span data-ttu-id="5baf9-1452">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-1452">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1454">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-1454">Shader ld</span></span> | \- |
| <span data-ttu-id="5baf9-1455">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1455">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1456">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1456">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1457">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1457">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1458">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-1458">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-1459">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-1459">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-1460">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1460">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1462">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1462">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-1463">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1463">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1464">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-1464">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1465">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-1465">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-1466">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-1466">Depth/Stencil Target</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1468">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-1468">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1469">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1469">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1470">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1470">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-1471">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1471">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-1472">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1472">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-1473">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1473">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-1474">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-1474">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-1475">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-1475">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-1476">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1476">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-1477">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-1477">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1478">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1478">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1479">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-1479">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1481">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1481">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1483">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-1483">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1485">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-1485">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1487">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-1487">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-1488">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-1488">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-1489">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-1489">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-1490">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-1490">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1492">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1492">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-1493">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1493">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-1494">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1494">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-1495">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1495">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-1496">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-1496">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfcssup-21"></a><span data-ttu-id="5baf9-1497">\_FCS DXGI_FORMAT_R32 \_ \_ de tipo float<sup></sup> X8X24 (21)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1497">DXGI_FORMAT_R32\_FLOAT\_X8X24\_TYPELESS<sup>FCS</sup> (21)</span></span>
| <span data-ttu-id="5baf9-1498">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-1498">Target</span></span> | <span data-ttu-id="5baf9-1499">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-1499">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-1500">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1500">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-1501">64</span><span class="sxs-lookup"><span data-stu-id="5baf9-1501">64</span></span> |
| <span data-ttu-id="5baf9-1502">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-1502">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1504">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-1504">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1505">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-1505">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1506">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-1506">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1507">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1507">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1508">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1508">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1510">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1510">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1512">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1512">Texture3D</span></span> | \- |
| <span data-ttu-id="5baf9-1513">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-1513">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1515">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-1515">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1517">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1517">Shader sample (any filter)</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1519">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1519">Shader sample\_c (comparison filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1521">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1521">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1522">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-1522">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-1523">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-1523">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-1524">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1524">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1526">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1526">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-1527">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1527">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1528">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-1528">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1529">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-1529">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-1530">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-1530">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-1531">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-1531">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1532">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1532">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1533">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1533">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-1534">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1534">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-1535">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1535">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-1536">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1536">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-1537">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-1537">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-1538">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-1538">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-1539">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1539">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-1540">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-1540">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1541">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1541">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1542">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-1542">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1544">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1544">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1545">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-1545">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1546">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-1546">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-1547">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-1547">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-1548">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-1548">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-1549">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-1549">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-1550">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-1550">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1552">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1552">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-1553">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1553">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-1554">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1554">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-1555">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1555">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-1556">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-1556">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfcssup-22"></a><span data-ttu-id="5baf9-1557">\_ \_ G8X24 \_ de<sup>FCS</sup> (22) não tipado DXGI_FORMAT_X32</span><span class="sxs-lookup"><span data-stu-id="5baf9-1557">DXGI_FORMAT_X32\_TYPELESS\_G8X24\_UINT<sup>FCS</sup> (22)</span></span>
| <span data-ttu-id="5baf9-1558">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-1558">Target</span></span> | <span data-ttu-id="5baf9-1559">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-1559">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-1560">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1560">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-1561">64</span><span class="sxs-lookup"><span data-stu-id="5baf9-1561">64</span></span> |
| <span data-ttu-id="5baf9-1562">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-1562">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1564">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-1564">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1565">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-1565">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1566">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-1566">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1567">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1567">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1568">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1568">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1570">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1570">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1572">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1572">Texture3D</span></span> | \- |
| <span data-ttu-id="5baf9-1573">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-1573">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1575">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-1575">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1577">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1577">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1578">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1578">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1579">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1579">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1580">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-1580">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-1581">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-1581">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-1582">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1582">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1584">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1584">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-1585">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1585">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1586">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-1586">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1587">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-1587">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-1588">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-1588">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-1589">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-1589">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1590">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1590">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1591">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1591">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-1592">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1592">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-1593">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1593">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-1594">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1594">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-1595">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-1595">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-1596">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-1596">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-1597">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1597">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-1598">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-1598">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1599">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1599">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1600">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-1600">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1602">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1602">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1603">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-1603">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1604">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-1604">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-1605">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-1605">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-1606">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-1606">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-1607">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-1607">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-1608">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-1608">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1610">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1610">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-1611">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1611">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-1612">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1612">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-1613">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1613">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-1614">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-1614">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="5baf9-1615">DXGI_FORMAT_R10G10B10A2 \_ <sup>PCs</sup> não tipados (23)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1615">DXGI_FORMAT_R10G10B10A2\_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="5baf9-1616">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-1616">Target</span></span> | <span data-ttu-id="5baf9-1617">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-1617">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-1618">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1618">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-1619">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-1619">32</span></span> |
| <span data-ttu-id="5baf9-1620">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-1620">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1622">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-1622">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1623">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-1623">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1624">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-1624">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1625">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1625">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1626">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1626">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1628">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1628">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1630">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1630">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1632">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-1632">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1634">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-1634">Shader ld</span></span> | \- |
| <span data-ttu-id="5baf9-1635">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1635">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1636">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1636">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1637">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1637">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1638">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-1638">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-1639">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-1639">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-1640">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1640">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1642">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1642">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-1643">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1643">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1644">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-1644">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1645">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-1645">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-1646">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-1646">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-1647">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-1647">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1648">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1648">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1649">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1649">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-1650">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1650">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-1651">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1651">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-1652">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1652">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-1653">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-1653">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-1654">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-1654">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-1655">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1655">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-1656">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-1656">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1657">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1657">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1658">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-1658">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1660">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1660">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1661">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-1661">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1662">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-1662">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-1663">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-1663">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-1664">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-1664">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-1665">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-1665">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-1666">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-1666">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1668">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1668">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-1669">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1669">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-1670">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1670">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-1671">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1671">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1673">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-1673">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfcssup-24"></a><span data-ttu-id="5baf9-1674">\_UNORM<sup>FCS</sup> de DXGI_FORMAT_R10G10B10A2 (24)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1674">DXGI_FORMAT_R10G10B10A2\_UNORM<sup>FCS</sup> (24)</span></span>
| <span data-ttu-id="5baf9-1675">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-1675">Target</span></span> | <span data-ttu-id="5baf9-1676">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-1676">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-1677">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1677">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-1678">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-1678">32</span></span> |
| <span data-ttu-id="5baf9-1679">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-1679">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1681">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-1681">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1683">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-1683">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1685">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-1685">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1686">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1686">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1687">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1687">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1689">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1689">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1691">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1691">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1693">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-1693">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1695">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-1695">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1697">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1697">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1699">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1699">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1700">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1700">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1701">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-1701">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-1702">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-1702">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-1703">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1703">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1705">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1705">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1707">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1707">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1709">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-1709">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1711">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-1711">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-1712">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-1712">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-1713">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-1713">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1714">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1714">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1715">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1715">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-1716">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1716">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-1717">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1717">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-1718">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1718">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-1719">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-1719">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-1720">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-1720">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-1721">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1721">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-1722">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-1722">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1723">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1723">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1724">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-1724">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1726">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1726">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1728">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-1728">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1730">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-1730">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1732">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-1732">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1734">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-1734">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1736">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-1736">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1738">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-1738">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1740">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1740">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-1741">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1741">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1743">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1743">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1745">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1745">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1747">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-1747">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfcssup-25"></a><span data-ttu-id="5baf9-1748">\_<sup>FCS</sup> DXGI_FORMAT_R10G10B10A2 uint (25)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1748">DXGI_FORMAT_R10G10B10A2\_UINT<sup>FCS</sup> (25)</span></span>
| <span data-ttu-id="5baf9-1749">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-1749">Target</span></span> | <span data-ttu-id="5baf9-1750">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-1750">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-1751">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1751">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-1752">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-1752">32</span></span> |
| <span data-ttu-id="5baf9-1753">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-1753">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1755">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-1755">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1757">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-1757">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1759">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-1759">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1760">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1760">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1761">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1761">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1763">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1763">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1765">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1765">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1767">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-1767">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1769">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-1769">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1771">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1771">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1772">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1772">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1773">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1773">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1774">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-1774">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-1775">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-1775">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-1776">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1776">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1778">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1778">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-1779">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1779">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1781">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-1781">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1782">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-1782">Output Merger Logic Op</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1784">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-1784">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-1785">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-1785">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1786">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1786">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1787">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1787">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-1788">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1788">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-1789">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1789">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-1790">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1790">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-1791">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-1791">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-1792">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-1792">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-1793">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1793">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-1794">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-1794">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1795">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1795">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1796">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-1796">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1798">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1798">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1800">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-1800">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1802">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-1802">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1804">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-1804">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-1805">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-1805">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1807">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-1807">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-1808">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-1808">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1810">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1810">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-1811">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1811">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-1812">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1812">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-1813">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1813">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1815">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-1815">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfcssup-89"></a><span data-ttu-id="5baf9-1816">DXGI_FORMAT_R10G10B10 \_ XR \_ Bias \_ a2 \_ UNORM<sup>FCS</sup> (89)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1816">DXGI_FORMAT_R10G10B10\_XR\_BIAS\_A2\_UNORM<sup>FCS</sup> (89)</span></span>
| <span data-ttu-id="5baf9-1817">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-1817">Target</span></span> | <span data-ttu-id="5baf9-1818">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-1818">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-1819">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1819">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-1820">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-1820">32</span></span> |
| <span data-ttu-id="5baf9-1821">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-1821">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1823">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-1823">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1824">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-1824">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1825">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-1825">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1826">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1826">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1827">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1827">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-1828">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1828">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1830">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1830">Texture3D</span></span> | \- |
| <span data-ttu-id="5baf9-1831">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-1831">TextureCube</span></span> | \- |
| <span data-ttu-id="5baf9-1832">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-1832">Shader ld</span></span> | \- |
| <span data-ttu-id="5baf9-1833">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1833">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1834">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1834">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1835">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1835">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1836">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-1836">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-1837">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-1837">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-1838">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1838">Mipmap</span></span> | \- |
| <span data-ttu-id="5baf9-1839">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1839">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-1840">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1840">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1841">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-1841">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1842">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-1842">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-1843">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-1843">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-1844">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-1844">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1845">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1845">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1846">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1846">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-1847">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1847">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-1848">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1848">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-1849">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1849">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-1850">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-1850">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-1851">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-1851">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-1852">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1852">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-1853">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-1853">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1854">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1854">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1855">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-1855">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1857">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1857">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1858">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-1858">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1859">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-1859">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-1860">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-1860">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-1861">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-1861">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-1862">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-1862">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1864">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-1864">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1866">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1866">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-1867">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1867">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1869">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1869">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1871">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1871">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1873">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-1873">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="5baf9-1874">DXGI_FORMAT_R11G11B10 \_ float<sup>FNS</sup> (26)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1874">DXGI_FORMAT_R11G11B10\_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="5baf9-1875">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-1875">Target</span></span> | <span data-ttu-id="5baf9-1876">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-1876">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-1877">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1877">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-1878">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-1878">32</span></span> |
| <span data-ttu-id="5baf9-1879">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-1879">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1881">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-1881">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1883">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-1883">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1885">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-1885">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1886">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1886">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1887">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1887">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1889">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1889">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1891">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1891">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1893">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-1893">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1895">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-1895">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1897">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1897">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1899">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1899">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1900">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1900">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1901">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-1901">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-1902">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-1902">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-1903">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1903">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1905">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1905">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1907">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1907">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1909">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-1909">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1911">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-1911">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-1912">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-1912">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-1913">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-1913">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1914">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1914">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1915">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1915">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-1916">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1916">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-1917">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1917">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-1918">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1918">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-1919">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-1919">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-1920">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-1920">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-1921">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1921">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-1922">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-1922">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1923">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1923">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1924">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-1924">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1926">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1926">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1928">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-1928">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1930">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-1930">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1932">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-1932">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1934">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-1934">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-1936">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-1936">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-1937">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-1937">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="5baf9-1938">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1938">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-1939">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1939">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-1940">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1940">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-1941">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1941">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-1942">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-1942">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="5baf9-1943">DXGI_FORMAT_R8G8B8A8 \_ <sup>PCs</sup> não tipados (27)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1943">DXGI_FORMAT_R8G8B8A8\_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="5baf9-1944">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-1944">Target</span></span> | <span data-ttu-id="5baf9-1945">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-1945">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-1946">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1946">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-1947">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-1947">32</span></span> |
| <span data-ttu-id="5baf9-1948">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-1948">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1950">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-1950">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1951">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-1951">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1952">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-1952">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1953">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1953">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-1954">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1954">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1956">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1956">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1958">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-1958">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1960">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-1960">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1962">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-1962">Shader ld</span></span> | \- |
| <span data-ttu-id="5baf9-1963">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1963">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1964">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1964">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1965">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-1965">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-1966">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-1966">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-1967">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-1967">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-1968">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1968">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1970">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-1970">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-1971">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1971">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1972">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-1972">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1973">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-1973">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-1974">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-1974">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-1975">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-1975">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1976">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1976">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-1977">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1977">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-1978">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1978">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-1979">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1979">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-1980">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1980">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-1981">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-1981">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-1982">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-1982">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-1983">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-1983">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-1984">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-1984">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1985">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1985">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-1986">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-1986">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1988">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-1988">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1989">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-1989">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-1990">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-1990">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-1991">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-1991">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-1992">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-1992">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-1993">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-1993">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-1994">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-1994">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-1996">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1996">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-1997">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1997">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-1998">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-1998">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-1999">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-1999">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2001">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-2001">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfcssup-28"></a><span data-ttu-id="5baf9-2002">\_UNORM<sup>FCS</sup> de DXGI_FORMAT_R8G8B8A8 (28)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2002">DXGI_FORMAT_R8G8B8A8\_UNORM<sup>FCS</sup> (28)</span></span>
| <span data-ttu-id="5baf9-2003">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-2003">Target</span></span> | <span data-ttu-id="5baf9-2004">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-2004">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-2005">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2005">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-2006">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-2006">32</span></span> |
| <span data-ttu-id="5baf9-2007">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-2007">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2009">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-2009">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2011">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-2011">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2013">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-2013">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2014">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2014">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2015">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2015">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2017">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2017">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2019">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2019">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2021">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-2021">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2023">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-2023">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2025">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2025">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2027">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2027">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2028">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2028">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2029">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-2029">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-2030">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-2030">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-2031">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-2031">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2033">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-2033">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2035">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-2035">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2037">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-2037">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2039">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-2039">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-2040">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-2040">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-2041">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-2041">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-2042">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2042">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-2043">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-2043">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-2044">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2044">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-2045">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2045">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-2046">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2046">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-2047">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-2047">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-2048">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-2048">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-2049">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2049">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-2050">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-2050">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-2051">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2051">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-2052">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-2052">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2054">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-2054">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2056">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-2056">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2058">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-2058">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2060">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-2060">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2062">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-2062">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2064">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-2064">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2066">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-2066">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2068">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2068">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-2069">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2069">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2071">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2071">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2073">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-2073">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2075">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-2075">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfcssup-29"></a><span data-ttu-id="5baf9-2076">\_FCS DXGI_FORMAT_R8G8B8A8 \_ UNORM<sup></sup> sRGB (29)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2076">DXGI_FORMAT_R8G8B8A8\_UNORM\_SRGB<sup>FCS</sup> (29)</span></span>
| <span data-ttu-id="5baf9-2077">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-2077">Target</span></span> | <span data-ttu-id="5baf9-2078">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-2078">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-2079">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2079">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-2080">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-2080">32</span></span> |
| <span data-ttu-id="5baf9-2081">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-2081">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2083">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-2083">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2084">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-2084">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2085">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-2085">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2086">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2086">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2087">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2087">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2089">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2089">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2091">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2091">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2093">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-2093">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2095">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-2095">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2097">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2097">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2099">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2099">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2100">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2100">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2101">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-2101">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-2102">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-2102">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-2103">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-2103">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2105">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-2105">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2107">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-2107">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2109">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-2109">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2111">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-2111">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-2112">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-2112">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-2113">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-2113">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-2114">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2114">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-2115">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-2115">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-2116">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2116">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-2117">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2117">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-2118">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2118">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-2119">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-2119">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-2120">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-2120">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-2121">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2121">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-2122">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-2122">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-2123">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2123">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-2124">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-2124">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2126">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-2126">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2128">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-2128">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2130">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-2130">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2132">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-2132">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2134">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-2134">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2136">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-2136">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2138">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-2138">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2140">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2140">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-2141">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2141">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2143">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2143">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2145">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-2145">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2147">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-2147">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfcssup-30"></a><span data-ttu-id="5baf9-2148">\_<sup>FCS</sup> DXGI_FORMAT_R8G8B8A8 uint (30)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2148">DXGI_FORMAT_R8G8B8A8\_UINT<sup>FCS</sup> (30)</span></span>
| <span data-ttu-id="5baf9-2149">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-2149">Target</span></span> | <span data-ttu-id="5baf9-2150">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-2150">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-2151">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2151">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-2152">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-2152">32</span></span> |
| <span data-ttu-id="5baf9-2153">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-2153">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2155">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-2155">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2157">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-2157">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2159">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-2159">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2160">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2160">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2161">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2161">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2163">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2163">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2165">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2165">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2167">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-2167">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2169">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-2169">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2171">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2171">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2172">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2172">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2173">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2173">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2174">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-2174">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-2175">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-2175">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-2176">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-2176">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2178">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-2178">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-2179">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-2179">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2181">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-2181">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-2182">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-2182">Output Merger Logic Op</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2184">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-2184">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-2185">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-2185">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-2186">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2186">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-2187">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-2187">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-2188">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2188">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-2189">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2189">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-2190">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2190">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-2191">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-2191">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-2192">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-2192">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-2193">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2193">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-2194">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-2194">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-2195">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2195">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-2196">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-2196">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2198">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-2198">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2200">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-2200">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2202">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-2202">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2204">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-2204">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-2205">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-2205">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2207">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-2207">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-2208">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-2208">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2210">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2210">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-2211">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2211">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-2212">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2212">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-2213">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-2213">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2215">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-2215">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfcssup-31"></a><span data-ttu-id="5baf9-2216">DXGI_FORMAT_R8G8B8A8 \_ <sup>FCS</sup> SNORM (31)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2216">DXGI_FORMAT_R8G8B8A8\_SNORM<sup>FCS</sup> (31)</span></span>
| <span data-ttu-id="5baf9-2217">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-2217">Target</span></span> | <span data-ttu-id="5baf9-2218">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-2218">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-2219">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2219">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-2220">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-2220">32</span></span> |
| <span data-ttu-id="5baf9-2221">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-2221">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2223">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-2223">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2225">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-2225">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2227">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-2227">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2228">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2228">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2229">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2229">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2231">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2231">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2233">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2233">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2235">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-2235">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2237">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-2237">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2239">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2239">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2241">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2241">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2242">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2242">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2243">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-2243">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-2244">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-2244">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-2245">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-2245">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2247">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-2247">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2249">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-2249">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2251">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-2251">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-2252">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-2252">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-2253">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-2253">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-2254">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-2254">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-2255">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2255">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-2256">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-2256">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-2257">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2257">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-2258">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2258">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-2259">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2259">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-2260">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-2260">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-2261">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-2261">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-2262">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2262">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-2263">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-2263">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-2264">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2264">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-2265">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-2265">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2267">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-2267">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2269">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-2269">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2271">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-2271">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2273">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-2273">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2275">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-2275">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2277">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-2277">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-2278">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-2278">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2280">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2280">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-2281">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2281">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-2282">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2282">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-2283">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-2283">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2285">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-2285">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfcssup-32"></a><span data-ttu-id="5baf9-2286">\_<sup>FCS</sup> DXGI_FORMAT_R8G8B8A8 Santo (32)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2286">DXGI_FORMAT_R8G8B8A8\_SINT<sup>FCS</sup> (32)</span></span>
| <span data-ttu-id="5baf9-2287">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-2287">Target</span></span> | <span data-ttu-id="5baf9-2288">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-2288">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-2289">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2289">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-2290">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-2290">32</span></span> |
| <span data-ttu-id="5baf9-2291">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-2291">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2293">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-2293">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2295">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-2295">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2297">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-2297">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2298">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2298">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2299">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2299">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2301">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2301">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2303">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2303">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2305">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-2305">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2307">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-2307">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2309">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2309">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2310">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2310">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2311">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2311">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2312">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-2312">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-2313">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-2313">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-2314">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-2314">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2316">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-2316">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-2317">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-2317">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2319">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-2319">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-2320">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-2320">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-2321">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-2321">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-2322">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-2322">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-2323">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2323">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-2324">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-2324">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-2325">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2325">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-2326">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2326">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-2327">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2327">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-2328">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-2328">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-2329">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-2329">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-2330">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2330">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-2331">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-2331">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-2332">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2332">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-2333">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-2333">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2335">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-2335">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2337">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-2337">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2339">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-2339">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2341">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-2341">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-2342">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-2342">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2344">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-2344">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-2345">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-2345">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2347">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2347">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-2348">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2348">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-2349">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2349">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-2350">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-2350">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2352">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-2352">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="5baf9-2353">DXGI_FORMAT_R16G16 \_ <sup>PCs</sup> não tipados (33)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2353">DXGI_FORMAT_R16G16\_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="5baf9-2354">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-2354">Target</span></span> | <span data-ttu-id="5baf9-2355">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-2355">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-2356">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2356">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-2357">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-2357">32</span></span> |
| <span data-ttu-id="5baf9-2358">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-2358">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2360">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-2360">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2361">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-2361">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2362">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-2362">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2363">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2363">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2364">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2364">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2366">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2366">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2368">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2368">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2370">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-2370">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2372">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-2372">Shader ld</span></span> | \- |
| <span data-ttu-id="5baf9-2373">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2373">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2374">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2374">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2375">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2375">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2376">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-2376">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-2377">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-2377">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-2378">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-2378">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2380">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-2380">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-2381">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-2381">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-2382">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-2382">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-2383">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-2383">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-2384">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-2384">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-2385">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-2385">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-2386">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2386">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-2387">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-2387">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-2388">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2388">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-2389">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2389">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-2390">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2390">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-2391">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-2391">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-2392">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-2392">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-2393">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2393">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-2394">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-2394">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-2395">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2395">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-2396">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-2396">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2398">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-2398">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-2399">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-2399">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-2400">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-2400">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-2401">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-2401">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-2402">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-2402">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-2403">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-2403">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-2404">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-2404">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2406">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2406">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-2407">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2407">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-2408">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2408">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-2409">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-2409">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-2410">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-2410">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_floatsupfcssup-34"></a><span data-ttu-id="5baf9-2411">\_<sup>FCS</sup> de DXGI_FORMAT_R16G16 float (34)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2411">DXGI_FORMAT_R16G16\_FLOAT<sup>FCS</sup> (34)</span></span>
| <span data-ttu-id="5baf9-2412">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-2412">Target</span></span> | <span data-ttu-id="5baf9-2413">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-2413">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-2414">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2414">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-2415">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-2415">32</span></span> |
| <span data-ttu-id="5baf9-2416">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-2416">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2418">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-2418">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2420">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-2420">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2422">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-2422">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2423">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2423">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2424">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2424">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2426">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2426">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2428">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2428">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2430">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-2430">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2432">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-2432">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2434">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2434">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2436">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2436">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2437">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2437">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2438">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-2438">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-2439">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-2439">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-2440">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-2440">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2442">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-2442">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2444">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-2444">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2446">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-2446">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2448">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-2448">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-2449">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-2449">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-2450">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-2450">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-2451">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2451">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-2452">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-2452">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-2453">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2453">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-2454">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2454">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-2455">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2455">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-2456">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-2456">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-2457">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-2457">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-2458">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2458">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-2459">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-2459">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-2460">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2460">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-2461">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-2461">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2463">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-2463">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2465">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-2465">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2467">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-2467">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2469">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-2469">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2471">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-2471">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2473">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-2473">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-2474">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-2474">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2476">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2476">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-2477">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2477">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-2478">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2478">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-2479">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-2479">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-2480">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-2480">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_unormsupfcssup-35"></a><span data-ttu-id="5baf9-2481">\_UNORM<sup>FCS</sup> de DXGI_FORMAT_R16G16 (35)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2481">DXGI_FORMAT_R16G16\_UNORM<sup>FCS</sup> (35)</span></span>
| <span data-ttu-id="5baf9-2482">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-2482">Target</span></span> | <span data-ttu-id="5baf9-2483">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-2483">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-2484">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2484">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-2485">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-2485">32</span></span> |
| <span data-ttu-id="5baf9-2486">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-2486">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2488">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-2488">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2490">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-2490">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2492">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-2492">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2493">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2493">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2494">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2494">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2496">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2496">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2498">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2498">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2500">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-2500">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2502">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-2502">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2504">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2504">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2506">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2506">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2507">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2507">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2508">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-2508">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-2509">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-2509">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-2510">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-2510">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2512">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-2512">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2514">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-2514">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2516">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-2516">Blendable RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2518">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-2518">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-2519">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-2519">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-2520">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-2520">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-2521">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2521">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-2522">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-2522">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-2523">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2523">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-2524">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2524">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-2525">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2525">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-2526">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-2526">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-2527">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-2527">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-2528">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2528">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-2529">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-2529">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-2530">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2530">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-2531">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-2531">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2533">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-2533">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2535">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-2535">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2537">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-2537">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2539">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-2539">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2541">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-2541">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2543">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-2543">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-2544">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-2544">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2546">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2546">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-2547">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2547">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-2548">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2548">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-2549">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-2549">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-2550">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-2550">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_uintsupfcssup-36"></a><span data-ttu-id="5baf9-2551">\_<sup>FCS</sup> DXGI_FORMAT_R16G16 uint (36)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2551">DXGI_FORMAT_R16G16\_UINT<sup>FCS</sup> (36)</span></span>
| <span data-ttu-id="5baf9-2552">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-2552">Target</span></span> | <span data-ttu-id="5baf9-2553">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-2553">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-2554">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2554">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-2555">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-2555">32</span></span> |
| <span data-ttu-id="5baf9-2556">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-2556">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2558">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-2558">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2560">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-2560">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2562">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-2562">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2563">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2563">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2564">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2564">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2566">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2566">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2568">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2568">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2570">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-2570">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2572">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-2572">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2574">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2574">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2575">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2575">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2576">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2576">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2577">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-2577">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-2578">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-2578">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-2579">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-2579">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2581">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-2581">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-2582">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-2582">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2584">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-2584">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-2585">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-2585">Output Merger Logic Op</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2587">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-2587">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-2588">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-2588">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-2589">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2589">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-2590">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-2590">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-2591">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2591">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-2592">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2592">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-2593">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2593">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-2594">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-2594">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-2595">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-2595">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-2596">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2596">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-2597">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-2597">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-2598">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2598">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-2599">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-2599">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2601">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-2601">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2603">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-2603">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2605">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-2605">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2607">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-2607">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-2608">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-2608">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2610">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-2610">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-2611">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-2611">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2613">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2613">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-2614">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2614">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-2615">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2615">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-2616">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-2616">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-2617">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-2617">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_snormsupfcssup-37"></a><span data-ttu-id="5baf9-2618">\_SNORM<sup>FCS</sup> de DXGI_FORMAT_R16G16 (37)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2618">DXGI_FORMAT_R16G16\_SNORM<sup>FCS</sup> (37)</span></span>
| <span data-ttu-id="5baf9-2619">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-2619">Target</span></span> | <span data-ttu-id="5baf9-2620">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-2620">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-2621">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2621">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-2622">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-2622">32</span></span> |
| <span data-ttu-id="5baf9-2623">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-2623">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2625">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-2625">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2627">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-2627">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2629">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-2629">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2630">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2630">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2631">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2631">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2633">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2633">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2635">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2635">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2637">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-2637">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2639">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-2639">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2641">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2641">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2643">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2643">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2644">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2644">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2645">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-2645">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-2646">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-2646">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-2647">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-2647">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2649">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-2649">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2651">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-2651">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2653">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-2653">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-2654">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-2654">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-2655">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-2655">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-2656">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-2656">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-2657">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2657">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-2658">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-2658">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-2659">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2659">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-2660">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2660">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-2661">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2661">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-2662">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-2662">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-2663">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-2663">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-2664">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2664">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-2665">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-2665">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-2666">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2666">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-2667">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-2667">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2669">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-2669">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2671">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-2671">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2673">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-2673">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2675">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-2675">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2677">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-2677">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2679">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-2679">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-2680">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-2680">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2682">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2682">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-2683">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2683">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-2684">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2684">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-2685">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-2685">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-2686">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-2686">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_sintsupfcssup-38"></a><span data-ttu-id="5baf9-2687">\_<sup>FCS</sup> DXGI_FORMAT_R16G16 Santo (38)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2687">DXGI_FORMAT_R16G16\_SINT<sup>FCS</sup> (38)</span></span>
| <span data-ttu-id="5baf9-2688">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-2688">Target</span></span> | <span data-ttu-id="5baf9-2689">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-2689">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-2690">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2690">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-2691">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-2691">32</span></span> |
| <span data-ttu-id="5baf9-2692">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-2692">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2694">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-2694">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2696">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-2696">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2698">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-2698">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2699">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2699">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2700">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2700">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2702">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2702">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2704">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2704">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2706">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-2706">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2708">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-2708">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2710">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2710">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2711">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2711">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2712">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2712">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2713">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-2713">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-2714">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-2714">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-2715">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-2715">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2717">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-2717">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-2718">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-2718">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2720">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-2720">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-2721">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-2721">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-2722">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-2722">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-2723">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-2723">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-2724">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2724">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-2725">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-2725">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-2726">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2726">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-2727">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2727">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-2728">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2728">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-2729">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-2729">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-2730">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-2730">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-2731">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2731">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-2732">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-2732">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-2733">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2733">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-2734">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-2734">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2736">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-2736">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2738">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-2738">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2740">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-2740">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2742">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-2742">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-2743">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-2743">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2745">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-2745">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-2746">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-2746">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2748">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2748">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-2749">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2749">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-2750">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2750">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-2751">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-2751">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-2752">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-2752">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="5baf9-2753">DXGI_FORMAT_R32 \_ <sup>PCs</sup> não tipados (39)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2753">DXGI_FORMAT_R32\_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="5baf9-2754">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-2754">Target</span></span> | <span data-ttu-id="5baf9-2755">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-2755">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-2756">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2756">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-2757">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-2757">32</span></span> |
| <span data-ttu-id="5baf9-2758">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-2758">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2760">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-2760">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2761">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-2761">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2762">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-2762">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2763">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2763">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2764">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2764">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2766">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2766">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2768">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2768">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2770">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-2770">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2772">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-2772">Shader ld</span></span> | \- |
| <span data-ttu-id="5baf9-2773">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2773">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2774">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2774">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2775">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2775">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2776">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-2776">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-2777">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-2777">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-2778">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-2778">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2780">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-2780">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-2781">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-2781">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-2782">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-2782">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-2783">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-2783">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-2784">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-2784">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-2785">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-2785">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-2786">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2786">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-2787">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-2787">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-2788">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2788">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-2789">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2789">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-2790">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2790">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-2791">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-2791">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-2792">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-2792">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-2793">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2793">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-2794">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-2794">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-2795">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2795">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-2796">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-2796">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2798">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-2798">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-2799">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-2799">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-2800">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-2800">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-2801">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-2801">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-2802">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-2802">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-2803">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-2803">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-2804">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-2804">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2806">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2806">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-2807">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2807">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-2808">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2808">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-2809">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-2809">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2811">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-2811">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_floatsupfcssup-40"></a><span data-ttu-id="5baf9-2812">\_<sup>FCS</sup> de DXGI_FORMAT_D32 float (40)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2812">DXGI_FORMAT_D32\_FLOAT<sup>FCS</sup> (40)</span></span>
| <span data-ttu-id="5baf9-2813">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-2813">Target</span></span> | <span data-ttu-id="5baf9-2814">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-2814">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-2815">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2815">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-2816">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-2816">32</span></span> |
| <span data-ttu-id="5baf9-2817">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-2817">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2819">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-2819">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2820">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-2820">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2821">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-2821">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2822">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2822">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2823">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2823">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2825">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2825">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2827">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2827">Texture3D</span></span> | \- |
| <span data-ttu-id="5baf9-2828">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-2828">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2830">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-2830">Shader ld</span></span> | \- |
| <span data-ttu-id="5baf9-2831">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2831">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2832">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2832">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2833">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2833">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2834">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-2834">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-2835">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-2835">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-2836">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-2836">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2838">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-2838">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-2839">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-2839">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-2840">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-2840">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-2841">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-2841">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-2842">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-2842">Depth/Stencil Target</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2844">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-2844">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-2845">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2845">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-2846">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-2846">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-2847">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2847">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-2848">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2848">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-2849">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2849">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-2850">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-2850">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-2851">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-2851">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-2852">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2852">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-2853">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-2853">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-2854">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2854">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-2855">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-2855">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2857">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-2857">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2859">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-2859">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2861">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-2861">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2863">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-2863">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-2864">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-2864">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-2865">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-2865">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-2866">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-2866">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2868">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2868">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-2869">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2869">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-2870">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2870">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-2871">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-2871">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2873">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-2873">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_floatsupfcssup-41"></a><span data-ttu-id="5baf9-2874">\_<sup>FCS</sup> de DXGI_FORMAT_R32 float (41)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2874">DXGI_FORMAT_R32\_FLOAT<sup>FCS</sup> (41)</span></span>
| <span data-ttu-id="5baf9-2875">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-2875">Target</span></span> | <span data-ttu-id="5baf9-2876">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-2876">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-2877">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2877">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-2878">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-2878">32</span></span> |
| <span data-ttu-id="5baf9-2879">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-2879">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2881">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-2881">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2883">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-2883">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2885">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-2885">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-2886">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2886">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2888">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2888">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2890">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2890">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2892">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2892">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2894">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-2894">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2896">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-2896">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2898">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2898">Shader sample (any filter)</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2900">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2900">Shader sample\_c (comparison filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2902">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2902">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2903">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-2903">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-2904">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-2904">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-2905">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-2905">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2907">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-2907">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2909">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-2909">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2911">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-2911">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2913">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-2913">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-2914">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-2914">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-2915">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-2915">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-2916">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2916">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-2917">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-2917">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-2918">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2918">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-2919">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2919">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-2920">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2920">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-2921">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-2921">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-2922">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-2922">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-2923">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2923">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-2924">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-2924">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-2925">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2925">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-2926">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-2926">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2928">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-2928">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2930">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-2930">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2932">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-2932">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2934">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-2934">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2936">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-2936">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2938">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-2938">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-2939">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-2939">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2941">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2941">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-2942">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2942">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-2943">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2943">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-2944">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-2944">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2946">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-2946">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_uintsupfcssup-42"></a><span data-ttu-id="5baf9-2947">\_<sup>FCS</sup> DXGI_FORMAT_R32 uint (42)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2947">DXGI_FORMAT_R32\_UINT<sup>FCS</sup> (42)</span></span>
| <span data-ttu-id="5baf9-2948">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-2948">Target</span></span> | <span data-ttu-id="5baf9-2949">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-2949">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-2950">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2950">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-2951">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-2951">32</span></span> |
| <span data-ttu-id="5baf9-2952">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-2952">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2954">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-2954">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2956">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-2956">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2958">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-2958">Input Assembler Index Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2960">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2960">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2962">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2962">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2964">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2964">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2966">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-2966">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2968">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-2968">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2970">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-2970">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2972">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2972">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2973">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2973">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2974">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-2974">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-2975">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-2975">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-2976">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-2976">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-2977">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-2977">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2979">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-2979">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-2980">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-2980">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2982">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-2982">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-2983">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-2983">Output Merger Logic Op</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-2985">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-2985">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-2986">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-2986">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-2987">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2987">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-2988">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-2988">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-2989">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2989">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-2990">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2990">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-2991">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2991">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-2992">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-2992">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-2993">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-2993">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-2994">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-2994">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-2995">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-2995">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-2996">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-2996">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-2997">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-2997">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-2999">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-2999">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3001">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-3001">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3003">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-3003">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3005">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-3005">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-3006">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-3006">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3008">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-3008">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-3009">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-3009">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3011">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3011">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-3012">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3012">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-3013">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3013">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-3014">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-3014">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3016">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-3016">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_sintsupfcssup-43"></a><span data-ttu-id="5baf9-3017">\_<sup>FCS</sup> DXGI_FORMAT_R32 Santo (43)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3017">DXGI_FORMAT_R32\_SINT<sup>FCS</sup> (43)</span></span>
| <span data-ttu-id="5baf9-3018">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-3018">Target</span></span> | <span data-ttu-id="5baf9-3019">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-3019">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-3020">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3020">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-3021">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-3021">32</span></span> |
| <span data-ttu-id="5baf9-3022">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-3022">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3024">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-3024">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3026">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3026">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3028">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3028">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3029">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3029">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3031">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3031">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3033">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3033">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3035">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3035">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3037">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-3037">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3039">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-3039">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3041">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3041">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3042">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3042">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3043">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3043">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3044">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-3044">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-3045">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-3045">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-3046">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-3046">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3048">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-3048">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-3049">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-3049">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3051">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-3051">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-3052">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-3052">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-3053">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-3053">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-3054">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-3054">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-3055">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3055">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-3056">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-3056">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-3057">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3057">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-3058">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3058">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-3059">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3059">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-3060">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-3060">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-3061">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-3061">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-3062">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3062">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-3063">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-3063">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-3064">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3064">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-3065">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-3065">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3067">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-3067">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3069">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-3069">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3071">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-3071">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3073">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-3073">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-3074">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-3074">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3076">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-3076">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-3077">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-3077">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3079">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3079">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-3080">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3080">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-3081">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3081">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-3082">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-3082">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3084">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-3084">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a><span data-ttu-id="5baf9-3085">DXGI_FORMAT_R24G8 \_ <sup>PCs</sup> não tipados (44)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3085">DXGI_FORMAT_R24G8\_TYPELESS<sup>PCS</sup> (44)</span></span>
| <span data-ttu-id="5baf9-3086">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-3086">Target</span></span> | <span data-ttu-id="5baf9-3087">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-3087">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-3088">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3088">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-3089">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-3089">32</span></span> |
| <span data-ttu-id="5baf9-3090">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-3090">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3092">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-3092">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3093">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3093">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3094">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3094">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3095">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3095">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3096">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3096">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3098">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3098">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3100">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3100">Texture3D</span></span> | \- |
| <span data-ttu-id="5baf9-3101">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-3101">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3103">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-3103">Shader ld</span></span> | \- |
| <span data-ttu-id="5baf9-3104">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3104">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3105">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3105">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3106">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3106">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3107">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-3107">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-3108">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-3108">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-3109">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-3109">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3111">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-3111">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-3112">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-3112">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-3113">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-3113">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-3114">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-3114">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-3115">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-3115">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-3116">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-3116">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-3117">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3117">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-3118">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-3118">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-3119">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3119">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-3120">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3120">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-3121">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3121">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-3122">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-3122">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-3123">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-3123">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-3124">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3124">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-3125">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-3125">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-3126">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3126">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-3127">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-3127">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3129">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-3129">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-3130">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-3130">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-3131">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-3131">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-3132">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-3132">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-3133">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-3133">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-3134">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-3134">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-3135">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-3135">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3137">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3137">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-3138">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3138">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-3139">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3139">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-3140">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-3140">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-3141">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-3141">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfcssup-45"></a><span data-ttu-id="5baf9-3142">\_FCS DXGI_FORMAT_D24 \_ UNORM \_ S8<sup></sup> uint (45)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3142">DXGI_FORMAT_D24\_UNORM\_S8\_UINT<sup>FCS</sup> (45)</span></span>
| <span data-ttu-id="5baf9-3143">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-3143">Target</span></span> | <span data-ttu-id="5baf9-3144">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-3144">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-3145">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3145">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-3146">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-3146">32</span></span> |
| <span data-ttu-id="5baf9-3147">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-3147">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3149">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-3149">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3150">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3150">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3151">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3151">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3152">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3152">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3153">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3153">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3155">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3155">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3157">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3157">Texture3D</span></span> | \- |
| <span data-ttu-id="5baf9-3158">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-3158">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3160">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-3160">Shader ld</span></span> | \- |
| <span data-ttu-id="5baf9-3161">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3161">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3162">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3162">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3163">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3163">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3164">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-3164">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-3165">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-3165">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-3166">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-3166">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3168">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-3168">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-3169">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-3169">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-3170">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-3170">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-3171">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-3171">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-3172">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-3172">Depth/Stencil Target</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3174">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-3174">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-3175">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3175">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-3176">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-3176">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-3177">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3177">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-3178">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3178">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-3179">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3179">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-3180">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-3180">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-3181">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-3181">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-3182">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3182">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-3183">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-3183">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-3184">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3184">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-3185">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-3185">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3187">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-3187">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3189">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-3189">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3191">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-3191">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3193">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-3193">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-3194">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-3194">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-3195">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-3195">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-3196">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-3196">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3198">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3198">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-3199">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3199">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-3200">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3200">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-3201">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-3201">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-3202">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-3202">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfcssup-46"></a><span data-ttu-id="5baf9-3203">\_FCS com \_ \_ tipo de UNORM<sup></sup> x8 (46) DXGI_FORMAT_R24</span><span class="sxs-lookup"><span data-stu-id="5baf9-3203">DXGI_FORMAT_R24\_UNORM\_X8\_TYPELESS<sup>FCS</sup> (46)</span></span>
| <span data-ttu-id="5baf9-3204">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-3204">Target</span></span> | <span data-ttu-id="5baf9-3205">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-3205">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-3206">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3206">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-3207">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-3207">32</span></span> |
| <span data-ttu-id="5baf9-3208">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-3208">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3210">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-3210">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3211">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3211">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3212">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3212">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3213">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3213">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3214">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3214">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3216">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3216">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3218">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3218">Texture3D</span></span> | \- |
| <span data-ttu-id="5baf9-3219">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-3219">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3221">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-3221">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3223">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3223">Shader sample (any filter)</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3225">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3225">Shader sample\_c (comparison filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3227">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3227">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3228">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-3228">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-3229">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-3229">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-3230">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-3230">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3232">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-3232">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-3233">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-3233">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-3234">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-3234">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-3235">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-3235">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-3236">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-3236">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-3237">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-3237">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-3238">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3238">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-3239">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-3239">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-3240">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3240">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-3241">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3241">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-3242">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3242">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-3243">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-3243">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-3244">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-3244">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-3245">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3245">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-3246">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-3246">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-3247">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3247">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-3248">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-3248">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3250">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-3250">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-3251">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-3251">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-3252">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-3252">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-3253">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-3253">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-3254">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-3254">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-3255">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-3255">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-3256">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-3256">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3258">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3258">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-3259">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3259">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-3260">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3260">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-3261">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-3261">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-3262">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-3262">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfcssup-47"></a><span data-ttu-id="5baf9-3263">\_FCS uint não tipado \_ de DXGI_FORMAT_X24 \_ (47)<sup></sup></span><span class="sxs-lookup"><span data-stu-id="5baf9-3263">DXGI_FORMAT_X24\_TYPELESS\_G8\_UINT<sup>FCS</sup> (47)</span></span>
| <span data-ttu-id="5baf9-3264">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-3264">Target</span></span> | <span data-ttu-id="5baf9-3265">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-3265">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-3266">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3266">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-3267">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-3267">32</span></span> |
| <span data-ttu-id="5baf9-3268">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-3268">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3270">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-3270">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3271">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3271">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3272">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3272">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3273">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3273">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3274">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3274">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3276">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3276">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3278">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3278">Texture3D</span></span> | \- |
| <span data-ttu-id="5baf9-3279">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-3279">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3281">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-3281">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3283">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3283">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3284">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3284">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3285">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3285">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3286">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-3286">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-3287">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-3287">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-3288">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-3288">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3290">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-3290">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-3291">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-3291">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-3292">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-3292">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-3293">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-3293">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-3294">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-3294">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-3295">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-3295">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-3296">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3296">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-3297">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-3297">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-3298">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3298">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-3299">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3299">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-3300">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3300">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-3301">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-3301">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-3302">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-3302">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-3303">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3303">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-3304">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-3304">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-3305">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3305">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-3306">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-3306">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3308">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-3308">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-3309">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-3309">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-3310">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-3310">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-3311">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-3311">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-3312">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-3312">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-3313">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-3313">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-3314">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-3314">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3316">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3316">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-3317">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3317">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-3318">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3318">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-3319">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-3319">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-3320">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-3320">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="5baf9-3321">DXGI_FORMAT_R8G8 \_ <sup>PCs</sup> não tipados (48)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3321">DXGI_FORMAT_R8G8\_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="5baf9-3322">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-3322">Target</span></span> | <span data-ttu-id="5baf9-3323">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-3323">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-3324">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3324">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-3325">16</span><span class="sxs-lookup"><span data-stu-id="5baf9-3325">16</span></span> |
| <span data-ttu-id="5baf9-3326">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-3326">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3328">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-3328">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3329">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3329">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3330">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3330">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3331">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3331">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3332">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3332">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3334">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3334">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3336">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3336">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3338">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-3338">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3340">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-3340">Shader ld</span></span> | \- |
| <span data-ttu-id="5baf9-3341">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3341">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3342">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3342">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3343">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3343">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3344">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-3344">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-3345">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-3345">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-3346">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-3346">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3348">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-3348">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-3349">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-3349">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-3350">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-3350">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-3351">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-3351">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-3352">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-3352">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-3353">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-3353">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-3354">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3354">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-3355">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-3355">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-3356">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3356">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-3357">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3357">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-3358">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3358">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-3359">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-3359">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-3360">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-3360">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-3361">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3361">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-3362">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-3362">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-3363">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3363">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-3364">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-3364">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3366">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-3366">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-3367">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-3367">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-3368">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-3368">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-3369">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-3369">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-3370">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-3370">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-3371">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-3371">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-3372">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-3372">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3374">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3374">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-3375">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3375">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-3376">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3376">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-3377">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-3377">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-3378">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-3378">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_unormsupfcssup-49"></a><span data-ttu-id="5baf9-3379">\_UNORM<sup>FCS</sup> de DXGI_FORMAT_R8G8 (49)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3379">DXGI_FORMAT_R8G8\_UNORM<sup>FCS</sup> (49)</span></span>
| <span data-ttu-id="5baf9-3380">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-3380">Target</span></span> | <span data-ttu-id="5baf9-3381">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-3381">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-3382">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3382">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-3383">16</span><span class="sxs-lookup"><span data-stu-id="5baf9-3383">16</span></span> |
| <span data-ttu-id="5baf9-3384">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-3384">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3386">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-3386">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3388">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3388">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3390">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3390">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3391">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3391">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3392">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3392">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3394">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3394">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3396">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3396">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3398">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-3398">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3400">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-3400">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3402">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3402">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3404">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3404">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3405">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3405">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3406">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-3406">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-3407">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-3407">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-3408">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-3408">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3410">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-3410">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3412">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-3412">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3414">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-3414">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3416">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-3416">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-3417">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-3417">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-3418">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-3418">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-3419">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3419">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-3420">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-3420">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-3421">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3421">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-3422">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3422">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-3423">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3423">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-3424">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-3424">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-3425">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-3425">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-3426">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3426">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-3427">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-3427">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-3428">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3428">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-3429">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-3429">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3431">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-3431">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3433">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-3433">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3435">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-3435">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3437">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-3437">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3439">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-3439">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3441">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-3441">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-3442">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-3442">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3444">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3444">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-3445">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3445">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-3446">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3446">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-3447">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-3447">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3449">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-3449">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_uintsupfcssup-50"></a><span data-ttu-id="5baf9-3450">\_<sup>FCS</sup> DXGI_FORMAT_R8G8 uint (50)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3450">DXGI_FORMAT_R8G8\_UINT<sup>FCS</sup> (50)</span></span>
| <span data-ttu-id="5baf9-3451">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-3451">Target</span></span> | <span data-ttu-id="5baf9-3452">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-3452">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-3453">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3453">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-3454">16</span><span class="sxs-lookup"><span data-stu-id="5baf9-3454">16</span></span> |
| <span data-ttu-id="5baf9-3455">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-3455">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3457">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-3457">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3459">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3459">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3461">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3461">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3462">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3462">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3463">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3463">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3465">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3465">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3467">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3467">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3469">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-3469">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3471">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-3471">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3473">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3473">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3474">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3474">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3475">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3475">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3476">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-3476">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-3477">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-3477">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-3478">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-3478">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3480">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-3480">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-3481">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-3481">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3483">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-3483">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-3484">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-3484">Output Merger Logic Op</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3486">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-3486">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-3487">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-3487">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-3488">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3488">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-3489">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-3489">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-3490">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3490">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-3491">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3491">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-3492">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3492">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-3493">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-3493">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-3494">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-3494">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-3495">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3495">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-3496">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-3496">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-3497">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3497">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-3498">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-3498">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3500">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-3500">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3502">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-3502">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3504">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-3504">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3506">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-3506">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-3507">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-3507">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3509">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-3509">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-3510">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-3510">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3512">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3512">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-3513">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3513">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-3514">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3514">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-3515">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-3515">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-3516">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-3516">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_snormsupfcssup-51"></a><span data-ttu-id="5baf9-3517">\_SNORM<sup>FCS</sup> de DXGI_FORMAT_R8G8 (51)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3517">DXGI_FORMAT_R8G8\_SNORM<sup>FCS</sup> (51)</span></span>
| <span data-ttu-id="5baf9-3518">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-3518">Target</span></span> | <span data-ttu-id="5baf9-3519">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-3519">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-3520">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3520">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-3521">16</span><span class="sxs-lookup"><span data-stu-id="5baf9-3521">16</span></span> |
| <span data-ttu-id="5baf9-3522">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-3522">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3524">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-3524">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3526">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3526">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3528">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3528">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3529">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3529">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3530">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3530">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3532">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3532">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3534">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3534">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3536">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-3536">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3538">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-3538">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3540">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3540">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3542">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3542">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3543">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3543">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3544">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-3544">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-3545">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-3545">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-3546">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-3546">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3548">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-3548">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3550">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-3550">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3552">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-3552">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-3553">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-3553">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-3554">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-3554">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-3555">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-3555">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-3556">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3556">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-3557">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-3557">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-3558">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3558">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-3559">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3559">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-3560">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3560">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-3561">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-3561">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-3562">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-3562">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-3563">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3563">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-3564">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-3564">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-3565">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3565">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-3566">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-3566">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3568">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-3568">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3570">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-3570">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3572">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-3572">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3574">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-3574">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3576">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-3576">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3578">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-3578">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-3579">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-3579">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3581">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3581">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-3582">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3582">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-3583">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3583">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-3584">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-3584">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-3585">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-3585">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_sintsupfcssup-52"></a><span data-ttu-id="5baf9-3586">\_<sup>FCS</sup> DXGI_FORMAT_R8G8 Santo (52)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3586">DXGI_FORMAT_R8G8\_SINT<sup>FCS</sup> (52)</span></span>
| <span data-ttu-id="5baf9-3587">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-3587">Target</span></span> | <span data-ttu-id="5baf9-3588">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-3588">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-3589">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3589">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-3590">16</span><span class="sxs-lookup"><span data-stu-id="5baf9-3590">16</span></span> |
| <span data-ttu-id="5baf9-3591">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-3591">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3593">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-3593">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3595">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3595">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3597">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3597">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3598">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3598">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3599">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3599">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3601">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3601">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3603">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3603">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-3605">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3607">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-3607">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3609">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3609">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3610">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3610">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3611">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3611">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3612">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-3612">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-3613">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-3613">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-3614">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-3614">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3616">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-3616">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-3617">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-3617">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3619">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-3619">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-3620">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-3620">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-3621">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-3621">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-3622">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-3622">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-3623">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3623">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-3624">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-3624">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-3625">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3625">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-3626">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3626">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-3627">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3627">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-3628">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-3628">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-3629">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-3629">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-3630">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3630">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-3631">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-3631">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-3632">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3632">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-3633">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-3633">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3635">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-3635">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3637">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-3637">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3639">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-3639">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3641">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-3641">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-3642">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-3642">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3644">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-3644">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-3645">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-3645">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3647">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3647">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-3648">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3648">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-3649">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3649">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-3650">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-3650">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-3651">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-3651">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="5baf9-3652">DXGI_FORMAT_R16 \_ <sup>PCs</sup> não tipados (53)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3652">DXGI_FORMAT_R16\_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="5baf9-3653">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-3653">Target</span></span> | <span data-ttu-id="5baf9-3654">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-3654">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-3655">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3655">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-3656">16</span><span class="sxs-lookup"><span data-stu-id="5baf9-3656">16</span></span> |
| <span data-ttu-id="5baf9-3657">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-3657">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3659">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-3659">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3660">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3660">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3661">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3661">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3662">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3662">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3663">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3663">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3665">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3665">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3667">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3667">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3669">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-3669">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3671">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-3671">Shader ld</span></span> | \- |
| <span data-ttu-id="5baf9-3672">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3672">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3673">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3673">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3674">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3674">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3675">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-3675">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-3676">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-3676">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-3677">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-3677">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3679">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-3679">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-3680">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-3680">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-3681">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-3681">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-3682">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-3682">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-3683">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-3683">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-3684">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-3684">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-3685">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3685">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-3686">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-3686">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-3687">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3687">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-3688">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3688">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-3689">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3689">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-3690">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-3690">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-3691">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-3691">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-3692">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3692">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-3693">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-3693">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-3694">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3694">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-3695">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-3695">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3697">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-3697">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-3698">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-3698">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-3699">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-3699">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-3700">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-3700">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-3701">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-3701">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-3702">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-3702">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-3703">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-3703">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3705">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3705">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-3706">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3706">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-3707">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3707">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-3708">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-3708">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3710">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-3710">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_floatsupfcssup-54"></a><span data-ttu-id="5baf9-3711">\_<sup>FCS</sup> de DXGI_FORMAT_R16 float (54)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3711">DXGI_FORMAT_R16\_FLOAT<sup>FCS</sup> (54)</span></span>
| <span data-ttu-id="5baf9-3712">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-3712">Target</span></span> | <span data-ttu-id="5baf9-3713">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-3713">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-3714">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3714">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-3715">16</span><span class="sxs-lookup"><span data-stu-id="5baf9-3715">16</span></span> |
| <span data-ttu-id="5baf9-3716">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-3716">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3718">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-3718">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3720">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3720">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3722">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3722">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3723">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3723">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3724">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3724">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3726">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3726">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3728">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3728">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3730">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-3730">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3732">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-3732">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3734">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3734">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3736">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3736">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3737">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3737">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3738">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-3738">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-3739">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-3739">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-3740">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-3740">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3742">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-3742">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3744">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-3744">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3746">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-3746">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3748">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-3748">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-3749">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-3749">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-3750">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-3750">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-3751">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3751">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-3752">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-3752">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-3753">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3753">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-3754">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3754">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-3755">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3755">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-3756">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-3756">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-3757">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-3757">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-3758">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3758">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-3759">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-3759">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-3760">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3760">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-3761">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-3761">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3763">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-3763">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3765">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-3765">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3767">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-3767">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3769">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-3769">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3771">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-3771">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3773">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-3773">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-3774">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-3774">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3776">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3776">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-3777">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3777">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-3778">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3778">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-3779">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-3779">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3781">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-3781">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d16_unormsupfcssup-55"></a><span data-ttu-id="5baf9-3782">\_UNORM<sup>FCS</sup> de DXGI_FORMAT_D16 (55)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3782">DXGI_FORMAT_D16\_UNORM<sup>FCS</sup> (55)</span></span>
| <span data-ttu-id="5baf9-3783">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-3783">Target</span></span> | <span data-ttu-id="5baf9-3784">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-3784">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-3785">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3785">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-3786">16</span><span class="sxs-lookup"><span data-stu-id="5baf9-3786">16</span></span> |
| <span data-ttu-id="5baf9-3787">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-3787">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3789">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-3789">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3790">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3790">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3791">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3791">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3792">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3792">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3793">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3793">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3795">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3795">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3797">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3797">Texture3D</span></span> | \- |
| <span data-ttu-id="5baf9-3798">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-3798">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3800">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-3800">Shader ld</span></span> | \- |
| <span data-ttu-id="5baf9-3801">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3801">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3802">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3802">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3803">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3803">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3804">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-3804">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-3805">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-3805">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-3806">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-3806">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3808">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-3808">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-3809">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-3809">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-3810">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-3810">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-3811">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-3811">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-3812">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-3812">Depth/Stencil Target</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3814">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-3814">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-3815">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3815">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-3816">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-3816">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-3817">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3817">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-3818">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3818">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-3819">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3819">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-3820">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-3820">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-3821">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-3821">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-3822">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3822">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-3823">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-3823">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-3824">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3824">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-3825">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-3825">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3827">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-3827">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3829">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-3829">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3831">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-3831">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3833">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-3833">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-3834">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-3834">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-3835">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-3835">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-3836">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-3836">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3838">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3838">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-3839">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3839">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-3840">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3840">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-3841">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-3841">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3843">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-3843">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_unormsupfcssup-56"></a><span data-ttu-id="5baf9-3844">\_UNORM<sup>FCS</sup> de DXGI_FORMAT_R16 (56)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3844">DXGI_FORMAT_R16\_UNORM<sup>FCS</sup> (56)</span></span>
| <span data-ttu-id="5baf9-3845">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-3845">Target</span></span> | <span data-ttu-id="5baf9-3846">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-3846">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-3847">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3847">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-3848">16</span><span class="sxs-lookup"><span data-stu-id="5baf9-3848">16</span></span> |
| <span data-ttu-id="5baf9-3849">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-3849">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3851">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-3851">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3853">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3853">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3855">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3855">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3856">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3856">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3857">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3857">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3859">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3859">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3861">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3861">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3863">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-3863">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3865">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-3865">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3867">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3867">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3869">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3869">Shader sample\_c (comparison filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3871">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3871">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3872">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-3872">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-3873">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-3873">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-3874">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-3874">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3876">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-3876">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3878">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-3878">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3880">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-3880">Blendable RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3882">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-3882">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-3883">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-3883">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-3884">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-3884">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-3885">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3885">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-3886">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-3886">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-3887">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3887">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-3888">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3888">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-3889">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3889">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-3890">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-3890">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-3891">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-3891">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-3892">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3892">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-3893">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-3893">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-3894">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3894">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-3895">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-3895">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3897">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-3897">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3899">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-3899">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3901">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-3901">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3903">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-3903">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3905">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-3905">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3907">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-3907">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-3908">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-3908">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3910">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3910">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-3911">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3911">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-3912">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3912">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-3913">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-3913">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3915">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-3915">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_uintsupfcssup-57"></a><span data-ttu-id="5baf9-3916">\_<sup>FCS</sup> DXGI_FORMAT_R16 uint (57)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3916">DXGI_FORMAT_R16\_UINT<sup>FCS</sup> (57)</span></span>
| <span data-ttu-id="5baf9-3917">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-3917">Target</span></span> | <span data-ttu-id="5baf9-3918">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-3918">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-3919">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3919">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-3920">16</span><span class="sxs-lookup"><span data-stu-id="5baf9-3920">16</span></span> |
| <span data-ttu-id="5baf9-3921">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-3921">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3923">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-3923">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3925">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3925">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3927">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3927">Input Assembler Index Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3929">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3929">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3930">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3930">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3932">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3932">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3934">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3934">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3936">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-3936">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3938">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-3938">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3940">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3940">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3941">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3941">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3942">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3942">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-3943">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-3943">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-3944">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-3944">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-3945">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-3945">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3947">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-3947">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-3948">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-3948">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3950">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-3950">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-3951">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-3951">Output Merger Logic Op</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3953">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-3953">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-3954">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-3954">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-3955">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3955">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-3956">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-3956">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-3957">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3957">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-3958">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3958">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-3959">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3959">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-3960">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-3960">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-3961">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-3961">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-3962">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-3962">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-3963">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-3963">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-3964">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3964">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-3965">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-3965">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3967">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-3967">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3969">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-3969">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3971">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-3971">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3973">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-3973">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-3974">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-3974">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-3976">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-3976">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-3977">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-3977">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3979">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3979">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-3980">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3980">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-3981">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3981">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-3982">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-3982">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3984">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-3984">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_snormsupfcssup-58"></a><span data-ttu-id="5baf9-3985">\_SNORM<sup>FCS</sup> de DXGI_FORMAT_R16 (58)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3985">DXGI_FORMAT_R16\_SNORM<sup>FCS</sup> (58)</span></span>
| <span data-ttu-id="5baf9-3986">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-3986">Target</span></span> | <span data-ttu-id="5baf9-3987">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-3987">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-3988">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-3988">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-3989">16</span><span class="sxs-lookup"><span data-stu-id="5baf9-3989">16</span></span> |
| <span data-ttu-id="5baf9-3990">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-3990">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3992">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-3992">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3994">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3994">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-3996">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-3996">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3997">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-3997">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-3998">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-3998">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4000">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4000">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4002">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4002">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4004">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-4004">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4006">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-4006">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4008">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4008">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4010">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4010">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4011">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4011">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4012">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-4012">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-4013">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-4013">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-4014">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4014">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4016">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4016">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4018">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4018">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4020">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-4020">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4021">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-4021">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-4022">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-4022">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-4023">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-4023">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4024">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4024">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4025">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4025">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-4026">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4026">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-4027">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4027">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-4028">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4028">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-4029">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-4029">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-4030">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-4030">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-4031">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4031">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-4032">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-4032">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4033">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4033">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4034">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-4034">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4036">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4036">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-4038">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-4038">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-4040">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-4040">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-4042">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-4042">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4044">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-4044">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-4046">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-4046">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-4047">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-4047">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4049">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4049">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-4050">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4050">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-4051">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4051">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-4052">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4052">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4054">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-4054">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_sintsupfcssup-59"></a><span data-ttu-id="5baf9-4055">\_<sup>FCS</sup> DXGI_FORMAT_R16 Santo (59)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4055">DXGI_FORMAT_R16\_SINT<sup>FCS</sup> (59)</span></span>
| <span data-ttu-id="5baf9-4056">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-4056">Target</span></span> | <span data-ttu-id="5baf9-4057">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-4057">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-4058">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4058">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-4059">16</span><span class="sxs-lookup"><span data-stu-id="5baf9-4059">16</span></span> |
| <span data-ttu-id="5baf9-4060">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-4060">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4062">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-4062">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4064">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-4064">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4066">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-4066">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4067">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4067">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4068">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4068">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4070">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4070">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4072">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4072">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4074">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-4074">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4076">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-4076">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4078">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4078">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4079">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4079">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4080">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4080">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4081">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-4081">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-4082">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-4082">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-4083">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4083">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4085">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4085">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-4086">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4086">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4088">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-4088">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4089">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-4089">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-4090">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-4090">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-4091">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-4091">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4092">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4092">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4093">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4093">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-4094">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4094">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-4095">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4095">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-4096">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4096">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-4097">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-4097">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-4098">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-4098">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-4099">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4099">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-4100">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-4100">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4101">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4101">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4102">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-4102">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4104">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4104">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-4106">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-4106">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-4108">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-4108">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-4110">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-4110">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-4111">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-4111">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-4113">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-4113">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-4114">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-4114">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4116">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4116">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-4117">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4117">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-4118">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4118">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-4119">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4119">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4121">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-4121">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="5baf9-4122">DXGI_FORMAT_R8 \_ <sup>PCs</sup> não tipados (60)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4122">DXGI_FORMAT_R8\_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="5baf9-4123">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-4123">Target</span></span> | <span data-ttu-id="5baf9-4124">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-4124">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-4125">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4125">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-4126">8</span><span class="sxs-lookup"><span data-stu-id="5baf9-4126">8</span></span> |
| <span data-ttu-id="5baf9-4127">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-4127">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4129">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-4129">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4130">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-4130">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4131">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-4131">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4132">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4132">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4133">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4135">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4135">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4137">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4137">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4139">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-4139">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4141">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-4141">Shader ld</span></span> | \- |
| <span data-ttu-id="5baf9-4142">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4142">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4143">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4143">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4144">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4144">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4145">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-4145">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-4146">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-4146">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-4147">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4147">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4149">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4149">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-4150">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4150">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4151">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-4151">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4152">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-4152">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-4153">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-4153">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-4154">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-4154">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4155">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4155">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4156">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4156">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-4157">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4157">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-4158">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4158">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-4159">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4159">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-4160">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-4160">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-4161">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-4161">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-4162">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4162">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-4163">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-4163">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4164">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4164">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4165">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-4165">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4167">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4167">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4168">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-4168">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4169">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-4169">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-4170">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-4170">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-4171">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-4171">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-4172">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-4172">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-4173">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-4173">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4175">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4175">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-4176">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4176">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-4177">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4177">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-4178">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4178">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4180">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-4180">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_unormsupfcssup-61"></a><span data-ttu-id="5baf9-4181">\_UNORM<sup>FCS</sup> de DXGI_FORMAT_R8 (61)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4181">DXGI_FORMAT_R8\_UNORM<sup>FCS</sup> (61)</span></span>
| <span data-ttu-id="5baf9-4182">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-4182">Target</span></span> | <span data-ttu-id="5baf9-4183">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-4183">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-4184">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4184">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-4185">8</span><span class="sxs-lookup"><span data-stu-id="5baf9-4185">8</span></span> |
| <span data-ttu-id="5baf9-4186">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-4186">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4188">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-4188">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4190">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-4190">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4192">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-4192">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4193">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4193">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4194">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4194">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4196">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4196">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4198">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4198">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4200">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-4200">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4202">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-4202">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4204">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4204">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4206">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4206">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4207">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4207">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4208">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-4208">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-4209">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-4209">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-4210">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4210">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4212">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4212">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4214">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4214">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4216">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-4216">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4218">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-4218">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-4219">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-4219">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-4220">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-4220">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4221">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4221">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4222">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4222">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-4223">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4223">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-4224">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4224">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-4225">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4225">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-4226">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-4226">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-4227">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-4227">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-4228">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4228">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-4229">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-4229">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4230">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4230">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4231">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-4231">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4233">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4233">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-4235">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-4235">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-4237">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-4237">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-4239">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-4239">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4241">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-4241">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-4243">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-4243">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-4244">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-4244">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4246">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4246">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-4247">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4247">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-4248">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4248">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-4249">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4249">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4251">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-4251">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_uintsupfcssup-62"></a><span data-ttu-id="5baf9-4252">\_<sup>FCS</sup> DXGI_FORMAT_R8 uint (62)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4252">DXGI_FORMAT_R8\_UINT<sup>FCS</sup> (62)</span></span>
| <span data-ttu-id="5baf9-4253">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-4253">Target</span></span> | <span data-ttu-id="5baf9-4254">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-4254">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-4255">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4255">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-4256">8</span><span class="sxs-lookup"><span data-stu-id="5baf9-4256">8</span></span> |
| <span data-ttu-id="5baf9-4257">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-4257">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4259">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-4259">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4261">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-4261">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4263">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-4263">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4264">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4264">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4265">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4265">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4267">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4267">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4269">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4269">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4271">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-4271">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4273">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-4273">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4275">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4275">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4276">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4276">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4277">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4277">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4278">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-4278">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-4279">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-4279">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-4280">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4280">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4282">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4282">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-4283">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4283">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4285">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-4285">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4286">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-4286">Output Merger Logic Op</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-4288">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-4288">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-4289">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-4289">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4290">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4290">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4291">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4291">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-4292">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4292">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-4293">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4293">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-4294">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4294">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-4295">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-4295">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-4296">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-4296">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-4297">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4297">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-4298">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-4298">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4299">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4299">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4300">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-4300">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4302">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4302">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-4304">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-4304">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-4306">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-4306">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-4308">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-4308">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-4309">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-4309">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-4311">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-4311">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-4312">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-4312">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4314">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4314">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-4315">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4315">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-4316">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4316">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-4317">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4317">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4319">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-4319">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_snormsupfcssup-63"></a><span data-ttu-id="5baf9-4320">\_SNORM<sup>FCS</sup> de DXGI_FORMAT_R8 (63)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4320">DXGI_FORMAT_R8\_SNORM<sup>FCS</sup> (63)</span></span>
| <span data-ttu-id="5baf9-4321">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-4321">Target</span></span> | <span data-ttu-id="5baf9-4322">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-4322">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-4323">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4323">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-4324">8</span><span class="sxs-lookup"><span data-stu-id="5baf9-4324">8</span></span> |
| <span data-ttu-id="5baf9-4325">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-4325">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4327">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-4327">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4329">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-4329">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4331">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-4331">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4332">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4332">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4333">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4333">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4335">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4335">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4337">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4337">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4339">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-4339">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4341">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-4341">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4343">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4343">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4345">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4345">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4346">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4346">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4347">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-4347">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-4348">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-4348">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-4349">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4349">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4351">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4351">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4353">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4353">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4355">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-4355">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4356">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-4356">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-4357">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-4357">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-4358">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-4358">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4359">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4359">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4360">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4360">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-4361">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4361">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-4362">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4362">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-4363">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4363">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-4364">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-4364">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-4365">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-4365">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-4366">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4366">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-4367">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-4367">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4368">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4368">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4369">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-4369">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4371">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4371">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-4373">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-4373">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-4375">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-4375">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-4377">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-4377">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4379">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-4379">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-4381">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-4381">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-4382">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-4382">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4384">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4384">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-4385">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4385">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-4386">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4386">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-4387">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4387">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4389">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-4389">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_sintsupfcssup-64"></a><span data-ttu-id="5baf9-4390">\_<sup>FCS</sup> DXGI_FORMAT_R8 Santo (64)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4390">DXGI_FORMAT_R8\_SINT<sup>FCS</sup> (64)</span></span>
| <span data-ttu-id="5baf9-4391">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-4391">Target</span></span> | <span data-ttu-id="5baf9-4392">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-4392">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-4393">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4393">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-4394">8</span><span class="sxs-lookup"><span data-stu-id="5baf9-4394">8</span></span> |
| <span data-ttu-id="5baf9-4395">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-4395">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4397">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-4397">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4399">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-4399">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4401">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-4401">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4402">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4402">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4403">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4403">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4405">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4405">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4407">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4407">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4409">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-4409">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4411">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-4411">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4413">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4413">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4414">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4414">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4415">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4415">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4416">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-4416">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-4417">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-4417">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-4418">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4418">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4420">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4420">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-4421">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4421">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4423">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-4423">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4424">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-4424">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-4425">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-4425">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-4426">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-4426">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4427">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4427">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4428">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4428">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-4429">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4429">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-4430">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4430">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-4431">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4431">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-4432">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-4432">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-4433">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-4433">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-4434">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4434">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-4435">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-4435">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4436">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4436">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4437">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-4437">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4439">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4439">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-4441">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-4441">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-4443">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-4443">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-4445">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-4445">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-4446">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-4446">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-4448">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-4448">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-4449">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-4449">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4451">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4451">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-4452">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4452">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-4453">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4453">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-4454">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4454">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4456">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-4456">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="5baf9-4457">DXGI_FORMAT_A8 \_ UNORM<sup>FNS</sup> (65)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4457">DXGI_FORMAT_A8\_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="5baf9-4458">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-4458">Target</span></span> | <span data-ttu-id="5baf9-4459">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-4459">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-4460">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4460">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-4461">8</span><span class="sxs-lookup"><span data-stu-id="5baf9-4461">8</span></span> |
| <span data-ttu-id="5baf9-4462">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-4462">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4464">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-4464">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4465">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-4465">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4466">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-4466">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4467">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4467">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4468">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4468">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4470">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4470">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4472">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4472">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4474">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-4474">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4476">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-4476">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4478">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4478">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4480">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4480">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4481">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4481">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4482">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-4482">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-4483">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-4483">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-4484">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4484">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4486">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4486">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4488">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4488">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4490">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-4490">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4492">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-4492">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-4493">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-4493">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-4494">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-4494">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4495">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4495">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4496">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4496">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-4497">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4497">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-4498">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4498">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-4499">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4499">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-4500">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-4500">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-4501">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-4501">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-4502">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4502">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-4503">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-4503">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4504">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4504">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4505">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-4505">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4507">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4507">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-4509">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-4509">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-4511">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-4511">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-4513">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-4513">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4515">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-4515">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-4517">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-4517">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-4518">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-4518">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="5baf9-4519">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4519">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-4520">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4520">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-4521">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4521">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-4522">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4522">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4524">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-4524">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="5baf9-4525">DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4525">DXGI_FORMAT_R9G9B9E5\_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="5baf9-4526">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-4526">Target</span></span> | <span data-ttu-id="5baf9-4527">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-4527">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-4528">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4528">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-4529">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-4529">32</span></span> |
| <span data-ttu-id="5baf9-4530">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-4530">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4532">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-4532">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4533">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-4533">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4534">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-4534">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4535">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4535">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4536">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4536">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4538">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4538">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4540">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4540">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4542">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-4542">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4544">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-4544">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4546">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4546">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4548">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4548">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4549">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4549">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4550">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-4550">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-4551">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-4551">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-4552">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4552">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4554">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4554">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-4555">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4555">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4556">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-4556">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4557">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-4557">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-4558">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-4558">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-4559">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-4559">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4560">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4560">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4561">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4561">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-4562">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4562">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-4563">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4563">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-4564">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4564">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-4565">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-4565">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-4566">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-4566">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-4567">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4567">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-4568">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-4568">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4569">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4569">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4570">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-4570">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4572">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4572">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4573">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-4573">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4574">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-4574">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-4575">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-4575">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-4576">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-4576">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-4577">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-4577">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-4578">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-4578">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="5baf9-4579">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4579">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-4580">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4580">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-4581">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4581">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-4582">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4582">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-4583">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-4583">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="5baf9-4584">DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4584">DXGI_FORMAT_R8G8\_B8G8\_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="5baf9-4585">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-4585">Target</span></span> | <span data-ttu-id="5baf9-4586">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-4586">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-4587">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4587">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-4588">16</span><span class="sxs-lookup"><span data-stu-id="5baf9-4588">16</span></span> |
| <span data-ttu-id="5baf9-4589">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-4589">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4591">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-4591">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4592">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-4592">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4593">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-4593">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4594">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4594">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4595">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4595">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4597">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4597">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4599">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4599">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4601">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-4601">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4603">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-4603">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4605">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4605">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4607">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4607">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4608">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4608">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4609">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-4609">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-4610">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-4610">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-4611">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4611">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4613">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4613">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-4614">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4614">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4615">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-4615">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4616">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-4616">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-4617">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-4617">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-4618">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-4618">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4619">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4619">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4620">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4620">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-4621">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4621">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-4622">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4622">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-4623">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4623">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-4624">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-4624">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-4625">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-4625">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-4626">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4626">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-4627">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-4627">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4628">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4628">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4629">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-4629">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4631">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4631">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4632">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-4632">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4633">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-4633">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-4634">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-4634">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-4635">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-4635">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-4636">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-4636">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-4637">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-4637">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="5baf9-4638">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4638">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-4639">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4639">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-4640">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4640">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-4641">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4641">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-4642">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-4642">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="5baf9-4643">DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>FNC</sup> (69)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4643">DXGI_FORMAT_G8R8\_G8B8\_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="5baf9-4644">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-4644">Target</span></span> | <span data-ttu-id="5baf9-4645">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-4645">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-4646">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4646">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-4647">16</span><span class="sxs-lookup"><span data-stu-id="5baf9-4647">16</span></span> |
| <span data-ttu-id="5baf9-4648">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-4648">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4650">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-4650">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4651">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-4651">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4652">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-4652">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4653">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4653">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4654">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4654">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4656">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4656">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4658">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4658">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4660">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-4660">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4662">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-4662">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4664">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4664">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4666">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4666">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4667">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4667">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4668">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-4668">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-4669">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-4669">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-4670">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4670">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4672">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4672">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-4673">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4673">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4674">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-4674">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4675">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-4675">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-4676">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-4676">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-4677">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-4677">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4678">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4678">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4679">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4679">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-4680">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4680">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-4681">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4681">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-4682">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4682">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-4683">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-4683">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-4684">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-4684">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-4685">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4685">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-4686">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-4686">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4687">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4687">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4688">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-4688">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4690">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4690">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4691">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-4691">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4692">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-4692">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-4693">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-4693">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-4694">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-4694">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-4695">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-4695">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-4696">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-4696">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="5baf9-4697">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4697">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-4698">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4698">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-4699">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4699">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-4700">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4700">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-4701">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-4701">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="5baf9-4702">DXGI_FORMAT_BC1 \_ <sup>PCC</sup> de tipo (70)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4702">DXGI_FORMAT_BC1\_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="5baf9-4703">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-4703">Target</span></span> | <span data-ttu-id="5baf9-4704">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-4704">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-4705">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4705">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-4706">4</span><span class="sxs-lookup"><span data-stu-id="5baf9-4706">4</span></span> |
| <span data-ttu-id="5baf9-4707">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-4707">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4709">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-4709">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4710">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-4710">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4711">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-4711">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4712">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4712">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4713">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4713">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-4714">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4714">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4716">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4716">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4718">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-4718">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4720">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-4720">Shader ld</span></span> | \- |
| <span data-ttu-id="5baf9-4721">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4721">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4722">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4722">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4723">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4723">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4724">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-4724">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-4725">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-4725">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-4726">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4726">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4728">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4728">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-4729">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4729">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4730">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-4730">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4731">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-4731">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-4732">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-4732">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-4733">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-4733">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4734">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4734">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4735">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4735">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-4736">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4736">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-4737">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4737">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-4738">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4738">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-4739">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-4739">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-4740">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-4740">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-4741">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4741">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-4742">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-4742">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4743">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4743">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4744">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-4744">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4746">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4746">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4747">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-4747">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4748">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-4748">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-4749">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-4749">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-4750">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-4750">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-4751">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-4751">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-4752">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-4752">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4754">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4754">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-4755">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4755">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-4756">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4756">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-4757">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4757">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4759">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-4759">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unormsupfccsup-71"></a><span data-ttu-id="5baf9-4760">DXGI_FORMAT_BC1 \_ UNORM<sup>FCC</sup> (71)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4760">DXGI_FORMAT_BC1\_UNORM<sup>FCC</sup> (71)</span></span>
| <span data-ttu-id="5baf9-4761">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-4761">Target</span></span> | <span data-ttu-id="5baf9-4762">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-4762">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-4763">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4763">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-4764">4</span><span class="sxs-lookup"><span data-stu-id="5baf9-4764">4</span></span> |
| <span data-ttu-id="5baf9-4765">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-4765">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4767">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-4767">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4768">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-4768">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4769">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-4769">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4770">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4770">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4771">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4771">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-4772">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4772">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4774">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4774">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4776">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-4776">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4778">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-4778">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4780">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4780">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4782">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4782">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4783">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4783">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4784">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-4784">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-4785">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-4785">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-4786">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4786">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4788">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4788">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-4789">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4789">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4790">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-4790">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4791">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-4791">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-4792">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-4792">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-4793">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-4793">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4794">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4794">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4795">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4795">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-4796">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4796">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-4797">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4797">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-4798">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4798">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-4799">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-4799">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-4800">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-4800">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-4801">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4801">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-4802">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-4802">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4803">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4803">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4804">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-4804">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4806">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4806">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4807">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-4807">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4808">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-4808">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-4809">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-4809">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-4810">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-4810">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-4811">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-4811">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-4812">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-4812">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4814">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4814">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-4815">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4815">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-4816">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4816">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-4817">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4817">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4819">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-4819">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfccsup-72"></a><span data-ttu-id="5baf9-4820">DXGI_FORMAT_BC1 \_ UNORM \_ sRGB<sup>FCC</sup> (72)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4820">DXGI_FORMAT_BC1\_UNORM\_SRGB<sup>FCC</sup> (72)</span></span>
| <span data-ttu-id="5baf9-4821">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-4821">Target</span></span> | <span data-ttu-id="5baf9-4822">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-4822">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-4823">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4823">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-4824">4</span><span class="sxs-lookup"><span data-stu-id="5baf9-4824">4</span></span> |
| <span data-ttu-id="5baf9-4825">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-4825">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4827">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-4827">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4828">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-4828">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4829">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-4829">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4830">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4830">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4831">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4831">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-4832">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4832">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4834">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4834">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4836">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-4836">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4838">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-4838">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4840">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4840">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4842">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4842">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4843">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4843">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4844">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-4844">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-4845">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-4845">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-4846">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4846">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4848">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4848">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-4849">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4849">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4850">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-4850">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4851">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-4851">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-4852">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-4852">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-4853">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-4853">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4854">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4854">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4855">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4855">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-4856">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4856">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-4857">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4857">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-4858">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4858">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-4859">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-4859">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-4860">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-4860">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-4861">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4861">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-4862">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-4862">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4863">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4863">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4864">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-4864">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4866">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4866">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4867">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-4867">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4868">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-4868">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-4869">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-4869">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-4870">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-4870">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-4871">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-4871">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-4872">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-4872">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4874">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4874">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-4875">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4875">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-4876">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4876">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-4877">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4877">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4879">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-4879">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="5baf9-4880">DXGI_FORMAT_BC2 \_ <sup>PCC</sup> de tipo (73)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4880">DXGI_FORMAT_BC2\_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="5baf9-4881">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-4881">Target</span></span> | <span data-ttu-id="5baf9-4882">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-4882">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-4883">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4883">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-4884">8</span><span class="sxs-lookup"><span data-stu-id="5baf9-4884">8</span></span> |
| <span data-ttu-id="5baf9-4885">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-4885">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4887">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-4887">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4888">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-4888">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4889">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-4889">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4890">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4890">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4891">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4891">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-4892">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4892">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4894">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4894">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4896">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-4896">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4898">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-4898">Shader ld</span></span> | \- |
| <span data-ttu-id="5baf9-4899">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4899">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4900">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4900">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4901">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4901">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4902">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-4902">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-4903">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-4903">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-4904">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4904">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4906">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4906">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-4907">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4907">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4908">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-4908">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4909">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-4909">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-4910">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-4910">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-4911">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-4911">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4912">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4912">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4913">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4913">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-4914">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4914">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-4915">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4915">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-4916">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4916">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-4917">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-4917">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-4918">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-4918">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-4919">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4919">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-4920">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-4920">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4921">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4921">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4922">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-4922">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4924">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4924">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4925">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-4925">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4926">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-4926">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-4927">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-4927">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-4928">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-4928">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-4929">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-4929">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-4930">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-4930">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4932">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4932">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-4933">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4933">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-4934">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4934">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-4935">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4935">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4937">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-4937">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unormsupfccsup-74"></a><span data-ttu-id="5baf9-4938">DXGI_FORMAT_BC2 \_ UNORM<sup>FCC</sup> (74)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4938">DXGI_FORMAT_BC2\_UNORM<sup>FCC</sup> (74)</span></span>
| <span data-ttu-id="5baf9-4939">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-4939">Target</span></span> | <span data-ttu-id="5baf9-4940">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-4940">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-4941">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4941">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-4942">8</span><span class="sxs-lookup"><span data-stu-id="5baf9-4942">8</span></span> |
| <span data-ttu-id="5baf9-4943">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-4943">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4945">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-4945">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4946">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-4946">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4947">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-4947">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4948">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4948">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-4949">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4949">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-4950">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4950">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4952">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-4952">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4954">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-4954">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4956">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-4956">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4958">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4958">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4960">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4960">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4961">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4961">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-4962">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-4962">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-4963">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-4963">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-4964">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4964">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4966">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-4966">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-4967">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4967">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4968">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-4968">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4969">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-4969">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-4970">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-4970">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-4971">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-4971">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4972">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4972">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-4973">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4973">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-4974">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4974">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-4975">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4975">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-4976">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4976">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-4977">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-4977">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-4978">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-4978">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-4979">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-4979">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-4980">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-4980">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4981">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4981">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-4982">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-4982">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4984">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-4984">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4985">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-4985">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-4986">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-4986">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-4987">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-4987">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-4988">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-4988">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-4989">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-4989">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-4990">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-4990">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4992">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4992">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-4993">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4993">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-4994">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-4994">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-4995">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-4995">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-4997">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-4997">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfccsup-75"></a><span data-ttu-id="5baf9-4998">DXGI_FORMAT_BC2 \_ UNORM \_ sRGB<sup>FCC</sup> (75)</span><span class="sxs-lookup"><span data-stu-id="5baf9-4998">DXGI_FORMAT_BC2\_UNORM\_SRGB<sup>FCC</sup> (75)</span></span>
| <span data-ttu-id="5baf9-4999">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-4999">Target</span></span> | <span data-ttu-id="5baf9-5000">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-5000">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-5001">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5001">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-5002">8</span><span class="sxs-lookup"><span data-stu-id="5baf9-5002">8</span></span> |
| <span data-ttu-id="5baf9-5003">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-5003">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5005">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-5005">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5006">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5006">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5007">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5007">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5008">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5008">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5009">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5009">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-5010">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5010">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5012">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5012">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5014">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-5014">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5016">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-5016">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5018">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5018">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5020">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5020">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5021">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5021">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5022">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-5022">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-5023">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-5023">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-5024">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5024">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5026">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5026">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-5027">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5027">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5028">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-5028">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5029">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-5029">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-5030">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-5030">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-5031">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-5031">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5032">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5032">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5033">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5033">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-5034">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5034">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-5035">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5035">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-5036">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5036">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-5037">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-5037">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-5038">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-5038">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-5039">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5039">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-5040">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-5040">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5041">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5041">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5042">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-5042">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5044">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5044">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5045">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-5045">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5046">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-5046">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-5047">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-5047">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-5048">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-5048">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-5049">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-5049">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-5050">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-5050">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5052">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5052">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-5053">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5053">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-5054">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5054">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-5055">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5055">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5057">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-5057">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="5baf9-5058">DXGI_FORMAT_BC3 \_ <sup>PCC</sup> de tipo (76)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5058">DXGI_FORMAT_BC3\_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="5baf9-5059">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-5059">Target</span></span> | <span data-ttu-id="5baf9-5060">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-5060">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-5061">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5061">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-5062">8</span><span class="sxs-lookup"><span data-stu-id="5baf9-5062">8</span></span> |
| <span data-ttu-id="5baf9-5063">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-5063">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5065">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-5065">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5066">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5066">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5067">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5067">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5068">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5068">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5069">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5069">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-5070">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5070">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5072">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5072">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5074">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-5074">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5076">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-5076">Shader ld</span></span> | \- |
| <span data-ttu-id="5baf9-5077">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5077">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5078">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5078">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5079">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5079">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5080">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-5080">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-5081">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-5081">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-5082">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5082">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5084">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5084">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-5085">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5085">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5086">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-5086">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5087">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-5087">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-5088">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-5088">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-5089">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-5089">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5090">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5090">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5091">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5091">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-5092">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5092">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-5093">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5093">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-5094">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5094">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-5095">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-5095">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-5096">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-5096">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-5097">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5097">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-5098">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-5098">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5099">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5099">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5100">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-5100">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5102">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5102">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5103">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-5103">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5104">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-5104">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-5105">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-5105">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-5106">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-5106">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-5107">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-5107">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-5108">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-5108">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5110">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5110">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-5111">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5111">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-5112">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5112">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-5113">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5113">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5115">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-5115">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unormsupfccsup-77"></a><span data-ttu-id="5baf9-5116">DXGI_FORMAT_BC3 \_ UNORM<sup>FCC</sup> (77)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5116">DXGI_FORMAT_BC3\_UNORM<sup>FCC</sup> (77)</span></span>
| <span data-ttu-id="5baf9-5117">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-5117">Target</span></span> | <span data-ttu-id="5baf9-5118">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-5118">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-5119">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5119">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-5120">8</span><span class="sxs-lookup"><span data-stu-id="5baf9-5120">8</span></span> |
| <span data-ttu-id="5baf9-5121">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-5121">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5123">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-5123">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5124">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5124">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5125">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5125">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5126">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5126">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5127">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5127">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-5128">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5128">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5130">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5130">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5132">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-5132">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5134">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-5134">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5136">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5136">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5138">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5138">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5139">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5139">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5140">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-5140">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-5141">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-5141">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-5142">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5142">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5144">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5144">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-5145">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5145">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5146">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-5146">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5147">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-5147">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-5148">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-5148">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-5149">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-5149">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5150">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5150">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5151">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5151">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-5152">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5152">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-5153">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5153">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-5154">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5154">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-5155">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-5155">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-5156">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-5156">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-5157">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5157">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-5158">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-5158">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5159">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5159">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5160">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-5160">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5162">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5162">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5163">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-5163">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5164">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-5164">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-5165">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-5165">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-5166">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-5166">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-5167">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-5167">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-5168">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-5168">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5170">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5170">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-5171">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5171">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-5172">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5172">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-5173">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5173">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5175">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-5175">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfccsup-78"></a><span data-ttu-id="5baf9-5176">DXGI_FORMAT_BC3 \_ UNORM \_ sRGB<sup>FCC</sup> (78)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5176">DXGI_FORMAT_BC3\_UNORM\_SRGB<sup>FCC</sup> (78)</span></span>
| <span data-ttu-id="5baf9-5177">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-5177">Target</span></span> | <span data-ttu-id="5baf9-5178">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-5178">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-5179">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5179">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-5180">8</span><span class="sxs-lookup"><span data-stu-id="5baf9-5180">8</span></span> |
| <span data-ttu-id="5baf9-5181">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-5181">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5183">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-5183">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5184">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5184">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5185">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5185">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5186">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5186">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5187">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5187">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-5188">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5188">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5190">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5190">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5192">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-5192">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5194">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-5194">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5196">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5196">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5198">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5198">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5199">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5199">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5200">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-5200">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-5201">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-5201">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-5202">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5202">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5204">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5204">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-5205">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5205">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5206">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-5206">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5207">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-5207">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-5208">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-5208">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-5209">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-5209">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5210">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5210">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5211">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5211">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-5212">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5212">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-5213">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5213">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-5214">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5214">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-5215">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-5215">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-5216">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-5216">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-5217">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5217">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-5218">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-5218">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5219">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5219">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5220">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-5220">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5222">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5222">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5223">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-5223">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5224">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-5224">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-5225">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-5225">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-5226">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-5226">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-5227">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-5227">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-5228">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-5228">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5230">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5230">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-5231">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5231">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-5232">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5232">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-5233">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5233">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5235">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-5235">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="5baf9-5236">DXGI_FORMAT_BC4 \_ <sup>PCC</sup> de tipo (79)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5236">DXGI_FORMAT_BC4\_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="5baf9-5237">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-5237">Target</span></span> | <span data-ttu-id="5baf9-5238">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-5238">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-5239">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5239">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-5240">4</span><span class="sxs-lookup"><span data-stu-id="5baf9-5240">4</span></span> |
| <span data-ttu-id="5baf9-5241">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-5241">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5243">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-5243">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5244">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5244">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5245">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5245">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5246">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5246">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5247">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5247">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-5248">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5248">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5250">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5250">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5252">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-5252">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5254">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-5254">Shader ld</span></span> | \- |
| <span data-ttu-id="5baf9-5255">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5255">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5256">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5256">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5257">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5257">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5258">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-5258">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-5259">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-5259">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-5260">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5260">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5262">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5262">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-5263">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5263">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5264">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-5264">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5265">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-5265">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-5266">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-5266">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-5267">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-5267">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5268">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5268">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5269">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5269">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-5270">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5270">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-5271">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5271">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-5272">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5272">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-5273">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-5273">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-5274">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-5274">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-5275">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5275">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-5276">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-5276">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5277">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5277">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5278">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-5278">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5280">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5280">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5281">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-5281">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5282">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-5282">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-5283">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-5283">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-5284">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-5284">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-5285">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-5285">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-5286">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-5286">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5288">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5288">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-5289">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5289">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-5290">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5290">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-5291">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5291">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-5292">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-5292">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_unormsupfccsup-80"></a><span data-ttu-id="5baf9-5293">DXGI_FORMAT_BC4 \_ UNORM<sup>FCC</sup> (80)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5293">DXGI_FORMAT_BC4\_UNORM<sup>FCC</sup> (80)</span></span>
| <span data-ttu-id="5baf9-5294">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-5294">Target</span></span> | <span data-ttu-id="5baf9-5295">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-5295">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-5296">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5296">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-5297">4</span><span class="sxs-lookup"><span data-stu-id="5baf9-5297">4</span></span> |
| <span data-ttu-id="5baf9-5298">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-5298">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5300">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-5300">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5301">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5301">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5302">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5302">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5303">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5303">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5304">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5304">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-5305">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5305">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5307">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5307">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5309">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-5309">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5311">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-5311">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5313">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5313">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5315">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5315">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5316">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5316">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5317">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-5317">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-5318">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-5318">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-5319">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5319">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5321">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5321">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-5322">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5322">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5323">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-5323">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5324">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-5324">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-5325">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-5325">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-5326">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-5326">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5327">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5327">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5328">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5328">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-5329">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5329">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-5330">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5330">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-5331">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5331">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-5332">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-5332">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-5333">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-5333">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-5334">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5334">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-5335">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-5335">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5336">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5336">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5337">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-5337">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5339">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5339">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5340">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-5340">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5341">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-5341">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-5342">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-5342">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-5343">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-5343">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-5344">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-5344">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-5345">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-5345">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5347">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5347">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-5348">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5348">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-5349">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5349">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-5350">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5350">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-5351">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-5351">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_snormsupfccsup-81"></a><span data-ttu-id="5baf9-5352">DXGI_FORMAT_BC4 \_ SNORM<sup>FCC</sup> (81)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5352">DXGI_FORMAT_BC4\_SNORM<sup>FCC</sup> (81)</span></span>
| <span data-ttu-id="5baf9-5353">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-5353">Target</span></span> | <span data-ttu-id="5baf9-5354">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-5354">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-5355">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5355">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-5356">4</span><span class="sxs-lookup"><span data-stu-id="5baf9-5356">4</span></span> |
| <span data-ttu-id="5baf9-5357">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-5357">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5359">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-5359">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5360">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5360">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5361">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5361">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5362">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5362">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5363">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5363">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-5364">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5364">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5366">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5366">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5368">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-5368">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5370">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-5370">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5372">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5372">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5374">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5374">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5375">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5375">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5376">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-5376">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-5377">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-5377">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-5378">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5378">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5380">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5380">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-5381">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5381">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5382">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-5382">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5383">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-5383">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-5384">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-5384">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-5385">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-5385">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5386">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5386">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5387">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5387">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-5388">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5388">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-5389">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5389">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-5390">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5390">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-5391">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-5391">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-5392">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-5392">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-5393">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5393">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-5394">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-5394">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5395">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5395">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5396">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-5396">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5398">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5398">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5399">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-5399">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5400">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-5400">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-5401">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-5401">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-5402">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-5402">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-5403">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-5403">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-5404">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-5404">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5406">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5406">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-5407">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5407">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-5408">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5408">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-5409">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5409">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-5410">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-5410">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="5baf9-5411">DXGI_FORMAT_BC5 \_ <sup>PCC</sup> de tipo (82)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5411">DXGI_FORMAT_BC5\_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="5baf9-5412">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-5412">Target</span></span> | <span data-ttu-id="5baf9-5413">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-5413">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-5414">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5414">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-5415">8</span><span class="sxs-lookup"><span data-stu-id="5baf9-5415">8</span></span> |
| <span data-ttu-id="5baf9-5416">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-5416">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5418">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-5418">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5419">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5419">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5420">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5420">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5421">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5421">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5422">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5422">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-5423">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5423">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5425">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5425">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5427">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-5427">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5429">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-5429">Shader ld</span></span> | \- |
| <span data-ttu-id="5baf9-5430">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5430">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5431">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5431">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5432">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5432">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5433">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-5433">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-5434">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-5434">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-5435">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5435">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5437">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5437">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-5438">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5438">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5439">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-5439">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5440">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-5440">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-5441">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-5441">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-5442">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-5442">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5443">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5443">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5444">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5444">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-5445">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5445">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-5446">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5446">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-5447">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5447">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-5448">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-5448">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-5449">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-5449">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-5450">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5450">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-5451">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-5451">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5452">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5452">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5453">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-5453">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5455">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5455">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5456">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-5456">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5457">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-5457">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-5458">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-5458">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-5459">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-5459">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-5460">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-5460">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-5461">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-5461">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5463">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5463">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-5464">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5464">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-5465">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5465">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-5466">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5466">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-5467">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-5467">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_unormsupfccsup-83"></a><span data-ttu-id="5baf9-5468">DXGI_FORMAT_BC5 \_ UNORM<sup>FCC</sup> (83)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5468">DXGI_FORMAT_BC5\_UNORM<sup>FCC</sup> (83)</span></span>
| <span data-ttu-id="5baf9-5469">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-5469">Target</span></span> | <span data-ttu-id="5baf9-5470">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-5470">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-5471">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5471">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-5472">8</span><span class="sxs-lookup"><span data-stu-id="5baf9-5472">8</span></span> |
| <span data-ttu-id="5baf9-5473">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-5473">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5475">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-5475">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5476">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5476">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5477">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5477">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5478">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5478">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5479">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5479">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-5480">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5480">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5482">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5482">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5484">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-5484">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5486">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-5486">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5488">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5488">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5490">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5490">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5491">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5491">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5492">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-5492">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-5493">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-5493">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-5494">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5494">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5496">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5496">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-5497">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5497">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5498">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-5498">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5499">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-5499">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-5500">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-5500">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-5501">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-5501">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5502">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5502">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5503">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5503">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-5504">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5504">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-5505">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5505">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-5506">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5506">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-5507">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-5507">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-5508">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-5508">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-5509">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5509">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-5510">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-5510">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5511">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5511">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5512">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-5512">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5514">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5514">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5515">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-5515">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5516">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-5516">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-5517">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-5517">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-5518">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-5518">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-5519">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-5519">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-5520">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-5520">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5522">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5522">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-5523">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5523">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-5524">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5524">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-5525">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5525">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-5526">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-5526">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_snormsupfccsup-84"></a><span data-ttu-id="5baf9-5527">DXGI_FORMAT_BC5 \_ SNORM<sup>FCC</sup> (84)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5527">DXGI_FORMAT_BC5\_SNORM<sup>FCC</sup> (84)</span></span>
| <span data-ttu-id="5baf9-5528">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-5528">Target</span></span> | <span data-ttu-id="5baf9-5529">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-5529">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-5530">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5530">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-5531">8</span><span class="sxs-lookup"><span data-stu-id="5baf9-5531">8</span></span> |
| <span data-ttu-id="5baf9-5532">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-5532">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5534">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-5534">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5535">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5535">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5536">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5536">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5537">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5537">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5538">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5538">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-5539">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5539">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5541">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5541">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5543">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-5543">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5545">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-5545">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5547">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5547">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5549">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5549">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5550">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5550">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5551">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-5551">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-5552">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-5552">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-5553">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5553">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5555">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5555">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-5556">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5556">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5557">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-5557">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5558">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-5558">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-5559">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-5559">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-5560">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-5560">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5561">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5561">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5562">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5562">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-5563">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5563">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-5564">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5564">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-5565">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5565">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-5566">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-5566">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-5567">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-5567">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-5568">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5568">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-5569">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-5569">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5570">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5570">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5571">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-5571">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5573">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5573">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5574">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-5574">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5575">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-5575">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-5576">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-5576">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-5577">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-5577">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-5578">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-5578">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-5579">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-5579">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5581">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5581">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-5582">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5582">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-5583">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5583">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-5584">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5584">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-5585">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-5585">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="5baf9-5586">DXGI_FORMAT_B5G6R5 \_ UNORM<sup>FNS</sup> (85)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5586">DXGI_FORMAT_B5G6R5\_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="5baf9-5587">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-5587">Target</span></span> | <span data-ttu-id="5baf9-5588">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-5588">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-5589">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5589">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-5590">16</span><span class="sxs-lookup"><span data-stu-id="5baf9-5590">16</span></span> |
| <span data-ttu-id="5baf9-5591">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-5591">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5593">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-5593">Buffer</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-5595">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5595">Input Assembler Vertex Buffer</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-5597">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5597">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5598">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5598">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5599">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5599">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5601">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5601">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5603">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5603">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-5605">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5607">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-5607">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5609">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5609">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5611">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5611">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5612">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5612">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5613">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-5613">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-5614">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-5614">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-5615">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5615">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5617">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5617">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5619">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5619">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5621">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-5621">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5623">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-5623">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-5624">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-5624">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-5625">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-5625">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5626">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5626">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5627">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5627">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-5628">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5628">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-5629">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5629">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-5630">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5630">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-5631">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-5631">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-5632">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-5632">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-5633">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5633">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-5634">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-5634">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5635">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5635">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5636">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-5636">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5638">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5638">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-5640">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-5640">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-5642">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-5642">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-5644">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-5644">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5646">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-5646">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-5648">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-5648">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-5649">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-5649">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="5baf9-5650">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5650">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-5651">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5651">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-5652">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5652">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-5653">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5653">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-5654">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-5654">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="5baf9-5655">DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>FNS</sup> (86)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5655">DXGI_FORMAT_B5G5R5A1\_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="5baf9-5656">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-5656">Target</span></span> | <span data-ttu-id="5baf9-5657">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-5657">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-5658">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5658">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-5659">16</span><span class="sxs-lookup"><span data-stu-id="5baf9-5659">16</span></span> |
| <span data-ttu-id="5baf9-5660">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-5660">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5662">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-5662">Buffer</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-5664">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5664">Input Assembler Vertex Buffer</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-5666">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5666">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5667">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5667">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5668">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5668">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5670">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5670">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5672">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5672">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5674">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-5674">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5676">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-5676">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5678">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5678">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5680">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5680">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5681">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5681">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5682">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-5682">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-5683">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-5683">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-5684">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5684">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5686">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5686">Mipmap Auto-Generation</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-5688">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5688">RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-5690">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-5690">Blendable RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-5692">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-5692">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-5693">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-5693">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-5694">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-5694">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5695">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5695">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5696">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5696">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-5697">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5697">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-5698">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5698">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-5699">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5699">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-5700">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-5700">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-5701">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-5701">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-5702">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5702">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-5703">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-5703">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5704">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5704">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5705">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-5705">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5707">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5707">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-5709">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-5709">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-5711">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-5711">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-5713">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-5713">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5715">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-5715">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-5717">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-5717">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-5718">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-5718">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="5baf9-5719">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5719">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-5720">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5720">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-5721">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5721">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-5722">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5722">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-5723">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-5723">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="5baf9-5724">DXGI_FORMAT_B8G8R8A8 \_ <sup>PCs</sup> não tipados (90)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5724">DXGI_FORMAT_B8G8R8A8\_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="5baf9-5725">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-5725">Target</span></span> | <span data-ttu-id="5baf9-5726">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-5726">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-5727">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5727">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-5728">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-5728">32</span></span> |
| <span data-ttu-id="5baf9-5729">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-5729">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5731">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-5731">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5732">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5732">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5733">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5733">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5734">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5734">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5735">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5735">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5737">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5737">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5739">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5739">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5741">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-5741">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5743">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-5743">Shader ld</span></span> | \- |
| <span data-ttu-id="5baf9-5744">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5744">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5745">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5745">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5746">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5746">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5747">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-5747">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-5748">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-5748">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-5749">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5749">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5751">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5751">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-5752">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5752">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5753">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-5753">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5754">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-5754">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-5755">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-5755">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-5756">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-5756">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5757">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5757">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5758">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5758">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-5759">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5759">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-5760">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5760">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-5761">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5761">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-5762">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-5762">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-5763">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-5763">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-5764">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5764">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-5765">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-5765">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5766">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5766">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5767">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-5767">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5769">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5769">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5770">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-5770">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5771">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-5771">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-5772">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-5772">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-5773">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-5773">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-5774">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-5774">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-5775">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-5775">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5777">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5777">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-5778">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5778">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-5779">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5779">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-5780">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5780">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5782">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-5782">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfcssup-87"></a><span data-ttu-id="5baf9-5783">\_UNORM<sup>FCS</sup> de DXGI_FORMAT_B8G8R8A8 (87)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5783">DXGI_FORMAT_B8G8R8A8\_UNORM<sup>FCS</sup> (87)</span></span>
| <span data-ttu-id="5baf9-5784">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-5784">Target</span></span> | <span data-ttu-id="5baf9-5785">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-5785">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-5786">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5786">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-5787">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-5787">32</span></span> |
| <span data-ttu-id="5baf9-5788">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-5788">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5790">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-5790">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5792">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5792">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5794">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5794">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5795">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5795">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5796">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5796">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5798">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5798">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5800">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5800">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5802">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-5802">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5804">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-5804">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5806">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5806">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5808">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5808">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5809">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5809">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5810">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-5810">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-5811">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-5811">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-5812">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5812">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5814">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5814">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5816">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5816">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5818">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-5818">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5820">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-5820">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-5821">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-5821">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-5822">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-5822">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5823">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5823">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5824">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5824">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-5825">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5825">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-5826">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5826">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-5827">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5827">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-5828">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-5828">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-5829">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-5829">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-5830">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5830">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-5831">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-5831">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5832">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5832">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5833">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-5833">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5835">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5835">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-5837">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-5837">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-5839">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-5839">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-5841">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-5841">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5843">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-5843">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-5845">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-5845">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5847">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-5847">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5849">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5849">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-5850">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5850">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-5852">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5852">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-5854">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5854">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5856">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-5856">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfcssup-91"></a><span data-ttu-id="5baf9-5857">\_FCS DXGI_FORMAT_B8G8R8A8 \_ UNORM<sup></sup> sRGB (91)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5857">DXGI_FORMAT_B8G8R8A8\_UNORM\_SRGB<sup>FCS</sup> (91)</span></span>
| <span data-ttu-id="5baf9-5858">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-5858">Target</span></span> | <span data-ttu-id="5baf9-5859">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-5859">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-5860">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5860">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-5861">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-5861">32</span></span> |
| <span data-ttu-id="5baf9-5862">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-5862">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5864">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-5864">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5865">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5865">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5866">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5866">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5867">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5867">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5868">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5868">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5870">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5870">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5872">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5872">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5874">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-5874">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5876">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-5876">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5878">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5878">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5880">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5880">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5881">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5881">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5882">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-5882">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-5883">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-5883">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-5884">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5884">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5886">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5886">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5888">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5888">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5890">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-5890">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5892">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-5892">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-5893">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-5893">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-5894">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-5894">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5895">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5895">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5896">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5896">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-5897">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5897">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-5898">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5898">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-5899">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5899">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-5900">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-5900">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-5901">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-5901">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-5902">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5902">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-5903">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-5903">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5904">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5904">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5905">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-5905">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5907">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5907">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-5909">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-5909">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-5911">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-5911">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-5913">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-5913">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5915">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-5915">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5917">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-5917">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5919">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-5919">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5921">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5921">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-5922">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5922">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-5924">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5924">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-5926">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5926">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5928">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-5928">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="5baf9-5929">DXGI_FORMAT_B8G8R8X8 \_ <sup>PCs</sup> não tipados (92)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5929">DXGI_FORMAT_B8G8R8X8\_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="5baf9-5930">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-5930">Target</span></span> | <span data-ttu-id="5baf9-5931">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-5931">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-5932">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5932">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-5933">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-5933">32</span></span> |
| <span data-ttu-id="5baf9-5934">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-5934">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5936">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-5936">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5937">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5937">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5938">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5938">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5939">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5939">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-5940">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5940">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5942">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5942">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5944">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-5944">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5946">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-5946">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5948">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-5948">Shader ld</span></span> | \- |
| <span data-ttu-id="5baf9-5949">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5949">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5950">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5950">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5951">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5951">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-5952">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-5952">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-5953">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-5953">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-5954">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5954">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5956">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-5956">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-5957">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5957">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5958">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-5958">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5959">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-5959">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-5960">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-5960">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-5961">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-5961">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5962">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5962">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-5963">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5963">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-5964">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5964">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-5965">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5965">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-5966">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5966">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-5967">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-5967">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-5968">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-5968">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-5969">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-5969">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-5970">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-5970">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5971">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5971">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-5972">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-5972">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5974">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-5974">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5975">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-5975">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-5976">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-5976">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-5977">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-5977">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-5978">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-5978">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-5979">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-5979">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-5980">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-5980">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5982">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5982">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-5983">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5983">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-5984">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-5984">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-5985">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-5985">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5987">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-5987">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfcssup-88"></a><span data-ttu-id="5baf9-5988">\_UNORM<sup>FCS</sup> de DXGI_FORMAT_B8G8R8X8 (88)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5988">DXGI_FORMAT_B8G8R8X8\_UNORM<sup>FCS</sup> (88)</span></span>
| <span data-ttu-id="5baf9-5989">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-5989">Target</span></span> | <span data-ttu-id="5baf9-5990">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-5990">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-5991">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-5991">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-5992">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-5992">32</span></span> |
| <span data-ttu-id="5baf9-5993">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-5993">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5995">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-5995">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5997">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5997">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-5999">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-5999">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6000">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6000">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6001">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6001">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6003">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6003">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6005">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6005">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6007">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-6007">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6009">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-6009">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6011">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6011">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6013">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6013">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6014">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6014">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6015">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-6015">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-6016">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-6016">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-6017">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6017">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6019">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6019">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6021">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6021">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6023">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-6023">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6025">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-6025">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-6026">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-6026">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-6027">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-6027">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6028">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6028">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6029">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6029">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-6030">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6030">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-6031">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6031">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-6032">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6032">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-6033">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-6033">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-6034">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-6034">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-6035">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6035">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-6036">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-6036">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6037">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6037">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6038">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-6038">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6040">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6040">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6042">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-6042">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6044">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-6044">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6046">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-6046">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6048">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-6048">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6050">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-6050">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-6051">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-6051">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6053">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6053">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-6054">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6054">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6056">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6056">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6058">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6058">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6060">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-6060">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfcssup-93"></a><span data-ttu-id="5baf9-6061">\_FCS DXGI_FORMAT_B8G8R8X8 \_ UNORM<sup></sup> sRGB (93)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6061">DXGI_FORMAT_B8G8R8X8\_UNORM\_SRGB<sup>FCS</sup> (93)</span></span>
| <span data-ttu-id="5baf9-6062">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-6062">Target</span></span> | <span data-ttu-id="5baf9-6063">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-6063">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-6064">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6064">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-6065">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-6065">32</span></span> |
| <span data-ttu-id="5baf9-6066">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-6066">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6068">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-6068">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6069">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6069">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6070">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6070">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6071">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6071">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6072">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6072">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6074">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6074">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6076">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6076">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6078">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-6078">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6080">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-6080">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6082">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6082">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6084">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6084">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6085">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6085">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6086">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-6086">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-6087">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-6087">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-6088">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6088">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6090">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6090">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6092">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6092">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6094">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-6094">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6096">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-6096">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-6097">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-6097">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-6098">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-6098">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6099">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6099">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6100">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6100">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-6101">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6101">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-6102">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6102">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-6103">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6103">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-6104">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-6104">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-6105">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-6105">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-6106">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6106">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-6107">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-6107">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6108">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6108">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6109">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-6109">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6111">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6111">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6113">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-6113">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6115">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-6115">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6117">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-6117">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6119">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-6119">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6121">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-6121">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-6122">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-6122">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6124">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6124">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-6125">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6125">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-6126">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6126">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-6127">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6127">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6129">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-6129">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="5baf9-6130">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6130">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="5baf9-6131">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-6131">Target</span></span> | <span data-ttu-id="5baf9-6132">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-6132">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-6133">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6133">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-6134">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-6134">32</span></span> |
| <span data-ttu-id="5baf9-6135">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-6135">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6137">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-6137">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6138">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6138">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6139">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6139">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6140">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6140">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6141">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6141">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-6142">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6142">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6144">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6144">Texture3D</span></span> | \- |
| <span data-ttu-id="5baf9-6145">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-6145">TextureCube</span></span> | \- |
| <span data-ttu-id="5baf9-6146">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-6146">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6148">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6148">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6150">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6150">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6151">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6151">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6152">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-6152">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-6153">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-6153">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-6154">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6154">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6156">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6156">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6158">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6158">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6160">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-6160">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6162">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-6162">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-6163">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-6163">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-6164">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-6164">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6165">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6165">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6166">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6166">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-6167">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6167">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-6168">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6168">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-6169">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6169">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-6170">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-6170">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-6171">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-6171">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-6172">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6172">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-6173">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-6173">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6174">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6174">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6175">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-6175">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6177">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6177">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6178">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-6178">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6179">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-6179">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-6180">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-6180">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-6181">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-6181">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-6182">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-6182">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-6183">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-6183">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="5baf9-6184">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6184">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6186">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6186">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6188">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6188">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6190">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6190">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6192">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-6192">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="5baf9-6193">DXGI_FORMAT_Y410<sup>V</sup> (101)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6193">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="5baf9-6194">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-6194">Target</span></span> | <span data-ttu-id="5baf9-6195">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-6195">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-6196">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6196">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-6197">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-6197">32</span></span> |
| <span data-ttu-id="5baf9-6198">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-6198">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6200">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-6200">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6201">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6201">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6202">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6202">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6203">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6203">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6204">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6204">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-6205">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6205">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6207">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6207">Texture3D</span></span> | \- |
| <span data-ttu-id="5baf9-6208">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-6208">TextureCube</span></span> | \- |
| <span data-ttu-id="5baf9-6209">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-6209">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6211">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6211">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6213">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6213">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6214">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6214">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6215">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-6215">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-6216">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-6216">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-6217">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6217">Mipmap</span></span> | \- |
| <span data-ttu-id="5baf9-6218">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6218">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-6219">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6219">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6220">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-6220">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6221">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-6221">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-6222">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-6222">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-6223">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-6223">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6224">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6224">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6225">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6225">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-6226">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6226">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-6227">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6227">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-6228">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6228">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-6229">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-6229">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-6230">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-6230">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-6231">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6231">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-6232">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-6232">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6233">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6233">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6234">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-6234">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6236">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6236">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6237">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-6237">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6238">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-6238">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-6239">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-6239">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-6240">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-6240">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-6241">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-6241">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-6242">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-6242">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="5baf9-6243">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6243">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6245">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6245">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6247">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6247">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6249">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6249">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6251">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-6251">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="5baf9-6252">DXGI_FORMAT_Y416<sup>V</sup> (102)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6252">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="5baf9-6253">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-6253">Target</span></span> | <span data-ttu-id="5baf9-6254">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-6254">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-6255">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6255">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-6256">64</span><span class="sxs-lookup"><span data-stu-id="5baf9-6256">64</span></span> |
| <span data-ttu-id="5baf9-6257">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-6257">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6259">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-6259">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6260">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6260">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6261">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6261">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6262">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6262">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6263">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6263">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-6264">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6264">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6266">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6266">Texture3D</span></span> | \- |
| <span data-ttu-id="5baf9-6267">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-6267">TextureCube</span></span> | \- |
| <span data-ttu-id="5baf9-6268">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-6268">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6270">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6270">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6272">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6272">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6273">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6273">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6274">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-6274">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-6275">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-6275">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-6276">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6276">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6278">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6278">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-6279">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6279">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6280">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-6280">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6281">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-6281">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-6282">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-6282">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-6283">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-6283">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6284">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6284">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6285">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6285">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-6286">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6286">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-6287">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6287">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-6288">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6288">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-6289">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-6289">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-6290">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-6290">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-6291">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6291">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-6292">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-6292">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6293">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6293">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6294">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-6294">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6296">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6296">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6297">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-6297">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6298">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-6298">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-6299">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-6299">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-6300">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-6300">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-6301">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-6301">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-6302">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-6302">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="5baf9-6303">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6303">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6305">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6305">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6307">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6307">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6309">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6309">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6311">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-6311">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="5baf9-6312">DXGI_FORMAT_NV12<sup>V</sup> (103)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6312">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="5baf9-6313">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-6313">Target</span></span> | <span data-ttu-id="5baf9-6314">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-6314">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-6315">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6315">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-6316">8</span><span class="sxs-lookup"><span data-stu-id="5baf9-6316">8</span></span> |
| <span data-ttu-id="5baf9-6317">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-6317">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6319">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-6319">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6320">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6320">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6321">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6321">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6322">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6322">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6323">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6323">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-6324">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6324">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6326">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6326">Texture3D</span></span> | \- |
| <span data-ttu-id="5baf9-6327">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-6327">TextureCube</span></span> | \- |
| <span data-ttu-id="5baf9-6328">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-6328">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6330">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6330">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6332">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6332">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6333">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6333">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6334">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-6334">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-6335">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-6335">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-6336">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6336">Mipmap</span></span> | \- |
| <span data-ttu-id="5baf9-6337">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6337">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-6338">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6338">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6340">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-6340">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6342">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-6342">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-6343">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-6343">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-6344">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-6344">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6345">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6345">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6346">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6346">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-6347">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6347">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-6348">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6348">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-6349">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6349">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-6350">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-6350">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-6351">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-6351">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-6352">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6352">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-6353">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-6353">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6354">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6354">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6355">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-6355">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6357">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6357">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6358">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-6358">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6359">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-6359">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-6360">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-6360">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-6361">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-6361">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-6362">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-6362">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-6363">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-6363">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="5baf9-6364">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6364">Video Decoder Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6366">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6366">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6368">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6368">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6370">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6370">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6372">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-6372">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="5baf9-6373">DXGI_FORMAT_P010<sup>V</sup> (104)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6373">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="5baf9-6374">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-6374">Target</span></span> | <span data-ttu-id="5baf9-6375">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-6375">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-6376">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6376">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-6377">16</span><span class="sxs-lookup"><span data-stu-id="5baf9-6377">16</span></span> |
| <span data-ttu-id="5baf9-6378">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-6378">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6380">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-6380">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6381">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6381">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6382">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6382">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6383">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6383">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6384">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6384">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-6385">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6385">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6387">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6387">Texture3D</span></span> | \- |
| <span data-ttu-id="5baf9-6388">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-6388">TextureCube</span></span> | \- |
| <span data-ttu-id="5baf9-6389">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-6389">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6391">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6391">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6393">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6393">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6394">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6394">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6395">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-6395">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-6396">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-6396">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-6397">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6397">Mipmap</span></span> | \- |
| <span data-ttu-id="5baf9-6398">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6398">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-6399">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6399">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6401">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-6401">Blendable RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6403">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-6403">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-6404">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-6404">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-6405">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-6405">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6406">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6406">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6407">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6407">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-6408">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6408">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-6409">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6409">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-6410">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6410">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-6411">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-6411">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-6412">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-6412">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-6413">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6413">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-6414">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-6414">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6415">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6415">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6416">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-6416">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6418">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6418">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6419">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-6419">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6420">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-6420">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-6421">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-6421">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-6422">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-6422">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-6423">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-6423">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-6424">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-6424">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="5baf9-6425">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6425">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6427">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6427">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6429">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6429">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6431">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6431">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6433">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-6433">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="5baf9-6434">DXGI_FORMAT_P016<sup>V</sup> (105)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6434">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="5baf9-6435">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-6435">Target</span></span> | <span data-ttu-id="5baf9-6436">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-6436">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-6437">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6437">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-6438">16</span><span class="sxs-lookup"><span data-stu-id="5baf9-6438">16</span></span> |
| <span data-ttu-id="5baf9-6439">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-6439">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6441">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-6441">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6442">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6442">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6443">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6443">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6444">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6444">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6445">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6445">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-6446">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6446">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6448">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6448">Texture3D</span></span> | \- |
| <span data-ttu-id="5baf9-6449">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-6449">TextureCube</span></span> | \- |
| <span data-ttu-id="5baf9-6450">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-6450">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6452">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6452">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6454">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6454">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6455">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6455">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6456">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-6456">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-6457">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-6457">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-6458">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6458">Mipmap</span></span> | \- |
| <span data-ttu-id="5baf9-6459">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6459">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-6460">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6460">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6462">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-6462">Blendable RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6464">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-6464">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-6465">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-6465">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-6466">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-6466">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6467">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6467">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6468">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6468">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-6469">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6469">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-6470">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6470">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-6471">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6471">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-6472">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-6472">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-6473">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-6473">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-6474">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6474">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-6475">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-6475">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6476">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6476">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6477">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-6477">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6479">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6479">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6480">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-6480">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6481">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-6481">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-6482">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-6482">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-6483">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-6483">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-6484">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-6484">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-6485">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-6485">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="5baf9-6486">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6486">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6488">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6488">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6490">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6490">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6492">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6492">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6494">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-6494">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="5baf9-6495">DXGI_FORMAT_420 \_ opaco<sup>V</sup> (106)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6495">DXGI_FORMAT_420\_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="5baf9-6496">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-6496">Target</span></span> | <span data-ttu-id="5baf9-6497">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-6497">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-6498">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6498">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-6499">8</span><span class="sxs-lookup"><span data-stu-id="5baf9-6499">8</span></span> |
| <span data-ttu-id="5baf9-6500">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-6500">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6502">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-6502">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6503">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6503">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6504">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6504">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6505">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6505">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6506">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6506">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-6507">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6507">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6509">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6509">Texture3D</span></span> | \- |
| <span data-ttu-id="5baf9-6510">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-6510">TextureCube</span></span> | \- |
| <span data-ttu-id="5baf9-6511">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-6511">Shader ld</span></span> | \- |
| <span data-ttu-id="5baf9-6512">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6512">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6513">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6513">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6514">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6514">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6515">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-6515">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-6516">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-6516">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-6517">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6517">Mipmap</span></span> | \- |
| <span data-ttu-id="5baf9-6518">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6518">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-6519">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6519">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6520">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-6520">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6521">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-6521">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-6522">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-6522">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-6523">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-6523">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6524">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6524">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6525">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6525">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-6526">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6526">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-6527">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6527">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-6528">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6528">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-6529">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-6529">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-6530">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-6530">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-6531">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6531">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-6532">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-6532">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6533">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6533">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6534">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-6534">CPU Lockable</span></span> | \- |
| <span data-ttu-id="5baf9-6535">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6535">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6536">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-6536">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6537">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-6537">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-6538">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-6538">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-6539">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-6539">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-6540">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-6540">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-6541">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-6541">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="5baf9-6542">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6542">Video Decoder Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6544">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6544">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6546">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6546">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6548">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6548">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6550">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-6550">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="5baf9-6551">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6551">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="5baf9-6552">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-6552">Target</span></span> | <span data-ttu-id="5baf9-6553">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-6553">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-6554">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6554">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-6555">16</span><span class="sxs-lookup"><span data-stu-id="5baf9-6555">16</span></span> |
| <span data-ttu-id="5baf9-6556">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-6556">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6558">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-6558">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6559">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6559">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6560">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6560">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6561">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6561">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6562">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6562">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-6563">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6563">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6565">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6565">Texture3D</span></span> | \- |
| <span data-ttu-id="5baf9-6566">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-6566">TextureCube</span></span> | \- |
| <span data-ttu-id="5baf9-6567">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-6567">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6569">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6569">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6571">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6571">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6572">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6572">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6573">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-6573">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-6574">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-6574">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-6575">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6575">Mipmap</span></span> | \- |
| <span data-ttu-id="5baf9-6576">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6576">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-6577">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6577">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6578">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-6578">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6579">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-6579">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-6580">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-6580">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-6581">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-6581">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6582">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6582">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6583">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6583">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-6584">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6584">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-6585">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6585">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-6586">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6586">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-6587">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-6587">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-6588">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-6588">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-6589">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6589">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-6590">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-6590">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6591">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6591">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6592">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-6592">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6594">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6594">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6595">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-6595">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6596">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-6596">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-6597">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-6597">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-6598">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-6598">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-6599">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-6599">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-6600">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-6600">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="5baf9-6601">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6601">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6603">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6603">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6605">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6605">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6607">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6607">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6609">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-6609">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="5baf9-6610">DXGI_FORMAT_Y210<sup>V</sup> (108)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6610">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="5baf9-6611">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-6611">Target</span></span> | <span data-ttu-id="5baf9-6612">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-6612">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-6613">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6613">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-6614">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-6614">32</span></span> |
| <span data-ttu-id="5baf9-6615">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-6615">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6617">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-6617">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6618">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6618">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6619">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6619">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6620">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6620">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6621">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6621">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-6622">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6622">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6624">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6624">Texture3D</span></span> | \- |
| <span data-ttu-id="5baf9-6625">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-6625">TextureCube</span></span> | \- |
| <span data-ttu-id="5baf9-6626">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-6626">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6628">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6628">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6630">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6630">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6631">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6631">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6632">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-6632">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-6633">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-6633">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-6634">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6634">Mipmap</span></span> | \- |
| <span data-ttu-id="5baf9-6635">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6635">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-6636">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6636">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6637">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-6637">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6638">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-6638">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-6639">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-6639">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-6640">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-6640">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6641">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6641">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6642">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6642">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-6643">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6643">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-6644">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6644">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-6645">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6645">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-6646">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-6646">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-6647">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-6647">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-6648">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6648">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-6649">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-6649">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6650">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6650">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6651">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-6651">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6653">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6653">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6654">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-6654">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6655">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-6655">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-6656">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-6656">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-6657">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-6657">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-6658">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-6658">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-6659">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-6659">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="5baf9-6660">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6660">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6662">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6662">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6664">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6664">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6666">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6666">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6668">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-6668">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="5baf9-6669">DXGI_FORMAT_Y216<sup>V</sup> (109)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6669">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="5baf9-6670">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-6670">Target</span></span> | <span data-ttu-id="5baf9-6671">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-6671">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-6672">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6672">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-6673">32</span><span class="sxs-lookup"><span data-stu-id="5baf9-6673">32</span></span> |
| <span data-ttu-id="5baf9-6674">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-6674">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6676">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-6676">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6677">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6677">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6678">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6678">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6679">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6679">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6680">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6680">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-6681">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6681">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6683">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6683">Texture3D</span></span> | \- |
| <span data-ttu-id="5baf9-6684">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-6684">TextureCube</span></span> | \- |
| <span data-ttu-id="5baf9-6685">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-6685">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6687">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6687">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6689">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6689">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6690">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6690">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6691">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-6691">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-6692">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-6692">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-6693">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6693">Mipmap</span></span> | \- |
| <span data-ttu-id="5baf9-6694">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6694">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-6695">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6695">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6696">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-6696">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6697">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-6697">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-6698">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-6698">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-6699">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-6699">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6700">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6700">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6701">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6701">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-6702">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6702">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-6703">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6703">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-6704">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6704">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-6705">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-6705">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-6706">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-6706">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-6707">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6707">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-6708">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-6708">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6709">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6709">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6710">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-6710">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6712">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6712">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6713">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-6713">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6714">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-6714">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-6715">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-6715">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-6716">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-6716">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-6717">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-6717">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-6718">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-6718">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="5baf9-6719">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6719">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6721">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6721">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6723">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6723">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6725">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6725">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6727">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-6727">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="5baf9-6728">DXGI_FORMAT_NV11<sup>V</sup> (110)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6728">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="5baf9-6729">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-6729">Target</span></span> | <span data-ttu-id="5baf9-6730">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-6730">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-6731">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6731">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-6732">8</span><span class="sxs-lookup"><span data-stu-id="5baf9-6732">8</span></span> |
| <span data-ttu-id="5baf9-6733">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-6733">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6735">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-6735">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6736">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6736">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6737">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6737">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6738">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6738">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6739">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6739">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-6740">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6740">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6742">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6742">Texture3D</span></span> | \- |
| <span data-ttu-id="5baf9-6743">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-6743">TextureCube</span></span> | \- |
| <span data-ttu-id="5baf9-6744">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-6744">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6746">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6746">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6748">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6748">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6749">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6749">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6750">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-6750">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-6751">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-6751">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-6752">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6752">Mipmap</span></span> | \- |
| <span data-ttu-id="5baf9-6753">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6753">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-6754">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6754">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6756">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-6756">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6758">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-6758">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-6759">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-6759">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-6760">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-6760">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6761">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6761">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6762">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6762">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-6763">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6763">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-6764">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6764">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-6765">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6765">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-6766">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-6766">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-6767">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-6767">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-6768">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6768">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-6769">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-6769">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6770">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6770">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6771">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-6771">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6773">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6773">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6774">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-6774">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6775">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-6775">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-6776">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-6776">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-6777">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-6777">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-6778">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-6778">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-6779">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-6779">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="5baf9-6780">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6780">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6782">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6782">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6784">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6784">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6786">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6786">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6788">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-6788">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="5baf9-6789">DXGI_FORMAT_AI44<sup>V</sup> (111)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6789">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="5baf9-6790">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-6790">Target</span></span> | <span data-ttu-id="5baf9-6791">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-6791">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-6792">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6792">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-6793">8</span><span class="sxs-lookup"><span data-stu-id="5baf9-6793">8</span></span> |
| <span data-ttu-id="5baf9-6794">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-6794">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6796">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-6796">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6797">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6797">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6798">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6798">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6799">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6799">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6800">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6800">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-6801">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6801">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6803">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6803">Texture3D</span></span> | \- |
| <span data-ttu-id="5baf9-6804">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-6804">TextureCube</span></span> | \- |
| <span data-ttu-id="5baf9-6805">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-6805">Shader ld</span></span> | \- |
| <span data-ttu-id="5baf9-6806">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6806">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6807">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6807">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6808">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6808">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6809">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-6809">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-6810">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-6810">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-6811">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6811">Mipmap</span></span> | \- |
| <span data-ttu-id="5baf9-6812">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6812">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-6813">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6813">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6814">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-6814">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6815">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-6815">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-6816">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-6816">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-6817">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-6817">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6818">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6818">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6819">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6819">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-6820">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6820">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-6821">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6821">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-6822">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6822">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-6823">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-6823">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-6824">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-6824">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-6825">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6825">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-6826">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-6826">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6827">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6827">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6828">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-6828">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6830">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6830">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6831">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-6831">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6832">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-6832">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-6833">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-6833">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-6834">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-6834">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-6835">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-6835">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-6836">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-6836">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="5baf9-6837">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6837">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-6838">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6838">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6840">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6840">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-6841">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6841">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-6842">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-6842">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="5baf9-6843">DXGI_FORMAT_IA44<sup>V</sup> (112)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6843">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="5baf9-6844">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-6844">Target</span></span> | <span data-ttu-id="5baf9-6845">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-6845">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-6846">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6846">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-6847">8</span><span class="sxs-lookup"><span data-stu-id="5baf9-6847">8</span></span> |
| <span data-ttu-id="5baf9-6848">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-6848">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6850">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-6850">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6851">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6851">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6852">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6852">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6853">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6853">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6854">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6854">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-6855">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6855">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6857">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6857">Texture3D</span></span> | \- |
| <span data-ttu-id="5baf9-6858">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-6858">TextureCube</span></span> | \- |
| <span data-ttu-id="5baf9-6859">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-6859">Shader ld</span></span> | \- |
| <span data-ttu-id="5baf9-6860">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6860">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6861">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6861">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6862">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6862">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6863">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-6863">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-6864">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-6864">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-6865">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6865">Mipmap</span></span> | \- |
| <span data-ttu-id="5baf9-6866">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6866">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-6867">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6867">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6868">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-6868">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6869">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-6869">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-6870">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-6870">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-6871">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-6871">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6872">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6872">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6873">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6873">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-6874">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6874">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-6875">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6875">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-6876">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6876">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-6877">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-6877">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-6878">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-6878">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-6879">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6879">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-6880">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-6880">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6881">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6881">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6882">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-6882">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6884">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6884">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6885">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-6885">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6886">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-6886">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-6887">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-6887">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-6888">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-6888">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-6889">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-6889">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-6890">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-6890">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="5baf9-6891">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6891">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-6892">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6892">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6894">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6894">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-6895">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6895">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-6896">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-6896">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="5baf9-6897">DXGI_FORMAT_P8<sup>V</sup> (113)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6897">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="5baf9-6898">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-6898">Target</span></span> | <span data-ttu-id="5baf9-6899">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-6899">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-6900">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6900">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-6901">8</span><span class="sxs-lookup"><span data-stu-id="5baf9-6901">8</span></span> |
| <span data-ttu-id="5baf9-6902">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-6902">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6904">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-6904">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6905">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6905">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6906">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6906">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6907">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6907">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6908">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6908">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-6909">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6909">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6911">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6911">Texture3D</span></span> | \- |
| <span data-ttu-id="5baf9-6912">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-6912">TextureCube</span></span> | \- |
| <span data-ttu-id="5baf9-6913">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-6913">Shader ld</span></span> | \- |
| <span data-ttu-id="5baf9-6914">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6914">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6915">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6915">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6916">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6916">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6917">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-6917">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-6918">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-6918">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-6919">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6919">Mipmap</span></span> | \- |
| <span data-ttu-id="5baf9-6920">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6920">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-6921">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6921">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6922">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-6922">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6923">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-6923">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-6924">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-6924">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-6925">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-6925">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6926">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6926">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6927">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6927">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-6928">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6928">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-6929">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6929">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-6930">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6930">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-6931">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-6931">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-6932">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-6932">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-6933">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6933">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-6934">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-6934">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6935">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6935">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6936">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-6936">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6938">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6938">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6939">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-6939">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6940">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-6940">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-6941">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-6941">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-6942">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-6942">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-6943">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-6943">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-6944">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-6944">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="5baf9-6945">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6945">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-6946">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6946">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6948">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6948">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-6949">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6949">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-6950">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-6950">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="5baf9-6951">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6951">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="5baf9-6952">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-6952">Target</span></span> | <span data-ttu-id="5baf9-6953">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-6953">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-6954">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6954">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-6955">16</span><span class="sxs-lookup"><span data-stu-id="5baf9-6955">16</span></span> |
| <span data-ttu-id="5baf9-6956">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-6956">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-6958">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-6958">Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6959">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6959">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6960">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-6960">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6961">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6961">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-6962">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6962">Texture1D</span></span> | \- |
| <span data-ttu-id="5baf9-6963">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6963">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6965">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-6965">Texture3D</span></span> | \- |
| <span data-ttu-id="5baf9-6966">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-6966">TextureCube</span></span> | \- |
| <span data-ttu-id="5baf9-6967">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-6967">Shader ld</span></span> | \- |
| <span data-ttu-id="5baf9-6968">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6968">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6969">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6969">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6970">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-6970">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-6971">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-6971">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-6972">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-6972">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-6973">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6973">Mipmap</span></span> | \- |
| <span data-ttu-id="5baf9-6974">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-6974">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="5baf9-6975">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6975">RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6976">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-6976">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6977">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-6977">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-6978">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-6978">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-6979">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-6979">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6980">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6980">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-6981">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-6981">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-6982">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6982">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-6983">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6983">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-6984">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6984">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-6985">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-6985">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-6986">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-6986">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-6987">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-6987">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-6988">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-6988">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6989">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6989">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-6990">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-6990">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-6992">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-6992">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6993">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-6993">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="5baf9-6994">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-6994">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="5baf9-6995">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-6995">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="5baf9-6996">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-6996">Multisample Load</span></span> | \- |
| <span data-ttu-id="5baf9-6997">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-6997">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-6998">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-6998">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="5baf9-6999">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-6999">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-7000">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-7000">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-7002">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-7002">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-7003">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-7003">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-7004">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-7004">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a><span data-ttu-id="5baf9-7005">DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>FNS</sup> (115)</span><span class="sxs-lookup"><span data-stu-id="5baf9-7005">DXGI_FORMAT_B4G4R4A4\_UNORM<sup>FNS</sup> (115)</span></span>
| <span data-ttu-id="5baf9-7006">Destino</span><span class="sxs-lookup"><span data-stu-id="5baf9-7006">Target</span></span> | <span data-ttu-id="5baf9-7007">Suporte</span><span class="sxs-lookup"><span data-stu-id="5baf9-7007">Support</span></span> |
| - | - |
| <span data-ttu-id="5baf9-7008">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="5baf9-7008">Bits Per Element (BPE)</span></span> | <span data-ttu-id="5baf9-7009">16</span><span class="sxs-lookup"><span data-stu-id="5baf9-7009">16</span></span> |
| <span data-ttu-id="5baf9-7010">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-7010">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-7012">Buffer</span><span class="sxs-lookup"><span data-stu-id="5baf9-7012">Buffer</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-7014">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-7014">Input Assembler Vertex Buffer</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-7016">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="5baf9-7016">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-7017">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="5baf9-7017">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="5baf9-7018">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5baf9-7018">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-7020">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5baf9-7020">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-7022">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5baf9-7022">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-7024">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5baf9-7024">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-7026">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="5baf9-7026">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-7028">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="5baf9-7028">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-7030">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="5baf9-7030">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="5baf9-7031">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="5baf9-7031">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="5baf9-7032">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="5baf9-7032">Shader gather4</span></span> | \- |
| <span data-ttu-id="5baf9-7033">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="5baf9-7033">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="5baf9-7034">Mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-7034">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-7036">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="5baf9-7036">Mipmap Auto-Generation</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-7038">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-7038">RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-7040">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="5baf9-7040">Blendable RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-7042">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="5baf9-7042">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="5baf9-7043">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="5baf9-7043">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="5baf9-7044">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="5baf9-7044">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-7045">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="5baf9-7045">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="5baf9-7046">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="5baf9-7046">Typed UAV</span></span> | \- |
| <span data-ttu-id="5baf9-7047">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-7047">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="5baf9-7048">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-7048">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="5baf9-7049">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-7049">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="5baf9-7050">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="5baf9-7050">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="5baf9-7051">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="5baf9-7051">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="5baf9-7052">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="5baf9-7052">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="5baf9-7053">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="5baf9-7053">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-7054">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="5baf9-7054">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="5baf9-7055">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="5baf9-7055">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-7057">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="5baf9-7057">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-7059">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="5baf9-7059">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-7061">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="5baf9-7061">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-7063">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="5baf9-7063">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="5baf9-7065">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="5baf9-7065">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="5baf9-7067">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="5baf9-7067">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="5baf9-7068">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="5baf9-7068">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="5baf9-7069">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-7069">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="5baf9-7070">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-7070">Video Processor Input</span></span> | \- |
| <span data-ttu-id="5baf9-7071">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-7071">Video Processor Output</span></span> | \- |
| <span data-ttu-id="5baf9-7072">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="5baf9-7072">Shared Resource</span></span> | \- |
| <span data-ttu-id="5baf9-7073">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="5baf9-7073">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="5baf9-7074">Observações de formato</span><span class="sxs-lookup"><span data-stu-id="5baf9-7074">Format notes</span></span>

<span data-ttu-id="5baf9-7075">A finalidade do formato pode mudar de um nível de recurso de hardware para o próximo.</span><span class="sxs-lookup"><span data-stu-id="5baf9-7075">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="5baf9-7076"><sup>L</sup> : formato de tipo informativo</span><span class="sxs-lookup"><span data-stu-id="5baf9-7076"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="5baf9-7077"><sup>PCs</sup> : layout de tipo parcial, convertido e simples</span><span class="sxs-lookup"><span data-stu-id="5baf9-7077"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="5baf9-7078"><sup>FCS</sup> : layout totalmente tipado, convertido e simples</span><span class="sxs-lookup"><span data-stu-id="5baf9-7078"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="5baf9-7079"><sup>FNS</sup> : layout totalmente tipado, não-convertido e simples</span><span class="sxs-lookup"><span data-stu-id="5baf9-7079"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="5baf9-7080"><sup>PCC</sup> : layout complexo, convertido e de tipo parcial</span><span class="sxs-lookup"><span data-stu-id="5baf9-7080"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="5baf9-7081"><sup>FCC</sup> : layout totalmente tipado, convertido e complexo</span><span class="sxs-lookup"><span data-stu-id="5baf9-7081"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="5baf9-7082"><sup>FNC</sup> : layout totalmente tipado, não-convertido e complexo</span><span class="sxs-lookup"><span data-stu-id="5baf9-7082"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="5baf9-7083"><sup>V</sup> : formato de vídeo</span><span class="sxs-lookup"><span data-stu-id="5baf9-7083"><sup>V</sup> : video format</span></span>
</dt> </dl>

<span data-ttu-id="5baf9-7084">Os buffers traseiros e os exames com o formato [**\_ \_ R16G16B16A16 \_ float de formato dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) contêm dados de gama com valor linear.</span><span class="sxs-lookup"><span data-stu-id="5baf9-7084">Back buffers and scan outs with the [**DXGI\_FORMAT\_R16G16B16A16\_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) format contain linear-valued gamma data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5baf9-7085">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5baf9-7085">Related topics</span></span>

[<span data-ttu-id="5baf9-7086">Níveis de recursos de hardware do D3D12</span><span class="sxs-lookup"><span data-stu-id="5baf9-7086">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

[<span data-ttu-id="5baf9-7087">**ID3D10Device::CheckFormatSupport**</span><span class="sxs-lookup"><span data-stu-id="5baf9-7087">**ID3D10Device::CheckFormatSupport**</span></span>](/windows/win32/api/d3d10/nf-d3d10-id3d10device-checkformatsupport)

[<span data-ttu-id="5baf9-7088">Guia de programação para DXGI</span><span class="sxs-lookup"><span data-stu-id="5baf9-7088">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
