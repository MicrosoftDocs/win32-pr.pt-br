---
description: Esta seção especifica os formatos ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valores) que têm suporte no hardware do nível de recurso do Direct3D 10,1.
ms.assetid: 2C7E16D7-EEF0-4EA7-A819-5274C9105F68
title: Suporte de formato para hardware 10.1 do Nível de Recursos do Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5edb5c81ef0a99bc14031a9a7a505736e91e13d8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456518"
---
# <a name="format-support-for-direct3d-feature-level-101-hardware"></a><span data-ttu-id="a1cc3-103">Suporte de formato para hardware 10.1 do Nível de Recursos do Direct3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-103">Format support for Direct3D Feature Level 10.1 hardware</span></span>

<span data-ttu-id="a1cc3-104">Esta seção especifica os formatos ([_\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valores) que têm suporte no hardware do nível de recurso do Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="a1cc3-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature Level 10.1 hardware.</span></span>

<span data-ttu-id="a1cc3-105">A tabela resume o suporte a recursos, usando a chave a seguir.</span><span class="sxs-lookup"><span data-stu-id="a1cc3-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="a1cc3-106">Símbolo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-106">Symbol</span></span>                            | <span data-ttu-id="a1cc3-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a1cc3-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="a1cc3-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="a1cc3-108">_ *-*\*</span></span>                             | <span data-ttu-id="a1cc3-109">Não permitido ou não disponível.</span><span class="sxs-lookup"><span data-stu-id="a1cc3-109">Disallowed or not available.</span></span>                                                  |
| ![exigido](images/letter-r.jpg)  | <span data-ttu-id="a1cc3-111">O suporte a hardware é necessário.</span><span class="sxs-lookup"><span data-stu-id="a1cc3-111">Hardware support is required.</span></span>                                                 |
| ![opcionais](images/letter-o.jpg)  | <span data-ttu-id="a1cc3-113">Suporte a hardware opcional, o formato pode ou não ser acelerado por hardware.</span><span class="sxs-lookup"><span data-stu-id="a1cc3-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![dependentes](images/letter-d.jpg) | <span data-ttu-id="a1cc3-115">Necessário se houver suporte para o recurso opcional relacionado.</span><span class="sxs-lookup"><span data-stu-id="a1cc3-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="a1cc3-116">Este tópico contém uma seção por formato.</span><span class="sxs-lookup"><span data-stu-id="a1cc3-116">This topic contains a section per format.</span></span> <span data-ttu-id="a1cc3-117">Um *destino* de formato (as tabelas contêm uma linha por destino) pode ser um tipo de recurso, uma função intrínseca HLSL ou uma funcionalidade específica que depende de um formato específico.</span><span class="sxs-lookup"><span data-stu-id="a1cc3-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="a1cc3-118">Para verificar programaticamente o suporte a Format em D3D11 e D3D12, consulte [verificando o suporte a recursos de hardware](checking-hardware-feature-support.md).</span><span class="sxs-lookup"><span data-stu-id="a1cc3-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="a1cc3-119">Os números dos formatos são principalmente, mas nem todos, em ordem numérica crescente &mdash; alguns estão fora de ordem numérica e listados junto com outros formatos relevantes.</span><span class="sxs-lookup"><span data-stu-id="a1cc3-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="a1cc3-120">Observe também que sem *tipo* em um nome de formato pode significar digitação *parcial* e não estritamente tipado (consulte a seção [observações de formato](#format-notes) no final do tópico).</span><span class="sxs-lookup"><span data-stu-id="a1cc3-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>

## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="a1cc3-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="a1cc3-122">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-122">Target</span></span> | <span data-ttu-id="a1cc3-123">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-123">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-124">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-125">0</span><span class="sxs-lookup"><span data-stu-id="a1cc3-125">0</span></span> |
| <span data-ttu-id="a1cc3-126">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-126">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-128">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-128">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-130">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-130">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-131">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-131">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-132">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-132">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-133">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-134">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-134">Texture2D</span></span> | \- |
| <span data-ttu-id="a1cc3-135">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-135">Texture3D</span></span> | \- |
| <span data-ttu-id="a1cc3-136">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-136">TextureCube</span></span> | \- |
| <span data-ttu-id="a1cc3-137">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-137">Shader ld</span></span> | \- |
| <span data-ttu-id="a1cc3-138">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-138">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-139">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-139">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-140">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-140">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-141">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-141">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-142">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-142">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-143">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-143">Mipmap</span></span> | \- |
| <span data-ttu-id="a1cc3-144">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-144">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-145">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-145">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-146">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-146">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-147">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-147">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-148">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-148">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-149">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-149">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-150">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-150">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-151">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-151">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-152">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-152">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-153">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-153">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-154">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-154">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-155">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-155">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-156">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-156">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-157">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-157">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-158">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-158">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-159">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-159">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-160">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-160">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-162">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-162">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-163">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-163">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-164">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-164">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-165">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-165">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-166">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-166">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-167">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-167">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-168">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-168">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a1cc3-169">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-169">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-170">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-170">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-171">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-171">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-172">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-172">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-173">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-173">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="a1cc3-174">DXGI_FORMAT_R32G32B32A32 \_ <sup>PCs</sup> não tipados (1)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-174">DXGI_FORMAT_R32G32B32A32\_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="a1cc3-175">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-175">Target</span></span> | <span data-ttu-id="a1cc3-176">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-176">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-177">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-177">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-178">128</span><span class="sxs-lookup"><span data-stu-id="a1cc3-178">128</span></span> |
| <span data-ttu-id="a1cc3-179">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-179">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-181">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-181">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-182">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-182">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-183">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-183">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-184">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-184">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-185">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-185">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-187">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-187">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-189">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-189">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-191">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-191">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-193">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-193">Shader ld</span></span> | \- |
| <span data-ttu-id="a1cc3-194">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-194">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-195">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-195">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-196">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-196">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-197">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-197">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-198">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-198">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-199">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-199">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-201">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-201">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-202">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-202">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-203">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-203">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-204">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-204">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-205">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-205">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-206">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-206">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-207">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-207">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-208">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-208">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-209">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-209">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-210">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-210">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-211">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-211">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-212">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-212">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-213">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-213">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-214">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-214">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-215">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-215">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-216">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-216">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-217">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-217">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-219">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-219">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-220">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-220">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-221">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-221">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-222">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-222">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-223">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-223">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-224">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-224">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-225">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-225">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-227">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-227">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-228">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-228">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-229">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-229">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-230">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-230">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-232">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-232">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfcssup-2"></a><span data-ttu-id="a1cc3-233">\_<sup>FCS</sup> de DXGI_FORMAT_R32G32B32A32 float (2)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-233">DXGI_FORMAT_R32G32B32A32\_FLOAT<sup>FCS</sup> (2)</span></span>
| <span data-ttu-id="a1cc3-234">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-234">Target</span></span> | <span data-ttu-id="a1cc3-235">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-235">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-236">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-236">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-237">128</span><span class="sxs-lookup"><span data-stu-id="a1cc3-237">128</span></span> |
| <span data-ttu-id="a1cc3-238">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-238">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-240">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-240">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-242">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-242">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-244">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-244">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-245">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-245">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-247">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-247">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-249">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-249">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-251">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-251">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-253">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-253">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-255">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-255">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-257">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-257">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-259">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-259">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-260">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-260">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-261">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-261">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-262">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-262">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-263">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-263">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-265">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-265">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-267">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-267">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-269">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-269">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-271">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-271">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-272">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-272">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-273">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-273">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-274">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-274">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-275">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-275">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-276">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-276">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-277">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-277">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-278">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-278">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-279">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-279">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-280">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-280">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-281">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-281">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-282">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-282">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-283">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-283">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-284">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-284">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-286">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-286">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-288">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-288">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-290">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-290">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-292">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-292">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-294">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-294">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-296">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-296">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-297">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-297">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-299">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-299">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-300">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-300">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-301">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-301">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-302">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-302">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-304">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-304">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfcssup-3"></a><span data-ttu-id="a1cc3-305">\_<sup>FCS</sup> DXGI_FORMAT_R32G32B32A32 uint (3)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-305">DXGI_FORMAT_R32G32B32A32\_UINT<sup>FCS</sup> (3)</span></span>
| <span data-ttu-id="a1cc3-306">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-306">Target</span></span> | <span data-ttu-id="a1cc3-307">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-307">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-308">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-308">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-309">128</span><span class="sxs-lookup"><span data-stu-id="a1cc3-309">128</span></span> |
| <span data-ttu-id="a1cc3-310">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-310">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-312">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-312">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-314">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-314">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-316">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-316">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-317">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-317">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-319">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-319">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-321">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-321">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-323">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-323">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-325">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-325">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-327">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-327">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-329">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-329">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-330">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-330">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-331">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-331">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-332">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-332">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-333">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-333">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-334">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-334">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-336">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-336">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-337">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-337">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-339">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-339">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-340">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-340">Output Merger Logic Op</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-342">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-342">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-343">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-343">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-344">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-344">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-345">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-345">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-346">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-346">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-347">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-347">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-348">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-348">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-349">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-349">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-350">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-350">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-351">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-351">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-352">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-352">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-353">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-353">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-354">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-354">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-356">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-356">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-358">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-358">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-360">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-360">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-362">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-362">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-363">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-363">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-365">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-365">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-366">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-366">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-368">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-368">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-369">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-369">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-370">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-370">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-371">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-371">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-373">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-373">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfcssup-4"></a><span data-ttu-id="a1cc3-374">DXGI_FORMAT_R32G32B32A32 \_ Santo<sup>FCS</sup> (4)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-374">DXGI_FORMAT_R32G32B32A32\_SINT<sup>FCS</sup> (4)</span></span>
| <span data-ttu-id="a1cc3-375">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-375">Target</span></span> | <span data-ttu-id="a1cc3-376">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-376">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-377">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-377">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-378">128</span><span class="sxs-lookup"><span data-stu-id="a1cc3-378">128</span></span> |
| <span data-ttu-id="a1cc3-379">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-379">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-381">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-381">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-383">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-383">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-385">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-385">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-386">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-386">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-388">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-388">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-390">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-390">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-392">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-392">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-394">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-394">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-396">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-396">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-398">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-398">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-399">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-399">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-400">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-400">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-401">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-401">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-402">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-402">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-403">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-403">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-405">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-405">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-406">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-406">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-408">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-408">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-409">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-409">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-410">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-410">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-411">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-411">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-412">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-412">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-413">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-413">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-414">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-414">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-415">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-415">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-416">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-416">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-417">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-417">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-418">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-418">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-419">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-419">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-420">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-420">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-421">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-421">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-422">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-422">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-424">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-424">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-426">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-426">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-428">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-428">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-430">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-430">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-431">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-431">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-433">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-433">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-434">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-434">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-436">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-436">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-437">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-437">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-438">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-438">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-439">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-439">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-441">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-441">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="a1cc3-442">DXGI_FORMAT_R32G32B32 \_ <sup>PCs</sup> não tipados (5)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-442">DXGI_FORMAT_R32G32B32\_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="a1cc3-443">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-443">Target</span></span> | <span data-ttu-id="a1cc3-444">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-444">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-445">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-445">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-446">96</span><span class="sxs-lookup"><span data-stu-id="a1cc3-446">96</span></span> |
| <span data-ttu-id="a1cc3-447">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-447">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-449">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-449">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-450">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-450">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-451">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-451">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-452">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-452">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-453">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-453">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-455">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-455">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-457">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-457">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-459">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-459">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-461">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-461">Shader ld</span></span> | \- |
| <span data-ttu-id="a1cc3-462">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-462">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-463">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-463">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-464">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-464">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-465">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-465">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-466">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-466">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-467">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-467">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-469">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-469">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-470">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-470">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-471">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-471">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-472">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-472">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-473">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-473">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-474">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-474">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-475">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-475">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-476">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-476">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-477">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-477">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-478">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-478">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-479">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-479">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-480">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-480">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-481">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-481">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-482">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-482">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-483">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-483">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-484">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-484">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-485">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-485">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-487">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-487">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-488">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-488">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-489">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-489">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-490">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-490">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-491">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-491">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-492">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-492">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-493">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-493">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-495">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-495">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-496">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-496">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-497">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-497">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-498">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-498">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-499">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-499">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfcssup-6"></a><span data-ttu-id="a1cc3-500">\_<sup>FCS</sup> de DXGI_FORMAT_R32G32B32 float (6)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-500">DXGI_FORMAT_R32G32B32\_FLOAT<sup>FCS</sup> (6)</span></span>
| <span data-ttu-id="a1cc3-501">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-501">Target</span></span> | <span data-ttu-id="a1cc3-502">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-502">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-503">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-503">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-504">96</span><span class="sxs-lookup"><span data-stu-id="a1cc3-504">96</span></span> |
| <span data-ttu-id="a1cc3-505">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-505">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-507">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-507">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-509">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-509">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-511">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-511">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-512">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-512">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-514">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-514">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-516">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-516">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-518">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-518">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-520">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-520">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-522">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-522">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-524">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-524">Shader sample (any filter)</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-526">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-526">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-527">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-527">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-528">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-528">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-529">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-529">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-530">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-530">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-532">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-532">Mipmap Auto-Generation</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-534">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-534">RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-536">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-536">Blendable RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="a1cc3-538">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-538">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-539">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-539">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-540">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-540">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-541">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-541">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-542">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-542">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-543">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-543">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-544">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-544">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-545">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-545">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-546">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-546">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-547">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-547">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-548">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-548">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-549">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-549">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-550">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-550">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-551">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-551">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-553">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-553">4x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="a1cc3-555">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-555">8x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="a1cc3-557">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-557">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-559">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-559">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-561">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-561">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-563">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-563">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-564">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-564">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-566">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-566">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-567">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-567">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-568">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-568">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-569">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-569">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-570">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-570">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfcssup-7"></a><span data-ttu-id="a1cc3-571">\_<sup>FCS</sup> DXGI_FORMAT_R32G32B32 uint (7)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-571">DXGI_FORMAT_R32G32B32\_UINT<sup>FCS</sup> (7)</span></span>
| <span data-ttu-id="a1cc3-572">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-572">Target</span></span> | <span data-ttu-id="a1cc3-573">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-573">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-574">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-574">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-575">96</span><span class="sxs-lookup"><span data-stu-id="a1cc3-575">96</span></span> |
| <span data-ttu-id="a1cc3-576">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-576">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-578">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-578">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-580">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-580">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-582">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-582">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-583">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-583">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-585">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-585">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-587">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-587">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-589">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-589">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-591">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-591">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-593">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-593">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-595">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-595">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-596">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-596">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-597">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-597">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-598">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-598">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-599">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-599">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-600">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-600">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-602">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-602">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-603">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-603">RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-605">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-605">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-606">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-606">Output Merger Logic Op</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-608">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-608">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-609">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-609">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-610">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-610">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-611">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-611">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-612">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-612">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-613">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-613">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-614">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-614">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-615">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-615">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-616">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-616">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-617">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-617">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-618">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-618">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-619">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-619">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-620">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-620">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-622">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-622">4x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="a1cc3-624">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-624">8x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="a1cc3-626">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-626">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-628">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-628">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-629">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-629">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-631">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-631">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-632">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-632">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-634">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-634">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-635">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-635">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-636">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-636">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-637">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-637">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-638">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-638">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfcssup-8"></a><span data-ttu-id="a1cc3-639">DXGI_FORMAT_R32G32B32 \_ Santo<sup>FCS</sup> (8)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-639">DXGI_FORMAT_R32G32B32\_SINT<sup>FCS</sup> (8)</span></span>
| <span data-ttu-id="a1cc3-640">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-640">Target</span></span> | <span data-ttu-id="a1cc3-641">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-641">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-642">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-642">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-643">96</span><span class="sxs-lookup"><span data-stu-id="a1cc3-643">96</span></span> |
| <span data-ttu-id="a1cc3-644">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-644">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-646">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-646">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-648">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-648">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-650">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-650">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-651">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-651">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-653">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-653">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-655">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-655">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-657">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-657">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-659">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-659">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-661">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-661">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-663">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-663">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-664">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-664">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-665">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-665">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-666">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-666">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-667">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-667">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-668">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-668">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-670">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-670">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-671">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-671">RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-673">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-673">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-674">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-674">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-675">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-675">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-676">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-676">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-677">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-677">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-678">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-678">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-679">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-679">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-680">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-680">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-681">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-681">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-682">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-682">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-683">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-683">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-684">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-684">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-685">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-685">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-686">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-686">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-687">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-687">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-689">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-689">4x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="a1cc3-691">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-691">8x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="a1cc3-693">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-693">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-695">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-695">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-696">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-696">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-698">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-698">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-699">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-699">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-701">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-701">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-702">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-702">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-703">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-703">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-704">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-704">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-705">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-705">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="a1cc3-706">DXGI_FORMAT_R16G16B16A16 \_ <sup>PCs</sup> não tipados (9)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-706">DXGI_FORMAT_R16G16B16A16\_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="a1cc3-707">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-707">Target</span></span> | <span data-ttu-id="a1cc3-708">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-708">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-709">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-709">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-710">64</span><span class="sxs-lookup"><span data-stu-id="a1cc3-710">64</span></span> |
| <span data-ttu-id="a1cc3-711">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-711">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-713">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-713">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-714">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-714">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-715">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-715">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-716">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-716">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-717">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-717">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-719">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-719">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-721">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-721">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-723">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-723">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-725">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-725">Shader ld</span></span> | \- |
| <span data-ttu-id="a1cc3-726">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-726">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-727">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-727">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-728">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-728">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-729">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-729">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-730">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-730">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-731">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-731">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-733">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-733">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-734">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-734">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-735">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-735">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-736">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-736">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-737">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-737">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-738">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-738">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-739">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-739">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-740">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-740">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-741">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-741">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-742">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-742">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-743">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-743">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-744">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-744">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-745">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-745">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-746">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-746">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-747">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-747">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-748">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-748">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-749">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-749">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-751">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-751">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-752">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-752">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-753">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-753">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-754">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-754">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-755">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-755">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-756">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-756">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-757">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-757">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-759">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-759">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-760">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-760">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-761">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-761">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-762">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-762">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-764">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-764">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfcssup-10"></a><span data-ttu-id="a1cc3-765">\_<sup>FCS</sup> de DXGI_FORMAT_R16G16B16A16 float (10)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-765">DXGI_FORMAT_R16G16B16A16\_FLOAT<sup>FCS</sup> (10)</span></span>
| <span data-ttu-id="a1cc3-766">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-766">Target</span></span> | <span data-ttu-id="a1cc3-767">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-767">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-768">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-768">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-769">64</span><span class="sxs-lookup"><span data-stu-id="a1cc3-769">64</span></span> |
| <span data-ttu-id="a1cc3-770">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-770">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-772">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-772">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-774">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-774">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-776">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-776">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-777">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-777">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-778">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-778">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-780">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-780">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-782">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-782">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-784">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-784">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-786">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-786">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-788">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-788">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-790">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-790">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-791">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-791">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-792">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-792">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-793">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-793">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-794">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-794">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-796">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-796">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-798">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-798">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-800">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-800">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-802">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-802">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-803">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-803">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-804">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-804">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-805">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-805">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-806">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-806">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-807">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-807">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-808">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-808">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-809">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-809">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-810">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-810">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-811">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-811">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-812">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-812">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-813">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-813">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-814">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-814">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-815">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-815">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-817">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-817">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-819">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-819">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-821">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-821">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-823">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-823">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-825">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-825">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-827">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-827">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-829">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-829">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-831">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-831">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-832">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-832">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-834">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-834">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-836">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-836">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-838">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-838">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfcssup-11"></a><span data-ttu-id="a1cc3-839">\_<sup>FCS</sup> DXGI_FORMAT_R16G16B16A16 UNORM (11)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-839">DXGI_FORMAT_R16G16B16A16\_UNORM<sup>FCS</sup> (11)</span></span>
| <span data-ttu-id="a1cc3-840">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-840">Target</span></span> | <span data-ttu-id="a1cc3-841">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-841">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-842">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-842">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-843">64</span><span class="sxs-lookup"><span data-stu-id="a1cc3-843">64</span></span> |
| <span data-ttu-id="a1cc3-844">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-844">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-846">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-846">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-848">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-848">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-850">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-850">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-851">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-851">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-852">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-852">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-854">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-854">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-856">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-856">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-858">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-858">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-860">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-860">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-862">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-862">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-864">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-864">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-865">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-865">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-866">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-866">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-867">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-867">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-868">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-868">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-870">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-870">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-872">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-872">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-874">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-874">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-876">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-876">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-877">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-877">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-878">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-878">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-879">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-879">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-880">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-880">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-881">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-881">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-882">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-882">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-883">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-883">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-884">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-884">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-885">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-885">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-886">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-886">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-887">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-887">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-888">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-888">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-889">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-889">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-891">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-891">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-893">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-893">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-895">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-895">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-897">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-897">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-899">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-899">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-901">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-901">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-902">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-902">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-904">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-904">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-905">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-905">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-906">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-906">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-907">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-907">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-909">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-909">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfcssup-12"></a><span data-ttu-id="a1cc3-910">\_<sup>FCS</sup> DXGI_FORMAT_R16G16B16A16 uint (12)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-910">DXGI_FORMAT_R16G16B16A16\_UINT<sup>FCS</sup> (12)</span></span>
| <span data-ttu-id="a1cc3-911">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-911">Target</span></span> | <span data-ttu-id="a1cc3-912">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-912">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-913">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-913">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-914">64</span><span class="sxs-lookup"><span data-stu-id="a1cc3-914">64</span></span> |
| <span data-ttu-id="a1cc3-915">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-915">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-917">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-917">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-919">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-919">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-921">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-921">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-922">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-922">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-923">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-923">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-925">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-925">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-927">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-927">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-929">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-929">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-931">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-931">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-933">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-933">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-934">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-934">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-935">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-935">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-936">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-936">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-937">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-937">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-938">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-938">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-940">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-940">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-941">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-941">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-943">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-943">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-944">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-944">Output Merger Logic Op</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-946">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-946">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-947">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-947">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-948">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-948">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-949">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-949">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-950">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-950">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-951">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-951">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-952">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-952">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-953">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-953">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-954">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-954">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-955">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-955">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-956">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-956">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-957">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-957">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-958">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-958">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-960">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-960">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-962">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-962">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-964">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-964">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-966">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-966">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-967">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-967">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-969">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-969">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-970">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-970">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-972">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-972">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-973">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-973">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-974">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-974">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-975">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-975">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-977">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-977">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfcssup-13"></a><span data-ttu-id="a1cc3-978">\_SNORM<sup>FCS</sup> de DXGI_FORMAT_R16G16B16A16 (13)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-978">DXGI_FORMAT_R16G16B16A16\_SNORM<sup>FCS</sup> (13)</span></span>
| <span data-ttu-id="a1cc3-979">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-979">Target</span></span> | <span data-ttu-id="a1cc3-980">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-980">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-981">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-981">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-982">64</span><span class="sxs-lookup"><span data-stu-id="a1cc3-982">64</span></span> |
| <span data-ttu-id="a1cc3-983">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-983">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-985">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-985">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-987">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-987">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-989">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-989">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-990">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-990">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-991">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-991">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-993">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-993">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-995">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-995">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-997">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-997">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-999">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-999">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1001">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1001">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1003">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1003">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1004">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1004">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1005">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1005">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-1006">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1006">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-1007">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1007">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1009">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1009">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1011">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1011">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1013">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1013">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1015">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1015">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-1016">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1016">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-1017">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1017">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1018">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1018">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1019">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1019">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-1020">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1020">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-1021">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1021">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-1022">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1022">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-1023">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1023">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-1024">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1024">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-1025">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1025">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-1026">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1026">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1027">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1027">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1028">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1028">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1030">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1030">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-1032">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1032">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-1034">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1034">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-1036">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1036">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1038">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1038">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1040">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1040">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-1041">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1041">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1043">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1043">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-1044">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1044">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-1045">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1045">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-1046">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1046">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1048">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1048">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfcssup-14"></a><span data-ttu-id="a1cc3-1049">DXGI_FORMAT_R16G16B16A16 \_ Santo<sup>FCS</sup> (14)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1049">DXGI_FORMAT_R16G16B16A16\_SINT<sup>FCS</sup> (14)</span></span>
| <span data-ttu-id="a1cc3-1050">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1050">Target</span></span> | <span data-ttu-id="a1cc3-1051">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1051">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-1052">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1052">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-1053">64</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1053">64</span></span> |
| <span data-ttu-id="a1cc3-1054">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1054">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1056">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1056">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1058">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1058">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1060">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1060">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1061">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1061">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1062">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1062">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1064">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1064">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1066">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1066">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1068">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1068">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1070">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1070">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1072">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1072">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1073">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1073">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1074">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1074">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1075">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1075">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-1076">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1076">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-1077">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1077">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1079">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1079">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-1080">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1080">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1082">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1082">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1083">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1083">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-1084">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1084">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-1085">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1085">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1086">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1086">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1087">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1087">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-1088">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1088">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-1089">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1089">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-1090">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1090">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-1091">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1091">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-1092">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1092">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-1093">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1093">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-1094">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1094">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1095">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1095">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1096">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1096">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1098">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1098">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-1100">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1100">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-1102">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1102">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-1104">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1104">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-1105">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1105">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1107">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1107">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-1108">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1108">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1110">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1110">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-1111">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1111">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-1112">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1112">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-1113">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1113">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1115">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1115">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="a1cc3-1116">DXGI_FORMAT_R32G32 \_ <sup>PCs</sup> não tipados (15)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1116">DXGI_FORMAT_R32G32\_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="a1cc3-1117">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1117">Target</span></span> | <span data-ttu-id="a1cc3-1118">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1118">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-1119">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1119">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-1120">64</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1120">64</span></span> |
| <span data-ttu-id="a1cc3-1121">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1121">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1123">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1123">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1124">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1124">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1125">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1125">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1126">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1126">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1127">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1127">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1129">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1129">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1131">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1131">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1133">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1133">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1135">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1135">Shader ld</span></span> | \- |
| <span data-ttu-id="a1cc3-1136">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1136">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1137">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1137">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1138">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1138">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1139">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1139">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-1140">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1140">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-1141">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1141">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1143">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1143">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-1144">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1144">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1145">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1145">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1146">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1146">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-1147">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1147">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-1148">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1148">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1149">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1149">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1150">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1150">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-1151">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1151">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-1152">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1152">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-1153">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1153">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-1154">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1154">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-1155">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1155">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-1156">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1156">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-1157">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1157">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1158">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1158">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1159">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1159">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1161">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1161">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1162">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1162">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1163">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1163">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-1164">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1164">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-1165">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1165">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-1166">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1166">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-1167">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1167">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1169">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1169">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-1170">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1170">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-1171">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1171">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-1172">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1172">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-1173">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1173">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_floatsupfcssup-16"></a><span data-ttu-id="a1cc3-1174">\_<sup>FCS</sup> de DXGI_FORMAT_R32G32 float (16)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1174">DXGI_FORMAT_R32G32\_FLOAT<sup>FCS</sup> (16)</span></span>
| <span data-ttu-id="a1cc3-1175">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1175">Target</span></span> | <span data-ttu-id="a1cc3-1176">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1176">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-1177">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1177">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-1178">64</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1178">64</span></span> |
| <span data-ttu-id="a1cc3-1179">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1179">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1181">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1181">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1183">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1183">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1185">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1185">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1186">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1186">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1188">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1188">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1190">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1190">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1192">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1192">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1194">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1194">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1196">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1196">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1198">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1198">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1200">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1200">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1201">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1201">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1202">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1202">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-1203">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1203">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-1204">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1204">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1206">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1206">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1208">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1208">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1210">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1210">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1212">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1212">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-1213">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1213">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-1214">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1214">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1215">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1215">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1216">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1216">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-1217">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1217">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-1218">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1218">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-1219">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1219">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-1220">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1220">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-1221">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1221">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-1222">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1222">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-1223">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1223">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1224">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1224">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1225">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1225">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1227">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1227">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-1229">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1229">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-1231">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1231">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-1233">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1233">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1235">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1235">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1237">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1237">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-1238">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1238">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1240">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1240">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-1241">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1241">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-1242">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1242">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-1243">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1243">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-1244">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1244">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_uintsupfcssup-17"></a><span data-ttu-id="a1cc3-1245">\_<sup>FCS</sup> DXGI_FORMAT_R32G32 uint (17)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1245">DXGI_FORMAT_R32G32\_UINT<sup>FCS</sup> (17)</span></span>
| <span data-ttu-id="a1cc3-1246">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1246">Target</span></span> | <span data-ttu-id="a1cc3-1247">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1247">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-1248">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1248">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-1249">64</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1249">64</span></span> |
| <span data-ttu-id="a1cc3-1250">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1250">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1252">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1252">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1254">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1254">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1256">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1256">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1257">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1257">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1259">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1259">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1261">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1261">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1263">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1263">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1265">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1265">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1267">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1267">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1269">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1269">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1270">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1270">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1271">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1271">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1272">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1272">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-1273">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1273">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-1274">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1274">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1276">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1276">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-1277">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1277">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1279">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1279">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1280">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1280">Output Merger Logic Op</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-1282">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1282">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-1283">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1283">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1284">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1284">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1285">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1285">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-1286">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1286">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-1287">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1287">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-1288">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1288">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-1289">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1289">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-1290">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1290">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-1291">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1291">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-1292">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1292">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1293">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1293">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1294">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1294">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1296">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1296">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-1298">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1298">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-1300">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1300">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-1302">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1302">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-1303">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1303">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1305">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1305">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-1306">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1306">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1308">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1308">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-1309">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1309">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-1310">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1310">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-1311">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1311">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-1312">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1312">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_sintsupfcssup-18"></a><span data-ttu-id="a1cc3-1313">DXGI_FORMAT_R32G32 \_ Santo<sup>FCS</sup> (18)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1313">DXGI_FORMAT_R32G32\_SINT<sup>FCS</sup> (18)</span></span>
| <span data-ttu-id="a1cc3-1314">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1314">Target</span></span> | <span data-ttu-id="a1cc3-1315">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1315">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-1316">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1316">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-1317">64</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1317">64</span></span> |
| <span data-ttu-id="a1cc3-1318">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1318">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1320">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1320">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1322">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1322">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1324">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1324">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1325">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1325">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1327">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1327">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1329">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1329">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1331">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1331">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1333">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1333">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1335">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1335">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1337">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1337">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1338">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1338">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1339">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1339">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1340">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1340">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-1341">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1341">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-1342">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1342">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1344">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1344">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-1345">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1345">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1347">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1347">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1348">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1348">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-1349">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1349">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-1350">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1350">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1351">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1351">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1352">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1352">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-1353">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1353">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-1354">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1354">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-1355">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1355">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-1356">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1356">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-1357">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1357">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-1358">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1358">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-1359">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1359">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1360">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1360">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1361">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1361">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1363">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1363">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-1365">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1365">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-1367">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1367">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-1369">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1369">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-1370">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1370">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1372">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1372">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-1373">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1373">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1375">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1375">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-1376">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1376">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-1377">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1377">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-1378">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1378">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-1379">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1379">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a><span data-ttu-id="a1cc3-1380">DXGI_FORMAT_R32G8X24 \_ <sup>PCs</sup> não tipados (19)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1380">DXGI_FORMAT_R32G8X24\_TYPELESS<sup>PCS</sup> (19)</span></span>
| <span data-ttu-id="a1cc3-1381">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1381">Target</span></span> | <span data-ttu-id="a1cc3-1382">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1382">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-1383">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1383">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-1384">64</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1384">64</span></span> |
| <span data-ttu-id="a1cc3-1385">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1385">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1387">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1387">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1388">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1388">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1389">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1389">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1390">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1390">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1391">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1391">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1393">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1393">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1395">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1395">Texture3D</span></span> | \- |
| <span data-ttu-id="a1cc3-1396">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1396">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1398">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1398">Shader ld</span></span> | \- |
| <span data-ttu-id="a1cc3-1399">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1399">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1400">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1400">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1401">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1401">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1402">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1402">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-1403">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1403">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-1404">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1404">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1406">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1406">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-1407">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1407">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1408">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1408">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1409">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1409">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-1410">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1410">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-1411">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1411">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1412">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1412">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1413">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1413">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-1414">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1414">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-1415">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1415">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-1416">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1416">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-1417">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1417">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-1418">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1418">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-1419">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1419">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-1420">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1420">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1421">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1421">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1422">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1422">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1424">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1424">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1425">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1425">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1426">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1426">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-1427">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1427">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-1428">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1428">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-1429">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1429">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-1430">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1430">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1432">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1432">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-1433">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1433">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-1434">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1434">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-1435">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1435">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-1436">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1436">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfcssup-20"></a><span data-ttu-id="a1cc3-1437">DXGI_FORMAT_D32 \_ float \_ S8X24 \_ uint do<sup>FCS</sup> (20)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1437">DXGI_FORMAT_D32\_FLOAT\_S8X24\_UINT<sup>FCS</sup> (20)</span></span>
| <span data-ttu-id="a1cc3-1438">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1438">Target</span></span> | <span data-ttu-id="a1cc3-1439">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1439">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-1440">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1440">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-1441">64</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1441">64</span></span> |
| <span data-ttu-id="a1cc3-1442">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1442">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1444">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1444">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1445">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1445">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1446">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1446">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1447">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1447">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1448">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1448">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1450">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1450">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1452">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1452">Texture3D</span></span> | \- |
| <span data-ttu-id="a1cc3-1453">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1453">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1455">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1455">Shader ld</span></span> | \- |
| <span data-ttu-id="a1cc3-1456">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1456">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1457">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1457">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1458">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1458">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1459">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1459">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-1460">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1460">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-1461">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1461">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1463">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1463">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-1464">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1464">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1465">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1465">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1466">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1466">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-1467">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1467">Depth/Stencil Target</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1469">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1469">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1470">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1470">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1471">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1471">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-1472">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1472">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-1473">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1473">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-1474">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1474">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-1475">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1475">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-1476">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1476">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-1477">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1477">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-1478">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1478">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1479">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1479">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1480">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1480">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1482">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1482">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-1484">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1484">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-1486">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1486">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-1488">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1488">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-1489">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1489">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-1490">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1490">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-1491">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1491">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1493">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1493">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-1494">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1494">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-1495">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1495">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-1496">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1496">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-1497">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1497">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfcssup-21"></a><span data-ttu-id="a1cc3-1498">\_FCS DXGI_FORMAT_R32 \_ \_ de tipo float<sup></sup> X8X24 (21)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1498">DXGI_FORMAT_R32\_FLOAT\_X8X24\_TYPELESS<sup>FCS</sup> (21)</span></span>
| <span data-ttu-id="a1cc3-1499">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1499">Target</span></span> | <span data-ttu-id="a1cc3-1500">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1500">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-1501">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1501">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-1502">64</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1502">64</span></span> |
| <span data-ttu-id="a1cc3-1503">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1503">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1505">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1505">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1506">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1506">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1507">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1507">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1508">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1508">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1509">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1509">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1511">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1511">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1513">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1513">Texture3D</span></span> | \- |
| <span data-ttu-id="a1cc3-1514">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1514">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1516">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1516">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1518">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1518">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1520">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1520">Shader sample\_c (comparison filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1522">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1522">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1523">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1523">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1525">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1525">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-1526">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1526">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1528">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1528">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-1529">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1529">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1530">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1530">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1531">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1531">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-1532">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1532">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-1533">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1533">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1534">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1534">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1535">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1535">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-1536">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1536">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-1537">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1537">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-1538">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1538">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-1539">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1539">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-1540">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1540">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-1541">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1541">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-1542">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1542">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1543">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1543">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1544">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1544">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1546">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1546">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1547">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1547">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1548">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1548">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-1549">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1549">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-1550">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1550">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1552">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1552">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-1553">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1553">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1555">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1555">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-1556">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1556">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-1557">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1557">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-1558">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1558">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-1559">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1559">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfcssup-22"></a><span data-ttu-id="a1cc3-1560">\_ \_ G8X24 \_ de<sup>FCS</sup> (22) não tipado DXGI_FORMAT_X32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1560">DXGI_FORMAT_X32\_TYPELESS\_G8X24\_UINT<sup>FCS</sup> (22)</span></span>
| <span data-ttu-id="a1cc3-1561">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1561">Target</span></span> | <span data-ttu-id="a1cc3-1562">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1562">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-1563">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1563">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-1564">64</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1564">64</span></span> |
| <span data-ttu-id="a1cc3-1565">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1565">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1567">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1567">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1568">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1568">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1569">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1569">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1570">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1570">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1571">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1571">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1573">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1573">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1575">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1575">Texture3D</span></span> | \- |
| <span data-ttu-id="a1cc3-1576">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1576">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1578">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1578">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1580">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1580">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1581">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1581">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1582">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1582">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1583">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1583">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-1584">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1584">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-1585">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1585">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1587">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1587">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-1588">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1588">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1589">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1589">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1590">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1590">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-1591">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1591">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-1592">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1592">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1593">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1593">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1594">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1594">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-1595">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1595">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-1596">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1596">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-1597">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1597">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-1598">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1598">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-1599">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1599">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-1600">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1600">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-1601">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1601">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1602">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1602">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1603">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1603">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1605">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1605">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1606">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1606">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1607">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1607">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-1608">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1608">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-1609">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1609">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1611">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1611">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-1612">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1612">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1614">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1614">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-1615">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1615">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-1616">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1616">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-1617">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1617">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-1618">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1618">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="a1cc3-1619">DXGI_FORMAT_R10G10B10A2 \_ <sup>PCs</sup> não tipados (23)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1619">DXGI_FORMAT_R10G10B10A2\_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="a1cc3-1620">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1620">Target</span></span> | <span data-ttu-id="a1cc3-1621">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1621">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-1622">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1622">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-1623">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1623">32</span></span> |
| <span data-ttu-id="a1cc3-1624">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1624">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1626">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1626">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1627">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1627">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1628">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1628">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1629">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1629">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1630">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1630">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1632">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1632">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1634">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1634">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1636">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1636">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1638">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1638">Shader ld</span></span> | \- |
| <span data-ttu-id="a1cc3-1639">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1639">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1640">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1640">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1641">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1641">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1642">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1642">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-1643">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1643">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-1644">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1644">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1646">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1646">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-1647">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1647">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1648">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1648">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1649">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1649">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-1650">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1650">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-1651">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1651">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1652">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1652">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1653">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1653">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-1654">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1654">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-1655">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1655">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-1656">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1656">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-1657">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1657">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-1658">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1658">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-1659">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1659">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-1660">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1660">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1661">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1661">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1662">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1662">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1664">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1664">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1665">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1665">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1666">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1666">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-1667">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1667">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-1668">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1668">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-1669">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1669">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-1670">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1670">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1672">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1672">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-1673">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1673">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-1674">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1674">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-1675">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1675">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1677">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1677">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfcssup-24"></a><span data-ttu-id="a1cc3-1678">\_UNORM<sup>FCS</sup> de DXGI_FORMAT_R10G10B10A2 (24)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1678">DXGI_FORMAT_R10G10B10A2\_UNORM<sup>FCS</sup> (24)</span></span>
| <span data-ttu-id="a1cc3-1679">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1679">Target</span></span> | <span data-ttu-id="a1cc3-1680">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1680">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-1681">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1681">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-1682">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1682">32</span></span> |
| <span data-ttu-id="a1cc3-1683">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1683">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1685">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1685">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1687">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1687">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1689">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1689">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1690">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1690">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1691">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1691">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1693">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1693">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1695">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1695">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1697">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1697">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1699">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1699">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1701">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1701">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1703">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1703">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1704">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1704">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1705">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1705">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-1706">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1706">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-1707">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1707">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1709">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1709">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1711">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1711">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1713">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1713">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1715">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1715">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-1716">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1716">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-1717">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1717">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1718">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1718">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1719">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1719">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-1720">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1720">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-1721">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1721">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-1722">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1722">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-1723">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1723">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-1724">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1724">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-1725">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1725">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-1726">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1726">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1727">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1727">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1728">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1728">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1730">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1730">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1732">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1732">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-1734">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1734">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-1736">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1736">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1738">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1738">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1740">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1740">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1742">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1742">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1744">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1744">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-1745">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1745">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-1747">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1747">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1749">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1749">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1751">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1751">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfcssup-25"></a><span data-ttu-id="a1cc3-1752">\_<sup>FCS</sup> DXGI_FORMAT_R10G10B10A2 uint (25)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1752">DXGI_FORMAT_R10G10B10A2\_UINT<sup>FCS</sup> (25)</span></span>
| <span data-ttu-id="a1cc3-1753">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1753">Target</span></span> | <span data-ttu-id="a1cc3-1754">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1754">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-1755">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1755">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-1756">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1756">32</span></span> |
| <span data-ttu-id="a1cc3-1757">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1757">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1759">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1759">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1761">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1761">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1763">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1763">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1764">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1764">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1765">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1765">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1767">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1767">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1769">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1769">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1771">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1771">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1773">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1773">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1775">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1775">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1776">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1776">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1777">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1777">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1778">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1778">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-1779">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1779">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-1780">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1780">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1782">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1782">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-1783">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1783">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1785">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1785">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1786">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1786">Output Merger Logic Op</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-1788">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1788">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-1789">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1789">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1790">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1790">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1791">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1791">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-1792">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1792">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-1793">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1793">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-1794">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1794">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-1795">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1795">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-1796">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1796">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-1797">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1797">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-1798">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1798">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1799">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1799">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1800">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1800">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1802">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1802">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1804">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1804">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-1806">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1806">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-1808">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1808">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-1809">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1809">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1811">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1811">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-1812">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1812">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1814">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1814">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-1815">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1815">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-1816">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1816">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-1817">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1817">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1819">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1819">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfcssup-89"></a><span data-ttu-id="a1cc3-1820">DXGI_FORMAT_R10G10B10 \_ XR \_ Bias \_ a2 \_ UNORM<sup>FCS</sup> (89)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1820">DXGI_FORMAT_R10G10B10\_XR\_BIAS\_A2\_UNORM<sup>FCS</sup> (89)</span></span>
| <span data-ttu-id="a1cc3-1821">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1821">Target</span></span> | <span data-ttu-id="a1cc3-1822">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1822">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-1823">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1823">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-1824">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1824">32</span></span> |
| <span data-ttu-id="a1cc3-1825">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1825">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1827">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1827">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1828">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1828">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1829">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1829">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1830">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1830">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1831">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1831">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-1832">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1832">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1834">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1834">Texture3D</span></span> | \- |
| <span data-ttu-id="a1cc3-1835">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1835">TextureCube</span></span> | \- |
| <span data-ttu-id="a1cc3-1836">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1836">Shader ld</span></span> | \- |
| <span data-ttu-id="a1cc3-1837">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1837">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1838">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1838">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1839">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1839">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1840">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1840">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-1841">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1841">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-1842">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1842">Mipmap</span></span> | \- |
| <span data-ttu-id="a1cc3-1843">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1843">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-1844">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1844">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1845">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1845">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1846">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1846">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-1847">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1847">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-1848">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1848">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1849">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1849">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1850">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1850">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-1851">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1851">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-1852">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1852">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-1853">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1853">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-1854">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1854">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-1855">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1855">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-1856">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1856">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-1857">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1857">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1858">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1858">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1859">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1859">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1861">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1861">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1862">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1862">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1863">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1863">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-1864">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1864">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-1865">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1865">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-1866">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1866">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1868">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1868">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1870">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1870">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-1871">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1871">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-1873">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1873">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-1875">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1875">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1877">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1877">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="a1cc3-1878">DXGI_FORMAT_R11G11B10 \_ float<sup>FNS</sup> (26)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1878">DXGI_FORMAT_R11G11B10\_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="a1cc3-1879">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1879">Target</span></span> | <span data-ttu-id="a1cc3-1880">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1880">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-1881">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1881">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-1882">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1882">32</span></span> |
| <span data-ttu-id="a1cc3-1883">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1883">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1885">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1885">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1887">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1887">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1889">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1889">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1890">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1890">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1891">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1891">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1893">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1893">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1895">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1895">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1897">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1897">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1899">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1899">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1901">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1901">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1903">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1903">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1904">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1904">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1905">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1905">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-1906">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1906">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-1907">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1907">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1909">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1909">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1911">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1911">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1913">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1913">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1915">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1915">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-1916">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1916">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-1917">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1917">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1918">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1918">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1919">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1919">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-1920">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1920">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-1921">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1921">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-1922">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1922">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-1923">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1923">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-1924">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1924">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-1925">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1925">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-1926">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1926">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1927">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1927">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1928">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1928">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1930">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1930">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1932">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1932">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-1934">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1934">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-1936">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1936">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1938">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1938">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1940">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1940">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-1941">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1941">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a1cc3-1942">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1942">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-1943">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1943">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-1944">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1944">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-1945">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1945">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-1946">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1946">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="a1cc3-1947">DXGI_FORMAT_R8G8B8A8 \_ <sup>PCs</sup> não tipados (27)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1947">DXGI_FORMAT_R8G8B8A8\_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="a1cc3-1948">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1948">Target</span></span> | <span data-ttu-id="a1cc3-1949">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1949">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-1950">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1950">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-1951">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1951">32</span></span> |
| <span data-ttu-id="a1cc3-1952">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1952">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1954">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1954">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1955">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1955">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1956">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1956">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1957">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1957">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-1958">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1958">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1960">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1960">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1962">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1962">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1964">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1964">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1966">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1966">Shader ld</span></span> | \- |
| <span data-ttu-id="a1cc3-1967">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1967">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1968">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1968">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1969">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1969">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-1970">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1970">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-1971">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1971">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-1972">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1972">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1974">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1974">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-1975">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1975">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1976">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1976">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1977">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1977">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-1978">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1978">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-1979">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1979">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1980">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1980">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-1981">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1981">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-1982">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1982">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-1983">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1983">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-1984">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1984">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-1985">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1985">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-1986">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1986">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-1987">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1987">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-1988">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1988">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1989">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1989">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-1990">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1990">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-1992">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1992">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1993">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1993">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-1994">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1994">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-1995">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1995">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-1996">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1996">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-1997">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1997">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-1998">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-1998">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2000">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2000">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-2001">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2001">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-2002">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2002">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-2003">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2003">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2005">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2005">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfcssup-28"></a><span data-ttu-id="a1cc3-2006">\_UNORM<sup>FCS</sup> de DXGI_FORMAT_R8G8B8A8 (28)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2006">DXGI_FORMAT_R8G8B8A8\_UNORM<sup>FCS</sup> (28)</span></span>
| <span data-ttu-id="a1cc3-2007">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2007">Target</span></span> | <span data-ttu-id="a1cc3-2008">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2008">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-2009">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2009">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-2010">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2010">32</span></span> |
| <span data-ttu-id="a1cc3-2011">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2011">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2013">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2013">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2015">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2015">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2017">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2017">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2018">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2018">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2019">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2019">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2021">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2021">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2023">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2023">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2025">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2025">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2027">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2027">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2029">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2029">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2031">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2031">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2032">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2032">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2033">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2033">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-2034">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2034">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-2035">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2035">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2037">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2037">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2039">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2039">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2041">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2041">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2043">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2043">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-2044">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2044">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-2045">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2045">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-2046">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2046">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-2047">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2047">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-2048">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2048">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-2049">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2049">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-2050">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2050">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-2051">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2051">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-2052">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2052">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-2053">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2053">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-2054">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2054">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-2055">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2055">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-2056">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2056">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2058">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2058">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2060">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2060">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-2062">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2062">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-2064">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2064">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2066">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2066">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2068">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2068">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2070">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2070">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2072">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2072">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-2073">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2073">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-2075">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2075">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2077">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2077">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2079">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2079">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfcssup-29"></a><span data-ttu-id="a1cc3-2080">\_FCS DXGI_FORMAT_R8G8B8A8 \_ UNORM<sup></sup> sRGB (29)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2080">DXGI_FORMAT_R8G8B8A8\_UNORM\_SRGB<sup>FCS</sup> (29)</span></span>
| <span data-ttu-id="a1cc3-2081">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2081">Target</span></span> | <span data-ttu-id="a1cc3-2082">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2082">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-2083">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2083">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-2084">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2084">32</span></span> |
| <span data-ttu-id="a1cc3-2085">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2085">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2087">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2087">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2088">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2088">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2089">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2089">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2090">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2090">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2091">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2091">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2093">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2093">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2095">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2095">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2097">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2097">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2099">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2099">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2101">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2101">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2103">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2103">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2104">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2104">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2105">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2105">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-2106">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2106">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-2107">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2107">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2109">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2109">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2111">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2111">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2113">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2113">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2115">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2115">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-2116">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2116">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-2117">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2117">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-2118">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2118">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-2119">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2119">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-2120">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2120">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-2121">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2121">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-2122">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2122">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-2123">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2123">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-2124">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2124">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-2125">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2125">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-2126">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2126">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-2127">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2127">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-2128">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2128">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2130">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2130">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2132">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2132">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-2134">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2134">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-2136">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2136">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2138">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2138">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2140">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2140">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2142">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2142">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2144">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2144">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-2145">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2145">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-2147">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2147">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2149">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2149">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2151">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2151">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfcssup-30"></a><span data-ttu-id="a1cc3-2152">\_<sup>FCS</sup> DXGI_FORMAT_R8G8B8A8 uint (30)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2152">DXGI_FORMAT_R8G8B8A8\_UINT<sup>FCS</sup> (30)</span></span>
| <span data-ttu-id="a1cc3-2153">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2153">Target</span></span> | <span data-ttu-id="a1cc3-2154">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2154">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-2155">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2155">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-2156">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2156">32</span></span> |
| <span data-ttu-id="a1cc3-2157">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2157">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2159">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2159">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2161">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2161">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2163">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2163">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2164">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2164">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2165">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2165">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2167">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2167">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2169">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2169">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2171">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2171">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2173">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2173">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2175">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2175">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2176">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2176">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2177">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2177">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2178">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2178">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-2179">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2179">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-2180">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2180">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2182">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2182">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-2183">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2183">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2185">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2185">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-2186">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2186">Output Merger Logic Op</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-2188">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2188">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-2189">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2189">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-2190">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2190">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-2191">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2191">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-2192">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2192">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-2193">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2193">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-2194">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2194">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-2195">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2195">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-2196">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2196">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-2197">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2197">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-2198">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2198">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-2199">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2199">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-2200">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2200">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2202">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2202">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2204">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2204">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-2206">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2206">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-2208">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2208">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-2209">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2209">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2211">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2211">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-2212">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2212">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2214">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2214">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-2215">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2215">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-2216">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2216">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-2217">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2217">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2219">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2219">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfcssup-31"></a><span data-ttu-id="a1cc3-2220">DXGI_FORMAT_R8G8B8A8 \_ <sup>FCS</sup> SNORM (31)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2220">DXGI_FORMAT_R8G8B8A8\_SNORM<sup>FCS</sup> (31)</span></span>
| <span data-ttu-id="a1cc3-2221">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2221">Target</span></span> | <span data-ttu-id="a1cc3-2222">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2222">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-2223">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2223">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-2224">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2224">32</span></span> |
| <span data-ttu-id="a1cc3-2225">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2225">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2227">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2227">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2229">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2229">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2231">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2231">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2232">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2232">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2233">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2233">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2235">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2235">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2237">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2237">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2239">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2239">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2241">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2241">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2243">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2243">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2245">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2245">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2246">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2246">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2247">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2247">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-2248">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2248">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-2249">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2249">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2251">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2251">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2253">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2253">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2255">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2255">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2257">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2257">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-2258">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2258">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-2259">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2259">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-2260">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2260">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-2261">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2261">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-2262">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2262">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-2263">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2263">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-2264">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2264">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-2265">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2265">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-2266">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2266">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-2267">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2267">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-2268">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2268">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-2269">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2269">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-2270">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2270">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2272">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2272">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2274">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2274">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-2276">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2276">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-2278">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2278">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2280">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2280">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2282">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2282">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-2283">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2283">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2285">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2285">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-2286">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2286">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-2287">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2287">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-2288">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2288">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2290">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2290">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfcssup-32"></a><span data-ttu-id="a1cc3-2291">\_<sup>FCS</sup> DXGI_FORMAT_R8G8B8A8 Santo (32)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2291">DXGI_FORMAT_R8G8B8A8\_SINT<sup>FCS</sup> (32)</span></span>
| <span data-ttu-id="a1cc3-2292">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2292">Target</span></span> | <span data-ttu-id="a1cc3-2293">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2293">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-2294">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2294">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-2295">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2295">32</span></span> |
| <span data-ttu-id="a1cc3-2296">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2296">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2298">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2298">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2300">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2300">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2302">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2302">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2303">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2303">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2304">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2304">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2306">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2306">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2308">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2308">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2310">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2310">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2312">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2312">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2314">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2314">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2315">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2315">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2316">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2316">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2317">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2317">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-2318">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2318">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-2319">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2319">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2321">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2321">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-2322">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2322">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2324">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2324">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-2325">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2325">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-2326">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2326">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-2327">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2327">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-2328">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2328">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-2329">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2329">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-2330">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2330">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-2331">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2331">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-2332">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2332">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-2333">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2333">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-2334">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2334">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-2335">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2335">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-2336">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2336">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-2337">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2337">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-2338">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2338">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2340">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2340">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2342">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2342">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-2344">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2344">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-2346">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2346">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-2347">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2347">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2349">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2349">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-2350">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2350">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2352">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2352">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-2353">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2353">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-2354">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2354">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-2355">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2355">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2357">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2357">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="a1cc3-2358">DXGI_FORMAT_R16G16 \_ <sup>PCs</sup> não tipados (33)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2358">DXGI_FORMAT_R16G16\_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="a1cc3-2359">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2359">Target</span></span> | <span data-ttu-id="a1cc3-2360">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2360">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-2361">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2361">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-2362">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2362">32</span></span> |
| <span data-ttu-id="a1cc3-2363">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2363">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2365">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2365">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2366">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2366">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2367">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2367">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2368">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2368">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2369">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2369">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2371">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2371">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2373">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2373">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2375">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2375">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2377">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2377">Shader ld</span></span> | \- |
| <span data-ttu-id="a1cc3-2378">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2378">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2379">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2379">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2380">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2380">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2381">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2381">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-2382">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2382">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-2383">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2383">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2385">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2385">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-2386">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2386">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-2387">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2387">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-2388">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2388">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-2389">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2389">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-2390">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2390">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-2391">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2391">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-2392">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2392">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-2393">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2393">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-2394">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2394">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-2395">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2395">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-2396">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2396">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-2397">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2397">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-2398">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2398">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-2399">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2399">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-2400">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2400">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-2401">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2401">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2403">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2403">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-2404">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2404">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-2405">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2405">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-2406">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2406">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-2407">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2407">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-2408">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2408">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-2409">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2409">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2411">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2411">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-2412">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2412">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-2413">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2413">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-2414">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2414">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-2415">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2415">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_floatsupfcssup-34"></a><span data-ttu-id="a1cc3-2416">\_<sup>FCS</sup> de DXGI_FORMAT_R16G16 float (34)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2416">DXGI_FORMAT_R16G16\_FLOAT<sup>FCS</sup> (34)</span></span>
| <span data-ttu-id="a1cc3-2417">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2417">Target</span></span> | <span data-ttu-id="a1cc3-2418">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2418">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-2419">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2419">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-2420">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2420">32</span></span> |
| <span data-ttu-id="a1cc3-2421">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2421">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2423">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2423">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2425">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2425">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2427">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2427">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2428">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2428">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2429">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2429">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2431">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2431">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2433">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2433">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2435">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2435">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2437">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2437">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2439">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2439">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2441">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2441">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2442">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2442">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2443">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2443">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-2444">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2444">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-2445">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2445">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2447">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2447">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2449">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2449">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2451">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2451">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2453">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2453">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-2454">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2454">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-2455">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2455">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-2456">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2456">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-2457">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2457">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-2458">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2458">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-2459">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2459">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-2460">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2460">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-2461">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2461">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-2462">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2462">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-2463">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2463">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-2464">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2464">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-2465">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2465">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-2466">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2466">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2468">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2468">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2470">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2470">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-2472">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2472">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-2474">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2474">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2476">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2476">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2478">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2478">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-2479">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2479">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2481">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2481">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-2482">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2482">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-2483">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2483">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-2484">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2484">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-2485">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2485">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_unormsupfcssup-35"></a><span data-ttu-id="a1cc3-2486">\_UNORM<sup>FCS</sup> de DXGI_FORMAT_R16G16 (35)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2486">DXGI_FORMAT_R16G16\_UNORM<sup>FCS</sup> (35)</span></span>
| <span data-ttu-id="a1cc3-2487">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2487">Target</span></span> | <span data-ttu-id="a1cc3-2488">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2488">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-2489">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2489">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-2490">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2490">32</span></span> |
| <span data-ttu-id="a1cc3-2491">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2491">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2493">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2493">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2495">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2495">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2497">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2497">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2498">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2498">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2499">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2499">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2501">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2501">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2503">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2503">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2505">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2505">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2507">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2507">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2509">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2509">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2511">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2511">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2512">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2512">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2513">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2513">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-2514">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2514">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-2515">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2515">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2517">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2517">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2519">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2519">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2521">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2521">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2523">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2523">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-2524">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2524">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-2525">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2525">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-2526">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2526">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-2527">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2527">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-2528">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2528">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-2529">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2529">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-2530">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2530">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-2531">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2531">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-2532">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2532">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-2533">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2533">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-2534">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2534">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-2535">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2535">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-2536">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2536">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2538">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2538">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2540">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2540">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-2542">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2542">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-2544">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2544">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2546">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2546">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2548">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2548">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-2549">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2549">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2551">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2551">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-2552">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2552">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-2553">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2553">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-2554">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2554">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-2555">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2555">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_uintsupfcssup-36"></a><span data-ttu-id="a1cc3-2556">\_<sup>FCS</sup> DXGI_FORMAT_R16G16 uint (36)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2556">DXGI_FORMAT_R16G16\_UINT<sup>FCS</sup> (36)</span></span>
| <span data-ttu-id="a1cc3-2557">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2557">Target</span></span> | <span data-ttu-id="a1cc3-2558">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2558">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-2559">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2559">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-2560">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2560">32</span></span> |
| <span data-ttu-id="a1cc3-2561">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2561">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2563">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2563">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2565">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2565">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2567">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2567">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2568">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2568">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2569">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2569">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2571">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2571">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2573">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2573">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2575">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2575">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2577">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2577">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2579">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2579">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2580">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2580">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2581">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2581">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2582">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2582">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-2583">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2583">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-2584">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2584">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2586">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2586">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-2587">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2587">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2589">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2589">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-2590">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2590">Output Merger Logic Op</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-2592">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2592">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-2593">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2593">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-2594">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2594">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-2595">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2595">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-2596">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2596">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-2597">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2597">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-2598">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2598">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-2599">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2599">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-2600">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2600">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-2601">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2601">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-2602">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2602">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-2603">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2603">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-2604">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2604">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2606">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2606">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2608">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2608">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-2610">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2610">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-2612">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2612">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-2613">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2613">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2615">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2615">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-2616">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2616">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2618">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2618">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-2619">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2619">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-2620">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2620">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-2621">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2621">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-2622">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2622">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_snormsupfcssup-37"></a><span data-ttu-id="a1cc3-2623">\_SNORM<sup>FCS</sup> de DXGI_FORMAT_R16G16 (37)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2623">DXGI_FORMAT_R16G16\_SNORM<sup>FCS</sup> (37)</span></span>
| <span data-ttu-id="a1cc3-2624">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2624">Target</span></span> | <span data-ttu-id="a1cc3-2625">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2625">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-2626">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2626">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-2627">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2627">32</span></span> |
| <span data-ttu-id="a1cc3-2628">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2628">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2630">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2630">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2632">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2632">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2634">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2634">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2635">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2635">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2636">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2636">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2638">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2638">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2640">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2640">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2642">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2642">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2644">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2644">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2646">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2646">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2648">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2648">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2649">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2649">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2650">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2650">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-2651">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2651">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-2652">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2652">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2654">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2654">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2656">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2656">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2658">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2658">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2660">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2660">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-2661">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2661">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-2662">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2662">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-2663">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2663">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-2664">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2664">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-2665">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2665">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-2666">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2666">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-2667">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2667">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-2668">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2668">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-2669">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2669">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-2670">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2670">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-2671">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2671">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-2672">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2672">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-2673">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2673">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2675">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2675">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2677">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2677">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-2679">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2679">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-2681">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2681">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2683">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2683">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2685">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2685">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-2686">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2686">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2688">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2688">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-2689">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2689">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-2690">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2690">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-2691">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2691">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-2692">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2692">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_sintsupfcssup-38"></a><span data-ttu-id="a1cc3-2693">\_<sup>FCS</sup> DXGI_FORMAT_R16G16 Santo (38)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2693">DXGI_FORMAT_R16G16\_SINT<sup>FCS</sup> (38)</span></span>
| <span data-ttu-id="a1cc3-2694">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2694">Target</span></span> | <span data-ttu-id="a1cc3-2695">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2695">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-2696">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2696">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-2697">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2697">32</span></span> |
| <span data-ttu-id="a1cc3-2698">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2698">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2700">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2700">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2702">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2702">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2704">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2704">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2705">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2705">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2706">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2706">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2708">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2708">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2710">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2710">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2712">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2712">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2714">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2714">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2716">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2716">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2717">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2717">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2718">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2718">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2719">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2719">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-2720">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2720">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-2721">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2721">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2723">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2723">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-2724">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2724">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2726">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2726">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-2727">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2727">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-2728">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2728">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-2729">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2729">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-2730">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2730">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-2731">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2731">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-2732">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2732">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-2733">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2733">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-2734">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2734">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-2735">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2735">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-2736">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2736">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-2737">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2737">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-2738">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2738">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-2739">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2739">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-2740">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2740">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2742">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2742">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2744">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2744">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-2746">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2746">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-2748">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2748">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-2749">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2749">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2751">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2751">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-2752">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2752">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2754">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2754">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-2755">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2755">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-2756">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2756">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-2757">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2757">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-2758">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2758">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="a1cc3-2759">DXGI_FORMAT_R32 \_ <sup>PCs</sup> não tipados (39)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2759">DXGI_FORMAT_R32\_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="a1cc3-2760">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2760">Target</span></span> | <span data-ttu-id="a1cc3-2761">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2761">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-2762">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2762">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-2763">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2763">32</span></span> |
| <span data-ttu-id="a1cc3-2764">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2764">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2766">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2766">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2767">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2767">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2768">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2768">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2769">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2769">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2770">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2770">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2772">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2772">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2774">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2774">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2776">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2776">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2778">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2778">Shader ld</span></span> | \- |
| <span data-ttu-id="a1cc3-2779">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2779">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2780">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2780">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2781">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2781">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2782">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2782">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-2783">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2783">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-2784">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2784">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2786">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2786">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-2787">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2787">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-2788">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2788">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-2789">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2789">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-2790">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2790">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-2791">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2791">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-2792">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2792">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-2793">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2793">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-2794">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2794">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-2795">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2795">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-2796">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2796">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-2797">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2797">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-2798">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2798">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-2799">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2799">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-2800">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2800">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-2801">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2801">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-2802">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2802">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2804">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2804">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-2805">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2805">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-2806">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2806">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-2807">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2807">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-2808">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2808">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-2809">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2809">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-2810">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2810">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2812">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2812">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-2813">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2813">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-2814">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2814">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-2815">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2815">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2817">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2817">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_floatsupfcssup-40"></a><span data-ttu-id="a1cc3-2818">\_<sup>FCS</sup> de DXGI_FORMAT_D32 float (40)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2818">DXGI_FORMAT_D32\_FLOAT<sup>FCS</sup> (40)</span></span>
| <span data-ttu-id="a1cc3-2819">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2819">Target</span></span> | <span data-ttu-id="a1cc3-2820">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2820">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-2821">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2821">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-2822">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2822">32</span></span> |
| <span data-ttu-id="a1cc3-2823">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2823">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2825">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2825">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2826">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2826">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2827">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2827">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2828">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2828">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2829">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2829">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2831">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2831">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2833">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2833">Texture3D</span></span> | \- |
| <span data-ttu-id="a1cc3-2834">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2834">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2836">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2836">Shader ld</span></span> | \- |
| <span data-ttu-id="a1cc3-2837">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2837">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2838">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2838">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2839">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2839">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2840">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2840">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-2841">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2841">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-2842">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2842">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2844">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2844">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-2845">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2845">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-2846">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2846">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-2847">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2847">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-2848">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2848">Depth/Stencil Target</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2850">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2850">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-2851">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2851">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-2852">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2852">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-2853">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2853">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-2854">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2854">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-2855">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2855">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-2856">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2856">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-2857">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2857">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-2858">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2858">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-2859">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2859">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-2860">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2860">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-2861">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2861">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2863">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2863">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2865">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2865">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-2867">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2867">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-2869">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2869">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-2870">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2870">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-2871">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2871">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-2872">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2872">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2874">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2874">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-2875">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2875">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-2876">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2876">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-2877">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2877">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2879">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2879">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_floatsupfcssup-41"></a><span data-ttu-id="a1cc3-2880">\_<sup>FCS</sup> de DXGI_FORMAT_R32 float (41)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2880">DXGI_FORMAT_R32\_FLOAT<sup>FCS</sup> (41)</span></span>
| <span data-ttu-id="a1cc3-2881">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2881">Target</span></span> | <span data-ttu-id="a1cc3-2882">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2882">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-2883">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2883">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-2884">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2884">32</span></span> |
| <span data-ttu-id="a1cc3-2885">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2885">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2887">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2887">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2889">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2889">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2891">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2891">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-2892">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2892">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2894">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2894">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2896">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2896">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2898">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2898">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2900">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2900">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2902">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2902">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2904">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2904">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2906">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2906">Shader sample\_c (comparison filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2908">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2908">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2909">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2909">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2911">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2911">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-2912">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2912">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2914">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2914">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2916">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2916">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2918">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2918">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2920">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2920">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-2921">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2921">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-2922">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2922">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-2923">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2923">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-2924">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2924">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-2925">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2925">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-2926">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2926">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-2927">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2927">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-2928">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2928">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-2929">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2929">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-2930">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2930">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-2931">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2931">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-2932">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2932">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-2933">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2933">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2935">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2935">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2937">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2937">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-2939">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2939">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-2941">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2941">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2943">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2943">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2945">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2945">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-2946">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2946">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2948">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2948">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-2949">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2949">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-2950">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2950">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-2951">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2951">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2953">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2953">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_uintsupfcssup-42"></a><span data-ttu-id="a1cc3-2954">\_<sup>FCS</sup> DXGI_FORMAT_R32 uint (42)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2954">DXGI_FORMAT_R32\_UINT<sup>FCS</sup> (42)</span></span>
| <span data-ttu-id="a1cc3-2955">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2955">Target</span></span> | <span data-ttu-id="a1cc3-2956">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2956">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-2957">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2957">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-2958">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2958">32</span></span> |
| <span data-ttu-id="a1cc3-2959">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2959">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2961">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2961">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2963">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2963">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2965">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2965">Input Assembler Index Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2967">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2967">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2969">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2969">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2971">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2971">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2973">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2973">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2975">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2975">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2977">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2977">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2979">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2979">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2980">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2980">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2981">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2981">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-2982">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2982">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-2983">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2983">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-2984">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2984">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2986">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2986">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-2987">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2987">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-2989">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2989">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-2990">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2990">Output Merger Logic Op</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-2992">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2992">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-2993">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2993">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-2994">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2994">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-2995">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2995">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-2996">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2996">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-2997">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2997">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-2998">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2998">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-2999">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-2999">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-3000">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3000">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-3001">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3001">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-3002">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3002">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3003">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3003">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3004">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3004">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3006">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3006">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3008">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3008">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-3010">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3010">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-3012">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3012">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-3013">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3013">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3015">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3015">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-3016">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3016">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3018">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3018">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-3019">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3019">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-3020">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3020">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-3021">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3021">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3023">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3023">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_sintsupfcssup-43"></a><span data-ttu-id="a1cc3-3024">\_<sup>FCS</sup> DXGI_FORMAT_R32 Santo (43)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3024">DXGI_FORMAT_R32\_SINT<sup>FCS</sup> (43)</span></span>
| <span data-ttu-id="a1cc3-3025">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3025">Target</span></span> | <span data-ttu-id="a1cc3-3026">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3026">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-3027">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3027">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-3028">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3028">32</span></span> |
| <span data-ttu-id="a1cc3-3029">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3029">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3031">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3031">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3033">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3033">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3035">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3035">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3036">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3036">Stream Output Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3038">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3038">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3040">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3040">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3042">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3042">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3044">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3044">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3046">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3046">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3048">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3048">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3049">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3049">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3050">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3050">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3051">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3051">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-3052">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3052">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-3053">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3053">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3055">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3055">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-3056">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3056">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3058">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3058">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-3059">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3059">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-3060">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3060">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-3061">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3061">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-3062">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3062">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-3063">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3063">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-3064">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3064">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-3065">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3065">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-3066">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3066">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-3067">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3067">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-3068">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3068">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-3069">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3069">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-3070">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3070">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3071">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3071">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3072">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3072">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3074">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3074">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3076">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3076">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-3078">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3078">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-3080">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3080">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-3081">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3081">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3083">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3083">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-3084">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3084">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3086">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3086">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-3087">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3087">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-3088">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3088">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-3089">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3089">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3091">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3091">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a><span data-ttu-id="a1cc3-3092">DXGI_FORMAT_R24G8 \_ <sup>PCs</sup> não tipados (44)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3092">DXGI_FORMAT_R24G8\_TYPELESS<sup>PCS</sup> (44)</span></span>
| <span data-ttu-id="a1cc3-3093">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3093">Target</span></span> | <span data-ttu-id="a1cc3-3094">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3094">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-3095">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3095">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-3096">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3096">32</span></span> |
| <span data-ttu-id="a1cc3-3097">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3097">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3099">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3099">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3100">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3100">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3101">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3101">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3102">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3102">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3103">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3103">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3105">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3105">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3107">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3107">Texture3D</span></span> | \- |
| <span data-ttu-id="a1cc3-3108">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3108">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3110">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3110">Shader ld</span></span> | \- |
| <span data-ttu-id="a1cc3-3111">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3111">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3112">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3112">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3113">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3113">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3114">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3114">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-3115">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3115">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-3116">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3116">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3118">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3118">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-3119">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3119">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-3120">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3120">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-3121">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3121">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-3122">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3122">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-3123">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3123">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-3124">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3124">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-3125">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3125">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-3126">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3126">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-3127">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3127">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-3128">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3128">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-3129">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3129">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-3130">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3130">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-3131">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3131">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-3132">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3132">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3133">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3133">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3134">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3134">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3136">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3136">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-3137">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3137">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-3138">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3138">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-3139">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3139">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-3140">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3140">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-3141">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3141">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-3142">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3142">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3144">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3144">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-3145">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3145">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-3146">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3146">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-3147">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3147">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-3148">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3148">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfcssup-45"></a><span data-ttu-id="a1cc3-3149">\_FCS DXGI_FORMAT_D24 \_ UNORM \_ S8<sup></sup> uint (45)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3149">DXGI_FORMAT_D24\_UNORM\_S8\_UINT<sup>FCS</sup> (45)</span></span>
| <span data-ttu-id="a1cc3-3150">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3150">Target</span></span> | <span data-ttu-id="a1cc3-3151">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3151">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-3152">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3152">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-3153">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3153">32</span></span> |
| <span data-ttu-id="a1cc3-3154">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3154">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3156">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3156">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3157">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3157">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3158">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3158">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3159">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3159">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3160">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3160">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3162">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3162">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3164">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3164">Texture3D</span></span> | \- |
| <span data-ttu-id="a1cc3-3165">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3165">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3167">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3167">Shader ld</span></span> | \- |
| <span data-ttu-id="a1cc3-3168">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3168">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3169">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3169">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3170">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3170">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3171">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3171">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-3172">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3172">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-3173">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3173">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3175">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3175">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-3176">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3176">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-3177">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3177">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-3178">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3178">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-3179">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3179">Depth/Stencil Target</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3181">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3181">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-3182">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3182">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-3183">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3183">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-3184">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3184">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-3185">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3185">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-3186">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3186">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-3187">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3187">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-3188">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3188">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-3189">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3189">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-3190">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3190">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3191">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3191">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3192">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3192">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3194">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3194">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3196">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3196">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-3198">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3198">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-3200">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3200">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-3201">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3201">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-3202">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3202">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-3203">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3203">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3205">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3205">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-3206">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3206">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-3207">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3207">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-3208">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3208">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-3209">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3209">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfcssup-46"></a><span data-ttu-id="a1cc3-3210">\_FCS com \_ \_ tipo de UNORM<sup></sup> x8 (46) DXGI_FORMAT_R24</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3210">DXGI_FORMAT_R24\_UNORM\_X8\_TYPELESS<sup>FCS</sup> (46)</span></span>
| <span data-ttu-id="a1cc3-3211">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3211">Target</span></span> | <span data-ttu-id="a1cc3-3212">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3212">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-3213">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3213">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-3214">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3214">32</span></span> |
| <span data-ttu-id="a1cc3-3215">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3215">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3217">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3217">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3218">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3218">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3219">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3219">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3220">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3220">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3221">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3221">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3223">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3223">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3225">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3225">Texture3D</span></span> | \- |
| <span data-ttu-id="a1cc3-3226">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3226">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3228">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3228">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3230">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3230">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3232">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3232">Shader sample\_c (comparison filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3234">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3234">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3235">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3235">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3237">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3237">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-3238">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3238">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3240">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3240">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-3241">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3241">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-3242">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3242">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-3243">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3243">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-3244">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3244">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-3245">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3245">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-3246">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3246">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-3247">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3247">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-3248">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3248">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-3249">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3249">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-3250">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3250">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-3251">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3251">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-3252">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3252">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-3253">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3253">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-3254">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3254">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3255">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3255">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3256">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3256">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3258">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3258">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-3259">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3259">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-3260">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3260">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-3261">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3261">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-3262">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3262">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3264">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3264">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-3265">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3265">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3267">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3267">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-3268">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3268">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-3269">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3269">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-3270">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3270">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-3271">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3271">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfcssup-47"></a><span data-ttu-id="a1cc3-3272">\_FCS uint não tipado \_ de DXGI_FORMAT_X24 \_ (47)<sup></sup></span><span class="sxs-lookup"><span data-stu-id="a1cc3-3272">DXGI_FORMAT_X24\_TYPELESS\_G8\_UINT<sup>FCS</sup> (47)</span></span>
| <span data-ttu-id="a1cc3-3273">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3273">Target</span></span> | <span data-ttu-id="a1cc3-3274">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3274">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-3275">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3275">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-3276">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3276">32</span></span> |
| <span data-ttu-id="a1cc3-3277">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3277">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3279">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3279">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3280">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3280">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3281">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3281">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3282">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3282">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3283">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3283">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3285">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3285">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3287">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3287">Texture3D</span></span> | \- |
| <span data-ttu-id="a1cc3-3288">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3288">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3290">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3290">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3292">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3292">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3293">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3293">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3294">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3294">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3295">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3295">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-3296">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3296">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-3297">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3297">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3299">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3299">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-3300">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3300">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-3301">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3301">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-3302">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3302">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-3303">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3303">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-3304">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3304">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-3305">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3305">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-3306">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3306">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-3307">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3307">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-3308">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3308">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-3309">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3309">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-3310">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3310">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-3311">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3311">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-3312">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3312">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-3313">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3313">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3314">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3314">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3315">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3315">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3317">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3317">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-3318">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3318">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-3319">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3319">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-3320">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3320">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-3321">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3321">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3323">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3323">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-3324">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3324">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3326">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3326">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-3327">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3327">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-3328">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3328">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-3329">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3329">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-3330">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3330">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="a1cc3-3331">DXGI_FORMAT_R8G8 \_ <sup>PCs</sup> não tipados (48)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3331">DXGI_FORMAT_R8G8\_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="a1cc3-3332">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3332">Target</span></span> | <span data-ttu-id="a1cc3-3333">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3333">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-3334">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3334">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-3335">16</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3335">16</span></span> |
| <span data-ttu-id="a1cc3-3336">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3336">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3338">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3338">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3339">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3339">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3340">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3340">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3341">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3341">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3342">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3342">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3344">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3344">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3346">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3346">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3348">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3348">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3350">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3350">Shader ld</span></span> | \- |
| <span data-ttu-id="a1cc3-3351">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3351">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3352">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3352">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3353">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3353">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3354">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3354">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-3355">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3355">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-3356">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3356">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3358">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3358">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-3359">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3359">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-3360">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3360">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-3361">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3361">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-3362">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3362">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-3363">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3363">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-3364">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3364">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-3365">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3365">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-3366">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3366">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-3367">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3367">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-3368">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3368">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-3369">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3369">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-3370">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3370">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-3371">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3371">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-3372">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3372">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3373">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3373">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3374">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3374">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3376">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3376">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-3377">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3377">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-3378">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3378">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-3379">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3379">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-3380">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3380">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-3381">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3381">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-3382">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3382">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3384">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3384">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-3385">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3385">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-3386">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3386">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-3387">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3387">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-3388">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3388">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_unormsupfcssup-49"></a><span data-ttu-id="a1cc3-3389">\_UNORM<sup>FCS</sup> de DXGI_FORMAT_R8G8 (49)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3389">DXGI_FORMAT_R8G8\_UNORM<sup>FCS</sup> (49)</span></span>
| <span data-ttu-id="a1cc3-3390">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3390">Target</span></span> | <span data-ttu-id="a1cc3-3391">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3391">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-3392">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3392">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-3393">16</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3393">16</span></span> |
| <span data-ttu-id="a1cc3-3394">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3394">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3396">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3396">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3398">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3398">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3400">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3400">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3401">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3401">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3402">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3402">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3404">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3404">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3406">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3406">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3408">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3408">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3410">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3410">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3412">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3412">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3414">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3414">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3415">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3415">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3416">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3416">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-3417">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3417">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-3418">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3418">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3420">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3420">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3422">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3422">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3424">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3424">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3426">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3426">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-3427">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3427">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-3428">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3428">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-3429">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3429">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-3430">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3430">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-3431">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3431">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-3432">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3432">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-3433">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3433">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-3434">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3434">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-3435">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3435">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-3436">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3436">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-3437">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3437">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3438">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3438">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3439">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3439">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3441">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3441">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3443">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3443">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-3445">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3445">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-3447">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3447">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3449">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3449">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3451">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3451">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-3452">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3452">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3454">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3454">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-3455">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3455">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-3456">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3456">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-3457">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3457">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3459">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3459">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_uintsupfcssup-50"></a><span data-ttu-id="a1cc3-3460">\_<sup>FCS</sup> DXGI_FORMAT_R8G8 uint (50)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3460">DXGI_FORMAT_R8G8\_UINT<sup>FCS</sup> (50)</span></span>
| <span data-ttu-id="a1cc3-3461">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3461">Target</span></span> | <span data-ttu-id="a1cc3-3462">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3462">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-3463">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3463">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-3464">16</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3464">16</span></span> |
| <span data-ttu-id="a1cc3-3465">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3465">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3467">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3467">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3469">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3469">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3471">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3471">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3472">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3472">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3473">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3473">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3475">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3475">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3477">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3477">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3479">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3479">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3481">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3481">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3483">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3483">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3484">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3484">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3485">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3485">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3486">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3486">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-3487">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3487">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-3488">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3488">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3490">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3490">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-3491">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3491">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3493">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3493">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-3494">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3494">Output Merger Logic Op</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-3496">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3496">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-3497">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3497">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-3498">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3498">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-3499">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3499">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-3500">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3500">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-3501">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3501">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-3502">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3502">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-3503">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3503">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-3504">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3504">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-3505">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3505">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-3506">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3506">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3507">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3507">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3508">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3508">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3510">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3510">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3512">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3512">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-3514">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3514">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-3516">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3516">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-3517">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3517">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3519">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3519">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-3520">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3520">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3522">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3522">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-3523">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3523">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-3524">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3524">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-3525">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3525">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-3526">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3526">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_snormsupfcssup-51"></a><span data-ttu-id="a1cc3-3527">\_SNORM<sup>FCS</sup> de DXGI_FORMAT_R8G8 (51)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3527">DXGI_FORMAT_R8G8\_SNORM<sup>FCS</sup> (51)</span></span>
| <span data-ttu-id="a1cc3-3528">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3528">Target</span></span> | <span data-ttu-id="a1cc3-3529">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3529">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-3530">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3530">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-3531">16</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3531">16</span></span> |
| <span data-ttu-id="a1cc3-3532">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3532">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3534">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3534">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3536">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3536">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3538">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3538">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3539">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3539">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3540">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3540">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3542">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3542">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3544">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3544">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3546">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3546">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3548">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3548">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3550">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3550">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3552">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3552">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3553">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3553">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3554">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3554">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-3555">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3555">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-3556">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3556">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3558">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3558">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3560">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3560">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3562">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3562">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3564">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3564">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-3565">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3565">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-3566">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3566">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-3567">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3567">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-3568">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3568">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-3569">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3569">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-3570">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3570">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-3571">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3571">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-3572">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3572">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-3573">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3573">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-3574">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3574">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-3575">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3575">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3576">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3576">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3577">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3577">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3579">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3579">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3581">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3581">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-3583">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3583">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-3585">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3585">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3587">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3587">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3589">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3589">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-3590">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3590">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3592">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3592">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-3593">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3593">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-3594">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3594">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-3595">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3595">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-3596">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3596">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_sintsupfcssup-52"></a><span data-ttu-id="a1cc3-3597">\_<sup>FCS</sup> DXGI_FORMAT_R8G8 Santo (52)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3597">DXGI_FORMAT_R8G8\_SINT<sup>FCS</sup> (52)</span></span>
| <span data-ttu-id="a1cc3-3598">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3598">Target</span></span> | <span data-ttu-id="a1cc3-3599">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3599">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-3600">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3600">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-3601">16</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3601">16</span></span> |
| <span data-ttu-id="a1cc3-3602">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3602">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3604">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3604">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3606">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3606">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3608">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3608">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3609">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3609">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3610">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3610">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3612">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3612">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3614">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3614">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3616">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3616">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3618">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3618">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3620">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3620">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3621">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3621">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3622">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3622">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3623">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3623">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-3624">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3624">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-3625">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3625">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3627">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3627">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-3628">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3628">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3630">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3630">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-3631">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3631">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-3632">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3632">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-3633">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3633">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-3634">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3634">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-3635">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3635">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-3636">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3636">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-3637">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3637">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-3638">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3638">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-3639">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3639">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-3640">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3640">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-3641">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3641">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-3642">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3642">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3643">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3643">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3644">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3644">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3646">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3646">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3648">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3648">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-3650">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3650">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-3652">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3652">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-3653">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3653">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3655">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3655">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-3656">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3656">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3658">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3658">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-3659">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3659">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-3660">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3660">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-3661">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3661">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-3662">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3662">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="a1cc3-3663">DXGI_FORMAT_R16 \_ <sup>PCs</sup> não tipados (53)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3663">DXGI_FORMAT_R16\_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="a1cc3-3664">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3664">Target</span></span> | <span data-ttu-id="a1cc3-3665">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3665">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-3666">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3666">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-3667">16</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3667">16</span></span> |
| <span data-ttu-id="a1cc3-3668">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3668">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3670">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3670">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3671">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3671">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3672">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3672">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3673">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3673">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3674">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3674">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3676">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3676">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3678">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3678">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3680">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3680">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3682">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3682">Shader ld</span></span> | \- |
| <span data-ttu-id="a1cc3-3683">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3683">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3684">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3684">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3685">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3685">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3686">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3686">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-3687">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3687">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-3688">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3688">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3690">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3690">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-3691">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3691">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-3692">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3692">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-3693">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3693">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-3694">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3694">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-3695">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3695">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-3696">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3696">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-3697">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3697">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-3698">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3698">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-3699">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3699">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-3700">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3700">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-3701">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3701">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-3702">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3702">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-3703">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3703">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-3704">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3704">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3705">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3705">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3706">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3706">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3708">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3708">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-3709">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3709">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-3710">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3710">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-3711">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3711">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-3712">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3712">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-3713">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3713">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-3714">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3714">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3716">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3716">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-3717">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3717">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-3718">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3718">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-3719">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3719">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3721">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3721">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_floatsupfcssup-54"></a><span data-ttu-id="a1cc3-3722">\_<sup>FCS</sup> de DXGI_FORMAT_R16 float (54)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3722">DXGI_FORMAT_R16\_FLOAT<sup>FCS</sup> (54)</span></span>
| <span data-ttu-id="a1cc3-3723">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3723">Target</span></span> | <span data-ttu-id="a1cc3-3724">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3724">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-3725">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3725">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-3726">16</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3726">16</span></span> |
| <span data-ttu-id="a1cc3-3727">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3727">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3729">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3729">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3731">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3731">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3733">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3733">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3734">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3734">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3735">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3735">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3737">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3737">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3739">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3739">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3741">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3741">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3743">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3743">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3745">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3745">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3747">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3747">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3748">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3748">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3749">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3749">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3751">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3751">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-3752">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3752">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3754">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3754">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3756">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3756">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3758">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3758">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3760">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3760">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-3761">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3761">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-3762">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3762">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-3763">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3763">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-3764">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3764">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-3765">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3765">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-3766">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3766">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-3767">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3767">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-3768">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3768">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-3769">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3769">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-3770">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3770">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-3771">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3771">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3772">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3772">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3773">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3773">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3775">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3775">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3777">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3777">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-3779">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3779">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-3781">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3781">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3783">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3783">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3785">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3785">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-3786">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3786">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3788">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3788">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-3789">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3789">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-3790">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3790">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-3791">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3791">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3793">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3793">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d16_unormsupfcssup-55"></a><span data-ttu-id="a1cc3-3794">\_UNORM<sup>FCS</sup> de DXGI_FORMAT_D16 (55)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3794">DXGI_FORMAT_D16\_UNORM<sup>FCS</sup> (55)</span></span>
| <span data-ttu-id="a1cc3-3795">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3795">Target</span></span> | <span data-ttu-id="a1cc3-3796">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3796">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-3797">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3797">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-3798">16</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3798">16</span></span> |
| <span data-ttu-id="a1cc3-3799">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3799">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3801">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3801">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3802">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3802">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3803">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3803">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3804">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3804">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3805">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3805">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3807">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3807">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3809">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3809">Texture3D</span></span> | \- |
| <span data-ttu-id="a1cc3-3810">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3810">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3812">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3812">Shader ld</span></span> | \- |
| <span data-ttu-id="a1cc3-3813">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3813">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3814">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3814">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3815">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3815">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3816">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3816">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-3817">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3817">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-3818">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3818">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3820">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3820">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-3821">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3821">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-3822">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3822">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-3823">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3823">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-3824">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3824">Depth/Stencil Target</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3826">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3826">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-3827">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3827">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-3828">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3828">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-3829">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3829">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-3830">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3830">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-3831">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3831">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-3832">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3832">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-3833">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3833">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-3834">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3834">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-3835">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3835">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3836">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3836">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3837">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3837">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3839">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3839">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3841">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3841">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-3843">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3843">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-3845">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3845">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-3846">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3846">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-3847">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3847">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-3848">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3848">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3850">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3850">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-3851">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3851">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-3852">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3852">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-3853">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3853">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3855">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3855">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_unormsupfcssup-56"></a><span data-ttu-id="a1cc3-3856">\_UNORM<sup>FCS</sup> de DXGI_FORMAT_R16 (56)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3856">DXGI_FORMAT_R16\_UNORM<sup>FCS</sup> (56)</span></span>
| <span data-ttu-id="a1cc3-3857">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3857">Target</span></span> | <span data-ttu-id="a1cc3-3858">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3858">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-3859">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3859">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-3860">16</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3860">16</span></span> |
| <span data-ttu-id="a1cc3-3861">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3861">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3863">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3863">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3865">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3865">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3867">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3867">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3868">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3868">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3869">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3869">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3871">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3871">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3873">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3873">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3875">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3875">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3877">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3877">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3879">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3879">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3881">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3881">Shader sample\_c (comparison filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3883">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3883">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3884">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3884">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3886">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3886">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-3887">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3887">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3889">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3889">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3891">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3891">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3893">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3893">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3895">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3895">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-3896">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3896">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-3897">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3897">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-3898">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3898">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-3899">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3899">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-3900">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3900">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-3901">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3901">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-3902">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3902">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-3903">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3903">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-3904">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3904">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-3905">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3905">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-3906">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3906">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3907">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3907">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3908">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3908">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3910">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3910">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3912">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3912">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-3914">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3914">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-3916">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3916">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3918">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3918">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3920">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3920">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-3921">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3921">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3923">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3923">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-3924">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3924">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-3925">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3925">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-3926">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3926">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3928">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3928">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_uintsupfcssup-57"></a><span data-ttu-id="a1cc3-3929">\_<sup>FCS</sup> DXGI_FORMAT_R16 uint (57)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3929">DXGI_FORMAT_R16\_UINT<sup>FCS</sup> (57)</span></span>
| <span data-ttu-id="a1cc3-3930">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3930">Target</span></span> | <span data-ttu-id="a1cc3-3931">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3931">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-3932">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3932">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-3933">16</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3933">16</span></span> |
| <span data-ttu-id="a1cc3-3934">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3934">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3936">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3936">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3938">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3938">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3940">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3940">Input Assembler Index Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3942">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3942">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-3943">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3943">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3945">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3945">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3947">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3947">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3949">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3949">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3951">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3951">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3953">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3953">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3954">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3954">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3955">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3955">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-3956">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3956">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-3957">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3957">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-3958">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3958">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3960">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3960">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-3961">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3961">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3963">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3963">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-3964">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3964">Output Merger Logic Op</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-3966">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3966">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-3967">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3967">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-3968">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3968">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-3969">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3969">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-3970">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3970">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-3971">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3971">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-3972">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3972">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-3973">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3973">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-3974">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3974">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-3975">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3975">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-3976">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3976">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3977">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3977">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-3978">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3978">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3980">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3980">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3982">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3982">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-3984">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3984">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-3986">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3986">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-3987">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3987">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3989">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3989">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-3990">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3990">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3992">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3992">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-3993">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3993">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-3994">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3994">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-3995">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3995">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-3997">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3997">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_snormsupfcssup-58"></a><span data-ttu-id="a1cc3-3998">\_SNORM<sup>FCS</sup> de DXGI_FORMAT_R16 (58)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3998">DXGI_FORMAT_R16\_SNORM<sup>FCS</sup> (58)</span></span>
| <span data-ttu-id="a1cc3-3999">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-3999">Target</span></span> | <span data-ttu-id="a1cc3-4000">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4000">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-4001">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4001">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-4002">16</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4002">16</span></span> |
| <span data-ttu-id="a1cc3-4003">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4003">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4005">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4005">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4007">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4007">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4009">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4009">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4010">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4010">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4011">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4011">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4013">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4013">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4015">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4015">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4017">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4017">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4019">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4019">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4021">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4021">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4023">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4023">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4024">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4024">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4025">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4025">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4027">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4027">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-4028">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4028">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4030">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4030">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4032">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4032">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4034">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4034">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4036">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4036">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-4037">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4037">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-4038">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4038">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4039">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4039">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4040">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4040">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-4041">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4041">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-4042">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4042">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-4043">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4043">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-4044">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4044">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-4045">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4045">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-4046">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4046">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-4047">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4047">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-4048">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4048">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-4049">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4049">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4051">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4051">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4053">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4053">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-4055">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4055">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-4057">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4057">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4059">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4059">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4061">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4061">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-4062">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4062">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4064">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4064">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-4065">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4065">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-4066">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4066">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-4067">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4067">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4069">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4069">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_sintsupfcssup-59"></a><span data-ttu-id="a1cc3-4070">\_<sup>FCS</sup> DXGI_FORMAT_R16 Santo (59)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4070">DXGI_FORMAT_R16\_SINT<sup>FCS</sup> (59)</span></span>
| <span data-ttu-id="a1cc3-4071">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4071">Target</span></span> | <span data-ttu-id="a1cc3-4072">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4072">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-4073">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4073">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-4074">16</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4074">16</span></span> |
| <span data-ttu-id="a1cc3-4075">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4075">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4077">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4077">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4079">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4079">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4081">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4081">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4082">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4082">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4083">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4083">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4085">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4085">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4087">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4087">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4089">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4089">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4091">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4091">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4093">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4093">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4094">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4094">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4095">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4095">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4096">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4096">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-4097">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4097">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-4098">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4098">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4100">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4100">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-4101">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4101">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4103">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4103">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4104">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4104">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-4105">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4105">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-4106">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4106">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4107">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4107">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4108">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4108">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-4109">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4109">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-4110">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4110">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-4111">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4111">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-4112">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4112">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-4113">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4113">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-4114">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4114">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-4115">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4115">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-4116">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4116">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-4117">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4117">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4119">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4119">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4121">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4121">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-4123">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4123">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-4125">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4125">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-4126">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4126">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4128">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4128">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-4129">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4129">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4131">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4131">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-4132">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4132">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-4133">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4133">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-4134">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4134">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4136">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4136">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="a1cc3-4137">DXGI_FORMAT_R8 \_ <sup>PCs</sup> não tipados (60)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4137">DXGI_FORMAT_R8\_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="a1cc3-4138">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4138">Target</span></span> | <span data-ttu-id="a1cc3-4139">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4139">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-4140">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4140">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-4141">8</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4141">8</span></span> |
| <span data-ttu-id="a1cc3-4142">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4142">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4144">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4144">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4145">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4145">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4146">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4146">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4147">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4147">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4148">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4148">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4150">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4150">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4152">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4152">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4154">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4154">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4156">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4156">Shader ld</span></span> | \- |
| <span data-ttu-id="a1cc3-4157">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4157">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4158">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4158">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4159">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4159">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4160">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4160">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-4161">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4161">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-4162">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4162">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4164">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4164">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-4165">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4165">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4166">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4166">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4167">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4167">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-4168">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4168">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-4169">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4169">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4170">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4170">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4171">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4171">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-4172">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4172">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-4173">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4173">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-4174">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4174">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-4175">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4175">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-4176">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4176">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-4177">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4177">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-4178">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4178">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-4179">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4179">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-4180">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4180">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4182">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4182">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4183">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4183">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4184">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4184">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-4185">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4185">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-4186">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4186">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-4187">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4187">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-4188">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4188">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4190">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4190">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-4191">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4191">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-4192">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4192">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-4193">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4193">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4195">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4195">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_unormsupfcssup-61"></a><span data-ttu-id="a1cc3-4196">\_UNORM<sup>FCS</sup> de DXGI_FORMAT_R8 (61)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4196">DXGI_FORMAT_R8\_UNORM<sup>FCS</sup> (61)</span></span>
| <span data-ttu-id="a1cc3-4197">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4197">Target</span></span> | <span data-ttu-id="a1cc3-4198">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4198">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-4199">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4199">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-4200">8</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4200">8</span></span> |
| <span data-ttu-id="a1cc3-4201">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4201">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4203">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4203">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4205">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4205">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4207">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4207">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4208">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4208">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4209">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4209">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4211">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4211">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4213">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4213">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4215">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4215">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4217">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4217">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4219">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4219">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4221">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4221">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4222">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4222">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4223">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4223">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4225">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4225">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-4226">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4226">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4228">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4228">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4230">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4230">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4232">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4232">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4234">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4234">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-4235">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4235">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-4236">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4236">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4237">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4237">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4238">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4238">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-4239">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4239">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-4240">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4240">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-4241">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4241">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-4242">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4242">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-4243">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4243">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-4244">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4244">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-4245">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4245">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-4246">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4246">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-4247">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4247">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4249">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4249">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4251">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4251">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-4253">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4253">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-4255">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4255">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4257">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4257">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4259">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4259">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-4260">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4260">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4262">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4262">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-4263">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4263">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-4264">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4264">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-4265">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4265">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4267">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4267">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_uintsupfcssup-62"></a><span data-ttu-id="a1cc3-4268">\_<sup>FCS</sup> DXGI_FORMAT_R8 uint (62)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4268">DXGI_FORMAT_R8\_UINT<sup>FCS</sup> (62)</span></span>
| <span data-ttu-id="a1cc3-4269">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4269">Target</span></span> | <span data-ttu-id="a1cc3-4270">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4270">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-4271">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4271">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-4272">8</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4272">8</span></span> |
| <span data-ttu-id="a1cc3-4273">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4273">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4275">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4275">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4277">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4277">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4279">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4279">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4280">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4280">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4281">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4281">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4283">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4283">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4285">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4285">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4287">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4287">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4289">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4289">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4291">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4291">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4292">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4292">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4293">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4293">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4294">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4294">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-4295">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4295">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-4296">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4296">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4298">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4298">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-4299">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4299">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4301">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4301">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4302">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4302">Output Merger Logic Op</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-4304">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4304">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-4305">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4305">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4306">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4306">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4307">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4307">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-4308">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4308">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-4309">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4309">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-4310">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4310">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-4311">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4311">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-4312">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4312">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-4313">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4313">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-4314">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4314">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-4315">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4315">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-4316">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4316">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4318">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4318">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4320">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4320">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-4322">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4322">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-4324">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4324">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-4325">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4325">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4327">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4327">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-4328">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4328">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4330">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4330">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-4331">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4331">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-4332">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4332">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-4333">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4333">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4335">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4335">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_snormsupfcssup-63"></a><span data-ttu-id="a1cc3-4336">\_SNORM<sup>FCS</sup> de DXGI_FORMAT_R8 (63)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4336">DXGI_FORMAT_R8\_SNORM<sup>FCS</sup> (63)</span></span>
| <span data-ttu-id="a1cc3-4337">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4337">Target</span></span> | <span data-ttu-id="a1cc3-4338">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4338">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-4339">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4339">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-4340">8</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4340">8</span></span> |
| <span data-ttu-id="a1cc3-4341">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4341">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4343">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4343">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4345">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4345">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4347">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4347">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4348">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4348">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4349">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4349">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4351">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4351">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4353">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4353">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4355">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4355">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4357">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4357">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4359">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4359">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4361">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4361">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4362">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4362">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4363">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4363">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4365">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4365">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-4366">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4366">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4368">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4368">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4370">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4370">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4372">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4372">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4374">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4374">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-4375">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4375">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-4376">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4376">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4377">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4377">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4378">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4378">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-4379">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4379">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-4380">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4380">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-4381">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4381">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-4382">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4382">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-4383">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4383">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-4384">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4384">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-4385">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4385">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-4386">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4386">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-4387">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4387">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4389">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4389">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4391">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4391">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-4393">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4393">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-4395">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4395">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4397">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4397">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4399">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4399">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-4400">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4400">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4402">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4402">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-4403">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4403">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-4404">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4404">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-4405">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4405">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4407">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4407">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_sintsupfcssup-64"></a><span data-ttu-id="a1cc3-4408">\_<sup>FCS</sup> DXGI_FORMAT_R8 Santo (64)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4408">DXGI_FORMAT_R8\_SINT<sup>FCS</sup> (64)</span></span>
| <span data-ttu-id="a1cc3-4409">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4409">Target</span></span> | <span data-ttu-id="a1cc3-4410">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4410">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-4411">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4411">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-4412">8</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4412">8</span></span> |
| <span data-ttu-id="a1cc3-4413">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4413">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4415">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4415">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4417">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4417">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4419">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4419">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4420">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4420">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4421">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4421">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4423">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4423">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4425">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4425">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4427">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4427">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4429">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4429">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4431">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4431">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4432">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4432">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4433">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4433">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4434">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4434">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-4435">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4435">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-4436">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4436">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4438">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4438">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-4439">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4439">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4441">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4441">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4442">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4442">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-4443">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4443">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-4444">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4444">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4445">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4445">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4446">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4446">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-4447">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4447">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-4448">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4448">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-4449">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4449">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-4450">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4450">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-4451">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4451">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-4452">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4452">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-4453">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4453">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-4454">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4454">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-4455">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4455">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4457">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4457">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4459">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4459">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-4461">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4461">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-4463">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4463">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-4464">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4464">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4466">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4466">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-4467">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4467">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4469">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4469">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-4470">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4470">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-4471">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4471">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-4472">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4472">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4474">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4474">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="a1cc3-4475">DXGI_FORMAT_A8 \_ UNORM<sup>FNS</sup> (65)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4475">DXGI_FORMAT_A8\_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="a1cc3-4476">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4476">Target</span></span> | <span data-ttu-id="a1cc3-4477">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4477">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-4478">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4478">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-4479">8</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4479">8</span></span> |
| <span data-ttu-id="a1cc3-4480">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4480">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4482">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4482">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4483">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4483">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4484">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4484">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4485">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4485">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4486">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4486">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4488">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4488">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4490">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4490">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4492">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4492">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4494">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4494">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4496">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4496">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4498">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4498">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4499">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4499">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4500">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4500">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-4501">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4501">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-4502">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4502">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4504">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4504">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4506">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4506">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4508">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4508">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4510">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4510">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-4511">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4511">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-4512">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4512">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4513">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4513">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4514">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4514">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-4515">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4515">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-4516">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4516">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-4517">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4517">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-4518">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4518">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-4519">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4519">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-4520">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4520">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-4521">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4521">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-4522">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4522">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-4523">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4523">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4525">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4525">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4527">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4527">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-4529">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4529">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-4531">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4531">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4533">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4533">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4535">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4535">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-4536">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4536">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a1cc3-4537">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4537">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-4538">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4538">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-4539">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4539">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-4540">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4540">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4542">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4542">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="a1cc3-4543">DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4543">DXGI_FORMAT_R9G9B9E5\_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="a1cc3-4544">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4544">Target</span></span> | <span data-ttu-id="a1cc3-4545">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4545">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-4546">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4546">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-4547">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4547">32</span></span> |
| <span data-ttu-id="a1cc3-4548">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4548">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4550">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4550">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4551">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4551">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4552">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4552">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4553">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4553">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4554">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4554">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4556">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4556">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4558">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4558">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4560">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4560">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4562">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4562">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4564">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4564">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4566">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4566">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4567">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4567">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4568">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4568">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-4569">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4569">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-4570">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4570">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4572">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4572">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-4573">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4573">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4574">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4574">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4575">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4575">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-4576">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4576">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-4577">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4577">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4578">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4578">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4579">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4579">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-4580">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4580">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-4581">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4581">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-4582">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4582">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-4583">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4583">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-4584">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4584">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-4585">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4585">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-4586">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4586">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-4587">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4587">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-4588">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4588">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4590">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4590">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4591">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4591">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4592">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4592">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-4593">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4593">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-4594">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4594">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-4595">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4595">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-4596">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4596">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a1cc3-4597">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4597">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-4598">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4598">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-4599">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4599">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-4600">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4600">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-4601">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4601">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="a1cc3-4602">DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4602">DXGI_FORMAT_R8G8\_B8G8\_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="a1cc3-4603">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4603">Target</span></span> | <span data-ttu-id="a1cc3-4604">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4604">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-4605">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4605">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-4606">16</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4606">16</span></span> |
| <span data-ttu-id="a1cc3-4607">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4607">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4609">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4609">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4610">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4610">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4611">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4611">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4612">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4612">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4613">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4613">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4615">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4615">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4617">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4617">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4619">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4619">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4621">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4621">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4623">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4623">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4625">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4625">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4626">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4626">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4627">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4627">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-4628">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4628">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-4629">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4629">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4631">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4631">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-4632">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4632">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4633">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4633">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4634">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4634">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-4635">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4635">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-4636">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4636">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4637">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4637">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4638">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4638">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-4639">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4639">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-4640">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4640">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-4641">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4641">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-4642">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4642">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-4643">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4643">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-4644">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4644">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-4645">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4645">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-4646">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4646">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-4647">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4647">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4649">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4649">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4650">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4650">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4651">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4651">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-4652">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4652">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-4653">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4653">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-4654">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4654">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-4655">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4655">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a1cc3-4656">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4656">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-4657">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4657">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-4658">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4658">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-4659">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4659">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-4660">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4660">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="a1cc3-4661">DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>FNC</sup> (69)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4661">DXGI_FORMAT_G8R8\_G8B8\_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="a1cc3-4662">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4662">Target</span></span> | <span data-ttu-id="a1cc3-4663">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4663">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-4664">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4664">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-4665">16</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4665">16</span></span> |
| <span data-ttu-id="a1cc3-4666">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4666">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4668">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4668">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4669">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4669">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4670">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4670">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4671">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4671">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4672">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4672">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4674">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4674">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4676">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4676">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4678">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4678">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4680">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4680">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4682">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4682">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4684">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4684">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4685">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4685">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4686">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4686">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-4687">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4687">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-4688">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4688">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4690">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4690">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-4691">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4691">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4692">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4692">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4693">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4693">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-4694">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4694">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-4695">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4695">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4696">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4696">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4697">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4697">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-4698">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4698">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-4699">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4699">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-4700">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4700">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-4701">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4701">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-4702">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4702">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-4703">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4703">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-4704">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4704">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-4705">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4705">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-4706">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4706">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4708">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4708">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4709">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4709">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4710">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4710">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-4711">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4711">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-4712">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4712">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-4713">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4713">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-4714">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4714">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a1cc3-4715">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4715">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-4716">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4716">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-4717">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4717">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-4718">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4718">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-4719">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4719">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="a1cc3-4720">DXGI_FORMAT_BC1 \_ <sup>PCC</sup> de tipo (70)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4720">DXGI_FORMAT_BC1\_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="a1cc3-4721">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4721">Target</span></span> | <span data-ttu-id="a1cc3-4722">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4722">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-4723">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4723">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-4724">4</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4724">4</span></span> |
| <span data-ttu-id="a1cc3-4725">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4725">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4727">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4727">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4728">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4728">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4729">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4729">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4730">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4730">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4731">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4731">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-4732">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4732">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4734">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4734">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4736">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4736">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4738">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4738">Shader ld</span></span> | \- |
| <span data-ttu-id="a1cc3-4739">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4739">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4740">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4740">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4741">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4741">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4742">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4742">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-4743">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4743">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-4744">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4744">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4746">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4746">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-4747">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4747">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4748">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4748">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4749">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4749">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-4750">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4750">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-4751">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4751">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4752">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4752">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4753">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4753">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-4754">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4754">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-4755">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4755">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-4756">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4756">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-4757">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4757">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-4758">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4758">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-4759">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4759">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-4760">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4760">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-4761">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4761">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-4762">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4762">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4764">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4764">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4765">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4765">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4766">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4766">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-4767">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4767">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-4768">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4768">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-4769">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4769">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-4770">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4770">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4772">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4772">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-4773">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4773">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-4774">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4774">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-4775">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4775">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4777">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4777">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unormsupfccsup-71"></a><span data-ttu-id="a1cc3-4778">DXGI_FORMAT_BC1 \_ UNORM<sup>FCC</sup> (71)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4778">DXGI_FORMAT_BC1\_UNORM<sup>FCC</sup> (71)</span></span>
| <span data-ttu-id="a1cc3-4779">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4779">Target</span></span> | <span data-ttu-id="a1cc3-4780">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4780">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-4781">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4781">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-4782">4</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4782">4</span></span> |
| <span data-ttu-id="a1cc3-4783">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4783">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4785">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4785">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4786">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4786">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4787">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4787">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4788">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4788">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4789">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4789">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-4790">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4790">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4792">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4792">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4794">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4794">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4796">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4796">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4798">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4798">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4800">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4800">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4801">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4801">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4802">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4802">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-4803">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4803">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-4804">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4804">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4806">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4806">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-4807">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4807">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4808">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4808">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4809">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4809">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-4810">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4810">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-4811">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4811">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4812">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4812">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4813">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4813">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-4814">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4814">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-4815">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4815">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-4816">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4816">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-4817">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4817">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-4818">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4818">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-4819">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4819">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-4820">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4820">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-4821">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4821">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-4822">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4822">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4824">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4824">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4825">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4825">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4826">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4826">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-4827">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4827">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-4828">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4828">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-4829">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4829">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-4830">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4830">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4832">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4832">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-4833">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4833">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-4834">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4834">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-4835">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4835">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4837">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4837">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfccsup-72"></a><span data-ttu-id="a1cc3-4838">DXGI_FORMAT_BC1 \_ UNORM \_ sRGB<sup>FCC</sup> (72)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4838">DXGI_FORMAT_BC1\_UNORM\_SRGB<sup>FCC</sup> (72)</span></span>
| <span data-ttu-id="a1cc3-4839">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4839">Target</span></span> | <span data-ttu-id="a1cc3-4840">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4840">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-4841">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4841">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-4842">4</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4842">4</span></span> |
| <span data-ttu-id="a1cc3-4843">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4843">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4845">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4845">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4846">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4846">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4847">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4847">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4848">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4848">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4849">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4849">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-4850">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4850">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4852">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4852">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4854">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4854">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4856">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4856">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4858">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4858">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4860">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4860">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4861">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4861">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4862">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4862">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-4863">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4863">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-4864">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4864">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4866">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4866">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-4867">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4867">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4868">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4868">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4869">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4869">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-4870">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4870">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-4871">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4871">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4872">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4872">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4873">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4873">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-4874">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4874">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-4875">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4875">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-4876">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4876">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-4877">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4877">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-4878">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4878">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-4879">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4879">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-4880">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4880">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-4881">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4881">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-4882">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4882">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4884">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4884">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4885">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4885">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4886">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4886">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-4887">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4887">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-4888">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4888">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-4889">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4889">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-4890">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4890">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4892">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4892">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-4893">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4893">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-4894">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4894">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-4895">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4895">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4897">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4897">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="a1cc3-4898">DXGI_FORMAT_BC2 \_ <sup>PCC</sup> de tipo (73)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4898">DXGI_FORMAT_BC2\_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="a1cc3-4899">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4899">Target</span></span> | <span data-ttu-id="a1cc3-4900">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4900">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-4901">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4901">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-4902">8</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4902">8</span></span> |
| <span data-ttu-id="a1cc3-4903">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4903">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4905">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4905">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4906">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4906">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4907">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4907">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4908">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4908">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4909">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4909">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-4910">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4910">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4912">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4912">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4914">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4914">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4916">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4916">Shader ld</span></span> | \- |
| <span data-ttu-id="a1cc3-4917">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4917">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4918">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4918">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4919">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4919">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4920">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4920">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-4921">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4921">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-4922">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4922">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4924">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4924">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-4925">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4925">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4926">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4926">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4927">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4927">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-4928">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4928">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-4929">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4929">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4930">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4930">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4931">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4931">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-4932">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4932">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-4933">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4933">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-4934">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4934">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-4935">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4935">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-4936">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4936">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-4937">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4937">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-4938">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4938">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-4939">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4939">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-4940">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4940">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4942">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4942">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4943">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4943">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4944">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4944">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-4945">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4945">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-4946">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4946">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-4947">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4947">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-4948">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4948">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4950">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4950">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-4951">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4951">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-4952">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4952">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-4953">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4953">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4955">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4955">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unormsupfccsup-74"></a><span data-ttu-id="a1cc3-4956">DXGI_FORMAT_BC2 \_ UNORM<sup>FCC</sup> (74)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4956">DXGI_FORMAT_BC2\_UNORM<sup>FCC</sup> (74)</span></span>
| <span data-ttu-id="a1cc3-4957">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4957">Target</span></span> | <span data-ttu-id="a1cc3-4958">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4958">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-4959">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4959">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-4960">8</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4960">8</span></span> |
| <span data-ttu-id="a1cc3-4961">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4961">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4963">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4963">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4964">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4964">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4965">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4965">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4966">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4966">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-4967">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4967">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-4968">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4968">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4970">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4970">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4972">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4972">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4974">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4974">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4976">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4976">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4978">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4978">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4979">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4979">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-4980">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4980">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-4981">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4981">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-4982">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4982">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-4984">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4984">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-4985">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4985">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4986">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4986">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-4987">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4987">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-4988">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4988">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-4989">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4989">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4990">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4990">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-4991">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4991">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-4992">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4992">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-4993">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4993">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-4994">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4994">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-4995">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4995">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-4996">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4996">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-4997">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4997">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-4998">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4998">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-4999">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-4999">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5000">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5000">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5002">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5002">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5003">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5003">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5004">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5004">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-5005">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5005">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-5006">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5006">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-5007">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5007">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-5008">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5008">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5010">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5010">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-5011">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5011">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-5012">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5012">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-5013">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5013">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5015">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5015">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfccsup-75"></a><span data-ttu-id="a1cc3-5016">DXGI_FORMAT_BC2 \_ UNORM \_ sRGB<sup>FCC</sup> (75)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5016">DXGI_FORMAT_BC2\_UNORM\_SRGB<sup>FCC</sup> (75)</span></span>
| <span data-ttu-id="a1cc3-5017">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5017">Target</span></span> | <span data-ttu-id="a1cc3-5018">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5018">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-5019">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5019">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-5020">8</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5020">8</span></span> |
| <span data-ttu-id="a1cc3-5021">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5021">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5023">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5023">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5024">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5024">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5025">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5025">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5026">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5026">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5027">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5027">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-5028">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5028">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5030">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5030">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5032">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5032">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5034">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5034">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5036">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5036">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5038">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5038">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5039">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5039">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5040">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5040">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-5041">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5041">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-5042">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5042">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5044">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5044">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-5045">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5045">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5046">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5046">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5047">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5047">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-5048">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5048">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-5049">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5049">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5050">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5050">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5051">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5051">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-5052">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5052">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-5053">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5053">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-5054">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5054">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-5055">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5055">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-5056">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5056">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-5057">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5057">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-5058">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5058">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5059">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5059">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5060">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5060">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5062">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5062">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5063">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5063">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5064">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5064">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-5065">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5065">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-5066">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5066">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-5067">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5067">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-5068">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5068">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5070">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5070">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-5071">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5071">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-5072">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5072">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-5073">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5073">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5075">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5075">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="a1cc3-5076">DXGI_FORMAT_BC3 \_ <sup>PCC</sup> de tipo (76)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5076">DXGI_FORMAT_BC3\_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="a1cc3-5077">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5077">Target</span></span> | <span data-ttu-id="a1cc3-5078">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5078">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-5079">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5079">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-5080">8</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5080">8</span></span> |
| <span data-ttu-id="a1cc3-5081">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5081">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5083">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5083">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5084">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5084">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5085">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5085">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5086">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5086">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5087">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5087">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-5088">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5088">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5090">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5090">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5092">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5092">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5094">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5094">Shader ld</span></span> | \- |
| <span data-ttu-id="a1cc3-5095">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5095">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5096">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5096">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5097">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5097">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5098">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5098">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-5099">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5099">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-5100">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5100">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5102">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5102">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-5103">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5103">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5104">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5104">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5105">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5105">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-5106">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5106">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-5107">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5107">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5108">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5108">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5109">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5109">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-5110">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5110">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-5111">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5111">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-5112">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5112">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-5113">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5113">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-5114">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5114">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-5115">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5115">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-5116">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5116">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5117">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5117">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5118">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5118">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5120">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5120">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5121">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5121">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5122">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5122">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-5123">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5123">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-5124">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5124">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-5125">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5125">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-5126">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5126">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5128">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5128">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-5129">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5129">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-5130">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5130">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-5131">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5131">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5133">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5133">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unormsupfccsup-77"></a><span data-ttu-id="a1cc3-5134">DXGI_FORMAT_BC3 \_ UNORM<sup>FCC</sup> (77)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5134">DXGI_FORMAT_BC3\_UNORM<sup>FCC</sup> (77)</span></span>
| <span data-ttu-id="a1cc3-5135">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5135">Target</span></span> | <span data-ttu-id="a1cc3-5136">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5136">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-5137">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5137">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-5138">8</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5138">8</span></span> |
| <span data-ttu-id="a1cc3-5139">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5139">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5141">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5141">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5142">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5142">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5143">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5143">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5144">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5144">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5145">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5145">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-5146">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5146">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5148">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5148">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5150">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5150">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5152">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5152">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5154">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5154">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5156">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5156">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5157">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5157">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5158">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5158">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-5159">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5159">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-5160">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5160">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5162">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5162">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-5163">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5163">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5164">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5164">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5165">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5165">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-5166">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5166">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-5167">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5167">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5168">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5168">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5169">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5169">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-5170">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5170">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-5171">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5171">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-5172">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5172">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-5173">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5173">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-5174">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5174">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-5175">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5175">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-5176">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5176">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5177">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5177">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5178">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5178">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5180">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5180">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5181">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5181">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5182">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5182">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-5183">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5183">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-5184">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5184">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-5185">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5185">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-5186">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5186">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5188">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5188">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-5189">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5189">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-5190">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5190">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-5191">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5191">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5193">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5193">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfccsup-78"></a><span data-ttu-id="a1cc3-5194">DXGI_FORMAT_BC3 \_ UNORM \_ sRGB<sup>FCC</sup> (78)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5194">DXGI_FORMAT_BC3\_UNORM\_SRGB<sup>FCC</sup> (78)</span></span>
| <span data-ttu-id="a1cc3-5195">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5195">Target</span></span> | <span data-ttu-id="a1cc3-5196">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5196">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-5197">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5197">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-5198">8</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5198">8</span></span> |
| <span data-ttu-id="a1cc3-5199">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5199">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5201">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5201">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5202">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5202">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5203">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5203">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5204">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5204">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5205">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5205">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-5206">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5206">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5208">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5208">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5210">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5210">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5212">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5212">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5214">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5214">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5216">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5216">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5217">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5217">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5218">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5218">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-5219">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5219">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-5220">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5220">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5222">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5222">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-5223">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5223">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5224">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5224">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5225">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5225">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-5226">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5226">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-5227">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5227">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5228">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5228">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5229">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5229">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-5230">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5230">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-5231">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5231">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-5232">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5232">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-5233">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5233">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-5234">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5234">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-5235">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5235">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-5236">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5236">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5237">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5237">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5238">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5238">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5240">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5240">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5241">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5241">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5242">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5242">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-5243">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5243">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-5244">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5244">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-5245">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5245">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-5246">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5246">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5248">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5248">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-5249">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5249">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-5250">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5250">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-5251">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5251">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5253">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5253">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="a1cc3-5254">DXGI_FORMAT_BC4 \_ <sup>PCC</sup> de tipo (79)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5254">DXGI_FORMAT_BC4\_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="a1cc3-5255">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5255">Target</span></span> | <span data-ttu-id="a1cc3-5256">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5256">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-5257">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5257">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-5258">4</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5258">4</span></span> |
| <span data-ttu-id="a1cc3-5259">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5259">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5261">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5261">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5262">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5262">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5263">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5263">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5264">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5264">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5265">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5265">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-5266">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5266">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5268">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5268">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5270">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5270">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5272">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5272">Shader ld</span></span> | \- |
| <span data-ttu-id="a1cc3-5273">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5273">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5274">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5274">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5275">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5275">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5276">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5276">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-5277">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5277">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-5278">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5278">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5280">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5280">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-5281">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5281">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5282">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5282">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5283">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5283">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-5284">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5284">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-5285">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5285">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5286">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5286">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5287">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5287">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-5288">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5288">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-5289">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5289">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-5290">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5290">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-5291">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5291">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-5292">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5292">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-5293">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5293">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-5294">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5294">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5295">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5295">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5296">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5296">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5298">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5298">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5299">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5299">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5300">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5300">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-5301">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5301">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-5302">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5302">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-5303">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5303">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-5304">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5304">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5306">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5306">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-5307">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5307">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-5308">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5308">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-5309">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5309">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-5310">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5310">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_unormsupfccsup-80"></a><span data-ttu-id="a1cc3-5311">DXGI_FORMAT_BC4 \_ UNORM<sup>FCC</sup> (80)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5311">DXGI_FORMAT_BC4\_UNORM<sup>FCC</sup> (80)</span></span>
| <span data-ttu-id="a1cc3-5312">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5312">Target</span></span> | <span data-ttu-id="a1cc3-5313">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5313">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-5314">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5314">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-5315">4</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5315">4</span></span> |
| <span data-ttu-id="a1cc3-5316">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5316">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5318">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5318">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5319">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5319">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5320">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5320">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5321">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5321">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5322">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5322">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-5323">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5323">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5325">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5325">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5327">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5327">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5329">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5329">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5331">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5331">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5333">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5333">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5334">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5334">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5335">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5335">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-5336">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5336">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-5337">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5337">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5339">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5339">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-5340">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5340">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5341">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5341">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5342">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5342">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-5343">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5343">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-5344">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5344">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5345">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5345">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5346">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5346">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-5347">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5347">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-5348">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5348">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-5349">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5349">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-5350">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5350">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-5351">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5351">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-5352">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5352">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-5353">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5353">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5354">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5354">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5355">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5355">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5357">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5357">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5358">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5358">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5359">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5359">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-5360">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5360">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-5361">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5361">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-5362">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5362">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-5363">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5363">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5365">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5365">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-5366">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5366">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-5367">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5367">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-5368">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5368">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-5369">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5369">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_snormsupfccsup-81"></a><span data-ttu-id="a1cc3-5370">DXGI_FORMAT_BC4 \_ SNORM<sup>FCC</sup> (81)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5370">DXGI_FORMAT_BC4\_SNORM<sup>FCC</sup> (81)</span></span>
| <span data-ttu-id="a1cc3-5371">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5371">Target</span></span> | <span data-ttu-id="a1cc3-5372">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5372">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-5373">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5373">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-5374">4</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5374">4</span></span> |
| <span data-ttu-id="a1cc3-5375">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5375">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5377">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5377">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5378">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5378">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5379">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5379">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5380">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5380">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5381">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5381">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-5382">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5382">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5384">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5384">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5386">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5386">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5388">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5388">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5390">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5390">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5392">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5392">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5393">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5393">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5394">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5394">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-5395">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5395">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-5396">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5396">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5398">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5398">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-5399">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5399">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5400">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5400">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5401">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5401">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-5402">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5402">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-5403">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5403">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5404">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5404">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5405">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5405">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-5406">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5406">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-5407">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5407">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-5408">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5408">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-5409">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5409">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-5410">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5410">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-5411">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5411">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-5412">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5412">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5413">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5413">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5414">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5414">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5416">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5416">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5417">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5417">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5418">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5418">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-5419">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5419">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-5420">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5420">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-5421">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5421">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-5422">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5422">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5424">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5424">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-5425">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5425">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-5426">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5426">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-5427">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5427">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-5428">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5428">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="a1cc3-5429">DXGI_FORMAT_BC5 \_ <sup>PCC</sup> de tipo (82)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5429">DXGI_FORMAT_BC5\_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="a1cc3-5430">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5430">Target</span></span> | <span data-ttu-id="a1cc3-5431">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5431">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-5432">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5432">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-5433">8</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5433">8</span></span> |
| <span data-ttu-id="a1cc3-5434">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5434">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5436">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5436">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5437">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5437">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5438">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5438">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5439">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5439">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5440">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5440">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-5441">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5441">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5443">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5443">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5445">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5445">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5447">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5447">Shader ld</span></span> | \- |
| <span data-ttu-id="a1cc3-5448">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5448">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5449">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5449">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5450">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5450">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5451">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5451">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-5452">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5452">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-5453">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5453">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5455">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5455">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-5456">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5456">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5457">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5457">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5458">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5458">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-5459">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5459">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-5460">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5460">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5461">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5461">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5462">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5462">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-5463">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5463">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-5464">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5464">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-5465">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5465">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-5466">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5466">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-5467">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5467">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-5468">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5468">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-5469">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5469">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5470">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5470">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5471">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5471">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5473">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5473">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5474">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5474">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5475">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5475">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-5476">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5476">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-5477">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5477">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-5478">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5478">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-5479">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5479">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5481">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5481">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-5482">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5482">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-5483">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5483">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-5484">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5484">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-5485">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5485">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_unormsupfccsup-83"></a><span data-ttu-id="a1cc3-5486">DXGI_FORMAT_BC5 \_ UNORM<sup>FCC</sup> (83)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5486">DXGI_FORMAT_BC5\_UNORM<sup>FCC</sup> (83)</span></span>
| <span data-ttu-id="a1cc3-5487">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5487">Target</span></span> | <span data-ttu-id="a1cc3-5488">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5488">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-5489">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5489">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-5490">8</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5490">8</span></span> |
| <span data-ttu-id="a1cc3-5491">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5491">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5493">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5493">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5494">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5494">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5495">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5495">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5496">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5496">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5497">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5497">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-5498">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5498">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5500">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5500">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5502">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5502">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5504">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5504">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5506">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5506">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5508">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5508">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5509">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5509">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5510">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5510">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-5511">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5511">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-5512">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5512">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5514">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5514">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-5515">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5515">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5516">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5516">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5517">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5517">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-5518">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5518">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-5519">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5519">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5520">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5520">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5521">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5521">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-5522">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5522">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-5523">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5523">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-5524">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5524">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-5525">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5525">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-5526">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5526">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-5527">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5527">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-5528">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5528">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5529">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5529">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5530">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5530">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5532">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5532">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5533">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5533">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5534">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5534">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-5535">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5535">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-5536">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5536">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-5537">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5537">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-5538">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5538">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5540">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5540">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-5541">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5541">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-5542">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5542">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-5543">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5543">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-5544">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5544">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_snormsupfccsup-84"></a><span data-ttu-id="a1cc3-5545">DXGI_FORMAT_BC5 \_ SNORM<sup>FCC</sup> (84)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5545">DXGI_FORMAT_BC5\_SNORM<sup>FCC</sup> (84)</span></span>
| <span data-ttu-id="a1cc3-5546">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5546">Target</span></span> | <span data-ttu-id="a1cc3-5547">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5547">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-5548">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5548">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-5549">8</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5549">8</span></span> |
| <span data-ttu-id="a1cc3-5550">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5550">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5552">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5552">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5553">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5553">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5554">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5554">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5555">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5555">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5556">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5556">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-5557">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5557">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5559">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5559">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5561">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5561">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5563">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5563">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5565">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5565">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5567">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5567">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5568">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5568">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5569">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5569">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-5570">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5570">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-5571">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5571">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5573">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5573">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-5574">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5574">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5575">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5575">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5576">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5576">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-5577">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5577">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-5578">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5578">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5579">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5579">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5580">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5580">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-5581">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5581">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-5582">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5582">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-5583">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5583">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-5584">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5584">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-5585">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5585">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-5586">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5586">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-5587">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5587">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5588">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5588">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5589">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5589">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5591">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5591">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5592">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5592">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5593">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5593">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-5594">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5594">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-5595">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5595">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-5596">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5596">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-5597">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5597">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5599">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5599">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-5600">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5600">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-5601">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5601">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-5602">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5602">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-5603">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5603">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="a1cc3-5604">DXGI_FORMAT_B5G6R5 \_ UNORM<sup>FNS</sup> (85)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5604">DXGI_FORMAT_B5G6R5\_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="a1cc3-5605">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5605">Target</span></span> | <span data-ttu-id="a1cc3-5606">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5606">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-5607">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5607">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-5608">16</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5608">16</span></span> |
| <span data-ttu-id="a1cc3-5609">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5609">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5611">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5611">Buffer</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-5613">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5613">Input Assembler Vertex Buffer</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-5615">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5615">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5616">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5616">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5617">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5617">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5619">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5619">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5621">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5621">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5623">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5623">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5625">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5625">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5627">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5627">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5629">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5629">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5630">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5630">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5631">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5631">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-5632">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5632">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-5633">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5633">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5635">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5635">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5637">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5637">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5639">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5639">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5641">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5641">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-5642">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5642">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-5643">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5643">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5644">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5644">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5645">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5645">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-5646">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5646">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-5647">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5647">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-5648">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5648">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-5649">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5649">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-5650">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5650">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-5651">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5651">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-5652">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5652">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5653">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5653">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5654">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5654">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5656">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5656">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5658">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5658">8x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5660">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5660">Other Multisample Count RT</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5662">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5662">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5664">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5664">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5666">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5666">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-5667">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5667">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a1cc3-5668">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5668">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-5669">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5669">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-5670">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5670">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-5671">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5671">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-5672">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5672">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="a1cc3-5673">DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>FNS</sup> (86)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5673">DXGI_FORMAT_B5G5R5A1\_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="a1cc3-5674">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5674">Target</span></span> | <span data-ttu-id="a1cc3-5675">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5675">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-5676">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5676">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-5677">16</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5677">16</span></span> |
| <span data-ttu-id="a1cc3-5678">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5678">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5680">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5680">Buffer</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-5682">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5682">Input Assembler Vertex Buffer</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-5684">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5684">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5685">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5685">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5686">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5686">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5688">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5688">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5690">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5690">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5692">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5692">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5694">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5694">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5696">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5696">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5698">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5698">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5699">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5699">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5700">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5700">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-5701">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5701">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-5702">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5702">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5704">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5704">Mipmap Auto-Generation</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-5706">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5706">RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-5708">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5708">Blendable RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-5710">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5710">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-5711">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5711">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-5712">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5712">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5713">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5713">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5714">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5714">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-5715">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5715">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-5716">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5716">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-5717">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5717">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-5718">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5718">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-5719">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5719">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-5720">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5720">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-5721">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5721">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5722">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5722">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5723">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5723">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5725">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5725">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-5727">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5727">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-5729">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5729">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-5731">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5731">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5733">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5733">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-5735">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5735">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-5736">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5736">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a1cc3-5737">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5737">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-5738">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5738">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-5739">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5739">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-5740">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5740">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-5741">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5741">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="a1cc3-5742">DXGI_FORMAT_B8G8R8A8 \_ <sup>PCs</sup> não tipados (90)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5742">DXGI_FORMAT_B8G8R8A8\_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="a1cc3-5743">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5743">Target</span></span> | <span data-ttu-id="a1cc3-5744">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5744">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-5745">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5745">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-5746">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5746">32</span></span> |
| <span data-ttu-id="a1cc3-5747">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5747">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5749">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5749">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5750">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5750">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5751">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5751">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5752">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5752">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5753">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5753">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5755">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5755">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5757">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5757">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5759">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5759">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5761">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5761">Shader ld</span></span> | \- |
| <span data-ttu-id="a1cc3-5762">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5762">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5763">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5763">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5764">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5764">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5765">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5765">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-5766">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5766">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-5767">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5767">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5769">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5769">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-5770">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5770">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5771">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5771">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5772">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5772">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-5773">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5773">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-5774">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5774">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5775">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5775">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5776">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5776">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-5777">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5777">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-5778">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5778">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-5779">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5779">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-5780">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5780">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-5781">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5781">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-5782">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5782">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-5783">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5783">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5784">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5784">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5785">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5785">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5787">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5787">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5788">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5788">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5789">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5789">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-5790">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5790">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-5791">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5791">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-5792">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5792">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-5793">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5793">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5795">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5795">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-5796">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5796">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-5797">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5797">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-5798">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5798">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5800">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5800">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfcssup-87"></a><span data-ttu-id="a1cc3-5801">\_UNORM<sup>FCS</sup> de DXGI_FORMAT_B8G8R8A8 (87)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5801">DXGI_FORMAT_B8G8R8A8\_UNORM<sup>FCS</sup> (87)</span></span>
| <span data-ttu-id="a1cc3-5802">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5802">Target</span></span> | <span data-ttu-id="a1cc3-5803">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5803">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-5804">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5804">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-5805">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5805">32</span></span> |
| <span data-ttu-id="a1cc3-5806">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5806">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5808">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5808">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5810">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5810">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5812">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5812">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5813">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5813">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5814">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5814">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5816">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5816">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5818">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5818">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5820">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5820">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5822">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5822">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5824">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5824">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5826">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5826">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5827">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5827">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5828">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5828">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-5829">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5829">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-5830">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5830">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5832">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5832">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5834">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5834">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5836">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5836">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5838">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5838">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-5839">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5839">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-5840">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5840">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5841">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5841">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5842">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5842">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-5843">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5843">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-5844">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5844">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-5845">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5845">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-5846">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5846">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-5847">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5847">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-5848">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5848">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-5849">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5849">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5850">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5850">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5851">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5851">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5853">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5853">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5855">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5855">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-5857">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5857">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-5859">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5859">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5861">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5861">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-5863">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5863">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5865">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5865">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5867">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5867">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-5868">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5868">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-5870">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5870">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-5872">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5872">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5874">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5874">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfcssup-91"></a><span data-ttu-id="a1cc3-5875">\_FCS DXGI_FORMAT_B8G8R8A8 \_ UNORM<sup></sup> sRGB (91)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5875">DXGI_FORMAT_B8G8R8A8\_UNORM\_SRGB<sup>FCS</sup> (91)</span></span>
| <span data-ttu-id="a1cc3-5876">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5876">Target</span></span> | <span data-ttu-id="a1cc3-5877">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5877">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-5878">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5878">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-5879">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5879">32</span></span> |
| <span data-ttu-id="a1cc3-5880">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5880">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5882">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5882">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5883">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5883">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5884">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5884">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5885">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5885">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5886">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5886">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5888">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5888">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5890">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5890">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5892">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5892">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5894">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5894">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5896">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5896">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5898">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5898">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5899">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5899">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5900">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5900">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-5901">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5901">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-5902">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5902">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5904">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5904">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5906">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5906">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5908">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5908">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5910">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5910">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-5911">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5911">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-5912">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5912">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5913">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5913">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5914">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5914">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-5915">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5915">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-5916">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5916">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-5917">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5917">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-5918">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5918">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-5919">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5919">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-5920">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5920">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-5921">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5921">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5922">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5922">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5923">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5923">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5925">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5925">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5927">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5927">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-5929">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5929">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-5931">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5931">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5933">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5933">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5935">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5935">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5937">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5937">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5939">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5939">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-5940">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5940">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-5942">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5942">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-5944">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5944">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5946">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5946">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="a1cc3-5947">DXGI_FORMAT_B8G8R8X8 \_ <sup>PCs</sup> não tipados (92)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5947">DXGI_FORMAT_B8G8R8X8\_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="a1cc3-5948">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5948">Target</span></span> | <span data-ttu-id="a1cc3-5949">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5949">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-5950">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5950">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-5951">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5951">32</span></span> |
| <span data-ttu-id="a1cc3-5952">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5952">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5954">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5954">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5955">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5955">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5956">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5956">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5957">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5957">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-5958">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5958">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5960">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5960">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5962">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5962">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5964">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5964">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5966">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5966">Shader ld</span></span> | \- |
| <span data-ttu-id="a1cc3-5967">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5967">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5968">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5968">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5969">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5969">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-5970">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5970">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-5971">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5971">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-5972">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5972">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5974">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5974">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-5975">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5975">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5976">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5976">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5977">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5977">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-5978">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5978">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-5979">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5979">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5980">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5980">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-5981">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5981">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-5982">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5982">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-5983">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5983">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-5984">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5984">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-5985">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5985">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-5986">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5986">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-5987">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5987">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-5988">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5988">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5989">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5989">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-5990">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5990">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-5992">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5992">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5993">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5993">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-5994">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5994">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-5995">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5995">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-5996">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5996">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-5997">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5997">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-5998">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-5998">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6000">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6000">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-6001">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6001">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-6002">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6002">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-6003">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6003">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6005">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6005">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfcssup-88"></a><span data-ttu-id="a1cc3-6006">\_UNORM<sup>FCS</sup> de DXGI_FORMAT_B8G8R8X8 (88)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6006">DXGI_FORMAT_B8G8R8X8\_UNORM<sup>FCS</sup> (88)</span></span>
| <span data-ttu-id="a1cc3-6007">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6007">Target</span></span> | <span data-ttu-id="a1cc3-6008">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6008">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-6009">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6009">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-6010">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6010">32</span></span> |
| <span data-ttu-id="a1cc3-6011">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6011">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6013">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6013">Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6015">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6015">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6017">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6017">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6018">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6018">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6019">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6019">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6021">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6021">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6023">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6023">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6025">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6025">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6027">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6027">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6029">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6029">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6031">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6031">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6032">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6032">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6033">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6033">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-6034">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6034">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-6035">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6035">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6037">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6037">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6039">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6039">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6041">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6041">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6043">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6043">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-6044">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6044">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-6045">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6045">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6046">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6046">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6047">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6047">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-6048">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6048">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-6049">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6049">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-6050">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6050">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-6051">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6051">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-6052">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6052">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-6053">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6053">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-6054">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6054">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6055">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6055">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6056">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6056">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6058">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6058">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6060">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6060">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6062">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6062">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6064">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6064">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6066">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6066">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6068">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6068">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-6069">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6069">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6071">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6071">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-6072">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6072">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6074">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6074">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6076">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6076">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6078">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6078">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfcssup-93"></a><span data-ttu-id="a1cc3-6079">\_FCS DXGI_FORMAT_B8G8R8X8 \_ UNORM<sup></sup> sRGB (93)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6079">DXGI_FORMAT_B8G8R8X8\_UNORM\_SRGB<sup>FCS</sup> (93)</span></span>
| <span data-ttu-id="a1cc3-6080">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6080">Target</span></span> | <span data-ttu-id="a1cc3-6081">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6081">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-6082">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6082">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-6083">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6083">32</span></span> |
| <span data-ttu-id="a1cc3-6084">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6084">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6086">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6086">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6087">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6087">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6088">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6088">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6089">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6089">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6090">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6090">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6092">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6092">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6094">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6094">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6096">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6096">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6098">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6098">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6100">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6100">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6102">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6102">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6103">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6103">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6104">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6104">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-6105">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6105">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-6106">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6106">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6108">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6108">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6110">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6110">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6112">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6112">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6114">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6114">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-6115">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6115">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-6116">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6116">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6117">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6117">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6118">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6118">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-6119">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6119">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-6120">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6120">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-6121">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6121">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-6122">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6122">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-6123">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6123">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-6124">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6124">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-6125">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6125">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6126">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6126">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6127">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6127">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6129">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6129">4x Multisample RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6131">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6131">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6133">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6133">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6135">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6135">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6137">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6137">Multisample Load</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6139">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6139">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-6140">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6140">Cast Within Bit Layout</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6142">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6142">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-6143">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6143">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-6144">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6144">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-6145">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6145">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6147">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6147">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="a1cc3-6148">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6148">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="a1cc3-6149">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6149">Target</span></span> | <span data-ttu-id="a1cc3-6150">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6150">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-6151">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6151">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-6152">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6152">32</span></span> |
| <span data-ttu-id="a1cc3-6153">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6153">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6155">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6155">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6156">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6156">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6157">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6157">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6158">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6158">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6159">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6159">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-6160">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6160">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6162">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6162">Texture3D</span></span> | \- |
| <span data-ttu-id="a1cc3-6163">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6163">TextureCube</span></span> | \- |
| <span data-ttu-id="a1cc3-6164">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6164">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6166">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6166">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6168">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6168">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6169">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6169">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6170">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6170">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6172">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6172">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-6173">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6173">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6175">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6175">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6177">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6177">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6179">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6179">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6181">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6181">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-6182">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6182">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-6183">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6183">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6184">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6184">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6185">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6185">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-6186">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6186">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-6187">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6187">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-6188">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6188">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-6189">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6189">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-6190">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6190">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-6191">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6191">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-6192">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6192">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6193">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6193">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6194">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6194">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6196">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6196">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6197">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6197">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6198">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6198">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-6199">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6199">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-6200">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6200">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-6201">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6201">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-6202">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6202">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a1cc3-6203">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6203">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6205">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6205">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6207">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6207">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6209">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6209">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6211">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6211">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="a1cc3-6212">DXGI_FORMAT_Y410<sup>V</sup> (101)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6212">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="a1cc3-6213">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6213">Target</span></span> | <span data-ttu-id="a1cc3-6214">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6214">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-6215">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6215">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-6216">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6216">32</span></span> |
| <span data-ttu-id="a1cc3-6217">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6217">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6219">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6219">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6220">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6220">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6221">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6221">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6222">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6222">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6223">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6223">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-6224">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6224">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6226">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6226">Texture3D</span></span> | \- |
| <span data-ttu-id="a1cc3-6227">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6227">TextureCube</span></span> | \- |
| <span data-ttu-id="a1cc3-6228">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6228">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6230">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6230">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6232">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6232">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6233">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6233">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6234">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6234">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6236">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6236">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-6237">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6237">Mipmap</span></span> | \- |
| <span data-ttu-id="a1cc3-6238">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6238">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-6239">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6239">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6240">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6240">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6241">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6241">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-6242">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6242">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-6243">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6243">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6244">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6244">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6245">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6245">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-6246">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6246">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-6247">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6247">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-6248">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6248">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-6249">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6249">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-6250">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6250">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-6251">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6251">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-6252">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6252">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6253">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6253">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6254">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6254">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6256">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6256">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6257">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6257">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6258">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6258">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-6259">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6259">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-6260">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6260">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-6261">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6261">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-6262">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6262">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a1cc3-6263">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6263">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6265">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6265">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6267">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6267">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6269">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6269">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6271">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6271">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="a1cc3-6272">DXGI_FORMAT_Y416<sup>V</sup> (102)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6272">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="a1cc3-6273">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6273">Target</span></span> | <span data-ttu-id="a1cc3-6274">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6274">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-6275">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6275">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-6276">64</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6276">64</span></span> |
| <span data-ttu-id="a1cc3-6277">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6277">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6279">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6279">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6280">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6280">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6281">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6281">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6282">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6282">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6283">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6283">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-6284">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6284">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6286">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6286">Texture3D</span></span> | \- |
| <span data-ttu-id="a1cc3-6287">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6287">TextureCube</span></span> | \- |
| <span data-ttu-id="a1cc3-6288">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6288">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6290">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6290">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6292">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6292">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6293">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6293">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6294">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6294">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6296">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6296">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-6297">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6297">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6299">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6299">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-6300">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6300">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6301">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6301">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6302">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6302">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-6303">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6303">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-6304">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6304">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6305">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6305">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6306">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6306">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-6307">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6307">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-6308">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6308">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-6309">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6309">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-6310">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6310">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-6311">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6311">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-6312">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6312">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-6313">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6313">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6314">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6314">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6315">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6315">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6317">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6317">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6318">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6318">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6319">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6319">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-6320">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6320">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-6321">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6321">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-6322">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6322">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-6323">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6323">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a1cc3-6324">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6324">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6326">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6326">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6328">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6328">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6330">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6330">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6332">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6332">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="a1cc3-6333">DXGI_FORMAT_NV12<sup>V</sup> (103)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6333">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="a1cc3-6334">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6334">Target</span></span> | <span data-ttu-id="a1cc3-6335">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6335">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-6336">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6336">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-6337">8</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6337">8</span></span> |
| <span data-ttu-id="a1cc3-6338">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6338">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6340">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6340">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6341">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6341">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6342">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6342">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6343">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6343">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6344">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6344">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-6345">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6345">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6347">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6347">Texture3D</span></span> | \- |
| <span data-ttu-id="a1cc3-6348">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6348">TextureCube</span></span> | \- |
| <span data-ttu-id="a1cc3-6349">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6349">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6351">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6351">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6353">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6353">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6354">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6354">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6355">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6355">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6357">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6357">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-6358">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6358">Mipmap</span></span> | \- |
| <span data-ttu-id="a1cc3-6359">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6359">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-6360">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6360">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6362">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6362">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6364">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6364">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-6365">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6365">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-6366">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6366">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6367">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6367">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6368">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6368">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-6369">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6369">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-6370">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6370">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-6371">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6371">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-6372">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6372">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-6373">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6373">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-6374">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6374">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-6375">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6375">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6376">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6376">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6377">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6377">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6379">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6379">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6380">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6380">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6381">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6381">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-6382">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6382">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-6383">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6383">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-6384">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6384">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-6385">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6385">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a1cc3-6386">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6386">Video Decoder Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6388">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6388">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6390">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6390">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6392">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6392">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6394">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6394">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="a1cc3-6395">DXGI_FORMAT_P010<sup>V</sup> (104)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6395">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="a1cc3-6396">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6396">Target</span></span> | <span data-ttu-id="a1cc3-6397">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6397">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-6398">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6398">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-6399">16</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6399">16</span></span> |
| <span data-ttu-id="a1cc3-6400">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6400">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6402">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6402">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6403">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6403">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6404">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6404">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6405">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6405">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6406">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6406">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-6407">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6407">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6409">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6409">Texture3D</span></span> | \- |
| <span data-ttu-id="a1cc3-6410">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6410">TextureCube</span></span> | \- |
| <span data-ttu-id="a1cc3-6411">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6411">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6413">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6413">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6415">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6415">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6416">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6416">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6417">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6417">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6419">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6419">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-6420">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6420">Mipmap</span></span> | \- |
| <span data-ttu-id="a1cc3-6421">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6421">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-6422">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6422">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6424">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6424">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6426">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6426">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-6427">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6427">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-6428">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6428">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6429">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6429">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6430">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6430">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-6431">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6431">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-6432">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6432">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-6433">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6433">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-6434">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6434">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-6435">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6435">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-6436">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6436">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-6437">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6437">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6438">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6438">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6439">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6439">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6441">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6441">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6442">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6442">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6443">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6443">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-6444">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6444">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-6445">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6445">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-6446">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6446">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-6447">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6447">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a1cc3-6448">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6448">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6450">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6450">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6452">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6452">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6454">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6454">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6456">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6456">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="a1cc3-6457">DXGI_FORMAT_P016<sup>V</sup> (105)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6457">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="a1cc3-6458">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6458">Target</span></span> | <span data-ttu-id="a1cc3-6459">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6459">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-6460">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6460">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-6461">16</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6461">16</span></span> |
| <span data-ttu-id="a1cc3-6462">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6462">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6464">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6464">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6465">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6465">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6466">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6466">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6467">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6467">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6468">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6468">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-6469">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6469">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6471">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6471">Texture3D</span></span> | \- |
| <span data-ttu-id="a1cc3-6472">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6472">TextureCube</span></span> | \- |
| <span data-ttu-id="a1cc3-6473">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6473">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6475">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6475">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6477">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6477">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6478">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6478">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6479">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6479">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6481">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6481">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-6482">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6482">Mipmap</span></span> | \- |
| <span data-ttu-id="a1cc3-6483">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6483">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-6484">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6484">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6486">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6486">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6488">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6488">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-6489">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6489">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-6490">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6490">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6491">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6491">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6492">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6492">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-6493">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6493">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-6494">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6494">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-6495">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6495">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-6496">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6496">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-6497">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6497">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-6498">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6498">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-6499">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6499">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6500">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6500">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6501">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6501">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6503">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6503">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6504">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6504">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6505">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6505">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-6506">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6506">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-6507">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6507">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-6508">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6508">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-6509">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6509">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a1cc3-6510">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6510">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6512">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6512">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6514">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6514">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6516">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6516">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6518">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6518">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="a1cc3-6519">DXGI_FORMAT_420 \_ opaco<sup>V</sup> (106)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6519">DXGI_FORMAT_420\_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="a1cc3-6520">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6520">Target</span></span> | <span data-ttu-id="a1cc3-6521">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6521">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-6522">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6522">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-6523">8</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6523">8</span></span> |
| <span data-ttu-id="a1cc3-6524">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6524">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6526">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6526">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6527">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6527">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6528">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6528">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6529">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6529">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6530">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6530">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-6531">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6531">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6533">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6533">Texture3D</span></span> | \- |
| <span data-ttu-id="a1cc3-6534">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6534">TextureCube</span></span> | \- |
| <span data-ttu-id="a1cc3-6535">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6535">Shader ld</span></span> | \- |
| <span data-ttu-id="a1cc3-6536">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6536">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6537">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6537">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6538">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6538">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6539">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6539">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-6540">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6540">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-6541">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6541">Mipmap</span></span> | \- |
| <span data-ttu-id="a1cc3-6542">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6542">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-6543">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6543">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6544">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6544">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6545">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6545">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-6546">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6546">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-6547">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6547">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6548">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6548">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6549">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6549">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-6550">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6550">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-6551">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6551">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-6552">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6552">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-6553">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6553">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-6554">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6554">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-6555">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6555">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-6556">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6556">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6557">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6557">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6558">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6558">CPU Lockable</span></span> | \- |
| <span data-ttu-id="a1cc3-6559">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6559">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6560">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6560">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6561">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6561">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-6562">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6562">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-6563">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6563">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-6564">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6564">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-6565">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6565">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a1cc3-6566">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6566">Video Decoder Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6568">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6568">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6570">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6570">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6572">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6572">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6574">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6574">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="a1cc3-6575">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6575">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="a1cc3-6576">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6576">Target</span></span> | <span data-ttu-id="a1cc3-6577">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6577">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-6578">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6578">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-6579">16</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6579">16</span></span> |
| <span data-ttu-id="a1cc3-6580">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6580">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6582">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6582">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6583">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6583">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6584">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6584">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6585">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6585">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6586">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6586">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-6587">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6587">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6589">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6589">Texture3D</span></span> | \- |
| <span data-ttu-id="a1cc3-6590">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6590">TextureCube</span></span> | \- |
| <span data-ttu-id="a1cc3-6591">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6591">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6593">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6593">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6595">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6595">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6596">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6596">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6597">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6597">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6599">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6599">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-6600">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6600">Mipmap</span></span> | \- |
| <span data-ttu-id="a1cc3-6601">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6601">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-6602">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6602">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6603">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6603">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6604">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6604">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-6605">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6605">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-6606">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6606">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6607">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6607">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6608">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6608">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-6609">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6609">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-6610">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6610">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-6611">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6611">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-6612">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6612">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-6613">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6613">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-6614">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6614">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-6615">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6615">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6616">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6616">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6617">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6617">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6619">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6619">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6620">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6620">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6621">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6621">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-6622">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6622">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-6623">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6623">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-6624">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6624">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-6625">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6625">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a1cc3-6626">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6626">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6628">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6628">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6630">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6630">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6632">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6632">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6634">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6634">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="a1cc3-6635">DXGI_FORMAT_Y210<sup>V</sup> (108)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6635">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="a1cc3-6636">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6636">Target</span></span> | <span data-ttu-id="a1cc3-6637">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6637">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-6638">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6638">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-6639">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6639">32</span></span> |
| <span data-ttu-id="a1cc3-6640">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6640">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6642">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6642">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6643">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6643">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6644">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6644">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6645">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6645">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6646">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6646">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-6647">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6647">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6649">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6649">Texture3D</span></span> | \- |
| <span data-ttu-id="a1cc3-6650">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6650">TextureCube</span></span> | \- |
| <span data-ttu-id="a1cc3-6651">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6651">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6653">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6653">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6655">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6655">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6656">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6656">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6657">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6657">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6659">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6659">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-6660">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6660">Mipmap</span></span> | \- |
| <span data-ttu-id="a1cc3-6661">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6661">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-6662">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6662">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6663">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6663">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6664">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6664">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-6665">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6665">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-6666">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6666">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6667">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6667">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6668">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6668">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-6669">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6669">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-6670">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6670">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-6671">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6671">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-6672">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6672">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-6673">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6673">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-6674">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6674">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-6675">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6675">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6676">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6676">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6677">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6677">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6679">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6679">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6680">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6680">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6681">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6681">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-6682">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6682">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-6683">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6683">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-6684">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6684">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-6685">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6685">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a1cc3-6686">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6686">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6688">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6688">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6690">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6690">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6692">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6692">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6694">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6694">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="a1cc3-6695">DXGI_FORMAT_Y216<sup>V</sup> (109)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6695">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="a1cc3-6696">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6696">Target</span></span> | <span data-ttu-id="a1cc3-6697">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6697">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-6698">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6698">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-6699">32</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6699">32</span></span> |
| <span data-ttu-id="a1cc3-6700">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6700">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6702">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6702">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6703">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6703">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6704">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6704">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6705">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6705">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6706">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6706">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-6707">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6707">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6709">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6709">Texture3D</span></span> | \- |
| <span data-ttu-id="a1cc3-6710">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6710">TextureCube</span></span> | \- |
| <span data-ttu-id="a1cc3-6711">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6711">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6713">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6713">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6715">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6715">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6716">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6716">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6717">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6717">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6719">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6719">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-6720">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6720">Mipmap</span></span> | \- |
| <span data-ttu-id="a1cc3-6721">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6721">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-6722">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6722">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6723">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6723">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6724">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6724">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-6725">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6725">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-6726">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6726">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6727">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6727">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6728">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6728">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-6729">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6729">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-6730">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6730">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-6731">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6731">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-6732">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6732">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-6733">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6733">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-6734">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6734">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-6735">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6735">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6736">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6736">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6737">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6737">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6739">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6739">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6740">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6740">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6741">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6741">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-6742">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6742">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-6743">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6743">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-6744">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6744">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-6745">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6745">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a1cc3-6746">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6746">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6748">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6748">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6750">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6750">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6752">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6752">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6754">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6754">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="a1cc3-6755">DXGI_FORMAT_NV11<sup>V</sup> (110)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6755">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="a1cc3-6756">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6756">Target</span></span> | <span data-ttu-id="a1cc3-6757">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6757">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-6758">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6758">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-6759">8</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6759">8</span></span> |
| <span data-ttu-id="a1cc3-6760">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6760">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6762">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6762">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6763">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6763">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6764">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6764">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6765">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6765">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6766">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6766">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-6767">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6767">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6769">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6769">Texture3D</span></span> | \- |
| <span data-ttu-id="a1cc3-6770">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6770">TextureCube</span></span> | \- |
| <span data-ttu-id="a1cc3-6771">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6771">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6773">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6773">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6775">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6775">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6776">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6776">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6777">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6777">Shader gather4</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6779">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6779">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-6780">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6780">Mipmap</span></span> | \- |
| <span data-ttu-id="a1cc3-6781">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6781">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-6782">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6782">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6784">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6784">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6786">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6786">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-6787">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6787">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-6788">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6788">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6789">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6789">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6790">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6790">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-6791">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6791">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-6792">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6792">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-6793">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6793">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-6794">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6794">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-6795">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6795">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-6796">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6796">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-6797">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6797">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6798">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6798">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6799">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6799">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6801">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6801">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6802">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6802">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6803">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6803">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-6804">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6804">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-6805">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6805">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-6806">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6806">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-6807">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6807">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a1cc3-6808">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6808">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6810">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6810">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6812">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6812">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6814">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6814">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6816">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6816">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="a1cc3-6817">DXGI_FORMAT_AI44<sup>V</sup> (111)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6817">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="a1cc3-6818">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6818">Target</span></span> | <span data-ttu-id="a1cc3-6819">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6819">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-6820">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6820">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-6821">8</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6821">8</span></span> |
| <span data-ttu-id="a1cc3-6822">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6822">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6824">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6824">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6825">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6825">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6826">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6826">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6827">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6827">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6828">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6828">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-6829">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6829">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6831">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6831">Texture3D</span></span> | \- |
| <span data-ttu-id="a1cc3-6832">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6832">TextureCube</span></span> | \- |
| <span data-ttu-id="a1cc3-6833">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6833">Shader ld</span></span> | \- |
| <span data-ttu-id="a1cc3-6834">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6834">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6835">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6835">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6836">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6836">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6837">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6837">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-6838">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6838">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-6839">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6839">Mipmap</span></span> | \- |
| <span data-ttu-id="a1cc3-6840">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6840">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-6841">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6841">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6842">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6842">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6843">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6843">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-6844">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6844">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-6845">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6845">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6846">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6846">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6847">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6847">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-6848">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6848">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-6849">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6849">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-6850">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6850">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-6851">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6851">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-6852">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6852">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-6853">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6853">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-6854">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6854">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6855">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6855">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6856">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6856">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6858">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6858">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6859">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6859">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6860">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6860">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-6861">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6861">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-6862">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6862">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-6863">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6863">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-6864">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6864">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a1cc3-6865">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6865">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-6866">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6866">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6868">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6868">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-6869">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6869">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-6870">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6870">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="a1cc3-6871">DXGI_FORMAT_IA44<sup>V</sup> (112)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6871">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="a1cc3-6872">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6872">Target</span></span> | <span data-ttu-id="a1cc3-6873">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6873">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-6874">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6874">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-6875">8</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6875">8</span></span> |
| <span data-ttu-id="a1cc3-6876">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6876">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6878">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6878">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6879">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6879">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6880">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6880">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6881">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6881">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6882">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6882">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-6883">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6883">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6885">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6885">Texture3D</span></span> | \- |
| <span data-ttu-id="a1cc3-6886">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6886">TextureCube</span></span> | \- |
| <span data-ttu-id="a1cc3-6887">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6887">Shader ld</span></span> | \- |
| <span data-ttu-id="a1cc3-6888">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6888">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6889">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6889">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6890">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6890">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6891">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6891">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-6892">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6892">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-6893">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6893">Mipmap</span></span> | \- |
| <span data-ttu-id="a1cc3-6894">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6894">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-6895">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6895">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6896">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6896">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6897">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6897">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-6898">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6898">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-6899">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6899">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6900">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6900">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6901">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6901">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-6902">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6902">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-6903">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6903">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-6904">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6904">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-6905">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6905">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-6906">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6906">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-6907">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6907">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-6908">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6908">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6909">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6909">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6910">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6910">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6912">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6912">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6913">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6913">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6914">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6914">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-6915">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6915">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-6916">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6916">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-6917">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6917">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-6918">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6918">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a1cc3-6919">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6919">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-6920">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6920">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6922">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6922">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-6923">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6923">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-6924">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6924">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="a1cc3-6925">DXGI_FORMAT_P8<sup>V</sup> (113)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6925">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="a1cc3-6926">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6926">Target</span></span> | <span data-ttu-id="a1cc3-6927">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6927">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-6928">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6928">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-6929">8</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6929">8</span></span> |
| <span data-ttu-id="a1cc3-6930">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6930">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6932">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6932">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6933">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6933">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6934">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6934">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6935">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6935">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6936">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6936">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-6937">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6937">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6939">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6939">Texture3D</span></span> | \- |
| <span data-ttu-id="a1cc3-6940">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6940">TextureCube</span></span> | \- |
| <span data-ttu-id="a1cc3-6941">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6941">Shader ld</span></span> | \- |
| <span data-ttu-id="a1cc3-6942">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6942">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6943">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6943">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6944">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6944">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6945">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6945">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-6946">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6946">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-6947">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6947">Mipmap</span></span> | \- |
| <span data-ttu-id="a1cc3-6948">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6948">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-6949">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6949">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6950">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6950">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6951">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6951">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-6952">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6952">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-6953">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6953">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6954">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6954">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-6955">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6955">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-6956">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6956">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-6957">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6957">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-6958">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6958">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-6959">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6959">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-6960">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6960">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-6961">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6961">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-6962">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6962">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6963">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6963">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-6964">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6964">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6966">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6966">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6967">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6967">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-6968">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6968">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-6969">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6969">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-6970">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6970">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-6971">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6971">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-6972">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6972">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a1cc3-6973">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6973">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-6974">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6974">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6976">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6976">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-6977">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6977">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-6978">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6978">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="a1cc3-6979">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6979">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="a1cc3-6980">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6980">Target</span></span> | <span data-ttu-id="a1cc3-6981">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6981">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-6982">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6982">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-6983">16</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6983">16</span></span> |
| <span data-ttu-id="a1cc3-6984">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6984">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-6986">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6986">Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6987">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6987">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6988">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6988">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6989">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6989">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-6990">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6990">Texture1D</span></span> | \- |
| <span data-ttu-id="a1cc3-6991">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6991">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-6993">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6993">Texture3D</span></span> | \- |
| <span data-ttu-id="a1cc3-6994">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6994">TextureCube</span></span> | \- |
| <span data-ttu-id="a1cc3-6995">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6995">Shader ld</span></span> | \- |
| <span data-ttu-id="a1cc3-6996">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6996">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6997">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6997">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6998">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6998">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-6999">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-6999">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-7000">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7000">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-7001">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7001">Mipmap</span></span> | \- |
| <span data-ttu-id="a1cc3-7002">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7002">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="a1cc3-7003">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7003">RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-7004">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7004">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-7005">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7005">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-7006">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7006">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-7007">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7007">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-7008">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7008">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-7009">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7009">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-7010">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7010">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-7011">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7011">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-7012">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7012">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-7013">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7013">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-7014">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7014">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-7015">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7015">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-7016">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7016">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-7017">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7017">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-7018">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7018">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-7020">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7020">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-7021">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7021">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="a1cc3-7022">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7022">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="a1cc3-7023">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7023">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="a1cc3-7024">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7024">Multisample Load</span></span> | \- |
| <span data-ttu-id="a1cc3-7025">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7025">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-7026">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7026">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a1cc3-7027">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7027">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-7028">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7028">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-7030">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7030">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-7031">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7031">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-7032">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7032">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a><span data-ttu-id="a1cc3-7033">DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>FNS</sup> (115)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7033">DXGI_FORMAT_B4G4R4A4\_UNORM<sup>FNS</sup> (115)</span></span>
| <span data-ttu-id="a1cc3-7034">Destino</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7034">Target</span></span> | <span data-ttu-id="a1cc3-7035">Suporte</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7035">Support</span></span> |
| - | - |
| <span data-ttu-id="a1cc3-7036">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7036">Bits Per Element (BPE)</span></span> | <span data-ttu-id="a1cc3-7037">16</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7037">16</span></span> |
| <span data-ttu-id="a1cc3-7038">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7038">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-7040">Buffer</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7040">Buffer</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-7042">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7042">Input Assembler Vertex Buffer</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-7044">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7044">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-7045">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7045">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="a1cc3-7046">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7046">Texture1D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-7048">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7048">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-7050">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7050">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-7052">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7052">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-7054">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7054">Shader ld</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-7056">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7056">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-7058">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7058">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-7059">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7059">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="a1cc3-7060">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7060">Shader gather4</span></span> | \- |
| <span data-ttu-id="a1cc3-7061">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7061">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="a1cc3-7062">Mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7062">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-7064">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7064">Mipmap Auto-Generation</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-7066">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7066">RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-7068">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7068">Blendable RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-7070">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7070">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="a1cc3-7071">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7071">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="a1cc3-7072">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7072">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-7073">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7073">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="a1cc3-7074">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7074">Typed UAV</span></span> | \- |
| <span data-ttu-id="a1cc3-7075">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7075">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="a1cc3-7076">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7076">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="a1cc3-7077">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7077">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="a1cc3-7078">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7078">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="a1cc3-7079">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7079">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="a1cc3-7080">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7080">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="a1cc3-7081">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7081">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-7082">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7082">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="a1cc3-7083">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7083">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-7085">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7085">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-7087">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7087">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-7089">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7089">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-7091">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7091">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="a1cc3-7093">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7093">Multisample Load</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="a1cc3-7095">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7095">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="a1cc3-7096">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7096">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="a1cc3-7097">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7097">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="a1cc3-7098">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7098">Video Processor Input</span></span> | \- |
| <span data-ttu-id="a1cc3-7099">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7099">Video Processor Output</span></span> | \- |
| <span data-ttu-id="a1cc3-7100">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7100">Shared Resource</span></span> | \- |
| <span data-ttu-id="a1cc3-7101">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7101">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="a1cc3-7102">Observações de formato</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7102">Format notes</span></span>

<span data-ttu-id="a1cc3-7103">A finalidade do formato pode mudar de um nível de recurso de hardware para o próximo.</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7103">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="a1cc3-7104"><sup>L</sup> : formato de tipo informativo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7104"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="a1cc3-7105"><sup>PCs</sup> : layout de tipo parcial, convertido e simples</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7105"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="a1cc3-7106"><sup>FCS</sup> : layout totalmente tipado, convertido e simples</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7106"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="a1cc3-7107"><sup>FNS</sup> : layout totalmente tipado, não-convertido e simples</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7107"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="a1cc3-7108"><sup>PCC</sup> : layout complexo, convertido e de tipo parcial</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7108"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="a1cc3-7109"><sup>FCC</sup> : layout totalmente tipado, convertido e complexo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7109"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="a1cc3-7110"><sup>FNC</sup> : layout totalmente tipado, não-convertido e complexo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7110"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="a1cc3-7111"><sup>V</sup> : formato de vídeo</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7111"><sup>V</sup> : video format</span></span>
</dt> </dl>

<span data-ttu-id="a1cc3-7112">Os buffers traseiros e os exames com o formato [**\_ \_ R16G16B16A16 \_ float de formato dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) contêm dados de gama com valor linear.</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7112">Back buffers and scan outs with the [**DXGI\_FORMAT\_R16G16B16A16\_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) format contain linear-valued gamma data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1cc3-7113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7113">Related topics</span></span>

[<span data-ttu-id="a1cc3-7114">Níveis de recursos de hardware do D3D12</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7114">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

[<span data-ttu-id="a1cc3-7115">**ID3D10Device::CheckFormatSupport**</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7115">**ID3D10Device::CheckFormatSupport**</span></span>](/windows/win32/api/d3d10/nf-d3d10-id3d10device-checkformatsupport)

[<span data-ttu-id="a1cc3-7116">Guia de programação para DXGI</span><span class="sxs-lookup"><span data-stu-id="a1cc3-7116">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
