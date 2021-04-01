---
description: Esta seção especifica os formatos ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valores) que têm suporte no hardware do nível de recurso do Direct3D 12,1.
ms.assetid: 0DC50FF3-3193-4F3B-9976-EE504C6FCC87
title: Suporte de formato para hardware 12.1 do Nível de Recursos do Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2d20b00a2cfb5b0343a2ebb1a56a1253ddd1966
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645618"
---
# <a name="format-support-for-direct3d-feature-level-121-hardware"></a><span data-ttu-id="80490-103">Suporte de formato para hardware 12.1 do Nível de Recursos do Direct3D</span><span class="sxs-lookup"><span data-stu-id="80490-103">Format support for Direct3D Feature Level 12.1 hardware</span></span>

<span data-ttu-id="80490-104">Esta seção especifica os formatos ([_\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valores) que têm suporte no hardware do nível de recurso do Direct3D 12,1.</span><span class="sxs-lookup"><span data-stu-id="80490-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature Level 12.1 hardware.</span></span>

<span data-ttu-id="80490-105">A tabela resume o suporte a recursos, usando a chave a seguir.</span><span class="sxs-lookup"><span data-stu-id="80490-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="80490-106">Símbolo</span><span class="sxs-lookup"><span data-stu-id="80490-106">Symbol</span></span>                            | <span data-ttu-id="80490-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="80490-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="80490-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="80490-108">_ *-*\*</span></span>                             | <span data-ttu-id="80490-109">Não permitido ou não disponível.</span><span class="sxs-lookup"><span data-stu-id="80490-109">Disallowed or not available.</span></span>                                                  |
| ![exigido](images/letter-r.jpg)  | <span data-ttu-id="80490-111">O suporte a hardware é necessário.</span><span class="sxs-lookup"><span data-stu-id="80490-111">Hardware support is required.</span></span>                                                 |
| ![opcionais](images/letter-o.jpg)  | <span data-ttu-id="80490-113">Suporte a hardware opcional, o formato pode ou não ser acelerado por hardware.</span><span class="sxs-lookup"><span data-stu-id="80490-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![dependentes](images/letter-d.jpg) | <span data-ttu-id="80490-115">Necessário se houver suporte para o recurso opcional relacionado.</span><span class="sxs-lookup"><span data-stu-id="80490-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="80490-116">Este tópico contém uma seção por formato.</span><span class="sxs-lookup"><span data-stu-id="80490-116">This topic contains a section per format.</span></span> <span data-ttu-id="80490-117">Um *destino* de formato (as tabelas contêm uma linha por destino) pode ser um tipo de recurso, uma função intrínseca HLSL ou uma funcionalidade específica que depende de um formato específico.</span><span class="sxs-lookup"><span data-stu-id="80490-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="80490-118">Para verificar programaticamente o suporte a Format em D3D11 e D3D12, consulte [verificando o suporte a recursos de hardware](checking-hardware-feature-support.md).</span><span class="sxs-lookup"><span data-stu-id="80490-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="80490-119">Os números dos formatos são principalmente, mas nem todos, em ordem numérica crescente &mdash; alguns estão fora de ordem numérica e listados junto com outros formatos relevantes.</span><span class="sxs-lookup"><span data-stu-id="80490-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="80490-120">Observe também que sem *tipo* em um nome de formato pode significar digitação *parcial* e não estritamente tipado (consulte a seção [observações de formato](#format-notes) no final do tópico).</span><span class="sxs-lookup"><span data-stu-id="80490-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>

## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="80490-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span><span class="sxs-lookup"><span data-stu-id="80490-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="80490-122">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-122">Target</span></span> | <span data-ttu-id="80490-123">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-123">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-124">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-125">0</span><span class="sxs-lookup"><span data-stu-id="80490-125">0</span></span> |
| <span data-ttu-id="80490-126">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-126">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-128">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-128">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-130">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-130">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-131">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-131">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-132">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-132">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-133">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-134">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-134">Texture2D</span></span> | \- |
| <span data-ttu-id="80490-135">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-135">Texture3D</span></span> | \- |
| <span data-ttu-id="80490-136">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-136">TextureCube</span></span> | \- |
| <span data-ttu-id="80490-137">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-137">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-138">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-138">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-139">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-139">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-140">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-140">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-141">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-141">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-142">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-142">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-143">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-143">Mipmap</span></span> | \- |
| <span data-ttu-id="80490-144">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-144">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-145">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-145">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-146">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-146">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-147">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-147">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-148">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-148">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-149">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-149">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-150">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-150">Structured UAV and SRV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-152">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-152">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-153">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-153">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-154">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-154">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-155">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-155">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-156">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-156">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-157">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-157">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-158">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-158">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-159">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-159">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-160">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-160">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-161">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-161">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-163">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-163">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-164">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-164">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-165">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-165">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-166">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-166">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-167">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-167">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-168">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-168">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-169">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-169">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="80490-170">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-170">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-171">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-171">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-172">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-172">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-173">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-173">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-174">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-174">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-175">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-175">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="80490-177"><sup>Computadores</sup> DXGI_FORMAT_R32G32B32A32_TYPELESS (1)</span><span class="sxs-lookup"><span data-stu-id="80490-177">DXGI_FORMAT_R32G32B32A32_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="80490-178">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-178">Target</span></span> | <span data-ttu-id="80490-179">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-179">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-180">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-180">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-181">128</span><span class="sxs-lookup"><span data-stu-id="80490-181">128</span></span> |
| <span data-ttu-id="80490-182">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-182">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-184">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-184">Buffer</span></span> | \- |
| <span data-ttu-id="80490-185">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-185">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-186">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-186">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-187">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-187">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-188">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-188">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-190">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-190">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-192">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-192">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-194">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-194">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-196">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-196">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-197">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-197">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-198">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-198">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-199">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-199">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-200">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-200">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-201">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-201">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-202">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-202">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-204">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-204">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-205">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-205">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-206">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-206">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-207">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-207">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-208">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-208">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-209">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-209">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-210">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-210">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-211">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-211">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-212">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-212">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-213">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-213">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-214">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-214">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-215">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-215">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-216">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-216">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-217">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-217">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-218">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-218">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-219">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-219">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-220">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-220">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-222">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-222">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-223">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-223">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-224">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-224">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-225">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-225">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-226">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-226">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-227">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-227">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-228">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-228">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-230">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-230">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-231">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-231">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-232">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-232">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-233">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-233">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-235">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-235">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-236">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-236">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_floatsupfcssup-2"></a><span data-ttu-id="80490-238">DXGI_FORMAT_R32G32B32A32_FLOAT<sup>FCS</sup> (2)</span><span class="sxs-lookup"><span data-stu-id="80490-238">DXGI_FORMAT_R32G32B32A32_FLOAT<sup>FCS</sup> (2)</span></span>
| <span data-ttu-id="80490-239">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-239">Target</span></span> | <span data-ttu-id="80490-240">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-240">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-241">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-241">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-242">128</span><span class="sxs-lookup"><span data-stu-id="80490-242">128</span></span> |
| <span data-ttu-id="80490-243">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-243">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-245">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-245">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-247">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-247">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-249">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-249">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-250">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-250">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-252">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-252">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-254">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-254">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-256">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-256">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-258">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-258">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-260">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-260">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-262">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-262">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-264">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-264">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-265">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-265">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-266">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-266">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-268">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-268">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-269">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-269">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-271">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-271">Mipmap Auto- Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-273">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-273">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-275">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-275">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-277">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-277">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-278">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-278">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-279">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-279">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-280">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-280">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-281">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-281">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-283">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-283">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-285">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-285">UAV Typed Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-287">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-287">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-288">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-288">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-289">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-289">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-290">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-290">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-291">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-291">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-292">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-292">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-293">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-293">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-295">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-295">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-297">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-297">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-299">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-299">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-301">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-301">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-303">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-303">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-305">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-305">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-306">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-306">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-308">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-308">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-309">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-309">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-310">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-310">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-311">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-311">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-313">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-313">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-314">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-314">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_uintsupfcssup-3"></a><span data-ttu-id="80490-316">DXGI_FORMAT_R32G32B32A32_UINT<sup>FCS</sup> (3)</span><span class="sxs-lookup"><span data-stu-id="80490-316">DXGI_FORMAT_R32G32B32A32_UINT<sup>FCS</sup> (3)</span></span>
| <span data-ttu-id="80490-317">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-317">Target</span></span> | <span data-ttu-id="80490-318">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-318">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-319">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-319">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-320">128</span><span class="sxs-lookup"><span data-stu-id="80490-320">128</span></span> |
| <span data-ttu-id="80490-321">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-321">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-323">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-323">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-325">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-325">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-327">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-327">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-328">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-328">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-330">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-330">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-332">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-332">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-334">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-334">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-336">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-336">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-338">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-338">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-340">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-340">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-341">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-341">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-342">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-342">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-343">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-343">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-344">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-344">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-345">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-345">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-347">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-347">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-348">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-348">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-350">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-350">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-351">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-351">Output Merger Logic Op</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-353">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-353">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-354">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-354">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-355">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-355">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-356">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-356">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-358">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-358">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-360">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-360">UAV Typed Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-362">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-362">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-363">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-363">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-364">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-364">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-365">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-365">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-366">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-366">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-367">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-367">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-368">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-368">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-370">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-370">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-372">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-372">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-374">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-374">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-376">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-376">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-377">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-377">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-379">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-379">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-380">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-380">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-382">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-382">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-383">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-383">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-384">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-384">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-385">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-385">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-387">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-387">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-388">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-388">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_sintsupfcssup-4"></a><span data-ttu-id="80490-390">DXGI_FORMAT_R32G32B32A32_SINT<sup>FCS</sup> (4)</span><span class="sxs-lookup"><span data-stu-id="80490-390">DXGI_FORMAT_R32G32B32A32_SINT<sup>FCS</sup> (4)</span></span>
| <span data-ttu-id="80490-391">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-391">Target</span></span> | <span data-ttu-id="80490-392">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-392">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-393">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-393">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-394">128</span><span class="sxs-lookup"><span data-stu-id="80490-394">128</span></span> |
| <span data-ttu-id="80490-395">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-395">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-397">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-397">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-399">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-399">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-401">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-401">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-402">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-402">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-404">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-404">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-406">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-406">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-408">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-408">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-410">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-410">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-412">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-412">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-414">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-414">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-415">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-415">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-416">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-416">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-417">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-417">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-418">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-418">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-419">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-419">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-421">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-421">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-422">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-422">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-424">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-424">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-425">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-425">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-426">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-426">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-427">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-427">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-428">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-428">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-429">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-429">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-431">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-431">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-433">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-433">UAV Typed Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-435">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-435">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-436">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-436">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-437">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-437">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-438">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-438">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-439">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-439">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-440">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-440">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-441">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-441">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-443">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-443">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-445">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-445">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-447">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-447">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-449">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-449">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-450">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-450">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-452">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-452">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-453">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-453">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-455">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-455">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-456">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-456">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-457">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-457">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-458">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-458">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-460">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-460">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-461">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-461">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="80490-463"><sup>Computadores</sup> DXGI_FORMAT_R32G32B32_TYPELESS (5)</span><span class="sxs-lookup"><span data-stu-id="80490-463">DXGI_FORMAT_R32G32B32_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="80490-464">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-464">Target</span></span> | <span data-ttu-id="80490-465">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-465">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-466">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-466">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-467">96</span><span class="sxs-lookup"><span data-stu-id="80490-467">96</span></span> |
| <span data-ttu-id="80490-468">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-468">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-470">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-470">Buffer</span></span> | \- |
| <span data-ttu-id="80490-471">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-471">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-472">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-472">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-473">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-473">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-474">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-474">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-476">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-476">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-478">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-478">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-480">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-480">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-482">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-482">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-483">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-483">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-484">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-484">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-485">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-485">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-486">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-486">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-487">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-487">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-488">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-488">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-490">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-490">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-491">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-491">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-492">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-492">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-493">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-493">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-494">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-494">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-495">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-495">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-496">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-496">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-497">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-497">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-498">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-498">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-499">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-499">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-500">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-500">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-501">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-501">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-502">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-502">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-503">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-503">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-504">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-504">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-505">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-505">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-506">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-506">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-508">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-508">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-509">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-509">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-510">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-510">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-511">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-511">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-512">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-512">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-513">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-513">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-514">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-514">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-516">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-516">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-517">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-517">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-518">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-518">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-519">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-519">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-520">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-520">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-521">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-521">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfcssup-6"></a><span data-ttu-id="80490-522">DXGI_FORMAT_R32G32B32_FLOAT<sup>FCS</sup> (6)</span><span class="sxs-lookup"><span data-stu-id="80490-522">DXGI_FORMAT_R32G32B32_FLOAT<sup>FCS</sup> (6)</span></span>
| <span data-ttu-id="80490-523">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-523">Target</span></span> | <span data-ttu-id="80490-524">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-524">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-525">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-525">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-526">96</span><span class="sxs-lookup"><span data-stu-id="80490-526">96</span></span> |
| <span data-ttu-id="80490-527">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-527">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-529">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-529">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-531">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-531">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-533">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-533">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-534">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-534">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-536">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-536">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-538">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-538">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-540">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-540">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-542">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-542">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-544">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-544">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-546">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-546">Shader sample (any filter)</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-548">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-548">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-549">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-549">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-550">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-550">Shader gather4</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-552">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-552">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-553">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-553">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-555">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-555">Mipmap Auto- Generation</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-557">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-557">RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-559">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-559">Blendable RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="80490-561">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-561">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-562">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-562">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-563">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-563">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-564">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-564">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-565">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-565">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-566">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-566">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-567">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-567">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-568">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-568">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-569">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-569">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-570">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-570">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-571">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-571">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-572">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-572">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-573">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-573">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-574">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-574">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-576">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-576">4x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="80490-578">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-578">8x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="80490-580">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-580">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-582">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-582">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-584">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-584">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-586">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-586">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-587">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-587">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-589">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-589">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-590">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-590">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-591">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-591">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-592">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-592">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-593">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-593">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-594">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-594">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfcssup-7"></a><span data-ttu-id="80490-595">DXGI_FORMAT_R32G32B32_UINT<sup>FCS</sup> (7)</span><span class="sxs-lookup"><span data-stu-id="80490-595">DXGI_FORMAT_R32G32B32_UINT<sup>FCS</sup> (7)</span></span>
| <span data-ttu-id="80490-596">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-596">Target</span></span> | <span data-ttu-id="80490-597">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-597">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-598">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-598">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-599">96</span><span class="sxs-lookup"><span data-stu-id="80490-599">96</span></span> |
| <span data-ttu-id="80490-600">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-600">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-602">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-602">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-604">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-604">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-606">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-606">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-607">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-607">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-609">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-609">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-611">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-611">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-613">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-613">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-615">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-615">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-617">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-617">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-619">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-619">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-620">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-620">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-621">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-621">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-622">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-622">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-623">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-623">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-624">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-624">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-626">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-626">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-627">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-627">RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-629">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-629">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-630">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-630">Output Merger Logic Op</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-632">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-632">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-633">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-633">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-634">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-634">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-635">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-635">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-636">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-636">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-637">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-637">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-638">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-638">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-639">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-639">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-640">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-640">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-641">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-641">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-642">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-642">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-643">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-643">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-644">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-644">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-646">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-646">4x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="80490-648">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-648">8x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="80490-650">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-650">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-652">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-652">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-653">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-653">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-655">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-655">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-656">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-656">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-658">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-658">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-659">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-659">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-660">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-660">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-661">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-661">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-662">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-662">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-663">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-663">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfcssup-8"></a><span data-ttu-id="80490-664">DXGI_FORMAT_R32G32B32_SINT<sup>FCS</sup> (8)</span><span class="sxs-lookup"><span data-stu-id="80490-664">DXGI_FORMAT_R32G32B32_SINT<sup>FCS</sup> (8)</span></span>
| <span data-ttu-id="80490-665">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-665">Target</span></span> | <span data-ttu-id="80490-666">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-666">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-667">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-667">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-668">96</span><span class="sxs-lookup"><span data-stu-id="80490-668">96</span></span> |
| <span data-ttu-id="80490-669">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-669">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-671">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-671">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-673">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-673">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-675">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-675">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-676">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-676">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-678">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-678">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-680">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-680">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-682">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-682">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-684">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-684">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-686">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-686">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-688">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-688">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-689">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-689">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-690">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-690">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-691">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-691">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-692">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-692">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-693">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-693">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-695">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-695">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-696">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-696">RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-698">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-698">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-699">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-699">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-700">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-700">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-701">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-701">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-702">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-702">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-703">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-703">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-704">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-704">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-705">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-705">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-706">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-706">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-707">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-707">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-708">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-708">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-709">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-709">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-710">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-710">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-711">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-711">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-712">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-712">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-714">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-714">4x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="80490-716">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-716">8x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="80490-718">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-718">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-720">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-720">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-721">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-721">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-723">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-723">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-724">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-724">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-726">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-726">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-727">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-727">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-728">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-728">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-729">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-729">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-730">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-730">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-731">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-731">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="80490-732"><sup>Computadores</sup> DXGI_FORMAT_R16G16B16A16_TYPELESS (9)</span><span class="sxs-lookup"><span data-stu-id="80490-732">DXGI_FORMAT_R16G16B16A16_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="80490-733">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-733">Target</span></span> | <span data-ttu-id="80490-734">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-734">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-735">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-735">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-736">64</span><span class="sxs-lookup"><span data-stu-id="80490-736">64</span></span> |
| <span data-ttu-id="80490-737">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-737">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-739">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-739">Buffer</span></span> | \- |
| <span data-ttu-id="80490-740">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-740">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-741">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-741">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-742">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-742">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-743">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-743">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-745">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-745">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-747">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-747">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-749">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-749">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-751">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-751">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-752">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-752">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-753">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-753">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-754">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-754">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-755">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-755">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-756">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-756">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-757">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-757">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-759">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-759">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-760">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-760">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-761">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-761">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-762">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-762">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-763">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-763">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-764">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-764">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-765">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-765">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-766">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-766">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-767">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-767">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-768">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-768">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-769">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-769">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-770">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-770">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-771">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-771">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-772">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-772">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-773">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-773">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-774">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-774">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-775">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-775">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-777">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-777">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-778">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-778">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-779">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-779">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-780">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-780">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-781">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-781">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-782">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-782">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-783">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-783">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-785">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-785">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-786">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-786">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-787">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-787">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-788">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-788">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-790">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-790">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-791">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-791">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_floatsupfcssup-10"></a><span data-ttu-id="80490-793">DXGI_FORMAT_R16G16B16A16_FLOAT<sup>FCS</sup> (10)</span><span class="sxs-lookup"><span data-stu-id="80490-793">DXGI_FORMAT_R16G16B16A16_FLOAT<sup>FCS</sup> (10)</span></span>
| <span data-ttu-id="80490-794">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-794">Target</span></span> | <span data-ttu-id="80490-795">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-795">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-796">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-796">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-797">64</span><span class="sxs-lookup"><span data-stu-id="80490-797">64</span></span> |
| <span data-ttu-id="80490-798">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-798">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-800">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-800">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-802">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-802">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-804">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-804">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-805">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-805">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-806">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-806">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-808">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-808">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-810">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-810">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-812">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-812">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-814">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-814">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-816">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-816">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-818">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-818">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-819">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-819">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-820">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-820">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-822">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-822">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-823">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-823">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-825">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-825">Mipmap Auto- Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-827">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-827">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-829">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-829">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-831">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-831">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-832">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-832">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-833">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-833">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-834">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-834">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-835">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-835">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-837">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-837">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-839">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-839">UAV Typed Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-841">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-841">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-842">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-842">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-843">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-843">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-844">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-844">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-845">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-845">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-846">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-846">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-847">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-847">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-849">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-849">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-851">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-851">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-853">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-853">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-855">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-855">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-857">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-857">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-859">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-859">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-861">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-861">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-863">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-863">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-864">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-864">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-866">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-866">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-868">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-868">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-870">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-870">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-871">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-871">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_unormsupfcssup-11"></a><span data-ttu-id="80490-873"><sup>FCS</sup> DXGI_FORMAT_R16G16B16A16_UNORM (11)</span><span class="sxs-lookup"><span data-stu-id="80490-873">DXGI_FORMAT_R16G16B16A16_UNORM<sup>FCS</sup> (11)</span></span>
| <span data-ttu-id="80490-874">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-874">Target</span></span> | <span data-ttu-id="80490-875">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-875">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-876">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-876">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-877">64</span><span class="sxs-lookup"><span data-stu-id="80490-877">64</span></span> |
| <span data-ttu-id="80490-878">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-878">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-880">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-880">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-882">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-882">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-884">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-884">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-885">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-885">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-886">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-886">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-888">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-888">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-890">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-890">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-892">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-892">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-894">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-894">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-896">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-896">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-898">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-898">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-899">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-899">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-900">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-900">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-902">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-902">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-903">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-903">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-905">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-905">Mipmap Auto- Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-907">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-907">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-909">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-909">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-911">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-911">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-912">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-912">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-913">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-913">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-914">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-914">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-915">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-915">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-917">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-917">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-919">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-919">UAV Typed Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-921">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-921">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-922">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-922">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-923">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-923">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-924">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-924">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-925">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-925">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-926">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-926">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-927">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-927">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-929">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-929">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-931">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-931">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-933">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-933">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-935">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-935">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-937">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-937">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-939">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-939">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-940">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-940">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-942">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-942">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-943">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-943">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-944">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-944">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-945">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-945">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-947">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-947">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-948">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-948">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_uintsupfcssup-12"></a><span data-ttu-id="80490-950"><sup>FCS</sup> DXGI_FORMAT_R16G16B16A16_UINT (12)</span><span class="sxs-lookup"><span data-stu-id="80490-950">DXGI_FORMAT_R16G16B16A16_UINT<sup>FCS</sup> (12)</span></span>
| <span data-ttu-id="80490-951">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-951">Target</span></span> | <span data-ttu-id="80490-952">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-952">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-953">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-953">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-954">64</span><span class="sxs-lookup"><span data-stu-id="80490-954">64</span></span> |
| <span data-ttu-id="80490-955">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-955">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-957">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-957">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-959">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-959">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-961">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-961">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-962">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-962">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-963">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-963">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-965">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-965">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-967">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-967">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-969">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-969">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-971">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-971">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-973">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-973">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-974">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-974">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-975">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-975">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-976">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-976">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-977">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-977">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-978">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-978">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-980">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-980">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-981">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-981">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-983">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-983">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-984">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-984">Output Merger Logic Op</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-986">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-986">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-987">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-987">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-988">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-988">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-989">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-989">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-991">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-991">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-993">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-993">UAV Typed Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-995">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-995">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-996">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-996">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-997">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-997">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-998">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-998">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-999">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-999">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-1000">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-1000">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-1001">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-1001">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1003">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-1003">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1005">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-1005">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1007">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-1007">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-1009">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-1009">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-1010">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-1010">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1012">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-1012">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-1013">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-1013">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1015">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1015">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-1016">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1016">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-1017">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1017">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-1018">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-1018">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1020">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-1020">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-1021">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-1021">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_snormsupfcssup-13"></a><span data-ttu-id="80490-1023"><sup>FCS</sup> DXGI_FORMAT_R16G16B16A16_SNORM (13)</span><span class="sxs-lookup"><span data-stu-id="80490-1023">DXGI_FORMAT_R16G16B16A16_SNORM<sup>FCS</sup> (13)</span></span>
| <span data-ttu-id="80490-1024">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-1024">Target</span></span> | <span data-ttu-id="80490-1025">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-1025">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-1026">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-1026">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-1027">64</span><span class="sxs-lookup"><span data-stu-id="80490-1027">64</span></span> |
| <span data-ttu-id="80490-1028">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-1028">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1030">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-1030">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1032">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-1032">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1034">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-1034">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-1035">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-1035">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-1036">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-1036">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1038">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-1038">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1040">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-1040">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1042">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-1042">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1044">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-1044">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1046">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-1046">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1048">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-1048">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-1049">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-1049">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-1050">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-1050">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1052">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-1052">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-1053">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-1053">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1055">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-1055">Mipmap Auto- Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1057">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-1057">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1059">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-1059">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1061">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-1061">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-1062">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-1062">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-1063">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-1063">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-1064">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-1064">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-1065">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-1065">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1067">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1067">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1069">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1069">UAV Typed Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-1071">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1071">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-1072">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-1072">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-1073">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-1073">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-1074">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1074">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-1075">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-1075">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-1076">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-1076">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-1077">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-1077">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1079">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-1079">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1081">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-1081">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1083">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-1083">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-1085">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-1085">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1087">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-1087">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1089">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-1089">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-1090">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-1090">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1092">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1092">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-1093">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1093">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-1094">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1094">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-1095">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-1095">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1097">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-1097">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-1098">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-1098">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_sintsupfcssup-14"></a><span data-ttu-id="80490-1100"><sup>FCS</sup> DXGI_FORMAT_R16G16B16A16_SINT (14)</span><span class="sxs-lookup"><span data-stu-id="80490-1100">DXGI_FORMAT_R16G16B16A16_SINT<sup>FCS</sup> (14)</span></span>
| <span data-ttu-id="80490-1101">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-1101">Target</span></span> | <span data-ttu-id="80490-1102">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-1102">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-1103">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-1103">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-1104">64</span><span class="sxs-lookup"><span data-stu-id="80490-1104">64</span></span> |
| <span data-ttu-id="80490-1105">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-1105">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1107">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-1107">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1109">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-1109">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1111">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-1111">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-1112">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-1112">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-1113">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-1113">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1115">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-1115">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1117">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-1117">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1119">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-1119">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1121">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-1121">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1123">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-1123">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-1124">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-1124">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-1125">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-1125">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-1126">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-1126">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-1127">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-1127">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-1128">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-1128">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1130">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-1130">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-1131">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-1131">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1133">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-1133">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-1134">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-1134">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-1135">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-1135">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-1136">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-1136">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-1137">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-1137">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-1138">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-1138">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1140">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1140">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1142">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1142">UAV Typed Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1144">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1144">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-1145">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-1145">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-1146">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-1146">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-1147">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1147">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-1148">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-1148">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-1149">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-1149">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-1150">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-1150">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1152">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-1152">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1154">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-1154">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1156">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-1156">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-1158">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-1158">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-1159">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-1159">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1161">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-1161">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-1162">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-1162">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1164">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1164">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-1165">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1165">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-1166">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1166">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-1167">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-1167">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1169">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-1169">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-1170">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-1170">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="80490-1172"><sup>Computadores</sup> DXGI_FORMAT_R32G32_TYPELESS (15)</span><span class="sxs-lookup"><span data-stu-id="80490-1172">DXGI_FORMAT_R32G32_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="80490-1173">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-1173">Target</span></span> | <span data-ttu-id="80490-1174">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-1174">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-1175">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-1175">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-1176">64</span><span class="sxs-lookup"><span data-stu-id="80490-1176">64</span></span> |
| <span data-ttu-id="80490-1177">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-1177">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1179">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-1179">Buffer</span></span> | \- |
| <span data-ttu-id="80490-1180">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-1180">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-1181">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-1181">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-1182">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-1182">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-1183">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-1183">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1185">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-1185">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1187">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-1187">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1189">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-1189">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1191">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-1191">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-1192">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-1192">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-1193">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-1193">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-1194">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-1194">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-1195">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-1195">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-1196">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-1196">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-1197">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-1197">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1199">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-1199">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-1200">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-1200">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-1201">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-1201">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-1202">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-1202">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-1203">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-1203">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-1204">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-1204">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-1205">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-1205">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-1206">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-1206">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-1207">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1207">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-1208">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1208">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-1209">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1209">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-1210">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-1210">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-1211">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-1211">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-1212">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1212">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-1213">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-1213">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-1214">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-1214">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-1215">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-1215">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1217">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-1217">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-1218">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-1218">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-1219">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-1219">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-1220">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-1220">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-1221">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-1221">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-1222">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-1222">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-1223">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-1223">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1225">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1225">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-1226">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1226">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-1227">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1227">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-1228">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-1228">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-1229">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-1229">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-1230">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-1230">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_floatsupfcssup-16"></a><span data-ttu-id="80490-1232">DXGI_FORMAT_R32G32_FLOAT<sup>FCS</sup> (16)</span><span class="sxs-lookup"><span data-stu-id="80490-1232">DXGI_FORMAT_R32G32_FLOAT<sup>FCS</sup> (16)</span></span>
| <span data-ttu-id="80490-1233">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-1233">Target</span></span> | <span data-ttu-id="80490-1234">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-1234">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-1235">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-1235">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-1236">64</span><span class="sxs-lookup"><span data-stu-id="80490-1236">64</span></span> |
| <span data-ttu-id="80490-1237">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-1237">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1239">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-1239">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1241">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-1241">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1243">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-1243">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-1244">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-1244">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1246">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-1246">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1248">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-1248">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1250">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-1250">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1252">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-1252">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1254">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-1254">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1256">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-1256">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1258">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-1258">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-1259">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-1259">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-1260">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-1260">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1262">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-1262">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-1263">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-1263">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1265">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-1265">Mipmap Auto- Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1267">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-1267">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1269">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-1269">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1271">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-1271">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-1272">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-1272">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-1273">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-1273">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-1274">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-1274">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-1275">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-1275">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1277">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1277">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1279">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1279">UAV Typed Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-1281">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1281">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-1282">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-1282">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-1283">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-1283">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-1284">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1284">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-1285">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-1285">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-1286">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-1286">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-1287">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-1287">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1289">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-1289">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1291">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-1291">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1293">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-1293">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-1295">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-1295">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1297">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-1297">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1299">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-1299">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-1300">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-1300">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1302">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1302">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-1303">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1303">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-1304">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1304">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-1305">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-1305">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-1306">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-1306">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-1307">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-1307">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_uintsupfcssup-17"></a><span data-ttu-id="80490-1309"><sup>FCS</sup> DXGI_FORMAT_R32G32_UINT (17)</span><span class="sxs-lookup"><span data-stu-id="80490-1309">DXGI_FORMAT_R32G32_UINT<sup>FCS</sup> (17)</span></span>
| <span data-ttu-id="80490-1310">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-1310">Target</span></span> | <span data-ttu-id="80490-1311">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-1311">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-1312">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-1312">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-1313">64</span><span class="sxs-lookup"><span data-stu-id="80490-1313">64</span></span> |
| <span data-ttu-id="80490-1314">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-1314">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1316">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-1316">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1318">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-1318">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1320">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-1320">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-1321">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-1321">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1323">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-1323">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1325">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-1325">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1327">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-1327">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1329">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-1329">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1331">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-1331">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1333">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-1333">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-1334">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-1334">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-1335">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-1335">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-1336">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-1336">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-1337">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-1337">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-1338">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-1338">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1340">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-1340">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-1341">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-1341">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1343">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-1343">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-1344">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-1344">Output Merger Logic Op</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1346">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-1346">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-1347">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-1347">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-1348">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-1348">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-1349">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-1349">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1351">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1351">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1353">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1353">UAV Typed Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-1355">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1355">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-1356">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-1356">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-1357">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-1357">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-1358">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1358">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-1359">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-1359">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-1360">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-1360">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-1361">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-1361">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1363">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-1363">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1365">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-1365">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1367">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-1367">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-1369">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-1369">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-1370">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-1370">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1372">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-1372">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-1373">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-1373">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1375">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1375">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-1376">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1376">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-1377">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1377">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-1378">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-1378">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-1379">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-1379">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-1380">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-1380">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_sintsupfcssup-18"></a><span data-ttu-id="80490-1382">DXGI_FORMAT_R32G32_SINT<sup>FCS</sup> (18)</span><span class="sxs-lookup"><span data-stu-id="80490-1382">DXGI_FORMAT_R32G32_SINT<sup>FCS</sup> (18)</span></span>
| <span data-ttu-id="80490-1383">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-1383">Target</span></span> | <span data-ttu-id="80490-1384">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-1384">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-1385">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-1385">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-1386">64</span><span class="sxs-lookup"><span data-stu-id="80490-1386">64</span></span> |
| <span data-ttu-id="80490-1387">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-1387">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1389">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-1389">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1391">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-1391">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1393">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-1393">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-1394">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-1394">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1396">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-1396">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1398">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-1398">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1400">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-1400">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1402">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-1402">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1404">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-1404">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1406">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-1406">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-1407">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-1407">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-1408">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-1408">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-1409">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-1409">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-1410">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-1410">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-1411">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-1411">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1413">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-1413">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-1414">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-1414">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1416">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-1416">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-1417">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-1417">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-1418">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-1418">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-1419">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-1419">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-1420">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-1420">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-1421">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-1421">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1423">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1423">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1425">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1425">UAV Typed Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-1427">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1427">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-1428">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-1428">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-1429">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-1429">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-1430">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1430">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-1431">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-1431">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-1432">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-1432">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-1433">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-1433">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1435">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-1435">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1437">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-1437">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1439">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-1439">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-1441">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-1441">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-1442">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-1442">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1444">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-1444">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-1445">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-1445">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1447">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1447">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-1448">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1448">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-1449">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1449">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-1450">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-1450">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-1451">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-1451">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-1452">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-1452">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r32g8x24_typelesssupvsup-19"></a><span data-ttu-id="80490-1454">DXGI_FORMAT_R32G8X24_TYPELESS<sup>V</sup> (19)</span><span class="sxs-lookup"><span data-stu-id="80490-1454">DXGI_FORMAT_R32G8X24_TYPELESS<sup>V</sup> (19)</span></span>
| <span data-ttu-id="80490-1455">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-1455">Target</span></span> | <span data-ttu-id="80490-1456">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-1456">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-1457">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-1457">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-1458">64</span><span class="sxs-lookup"><span data-stu-id="80490-1458">64</span></span> |
| <span data-ttu-id="80490-1459">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-1459">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1461">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-1461">Buffer</span></span> | \- |
| <span data-ttu-id="80490-1462">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-1462">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-1463">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-1463">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-1464">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-1464">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-1465">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-1465">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1467">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-1467">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1469">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-1469">Texture3D</span></span> | \- |
| <span data-ttu-id="80490-1470">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-1470">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1472">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-1472">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-1473">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-1473">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-1474">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-1474">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-1475">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-1475">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-1476">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-1476">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-1477">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-1477">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-1478">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-1478">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1480">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-1480">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-1481">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-1481">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-1482">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-1482">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-1483">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-1483">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-1484">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-1484">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-1485">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-1485">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-1486">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-1486">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-1487">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-1487">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-1488">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1488">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-1489">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1489">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-1490">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1490">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-1491">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-1491">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-1492">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-1492">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-1493">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1493">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-1494">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-1494">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-1495">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-1495">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-1496">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-1496">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1498">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-1498">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-1499">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-1499">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-1500">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-1500">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-1501">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-1501">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-1502">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-1502">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-1503">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-1503">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-1504">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-1504">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1506">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1506">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-1507">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1507">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-1508">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1508">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-1509">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-1509">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-1510">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-1510">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-1511">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-1511">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupvsup-20"></a><span data-ttu-id="80490-1512">DXGI_FORMAT_D32_FLOAT_S8X24_UINT<sup>V</sup> (20)</span><span class="sxs-lookup"><span data-stu-id="80490-1512">DXGI_FORMAT_D32_FLOAT_S8X24_UINT<sup>V</sup> (20)</span></span>
| <span data-ttu-id="80490-1513">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-1513">Target</span></span> | <span data-ttu-id="80490-1514">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-1514">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-1515">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-1515">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-1516">64</span><span class="sxs-lookup"><span data-stu-id="80490-1516">64</span></span> |
| <span data-ttu-id="80490-1517">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-1517">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1519">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-1519">Buffer</span></span> | \- |
| <span data-ttu-id="80490-1520">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-1520">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-1521">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-1521">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-1522">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-1522">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-1523">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-1523">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1525">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-1525">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1527">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-1527">Texture3D</span></span> | \- |
| <span data-ttu-id="80490-1528">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-1528">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1530">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-1530">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-1531">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-1531">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-1532">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-1532">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-1533">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-1533">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-1534">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-1534">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-1535">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-1535">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-1536">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-1536">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1538">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-1538">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-1539">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-1539">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-1540">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-1540">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-1541">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-1541">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-1542">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-1542">Depth/Stencil Target</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1544">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-1544">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-1545">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-1545">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-1546">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-1546">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-1547">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1547">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-1548">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1548">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-1549">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1549">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-1550">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-1550">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-1551">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-1551">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-1552">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1552">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-1553">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-1553">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-1554">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-1554">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-1555">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-1555">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1557">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-1557">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1559">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-1559">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1561">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-1561">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-1563">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-1563">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-1564">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-1564">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-1565">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-1565">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-1566">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-1566">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1568">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1568">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-1569">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1569">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-1570">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1570">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-1571">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-1571">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-1572">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-1572">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-1573">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-1573">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupvsup-21"></a><span data-ttu-id="80490-1574">DXGI_FORMAT_R32_FLOAT_X8X24_TYPELESS<sup>V</sup> (21)</span><span class="sxs-lookup"><span data-stu-id="80490-1574">DXGI_FORMAT_R32_FLOAT_X8X24_TYPELESS<sup>V</sup> (21)</span></span>
| <span data-ttu-id="80490-1575">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-1575">Target</span></span> | <span data-ttu-id="80490-1576">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-1576">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-1577">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-1577">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-1578">64</span><span class="sxs-lookup"><span data-stu-id="80490-1578">64</span></span> |
| <span data-ttu-id="80490-1579">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-1579">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1581">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-1581">Buffer</span></span> | \- |
| <span data-ttu-id="80490-1582">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-1582">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-1583">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-1583">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-1584">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-1584">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-1585">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-1585">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1587">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-1587">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1589">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-1589">Texture3D</span></span> | \- |
| <span data-ttu-id="80490-1590">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-1590">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1592">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-1592">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1594">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-1594">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1596">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-1596">Shader sample_c (comparison filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1598">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-1598">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-1599">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-1599">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1601">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-1601">Shader gather4_c</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1603">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-1603">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1605">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-1605">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-1606">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-1606">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-1607">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-1607">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-1608">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-1608">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-1609">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-1609">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-1610">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-1610">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-1611">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-1611">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-1612">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-1612">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-1613">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1613">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-1614">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1614">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-1615">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1615">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-1616">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-1616">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-1617">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-1617">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-1618">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1618">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-1619">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-1619">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-1620">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-1620">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-1621">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-1621">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1623">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-1623">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-1624">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-1624">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-1625">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-1625">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-1626">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-1626">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-1627">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-1627">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1629">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-1629">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-1630">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-1630">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1632">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1632">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-1633">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1633">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-1634">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1634">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-1635">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-1635">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-1636">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-1636">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-1637">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-1637">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupvsup-22"></a><span data-ttu-id="80490-1638">DXGI_FORMAT_X32_TYPELESS_G8X24_UINT<sup>V</sup> (22)</span><span class="sxs-lookup"><span data-stu-id="80490-1638">DXGI_FORMAT_X32_TYPELESS_G8X24_UINT<sup>V</sup> (22)</span></span>
| <span data-ttu-id="80490-1639">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-1639">Target</span></span> | <span data-ttu-id="80490-1640">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-1640">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-1641">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-1641">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-1642">64</span><span class="sxs-lookup"><span data-stu-id="80490-1642">64</span></span> |
| <span data-ttu-id="80490-1643">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-1643">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1645">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-1645">Buffer</span></span> | \- |
| <span data-ttu-id="80490-1646">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-1646">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-1647">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-1647">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-1648">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-1648">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-1649">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-1649">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1651">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-1651">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1653">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-1653">Texture3D</span></span> | \- |
| <span data-ttu-id="80490-1654">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-1654">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1656">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-1656">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1658">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-1658">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-1659">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-1659">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-1660">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-1660">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-1661">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-1661">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-1662">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-1662">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-1663">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-1663">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1665">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-1665">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-1666">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-1666">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-1667">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-1667">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-1668">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-1668">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-1669">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-1669">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-1670">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-1670">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-1671">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-1671">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-1672">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-1672">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-1673">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1673">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-1674">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1674">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-1675">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1675">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-1676">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-1676">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-1677">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-1677">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-1678">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1678">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-1679">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-1679">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-1680">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-1680">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-1681">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-1681">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1683">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-1683">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-1684">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-1684">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-1685">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-1685">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-1686">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-1686">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-1687">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-1687">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1689">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-1689">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-1690">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-1690">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1692">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1692">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-1693">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1693">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-1694">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1694">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-1695">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-1695">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-1696">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-1696">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-1697">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-1697">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="80490-1698"><sup>Computadores</sup> DXGI_FORMAT_R10G10B10A2_TYPELESS (23)</span><span class="sxs-lookup"><span data-stu-id="80490-1698">DXGI_FORMAT_R10G10B10A2_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="80490-1699">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-1699">Target</span></span> | <span data-ttu-id="80490-1700">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-1700">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-1701">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-1701">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-1702">32</span><span class="sxs-lookup"><span data-stu-id="80490-1702">32</span></span> |
| <span data-ttu-id="80490-1703">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-1703">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1705">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-1705">Buffer</span></span> | \- |
| <span data-ttu-id="80490-1706">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-1706">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-1707">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-1707">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-1708">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-1708">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-1709">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-1709">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1711">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-1711">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1713">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-1713">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1715">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-1715">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1717">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-1717">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-1718">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-1718">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-1719">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-1719">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-1720">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-1720">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-1721">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-1721">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-1722">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-1722">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-1723">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-1723">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1725">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-1725">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-1726">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-1726">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-1727">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-1727">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-1728">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-1728">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-1729">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-1729">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-1730">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-1730">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-1731">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-1731">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-1732">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-1732">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-1733">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1733">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-1734">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1734">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-1735">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1735">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-1736">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-1736">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-1737">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-1737">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-1738">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1738">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-1739">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-1739">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-1740">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-1740">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-1741">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-1741">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1743">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-1743">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-1744">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-1744">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-1745">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-1745">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-1746">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-1746">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-1747">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-1747">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-1748">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-1748">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-1749">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-1749">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1751">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1751">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-1752">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1752">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-1753">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1753">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-1754">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-1754">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1756">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-1756">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-1757">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-1757">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r10g10b10a2_unormsupfcssup-24"></a><span data-ttu-id="80490-1759"><sup>FCS</sup> DXGI_FORMAT_R10G10B10A2_UNORM (24)</span><span class="sxs-lookup"><span data-stu-id="80490-1759">DXGI_FORMAT_R10G10B10A2_UNORM<sup>FCS</sup> (24)</span></span>
| <span data-ttu-id="80490-1760">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-1760">Target</span></span> | <span data-ttu-id="80490-1761">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-1761">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-1762">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-1762">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-1763">32</span><span class="sxs-lookup"><span data-stu-id="80490-1763">32</span></span> |
| <span data-ttu-id="80490-1764">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-1764">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1766">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-1766">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1768">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-1768">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1770">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-1770">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-1771">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-1771">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-1772">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-1772">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1774">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-1774">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1776">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-1776">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1778">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-1778">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1780">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-1780">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1782">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-1782">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1784">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-1784">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-1785">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-1785">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-1786">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-1786">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1788">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-1788">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-1789">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-1789">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1791">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-1791">Mipmap Auto- Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1793">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-1793">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1795">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-1795">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1797">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-1797">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-1798">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-1798">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-1799">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-1799">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-1800">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-1800">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-1801">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-1801">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1803">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1803">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1805">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1805">UAV Typed Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-1807">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1807">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-1808">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-1808">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-1809">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-1809">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-1810">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1810">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-1811">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-1811">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-1812">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-1812">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-1813">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-1813">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1815">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-1815">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1817">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-1817">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1819">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-1819">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-1821">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-1821">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1823">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-1823">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1825">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-1825">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1827">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-1827">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1829">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1829">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-1830">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1830">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-1832">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1832">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1834">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-1834">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1836">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-1836">BackBuffer Castable Even Fully Typed</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1838">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-1838">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r10g10b10a2_uintsupfcssup-25"></a><span data-ttu-id="80490-1840">DXGI_FORMAT_R10G10B10A2_UINT<sup>FCS</sup> (25)</span><span class="sxs-lookup"><span data-stu-id="80490-1840">DXGI_FORMAT_R10G10B10A2_UINT<sup>FCS</sup> (25)</span></span>
| <span data-ttu-id="80490-1841">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-1841">Target</span></span> | <span data-ttu-id="80490-1842">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-1842">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-1843">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-1843">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-1844">32</span><span class="sxs-lookup"><span data-stu-id="80490-1844">32</span></span> |
| <span data-ttu-id="80490-1845">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-1845">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1847">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-1847">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1849">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-1849">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1851">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-1851">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-1852">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-1852">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-1853">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-1853">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1855">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-1855">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1857">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-1857">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1859">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-1859">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1861">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-1861">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1863">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-1863">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-1864">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-1864">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-1865">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-1865">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-1866">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-1866">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-1867">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-1867">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-1868">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-1868">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1870">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-1870">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-1871">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-1871">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1873">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-1873">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-1874">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-1874">Output Merger Logic Op</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1876">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-1876">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-1877">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-1877">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-1878">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-1878">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-1879">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-1879">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1881">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1881">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1883">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1883">UAV Typed Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-1885">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1885">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-1886">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-1886">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-1887">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-1887">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-1888">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1888">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-1889">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-1889">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-1890">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-1890">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-1891">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-1891">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1893">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-1893">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1895">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-1895">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1897">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-1897">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-1899">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-1899">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-1900">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-1900">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1902">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-1902">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-1903">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-1903">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1905">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1905">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-1906">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1906">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-1907">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1907">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-1908">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-1908">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1910">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-1910">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-1911">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-1911">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfcssup-89"></a><span data-ttu-id="80490-1913">DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM<sup>FCS</sup> (89)</span><span class="sxs-lookup"><span data-stu-id="80490-1913">DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM<sup>FCS</sup> (89)</span></span>
| <span data-ttu-id="80490-1914">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-1914">Target</span></span> | <span data-ttu-id="80490-1915">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-1915">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-1916">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-1916">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-1917">32</span><span class="sxs-lookup"><span data-stu-id="80490-1917">32</span></span> |
| <span data-ttu-id="80490-1918">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-1918">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1920">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-1920">Buffer</span></span> | \- |
| <span data-ttu-id="80490-1921">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-1921">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-1922">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-1922">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-1923">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-1923">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-1924">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-1924">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-1925">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-1925">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1927">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-1927">Texture3D</span></span> | \- |
| <span data-ttu-id="80490-1928">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-1928">TextureCube</span></span> | \- |
| <span data-ttu-id="80490-1929">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-1929">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-1930">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-1930">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-1931">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-1931">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-1932">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-1932">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-1933">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-1933">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-1934">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-1934">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-1935">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-1935">Mipmap</span></span> | \- |
| <span data-ttu-id="80490-1936">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-1936">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-1937">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-1937">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-1938">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-1938">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-1939">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-1939">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-1940">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-1940">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-1941">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-1941">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-1942">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-1942">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-1943">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-1943">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-1944">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1944">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-1945">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1945">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-1946">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1946">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-1947">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-1947">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-1948">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-1948">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-1949">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-1949">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-1950">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-1950">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-1951">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-1951">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-1952">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-1952">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1954">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-1954">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-1955">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-1955">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-1956">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-1956">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-1957">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-1957">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-1958">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-1958">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-1959">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-1959">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1961">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-1961">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1963">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1963">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-1964">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1964">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-1966">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-1966">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1968">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-1968">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1970">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-1970">BackBuffer Castable Even Fully Typed</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1972">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-1972">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="80490-1974">DXGI_FORMAT_R11G11B10_FLOAT<sup>FNS</sup> (26)</span><span class="sxs-lookup"><span data-stu-id="80490-1974">DXGI_FORMAT_R11G11B10_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="80490-1975">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-1975">Target</span></span> | <span data-ttu-id="80490-1976">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-1976">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-1977">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-1977">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-1978">32</span><span class="sxs-lookup"><span data-stu-id="80490-1978">32</span></span> |
| <span data-ttu-id="80490-1979">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-1979">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1981">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-1981">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1983">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-1983">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1985">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-1985">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-1986">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-1986">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-1987">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-1987">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1989">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-1989">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1991">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-1991">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1993">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-1993">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1995">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-1995">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1997">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-1997">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-1999">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-1999">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-2000">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-2000">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-2001">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-2001">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2003">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-2003">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-2004">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-2004">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2006">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-2006">Mipmap Auto- Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2008">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-2008">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2010">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-2010">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2012">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-2012">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-2013">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-2013">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-2014">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-2014">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-2015">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-2015">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-2016">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-2016">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2018">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2018">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2020">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2020">UAV Typed Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-2022">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2022">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-2023">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-2023">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-2024">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-2024">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-2025">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2025">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-2026">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-2026">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-2027">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-2027">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-2028">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-2028">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2030">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-2030">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2032">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-2032">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2034">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-2034">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-2036">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-2036">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2038">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-2038">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2040">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-2040">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-2041">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-2041">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="80490-2042">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2042">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-2043">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2043">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-2044">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2044">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-2045">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-2045">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-2046">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-2046">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-2047">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-2047">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="80490-2049"><sup>Computadores</sup> DXGI_FORMAT_R8G8B8A8_TYPELESS (27)</span><span class="sxs-lookup"><span data-stu-id="80490-2049">DXGI_FORMAT_R8G8B8A8_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="80490-2050">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-2050">Target</span></span> | <span data-ttu-id="80490-2051">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-2051">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-2052">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-2052">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-2053">32</span><span class="sxs-lookup"><span data-stu-id="80490-2053">32</span></span> |
| <span data-ttu-id="80490-2054">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-2054">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2056">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-2056">Buffer</span></span> | \- |
| <span data-ttu-id="80490-2057">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-2057">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-2058">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-2058">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-2059">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-2059">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-2060">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-2060">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2062">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-2062">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2064">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-2064">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2066">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-2066">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2068">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-2068">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-2069">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-2069">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-2070">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-2070">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-2071">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-2071">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-2072">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-2072">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-2073">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-2073">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-2074">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-2074">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2076">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-2076">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-2077">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-2077">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-2078">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-2078">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-2079">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-2079">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-2080">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-2080">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-2081">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-2081">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-2082">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-2082">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-2083">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-2083">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-2084">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2084">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-2085">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2085">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-2086">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2086">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-2087">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-2087">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-2088">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-2088">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-2089">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2089">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-2090">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-2090">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-2091">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-2091">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-2092">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-2092">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2094">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-2094">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-2095">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-2095">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-2096">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-2096">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-2097">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-2097">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-2098">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-2098">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-2099">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-2099">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-2100">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-2100">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2102">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2102">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-2103">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2103">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-2104">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2104">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-2105">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-2105">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2107">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-2107">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-2108">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-2108">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_unormsupfcssup-28"></a><span data-ttu-id="80490-2110"><sup>FCS</sup> DXGI_FORMAT_R8G8B8A8_UNORM (28)</span><span class="sxs-lookup"><span data-stu-id="80490-2110">DXGI_FORMAT_R8G8B8A8_UNORM<sup>FCS</sup> (28)</span></span>
| <span data-ttu-id="80490-2111">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-2111">Target</span></span> | <span data-ttu-id="80490-2112">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-2112">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-2113">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-2113">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-2114">32</span><span class="sxs-lookup"><span data-stu-id="80490-2114">32</span></span> |
| <span data-ttu-id="80490-2115">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-2115">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2117">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-2117">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2119">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-2119">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2121">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-2121">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-2122">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-2122">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-2123">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-2123">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2125">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-2125">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2127">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-2127">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2129">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-2129">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2131">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-2131">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2133">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-2133">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2135">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-2135">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-2136">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-2136">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-2137">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-2137">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2139">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-2139">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-2140">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-2140">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2142">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-2142">Mipmap Auto- Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2144">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-2144">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2146">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-2146">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2148">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-2148">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-2149">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-2149">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-2150">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-2150">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-2151">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-2151">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-2152">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-2152">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2154">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2154">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2156">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2156">UAV Typed Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2158">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2158">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-2159">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-2159">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-2160">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-2160">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-2161">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2161">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-2162">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-2162">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-2163">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-2163">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-2164">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-2164">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2166">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-2166">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2168">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-2168">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2170">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-2170">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-2172">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-2172">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2174">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-2174">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2176">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-2176">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2178">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-2178">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2180">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2180">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-2181">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2181">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-2183">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2183">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2185">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-2185">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2187">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-2187">BackBuffer Castable Even Fully Typed</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2189">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-2189">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfcssup-29"></a><span data-ttu-id="80490-2191"><sup>FCS</sup> DXGI_FORMAT_R8G8B8A8_UNORM_SRGB (29)</span><span class="sxs-lookup"><span data-stu-id="80490-2191">DXGI_FORMAT_R8G8B8A8_UNORM_SRGB<sup>FCS</sup> (29)</span></span>
| <span data-ttu-id="80490-2192">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-2192">Target</span></span> | <span data-ttu-id="80490-2193">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-2193">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-2194">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-2194">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-2195">32</span><span class="sxs-lookup"><span data-stu-id="80490-2195">32</span></span> |
| <span data-ttu-id="80490-2196">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-2196">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2198">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-2198">Buffer</span></span> | \- |
| <span data-ttu-id="80490-2199">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-2199">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-2200">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-2200">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-2201">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-2201">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-2202">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-2202">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2204">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-2204">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2206">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-2206">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2208">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-2208">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2210">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-2210">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2212">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-2212">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2214">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-2214">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-2215">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-2215">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-2216">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-2216">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2218">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-2218">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-2219">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-2219">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2221">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-2221">Mipmap Auto- Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2223">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-2223">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2225">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-2225">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2227">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-2227">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-2228">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-2228">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-2229">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-2229">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-2230">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-2230">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-2231">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-2231">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-2232">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2232">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-2233">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2233">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-2234">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2234">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-2235">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-2235">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-2236">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-2236">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-2237">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2237">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-2238">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-2238">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-2239">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-2239">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-2240">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-2240">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2242">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-2242">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2244">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-2244">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2246">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-2246">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-2248">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-2248">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2250">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-2250">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2252">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-2252">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2254">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-2254">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2256">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2256">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-2257">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2257">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-2259">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2259">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2261">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-2261">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2263">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-2263">BackBuffer Castable Even Fully Typed</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2265">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-2265">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_uintsupfcssup-30"></a><span data-ttu-id="80490-2267"><sup>FCS</sup> DXGI_FORMAT_R8G8B8A8_UINT (30)</span><span class="sxs-lookup"><span data-stu-id="80490-2267">DXGI_FORMAT_R8G8B8A8_UINT<sup>FCS</sup> (30)</span></span>
| <span data-ttu-id="80490-2268">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-2268">Target</span></span> | <span data-ttu-id="80490-2269">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-2269">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-2270">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-2270">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-2271">32</span><span class="sxs-lookup"><span data-stu-id="80490-2271">32</span></span> |
| <span data-ttu-id="80490-2272">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-2272">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2274">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-2274">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2276">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-2276">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2278">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-2278">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-2279">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-2279">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-2280">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-2280">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2282">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-2282">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2284">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-2284">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2286">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-2286">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2288">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-2288">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2290">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-2290">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-2291">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-2291">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-2292">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-2292">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-2293">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-2293">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-2294">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-2294">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-2295">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-2295">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2297">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-2297">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-2298">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-2298">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2300">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-2300">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-2301">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-2301">Output Merger Logic Op</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2303">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-2303">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-2304">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-2304">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-2305">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-2305">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-2306">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-2306">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2308">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2308">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2310">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2310">UAV Typed Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2312">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2312">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-2313">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-2313">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-2314">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-2314">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-2315">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2315">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-2316">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-2316">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-2317">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-2317">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-2318">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-2318">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2320">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-2320">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2322">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-2322">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2324">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-2324">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-2326">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-2326">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-2327">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-2327">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2329">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-2329">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-2330">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-2330">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2332">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2332">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-2333">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2333">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-2334">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2334">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-2335">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-2335">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2337">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-2337">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-2338">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-2338">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_snormsupfcssup-31"></a><span data-ttu-id="80490-2340">DXGI_FORMAT_R8G8B8A8_SNORM<sup>FCS</sup> (31)</span><span class="sxs-lookup"><span data-stu-id="80490-2340">DXGI_FORMAT_R8G8B8A8_SNORM<sup>FCS</sup> (31)</span></span>
| <span data-ttu-id="80490-2341">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-2341">Target</span></span> | <span data-ttu-id="80490-2342">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-2342">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-2343">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-2343">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-2344">32</span><span class="sxs-lookup"><span data-stu-id="80490-2344">32</span></span> |
| <span data-ttu-id="80490-2345">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-2345">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2347">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-2347">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2349">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-2349">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2351">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-2351">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-2352">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-2352">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-2353">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-2353">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2355">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-2355">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2357">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-2357">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2359">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-2359">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2361">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-2361">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2363">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-2363">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2365">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-2365">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-2366">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-2366">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-2367">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-2367">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2369">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-2369">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-2370">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-2370">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2372">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-2372">Mipmap Auto- Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2374">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-2374">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2376">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-2376">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2378">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-2378">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-2379">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-2379">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-2380">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-2380">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-2381">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-2381">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-2382">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-2382">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2384">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2384">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2386">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2386">UAV Typed Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-2388">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2388">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-2389">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-2389">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-2390">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-2390">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-2391">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2391">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-2392">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-2392">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-2393">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-2393">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-2394">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-2394">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2396">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-2396">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2398">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-2398">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2400">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-2400">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-2402">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-2402">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2404">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-2404">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2406">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-2406">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-2407">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-2407">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2409">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2409">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-2410">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2410">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-2411">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2411">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-2412">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-2412">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2414">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-2414">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-2415">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-2415">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_sintsupfcssup-32"></a><span data-ttu-id="80490-2417">DXGI_FORMAT_R8G8B8A8_SINT<sup>FCS</sup> (32)</span><span class="sxs-lookup"><span data-stu-id="80490-2417">DXGI_FORMAT_R8G8B8A8_SINT<sup>FCS</sup> (32)</span></span>
| <span data-ttu-id="80490-2418">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-2418">Target</span></span> | <span data-ttu-id="80490-2419">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-2419">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-2420">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-2420">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-2421">32</span><span class="sxs-lookup"><span data-stu-id="80490-2421">32</span></span> |
| <span data-ttu-id="80490-2422">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-2422">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2424">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-2424">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2426">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-2426">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2428">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-2428">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-2429">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-2429">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-2430">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-2430">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2432">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-2432">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2434">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-2434">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2436">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-2436">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2438">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-2438">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2440">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-2440">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-2441">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-2441">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-2442">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-2442">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-2443">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-2443">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-2444">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-2444">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-2445">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-2445">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2447">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-2447">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-2448">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-2448">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2450">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-2450">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-2451">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-2451">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-2452">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-2452">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-2453">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-2453">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-2454">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-2454">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-2455">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-2455">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2457">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2457">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2459">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2459">UAV Typed Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2461">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2461">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-2462">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-2462">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-2463">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-2463">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-2464">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2464">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-2465">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-2465">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-2466">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-2466">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-2467">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-2467">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2469">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-2469">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2471">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-2471">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2473">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-2473">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-2475">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-2475">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-2476">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-2476">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2478">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-2478">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-2479">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-2479">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2481">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2481">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-2482">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2482">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-2483">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2483">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-2484">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-2484">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2486">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-2486">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-2487">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-2487">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="80490-2489"><sup>Computadores</sup> DXGI_FORMAT_R16G16_TYPELESS (33)</span><span class="sxs-lookup"><span data-stu-id="80490-2489">DXGI_FORMAT_R16G16_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="80490-2490">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-2490">Target</span></span> | <span data-ttu-id="80490-2491">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-2491">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-2492">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-2492">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-2493">32</span><span class="sxs-lookup"><span data-stu-id="80490-2493">32</span></span> |
| <span data-ttu-id="80490-2494">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-2494">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2496">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-2496">Buffer</span></span> | \- |
| <span data-ttu-id="80490-2497">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-2497">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-2498">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-2498">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-2499">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-2499">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-2500">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-2500">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2502">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-2502">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2504">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-2504">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2506">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-2506">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2508">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-2508">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-2509">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-2509">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-2510">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-2510">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-2511">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-2511">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-2512">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-2512">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-2513">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-2513">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-2514">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-2514">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2516">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-2516">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-2517">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-2517">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-2518">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-2518">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-2519">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-2519">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-2520">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-2520">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-2521">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-2521">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-2522">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-2522">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-2523">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-2523">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-2524">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2524">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-2525">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2525">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-2526">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2526">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-2527">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-2527">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-2528">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-2528">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-2529">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2529">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-2530">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-2530">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-2531">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-2531">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-2532">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-2532">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2534">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-2534">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-2535">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-2535">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-2536">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-2536">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-2537">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-2537">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-2538">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-2538">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-2539">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-2539">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-2540">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-2540">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2542">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2542">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-2543">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2543">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-2544">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2544">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-2545">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-2545">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-2546">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-2546">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-2547">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-2547">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_floatsupfcssup-34"></a><span data-ttu-id="80490-2549">DXGI_FORMAT_R16G16_FLOAT<sup>FCS</sup> (34)</span><span class="sxs-lookup"><span data-stu-id="80490-2549">DXGI_FORMAT_R16G16_FLOAT<sup>FCS</sup> (34)</span></span>
| <span data-ttu-id="80490-2550">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-2550">Target</span></span> | <span data-ttu-id="80490-2551">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-2551">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-2552">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-2552">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-2553">32</span><span class="sxs-lookup"><span data-stu-id="80490-2553">32</span></span> |
| <span data-ttu-id="80490-2554">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-2554">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2556">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-2556">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2558">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-2558">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2560">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-2560">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-2561">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-2561">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-2562">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-2562">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2564">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-2564">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2566">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-2566">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2568">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-2568">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2570">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-2570">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2572">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-2572">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2574">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-2574">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-2575">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-2575">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-2576">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-2576">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2578">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-2578">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-2579">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-2579">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2581">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-2581">Mipmap Auto- Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2583">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-2583">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2585">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-2585">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2587">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-2587">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-2588">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-2588">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-2589">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-2589">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-2590">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-2590">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-2591">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-2591">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2593">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2593">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2595">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2595">UAV Typed Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-2597">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2597">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-2598">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-2598">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-2599">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-2599">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-2600">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2600">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-2601">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-2601">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-2602">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-2602">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-2603">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-2603">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2605">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-2605">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2607">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-2607">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2609">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-2609">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-2611">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-2611">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2613">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-2613">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2615">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-2615">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-2616">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-2616">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2618">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2618">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-2619">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2619">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-2620">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2620">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-2621">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-2621">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-2622">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-2622">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-2623">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-2623">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_unormsupfcssup-35"></a><span data-ttu-id="80490-2625">DXGI_FORMAT_R16G16_UNORM<sup>FCS</sup> (35)</span><span class="sxs-lookup"><span data-stu-id="80490-2625">DXGI_FORMAT_R16G16_UNORM<sup>FCS</sup> (35)</span></span>
| <span data-ttu-id="80490-2626">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-2626">Target</span></span> | <span data-ttu-id="80490-2627">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-2627">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-2628">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-2628">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-2629">32</span><span class="sxs-lookup"><span data-stu-id="80490-2629">32</span></span> |
| <span data-ttu-id="80490-2630">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-2630">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2632">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-2632">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2634">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-2634">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2636">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-2636">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-2637">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-2637">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-2638">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-2638">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2640">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-2640">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2642">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-2642">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2644">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-2644">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2646">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-2646">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2648">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-2648">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2650">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-2650">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-2651">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-2651">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-2652">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-2652">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2654">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-2654">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-2655">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-2655">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2657">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-2657">Mipmap Auto- Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2659">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-2659">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2661">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-2661">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2663">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-2663">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-2664">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-2664">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-2665">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-2665">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-2666">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-2666">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-2667">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-2667">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2669">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2669">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2671">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2671">UAV Typed Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-2673">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2673">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-2674">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-2674">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-2675">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-2675">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-2676">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2676">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-2677">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-2677">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-2678">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-2678">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-2679">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-2679">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2681">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-2681">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2683">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-2683">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2685">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-2685">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-2687">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-2687">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2689">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-2689">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2691">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-2691">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-2692">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-2692">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2694">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2694">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-2695">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2695">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-2696">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2696">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-2697">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-2697">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-2698">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-2698">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-2699">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-2699">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_uintsupfcssup-36"></a><span data-ttu-id="80490-2701">DXGI_FORMAT_R16G16_UINT<sup>FCS</sup> (36)</span><span class="sxs-lookup"><span data-stu-id="80490-2701">DXGI_FORMAT_R16G16_UINT<sup>FCS</sup> (36)</span></span>
| <span data-ttu-id="80490-2702">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-2702">Target</span></span> | <span data-ttu-id="80490-2703">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-2703">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-2704">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-2704">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-2705">32</span><span class="sxs-lookup"><span data-stu-id="80490-2705">32</span></span> |
| <span data-ttu-id="80490-2706">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-2706">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2708">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-2708">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2710">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-2710">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2712">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-2712">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-2713">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-2713">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-2714">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-2714">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2716">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-2716">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2718">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-2718">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2720">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-2720">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2722">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-2722">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2724">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-2724">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-2725">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-2725">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-2726">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-2726">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-2727">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-2727">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-2728">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-2728">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-2729">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-2729">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2731">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-2731">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-2732">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-2732">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2734">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-2734">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-2735">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-2735">Output Merger Logic Op</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2737">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-2737">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-2738">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-2738">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-2739">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-2739">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-2740">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-2740">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2742">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2742">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2744">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2744">UAV Typed Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-2746">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2746">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-2747">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-2747">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-2748">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-2748">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-2749">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2749">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-2750">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-2750">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-2751">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-2751">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-2752">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-2752">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2754">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-2754">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2756">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-2756">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2758">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-2758">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-2760">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-2760">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-2761">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-2761">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2763">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-2763">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-2764">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-2764">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2766">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2766">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-2767">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2767">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-2768">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2768">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-2769">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-2769">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-2770">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-2770">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-2771">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-2771">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_snormsupfcssup-37"></a><span data-ttu-id="80490-2773">DXGI_FORMAT_R16G16_SNORM<sup>FCS</sup> (37)</span><span class="sxs-lookup"><span data-stu-id="80490-2773">DXGI_FORMAT_R16G16_SNORM<sup>FCS</sup> (37)</span></span>
| <span data-ttu-id="80490-2774">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-2774">Target</span></span> | <span data-ttu-id="80490-2775">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-2775">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-2776">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-2776">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-2777">32</span><span class="sxs-lookup"><span data-stu-id="80490-2777">32</span></span> |
| <span data-ttu-id="80490-2778">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-2778">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2780">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-2780">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2782">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-2782">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2784">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-2784">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-2785">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-2785">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-2786">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-2786">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2788">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-2788">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2790">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-2790">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2792">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-2792">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2794">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-2794">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2796">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-2796">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2798">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-2798">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-2799">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-2799">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-2800">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-2800">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2802">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-2802">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-2803">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-2803">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2805">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-2805">Mipmap Auto- Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2807">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-2807">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2809">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-2809">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2811">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-2811">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-2812">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-2812">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-2813">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-2813">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-2814">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-2814">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-2815">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-2815">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2817">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2817">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2819">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2819">UAV Typed Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-2821">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2821">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-2822">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-2822">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-2823">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-2823">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-2824">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2824">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-2825">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-2825">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-2826">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-2826">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-2827">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-2827">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2829">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-2829">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2831">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-2831">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2833">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-2833">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-2835">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-2835">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2837">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-2837">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2839">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-2839">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-2840">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-2840">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2842">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2842">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-2843">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2843">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-2844">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2844">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-2845">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-2845">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-2846">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-2846">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-2847">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-2847">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_sintsupfcssup-38"></a><span data-ttu-id="80490-2849">DXGI_FORMAT_R16G16_SINT<sup>FCS</sup> (38)</span><span class="sxs-lookup"><span data-stu-id="80490-2849">DXGI_FORMAT_R16G16_SINT<sup>FCS</sup> (38)</span></span>
| <span data-ttu-id="80490-2850">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-2850">Target</span></span> | <span data-ttu-id="80490-2851">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-2851">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-2852">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-2852">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-2853">32</span><span class="sxs-lookup"><span data-stu-id="80490-2853">32</span></span> |
| <span data-ttu-id="80490-2854">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-2854">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2856">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-2856">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2858">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-2858">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2860">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-2860">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-2861">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-2861">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-2862">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-2862">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2864">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-2864">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2866">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-2866">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2868">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-2868">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2870">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-2870">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2872">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-2872">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-2873">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-2873">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-2874">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-2874">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-2875">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-2875">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-2876">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-2876">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-2877">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-2877">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2879">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-2879">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-2880">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-2880">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2882">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-2882">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-2883">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-2883">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-2884">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-2884">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-2885">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-2885">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-2886">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-2886">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-2887">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-2887">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2889">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2889">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2891">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2891">UAV Typed Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-2893">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2893">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-2894">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-2894">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-2895">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-2895">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-2896">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2896">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-2897">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-2897">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-2898">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-2898">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-2899">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-2899">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2901">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-2901">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2903">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-2903">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2905">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-2905">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-2907">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-2907">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-2908">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-2908">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2910">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-2910">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-2911">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-2911">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2913">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2913">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-2914">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2914">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-2915">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2915">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-2916">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-2916">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-2917">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-2917">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-2918">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-2918">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="80490-2920"><sup>Computadores</sup> DXGI_FORMAT_R32_TYPELESS (39)</span><span class="sxs-lookup"><span data-stu-id="80490-2920">DXGI_FORMAT_R32_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="80490-2921">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-2921">Target</span></span> | <span data-ttu-id="80490-2922">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-2922">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-2923">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-2923">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-2924">32</span><span class="sxs-lookup"><span data-stu-id="80490-2924">32</span></span> |
| <span data-ttu-id="80490-2925">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-2925">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2927">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-2927">Buffer</span></span> | \- |
| <span data-ttu-id="80490-2928">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-2928">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-2929">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-2929">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-2930">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-2930">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-2931">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-2931">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2933">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-2933">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2935">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-2935">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2937">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-2937">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2939">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-2939">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-2940">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-2940">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-2941">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-2941">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-2942">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-2942">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-2943">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-2943">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-2944">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-2944">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-2945">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-2945">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2947">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-2947">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-2948">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-2948">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-2949">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-2949">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-2950">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-2950">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-2951">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-2951">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-2952">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-2952">Raw UAV and SRV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2954">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-2954">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-2955">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-2955">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-2956">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2956">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-2957">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2957">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-2958">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2958">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-2959">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-2959">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-2960">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-2960">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-2961">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-2961">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-2962">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-2962">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-2963">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-2963">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-2964">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-2964">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2966">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-2966">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-2967">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-2967">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-2968">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-2968">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-2969">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-2969">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-2970">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-2970">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-2971">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-2971">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-2972">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-2972">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2974">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2974">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-2975">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2975">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-2976">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-2976">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-2977">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-2977">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2979">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-2979">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-2980">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-2980">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_d32_floatsupfcssup-40"></a><span data-ttu-id="80490-2982">DXGI_FORMAT_D32_FLOAT<sup>FCS</sup> (40)</span><span class="sxs-lookup"><span data-stu-id="80490-2982">DXGI_FORMAT_D32_FLOAT<sup>FCS</sup> (40)</span></span>
| <span data-ttu-id="80490-2983">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-2983">Target</span></span> | <span data-ttu-id="80490-2984">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-2984">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-2985">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-2985">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-2986">32</span><span class="sxs-lookup"><span data-stu-id="80490-2986">32</span></span> |
| <span data-ttu-id="80490-2987">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-2987">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2989">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-2989">Buffer</span></span> | \- |
| <span data-ttu-id="80490-2990">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-2990">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-2991">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-2991">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-2992">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-2992">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-2993">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-2993">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2995">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-2995">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-2997">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-2997">Texture3D</span></span> | \- |
| <span data-ttu-id="80490-2998">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-2998">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3000">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-3000">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-3001">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-3001">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-3002">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-3002">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-3003">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-3003">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-3004">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-3004">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-3005">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-3005">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-3006">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-3006">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3008">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-3008">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-3009">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-3009">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-3010">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-3010">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-3011">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-3011">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-3012">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-3012">Depth/Stencil Target</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3014">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-3014">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-3015">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-3015">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-3016">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-3016">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-3017">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3017">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-3018">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3018">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-3019">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3019">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-3020">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-3020">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-3021">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-3021">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-3022">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3022">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-3023">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-3023">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-3024">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-3024">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-3025">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-3025">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3027">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-3027">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3029">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-3029">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3031">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-3031">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-3033">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-3033">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-3034">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-3034">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-3035">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-3035">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-3036">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-3036">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3038">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3038">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-3039">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3039">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-3040">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3040">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-3041">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-3041">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3043">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-3043">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-3044">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-3044">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r32_floatsupfcssup-41"></a><span data-ttu-id="80490-3046">DXGI_FORMAT_R32_FLOAT<sup>FCS</sup> (41)</span><span class="sxs-lookup"><span data-stu-id="80490-3046">DXGI_FORMAT_R32_FLOAT<sup>FCS</sup> (41)</span></span>
| <span data-ttu-id="80490-3047">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-3047">Target</span></span> | <span data-ttu-id="80490-3048">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-3048">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-3049">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-3049">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-3050">32</span><span class="sxs-lookup"><span data-stu-id="80490-3050">32</span></span> |
| <span data-ttu-id="80490-3051">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-3051">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3053">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-3053">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3055">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-3055">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3057">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-3057">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-3058">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-3058">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3060">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-3060">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3062">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-3062">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3064">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-3064">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3066">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-3066">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3068">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-3068">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3070">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-3070">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3072">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-3072">Shader sample_c (comparison filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3074">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-3074">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-3075">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-3075">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3077">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-3077">Shader gather4_c</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3079">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-3079">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3081">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-3081">Mipmap Auto- Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3083">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-3083">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3085">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-3085">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3087">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-3087">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-3088">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-3088">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-3089">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-3089">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-3090">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-3090">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-3091">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-3091">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3093">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3093">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3095">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3095">UAV Typed Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3097">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3097">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-3098">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-3098">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-3099">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-3099">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-3100">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3100">UAV Atomic Exchange</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3102">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-3102">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-3103">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-3103">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-3104">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-3104">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3106">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-3106">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3108">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-3108">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3110">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-3110">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-3112">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-3112">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3114">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-3114">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3116">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-3116">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-3117">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-3117">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3119">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3119">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-3120">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3120">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-3121">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3121">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-3122">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-3122">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3124">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-3124">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-3125">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-3125">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r32_uintsupfcssup-42"></a><span data-ttu-id="80490-3127">DXGI_FORMAT_R32_UINT<sup>FCS</sup> (42)</span><span class="sxs-lookup"><span data-stu-id="80490-3127">DXGI_FORMAT_R32_UINT<sup>FCS</sup> (42)</span></span>
| <span data-ttu-id="80490-3128">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-3128">Target</span></span> | <span data-ttu-id="80490-3129">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-3129">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-3130">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-3130">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-3131">32</span><span class="sxs-lookup"><span data-stu-id="80490-3131">32</span></span> |
| <span data-ttu-id="80490-3132">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-3132">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3134">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-3134">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3136">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-3136">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3138">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-3138">Input Assembler Index Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3140">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-3140">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3142">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-3142">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3144">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-3144">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3146">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-3146">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3148">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-3148">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3150">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-3150">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3152">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-3152">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-3153">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-3153">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-3154">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-3154">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-3155">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-3155">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-3156">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-3156">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-3157">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-3157">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3159">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-3159">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-3160">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-3160">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3162">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-3162">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-3163">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-3163">Output Merger Logic Op</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3165">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-3165">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-3166">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-3166">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-3167">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-3167">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-3168">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-3168">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3170">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3170">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3172">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3172">UAV Typed Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3174">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3174">UAV Atomic Add</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3176">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-3176">UAV Atomic Bitwise Ops</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3178">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-3178">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3180">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3180">UAV Atomic Exchange</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3182">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-3182">UAV Atomic Signed Min/Max</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3184">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-3184">UAV Atomic Unsigned Min/Max</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3186">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-3186">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3188">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-3188">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3190">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-3190">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3192">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-3192">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-3194">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-3194">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-3195">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-3195">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3197">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-3197">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-3198">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-3198">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3200">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3200">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-3201">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3201">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-3202">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3202">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-3203">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-3203">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3205">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-3205">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-3206">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-3206">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r32_sintsupfcssup-43"></a><span data-ttu-id="80490-3208">DXGI_FORMAT_R32_SINT<sup>FCS</sup> (43)</span><span class="sxs-lookup"><span data-stu-id="80490-3208">DXGI_FORMAT_R32_SINT<sup>FCS</sup> (43)</span></span>
| <span data-ttu-id="80490-3209">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-3209">Target</span></span> | <span data-ttu-id="80490-3210">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-3210">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-3211">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-3211">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-3212">32</span><span class="sxs-lookup"><span data-stu-id="80490-3212">32</span></span> |
| <span data-ttu-id="80490-3213">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-3213">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3215">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-3215">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3217">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-3217">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3219">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-3219">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-3220">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-3220">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3222">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-3222">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3224">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-3224">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3226">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-3226">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3228">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-3228">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3230">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-3230">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3232">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-3232">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-3233">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-3233">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-3234">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-3234">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-3235">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-3235">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-3236">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-3236">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-3237">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-3237">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3239">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-3239">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-3240">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-3240">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3242">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-3242">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-3243">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-3243">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-3244">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-3244">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-3245">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-3245">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-3246">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-3246">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-3247">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-3247">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3249">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3249">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3251">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3251">UAV Typed Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3253">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3253">UAV Atomic Add</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3255">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-3255">UAV Atomic Bitwise Ops</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3257">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-3257">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3259">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3259">UAV Atomic Exchange</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3261">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-3261">UAV Atomic Signed Min/Max</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3263">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-3263">UAV Atomic Unsigned Min/Max</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3265">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-3265">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3267">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-3267">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3269">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-3269">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3271">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-3271">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-3273">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-3273">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-3274">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-3274">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3276">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-3276">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-3277">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-3277">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3279">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3279">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-3280">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3280">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-3281">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3281">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-3282">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-3282">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3284">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-3284">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-3285">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-3285">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r24g8_typelesssupvsup-44"></a><span data-ttu-id="80490-3287">DXGI_FORMAT_R24G8_TYPELESS<sup>V</sup> (44)</span><span class="sxs-lookup"><span data-stu-id="80490-3287">DXGI_FORMAT_R24G8_TYPELESS<sup>V</sup> (44)</span></span>
| <span data-ttu-id="80490-3288">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-3288">Target</span></span> | <span data-ttu-id="80490-3289">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-3289">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-3290">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-3290">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-3291">32</span><span class="sxs-lookup"><span data-stu-id="80490-3291">32</span></span> |
| <span data-ttu-id="80490-3292">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-3292">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3294">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-3294">Buffer</span></span> | \- |
| <span data-ttu-id="80490-3295">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-3295">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-3296">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-3296">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-3297">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-3297">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-3298">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-3298">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3300">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-3300">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3302">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-3302">Texture3D</span></span> | \- |
| <span data-ttu-id="80490-3303">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-3303">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3305">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-3305">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-3306">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-3306">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-3307">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-3307">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-3308">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-3308">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-3309">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-3309">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-3310">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-3310">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-3311">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-3311">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3313">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-3313">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-3314">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-3314">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-3315">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-3315">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-3316">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-3316">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-3317">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-3317">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-3318">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-3318">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-3319">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-3319">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-3320">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-3320">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-3321">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3321">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-3322">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3322">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-3323">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3323">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-3324">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-3324">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-3325">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-3325">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-3326">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3326">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-3327">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-3327">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-3328">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-3328">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-3329">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-3329">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3331">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-3331">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-3332">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-3332">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-3333">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-3333">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-3334">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-3334">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-3335">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-3335">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-3336">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-3336">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-3337">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-3337">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3339">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3339">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-3340">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3340">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-3341">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3341">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-3342">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-3342">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-3343">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-3343">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-3344">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-3344">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupvsup-45"></a><span data-ttu-id="80490-3345">DXGI_FORMAT_D24_UNORM_S8_UINT<sup>V</sup> (45)</span><span class="sxs-lookup"><span data-stu-id="80490-3345">DXGI_FORMAT_D24_UNORM_S8_UINT<sup>V</sup> (45)</span></span>
| <span data-ttu-id="80490-3346">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-3346">Target</span></span> | <span data-ttu-id="80490-3347">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-3347">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-3348">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-3348">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-3349">32</span><span class="sxs-lookup"><span data-stu-id="80490-3349">32</span></span> |
| <span data-ttu-id="80490-3350">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-3350">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3352">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-3352">Buffer</span></span> | \- |
| <span data-ttu-id="80490-3353">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-3353">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-3354">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-3354">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-3355">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-3355">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-3356">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-3356">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3358">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-3358">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3360">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-3360">Texture3D</span></span> | \- |
| <span data-ttu-id="80490-3361">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-3361">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3363">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-3363">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-3364">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-3364">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-3365">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-3365">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-3366">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-3366">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-3367">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-3367">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-3368">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-3368">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-3369">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-3369">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3371">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-3371">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-3372">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-3372">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-3373">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-3373">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-3374">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-3374">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-3375">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-3375">Depth/Stencil Target</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3377">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-3377">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-3378">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-3378">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-3379">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-3379">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-3380">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3380">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-3381">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3381">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-3382">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3382">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-3383">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-3383">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-3384">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-3384">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-3385">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3385">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-3386">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-3386">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-3387">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-3387">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-3388">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-3388">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3390">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-3390">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3392">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-3392">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3394">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-3394">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-3396">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-3396">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-3397">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-3397">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-3398">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-3398">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-3399">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-3399">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3401">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3401">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-3402">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3402">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-3403">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3403">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-3404">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-3404">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-3405">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-3405">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-3406">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-3406">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupvsup-46"></a><span data-ttu-id="80490-3407">DXGI_FORMAT_R24_UNORM_X8_TYPELESS<sup>V</sup> (46)</span><span class="sxs-lookup"><span data-stu-id="80490-3407">DXGI_FORMAT_R24_UNORM_X8_TYPELESS<sup>V</sup> (46)</span></span>
| <span data-ttu-id="80490-3408">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-3408">Target</span></span> | <span data-ttu-id="80490-3409">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-3409">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-3410">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-3410">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-3411">32</span><span class="sxs-lookup"><span data-stu-id="80490-3411">32</span></span> |
| <span data-ttu-id="80490-3412">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-3412">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3414">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-3414">Buffer</span></span> | \- |
| <span data-ttu-id="80490-3415">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-3415">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-3416">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-3416">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-3417">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-3417">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-3418">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-3418">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3420">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-3420">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3422">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-3422">Texture3D</span></span> | \- |
| <span data-ttu-id="80490-3423">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-3423">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3425">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-3425">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3427">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-3427">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3429">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-3429">Shader sample_c (comparison filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3431">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-3431">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-3432">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-3432">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3434">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-3434">Shader gather4_c</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3436">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-3436">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3438">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-3438">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-3439">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-3439">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-3440">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-3440">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-3441">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-3441">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-3442">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-3442">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-3443">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-3443">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-3444">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-3444">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-3445">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-3445">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-3446">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3446">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-3447">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3447">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-3448">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3448">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-3449">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-3449">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-3450">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-3450">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-3451">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3451">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-3452">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-3452">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-3453">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-3453">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-3454">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-3454">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3456">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-3456">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-3457">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-3457">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-3458">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-3458">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-3459">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-3459">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-3460">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-3460">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3462">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-3462">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-3463">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-3463">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3465">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3465">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-3466">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3466">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-3467">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3467">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-3468">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-3468">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-3469">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-3469">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-3470">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-3470">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupvsup-47"></a><span data-ttu-id="80490-3471">DXGI_FORMAT_X24_TYPELESS_G8_UINT<sup>V</sup> (47)</span><span class="sxs-lookup"><span data-stu-id="80490-3471">DXGI_FORMAT_X24_TYPELESS_G8_UINT<sup>V</sup> (47)</span></span>
| <span data-ttu-id="80490-3472">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-3472">Target</span></span> | <span data-ttu-id="80490-3473">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-3473">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-3474">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-3474">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-3475">32</span><span class="sxs-lookup"><span data-stu-id="80490-3475">32</span></span> |
| <span data-ttu-id="80490-3476">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-3476">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3478">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-3478">Buffer</span></span> | \- |
| <span data-ttu-id="80490-3479">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-3479">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-3480">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-3480">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-3481">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-3481">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-3482">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-3482">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3484">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-3484">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3486">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-3486">Texture3D</span></span> | \- |
| <span data-ttu-id="80490-3487">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-3487">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3489">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-3489">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3491">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-3491">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-3492">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-3492">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-3493">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-3493">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-3494">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-3494">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-3495">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-3495">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-3496">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-3496">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3498">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-3498">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-3499">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-3499">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-3500">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-3500">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-3501">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-3501">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-3502">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-3502">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-3503">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-3503">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-3504">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-3504">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-3505">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-3505">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-3506">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3506">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-3507">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3507">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-3508">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3508">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-3509">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-3509">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-3510">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-3510">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-3511">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3511">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-3512">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-3512">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-3513">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-3513">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-3514">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-3514">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3516">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-3516">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-3517">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-3517">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-3518">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-3518">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-3519">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-3519">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-3520">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-3520">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3522">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-3522">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-3523">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-3523">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3525">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3525">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-3526">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3526">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-3527">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3527">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-3528">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-3528">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-3529">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-3529">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-3530">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-3530">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="80490-3531"><sup>Computadores</sup> DXGI_FORMAT_R8G8_TYPELESS (48)</span><span class="sxs-lookup"><span data-stu-id="80490-3531">DXGI_FORMAT_R8G8_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="80490-3532">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-3532">Target</span></span> | <span data-ttu-id="80490-3533">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-3533">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-3534">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-3534">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-3535">16</span><span class="sxs-lookup"><span data-stu-id="80490-3535">16</span></span> |
| <span data-ttu-id="80490-3536">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-3536">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3538">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-3538">Buffer</span></span> | \- |
| <span data-ttu-id="80490-3539">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-3539">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-3540">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-3540">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-3541">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-3541">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-3542">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-3542">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3544">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-3544">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3546">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-3546">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3548">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-3548">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3550">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-3550">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-3551">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-3551">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-3552">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-3552">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-3553">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-3553">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-3554">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-3554">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-3555">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-3555">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-3556">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-3556">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3558">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-3558">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-3559">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-3559">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-3560">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-3560">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-3561">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-3561">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-3562">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-3562">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-3563">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-3563">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-3564">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-3564">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-3565">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-3565">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-3566">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3566">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-3567">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3567">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-3568">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3568">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-3569">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-3569">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-3570">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-3570">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-3571">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3571">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-3572">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-3572">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-3573">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-3573">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-3574">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-3574">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3576">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-3576">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-3577">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-3577">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-3578">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-3578">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-3579">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-3579">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-3580">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-3580">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-3581">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-3581">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-3582">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-3582">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3584">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3584">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-3585">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3585">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-3586">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3586">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-3587">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-3587">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-3588">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-3588">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-3589">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-3589">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_unormsupfcssup-49"></a><span data-ttu-id="80490-3591">DXGI_FORMAT_R8G8_UNORM<sup>FCS</sup> (49)</span><span class="sxs-lookup"><span data-stu-id="80490-3591">DXGI_FORMAT_R8G8_UNORM<sup>FCS</sup> (49)</span></span>
| <span data-ttu-id="80490-3592">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-3592">Target</span></span> | <span data-ttu-id="80490-3593">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-3593">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-3594">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-3594">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-3595">16</span><span class="sxs-lookup"><span data-stu-id="80490-3595">16</span></span> |
| <span data-ttu-id="80490-3596">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-3596">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3598">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-3598">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3600">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-3600">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3602">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-3602">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-3603">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-3603">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-3604">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-3604">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3606">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-3606">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3608">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-3608">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3610">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-3610">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3612">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-3612">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3614">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-3614">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3616">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-3616">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-3617">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-3617">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-3618">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-3618">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3620">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-3620">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-3621">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-3621">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3623">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-3623">Mipmap Auto- Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3625">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-3625">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3627">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-3627">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3629">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-3629">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-3630">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-3630">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-3631">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-3631">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-3632">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-3632">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-3633">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-3633">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3635">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3635">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3637">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3637">UAV Typed Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-3639">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3639">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-3640">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-3640">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-3641">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-3641">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-3642">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3642">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-3643">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-3643">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-3644">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-3644">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-3645">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-3645">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3647">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-3647">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3649">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-3649">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3651">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-3651">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-3653">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-3653">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3655">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-3655">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3657">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-3657">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-3658">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-3658">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3660">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3660">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-3661">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3661">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-3662">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3662">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-3663">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-3663">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3665">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-3665">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-3666">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-3666">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_uintsupfcssup-50"></a><span data-ttu-id="80490-3668">DXGI_FORMAT_R8G8_UINT<sup>FCS</sup> (50)</span><span class="sxs-lookup"><span data-stu-id="80490-3668">DXGI_FORMAT_R8G8_UINT<sup>FCS</sup> (50)</span></span>
| <span data-ttu-id="80490-3669">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-3669">Target</span></span> | <span data-ttu-id="80490-3670">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-3670">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-3671">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-3671">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-3672">16</span><span class="sxs-lookup"><span data-stu-id="80490-3672">16</span></span> |
| <span data-ttu-id="80490-3673">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-3673">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3675">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-3675">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3677">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-3677">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3679">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-3679">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-3680">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-3680">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-3681">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-3681">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3683">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-3683">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3685">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-3685">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3687">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-3687">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3689">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-3689">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3691">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-3691">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-3692">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-3692">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-3693">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-3693">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-3694">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-3694">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-3695">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-3695">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-3696">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-3696">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3698">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-3698">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-3699">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-3699">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3701">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-3701">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-3702">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-3702">Output Merger Logic Op</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3704">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-3704">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-3705">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-3705">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-3706">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-3706">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-3707">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-3707">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3709">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3709">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3711">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3711">UAV Typed Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-3713">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3713">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-3714">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-3714">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-3715">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-3715">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-3716">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3716">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-3717">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-3717">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-3718">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-3718">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-3719">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-3719">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3721">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-3721">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3723">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-3723">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3725">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-3725">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-3727">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-3727">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-3728">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-3728">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3730">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-3730">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-3731">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-3731">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3733">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3733">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-3734">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3734">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-3735">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3735">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-3736">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-3736">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-3737">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-3737">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-3738">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-3738">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_snormsupfcssup-51"></a><span data-ttu-id="80490-3740">DXGI_FORMAT_R8G8_SNORM<sup>FCS</sup> (51)</span><span class="sxs-lookup"><span data-stu-id="80490-3740">DXGI_FORMAT_R8G8_SNORM<sup>FCS</sup> (51)</span></span>
| <span data-ttu-id="80490-3741">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-3741">Target</span></span> | <span data-ttu-id="80490-3742">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-3742">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-3743">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-3743">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-3744">16</span><span class="sxs-lookup"><span data-stu-id="80490-3744">16</span></span> |
| <span data-ttu-id="80490-3745">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-3745">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3747">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-3747">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3749">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-3749">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3751">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-3751">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-3752">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-3752">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-3753">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-3753">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3755">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-3755">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3757">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-3757">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3759">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-3759">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3761">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-3761">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3763">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-3763">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3765">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-3765">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-3766">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-3766">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-3767">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-3767">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3769">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-3769">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-3770">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-3770">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3772">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-3772">Mipmap Auto- Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3774">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-3774">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3776">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-3776">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3778">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-3778">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-3779">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-3779">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-3780">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-3780">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-3781">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-3781">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-3782">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-3782">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3784">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3784">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3786">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3786">UAV Typed Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-3788">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3788">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-3789">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-3789">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-3790">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-3790">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-3791">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3791">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-3792">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-3792">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-3793">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-3793">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-3794">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-3794">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3796">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-3796">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3798">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-3798">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3800">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-3800">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-3802">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-3802">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3804">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-3804">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3806">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-3806">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-3807">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-3807">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3809">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3809">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-3810">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3810">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-3811">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3811">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-3812">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-3812">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-3813">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-3813">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-3814">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-3814">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_sintsupfcssup-52"></a><span data-ttu-id="80490-3816">DXGI_FORMAT_R8G8_SINT<sup>FCS</sup> (52)</span><span class="sxs-lookup"><span data-stu-id="80490-3816">DXGI_FORMAT_R8G8_SINT<sup>FCS</sup> (52)</span></span>
| <span data-ttu-id="80490-3817">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-3817">Target</span></span> | <span data-ttu-id="80490-3818">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-3818">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-3819">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-3819">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-3820">16</span><span class="sxs-lookup"><span data-stu-id="80490-3820">16</span></span> |
| <span data-ttu-id="80490-3821">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-3821">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3823">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-3823">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3825">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-3825">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3827">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-3827">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-3828">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-3828">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-3829">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-3829">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3831">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-3831">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3833">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-3833">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3835">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-3835">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3837">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-3837">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3839">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-3839">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-3840">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-3840">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-3841">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-3841">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-3842">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-3842">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-3843">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-3843">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-3844">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-3844">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3846">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-3846">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-3847">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-3847">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3849">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-3849">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-3850">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-3850">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-3851">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-3851">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-3852">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-3852">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-3853">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-3853">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-3854">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-3854">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3856">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3856">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3858">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3858">UAV Typed Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-3860">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3860">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-3861">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-3861">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-3862">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-3862">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-3863">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3863">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-3864">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-3864">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-3865">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-3865">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-3866">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-3866">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3868">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-3868">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3870">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-3870">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3872">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-3872">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-3874">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-3874">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-3875">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-3875">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3877">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-3877">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-3878">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-3878">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3880">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3880">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-3881">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3881">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-3882">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3882">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-3883">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-3883">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-3884">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-3884">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-3885">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-3885">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="80490-3887"><sup>Computadores</sup> DXGI_FORMAT_R16_TYPELESS (53)</span><span class="sxs-lookup"><span data-stu-id="80490-3887">DXGI_FORMAT_R16_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="80490-3888">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-3888">Target</span></span> | <span data-ttu-id="80490-3889">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-3889">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-3890">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-3890">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-3891">16</span><span class="sxs-lookup"><span data-stu-id="80490-3891">16</span></span> |
| <span data-ttu-id="80490-3892">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-3892">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3894">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-3894">Buffer</span></span> | \- |
| <span data-ttu-id="80490-3895">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-3895">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-3896">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-3896">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-3897">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-3897">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-3898">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-3898">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3900">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-3900">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3902">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-3902">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3904">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-3904">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3906">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-3906">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-3907">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-3907">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-3908">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-3908">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-3909">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-3909">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-3910">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-3910">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-3911">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-3911">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-3912">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-3912">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3914">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-3914">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-3915">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-3915">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-3916">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-3916">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-3917">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-3917">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-3918">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-3918">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-3919">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-3919">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-3920">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-3920">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-3921">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-3921">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-3922">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3922">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-3923">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3923">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-3924">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3924">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-3925">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-3925">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-3926">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-3926">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-3927">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3927">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-3928">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-3928">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-3929">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-3929">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-3930">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-3930">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3932">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-3932">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-3933">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-3933">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-3934">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-3934">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-3935">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-3935">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-3936">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-3936">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-3937">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-3937">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-3938">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-3938">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3940">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3940">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-3941">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3941">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-3942">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-3942">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-3943">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-3943">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3945">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-3945">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-3946">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-3946">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16_floatsupfcssup-54"></a><span data-ttu-id="80490-3948">DXGI_FORMAT_R16_FLOAT<sup>FCS</sup> (54)</span><span class="sxs-lookup"><span data-stu-id="80490-3948">DXGI_FORMAT_R16_FLOAT<sup>FCS</sup> (54)</span></span>
| <span data-ttu-id="80490-3949">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-3949">Target</span></span> | <span data-ttu-id="80490-3950">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-3950">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-3951">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-3951">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-3952">16</span><span class="sxs-lookup"><span data-stu-id="80490-3952">16</span></span> |
| <span data-ttu-id="80490-3953">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-3953">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3955">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-3955">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3957">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-3957">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3959">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-3959">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-3960">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-3960">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-3961">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-3961">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3963">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-3963">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3965">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-3965">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3967">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-3967">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3969">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-3969">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3971">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-3971">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3973">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-3973">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-3974">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-3974">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-3975">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-3975">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3977">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-3977">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-3978">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-3978">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3980">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-3980">Mipmap Auto- Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3982">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-3982">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3984">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-3984">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3986">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-3986">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-3987">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-3987">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-3988">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-3988">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-3989">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-3989">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-3990">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-3990">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3992">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3992">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3994">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3994">UAV Typed Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-3996">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3996">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-3997">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-3997">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-3998">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-3998">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-3999">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-3999">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-4000">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-4000">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-4001">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-4001">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-4002">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-4002">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4004">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-4004">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4006">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-4006">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4008">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-4008">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-4010">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-4010">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4012">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-4012">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4014">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-4014">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-4015">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-4015">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4017">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4017">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-4018">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4018">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-4019">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4019">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-4020">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-4020">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4022">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-4022">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-4023">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-4023">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_d16_unormsupfcssup-55"></a><span data-ttu-id="80490-4025">DXGI_FORMAT_D16_UNORM<sup>FCS</sup> (55)</span><span class="sxs-lookup"><span data-stu-id="80490-4025">DXGI_FORMAT_D16_UNORM<sup>FCS</sup> (55)</span></span>
| <span data-ttu-id="80490-4026">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-4026">Target</span></span> | <span data-ttu-id="80490-4027">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-4027">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-4028">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-4028">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-4029">16</span><span class="sxs-lookup"><span data-stu-id="80490-4029">16</span></span> |
| <span data-ttu-id="80490-4030">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-4030">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4032">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-4032">Buffer</span></span> | \- |
| <span data-ttu-id="80490-4033">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-4033">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-4034">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-4034">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-4035">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-4035">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-4036">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-4036">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4038">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-4038">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4040">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-4040">Texture3D</span></span> | \- |
| <span data-ttu-id="80490-4041">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-4041">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4043">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-4043">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-4044">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-4044">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-4045">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-4045">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-4046">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-4046">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-4047">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-4047">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-4048">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-4048">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-4049">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-4049">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4051">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-4051">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-4052">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-4052">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-4053">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-4053">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-4054">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-4054">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-4055">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-4055">Depth/Stencil Target</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4057">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-4057">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-4058">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-4058">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-4059">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-4059">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-4060">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4060">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-4061">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4061">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-4062">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4062">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-4063">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-4063">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-4064">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-4064">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-4065">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4065">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-4066">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-4066">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-4067">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-4067">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-4068">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-4068">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4070">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-4070">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4072">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-4072">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4074">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-4074">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-4076">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-4076">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-4077">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-4077">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-4078">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-4078">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-4079">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-4079">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4081">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4081">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-4082">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4082">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-4083">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4083">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-4084">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-4084">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4086">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-4086">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-4087">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-4087">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16_unormsupfcssup-56"></a><span data-ttu-id="80490-4089">DXGI_FORMAT_R16_UNORM<sup>FCS</sup> (56)</span><span class="sxs-lookup"><span data-stu-id="80490-4089">DXGI_FORMAT_R16_UNORM<sup>FCS</sup> (56)</span></span>
| <span data-ttu-id="80490-4090">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-4090">Target</span></span> | <span data-ttu-id="80490-4091">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-4091">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-4092">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-4092">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-4093">16</span><span class="sxs-lookup"><span data-stu-id="80490-4093">16</span></span> |
| <span data-ttu-id="80490-4094">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-4094">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4096">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-4096">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4098">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-4098">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4100">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-4100">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-4101">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-4101">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-4102">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-4102">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4104">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-4104">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4106">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-4106">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4108">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-4108">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4110">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-4110">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4112">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-4112">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4114">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-4114">Shader sample_c (comparison filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4116">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-4116">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-4117">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-4117">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4119">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-4119">Shader gather4_c</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4121">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-4121">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4123">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-4123">Mipmap Auto- Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4125">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-4125">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4127">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-4127">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4129">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-4129">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-4130">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-4130">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-4131">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-4131">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-4132">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-4132">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-4133">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-4133">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4135">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4135">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4137">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4137">UAV Typed Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-4139">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4139">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-4140">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-4140">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-4141">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-4141">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-4142">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4142">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-4143">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-4143">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-4144">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-4144">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-4145">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-4145">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4147">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-4147">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4149">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-4149">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4151">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-4151">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-4153">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-4153">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4155">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-4155">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4157">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-4157">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-4158">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-4158">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4160">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4160">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-4161">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4161">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-4162">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4162">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-4163">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-4163">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4165">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-4165">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-4166">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-4166">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16_uintsupfcssup-57"></a><span data-ttu-id="80490-4168">DXGI_FORMAT_R16_UINT<sup>FCS</sup> (57)</span><span class="sxs-lookup"><span data-stu-id="80490-4168">DXGI_FORMAT_R16_UINT<sup>FCS</sup> (57)</span></span>
| <span data-ttu-id="80490-4169">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-4169">Target</span></span> | <span data-ttu-id="80490-4170">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-4170">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-4171">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-4171">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-4172">16</span><span class="sxs-lookup"><span data-stu-id="80490-4172">16</span></span> |
| <span data-ttu-id="80490-4173">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-4173">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4175">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-4175">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4177">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-4177">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4179">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-4179">Input Assembler Index Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4181">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-4181">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-4182">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-4182">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4184">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-4184">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4186">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-4186">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4188">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-4188">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4190">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-4190">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4192">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-4192">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-4193">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-4193">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-4194">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-4194">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-4195">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-4195">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-4196">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-4196">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-4197">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-4197">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4199">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-4199">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-4200">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-4200">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4202">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-4202">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-4203">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-4203">Output Merger Logic Op</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4205">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-4205">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-4206">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-4206">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-4207">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-4207">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-4208">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-4208">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4210">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4210">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4212">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4212">UAV Typed Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4214">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4214">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-4215">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-4215">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-4216">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-4216">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-4217">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4217">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-4218">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-4218">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-4219">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-4219">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-4220">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-4220">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4222">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-4222">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4224">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-4224">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4226">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-4226">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-4228">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-4228">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-4229">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-4229">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4231">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-4231">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-4232">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-4232">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4234">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4234">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-4235">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4235">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-4236">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4236">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-4237">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-4237">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4239">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-4239">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-4240">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-4240">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16_snormsupfcssup-58"></a><span data-ttu-id="80490-4242">DXGI_FORMAT_R16_SNORM<sup>FCS</sup> (58)</span><span class="sxs-lookup"><span data-stu-id="80490-4242">DXGI_FORMAT_R16_SNORM<sup>FCS</sup> (58)</span></span>
| <span data-ttu-id="80490-4243">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-4243">Target</span></span> | <span data-ttu-id="80490-4244">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-4244">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-4245">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-4245">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-4246">16</span><span class="sxs-lookup"><span data-stu-id="80490-4246">16</span></span> |
| <span data-ttu-id="80490-4247">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-4247">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4249">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-4249">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4251">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-4251">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4253">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-4253">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-4254">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-4254">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-4255">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-4255">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4257">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-4257">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4259">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-4259">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4261">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-4261">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4263">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-4263">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4265">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-4265">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4267">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-4267">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-4268">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-4268">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-4269">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-4269">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4271">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-4271">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-4272">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-4272">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4274">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-4274">Mipmap Auto- Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4276">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-4276">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4278">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-4278">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4280">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-4280">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-4281">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-4281">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-4282">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-4282">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-4283">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-4283">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-4284">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-4284">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4286">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4286">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4288">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4288">UAV Typed Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-4290">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4290">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-4291">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-4291">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-4292">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-4292">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-4293">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4293">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-4294">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-4294">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-4295">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-4295">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-4296">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-4296">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4298">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-4298">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4300">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-4300">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4302">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-4302">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-4304">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-4304">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4306">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-4306">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4308">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-4308">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-4309">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-4309">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4311">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4311">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-4312">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4312">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-4313">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4313">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-4314">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-4314">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4316">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-4316">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-4317">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-4317">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16_sintsupfcssup-59"></a><span data-ttu-id="80490-4319">DXGI_FORMAT_R16_SINT<sup>FCS</sup> (59)</span><span class="sxs-lookup"><span data-stu-id="80490-4319">DXGI_FORMAT_R16_SINT<sup>FCS</sup> (59)</span></span>
| <span data-ttu-id="80490-4320">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-4320">Target</span></span> | <span data-ttu-id="80490-4321">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-4321">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-4322">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-4322">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-4323">16</span><span class="sxs-lookup"><span data-stu-id="80490-4323">16</span></span> |
| <span data-ttu-id="80490-4324">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-4324">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4326">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-4326">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4328">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-4328">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4330">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-4330">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-4331">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-4331">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-4332">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-4332">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4334">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-4334">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4336">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-4336">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4338">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-4338">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4340">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-4340">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4342">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-4342">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-4343">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-4343">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-4344">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-4344">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-4345">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-4345">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-4346">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-4346">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-4347">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-4347">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4349">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-4349">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-4350">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-4350">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4352">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-4352">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-4353">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-4353">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-4354">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-4354">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-4355">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-4355">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-4356">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-4356">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-4357">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-4357">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4359">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4359">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4361">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4361">UAV Typed Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4363">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4363">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-4364">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-4364">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-4365">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-4365">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-4366">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4366">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-4367">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-4367">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-4368">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-4368">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-4369">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-4369">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4371">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-4371">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4373">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-4373">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4375">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-4375">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-4377">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-4377">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-4378">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-4378">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4380">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-4380">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-4381">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-4381">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4383">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4383">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-4384">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4384">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-4385">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4385">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-4386">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-4386">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4388">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-4388">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-4389">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-4389">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="80490-4391"><sup>Computadores</sup> DXGI_FORMAT_R8_TYPELESS (60)</span><span class="sxs-lookup"><span data-stu-id="80490-4391">DXGI_FORMAT_R8_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="80490-4392">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-4392">Target</span></span> | <span data-ttu-id="80490-4393">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-4393">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-4394">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-4394">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-4395">8</span><span class="sxs-lookup"><span data-stu-id="80490-4395">8</span></span> |
| <span data-ttu-id="80490-4396">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-4396">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4398">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-4398">Buffer</span></span> | \- |
| <span data-ttu-id="80490-4399">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-4399">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-4400">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-4400">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-4401">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-4401">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-4402">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-4402">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4404">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-4404">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4406">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-4406">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4408">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-4408">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4410">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-4410">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-4411">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-4411">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-4412">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-4412">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-4413">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-4413">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-4414">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-4414">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-4415">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-4415">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-4416">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-4416">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4418">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-4418">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-4419">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-4419">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-4420">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-4420">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-4421">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-4421">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-4422">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-4422">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-4423">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-4423">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-4424">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-4424">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-4425">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-4425">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-4426">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4426">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-4427">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4427">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-4428">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4428">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-4429">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-4429">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-4430">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-4430">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-4431">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4431">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-4432">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-4432">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-4433">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-4433">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-4434">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-4434">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4436">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-4436">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-4437">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-4437">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-4438">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-4438">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-4439">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-4439">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-4440">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-4440">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-4441">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-4441">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-4442">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-4442">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4444">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4444">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-4445">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4445">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-4446">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4446">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-4447">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-4447">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4449">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-4449">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-4450">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-4450">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8_unormsupfcssup-61"></a><span data-ttu-id="80490-4452">DXGI_FORMAT_R8_UNORM<sup>FCS</sup> (61)</span><span class="sxs-lookup"><span data-stu-id="80490-4452">DXGI_FORMAT_R8_UNORM<sup>FCS</sup> (61)</span></span>
| <span data-ttu-id="80490-4453">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-4453">Target</span></span> | <span data-ttu-id="80490-4454">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-4454">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-4455">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-4455">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-4456">8</span><span class="sxs-lookup"><span data-stu-id="80490-4456">8</span></span> |
| <span data-ttu-id="80490-4457">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-4457">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4459">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-4459">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4461">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-4461">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4463">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-4463">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-4464">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-4464">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-4465">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-4465">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4467">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-4467">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4469">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-4469">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4471">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-4471">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4473">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-4473">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4475">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-4475">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4477">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-4477">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-4478">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-4478">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-4479">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-4479">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4481">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-4481">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-4482">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-4482">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4484">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-4484">Mipmap Auto- Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4486">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-4486">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4488">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-4488">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4490">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-4490">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-4491">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-4491">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-4492">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-4492">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-4493">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-4493">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-4494">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-4494">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4496">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4496">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4498">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4498">UAV Typed Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4500">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4500">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-4501">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-4501">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-4502">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-4502">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-4503">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4503">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-4504">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-4504">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-4505">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-4505">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-4506">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-4506">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4508">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-4508">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4510">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-4510">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4512">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-4512">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-4514">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-4514">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4516">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-4516">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4518">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-4518">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-4519">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-4519">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4521">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4521">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-4522">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4522">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-4523">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4523">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-4524">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-4524">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4526">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-4526">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-4527">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-4527">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8_uintsupfcssup-62"></a><span data-ttu-id="80490-4529">DXGI_FORMAT_R8_UINT<sup>FCS</sup> (62)</span><span class="sxs-lookup"><span data-stu-id="80490-4529">DXGI_FORMAT_R8_UINT<sup>FCS</sup> (62)</span></span>
| <span data-ttu-id="80490-4530">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-4530">Target</span></span> | <span data-ttu-id="80490-4531">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-4531">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-4532">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-4532">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-4533">8</span><span class="sxs-lookup"><span data-stu-id="80490-4533">8</span></span> |
| <span data-ttu-id="80490-4534">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-4534">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4536">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-4536">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4538">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-4538">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4540">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-4540">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-4541">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-4541">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-4542">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-4542">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4544">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-4544">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4546">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-4546">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4548">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-4548">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4550">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-4550">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4552">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-4552">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-4553">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-4553">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-4554">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-4554">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-4555">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-4555">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-4556">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-4556">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-4557">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-4557">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4559">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-4559">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-4560">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-4560">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4562">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-4562">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-4563">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-4563">Output Merger Logic Op</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4565">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-4565">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-4566">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-4566">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-4567">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-4567">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-4568">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-4568">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4570">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4570">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4572">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4572">UAV Typed Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4574">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4574">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-4575">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-4575">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-4576">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-4576">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-4577">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4577">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-4578">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-4578">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-4579">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-4579">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-4580">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-4580">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4582">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-4582">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4584">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-4584">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4586">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-4586">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-4588">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-4588">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-4589">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-4589">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4591">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-4591">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-4592">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-4592">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4594">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4594">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-4595">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4595">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-4596">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4596">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-4597">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-4597">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4599">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-4599">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-4600">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-4600">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8_snormsupfcssup-63"></a><span data-ttu-id="80490-4602">DXGI_FORMAT_R8_SNORM<sup>FCS</sup> (63)</span><span class="sxs-lookup"><span data-stu-id="80490-4602">DXGI_FORMAT_R8_SNORM<sup>FCS</sup> (63)</span></span>
| <span data-ttu-id="80490-4603">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-4603">Target</span></span> | <span data-ttu-id="80490-4604">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-4604">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-4605">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-4605">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-4606">8</span><span class="sxs-lookup"><span data-stu-id="80490-4606">8</span></span> |
| <span data-ttu-id="80490-4607">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-4607">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4609">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-4609">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4611">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-4611">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4613">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-4613">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-4614">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-4614">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-4615">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-4615">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4617">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-4617">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4619">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-4619">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4621">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-4621">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4623">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-4623">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4625">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-4625">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4627">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-4627">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-4628">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-4628">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-4629">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-4629">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4631">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-4631">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-4632">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-4632">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4634">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-4634">Mipmap Auto- Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4636">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-4636">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4638">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-4638">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4640">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-4640">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-4641">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-4641">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-4642">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-4642">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-4643">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-4643">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-4644">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-4644">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4646">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4646">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4648">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4648">UAV Typed Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-4650">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4650">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-4651">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-4651">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-4652">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-4652">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-4653">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4653">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-4654">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-4654">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-4655">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-4655">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-4656">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-4656">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4658">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-4658">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4660">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-4660">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4662">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-4662">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-4664">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-4664">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4666">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-4666">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4668">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-4668">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-4669">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-4669">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4671">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4671">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-4672">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4672">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-4673">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4673">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-4674">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-4674">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4676">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-4676">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-4677">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-4677">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8_sintsupfcssup-64"></a><span data-ttu-id="80490-4679">DXGI_FORMAT_R8_SINT<sup>FCS</sup> (64)</span><span class="sxs-lookup"><span data-stu-id="80490-4679">DXGI_FORMAT_R8_SINT<sup>FCS</sup> (64)</span></span>
| <span data-ttu-id="80490-4680">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-4680">Target</span></span> | <span data-ttu-id="80490-4681">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-4681">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-4682">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-4682">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-4683">8</span><span class="sxs-lookup"><span data-stu-id="80490-4683">8</span></span> |
| <span data-ttu-id="80490-4684">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-4684">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4686">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-4686">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4688">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-4688">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4690">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-4690">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-4691">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-4691">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-4692">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-4692">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4694">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-4694">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4696">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-4696">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4698">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-4698">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4700">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-4700">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4702">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-4702">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-4703">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-4703">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-4704">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-4704">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-4705">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-4705">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-4706">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-4706">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-4707">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-4707">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4709">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-4709">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-4710">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-4710">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4712">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-4712">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-4713">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-4713">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-4714">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-4714">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-4715">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-4715">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-4716">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-4716">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-4717">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-4717">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4719">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4719">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4721">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4721">UAV Typed Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4723">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4723">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-4724">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-4724">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-4725">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-4725">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-4726">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4726">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-4727">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-4727">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-4728">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-4728">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-4729">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-4729">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4731">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-4731">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4733">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-4733">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4735">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-4735">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-4737">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-4737">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-4738">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-4738">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4740">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-4740">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-4741">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-4741">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4743">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4743">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-4744">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4744">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-4745">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4745">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-4746">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-4746">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4748">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-4748">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-4749">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-4749">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="80490-4751">DXGI_FORMAT_A8_UNORM<sup>FNS</sup> (65)</span><span class="sxs-lookup"><span data-stu-id="80490-4751">DXGI_FORMAT_A8_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="80490-4752">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-4752">Target</span></span> | <span data-ttu-id="80490-4753">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-4753">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-4754">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-4754">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-4755">8</span><span class="sxs-lookup"><span data-stu-id="80490-4755">8</span></span> |
| <span data-ttu-id="80490-4756">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-4756">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4758">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-4758">Buffer</span></span> | \- |
| <span data-ttu-id="80490-4759">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-4759">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-4760">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-4760">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-4761">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-4761">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-4762">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-4762">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4764">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-4764">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4766">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-4766">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4768">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-4768">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4770">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-4770">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4772">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-4772">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4774">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-4774">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-4775">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-4775">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-4776">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-4776">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4778">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-4778">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-4779">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-4779">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4781">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-4781">Mipmap Auto- Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4783">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-4783">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4785">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-4785">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4787">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-4787">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-4788">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-4788">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-4789">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-4789">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-4790">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-4790">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-4791">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-4791">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4793">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4793">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4795">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4795">UAV Typed Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-4797">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4797">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-4798">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-4798">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-4799">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-4799">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-4800">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4800">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-4801">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-4801">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-4802">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-4802">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-4803">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-4803">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4805">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-4805">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4807">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-4807">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4809">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-4809">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-4811">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-4811">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4813">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-4813">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4815">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-4815">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-4816">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-4816">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="80490-4817">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4817">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-4818">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4818">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-4819">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4819">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-4820">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-4820">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4822">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-4822">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-4823">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-4823">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="80490-4825">DXGI_FORMAT_R9G9B9E5_SHAREDEXP<sup>FNC</sup> (67)</span><span class="sxs-lookup"><span data-stu-id="80490-4825">DXGI_FORMAT_R9G9B9E5_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="80490-4826">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-4826">Target</span></span> | <span data-ttu-id="80490-4827">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-4827">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-4828">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-4828">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-4829">32</span><span class="sxs-lookup"><span data-stu-id="80490-4829">32</span></span> |
| <span data-ttu-id="80490-4830">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-4830">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4832">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-4832">Buffer</span></span> | \- |
| <span data-ttu-id="80490-4833">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-4833">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-4834">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-4834">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-4835">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-4835">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-4836">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-4836">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4838">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-4838">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4840">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-4840">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4842">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-4842">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4844">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-4844">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4846">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-4846">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4848">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-4848">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-4849">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-4849">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-4850">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-4850">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4852">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-4852">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-4853">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-4853">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4855">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-4855">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-4856">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-4856">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-4857">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-4857">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-4858">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-4858">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-4859">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-4859">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-4860">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-4860">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-4861">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-4861">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-4862">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-4862">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-4863">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4863">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-4864">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4864">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-4865">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4865">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-4866">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-4866">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-4867">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-4867">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-4868">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4868">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-4869">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-4869">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-4870">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-4870">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-4871">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-4871">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4873">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-4873">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-4874">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-4874">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-4875">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-4875">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-4876">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-4876">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-4877">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-4877">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-4878">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-4878">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-4879">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-4879">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="80490-4880">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4880">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-4881">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4881">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-4882">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4882">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-4883">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-4883">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-4884">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-4884">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-4885">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-4885">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="80490-4887">DXGI_FORMAT_R8G8_B8G8_UNORM<sup>FNC</sup> (68)</span><span class="sxs-lookup"><span data-stu-id="80490-4887">DXGI_FORMAT_R8G8_B8G8_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="80490-4888">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-4888">Target</span></span> | <span data-ttu-id="80490-4889">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-4889">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-4890">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-4890">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-4891">16</span><span class="sxs-lookup"><span data-stu-id="80490-4891">16</span></span> |
| <span data-ttu-id="80490-4892">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-4892">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4894">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-4894">Buffer</span></span> | \- |
| <span data-ttu-id="80490-4895">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-4895">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-4896">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-4896">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-4897">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-4897">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-4898">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-4898">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4900">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-4900">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4902">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-4902">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4904">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-4904">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4906">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-4906">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4908">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-4908">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4910">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-4910">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-4911">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-4911">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-4912">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-4912">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4914">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-4914">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-4915">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-4915">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4917">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-4917">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-4918">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-4918">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-4919">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-4919">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-4920">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-4920">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-4921">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-4921">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-4922">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-4922">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-4923">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-4923">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-4924">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-4924">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-4925">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4925">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-4926">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4926">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-4927">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4927">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-4928">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-4928">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-4929">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-4929">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-4930">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4930">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-4931">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-4931">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-4932">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-4932">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-4933">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-4933">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4935">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-4935">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-4936">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-4936">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-4937">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-4937">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-4938">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-4938">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-4939">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-4939">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-4940">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-4940">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-4941">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-4941">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="80490-4942">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4942">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-4943">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4943">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-4944">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-4944">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-4945">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-4945">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-4946">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-4946">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-4947">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-4947">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="80490-4948">DXGI_FORMAT_G8R8_G8B8_UNORM<sup>FNC</sup> (69)</span><span class="sxs-lookup"><span data-stu-id="80490-4948">DXGI_FORMAT_G8R8_G8B8_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="80490-4949">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-4949">Target</span></span> | <span data-ttu-id="80490-4950">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-4950">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-4951">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-4951">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-4952">16</span><span class="sxs-lookup"><span data-stu-id="80490-4952">16</span></span> |
| <span data-ttu-id="80490-4953">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-4953">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4955">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-4955">Buffer</span></span> | \- |
| <span data-ttu-id="80490-4956">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-4956">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-4957">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-4957">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-4958">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-4958">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-4959">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-4959">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4961">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-4961">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4963">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-4963">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4965">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-4965">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4967">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-4967">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4969">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-4969">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4971">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-4971">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-4972">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-4972">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-4973">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-4973">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4975">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-4975">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-4976">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-4976">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4978">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-4978">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-4979">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-4979">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-4980">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-4980">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-4981">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-4981">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-4982">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-4982">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-4983">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-4983">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-4984">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-4984">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-4985">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-4985">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-4986">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4986">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-4987">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4987">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-4988">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4988">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-4989">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-4989">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-4990">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-4990">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-4991">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-4991">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-4992">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-4992">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-4993">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-4993">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-4994">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-4994">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-4996">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-4996">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-4997">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-4997">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-4998">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-4998">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-4999">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-4999">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-5000">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-5000">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-5001">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-5001">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-5002">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-5002">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="80490-5003">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5003">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-5004">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5004">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-5005">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5005">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-5006">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-5006">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-5007">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-5007">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-5008">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-5008">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="80490-5009">DXGI_FORMAT_BC1_TYPELESS<sup>PCC</sup> (70)</span><span class="sxs-lookup"><span data-stu-id="80490-5009">DXGI_FORMAT_BC1_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="80490-5010">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-5010">Target</span></span> | <span data-ttu-id="80490-5011">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-5011">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-5012">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-5012">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-5013">64</span><span class="sxs-lookup"><span data-stu-id="80490-5013">64</span></span> |
| <span data-ttu-id="80490-5014">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-5014">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5016">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-5016">Buffer</span></span> | \- |
| <span data-ttu-id="80490-5017">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5017">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-5018">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5018">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-5019">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-5019">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-5020">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-5020">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-5021">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-5021">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5023">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-5023">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5025">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-5025">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5027">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-5027">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-5028">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-5028">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-5029">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-5029">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-5030">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-5030">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-5031">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5031">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-5032">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5032">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-5033">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5033">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5035">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5035">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-5036">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5036">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5037">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-5037">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5038">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-5038">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-5039">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-5039">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-5040">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-5040">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5041">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-5041">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5042">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-5042">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-5043">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5043">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-5044">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5044">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-5045">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5045">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-5046">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-5046">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-5047">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-5047">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-5048">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5048">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-5049">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-5049">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5050">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-5050">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5051">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-5051">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5053">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5053">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5054">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-5054">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5055">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-5055">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-5056">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-5056">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-5057">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-5057">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-5058">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-5058">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-5059">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-5059">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5061">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5061">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-5062">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5062">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-5063">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5063">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-5064">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-5064">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5066">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-5066">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-5067">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-5067">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc1_unorm-supfccsup-71"></a><span data-ttu-id="80490-5069">DXGI_FORMAT_BC1_UNORM <sup>FCC</sup> (71)</span><span class="sxs-lookup"><span data-stu-id="80490-5069">DXGI_FORMAT_BC1_UNORM <sup>FCC</sup> (71)</span></span>
| <span data-ttu-id="80490-5070">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-5070">Target</span></span> | <span data-ttu-id="80490-5071">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-5071">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-5072">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-5072">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-5073">64</span><span class="sxs-lookup"><span data-stu-id="80490-5073">64</span></span> |
| <span data-ttu-id="80490-5074">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-5074">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5076">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-5076">Buffer</span></span> | \- |
| <span data-ttu-id="80490-5077">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5077">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-5078">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5078">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-5079">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-5079">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-5080">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-5080">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-5081">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-5081">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5083">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-5083">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5085">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-5085">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5087">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-5087">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5089">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-5089">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5091">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-5091">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-5092">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-5092">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-5093">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5093">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5095">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5095">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-5096">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5096">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5098">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5098">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-5099">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5099">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5100">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-5100">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5101">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-5101">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-5102">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-5102">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-5103">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-5103">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5104">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-5104">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5105">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-5105">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-5106">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5106">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-5107">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5107">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-5108">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5108">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-5109">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-5109">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-5110">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-5110">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-5111">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5111">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-5112">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-5112">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5113">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-5113">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5114">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-5114">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5116">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5116">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5117">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-5117">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5118">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-5118">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-5119">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-5119">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-5120">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-5120">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-5121">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-5121">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-5122">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-5122">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5124">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5124">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-5125">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5125">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-5126">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5126">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-5127">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-5127">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5129">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-5129">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-5130">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-5130">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc1_unorm_srgb-supfccsup-72"></a><span data-ttu-id="80490-5132">DXGI_FORMAT_BC1_UNORM_SRGB <sup>FCC</sup> (72)</span><span class="sxs-lookup"><span data-stu-id="80490-5132">DXGI_FORMAT_BC1_UNORM_SRGB <sup>FCC</sup> (72)</span></span>
| <span data-ttu-id="80490-5133">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-5133">Target</span></span> | <span data-ttu-id="80490-5134">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-5134">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-5135">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-5135">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-5136">64</span><span class="sxs-lookup"><span data-stu-id="80490-5136">64</span></span> |
| <span data-ttu-id="80490-5137">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-5137">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5139">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-5139">Buffer</span></span> | \- |
| <span data-ttu-id="80490-5140">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5140">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-5141">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5141">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-5142">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-5142">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-5143">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-5143">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-5144">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-5144">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5146">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-5146">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5148">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-5148">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5150">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-5150">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5152">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-5152">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5154">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-5154">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-5155">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-5155">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-5156">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5156">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5158">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5158">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-5159">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5159">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5161">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5161">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-5162">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5162">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5163">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-5163">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5164">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-5164">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-5165">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-5165">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-5166">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-5166">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5167">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-5167">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5168">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-5168">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-5169">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5169">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-5170">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5170">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-5171">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5171">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-5172">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-5172">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-5173">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-5173">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-5174">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5174">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-5175">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-5175">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5176">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-5176">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5177">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-5177">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5179">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5179">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5180">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-5180">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5181">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-5181">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-5182">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-5182">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-5183">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-5183">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-5184">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-5184">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-5185">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-5185">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5187">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5187">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-5188">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5188">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-5189">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5189">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-5190">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-5190">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5192">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-5192">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-5193">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-5193">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="80490-5195">DXGI_FORMAT_BC2_TYPELESS<sup>PCC</sup> (73)</span><span class="sxs-lookup"><span data-stu-id="80490-5195">DXGI_FORMAT_BC2_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="80490-5196">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-5196">Target</span></span> | <span data-ttu-id="80490-5197">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-5197">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-5198">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-5198">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-5199">128</span><span class="sxs-lookup"><span data-stu-id="80490-5199">128</span></span> |
| <span data-ttu-id="80490-5200">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-5200">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5202">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-5202">Buffer</span></span> | \- |
| <span data-ttu-id="80490-5203">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5203">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-5204">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5204">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-5205">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-5205">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-5206">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-5206">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-5207">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-5207">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5209">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-5209">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5211">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-5211">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5213">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-5213">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-5214">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-5214">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-5215">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-5215">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-5216">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-5216">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-5217">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5217">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-5218">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5218">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-5219">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5219">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5221">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5221">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-5222">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5222">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5223">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-5223">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5224">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-5224">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-5225">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-5225">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-5226">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-5226">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5227">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-5227">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5228">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-5228">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-5229">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5229">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-5230">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5230">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-5231">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5231">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-5232">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-5232">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-5233">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-5233">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-5234">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5234">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-5235">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-5235">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5236">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-5236">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5237">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-5237">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5239">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5239">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5240">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-5240">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5241">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-5241">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-5242">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-5242">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-5243">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-5243">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-5244">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-5244">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-5245">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-5245">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5247">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5247">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-5248">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5248">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-5249">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5249">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-5250">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-5250">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5252">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-5252">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-5253">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-5253">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc2_unorm-supfccsup-74"></a><span data-ttu-id="80490-5255">DXGI_FORMAT_BC2_UNORM <sup>FCC</sup> (74)</span><span class="sxs-lookup"><span data-stu-id="80490-5255">DXGI_FORMAT_BC2_UNORM <sup>FCC</sup> (74)</span></span>
| <span data-ttu-id="80490-5256">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-5256">Target</span></span> | <span data-ttu-id="80490-5257">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-5257">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-5258">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-5258">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-5259">128</span><span class="sxs-lookup"><span data-stu-id="80490-5259">128</span></span> |
| <span data-ttu-id="80490-5260">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-5260">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5262">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-5262">Buffer</span></span> | \- |
| <span data-ttu-id="80490-5263">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5263">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-5264">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5264">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-5265">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-5265">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-5266">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-5266">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-5267">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-5267">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5269">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-5269">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5271">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-5271">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5273">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-5273">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5275">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-5275">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5277">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-5277">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-5278">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-5278">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-5279">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5279">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5281">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5281">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-5282">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5282">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5284">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5284">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-5285">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5285">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5286">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-5286">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5287">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-5287">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-5288">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-5288">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-5289">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-5289">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5290">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-5290">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5291">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-5291">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-5292">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5292">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-5293">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5293">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-5294">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5294">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-5295">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-5295">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-5296">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-5296">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-5297">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5297">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-5298">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-5298">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5299">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-5299">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5300">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-5300">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5302">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5302">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5303">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-5303">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5304">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-5304">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-5305">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-5305">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-5306">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-5306">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-5307">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-5307">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-5308">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-5308">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5310">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5310">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-5311">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5311">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-5312">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5312">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-5313">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-5313">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5315">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-5315">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-5316">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-5316">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc2_unorm_srgb-supfccsup-75"></a><span data-ttu-id="80490-5318">DXGI_FORMAT_BC2_UNORM_SRGB <sup>FCC</sup> (75)</span><span class="sxs-lookup"><span data-stu-id="80490-5318">DXGI_FORMAT_BC2_UNORM_SRGB <sup>FCC</sup> (75)</span></span>
| <span data-ttu-id="80490-5319">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-5319">Target</span></span> | <span data-ttu-id="80490-5320">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-5320">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-5321">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-5321">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-5322">128</span><span class="sxs-lookup"><span data-stu-id="80490-5322">128</span></span> |
| <span data-ttu-id="80490-5323">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-5323">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5325">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-5325">Buffer</span></span> | \- |
| <span data-ttu-id="80490-5326">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5326">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-5327">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5327">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-5328">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-5328">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-5329">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-5329">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-5330">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-5330">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5332">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-5332">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5334">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-5334">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5336">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-5336">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5338">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-5338">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5340">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-5340">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-5341">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-5341">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-5342">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5342">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5344">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5344">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-5345">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5345">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5347">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5347">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-5348">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5348">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5349">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-5349">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5350">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-5350">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-5351">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-5351">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-5352">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-5352">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5353">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-5353">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5354">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-5354">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-5355">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5355">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-5356">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5356">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-5357">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5357">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-5358">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-5358">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-5359">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-5359">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-5360">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5360">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-5361">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-5361">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5362">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-5362">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5363">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-5363">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5365">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5365">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5366">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-5366">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5367">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-5367">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-5368">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-5368">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-5369">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-5369">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-5370">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-5370">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-5371">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-5371">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5373">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5373">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-5374">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5374">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-5375">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5375">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-5376">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-5376">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5378">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-5378">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-5379">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-5379">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="80490-5381">DXGI_FORMAT_BC3_TYPELESS<sup>PCC</sup> (76)</span><span class="sxs-lookup"><span data-stu-id="80490-5381">DXGI_FORMAT_BC3_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="80490-5382">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-5382">Target</span></span> | <span data-ttu-id="80490-5383">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-5383">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-5384">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-5384">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-5385">128</span><span class="sxs-lookup"><span data-stu-id="80490-5385">128</span></span> |
| <span data-ttu-id="80490-5386">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-5386">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5388">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-5388">Buffer</span></span> | \- |
| <span data-ttu-id="80490-5389">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5389">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-5390">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5390">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-5391">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-5391">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-5392">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-5392">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-5393">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-5393">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5395">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-5395">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5397">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-5397">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5399">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-5399">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-5400">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-5400">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-5401">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-5401">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-5402">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-5402">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-5403">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5403">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-5404">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5404">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-5405">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5405">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5407">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5407">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-5408">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5408">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5409">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-5409">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5410">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-5410">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-5411">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-5411">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-5412">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-5412">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5413">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-5413">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5414">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-5414">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-5415">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5415">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-5416">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5416">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-5417">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5417">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-5418">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-5418">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-5419">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-5419">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-5420">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5420">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-5421">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-5421">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5422">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-5422">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5423">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-5423">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5425">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5425">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5426">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-5426">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5427">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-5427">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-5428">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-5428">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-5429">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-5429">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-5430">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-5430">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-5431">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-5431">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5433">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5433">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-5434">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5434">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-5435">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5435">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-5436">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-5436">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5438">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-5438">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-5439">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-5439">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc3_unorm-supfccsup-77"></a><span data-ttu-id="80490-5441">DXGI_FORMAT_BC3_UNORM <sup>FCC</sup> (77)</span><span class="sxs-lookup"><span data-stu-id="80490-5441">DXGI_FORMAT_BC3_UNORM <sup>FCC</sup> (77)</span></span>
| <span data-ttu-id="80490-5442">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-5442">Target</span></span> | <span data-ttu-id="80490-5443">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-5443">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-5444">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-5444">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-5445">128</span><span class="sxs-lookup"><span data-stu-id="80490-5445">128</span></span> |
| <span data-ttu-id="80490-5446">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-5446">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5448">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-5448">Buffer</span></span> | \- |
| <span data-ttu-id="80490-5449">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5449">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-5450">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5450">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-5451">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-5451">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-5452">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-5452">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-5453">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-5453">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5455">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-5455">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5457">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-5457">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5459">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-5459">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5461">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-5461">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5463">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-5463">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-5464">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-5464">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-5465">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5465">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5467">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5467">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-5468">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5468">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5470">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5470">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-5471">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5471">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5472">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-5472">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5473">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-5473">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-5474">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-5474">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-5475">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-5475">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5476">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-5476">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5477">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-5477">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-5478">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5478">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-5479">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5479">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-5480">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5480">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-5481">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-5481">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-5482">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-5482">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-5483">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5483">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-5484">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-5484">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5485">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-5485">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5486">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-5486">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5488">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5488">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5489">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-5489">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5490">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-5490">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-5491">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-5491">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-5492">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-5492">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-5493">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-5493">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-5494">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-5494">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5496">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5496">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-5497">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5497">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-5498">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5498">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-5499">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-5499">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5501">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-5501">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-5502">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-5502">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc3_unorm_srgb-supfccsup-78"></a><span data-ttu-id="80490-5504">DXGI_FORMAT_BC3_UNORM_SRGB <sup>FCC</sup> (78)</span><span class="sxs-lookup"><span data-stu-id="80490-5504">DXGI_FORMAT_BC3_UNORM_SRGB <sup>FCC</sup> (78)</span></span>
| <span data-ttu-id="80490-5505">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-5505">Target</span></span> | <span data-ttu-id="80490-5506">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-5506">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-5507">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-5507">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-5508">128</span><span class="sxs-lookup"><span data-stu-id="80490-5508">128</span></span> |
| <span data-ttu-id="80490-5509">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-5509">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5511">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-5511">Buffer</span></span> | \- |
| <span data-ttu-id="80490-5512">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5512">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-5513">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5513">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-5514">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-5514">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-5515">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-5515">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-5516">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-5516">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5518">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-5518">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5520">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-5520">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5522">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-5522">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5524">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-5524">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5526">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-5526">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-5527">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-5527">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-5528">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5528">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5530">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5530">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-5531">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5531">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5533">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5533">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-5534">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5534">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5535">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-5535">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5536">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-5536">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-5537">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-5537">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-5538">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-5538">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5539">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-5539">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5540">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-5540">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-5541">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5541">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-5542">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5542">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-5543">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5543">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-5544">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-5544">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-5545">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-5545">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-5546">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5546">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-5547">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-5547">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5548">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-5548">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5549">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-5549">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5551">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5551">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5552">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-5552">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5553">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-5553">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-5554">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-5554">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-5555">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-5555">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-5556">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-5556">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-5557">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-5557">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5559">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5559">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-5560">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5560">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-5561">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5561">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-5562">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-5562">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5564">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-5564">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-5565">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-5565">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="80490-5567">DXGI_FORMAT_BC4_TYPELESS<sup>PCC</sup> (79)</span><span class="sxs-lookup"><span data-stu-id="80490-5567">DXGI_FORMAT_BC4_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="80490-5568">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-5568">Target</span></span> | <span data-ttu-id="80490-5569">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-5569">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-5570">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-5570">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-5571">64</span><span class="sxs-lookup"><span data-stu-id="80490-5571">64</span></span> |
| <span data-ttu-id="80490-5572">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-5572">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5574">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-5574">Buffer</span></span> | \- |
| <span data-ttu-id="80490-5575">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5575">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-5576">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5576">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-5577">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-5577">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-5578">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-5578">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-5579">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-5579">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5581">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-5581">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5583">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-5583">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5585">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-5585">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-5586">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-5586">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-5587">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-5587">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-5588">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-5588">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-5589">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5589">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-5590">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5590">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-5591">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5591">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5593">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5593">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-5594">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5594">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5595">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-5595">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5596">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-5596">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-5597">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-5597">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-5598">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-5598">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5599">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-5599">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5600">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-5600">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-5601">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5601">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-5602">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5602">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-5603">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5603">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-5604">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-5604">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-5605">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-5605">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-5606">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5606">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-5607">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-5607">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5608">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-5608">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5609">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-5609">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5611">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5611">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5612">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-5612">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5613">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-5613">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-5614">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-5614">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-5615">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-5615">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-5616">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-5616">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-5617">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-5617">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5619">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5619">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-5620">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5620">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-5621">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5621">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-5622">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-5622">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-5623">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-5623">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-5624">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-5624">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc4_unorm-supfccsup-80"></a><span data-ttu-id="80490-5626">DXGI_FORMAT_BC4_UNORM <sup>FCC</sup> (80)</span><span class="sxs-lookup"><span data-stu-id="80490-5626">DXGI_FORMAT_BC4_UNORM <sup>FCC</sup> (80)</span></span>
| <span data-ttu-id="80490-5627">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-5627">Target</span></span> | <span data-ttu-id="80490-5628">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-5628">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-5629">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-5629">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-5630">64</span><span class="sxs-lookup"><span data-stu-id="80490-5630">64</span></span> |
| <span data-ttu-id="80490-5631">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-5631">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5633">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-5633">Buffer</span></span> | \- |
| <span data-ttu-id="80490-5634">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5634">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-5635">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5635">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-5636">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-5636">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-5637">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-5637">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-5638">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-5638">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5640">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-5640">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5642">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-5642">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5644">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-5644">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5646">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-5646">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5648">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-5648">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-5649">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-5649">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-5650">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5650">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5652">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5652">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-5653">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5653">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5655">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5655">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-5656">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5656">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5657">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-5657">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5658">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-5658">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-5659">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-5659">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-5660">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-5660">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5661">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-5661">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5662">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-5662">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-5663">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5663">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-5664">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5664">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-5665">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5665">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-5666">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-5666">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-5667">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-5667">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-5668">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5668">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-5669">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-5669">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5670">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-5670">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5671">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-5671">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5673">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5673">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5674">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-5674">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5675">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-5675">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-5676">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-5676">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-5677">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-5677">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-5678">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-5678">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-5679">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-5679">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5681">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5681">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-5682">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5682">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-5683">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5683">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-5684">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-5684">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-5685">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-5685">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-5686">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-5686">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc4_snorm-supfccsup-81"></a><span data-ttu-id="80490-5688">DXGI_FORMAT_BC4_SNORM <sup>FCC</sup> (81)</span><span class="sxs-lookup"><span data-stu-id="80490-5688">DXGI_FORMAT_BC4_SNORM <sup>FCC</sup> (81)</span></span>
| <span data-ttu-id="80490-5689">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-5689">Target</span></span> | <span data-ttu-id="80490-5690">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-5690">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-5691">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-5691">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-5692">64</span><span class="sxs-lookup"><span data-stu-id="80490-5692">64</span></span> |
| <span data-ttu-id="80490-5693">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-5693">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5695">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-5695">Buffer</span></span> | \- |
| <span data-ttu-id="80490-5696">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5696">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-5697">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5697">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-5698">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-5698">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-5699">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-5699">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-5700">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-5700">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5702">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-5702">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5704">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-5704">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5706">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-5706">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5708">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-5708">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5710">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-5710">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-5711">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-5711">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-5712">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5712">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5714">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5714">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-5715">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5715">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5717">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5717">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-5718">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5718">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5719">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-5719">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5720">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-5720">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-5721">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-5721">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-5722">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-5722">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5723">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-5723">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5724">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-5724">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-5725">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5725">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-5726">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5726">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-5727">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5727">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-5728">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-5728">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-5729">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-5729">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-5730">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5730">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-5731">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-5731">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5732">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-5732">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5733">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-5733">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5735">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5735">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5736">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-5736">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5737">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-5737">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-5738">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-5738">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-5739">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-5739">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-5740">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-5740">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-5741">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-5741">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5743">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5743">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-5744">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5744">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-5745">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5745">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-5746">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-5746">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-5747">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-5747">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-5748">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-5748">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="80490-5750">DXGI_FORMAT_BC5_TYPELESS<sup>PCC</sup> (82)</span><span class="sxs-lookup"><span data-stu-id="80490-5750">DXGI_FORMAT_BC5_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="80490-5751">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-5751">Target</span></span> | <span data-ttu-id="80490-5752">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-5752">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-5753">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-5753">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-5754">128</span><span class="sxs-lookup"><span data-stu-id="80490-5754">128</span></span> |
| <span data-ttu-id="80490-5755">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-5755">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5757">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-5757">Buffer</span></span> | \- |
| <span data-ttu-id="80490-5758">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5758">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-5759">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5759">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-5760">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-5760">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-5761">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-5761">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-5762">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-5762">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5764">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-5764">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5766">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-5766">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5768">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-5768">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-5769">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-5769">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-5770">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-5770">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-5771">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-5771">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-5772">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5772">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-5773">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5773">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-5774">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5774">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5776">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5776">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-5777">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5777">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5778">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-5778">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5779">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-5779">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-5780">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-5780">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-5781">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-5781">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5782">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-5782">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5783">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-5783">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-5784">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5784">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-5785">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5785">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-5786">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5786">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-5787">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-5787">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-5788">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-5788">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-5789">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5789">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-5790">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-5790">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5791">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-5791">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5792">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-5792">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5794">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5794">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5795">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-5795">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5796">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-5796">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-5797">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-5797">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-5798">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-5798">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-5799">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-5799">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-5800">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-5800">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5802">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5802">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-5803">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5803">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-5804">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5804">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-5805">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-5805">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-5806">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-5806">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-5807">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-5807">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc5_unorm-supfccsup-83"></a><span data-ttu-id="80490-5809">DXGI_FORMAT_BC5_UNORM <sup>FCC</sup> (83)</span><span class="sxs-lookup"><span data-stu-id="80490-5809">DXGI_FORMAT_BC5_UNORM <sup>FCC</sup> (83)</span></span>
| <span data-ttu-id="80490-5810">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-5810">Target</span></span> | <span data-ttu-id="80490-5811">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-5811">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-5812">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-5812">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-5813">128</span><span class="sxs-lookup"><span data-stu-id="80490-5813">128</span></span> |
| <span data-ttu-id="80490-5814">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-5814">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5816">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-5816">Buffer</span></span> | \- |
| <span data-ttu-id="80490-5817">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5817">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-5818">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5818">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-5819">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-5819">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-5820">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-5820">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-5821">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-5821">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5823">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-5823">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5825">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-5825">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5827">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-5827">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5829">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-5829">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5831">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-5831">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-5832">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-5832">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-5833">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5833">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5835">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5835">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-5836">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5836">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5838">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5838">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-5839">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5839">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5840">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-5840">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5841">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-5841">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-5842">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-5842">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-5843">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-5843">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5844">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-5844">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5845">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-5845">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-5846">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5846">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-5847">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5847">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-5848">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5848">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-5849">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-5849">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-5850">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-5850">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-5851">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5851">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-5852">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-5852">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5853">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-5853">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5854">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-5854">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5856">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5856">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5857">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-5857">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5858">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-5858">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-5859">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-5859">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-5860">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-5860">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-5861">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-5861">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-5862">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-5862">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5864">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5864">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-5865">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5865">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-5866">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5866">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-5867">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-5867">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-5868">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-5868">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-5869">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-5869">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc5_snorm-supfccsup-84"></a><span data-ttu-id="80490-5871">DXGI_FORMAT_BC5_SNORM <sup>FCC</sup> (84)</span><span class="sxs-lookup"><span data-stu-id="80490-5871">DXGI_FORMAT_BC5_SNORM <sup>FCC</sup> (84)</span></span>
| <span data-ttu-id="80490-5872">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-5872">Target</span></span> | <span data-ttu-id="80490-5873">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-5873">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-5874">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-5874">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-5875">128</span><span class="sxs-lookup"><span data-stu-id="80490-5875">128</span></span> |
| <span data-ttu-id="80490-5876">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-5876">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5878">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-5878">Buffer</span></span> | \- |
| <span data-ttu-id="80490-5879">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5879">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-5880">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5880">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-5881">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-5881">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-5882">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-5882">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-5883">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-5883">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5885">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-5885">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5887">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-5887">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5889">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-5889">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5891">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-5891">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5893">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-5893">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-5894">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-5894">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-5895">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5895">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5897">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5897">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-5898">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5898">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5900">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5900">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-5901">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5901">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5902">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-5902">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5903">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-5903">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-5904">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-5904">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-5905">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-5905">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5906">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-5906">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5907">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-5907">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-5908">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5908">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-5909">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5909">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-5910">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5910">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-5911">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-5911">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-5912">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-5912">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-5913">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5913">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-5914">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-5914">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5915">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-5915">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5916">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-5916">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5918">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5918">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5919">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-5919">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-5920">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-5920">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-5921">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-5921">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-5922">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-5922">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-5923">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-5923">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-5924">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-5924">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5926">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5926">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-5927">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5927">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-5928">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-5928">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-5929">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-5929">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-5930">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-5930">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-5931">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-5931">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="80490-5933">DXGI_FORMAT_B5G6R5_UNORM<sup>FNS</sup> (85)</span><span class="sxs-lookup"><span data-stu-id="80490-5933">DXGI_FORMAT_B5G6R5_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="80490-5934">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-5934">Target</span></span> | <span data-ttu-id="80490-5935">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-5935">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-5936">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-5936">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-5937">16</span><span class="sxs-lookup"><span data-stu-id="80490-5937">16</span></span> |
| <span data-ttu-id="80490-5938">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-5938">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5940">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-5940">Buffer</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-5942">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5942">Input Assembler Vertex Buffer</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-5944">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-5944">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-5945">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-5945">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-5946">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-5946">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5948">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-5948">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5950">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-5950">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5952">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-5952">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5954">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-5954">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5956">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-5956">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5958">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-5958">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-5959">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-5959">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-5960">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5960">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5962">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-5962">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-5963">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5963">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5965">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-5965">Mipmap Auto- Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5967">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5967">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5969">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-5969">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5971">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-5971">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-5972">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-5972">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-5973">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-5973">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5974">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-5974">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-5975">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-5975">Typed UAV</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-5977">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5977">UAV Typed Store</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-5979">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5979">UAV Typed Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-5981">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5981">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-5982">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-5982">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-5983">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-5983">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-5984">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-5984">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-5985">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-5985">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5986">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-5986">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-5987">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-5987">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5989">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-5989">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5991">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-5991">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5993">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-5993">Other Multisample Count RT</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5995">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-5995">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5997">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-5997">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-5999">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-5999">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-6000">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-6000">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="80490-6001">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6001">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-6002">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6002">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-6003">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6003">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-6004">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-6004">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-6005">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-6005">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-6006">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-6006">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="80490-6008">DXGI_FORMAT_B5G5R5A1_UNORM<sup>FNS</sup> (86)</span><span class="sxs-lookup"><span data-stu-id="80490-6008">DXGI_FORMAT_B5G5R5A1_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="80490-6009">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-6009">Target</span></span> | <span data-ttu-id="80490-6010">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-6010">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-6011">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-6011">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-6012">16</span><span class="sxs-lookup"><span data-stu-id="80490-6012">16</span></span> |
| <span data-ttu-id="80490-6013">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-6013">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6015">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-6015">Buffer</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-6017">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-6017">Input Assembler Vertex Buffer</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-6019">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-6019">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-6020">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-6020">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-6021">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-6021">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6023">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-6023">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6025">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-6025">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6027">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-6027">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6029">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-6029">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6031">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-6031">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6033">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-6033">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-6034">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-6034">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-6035">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-6035">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6037">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-6037">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-6038">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-6038">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6040">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-6040">Mipmap Auto- Generation</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-6042">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-6042">RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-6044">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-6044">Blendable RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-6046">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-6046">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-6047">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-6047">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-6048">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-6048">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-6049">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-6049">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-6050">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-6050">Typed UAV</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-6052">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6052">UAV Typed Store</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-6054">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6054">UAV Typed Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-6056">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6056">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-6057">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-6057">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-6058">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-6058">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-6059">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6059">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-6060">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-6060">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-6061">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-6061">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-6062">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-6062">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6064">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-6064">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-6066">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-6066">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-6068">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-6068">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-6070">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-6070">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6072">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-6072">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-6074">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-6074">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-6075">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-6075">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="80490-6076">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6076">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-6077">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6077">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-6078">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6078">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-6079">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-6079">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-6080">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-6080">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-6081">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-6081">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="80490-6083"><sup>Computadores</sup> DXGI_FORMAT_B8G8R8A8_TYPELESS (90)</span><span class="sxs-lookup"><span data-stu-id="80490-6083">DXGI_FORMAT_B8G8R8A8_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="80490-6084">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-6084">Target</span></span> | <span data-ttu-id="80490-6085">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-6085">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-6086">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-6086">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-6087">32</span><span class="sxs-lookup"><span data-stu-id="80490-6087">32</span></span> |
| <span data-ttu-id="80490-6088">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-6088">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6090">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-6090">Buffer</span></span> | \- |
| <span data-ttu-id="80490-6091">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-6091">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-6092">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-6092">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-6093">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-6093">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-6094">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-6094">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6096">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-6096">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6098">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-6098">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6100">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-6100">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6102">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-6102">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-6103">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-6103">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-6104">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-6104">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-6105">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-6105">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-6106">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-6106">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-6107">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-6107">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-6108">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-6108">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6110">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-6110">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-6111">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-6111">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6112">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-6112">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6113">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-6113">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-6114">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-6114">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-6115">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-6115">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-6116">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-6116">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-6117">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-6117">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-6118">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6118">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-6119">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6119">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-6120">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6120">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-6121">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-6121">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-6122">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-6122">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-6123">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6123">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-6124">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-6124">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-6125">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-6125">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-6126">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-6126">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6128">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-6128">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6129">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-6129">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6130">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-6130">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-6131">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-6131">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-6132">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-6132">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-6133">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-6133">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-6134">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-6134">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6136">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6136">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-6137">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6137">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-6138">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6138">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-6139">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-6139">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6141">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-6141">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-6142">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-6142">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8a8_unormsupfcssup-87"></a><span data-ttu-id="80490-6144">DXGI_FORMAT_B8G8R8A8_UNORM<sup>FCS</sup> (87)</span><span class="sxs-lookup"><span data-stu-id="80490-6144">DXGI_FORMAT_B8G8R8A8_UNORM<sup>FCS</sup> (87)</span></span>
| <span data-ttu-id="80490-6145">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-6145">Target</span></span> | <span data-ttu-id="80490-6146">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-6146">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-6147">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-6147">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-6148">32</span><span class="sxs-lookup"><span data-stu-id="80490-6148">32</span></span> |
| <span data-ttu-id="80490-6149">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-6149">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6151">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-6151">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6153">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-6153">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6155">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-6155">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-6156">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-6156">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-6157">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-6157">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6159">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-6159">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6161">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-6161">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6163">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-6163">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6165">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-6165">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6167">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-6167">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6169">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-6169">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-6170">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-6170">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-6171">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-6171">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6173">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-6173">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-6174">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-6174">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6176">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-6176">Mipmap Auto- Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6178">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-6178">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6180">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-6180">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6182">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-6182">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-6183">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-6183">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-6184">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-6184">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-6185">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-6185">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-6186">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-6186">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-6187">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6187">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-6188">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6188">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-6189">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6189">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-6190">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-6190">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-6191">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-6191">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-6192">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6192">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-6193">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-6193">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-6194">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-6194">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-6195">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-6195">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6197">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-6197">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6199">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-6199">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6201">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-6201">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-6203">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-6203">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6205">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-6205">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6207">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-6207">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6209">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-6209">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6211">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6211">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-6212">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6212">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-6214">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6214">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6216">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-6216">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6218">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-6218">BackBuffer Castable Even Fully Typed</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6220">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-6220">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfcssup-91"></a><span data-ttu-id="80490-6222">DXGI_FORMAT_B8G8R8A8_UNORM_SRGB<sup>FCS</sup> (91)</span><span class="sxs-lookup"><span data-stu-id="80490-6222">DXGI_FORMAT_B8G8R8A8_UNORM_SRGB<sup>FCS</sup> (91)</span></span>
| <span data-ttu-id="80490-6223">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-6223">Target</span></span> | <span data-ttu-id="80490-6224">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-6224">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-6225">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-6225">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-6226">32</span><span class="sxs-lookup"><span data-stu-id="80490-6226">32</span></span> |
| <span data-ttu-id="80490-6227">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-6227">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6229">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-6229">Buffer</span></span> | \- |
| <span data-ttu-id="80490-6230">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-6230">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-6231">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-6231">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-6232">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-6232">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-6233">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-6233">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6235">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-6235">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6237">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-6237">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6239">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-6239">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6241">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-6241">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6243">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-6243">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6245">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-6245">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-6246">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-6246">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-6247">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-6247">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6249">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-6249">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-6250">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-6250">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6252">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-6252">Mipmap Auto- Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6254">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-6254">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6256">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-6256">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6258">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-6258">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-6259">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-6259">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-6260">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-6260">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-6261">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-6261">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-6262">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-6262">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-6263">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6263">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-6264">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6264">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-6265">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6265">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-6266">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-6266">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-6267">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-6267">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-6268">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6268">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-6269">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-6269">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-6270">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-6270">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-6271">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-6271">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6273">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-6273">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6275">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-6275">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6277">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-6277">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-6279">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-6279">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6281">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-6281">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6283">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-6283">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6285">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-6285">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6287">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6287">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-6288">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6288">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-6290">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6290">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6292">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-6292">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6294">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-6294">BackBuffer Castable Even Fully Typed</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6296">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-6296">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="80490-6298"><sup>Computadores</sup> DXGI_FORMAT_B8G8R8X8_TYPELESS (92)</span><span class="sxs-lookup"><span data-stu-id="80490-6298">DXGI_FORMAT_B8G8R8X8_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="80490-6299">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-6299">Target</span></span> | <span data-ttu-id="80490-6300">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-6300">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-6301">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-6301">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-6302">32</span><span class="sxs-lookup"><span data-stu-id="80490-6302">32</span></span> |
| <span data-ttu-id="80490-6303">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-6303">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6305">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-6305">Buffer</span></span> | \- |
| <span data-ttu-id="80490-6306">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-6306">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-6307">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-6307">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-6308">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-6308">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-6309">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-6309">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6311">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-6311">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6313">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-6313">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6315">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-6315">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6317">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-6317">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-6318">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-6318">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-6319">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-6319">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-6320">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-6320">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-6321">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-6321">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-6322">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-6322">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-6323">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-6323">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6325">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-6325">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-6326">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-6326">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6327">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-6327">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6328">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-6328">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-6329">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-6329">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-6330">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-6330">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-6331">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-6331">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-6332">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-6332">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-6333">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6333">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-6334">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6334">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-6335">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6335">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-6336">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-6336">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-6337">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-6337">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-6338">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6338">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-6339">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-6339">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-6340">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-6340">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-6341">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-6341">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6343">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-6343">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6344">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-6344">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6345">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-6345">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-6346">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-6346">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-6347">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-6347">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-6348">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-6348">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-6349">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-6349">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6351">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6351">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-6352">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6352">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-6353">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6353">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-6354">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-6354">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6356">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-6356">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-6357">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-6357">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8x8_unormsupfcssup-88"></a><span data-ttu-id="80490-6359">DXGI_FORMAT_B8G8R8X8_UNORM<sup>FCS</sup> (88)</span><span class="sxs-lookup"><span data-stu-id="80490-6359">DXGI_FORMAT_B8G8R8X8_UNORM<sup>FCS</sup> (88)</span></span>
| <span data-ttu-id="80490-6360">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-6360">Target</span></span> | <span data-ttu-id="80490-6361">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-6361">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-6362">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-6362">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-6363">32</span><span class="sxs-lookup"><span data-stu-id="80490-6363">32</span></span> |
| <span data-ttu-id="80490-6364">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-6364">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6366">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-6366">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6368">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-6368">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6370">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-6370">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-6371">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-6371">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-6372">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-6372">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6374">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-6374">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6376">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-6376">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6378">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-6378">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6380">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-6380">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6382">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-6382">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6384">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-6384">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-6385">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-6385">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-6386">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-6386">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6388">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-6388">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-6389">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-6389">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6391">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-6391">Mipmap Auto- Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6393">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-6393">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6395">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-6395">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6397">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-6397">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-6398">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-6398">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-6399">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-6399">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-6400">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-6400">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-6401">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-6401">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-6402">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6402">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-6403">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6403">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-6404">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6404">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-6405">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-6405">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-6406">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-6406">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-6407">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6407">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-6408">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-6408">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-6409">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-6409">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-6410">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-6410">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6412">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-6412">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6414">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-6414">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6416">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-6416">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-6418">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-6418">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6420">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-6420">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6422">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-6422">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-6423">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-6423">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6425">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6425">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-6426">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6426">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-6428">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6428">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-6430">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-6430">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6432">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-6432">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-6433">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-6433">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfcssup-93"></a><span data-ttu-id="80490-6435">DXGI_FORMAT_B8G8R8X8_UNORM_SRGB<sup>FCS</sup> (93)</span><span class="sxs-lookup"><span data-stu-id="80490-6435">DXGI_FORMAT_B8G8R8X8_UNORM_SRGB<sup>FCS</sup> (93)</span></span>
| <span data-ttu-id="80490-6436">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-6436">Target</span></span> | <span data-ttu-id="80490-6437">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-6437">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-6438">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-6438">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-6439">32</span><span class="sxs-lookup"><span data-stu-id="80490-6439">32</span></span> |
| <span data-ttu-id="80490-6440">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-6440">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6442">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-6442">Buffer</span></span> | \- |
| <span data-ttu-id="80490-6443">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-6443">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-6444">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-6444">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-6445">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-6445">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-6446">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-6446">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6448">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-6448">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6450">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-6450">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6452">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-6452">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6454">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-6454">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6456">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-6456">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6458">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-6458">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-6459">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-6459">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-6460">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-6460">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6462">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-6462">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-6463">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-6463">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6465">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-6465">Mipmap Auto- Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6467">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-6467">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6469">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-6469">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6471">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-6471">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-6472">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-6472">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-6473">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-6473">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-6474">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-6474">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-6475">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-6475">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-6476">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6476">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-6477">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6477">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-6478">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6478">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-6479">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-6479">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-6480">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-6480">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-6481">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6481">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-6482">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-6482">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-6483">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-6483">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-6484">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-6484">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6486">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-6486">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6488">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-6488">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6490">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-6490">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-6492">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-6492">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6494">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-6494">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6496">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-6496">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-6497">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-6497">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6499">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6499">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-6500">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6500">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-6501">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6501">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-6502">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-6502">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6504">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-6504">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-6505">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-6505">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc6h_typelesssuppccsup-94"></a><span data-ttu-id="80490-6507">DXGI_FORMAT_BC6H_TYPELESS<sup>PCC</sup> (94)</span><span class="sxs-lookup"><span data-stu-id="80490-6507">DXGI_FORMAT_BC6H_TYPELESS<sup>PCC</sup> (94)</span></span>
| <span data-ttu-id="80490-6508">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-6508">Target</span></span> | <span data-ttu-id="80490-6509">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-6509">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-6510">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-6510">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-6511">128</span><span class="sxs-lookup"><span data-stu-id="80490-6511">128</span></span> |
| <span data-ttu-id="80490-6512">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-6512">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6514">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-6514">Buffer</span></span> | \- |
| <span data-ttu-id="80490-6515">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-6515">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-6516">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-6516">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-6517">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-6517">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-6518">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-6518">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-6519">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-6519">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6521">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-6521">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6523">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-6523">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6525">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-6525">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-6526">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-6526">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-6527">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-6527">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-6528">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-6528">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-6529">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-6529">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-6530">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-6530">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-6531">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-6531">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6533">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-6533">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-6534">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-6534">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6535">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-6535">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6536">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-6536">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-6537">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-6537">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-6538">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-6538">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-6539">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-6539">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-6540">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-6540">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-6541">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6541">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-6542">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6542">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-6543">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6543">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-6544">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-6544">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-6545">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-6545">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-6546">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6546">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-6547">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-6547">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-6548">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-6548">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-6549">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-6549">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6551">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-6551">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6552">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-6552">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6553">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-6553">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-6554">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-6554">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-6555">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-6555">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-6556">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-6556">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-6557">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-6557">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6559">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6559">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-6560">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6560">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-6561">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6561">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-6562">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-6562">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-6563">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-6563">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-6564">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-6564">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc6h_uf16-supfccsup-95"></a><span data-ttu-id="80490-6566">DXGI_FORMAT_BC6H_UF16 <sup>FCC</sup> (95)</span><span class="sxs-lookup"><span data-stu-id="80490-6566">DXGI_FORMAT_BC6H_UF16 <sup>FCC</sup> (95)</span></span>
| <span data-ttu-id="80490-6567">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-6567">Target</span></span> | <span data-ttu-id="80490-6568">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-6568">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-6569">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-6569">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-6570">128</span><span class="sxs-lookup"><span data-stu-id="80490-6570">128</span></span> |
| <span data-ttu-id="80490-6571">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-6571">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6573">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-6573">Buffer</span></span> | \- |
| <span data-ttu-id="80490-6574">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-6574">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-6575">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-6575">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-6576">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-6576">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-6577">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-6577">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-6578">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-6578">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6580">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-6580">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6582">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-6582">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6584">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-6584">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6586">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-6586">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6588">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-6588">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-6589">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-6589">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-6590">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-6590">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6592">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-6592">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-6593">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-6593">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6595">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-6595">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-6596">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-6596">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6597">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-6597">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6598">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-6598">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-6599">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-6599">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-6600">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-6600">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-6601">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-6601">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-6602">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-6602">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-6603">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6603">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-6604">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6604">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-6605">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6605">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-6606">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-6606">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-6607">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-6607">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-6608">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6608">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-6609">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-6609">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-6610">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-6610">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-6611">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-6611">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6613">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-6613">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6614">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-6614">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6615">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-6615">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-6616">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-6616">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-6617">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-6617">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-6618">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-6618">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-6619">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-6619">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6621">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6621">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-6622">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6622">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-6623">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6623">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-6624">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-6624">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-6625">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-6625">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-6626">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-6626">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc6h_sf16-supfccsup-96"></a><span data-ttu-id="80490-6628">DXGI_FORMAT_BC6H_SF16 <sup>FCC</sup> (96)</span><span class="sxs-lookup"><span data-stu-id="80490-6628">DXGI_FORMAT_BC6H_SF16 <sup>FCC</sup> (96)</span></span>
| <span data-ttu-id="80490-6629">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-6629">Target</span></span> | <span data-ttu-id="80490-6630">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-6630">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-6631">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-6631">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-6632">128</span><span class="sxs-lookup"><span data-stu-id="80490-6632">128</span></span> |
| <span data-ttu-id="80490-6633">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-6633">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6635">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-6635">Buffer</span></span> | \- |
| <span data-ttu-id="80490-6636">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-6636">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-6637">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-6637">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-6638">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-6638">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-6639">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-6639">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-6640">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-6640">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6642">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-6642">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6644">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-6644">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6646">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-6646">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6648">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-6648">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6650">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-6650">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-6651">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-6651">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-6652">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-6652">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6654">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-6654">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-6655">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-6655">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6657">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-6657">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-6658">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-6658">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6659">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-6659">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6660">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-6660">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-6661">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-6661">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-6662">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-6662">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-6663">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-6663">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-6664">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-6664">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-6665">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6665">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-6666">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6666">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-6667">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6667">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-6668">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-6668">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-6669">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-6669">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-6670">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6670">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-6671">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-6671">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-6672">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-6672">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-6673">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-6673">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6675">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-6675">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6676">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-6676">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6677">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-6677">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-6678">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-6678">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-6679">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-6679">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-6680">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-6680">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-6681">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-6681">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6683">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6683">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-6684">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6684">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-6685">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6685">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-6686">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-6686">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-6687">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-6687">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-6688">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-6688">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc7_typelesssuppccsup-97"></a><span data-ttu-id="80490-6690">DXGI_FORMAT_BC7_TYPELESS<sup>PCC</sup> (97)</span><span class="sxs-lookup"><span data-stu-id="80490-6690">DXGI_FORMAT_BC7_TYPELESS<sup>PCC</sup> (97)</span></span>
| <span data-ttu-id="80490-6691">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-6691">Target</span></span> | <span data-ttu-id="80490-6692">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-6692">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-6693">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-6693">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-6694">128</span><span class="sxs-lookup"><span data-stu-id="80490-6694">128</span></span> |
| <span data-ttu-id="80490-6695">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-6695">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6697">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-6697">Buffer</span></span> | \- |
| <span data-ttu-id="80490-6698">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-6698">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-6699">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-6699">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-6700">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-6700">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-6701">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-6701">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-6702">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-6702">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6704">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-6704">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6706">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-6706">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6708">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-6708">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-6709">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-6709">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-6710">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-6710">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-6711">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-6711">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-6712">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-6712">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-6713">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-6713">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-6714">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-6714">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6716">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-6716">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-6717">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-6717">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6718">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-6718">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6719">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-6719">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-6720">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-6720">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-6721">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-6721">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-6722">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-6722">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-6723">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-6723">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-6724">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6724">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-6725">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6725">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-6726">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6726">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-6727">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-6727">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-6728">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-6728">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-6729">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6729">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-6730">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-6730">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-6731">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-6731">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-6732">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-6732">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6734">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-6734">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6735">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-6735">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6736">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-6736">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-6737">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-6737">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-6738">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-6738">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-6739">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-6739">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-6740">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-6740">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6742">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6742">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-6743">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6743">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-6744">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6744">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-6745">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-6745">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-6746">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-6746">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-6747">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-6747">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc7_unorm-supfccsup-98"></a><span data-ttu-id="80490-6749">DXGI_FORMAT_BC7_UNORM <sup>FCC</sup> (98)</span><span class="sxs-lookup"><span data-stu-id="80490-6749">DXGI_FORMAT_BC7_UNORM <sup>FCC</sup> (98)</span></span>
| <span data-ttu-id="80490-6750">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-6750">Target</span></span> | <span data-ttu-id="80490-6751">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-6751">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-6752">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-6752">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-6753">128</span><span class="sxs-lookup"><span data-stu-id="80490-6753">128</span></span> |
| <span data-ttu-id="80490-6754">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-6754">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6756">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-6756">Buffer</span></span> | \- |
| <span data-ttu-id="80490-6757">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-6757">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-6758">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-6758">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-6759">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-6759">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-6760">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-6760">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-6761">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-6761">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6763">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-6763">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6765">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-6765">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6767">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-6767">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6769">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-6769">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6771">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-6771">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-6772">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-6772">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-6773">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-6773">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6775">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-6775">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-6776">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-6776">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6778">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-6778">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-6779">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-6779">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6780">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-6780">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6781">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-6781">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-6782">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-6782">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-6783">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-6783">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-6784">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-6784">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-6785">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-6785">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-6786">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6786">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-6787">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6787">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-6788">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6788">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-6789">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-6789">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-6790">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-6790">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-6791">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6791">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-6792">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-6792">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-6793">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-6793">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-6794">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-6794">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6796">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-6796">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6797">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-6797">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6798">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-6798">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-6799">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-6799">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-6800">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-6800">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-6801">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-6801">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-6802">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-6802">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6804">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6804">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-6805">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6805">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-6806">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6806">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-6807">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-6807">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-6808">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-6808">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-6809">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-6809">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc7_unorm_srgb-supfccsup-99"></a><span data-ttu-id="80490-6811">DXGI_FORMAT_BC7_UNORM_SRGB <sup>FCC</sup> (99)</span><span class="sxs-lookup"><span data-stu-id="80490-6811">DXGI_FORMAT_BC7_UNORM_SRGB <sup>FCC</sup> (99)</span></span>
| <span data-ttu-id="80490-6812">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-6812">Target</span></span> | <span data-ttu-id="80490-6813">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-6813">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-6814">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-6814">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-6815">128</span><span class="sxs-lookup"><span data-stu-id="80490-6815">128</span></span> |
| <span data-ttu-id="80490-6816">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-6816">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6818">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-6818">Buffer</span></span> | \- |
| <span data-ttu-id="80490-6819">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-6819">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-6820">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-6820">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-6821">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-6821">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-6822">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-6822">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-6823">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-6823">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6825">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-6825">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6827">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-6827">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6829">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-6829">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6831">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-6831">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6833">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-6833">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-6834">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-6834">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-6835">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-6835">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6837">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-6837">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-6838">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-6838">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6840">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-6840">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-6841">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-6841">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6842">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-6842">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6843">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-6843">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-6844">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-6844">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-6845">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-6845">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-6846">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-6846">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-6847">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-6847">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-6848">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6848">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-6849">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6849">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-6850">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6850">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-6851">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-6851">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-6852">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-6852">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-6853">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6853">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-6854">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-6854">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-6855">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-6855">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-6856">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-6856">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6858">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-6858">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6859">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-6859">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6860">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-6860">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-6861">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-6861">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-6862">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-6862">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-6863">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-6863">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-6864">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-6864">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6866">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6866">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-6867">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6867">Video Processor Input</span></span> | \- |
| <span data-ttu-id="80490-6868">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6868">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-6869">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-6869">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-6870">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-6870">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-6871">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-6871">Tiled Resource</span></span> | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="80490-6873">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span><span class="sxs-lookup"><span data-stu-id="80490-6873">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="80490-6874">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-6874">Target</span></span> | <span data-ttu-id="80490-6875">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-6875">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-6876">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-6876">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-6877">32</span><span class="sxs-lookup"><span data-stu-id="80490-6877">32</span></span> |
| <span data-ttu-id="80490-6878">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-6878">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-6880">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-6880">Buffer</span></span> | \- |
| <span data-ttu-id="80490-6881">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-6881">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-6882">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-6882">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-6883">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-6883">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-6884">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-6884">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-6885">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-6885">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6887">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-6887">Texture3D</span></span> | \- |
| <span data-ttu-id="80490-6888">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-6888">TextureCube</span></span> | \- |
| <span data-ttu-id="80490-6889">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-6889">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6891">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-6891">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6893">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-6893">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-6894">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-6894">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-6895">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-6895">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6897">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-6897">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-6898">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-6898">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6900">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-6900">Mipmap Auto- Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6902">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-6902">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6904">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-6904">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6906">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-6906">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-6907">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-6907">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-6908">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-6908">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-6909">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-6909">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-6910">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-6910">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6912">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6912">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6914">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6914">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-6915">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6915">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-6916">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-6916">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-6917">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-6917">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-6918">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6918">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-6919">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-6919">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-6920">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-6920">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-6921">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-6921">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6923">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-6923">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6924">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-6924">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6925">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-6925">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-6926">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-6926">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-6927">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-6927">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-6928">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-6928">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-6929">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-6929">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="80490-6930">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6930">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-6932">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6932">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6934">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6934">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-6936">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-6936">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6938">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-6938">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-6939">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-6939">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="80490-6940">DXGI_FORMAT_Y410<sup>V</sup> (101)</span><span class="sxs-lookup"><span data-stu-id="80490-6940">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="80490-6941">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-6941">Target</span></span> | <span data-ttu-id="80490-6942">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-6942">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-6943">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-6943">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-6944">32</span><span class="sxs-lookup"><span data-stu-id="80490-6944">32</span></span> |
| <span data-ttu-id="80490-6945">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-6945">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-6947">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-6947">Buffer</span></span> | \- |
| <span data-ttu-id="80490-6948">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-6948">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-6949">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-6949">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-6950">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-6950">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-6951">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-6951">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-6952">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-6952">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6954">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-6954">Texture3D</span></span> | \- |
| <span data-ttu-id="80490-6955">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-6955">TextureCube</span></span> | \- |
| <span data-ttu-id="80490-6956">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-6956">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6958">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-6958">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6960">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-6960">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-6961">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-6961">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-6962">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-6962">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6964">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-6964">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-6965">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-6965">Mipmap</span></span> | \- |
| <span data-ttu-id="80490-6966">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-6966">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-6967">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-6967">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6968">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-6968">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6969">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-6969">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-6970">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-6970">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-6971">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-6971">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-6972">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-6972">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-6973">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-6973">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6975">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6975">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6977">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6977">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-6978">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6978">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-6979">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-6979">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-6980">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-6980">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-6981">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-6981">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-6982">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-6982">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-6983">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-6983">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-6984">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-6984">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-6986">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-6986">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6987">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-6987">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-6988">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-6988">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-6989">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-6989">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-6990">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-6990">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-6991">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-6991">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-6992">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-6992">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="80490-6993">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6993">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-6995">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6995">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-6997">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-6997">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-6999">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-6999">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7001">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-7001">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-7002">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-7002">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="80490-7003">DXGI_FORMAT_Y416<sup>V</sup> (102)</span><span class="sxs-lookup"><span data-stu-id="80490-7003">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="80490-7004">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-7004">Target</span></span> | <span data-ttu-id="80490-7005">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-7005">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-7006">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-7006">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-7007">64</span><span class="sxs-lookup"><span data-stu-id="80490-7007">64</span></span> |
| <span data-ttu-id="80490-7008">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-7008">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-7010">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-7010">Buffer</span></span> | \- |
| <span data-ttu-id="80490-7011">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-7011">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-7012">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-7012">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-7013">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-7013">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-7014">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-7014">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-7015">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-7015">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7017">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-7017">Texture3D</span></span> | \- |
| <span data-ttu-id="80490-7018">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-7018">TextureCube</span></span> | \- |
| <span data-ttu-id="80490-7019">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-7019">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7021">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-7021">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7023">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-7023">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-7024">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-7024">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-7025">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-7025">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7027">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-7027">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-7028">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-7028">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7030">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-7030">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-7031">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-7031">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7032">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-7032">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7033">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-7033">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-7034">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-7034">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-7035">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-7035">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-7036">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-7036">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-7037">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-7037">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7039">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7039">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7041">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7041">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-7042">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7042">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-7043">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-7043">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-7044">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-7044">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-7045">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7045">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-7046">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-7046">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-7047">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-7047">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-7048">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-7048">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7050">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-7050">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7051">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-7051">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7052">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-7052">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-7053">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-7053">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-7054">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-7054">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-7055">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-7055">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-7056">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-7056">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="80490-7057">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7057">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-7059">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7059">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-7061">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7061">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-7063">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-7063">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7065">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-7065">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-7066">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-7066">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="80490-7067">DXGI_FORMAT_NV12<sup>V</sup> (103)</span><span class="sxs-lookup"><span data-stu-id="80490-7067">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="80490-7068">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-7068">Target</span></span> | <span data-ttu-id="80490-7069">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-7069">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-7070">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-7070">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-7071">8</span><span class="sxs-lookup"><span data-stu-id="80490-7071">8</span></span> |
| <span data-ttu-id="80490-7072">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-7072">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7074">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-7074">Buffer</span></span> | \- |
| <span data-ttu-id="80490-7075">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-7075">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-7076">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-7076">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-7077">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-7077">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-7078">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-7078">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-7079">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-7079">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7081">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-7081">Texture3D</span></span> | \- |
| <span data-ttu-id="80490-7082">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-7082">TextureCube</span></span> | \- |
| <span data-ttu-id="80490-7083">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-7083">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7085">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-7085">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7087">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-7087">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-7088">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-7088">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-7089">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-7089">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7091">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-7091">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-7092">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-7092">Mipmap</span></span> | \- |
| <span data-ttu-id="80490-7093">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-7093">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-7094">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-7094">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7096">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-7096">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7098">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-7098">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-7099">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-7099">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-7100">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-7100">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-7101">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-7101">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-7102">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-7102">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7104">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7104">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7106">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7106">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-7107">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7107">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-7108">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-7108">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-7109">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-7109">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-7110">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7110">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-7111">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-7111">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-7112">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-7112">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-7113">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-7113">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7115">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-7115">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7116">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-7116">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7117">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-7117">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-7118">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-7118">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-7119">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-7119">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-7120">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-7120">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-7121">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-7121">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="80490-7122">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7122">Video Decoder Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7124">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7124">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7126">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7126">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7128">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-7128">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7130">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-7130">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-7131">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-7131">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="80490-7132">DXGI_FORMAT_P010<sup>V</sup> (104)</span><span class="sxs-lookup"><span data-stu-id="80490-7132">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="80490-7133">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-7133">Target</span></span> | <span data-ttu-id="80490-7134">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-7134">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-7135">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-7135">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-7136">16</span><span class="sxs-lookup"><span data-stu-id="80490-7136">16</span></span> |
| <span data-ttu-id="80490-7137">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-7137">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-7139">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-7139">Buffer</span></span> | \- |
| <span data-ttu-id="80490-7140">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-7140">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-7141">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-7141">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-7142">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-7142">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-7143">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-7143">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-7144">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-7144">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7146">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-7146">Texture3D</span></span> | \- |
| <span data-ttu-id="80490-7147">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-7147">TextureCube</span></span> | \- |
| <span data-ttu-id="80490-7148">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-7148">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7150">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-7150">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7152">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-7152">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-7153">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-7153">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-7154">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-7154">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7156">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-7156">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-7157">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-7157">Mipmap</span></span> | \- |
| <span data-ttu-id="80490-7158">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-7158">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-7159">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-7159">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7161">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-7161">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7163">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-7163">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-7164">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-7164">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-7165">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-7165">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-7166">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-7166">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-7167">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-7167">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7169">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7169">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7171">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7171">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-7172">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7172">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-7173">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-7173">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-7174">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-7174">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-7175">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7175">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-7176">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-7176">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-7177">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-7177">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-7178">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-7178">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7180">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-7180">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7181">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-7181">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7182">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-7182">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-7183">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-7183">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-7184">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-7184">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-7185">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-7185">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-7186">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-7186">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="80490-7187">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7187">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-7189">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7189">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-7191">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7191">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-7193">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-7193">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7195">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-7195">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-7196">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-7196">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="80490-7197">DXGI_FORMAT_P016<sup>V</sup> (105)</span><span class="sxs-lookup"><span data-stu-id="80490-7197">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="80490-7198">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-7198">Target</span></span> | <span data-ttu-id="80490-7199">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-7199">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-7200">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-7200">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-7201">16</span><span class="sxs-lookup"><span data-stu-id="80490-7201">16</span></span> |
| <span data-ttu-id="80490-7202">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-7202">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-7204">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-7204">Buffer</span></span> | \- |
| <span data-ttu-id="80490-7205">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-7205">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-7206">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-7206">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-7207">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-7207">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-7208">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-7208">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-7209">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-7209">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7211">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-7211">Texture3D</span></span> | \- |
| <span data-ttu-id="80490-7212">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-7212">TextureCube</span></span> | \- |
| <span data-ttu-id="80490-7213">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-7213">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7215">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-7215">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7217">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-7217">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-7218">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-7218">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-7219">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-7219">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7221">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-7221">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-7222">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-7222">Mipmap</span></span> | \- |
| <span data-ttu-id="80490-7223">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-7223">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-7224">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-7224">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7226">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-7226">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7228">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-7228">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-7229">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-7229">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-7230">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-7230">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-7231">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-7231">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-7232">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-7232">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7234">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7234">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7236">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7236">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-7237">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7237">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-7238">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-7238">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-7239">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-7239">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-7240">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7240">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-7241">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-7241">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-7242">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-7242">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-7243">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-7243">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7245">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-7245">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7246">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-7246">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7247">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-7247">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-7248">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-7248">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-7249">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-7249">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-7250">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-7250">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-7251">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-7251">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="80490-7252">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7252">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-7254">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7254">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-7256">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7256">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-7258">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-7258">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7260">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-7260">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-7261">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-7261">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="80490-7262">DXGI_FORMAT_420_OPAQUE<sup>V</sup> (106)</span><span class="sxs-lookup"><span data-stu-id="80490-7262">DXGI_FORMAT_420_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="80490-7263">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-7263">Target</span></span> | <span data-ttu-id="80490-7264">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-7264">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-7265">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-7265">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-7266">8</span><span class="sxs-lookup"><span data-stu-id="80490-7266">8</span></span> |
| <span data-ttu-id="80490-7267">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-7267">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7269">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-7269">Buffer</span></span> | \- |
| <span data-ttu-id="80490-7270">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-7270">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-7271">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-7271">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-7272">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-7272">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-7273">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-7273">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-7274">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-7274">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7276">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-7276">Texture3D</span></span> | \- |
| <span data-ttu-id="80490-7277">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-7277">TextureCube</span></span> | \- |
| <span data-ttu-id="80490-7278">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-7278">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-7279">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-7279">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-7280">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-7280">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-7281">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-7281">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-7282">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-7282">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-7283">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-7283">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-7284">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-7284">Mipmap</span></span> | \- |
| <span data-ttu-id="80490-7285">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-7285">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-7286">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-7286">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7287">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-7287">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7288">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-7288">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-7289">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-7289">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-7290">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-7290">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-7291">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-7291">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-7292">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-7292">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-7293">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7293">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-7294">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7294">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-7295">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7295">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-7296">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-7296">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-7297">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-7297">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-7298">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7298">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-7299">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-7299">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-7300">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-7300">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-7301">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-7301">CPU Lockable</span></span> | \- |
| <span data-ttu-id="80490-7302">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-7302">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7303">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-7303">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7304">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-7304">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-7305">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-7305">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-7306">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-7306">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-7307">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-7307">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-7308">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-7308">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="80490-7309">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7309">Video Decoder Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7311">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7311">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7313">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7313">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7315">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-7315">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7317">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-7317">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-7318">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-7318">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="80490-7319">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span><span class="sxs-lookup"><span data-stu-id="80490-7319">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="80490-7320">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-7320">Target</span></span> | <span data-ttu-id="80490-7321">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-7321">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-7322">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-7322">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-7323">16</span><span class="sxs-lookup"><span data-stu-id="80490-7323">16</span></span> |
| <span data-ttu-id="80490-7324">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-7324">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7326">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-7326">Buffer</span></span> | \- |
| <span data-ttu-id="80490-7327">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-7327">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-7328">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-7328">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-7329">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-7329">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-7330">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-7330">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-7331">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-7331">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7333">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-7333">Texture3D</span></span> | \- |
| <span data-ttu-id="80490-7334">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-7334">TextureCube</span></span> | \- |
| <span data-ttu-id="80490-7335">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-7335">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7337">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-7337">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7339">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-7339">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-7340">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-7340">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-7341">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-7341">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7343">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-7343">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-7344">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-7344">Mipmap</span></span> | \- |
| <span data-ttu-id="80490-7345">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-7345">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-7346">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-7346">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7347">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-7347">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7348">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-7348">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-7349">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-7349">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-7350">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-7350">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-7351">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-7351">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-7352">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-7352">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7354">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7354">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7356">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7356">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-7357">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7357">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-7358">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-7358">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-7359">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-7359">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-7360">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7360">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-7361">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-7361">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-7362">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-7362">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-7363">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-7363">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7365">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-7365">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7366">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-7366">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7367">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-7367">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-7368">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-7368">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-7369">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-7369">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-7370">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-7370">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-7371">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-7371">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="80490-7372">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7372">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-7374">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7374">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7376">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7376">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-7378">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-7378">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7380">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-7380">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-7381">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-7381">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="80490-7382">DXGI_FORMAT_Y210<sup>V</sup> (108)</span><span class="sxs-lookup"><span data-stu-id="80490-7382">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="80490-7383">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-7383">Target</span></span> | <span data-ttu-id="80490-7384">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-7384">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-7385">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-7385">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-7386">32</span><span class="sxs-lookup"><span data-stu-id="80490-7386">32</span></span> |
| <span data-ttu-id="80490-7387">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-7387">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-7389">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-7389">Buffer</span></span> | \- |
| <span data-ttu-id="80490-7390">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-7390">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-7391">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-7391">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-7392">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-7392">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-7393">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-7393">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-7394">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-7394">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7396">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-7396">Texture3D</span></span> | \- |
| <span data-ttu-id="80490-7397">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-7397">TextureCube</span></span> | \- |
| <span data-ttu-id="80490-7398">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-7398">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7400">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-7400">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7402">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-7402">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-7403">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-7403">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-7404">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-7404">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7406">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-7406">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-7407">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-7407">Mipmap</span></span> | \- |
| <span data-ttu-id="80490-7408">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-7408">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-7409">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-7409">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7410">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-7410">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7411">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-7411">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-7412">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-7412">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-7413">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-7413">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-7414">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-7414">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-7415">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-7415">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7417">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7417">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7419">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7419">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-7420">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7420">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-7421">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-7421">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-7422">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-7422">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-7423">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7423">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-7424">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-7424">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-7425">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-7425">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-7426">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-7426">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7428">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-7428">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7429">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-7429">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7430">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-7430">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-7431">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-7431">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-7432">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-7432">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-7433">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-7433">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-7434">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-7434">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="80490-7435">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7435">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-7437">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7437">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-7439">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7439">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-7441">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-7441">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7443">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-7443">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-7444">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-7444">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="80490-7445">DXGI_FORMAT_Y216<sup>V</sup> (109)</span><span class="sxs-lookup"><span data-stu-id="80490-7445">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="80490-7446">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-7446">Target</span></span> | <span data-ttu-id="80490-7447">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-7447">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-7448">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-7448">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-7449">32</span><span class="sxs-lookup"><span data-stu-id="80490-7449">32</span></span> |
| <span data-ttu-id="80490-7450">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-7450">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-7452">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-7452">Buffer</span></span> | \- |
| <span data-ttu-id="80490-7453">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-7453">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-7454">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-7454">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-7455">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-7455">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-7456">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-7456">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-7457">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-7457">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7459">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-7459">Texture3D</span></span> | \- |
| <span data-ttu-id="80490-7460">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-7460">TextureCube</span></span> | \- |
| <span data-ttu-id="80490-7461">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-7461">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7463">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-7463">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7465">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-7465">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-7466">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-7466">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-7467">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-7467">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7469">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-7469">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-7470">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-7470">Mipmap</span></span> | \- |
| <span data-ttu-id="80490-7471">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-7471">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-7472">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-7472">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7473">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-7473">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7474">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-7474">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-7475">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-7475">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-7476">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-7476">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-7477">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-7477">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-7478">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-7478">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7480">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7480">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7482">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7482">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-7483">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7483">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-7484">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-7484">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-7485">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-7485">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-7486">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7486">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-7487">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-7487">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-7488">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-7488">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-7489">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-7489">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7491">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-7491">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7492">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-7492">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7493">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-7493">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-7494">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-7494">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-7495">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-7495">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-7496">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-7496">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-7497">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-7497">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="80490-7498">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7498">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-7500">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7500">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-7502">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7502">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-7504">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-7504">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7506">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-7506">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-7507">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-7507">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="80490-7508">DXGI_FORMAT_NV11<sup>V</sup> (110)</span><span class="sxs-lookup"><span data-stu-id="80490-7508">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="80490-7509">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-7509">Target</span></span> | <span data-ttu-id="80490-7510">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-7510">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-7511">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-7511">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-7512">8</span><span class="sxs-lookup"><span data-stu-id="80490-7512">8</span></span> |
| <span data-ttu-id="80490-7513">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-7513">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-7515">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-7515">Buffer</span></span> | \- |
| <span data-ttu-id="80490-7516">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-7516">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-7517">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-7517">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-7518">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-7518">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-7519">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-7519">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-7520">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-7520">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7522">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-7522">Texture3D</span></span> | \- |
| <span data-ttu-id="80490-7523">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-7523">TextureCube</span></span> | \- |
| <span data-ttu-id="80490-7524">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-7524">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7526">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-7526">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7528">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-7528">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-7529">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-7529">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-7530">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-7530">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7532">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-7532">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-7533">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-7533">Mipmap</span></span> | \- |
| <span data-ttu-id="80490-7534">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-7534">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-7535">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-7535">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7537">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-7537">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7539">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-7539">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-7540">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-7540">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-7541">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-7541">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-7542">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-7542">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-7543">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-7543">Typed UAV</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7545">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7545">UAV Typed Store</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7547">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7547">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-7548">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7548">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-7549">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-7549">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-7550">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-7550">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-7551">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7551">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-7552">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-7552">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-7553">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-7553">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-7554">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-7554">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7556">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-7556">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7557">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-7557">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7558">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-7558">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-7559">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-7559">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-7560">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-7560">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-7561">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-7561">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-7562">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-7562">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="80490-7563">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7563">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-7565">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7565">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-7567">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7567">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-7569">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-7569">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7571">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-7571">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-7572">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-7572">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="80490-7573">DXGI_FORMAT_AI44<sup>V</sup> (111)</span><span class="sxs-lookup"><span data-stu-id="80490-7573">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="80490-7574">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-7574">Target</span></span> | <span data-ttu-id="80490-7575">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-7575">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-7576">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-7576">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-7577">8</span><span class="sxs-lookup"><span data-stu-id="80490-7577">8</span></span> |
| <span data-ttu-id="80490-7578">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-7578">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-7580">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-7580">Buffer</span></span> | \- |
| <span data-ttu-id="80490-7581">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-7581">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-7582">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-7582">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-7583">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-7583">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-7584">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-7584">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-7585">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-7585">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7587">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-7587">Texture3D</span></span> | \- |
| <span data-ttu-id="80490-7588">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-7588">TextureCube</span></span> | \- |
| <span data-ttu-id="80490-7589">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-7589">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-7590">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-7590">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-7591">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-7591">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-7592">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-7592">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-7593">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-7593">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-7594">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-7594">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-7595">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-7595">Mipmap</span></span> | \- |
| <span data-ttu-id="80490-7596">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-7596">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-7597">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-7597">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7598">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-7598">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7599">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-7599">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-7600">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-7600">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-7601">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-7601">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-7602">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-7602">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-7603">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-7603">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-7604">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7604">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-7605">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7605">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-7606">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7606">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-7607">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-7607">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-7608">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-7608">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-7609">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7609">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-7610">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-7610">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-7611">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-7611">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-7612">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-7612">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7614">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-7614">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7615">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-7615">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7616">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-7616">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-7617">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-7617">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-7618">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-7618">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-7619">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-7619">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-7620">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-7620">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="80490-7621">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7621">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-7622">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7622">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7624">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7624">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-7625">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-7625">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-7626">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-7626">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-7627">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-7627">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="80490-7628">DXGI_FORMAT_IA44<sup>V</sup> (112)</span><span class="sxs-lookup"><span data-stu-id="80490-7628">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="80490-7629">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-7629">Target</span></span> | <span data-ttu-id="80490-7630">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-7630">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-7631">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-7631">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-7632">8</span><span class="sxs-lookup"><span data-stu-id="80490-7632">8</span></span> |
| <span data-ttu-id="80490-7633">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-7633">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-7635">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-7635">Buffer</span></span> | \- |
| <span data-ttu-id="80490-7636">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-7636">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-7637">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-7637">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-7638">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-7638">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-7639">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-7639">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-7640">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-7640">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7642">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-7642">Texture3D</span></span> | \- |
| <span data-ttu-id="80490-7643">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-7643">TextureCube</span></span> | \- |
| <span data-ttu-id="80490-7644">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-7644">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-7645">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-7645">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-7646">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-7646">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-7647">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-7647">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-7648">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-7648">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-7649">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-7649">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-7650">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-7650">Mipmap</span></span> | \- |
| <span data-ttu-id="80490-7651">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-7651">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-7652">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-7652">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7653">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-7653">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7654">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-7654">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-7655">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-7655">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-7656">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-7656">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-7657">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-7657">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-7658">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-7658">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-7659">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7659">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-7660">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7660">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-7661">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7661">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-7662">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-7662">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-7663">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-7663">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-7664">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7664">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-7665">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-7665">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-7666">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-7666">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-7667">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-7667">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7669">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-7669">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7670">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-7670">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7671">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-7671">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-7672">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-7672">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-7673">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-7673">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-7674">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-7674">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-7675">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-7675">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="80490-7676">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7676">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-7677">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7677">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7679">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7679">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-7680">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-7680">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-7681">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-7681">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-7682">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-7682">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="80490-7683">DXGI_FORMAT_P8<sup>V</sup> (113)</span><span class="sxs-lookup"><span data-stu-id="80490-7683">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="80490-7684">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-7684">Target</span></span> | <span data-ttu-id="80490-7685">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-7685">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-7686">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-7686">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-7687">8</span><span class="sxs-lookup"><span data-stu-id="80490-7687">8</span></span> |
| <span data-ttu-id="80490-7688">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-7688">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-7690">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-7690">Buffer</span></span> | \- |
| <span data-ttu-id="80490-7691">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-7691">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-7692">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-7692">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-7693">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-7693">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-7694">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-7694">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-7695">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-7695">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7697">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-7697">Texture3D</span></span> | \- |
| <span data-ttu-id="80490-7698">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-7698">TextureCube</span></span> | \- |
| <span data-ttu-id="80490-7699">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-7699">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-7700">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-7700">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-7701">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-7701">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-7702">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-7702">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-7703">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-7703">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-7704">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-7704">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-7705">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-7705">Mipmap</span></span> | \- |
| <span data-ttu-id="80490-7706">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-7706">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-7707">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-7707">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7708">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-7708">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7709">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-7709">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-7710">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-7710">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-7711">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-7711">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-7712">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-7712">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-7713">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-7713">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-7714">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7714">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-7715">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7715">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-7716">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7716">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-7717">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-7717">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-7718">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-7718">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-7719">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7719">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-7720">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-7720">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-7721">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-7721">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-7722">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-7722">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7724">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-7724">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7725">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-7725">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7726">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-7726">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-7727">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-7727">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-7728">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-7728">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-7729">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-7729">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-7730">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-7730">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="80490-7731">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7731">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-7732">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7732">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7734">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7734">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-7735">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-7735">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-7736">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-7736">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-7737">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-7737">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="80490-7738">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span><span class="sxs-lookup"><span data-stu-id="80490-7738">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="80490-7739">Destino</span><span class="sxs-lookup"><span data-stu-id="80490-7739">Target</span></span> | <span data-ttu-id="80490-7740">Suporte</span><span class="sxs-lookup"><span data-stu-id="80490-7740">Support</span></span> |
| - | - |
| <span data-ttu-id="80490-7741">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="80490-7741">Bits Per Element (BPE)</span></span> | <span data-ttu-id="80490-7742">16</span><span class="sxs-lookup"><span data-stu-id="80490-7742">16</span></span> |
| <span data-ttu-id="80490-7743">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="80490-7743">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="80490-7745">Buffer</span><span class="sxs-lookup"><span data-stu-id="80490-7745">Buffer</span></span> | \- |
| <span data-ttu-id="80490-7746">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-7746">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="80490-7747">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="80490-7747">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="80490-7748">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80490-7748">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="80490-7749">Texture1D</span><span class="sxs-lookup"><span data-stu-id="80490-7749">Texture1D</span></span> | \- |
| <span data-ttu-id="80490-7750">Texture2D</span><span class="sxs-lookup"><span data-stu-id="80490-7750">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7752">Texture3D</span><span class="sxs-lookup"><span data-stu-id="80490-7752">Texture3D</span></span> | \- |
| <span data-ttu-id="80490-7753">TextureCube</span><span class="sxs-lookup"><span data-stu-id="80490-7753">TextureCube</span></span> | \- |
| <span data-ttu-id="80490-7754">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="80490-7754">Shader ld</span></span> | \- |
| <span data-ttu-id="80490-7755">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="80490-7755">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="80490-7756">Sample_c do sombreador (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="80490-7756">Shader sample_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="80490-7757">Exemplo de sombreador (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="80490-7757">Shader sample (mono 1_bit_filter)</span></span> | \- |
| <span data-ttu-id="80490-7758">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-7758">Shader gather4</span></span> | \- |
| <span data-ttu-id="80490-7759">Gather4_c do sombreador</span><span class="sxs-lookup"><span data-stu-id="80490-7759">Shader gather4_c</span></span> | \- |
| <span data-ttu-id="80490-7760">Mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-7760">Mipmap</span></span> | \- |
| <span data-ttu-id="80490-7761">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="80490-7761">Mipmap Auto- Generation</span></span> | \- |
| <span data-ttu-id="80490-7762">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-7762">RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7763">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="80490-7763">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7764">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="80490-7764">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="80490-7765">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="80490-7765">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="80490-7766">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="80490-7766">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-7767">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="80490-7767">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="80490-7768">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="80490-7768">Typed UAV</span></span> | \- |
| <span data-ttu-id="80490-7769">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7769">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="80490-7770">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7770">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="80490-7771">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7771">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="80490-7772">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="80490-7772">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="80490-7773">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="80490-7773">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="80490-7774">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="80490-7774">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="80490-7775">Mínimo de UAV assinado por Atomic/Max</span><span class="sxs-lookup"><span data-stu-id="80490-7775">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="80490-7776">UAV atômico sem sinal mínimo/máximo</span><span class="sxs-lookup"><span data-stu-id="80490-7776">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="80490-7777">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="80490-7777">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7779">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="80490-7779">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7780">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="80490-7780">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="80490-7781">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="80490-7781">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="80490-7782">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="80490-7782">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="80490-7783">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="80490-7783">Multisample Load</span></span> | \- |
| <span data-ttu-id="80490-7784">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="80490-7784">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="80490-7785">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="80490-7785">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="80490-7786">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7786">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="80490-7787">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7787">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="80490-7789">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7789">Video Processor Output</span></span> | \- |
| <span data-ttu-id="80490-7790">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="80490-7790">Shared Resource</span></span> | \- |
| <span data-ttu-id="80490-7791">BackBuffer convertida até mesmo totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="80490-7791">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="80490-7792">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="80490-7792">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="80490-7793">Observações de formato</span><span class="sxs-lookup"><span data-stu-id="80490-7793">Format notes</span></span>

<span data-ttu-id="80490-7794">A finalidade do formato pode mudar de um nível de recurso de hardware para o próximo.</span><span class="sxs-lookup"><span data-stu-id="80490-7794">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="80490-7795"><sup>L</sup> : formato de tipo informativo</span><span class="sxs-lookup"><span data-stu-id="80490-7795"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="80490-7796"><sup>PCs</sup> : layout de tipo parcial, convertido e simples</span><span class="sxs-lookup"><span data-stu-id="80490-7796"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="80490-7797"><sup>FCS</sup> : layout totalmente tipado, convertido e simples</span><span class="sxs-lookup"><span data-stu-id="80490-7797"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="80490-7798"><sup>FNS</sup> : layout totalmente tipado, não-convertido e simples</span><span class="sxs-lookup"><span data-stu-id="80490-7798"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="80490-7799"><sup>PCC</sup> : layout complexo, convertido e de tipo parcial</span><span class="sxs-lookup"><span data-stu-id="80490-7799"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="80490-7800"><sup>FCC</sup> : layout totalmente tipado, convertido e complexo</span><span class="sxs-lookup"><span data-stu-id="80490-7800"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="80490-7801"><sup>FNC</sup> : layout totalmente tipado, não-convertido e complexo</span><span class="sxs-lookup"><span data-stu-id="80490-7801"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="80490-7802"><sup>V</sup> : formato de vídeo</span><span class="sxs-lookup"><span data-stu-id="80490-7802"><sup>V</sup> : video format</span></span>
</dt> </dl>

## <a name="dxgi_format_related-topics"></a><span data-ttu-id="80490-7803">Tópicos de DXGI_FORMAT_Related</span><span class="sxs-lookup"><span data-stu-id="80490-7803">DXGI_FORMAT_Related topics</span></span>

[<span data-ttu-id="80490-7804">Níveis de recursos de hardware do D3D12</span><span class="sxs-lookup"><span data-stu-id="80490-7804">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

[<span data-ttu-id="80490-7805">Guia de programação para DXGI</span><span class="sxs-lookup"><span data-stu-id="80490-7805">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
