---
description: Esta seção especifica os formatos ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valores) que têm suporte no hardware do recurso Direct3D 10Level9 9,1.
ms.assetid: 770A5396-C5D9-442B-99FE-3D220C54E8EB
title: Suporte de formato para hardware 9.1 do Nível de 10Recursos9 do Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56653fd2fb504e3f23cfac13b432530ebaa7219b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825643"
---
# <a name="format-support-for-direct3d-feature-10level9-91-hardware"></a><span data-ttu-id="92888-103">Suporte de formato para hardware 9.1 do Nível de 10Recursos9 do Direct3D</span><span class="sxs-lookup"><span data-stu-id="92888-103">Format support for Direct3D Feature 10Level9 9.1 hardware</span></span>

<span data-ttu-id="92888-104">Esta seção especifica os formatos ([_\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valores) que têm suporte no hardware do recurso Direct3D 10Level9 9,1.</span><span class="sxs-lookup"><span data-stu-id="92888-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature 10Level9 9.1 hardware.</span></span>

<span data-ttu-id="92888-105">A tabela resume o suporte a recursos, usando a chave a seguir.</span><span class="sxs-lookup"><span data-stu-id="92888-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="92888-106">Símbolo</span><span class="sxs-lookup"><span data-stu-id="92888-106">Symbol</span></span>                            | <span data-ttu-id="92888-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="92888-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="92888-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="92888-108">_ *-*\*</span></span>                             | <span data-ttu-id="92888-109">Não permitido ou não disponível.</span><span class="sxs-lookup"><span data-stu-id="92888-109">Disallowed or not available.</span></span>                                                  |
| ![exigido](images/letter-r.jpg)  | <span data-ttu-id="92888-111">O suporte a hardware é necessário.</span><span class="sxs-lookup"><span data-stu-id="92888-111">Hardware support is required.</span></span>                                                 |
| ![opcionais](images/letter-o.jpg)  | <span data-ttu-id="92888-113">Suporte a hardware opcional, o formato pode ou não ser acelerado por hardware.</span><span class="sxs-lookup"><span data-stu-id="92888-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![dependentes](images/letter-d.jpg) | <span data-ttu-id="92888-115">Necessário se houver suporte para o recurso opcional relacionado.</span><span class="sxs-lookup"><span data-stu-id="92888-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="92888-116">Este tópico contém uma seção por formato.</span><span class="sxs-lookup"><span data-stu-id="92888-116">This topic contains a section per format.</span></span> <span data-ttu-id="92888-117">Um *destino* de formato (as tabelas contêm uma linha por destino) pode ser um tipo de recurso, uma função intrínseca HLSL ou uma funcionalidade específica que depende de um formato específico.</span><span class="sxs-lookup"><span data-stu-id="92888-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="92888-118">Para verificar programaticamente o suporte a Format em D3D11 e D3D12, consulte [verificando o suporte a recursos de hardware](checking-hardware-feature-support.md).</span><span class="sxs-lookup"><span data-stu-id="92888-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="92888-119">Os números dos formatos são principalmente, mas nem todos, em ordem numérica crescente &mdash; alguns estão fora de ordem numérica e listados junto com outros formatos relevantes.</span><span class="sxs-lookup"><span data-stu-id="92888-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="92888-120">Observe também que sem *tipo* em um nome de formato pode significar digitação *parcial* e não estritamente tipado (consulte a seção [observações de formato](#format-notes) no final do tópico).</span><span class="sxs-lookup"><span data-stu-id="92888-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>

// 

## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="92888-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span><span class="sxs-lookup"><span data-stu-id="92888-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="92888-122">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-122">Target</span></span> | <span data-ttu-id="92888-123">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-123">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-124">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-125">0</span><span class="sxs-lookup"><span data-stu-id="92888-125">0</span></span> |
| <span data-ttu-id="92888-126">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-126">Format Support</span></span> | \- |
| <span data-ttu-id="92888-127">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-127">Buffer</span></span> | \- |
| <span data-ttu-id="92888-128">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-128">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-129">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-129">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-130">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-130">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-131">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-131">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-132">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-132">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-133">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-133">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-134">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-134">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-135">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-135">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-136">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-136">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-137">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-137">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-138">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-138">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-139">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-139">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-140">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-140">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-141">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-141">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-142">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-142">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-143">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-143">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-144">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-144">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-145">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-145">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-146">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-146">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-147">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-147">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-148">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-148">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-149">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-149">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-150">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-150">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-151">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-151">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-152">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-152">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-153">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-153">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-154">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-154">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-155">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-155">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-156">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-156">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-157">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-157">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-158">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-158">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-159">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-159">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-160">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-160">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-161">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-161">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-162">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-162">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-163">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-163">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-164">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-164">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-165">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-165">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-166">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-166">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-167">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-167">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-168">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-168">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-169">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-169">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-170">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-170">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="92888-171">DXGI_FORMAT_R32G32B32A32 \_ <sup>PCs</sup> não tipados (1)</span><span class="sxs-lookup"><span data-stu-id="92888-171">DXGI_FORMAT_R32G32B32A32\_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="92888-172">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-172">Target</span></span> | <span data-ttu-id="92888-173">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-173">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-174">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-174">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-175">128</span><span class="sxs-lookup"><span data-stu-id="92888-175">128</span></span> |
| <span data-ttu-id="92888-176">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-176">Format Support</span></span> | \- |
| <span data-ttu-id="92888-177">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-177">Buffer</span></span> | \- |
| <span data-ttu-id="92888-178">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-178">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-179">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-179">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-180">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-180">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-181">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-181">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-182">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-182">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-183">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-183">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-184">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-184">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-185">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-185">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-186">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-186">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-187">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-187">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-188">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-188">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-189">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-189">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-190">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-190">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-191">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-191">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-192">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-192">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-193">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-193">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-194">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-194">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-195">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-195">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-196">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-196">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-197">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-197">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-198">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-198">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-199">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-199">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-200">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-200">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-201">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-201">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-202">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-202">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-203">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-203">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-204">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-204">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-205">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-205">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-206">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-206">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-207">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-207">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-208">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-208">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-209">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-209">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-210">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-210">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-211">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-211">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-212">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-212">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-213">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-213">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-214">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-214">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-215">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-215">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-216">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-216">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-217">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-217">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-218">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-218">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-219">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-219">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-220">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-220">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfnssup-2"></a><span data-ttu-id="92888-221">DXGI_FORMAT_R32G32B32A32 \_ float<sup>FNS</sup> (2)</span><span class="sxs-lookup"><span data-stu-id="92888-221">DXGI_FORMAT_R32G32B32A32\_FLOAT<sup>FNS</sup> (2)</span></span>
| <span data-ttu-id="92888-222">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-222">Target</span></span> | <span data-ttu-id="92888-223">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-223">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-224">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-224">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-225">128</span><span class="sxs-lookup"><span data-stu-id="92888-225">128</span></span> |
| <span data-ttu-id="92888-226">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-226">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-228">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-228">Buffer</span></span> | \- |
| <span data-ttu-id="92888-229">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-229">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-231">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-231">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-232">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-232">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-233">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-233">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-234">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-234">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-235">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-235">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-236">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-236">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-237">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-237">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-238">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-238">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-239">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-239">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-240">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-240">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-241">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-241">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-242">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-242">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-243">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-243">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-244">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-244">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-245">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-245">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-246">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-246">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-247">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-247">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-248">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-248">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-249">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-249">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-250">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-250">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-251">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-251">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-252">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-252">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-253">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-253">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-254">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-254">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-255">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-255">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-256">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-256">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-257">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-257">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-258">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-258">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-259">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-259">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-260">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-260">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-261">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-261">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-262">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-262">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-263">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-263">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-264">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-264">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-265">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-265">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-266">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-266">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-267">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-267">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-268">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-268">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-269">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-269">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-270">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-270">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-271">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-271">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-272">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-272">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfnssup-3"></a><span data-ttu-id="92888-273">DXGI_FORMAT_R32G32B32A32 \_ uint<sup>FNS</sup> (3)</span><span class="sxs-lookup"><span data-stu-id="92888-273">DXGI_FORMAT_R32G32B32A32\_UINT<sup>FNS</sup> (3)</span></span>
| <span data-ttu-id="92888-274">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-274">Target</span></span> | <span data-ttu-id="92888-275">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-275">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-276">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-276">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-277">128</span><span class="sxs-lookup"><span data-stu-id="92888-277">128</span></span> |
| <span data-ttu-id="92888-278">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-278">Format Support</span></span> | \- |
| <span data-ttu-id="92888-279">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-279">Buffer</span></span> | \- |
| <span data-ttu-id="92888-280">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-280">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-281">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-281">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-282">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-282">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-283">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-283">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-284">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-284">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-285">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-285">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-286">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-286">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-287">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-287">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-288">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-288">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-289">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-289">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-290">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-290">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-291">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-291">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-292">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-292">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-293">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-293">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-294">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-294">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-295">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-295">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-296">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-296">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-297">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-297">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-298">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-298">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-299">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-299">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-300">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-300">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-301">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-301">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-302">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-302">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-303">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-303">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-304">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-304">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-305">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-305">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-306">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-306">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-307">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-307">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-308">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-308">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-309">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-309">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-310">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-310">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-311">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-311">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-312">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-312">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-313">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-313">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-314">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-314">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-315">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-315">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-316">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-316">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-317">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-317">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-318">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-318">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-319">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-319">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-320">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-320">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-321">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-321">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-322">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-322">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfnssup-4"></a><span data-ttu-id="92888-323">DXGI_FORMAT_R32G32B32A32 \_ Santo<sup>FNS</sup> (4)</span><span class="sxs-lookup"><span data-stu-id="92888-323">DXGI_FORMAT_R32G32B32A32\_SINT<sup>FNS</sup> (4)</span></span>
| <span data-ttu-id="92888-324">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-324">Target</span></span> | <span data-ttu-id="92888-325">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-325">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-326">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-326">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-327">128</span><span class="sxs-lookup"><span data-stu-id="92888-327">128</span></span> |
| <span data-ttu-id="92888-328">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-328">Format Support</span></span> | \- |
| <span data-ttu-id="92888-329">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-329">Buffer</span></span> | \- |
| <span data-ttu-id="92888-330">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-330">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-331">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-331">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-332">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-332">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-333">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-333">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-334">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-334">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-335">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-335">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-336">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-336">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-337">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-337">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-338">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-338">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-339">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-339">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-340">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-340">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-341">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-341">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-342">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-342">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-343">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-343">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-344">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-344">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-345">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-345">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-346">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-346">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-347">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-347">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-348">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-348">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-349">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-349">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-350">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-350">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-351">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-351">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-352">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-352">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-353">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-353">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-354">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-354">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-355">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-355">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-356">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-356">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-357">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-357">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-358">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-358">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-359">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-359">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-360">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-360">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-361">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-361">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-362">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-362">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-363">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-363">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-364">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-364">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-365">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-365">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-366">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-366">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-367">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-367">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-368">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-368">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-369">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-369">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-370">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-370">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-371">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-371">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-372">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-372">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="92888-373">DXGI_FORMAT_R32G32B32 \_ <sup>PCs</sup> não tipados (5)</span><span class="sxs-lookup"><span data-stu-id="92888-373">DXGI_FORMAT_R32G32B32\_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="92888-374">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-374">Target</span></span> | <span data-ttu-id="92888-375">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-375">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-376">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-376">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-377">96</span><span class="sxs-lookup"><span data-stu-id="92888-377">96</span></span> |
| <span data-ttu-id="92888-378">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-378">Format Support</span></span> | \- |
| <span data-ttu-id="92888-379">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-379">Buffer</span></span> | \- |
| <span data-ttu-id="92888-380">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-380">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-381">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-381">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-382">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-382">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-383">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-383">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-384">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-384">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-385">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-385">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-386">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-386">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-387">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-387">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-388">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-388">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-389">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-389">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-390">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-390">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-391">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-391">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-392">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-392">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-393">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-393">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-394">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-394">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-395">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-395">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-396">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-396">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-397">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-397">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-398">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-398">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-399">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-399">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-400">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-400">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-401">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-401">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-402">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-402">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-403">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-403">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-404">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-404">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-405">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-405">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-406">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-406">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-407">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-407">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-408">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-408">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-409">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-409">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-410">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-410">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-411">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-411">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-412">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-412">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-413">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-413">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-414">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-414">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-415">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-415">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-416">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-416">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-417">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-417">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-418">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-418">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-419">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-419">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-420">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-420">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-421">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-421">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-422">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-422">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfnssup-6"></a><span data-ttu-id="92888-423">DXGI_FORMAT_R32G32B32 \_ float<sup>FNS</sup> (6)</span><span class="sxs-lookup"><span data-stu-id="92888-423">DXGI_FORMAT_R32G32B32\_FLOAT<sup>FNS</sup> (6)</span></span>
| <span data-ttu-id="92888-424">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-424">Target</span></span> | <span data-ttu-id="92888-425">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-425">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-426">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-426">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-427">96</span><span class="sxs-lookup"><span data-stu-id="92888-427">96</span></span> |
| <span data-ttu-id="92888-428">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-428">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-430">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-430">Buffer</span></span> | \- |
| <span data-ttu-id="92888-431">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-431">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-433">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-433">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-434">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-434">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-435">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-435">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-436">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-436">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-437">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-437">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-438">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-438">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-439">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-439">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-440">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-440">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-441">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-441">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-442">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-442">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-443">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-443">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-444">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-444">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-445">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-445">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-446">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-446">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-447">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-447">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-448">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-448">Blendable RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="92888-450">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-450">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-451">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-451">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-452">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-452">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-453">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-453">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-454">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-454">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-455">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-455">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-456">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-456">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-457">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-457">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-458">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-458">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-459">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-459">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-460">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-460">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-461">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-461">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-462">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-462">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-463">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-463">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-464">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-464">4x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="92888-466">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-466">8x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="92888-468">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-468">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-469">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-469">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-470">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-470">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-471">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-471">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-472">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-472">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-473">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-473">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-474">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-474">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-475">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-475">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-476">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-476">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-477">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-477">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfnssup-7"></a><span data-ttu-id="92888-478">DXGI_FORMAT_R32G32B32 \_ uint<sup>FNS</sup> (7)</span><span class="sxs-lookup"><span data-stu-id="92888-478">DXGI_FORMAT_R32G32B32\_UINT<sup>FNS</sup> (7)</span></span>
| <span data-ttu-id="92888-479">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-479">Target</span></span> | <span data-ttu-id="92888-480">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-480">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-481">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-481">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-482">96</span><span class="sxs-lookup"><span data-stu-id="92888-482">96</span></span> |
| <span data-ttu-id="92888-483">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-483">Format Support</span></span> | \- |
| <span data-ttu-id="92888-484">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-484">Buffer</span></span> | \- |
| <span data-ttu-id="92888-485">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-485">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-486">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-486">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-487">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-487">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-488">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-488">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-489">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-489">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-490">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-490">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-491">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-491">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-492">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-492">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-493">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-493">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-494">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-494">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-495">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-495">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-496">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-496">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-497">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-497">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-498">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-498">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-499">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-499">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-500">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-500">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-501">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-501">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-502">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-502">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-503">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-503">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-504">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-504">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-505">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-505">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-506">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-506">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-507">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-507">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-508">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-508">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-509">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-509">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-510">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-510">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-511">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-511">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-512">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-512">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-513">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-513">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-514">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-514">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-515">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-515">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-516">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-516">4x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="92888-518">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-518">8x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="92888-520">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-520">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-521">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-521">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-522">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-522">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-523">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-523">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-524">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-524">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-525">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-525">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-526">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-526">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-527">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-527">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-528">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-528">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-529">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-529">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfnssup-8"></a><span data-ttu-id="92888-530">DXGI_FORMAT_R32G32B32 \_ Santo<sup>FNS</sup> (8)</span><span class="sxs-lookup"><span data-stu-id="92888-530">DXGI_FORMAT_R32G32B32\_SINT<sup>FNS</sup> (8)</span></span>
| <span data-ttu-id="92888-531">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-531">Target</span></span> | <span data-ttu-id="92888-532">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-532">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-533">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-533">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-534">96</span><span class="sxs-lookup"><span data-stu-id="92888-534">96</span></span> |
| <span data-ttu-id="92888-535">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-535">Format Support</span></span> | \- |
| <span data-ttu-id="92888-536">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-536">Buffer</span></span> | \- |
| <span data-ttu-id="92888-537">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-537">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-538">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-538">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-539">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-539">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-540">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-540">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-541">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-541">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-542">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-542">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-543">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-543">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-544">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-544">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-545">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-545">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-546">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-546">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-547">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-547">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-548">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-548">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-549">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-549">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-550">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-550">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-551">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-551">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-552">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-552">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-553">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-553">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-554">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-554">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-555">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-555">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-556">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-556">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-557">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-557">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-558">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-558">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-559">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-559">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-560">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-560">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-561">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-561">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-562">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-562">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-563">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-563">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-564">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-564">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-565">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-565">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-566">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-566">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-567">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-567">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-568">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-568">4x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="92888-570">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-570">8x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="92888-572">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-572">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-573">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-573">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-574">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-574">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-575">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-575">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-576">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-576">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-577">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-577">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-578">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-578">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-579">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-579">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-580">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-580">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-581">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-581">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="92888-582">DXGI_FORMAT_R16G16B16A16 \_ <sup>PCs</sup> não tipados (9)</span><span class="sxs-lookup"><span data-stu-id="92888-582">DXGI_FORMAT_R16G16B16A16\_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="92888-583">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-583">Target</span></span> | <span data-ttu-id="92888-584">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-584">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-585">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-585">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-586">64</span><span class="sxs-lookup"><span data-stu-id="92888-586">64</span></span> |
| <span data-ttu-id="92888-587">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-587">Format Support</span></span> | \- |
| <span data-ttu-id="92888-588">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-588">Buffer</span></span> | \- |
| <span data-ttu-id="92888-589">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-589">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-590">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-590">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-591">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-591">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-592">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-592">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-593">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-593">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-594">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-594">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-595">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-595">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-596">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-596">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-597">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-597">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-598">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-598">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-599">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-599">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-600">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-600">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-601">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-601">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-602">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-602">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-603">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-603">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-604">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-604">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-605">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-605">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-606">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-606">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-607">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-607">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-608">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-608">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-609">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-609">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-610">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-610">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-611">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-611">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-612">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-612">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-613">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-613">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-614">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-614">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-615">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-615">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-616">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-616">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-617">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-617">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-618">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-618">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-619">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-619">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-620">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-620">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-621">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-621">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-622">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-622">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-623">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-623">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-624">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-624">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-625">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-625">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-626">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-626">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-627">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-627">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-628">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-628">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-629">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-629">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-630">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-630">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-631">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-631">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfnssup-10"></a><span data-ttu-id="92888-632">DXGI_FORMAT_R16G16B16A16 \_ float<sup>FNS</sup> (10)</span><span class="sxs-lookup"><span data-stu-id="92888-632">DXGI_FORMAT_R16G16B16A16\_FLOAT<sup>FNS</sup> (10)</span></span>
| <span data-ttu-id="92888-633">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-633">Target</span></span> | <span data-ttu-id="92888-634">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-634">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-635">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-635">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-636">64</span><span class="sxs-lookup"><span data-stu-id="92888-636">64</span></span> |
| <span data-ttu-id="92888-637">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-637">Format Support</span></span> | \- |
| <span data-ttu-id="92888-638">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-638">Buffer</span></span> | \- |
| <span data-ttu-id="92888-639">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-639">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-640">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-640">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-641">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-641">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-642">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-642">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-643">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-643">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-644">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-644">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-645">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-645">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-646">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-646">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-647">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-647">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-648">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-648">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-649">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-649">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-650">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-650">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-651">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-651">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-652">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-652">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-653">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-653">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-654">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-654">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-655">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-655">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-656">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-656">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-657">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-657">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-658">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-658">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-659">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-659">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-660">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-660">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-661">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-661">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-662">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-662">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-663">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-663">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-664">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-664">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-665">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-665">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-666">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-666">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-667">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-667">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-668">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-668">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-669">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-669">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-670">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-670">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-671">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-671">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-672">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-672">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-673">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-673">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-674">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-674">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-675">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-675">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-676">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-676">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-677">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-677">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-678">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-678">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-679">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-679">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-680">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-680">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-682">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-682">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfnssup-11"></a><span data-ttu-id="92888-683">DXGI_FORMAT_R16G16B16A16 \_ UNORM<sup>FNS</sup> (11)</span><span class="sxs-lookup"><span data-stu-id="92888-683">DXGI_FORMAT_R16G16B16A16\_UNORM<sup>FNS</sup> (11)</span></span>
| <span data-ttu-id="92888-684">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-684">Target</span></span> | <span data-ttu-id="92888-685">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-685">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-686">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-686">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-687">64</span><span class="sxs-lookup"><span data-stu-id="92888-687">64</span></span> |
| <span data-ttu-id="92888-688">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-688">Format Support</span></span> | \- |
| <span data-ttu-id="92888-689">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-689">Buffer</span></span> | \- |
| <span data-ttu-id="92888-690">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-690">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-691">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-691">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-692">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-692">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-693">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-693">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-694">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-694">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-695">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-695">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-696">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-696">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-697">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-697">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-698">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-698">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-699">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-699">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-700">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-700">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-701">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-701">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-702">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-702">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-703">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-703">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-704">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-704">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-705">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-705">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-706">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-706">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-707">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-707">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-708">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-708">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-709">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-709">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-710">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-710">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-711">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-711">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-712">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-712">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-713">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-713">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-714">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-714">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-715">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-715">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-716">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-716">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-717">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-717">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-718">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-718">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-719">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-719">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-720">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-720">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-721">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-721">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-722">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-722">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-723">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-723">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-724">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-724">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-725">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-725">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-726">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-726">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-727">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-727">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-728">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-728">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-729">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-729">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-730">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-730">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-731">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-731">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-732">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-732">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfnssup-12"></a><span data-ttu-id="92888-733">DXGI_FORMAT_R16G16B16A16 \_ uint<sup>FNS</sup> (12)</span><span class="sxs-lookup"><span data-stu-id="92888-733">DXGI_FORMAT_R16G16B16A16\_UINT<sup>FNS</sup> (12)</span></span>
| <span data-ttu-id="92888-734">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-734">Target</span></span> | <span data-ttu-id="92888-735">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-735">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-736">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-736">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-737">64</span><span class="sxs-lookup"><span data-stu-id="92888-737">64</span></span> |
| <span data-ttu-id="92888-738">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-738">Format Support</span></span> | \- |
| <span data-ttu-id="92888-739">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-739">Buffer</span></span> | \- |
| <span data-ttu-id="92888-740">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-740">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-741">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-741">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-742">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-742">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-743">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-743">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-744">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-744">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-745">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-745">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-746">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-746">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-747">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-747">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-748">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-748">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-749">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-749">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-750">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-750">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-751">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-751">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-752">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-752">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-753">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-753">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-754">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-754">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-755">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-755">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-756">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-756">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-757">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-757">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-758">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-758">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-759">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-759">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-760">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-760">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-761">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-761">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-762">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-762">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-763">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-763">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-764">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-764">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-765">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-765">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-766">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-766">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-767">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-767">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-768">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-768">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-769">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-769">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-770">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-770">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-771">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-771">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-772">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-772">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-773">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-773">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-774">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-774">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-775">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-775">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-776">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-776">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-777">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-777">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-778">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-778">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-779">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-779">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-780">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-780">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-781">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-781">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-782">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-782">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfnssup-13"></a><span data-ttu-id="92888-783">DXGI_FORMAT_R16G16B16A16 \_ SNORM<sup>FNS</sup> (13)</span><span class="sxs-lookup"><span data-stu-id="92888-783">DXGI_FORMAT_R16G16B16A16\_SNORM<sup>FNS</sup> (13)</span></span>
| <span data-ttu-id="92888-784">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-784">Target</span></span> | <span data-ttu-id="92888-785">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-785">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-786">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-786">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-787">64</span><span class="sxs-lookup"><span data-stu-id="92888-787">64</span></span> |
| <span data-ttu-id="92888-788">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-788">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-790">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-790">Buffer</span></span> | \- |
| <span data-ttu-id="92888-791">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-791">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-793">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-793">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-794">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-794">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-795">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-795">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-796">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-796">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-797">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-797">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-798">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-798">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-799">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-799">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-800">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-800">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-801">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-801">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-802">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-802">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-803">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-803">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-804">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-804">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-805">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-805">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-806">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-806">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-807">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-807">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-808">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-808">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-809">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-809">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-810">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-810">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-811">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-811">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-812">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-812">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-813">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-813">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-814">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-814">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-815">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-815">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-816">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-816">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-817">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-817">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-818">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-818">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-819">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-819">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-820">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-820">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-821">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-821">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-822">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-822">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-823">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-823">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-824">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-824">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-825">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-825">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-826">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-826">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-827">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-827">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-828">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-828">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-829">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-829">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-830">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-830">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-831">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-831">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-832">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-832">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-833">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-833">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-834">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-834">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfnssup-14"></a><span data-ttu-id="92888-835">DXGI_FORMAT_R16G16B16A16 \_ Santo<sup>FNS</sup> (14)</span><span class="sxs-lookup"><span data-stu-id="92888-835">DXGI_FORMAT_R16G16B16A16\_SINT<sup>FNS</sup> (14)</span></span>
| <span data-ttu-id="92888-836">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-836">Target</span></span> | <span data-ttu-id="92888-837">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-837">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-838">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-838">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-839">64</span><span class="sxs-lookup"><span data-stu-id="92888-839">64</span></span> |
| <span data-ttu-id="92888-840">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-840">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-842">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-842">Buffer</span></span> | \- |
| <span data-ttu-id="92888-843">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-843">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-845">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-845">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-846">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-846">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-847">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-847">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-848">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-848">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-849">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-849">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-850">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-850">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-851">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-851">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-852">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-852">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-853">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-853">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-854">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-854">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-855">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-855">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-856">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-856">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-857">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-857">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-858">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-858">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-859">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-859">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-860">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-860">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-861">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-861">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-862">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-862">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-863">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-863">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-864">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-864">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-865">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-865">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-866">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-866">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-867">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-867">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-868">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-868">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-869">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-869">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-870">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-870">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-871">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-871">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-872">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-872">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-873">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-873">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-874">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-874">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-875">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-875">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-876">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-876">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-877">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-877">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-878">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-878">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-879">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-879">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-880">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-880">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-881">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-881">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-882">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-882">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-883">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-883">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-884">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-884">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-885">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-885">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-886">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-886">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="92888-887">DXGI_FORMAT_R32G32 \_ <sup>PCs</sup> não tipados (15)</span><span class="sxs-lookup"><span data-stu-id="92888-887">DXGI_FORMAT_R32G32\_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="92888-888">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-888">Target</span></span> | <span data-ttu-id="92888-889">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-889">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-890">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-890">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-891">64</span><span class="sxs-lookup"><span data-stu-id="92888-891">64</span></span> |
| <span data-ttu-id="92888-892">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-892">Format Support</span></span> | \- |
| <span data-ttu-id="92888-893">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-893">Buffer</span></span> | \- |
| <span data-ttu-id="92888-894">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-894">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-895">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-895">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-896">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-896">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-897">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-897">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-898">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-898">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-899">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-899">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-900">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-900">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-901">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-901">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-902">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-902">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-903">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-903">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-904">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-904">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-905">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-905">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-906">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-906">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-907">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-907">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-908">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-908">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-909">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-909">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-910">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-910">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-911">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-911">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-912">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-912">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-913">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-913">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-914">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-914">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-915">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-915">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-916">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-916">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-917">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-917">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-918">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-918">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-919">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-919">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-920">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-920">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-921">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-921">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-922">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-922">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-923">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-923">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-924">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-924">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-925">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-925">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-926">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-926">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-927">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-927">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-928">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-928">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-929">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-929">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-930">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-930">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-931">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-931">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-932">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-932">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-933">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-933">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-934">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-934">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-935">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-935">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-936">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-936">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_floatsupfnssup-16"></a><span data-ttu-id="92888-937">DXGI_FORMAT_R32G32 \_ float<sup>FNS</sup> (16)</span><span class="sxs-lookup"><span data-stu-id="92888-937">DXGI_FORMAT_R32G32\_FLOAT<sup>FNS</sup> (16)</span></span>
| <span data-ttu-id="92888-938">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-938">Target</span></span> | <span data-ttu-id="92888-939">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-939">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-940">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-940">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-941">64</span><span class="sxs-lookup"><span data-stu-id="92888-941">64</span></span> |
| <span data-ttu-id="92888-942">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-942">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-944">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-944">Buffer</span></span> | \- |
| <span data-ttu-id="92888-945">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-945">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-947">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-947">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-948">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-948">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-949">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-949">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-950">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-950">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-951">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-951">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-952">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-952">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-953">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-953">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-954">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-954">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-955">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-955">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-956">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-956">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-957">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-957">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-958">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-958">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-959">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-959">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-960">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-960">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-961">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-961">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-962">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-962">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-963">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-963">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-964">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-964">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-965">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-965">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-966">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-966">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-967">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-967">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-968">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-968">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-969">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-969">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-970">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-970">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-971">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-971">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-972">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-972">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-973">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-973">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-974">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-974">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-975">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-975">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-976">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-976">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-977">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-977">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-978">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-978">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-979">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-979">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-980">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-980">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-981">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-981">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-982">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-982">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-983">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-983">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-984">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-984">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-985">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-985">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-986">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-986">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-987">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-987">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-988">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-988">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_uintsupfnssup-17"></a><span data-ttu-id="92888-989">DXGI_FORMAT_R32G32 \_ uint<sup>FNS</sup> (17)</span><span class="sxs-lookup"><span data-stu-id="92888-989">DXGI_FORMAT_R32G32\_UINT<sup>FNS</sup> (17)</span></span>
| <span data-ttu-id="92888-990">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-990">Target</span></span> | <span data-ttu-id="92888-991">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-991">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-992">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-992">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-993">64</span><span class="sxs-lookup"><span data-stu-id="92888-993">64</span></span> |
| <span data-ttu-id="92888-994">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-994">Format Support</span></span> | \- |
| <span data-ttu-id="92888-995">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-995">Buffer</span></span> | \- |
| <span data-ttu-id="92888-996">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-996">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-997">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-997">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-998">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-998">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-999">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-999">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-1000">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-1000">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-1001">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-1001">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-1002">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-1002">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-1003">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-1003">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-1004">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-1004">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-1005">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-1005">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-1006">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-1006">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-1007">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-1007">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-1008">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-1008">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-1009">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1009">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-1010">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1010">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-1011">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1011">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1012">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-1012">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1013">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-1013">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-1014">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-1014">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-1015">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-1015">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1016">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-1016">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1017">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-1017">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-1018">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1018">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-1019">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1019">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-1020">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1020">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-1021">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-1021">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-1022">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-1022">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-1023">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1023">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-1024">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-1024">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1025">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-1025">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1026">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-1026">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-1027">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1027">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1028">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-1028">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1029">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-1029">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-1030">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-1030">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-1031">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-1031">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-1032">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-1032">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-1033">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-1033">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-1034">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1034">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-1035">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1035">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-1036">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1036">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-1037">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-1037">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-1038">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-1038">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_sintsupfnssup-18"></a><span data-ttu-id="92888-1039">DXGI_FORMAT_R32G32 \_ Santo<sup>FNS</sup> (18)</span><span class="sxs-lookup"><span data-stu-id="92888-1039">DXGI_FORMAT_R32G32\_SINT<sup>FNS</sup> (18)</span></span>
| <span data-ttu-id="92888-1040">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-1040">Target</span></span> | <span data-ttu-id="92888-1041">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-1041">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-1042">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-1042">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-1043">64</span><span class="sxs-lookup"><span data-stu-id="92888-1043">64</span></span> |
| <span data-ttu-id="92888-1044">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-1044">Format Support</span></span> | \- |
| <span data-ttu-id="92888-1045">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-1045">Buffer</span></span> | \- |
| <span data-ttu-id="92888-1046">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1046">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-1047">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1047">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-1048">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-1048">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-1049">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-1049">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-1050">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-1050">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-1051">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-1051">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-1052">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-1052">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-1053">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-1053">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-1054">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-1054">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-1055">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-1055">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-1056">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-1056">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-1057">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-1057">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-1058">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-1058">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-1059">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1059">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-1060">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1060">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-1061">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1061">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1062">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-1062">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1063">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-1063">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-1064">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-1064">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-1065">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-1065">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1066">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-1066">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1067">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-1067">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-1068">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1068">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-1069">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1069">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-1070">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1070">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-1071">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-1071">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-1072">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-1072">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-1073">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1073">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-1074">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-1074">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1075">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-1075">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1076">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-1076">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-1077">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1077">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1078">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-1078">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1079">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-1079">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-1080">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-1080">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-1081">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-1081">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-1082">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-1082">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-1083">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-1083">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-1084">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1084">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-1085">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1085">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-1086">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1086">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-1087">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-1087">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-1088">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-1088">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a><span data-ttu-id="92888-1089">DXGI_FORMAT_R32G8X24 \_ <sup>PCs</sup> não tipados (19)</span><span class="sxs-lookup"><span data-stu-id="92888-1089">DXGI_FORMAT_R32G8X24\_TYPELESS<sup>PCS</sup> (19)</span></span>
| <span data-ttu-id="92888-1090">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-1090">Target</span></span> | <span data-ttu-id="92888-1091">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-1091">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-1092">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-1092">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-1093">64</span><span class="sxs-lookup"><span data-stu-id="92888-1093">64</span></span> |
| <span data-ttu-id="92888-1094">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-1094">Format Support</span></span> | \- |
| <span data-ttu-id="92888-1095">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-1095">Buffer</span></span> | \- |
| <span data-ttu-id="92888-1096">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1096">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-1097">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1097">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-1098">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-1098">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-1099">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-1099">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-1100">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-1100">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-1101">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-1101">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-1102">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-1102">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-1103">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-1103">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-1104">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-1104">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-1105">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-1105">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-1106">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-1106">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-1107">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-1107">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-1108">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-1108">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-1109">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1109">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-1110">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1110">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-1111">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1111">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1112">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-1112">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1113">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-1113">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-1114">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-1114">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-1115">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-1115">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1116">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-1116">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1117">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-1117">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-1118">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1118">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-1119">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1119">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-1120">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1120">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-1121">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-1121">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-1122">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-1122">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-1123">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1123">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-1124">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-1124">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1125">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-1125">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1126">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-1126">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-1127">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1127">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1128">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-1128">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1129">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-1129">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-1130">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-1130">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-1131">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-1131">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-1132">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-1132">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-1133">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-1133">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-1134">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1134">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-1135">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1135">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-1136">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1136">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-1137">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-1137">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-1138">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-1138">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfnssup-20"></a><span data-ttu-id="92888-1139">DXGI_FORMAT_D32 \_ float \_ S8X24 \_ uint<sup>FNS</sup> (20)</span><span class="sxs-lookup"><span data-stu-id="92888-1139">DXGI_FORMAT_D32\_FLOAT\_S8X24\_UINT<sup>FNS</sup> (20)</span></span>
| <span data-ttu-id="92888-1140">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-1140">Target</span></span> | <span data-ttu-id="92888-1141">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-1141">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-1142">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-1142">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-1143">64</span><span class="sxs-lookup"><span data-stu-id="92888-1143">64</span></span> |
| <span data-ttu-id="92888-1144">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-1144">Format Support</span></span> | \- |
| <span data-ttu-id="92888-1145">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-1145">Buffer</span></span> | \- |
| <span data-ttu-id="92888-1146">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1146">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-1147">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1147">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-1148">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-1148">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-1149">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-1149">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-1150">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-1150">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-1151">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-1151">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-1152">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-1152">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-1153">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-1153">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-1154">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-1154">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-1155">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-1155">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-1156">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-1156">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-1157">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-1157">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-1158">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-1158">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-1159">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1159">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-1160">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1160">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-1161">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1161">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1162">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-1162">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1163">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-1163">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-1164">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-1164">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-1165">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-1165">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1166">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-1166">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1167">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-1167">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-1168">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1168">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-1169">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1169">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-1170">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1170">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-1171">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-1171">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-1172">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-1172">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-1173">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1173">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-1174">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-1174">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1175">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-1175">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1176">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-1176">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-1177">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1177">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1178">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-1178">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1179">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-1179">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-1180">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-1180">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-1181">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-1181">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-1182">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-1182">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-1183">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-1183">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-1184">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1184">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-1185">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1185">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-1186">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1186">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-1187">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-1187">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-1188">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-1188">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfnssup-21"></a><span data-ttu-id="92888-1189">DXGI_FORMAT_R32 \_ float \_ X8X24 \_ <sup>FNS</sup> (21)</span><span class="sxs-lookup"><span data-stu-id="92888-1189">DXGI_FORMAT_R32\_FLOAT\_X8X24\_TYPELESS<sup>FNS</sup> (21)</span></span>
| <span data-ttu-id="92888-1190">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-1190">Target</span></span> | <span data-ttu-id="92888-1191">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-1191">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-1192">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-1192">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-1193">64</span><span class="sxs-lookup"><span data-stu-id="92888-1193">64</span></span> |
| <span data-ttu-id="92888-1194">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-1194">Format Support</span></span> | \- |
| <span data-ttu-id="92888-1195">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-1195">Buffer</span></span> | \- |
| <span data-ttu-id="92888-1196">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1196">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-1197">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1197">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-1198">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-1198">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-1199">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-1199">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-1200">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-1200">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-1201">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-1201">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-1202">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-1202">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-1203">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-1203">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-1204">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-1204">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-1205">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-1205">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-1206">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-1206">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-1207">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-1207">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-1208">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-1208">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-1209">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1209">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-1210">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1210">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-1211">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1211">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1212">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-1212">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1213">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-1213">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-1214">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-1214">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-1215">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-1215">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1216">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-1216">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1217">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-1217">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-1218">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1218">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-1219">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1219">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-1220">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1220">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-1221">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-1221">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-1222">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-1222">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-1223">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1223">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-1224">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-1224">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1225">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-1225">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1226">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-1226">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-1227">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1227">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1228">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-1228">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1229">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-1229">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-1230">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-1230">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-1231">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-1231">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-1232">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-1232">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-1233">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-1233">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-1234">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1234">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-1235">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1235">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-1236">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1236">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-1237">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-1237">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-1238">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-1238">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfnssup-22"></a><span data-ttu-id="92888-1239">DXGI_FORMAT_X32 \_ \_ \_ <sup>FNS</sup> uintless G8X24 (22)</span><span class="sxs-lookup"><span data-stu-id="92888-1239">DXGI_FORMAT_X32\_TYPELESS\_G8X24\_UINT<sup>FNS</sup> (22)</span></span>
| <span data-ttu-id="92888-1240">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-1240">Target</span></span> | <span data-ttu-id="92888-1241">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-1241">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-1242">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-1242">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-1243">64</span><span class="sxs-lookup"><span data-stu-id="92888-1243">64</span></span> |
| <span data-ttu-id="92888-1244">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-1244">Format Support</span></span> | \- |
| <span data-ttu-id="92888-1245">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-1245">Buffer</span></span> | \- |
| <span data-ttu-id="92888-1246">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1246">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-1247">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1247">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-1248">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-1248">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-1249">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-1249">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-1250">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-1250">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-1251">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-1251">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-1252">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-1252">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-1253">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-1253">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-1254">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-1254">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-1255">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-1255">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-1256">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-1256">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-1257">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-1257">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-1258">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-1258">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-1259">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1259">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-1260">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1260">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-1261">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1261">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1262">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-1262">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1263">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-1263">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-1264">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-1264">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-1265">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-1265">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1266">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-1266">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1267">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-1267">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-1268">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1268">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-1269">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1269">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-1270">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1270">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-1271">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-1271">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-1272">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-1272">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-1273">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1273">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-1274">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-1274">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1275">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-1275">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1276">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-1276">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-1277">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1277">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1278">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-1278">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1279">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-1279">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-1280">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-1280">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-1281">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-1281">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-1282">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-1282">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-1283">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-1283">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-1284">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1284">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-1285">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1285">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-1286">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1286">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-1287">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-1287">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-1288">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-1288">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="92888-1289">DXGI_FORMAT_R10G10B10A2 \_ <sup>PCs</sup> não tipados (23)</span><span class="sxs-lookup"><span data-stu-id="92888-1289">DXGI_FORMAT_R10G10B10A2\_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="92888-1290">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-1290">Target</span></span> | <span data-ttu-id="92888-1291">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-1291">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-1292">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-1292">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-1293">32</span><span class="sxs-lookup"><span data-stu-id="92888-1293">32</span></span> |
| <span data-ttu-id="92888-1294">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-1294">Format Support</span></span> | \- |
| <span data-ttu-id="92888-1295">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-1295">Buffer</span></span> | \- |
| <span data-ttu-id="92888-1296">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1296">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-1297">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1297">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-1298">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-1298">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-1299">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-1299">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-1300">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-1300">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-1301">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-1301">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-1302">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-1302">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-1303">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-1303">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-1304">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-1304">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-1305">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-1305">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-1306">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-1306">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-1307">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-1307">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-1308">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-1308">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-1309">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1309">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-1310">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1310">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-1311">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1311">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1312">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-1312">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1313">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-1313">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-1314">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-1314">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-1315">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-1315">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1316">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-1316">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1317">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-1317">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-1318">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1318">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-1319">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1319">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-1320">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1320">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-1321">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-1321">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-1322">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-1322">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-1323">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1323">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-1324">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-1324">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1325">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-1325">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1326">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-1326">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-1327">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1327">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1328">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-1328">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1329">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-1329">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-1330">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-1330">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-1331">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-1331">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-1332">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-1332">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-1333">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-1333">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-1334">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1334">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-1335">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1335">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-1336">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1336">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-1337">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-1337">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-1338">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-1338">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfnssup-24"></a><span data-ttu-id="92888-1339">DXGI_FORMAT_R10G10B10A2 \_ UNORM<sup>FNS</sup> (24)</span><span class="sxs-lookup"><span data-stu-id="92888-1339">DXGI_FORMAT_R10G10B10A2\_UNORM<sup>FNS</sup> (24)</span></span>
| <span data-ttu-id="92888-1340">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-1340">Target</span></span> | <span data-ttu-id="92888-1341">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-1341">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-1342">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-1342">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-1343">32</span><span class="sxs-lookup"><span data-stu-id="92888-1343">32</span></span> |
| <span data-ttu-id="92888-1344">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-1344">Format Support</span></span> | \- |
| <span data-ttu-id="92888-1345">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-1345">Buffer</span></span> | \- |
| <span data-ttu-id="92888-1346">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1346">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-1347">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1347">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-1348">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-1348">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-1349">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-1349">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-1350">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-1350">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-1351">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-1351">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-1352">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-1352">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-1353">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-1353">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-1354">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-1354">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-1355">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-1355">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-1356">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-1356">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-1357">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-1357">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-1358">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-1358">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-1359">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1359">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-1360">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1360">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-1361">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1361">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1362">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-1362">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1363">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-1363">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-1364">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-1364">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-1365">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-1365">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1366">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-1366">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1367">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-1367">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-1368">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1368">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-1369">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1369">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-1370">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1370">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-1371">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-1371">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-1372">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-1372">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-1373">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1373">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-1374">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-1374">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1375">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-1375">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1376">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-1376">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-1377">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1377">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1378">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-1378">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1379">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-1379">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-1380">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-1380">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-1381">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-1381">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-1382">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-1382">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-1383">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-1383">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-1384">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1384">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-1385">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1385">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-1386">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1386">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-1387">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-1387">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1389">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-1389">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfnssup-25"></a><span data-ttu-id="92888-1390">DXGI_FORMAT_R10G10B10A2 \_ uint<sup>FNS</sup> (25)</span><span class="sxs-lookup"><span data-stu-id="92888-1390">DXGI_FORMAT_R10G10B10A2\_UINT<sup>FNS</sup> (25)</span></span>
| <span data-ttu-id="92888-1391">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-1391">Target</span></span> | <span data-ttu-id="92888-1392">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-1392">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-1393">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-1393">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-1394">32</span><span class="sxs-lookup"><span data-stu-id="92888-1394">32</span></span> |
| <span data-ttu-id="92888-1395">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-1395">Format Support</span></span> | \- |
| <span data-ttu-id="92888-1396">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-1396">Buffer</span></span> | \- |
| <span data-ttu-id="92888-1397">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1397">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-1398">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1398">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-1399">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-1399">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-1400">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-1400">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-1401">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-1401">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-1402">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-1402">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-1403">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-1403">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-1404">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-1404">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-1405">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-1405">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-1406">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-1406">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-1407">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-1407">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-1408">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-1408">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-1409">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-1409">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-1410">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1410">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-1411">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1411">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-1412">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1412">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1413">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-1413">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1414">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-1414">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-1415">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-1415">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-1416">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-1416">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1417">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-1417">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1418">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-1418">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-1419">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1419">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-1420">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1420">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-1421">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1421">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-1422">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-1422">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-1423">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-1423">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-1424">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1424">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-1425">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-1425">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1426">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-1426">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1427">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-1427">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-1428">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1428">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1429">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-1429">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1430">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-1430">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-1431">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-1431">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-1432">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-1432">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-1433">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-1433">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-1434">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-1434">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-1435">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1435">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-1436">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1436">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-1437">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1437">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-1438">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-1438">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-1439">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-1439">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfnssup-89"></a><span data-ttu-id="92888-1440">DXGI_FORMAT_R10G10B10 \_ XR \_ Bias \_ a2 \_ UNORM<sup>FNS</sup> (89)</span><span class="sxs-lookup"><span data-stu-id="92888-1440">DXGI_FORMAT_R10G10B10\_XR\_BIAS\_A2\_UNORM<sup>FNS</sup> (89)</span></span>
| <span data-ttu-id="92888-1441">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-1441">Target</span></span> | <span data-ttu-id="92888-1442">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-1442">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-1443">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-1443">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-1444">32</span><span class="sxs-lookup"><span data-stu-id="92888-1444">32</span></span> |
| <span data-ttu-id="92888-1445">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-1445">Format Support</span></span> | \- |
| <span data-ttu-id="92888-1446">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-1446">Buffer</span></span> | \- |
| <span data-ttu-id="92888-1447">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1447">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-1448">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1448">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-1449">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-1449">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-1450">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-1450">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-1451">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-1451">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-1452">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-1452">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-1453">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-1453">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-1454">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-1454">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-1455">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-1455">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-1456">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-1456">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-1457">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-1457">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-1458">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-1458">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-1459">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-1459">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-1460">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1460">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-1461">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1461">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-1462">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1462">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1463">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-1463">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1464">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-1464">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-1465">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-1465">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-1466">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-1466">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1467">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-1467">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1468">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-1468">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-1469">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1469">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-1470">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1470">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-1471">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1471">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-1472">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-1472">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-1473">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-1473">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-1474">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1474">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-1475">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-1475">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1476">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-1476">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1477">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-1477">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-1478">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1478">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1479">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-1479">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1480">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-1480">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-1481">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-1481">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-1482">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-1482">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-1483">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-1483">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-1484">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-1484">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-1485">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1485">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-1486">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1486">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-1487">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1487">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-1488">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-1488">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-1489">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-1489">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="92888-1490">DXGI_FORMAT_R11G11B10 \_ float<sup>FNS</sup> (26)</span><span class="sxs-lookup"><span data-stu-id="92888-1490">DXGI_FORMAT_R11G11B10\_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="92888-1491">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-1491">Target</span></span> | <span data-ttu-id="92888-1492">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-1492">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-1493">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-1493">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-1494">32</span><span class="sxs-lookup"><span data-stu-id="92888-1494">32</span></span> |
| <span data-ttu-id="92888-1495">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-1495">Format Support</span></span> | \- |
| <span data-ttu-id="92888-1496">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-1496">Buffer</span></span> | \- |
| <span data-ttu-id="92888-1497">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1497">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-1498">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1498">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-1499">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-1499">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-1500">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-1500">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-1501">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-1501">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-1502">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-1502">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-1503">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-1503">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-1504">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-1504">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-1505">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-1505">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-1506">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-1506">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-1507">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-1507">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-1508">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-1508">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-1509">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-1509">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-1510">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1510">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-1511">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1511">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-1512">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1512">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1513">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-1513">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1514">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-1514">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-1515">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-1515">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-1516">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-1516">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1517">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-1517">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1518">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-1518">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-1519">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1519">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-1520">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1520">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-1521">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1521">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-1522">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-1522">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-1523">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-1523">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-1524">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1524">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-1525">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-1525">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1526">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-1526">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1527">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-1527">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-1528">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1528">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1529">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-1529">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1530">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-1530">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-1531">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-1531">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-1532">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-1532">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-1533">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-1533">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-1534">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-1534">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-1535">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1535">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-1536">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1536">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-1537">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1537">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-1538">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-1538">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-1539">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-1539">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="92888-1540">DXGI_FORMAT_R8G8B8A8 \_ <sup>PCs</sup> não tipados (27)</span><span class="sxs-lookup"><span data-stu-id="92888-1540">DXGI_FORMAT_R8G8B8A8\_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="92888-1541">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-1541">Target</span></span> | <span data-ttu-id="92888-1542">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-1542">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-1543">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-1543">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-1544">32</span><span class="sxs-lookup"><span data-stu-id="92888-1544">32</span></span> |
| <span data-ttu-id="92888-1545">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-1545">Format Support</span></span> | \- |
| <span data-ttu-id="92888-1546">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-1546">Buffer</span></span> | \- |
| <span data-ttu-id="92888-1547">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1547">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-1548">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1548">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-1549">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-1549">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-1550">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-1550">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-1551">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-1551">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-1552">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-1552">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-1553">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-1553">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-1554">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-1554">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-1555">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-1555">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-1556">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-1556">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-1557">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-1557">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-1558">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-1558">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-1559">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-1559">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-1560">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1560">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-1561">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1561">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-1562">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1562">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1563">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-1563">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1564">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-1564">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-1565">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-1565">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-1566">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-1566">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1567">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-1567">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1568">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-1568">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-1569">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1569">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-1570">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1570">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-1571">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1571">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-1572">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-1572">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-1573">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-1573">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-1574">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1574">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-1575">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-1575">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1576">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-1576">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1577">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-1577">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-1578">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1578">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1579">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-1579">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1580">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-1580">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-1581">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-1581">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-1582">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-1582">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-1583">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-1583">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-1584">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-1584">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-1585">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1585">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-1586">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1586">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-1587">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1587">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-1588">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-1588">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-1589">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-1589">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfnssup-28"></a><span data-ttu-id="92888-1590">DXGI_FORMAT_R8G8B8A8 \_ UNORM<sup>FNS</sup> (28)</span><span class="sxs-lookup"><span data-stu-id="92888-1590">DXGI_FORMAT_R8G8B8A8\_UNORM<sup>FNS</sup> (28)</span></span>
| <span data-ttu-id="92888-1591">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-1591">Target</span></span> | <span data-ttu-id="92888-1592">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-1592">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-1593">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-1593">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-1594">32</span><span class="sxs-lookup"><span data-stu-id="92888-1594">32</span></span> |
| <span data-ttu-id="92888-1595">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-1595">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1597">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-1597">Buffer</span></span> | \- |
| <span data-ttu-id="92888-1598">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1598">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1600">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1600">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-1601">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-1601">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-1602">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-1602">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-1603">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-1603">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1605">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-1605">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1607">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-1607">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1609">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-1609">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1611">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-1611">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1613">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-1613">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-1614">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-1614">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-1615">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-1615">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-1616">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-1616">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-1617">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1617">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1619">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1619">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1621">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1621">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1623">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-1623">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1625">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-1625">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-1626">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-1626">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-1627">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-1627">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1628">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-1628">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1629">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-1629">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-1630">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1630">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-1631">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1631">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-1632">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1632">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-1633">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-1633">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-1634">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-1634">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-1635">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1635">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-1636">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-1636">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1637">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-1637">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1638">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-1638">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1640">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1640">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-1642">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-1642">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-1644">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-1644">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-1646">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-1646">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1648">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-1648">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-1649">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-1649">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1651">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-1651">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-1652">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1652">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-1653">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1653">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-1655">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1655">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1657">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-1657">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1659">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-1659">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfnssup-29"></a><span data-ttu-id="92888-1660">DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ sRGB<sup>FNS</sup> (29)</span><span class="sxs-lookup"><span data-stu-id="92888-1660">DXGI_FORMAT_R8G8B8A8\_UNORM\_SRGB<sup>FNS</sup> (29)</span></span>
| <span data-ttu-id="92888-1661">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-1661">Target</span></span> | <span data-ttu-id="92888-1662">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-1662">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-1663">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-1663">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-1664">32</span><span class="sxs-lookup"><span data-stu-id="92888-1664">32</span></span> |
| <span data-ttu-id="92888-1665">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-1665">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1667">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-1667">Buffer</span></span> | \- |
| <span data-ttu-id="92888-1668">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1668">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-1669">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1669">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-1670">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-1670">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-1671">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-1671">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-1672">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-1672">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1674">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-1674">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1676">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-1676">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1678">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-1678">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1680">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-1680">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1682">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-1682">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-1683">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-1683">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-1684">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-1684">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-1685">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-1685">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-1686">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1686">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1688">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1688">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1690">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1690">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1692">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-1692">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1694">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-1694">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-1695">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-1695">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-1696">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-1696">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1697">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-1697">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1698">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-1698">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-1699">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1699">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-1700">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1700">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-1701">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1701">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-1702">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-1702">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-1703">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-1703">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-1704">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1704">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-1705">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-1705">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1706">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-1706">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1707">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-1707">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1709">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1709">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-1711">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-1711">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-1713">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-1713">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-1715">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-1715">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1717">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-1717">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-1718">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-1718">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1720">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-1720">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-1721">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1721">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-1722">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1722">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-1724">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1724">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1726">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-1726">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1728">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-1728">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfnssup-30"></a><span data-ttu-id="92888-1729">DXGI_FORMAT_R8G8B8A8 \_ uint<sup>FNS</sup> (30)</span><span class="sxs-lookup"><span data-stu-id="92888-1729">DXGI_FORMAT_R8G8B8A8\_UINT<sup>FNS</sup> (30)</span></span>
| <span data-ttu-id="92888-1730">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-1730">Target</span></span> | <span data-ttu-id="92888-1731">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-1731">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-1732">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-1732">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-1733">32</span><span class="sxs-lookup"><span data-stu-id="92888-1733">32</span></span> |
| <span data-ttu-id="92888-1734">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-1734">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1736">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-1736">Buffer</span></span> | \- |
| <span data-ttu-id="92888-1737">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1737">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1739">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1739">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-1740">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-1740">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-1741">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-1741">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-1742">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-1742">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-1743">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-1743">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-1744">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-1744">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-1745">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-1745">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-1746">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-1746">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-1747">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-1747">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-1748">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-1748">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-1749">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-1749">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-1750">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-1750">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-1751">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1751">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-1752">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1752">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-1753">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1753">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1754">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-1754">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1755">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-1755">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-1756">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-1756">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-1757">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-1757">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1758">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-1758">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1759">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-1759">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-1760">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1760">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-1761">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1761">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-1762">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1762">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-1763">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-1763">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-1764">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-1764">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-1765">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1765">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-1766">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-1766">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1767">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-1767">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1768">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-1768">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-1769">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1769">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1770">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-1770">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1771">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-1771">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-1772">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-1772">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-1773">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-1773">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-1774">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-1774">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-1775">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-1775">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-1776">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1776">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-1777">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1777">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-1778">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1778">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-1779">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-1779">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-1780">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-1780">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfnssup-31"></a><span data-ttu-id="92888-1781">DXGI_FORMAT_R8G8B8A8 \_ SNORM<sup>FNS</sup> (31)</span><span class="sxs-lookup"><span data-stu-id="92888-1781">DXGI_FORMAT_R8G8B8A8\_SNORM<sup>FNS</sup> (31)</span></span>
| <span data-ttu-id="92888-1782">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-1782">Target</span></span> | <span data-ttu-id="92888-1783">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-1783">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-1784">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-1784">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-1785">32</span><span class="sxs-lookup"><span data-stu-id="92888-1785">32</span></span> |
| <span data-ttu-id="92888-1786">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-1786">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1788">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-1788">Buffer</span></span> | \- |
| <span data-ttu-id="92888-1789">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1789">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-1790">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1790">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-1791">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-1791">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-1792">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-1792">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-1793">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-1793">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1795">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-1795">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-1796">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-1796">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1798">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-1798">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1800">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-1800">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1802">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-1802">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-1803">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-1803">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-1804">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-1804">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-1805">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-1805">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-1806">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1806">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1808">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1808">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-1809">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1809">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1810">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-1810">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1811">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-1811">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-1812">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-1812">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-1813">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-1813">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1814">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-1814">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1815">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-1815">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-1816">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1816">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-1817">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1817">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-1818">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1818">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-1819">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-1819">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-1820">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-1820">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-1821">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1821">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-1822">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-1822">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1823">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-1823">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1824">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-1824">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-1826">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1826">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1827">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-1827">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1828">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-1828">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-1829">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-1829">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-1830">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-1830">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-1831">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-1831">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-1832">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-1832">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-1833">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1833">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-1834">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1834">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-1835">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1835">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-1836">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-1836">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-1837">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-1837">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfnssup-32"></a><span data-ttu-id="92888-1838">DXGI_FORMAT_R8G8B8A8 \_ Santo<sup>FNS</sup> (32)</span><span class="sxs-lookup"><span data-stu-id="92888-1838">DXGI_FORMAT_R8G8B8A8\_SINT<sup>FNS</sup> (32)</span></span>
| <span data-ttu-id="92888-1839">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-1839">Target</span></span> | <span data-ttu-id="92888-1840">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-1840">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-1841">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-1841">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-1842">32</span><span class="sxs-lookup"><span data-stu-id="92888-1842">32</span></span> |
| <span data-ttu-id="92888-1843">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-1843">Format Support</span></span> | \- |
| <span data-ttu-id="92888-1844">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-1844">Buffer</span></span> | \- |
| <span data-ttu-id="92888-1845">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1845">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-1846">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1846">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-1847">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-1847">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-1848">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-1848">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-1849">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-1849">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-1850">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-1850">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-1851">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-1851">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-1852">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-1852">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-1853">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-1853">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-1854">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-1854">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-1855">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-1855">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-1856">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-1856">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-1857">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-1857">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-1858">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1858">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-1859">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1859">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-1860">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1860">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1861">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-1861">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1862">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-1862">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-1863">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-1863">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-1864">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-1864">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1865">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-1865">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1866">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-1866">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-1867">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1867">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-1868">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1868">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-1869">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1869">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-1870">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-1870">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-1871">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-1871">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-1872">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1872">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-1873">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-1873">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1874">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-1874">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1875">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-1875">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-1876">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1876">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1877">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-1877">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1878">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-1878">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-1879">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-1879">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-1880">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-1880">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-1881">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-1881">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-1882">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-1882">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-1883">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1883">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-1884">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1884">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-1885">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1885">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-1886">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-1886">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-1887">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-1887">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="92888-1888">DXGI_FORMAT_R16G16 \_ <sup>PCs</sup> não tipados (33)</span><span class="sxs-lookup"><span data-stu-id="92888-1888">DXGI_FORMAT_R16G16\_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="92888-1889">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-1889">Target</span></span> | <span data-ttu-id="92888-1890">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-1890">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-1891">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-1891">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-1892">32</span><span class="sxs-lookup"><span data-stu-id="92888-1892">32</span></span> |
| <span data-ttu-id="92888-1893">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-1893">Format Support</span></span> | \- |
| <span data-ttu-id="92888-1894">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-1894">Buffer</span></span> | \- |
| <span data-ttu-id="92888-1895">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1895">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-1896">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1896">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-1897">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-1897">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-1898">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-1898">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-1899">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-1899">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-1900">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-1900">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-1901">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-1901">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-1902">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-1902">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-1903">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-1903">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-1904">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-1904">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-1905">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-1905">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-1906">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-1906">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-1907">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-1907">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-1908">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1908">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-1909">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1909">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-1910">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1910">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1911">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-1911">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1912">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-1912">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-1913">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-1913">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-1914">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-1914">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1915">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-1915">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1916">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-1916">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-1917">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1917">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-1918">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1918">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-1919">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1919">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-1920">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-1920">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-1921">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-1921">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-1922">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1922">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-1923">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-1923">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1924">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-1924">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1925">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-1925">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-1926">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1926">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1927">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-1927">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1928">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-1928">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-1929">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-1929">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-1930">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-1930">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-1931">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-1931">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-1932">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-1932">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-1933">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1933">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-1934">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1934">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-1935">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1935">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-1936">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-1936">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-1937">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-1937">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_floatsupfnssup-34"></a><span data-ttu-id="92888-1938">DXGI_FORMAT_R16G16 \_ float<sup>FNS</sup> (34)</span><span class="sxs-lookup"><span data-stu-id="92888-1938">DXGI_FORMAT_R16G16\_FLOAT<sup>FNS</sup> (34)</span></span>
| <span data-ttu-id="92888-1939">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-1939">Target</span></span> | <span data-ttu-id="92888-1940">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-1940">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-1941">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-1941">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-1942">32</span><span class="sxs-lookup"><span data-stu-id="92888-1942">32</span></span> |
| <span data-ttu-id="92888-1943">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-1943">Format Support</span></span> | \- |
| <span data-ttu-id="92888-1944">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-1944">Buffer</span></span> | \- |
| <span data-ttu-id="92888-1945">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1945">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-1946">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1946">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-1947">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-1947">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-1948">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-1948">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-1949">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-1949">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-1950">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-1950">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-1951">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-1951">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-1952">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-1952">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-1953">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-1953">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-1954">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-1954">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-1955">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-1955">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-1956">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-1956">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-1957">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-1957">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-1958">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1958">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-1959">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-1959">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-1960">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1960">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1961">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-1961">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1962">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-1962">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-1963">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-1963">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-1964">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-1964">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1965">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-1965">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-1966">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-1966">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-1967">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1967">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-1968">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1968">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-1969">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1969">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-1970">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-1970">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-1971">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-1971">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-1972">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-1972">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-1973">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-1973">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1974">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-1974">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-1975">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-1975">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-1976">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-1976">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1977">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-1977">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-1978">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-1978">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-1979">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-1979">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-1980">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-1980">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-1981">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-1981">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-1982">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-1982">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-1983">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1983">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-1984">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1984">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-1985">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-1985">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-1986">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-1986">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-1987">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-1987">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_unormsupfnssup-35"></a><span data-ttu-id="92888-1988">DXGI_FORMAT_R16G16 \_ UNORM<sup>FNS</sup> (35)</span><span class="sxs-lookup"><span data-stu-id="92888-1988">DXGI_FORMAT_R16G16\_UNORM<sup>FNS</sup> (35)</span></span>
| <span data-ttu-id="92888-1989">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-1989">Target</span></span> | <span data-ttu-id="92888-1990">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-1990">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-1991">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-1991">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-1992">32</span><span class="sxs-lookup"><span data-stu-id="92888-1992">32</span></span> |
| <span data-ttu-id="92888-1993">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-1993">Format Support</span></span> | \- |
| <span data-ttu-id="92888-1994">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-1994">Buffer</span></span> | \- |
| <span data-ttu-id="92888-1995">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1995">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-1996">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-1996">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-1997">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-1997">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-1998">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-1998">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-1999">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-1999">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-2000">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-2000">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-2001">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-2001">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-2002">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-2002">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-2003">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-2003">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-2004">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-2004">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-2005">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-2005">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-2006">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-2006">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-2007">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-2007">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-2008">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2008">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-2009">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2009">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-2010">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2010">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2011">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-2011">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2012">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-2012">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-2013">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-2013">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-2014">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-2014">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2015">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-2015">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2016">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-2016">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-2017">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2017">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-2018">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2018">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-2019">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2019">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-2020">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-2020">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-2021">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-2021">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-2022">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2022">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-2023">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-2023">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2024">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-2024">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2025">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-2025">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-2026">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2026">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2027">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-2027">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2028">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-2028">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-2029">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-2029">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-2030">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-2030">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-2031">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-2031">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-2032">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-2032">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-2033">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2033">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-2034">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2034">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-2035">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2035">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-2036">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-2036">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-2037">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-2037">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_uintsupfnssup-36"></a><span data-ttu-id="92888-2038">DXGI_FORMAT_R16G16 \_ uint<sup>FNS</sup> (36)</span><span class="sxs-lookup"><span data-stu-id="92888-2038">DXGI_FORMAT_R16G16\_UINT<sup>FNS</sup> (36)</span></span>
| <span data-ttu-id="92888-2039">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-2039">Target</span></span> | <span data-ttu-id="92888-2040">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-2040">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-2041">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-2041">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-2042">32</span><span class="sxs-lookup"><span data-stu-id="92888-2042">32</span></span> |
| <span data-ttu-id="92888-2043">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-2043">Format Support</span></span> | \- |
| <span data-ttu-id="92888-2044">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-2044">Buffer</span></span> | \- |
| <span data-ttu-id="92888-2045">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2045">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-2046">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2046">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-2047">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-2047">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-2048">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-2048">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-2049">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-2049">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-2050">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-2050">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-2051">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-2051">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-2052">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-2052">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-2053">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-2053">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-2054">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-2054">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-2055">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-2055">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-2056">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-2056">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-2057">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-2057">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-2058">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2058">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-2059">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2059">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-2060">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2060">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2061">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-2061">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2062">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-2062">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-2063">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-2063">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-2064">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-2064">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2065">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-2065">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2066">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-2066">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-2067">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2067">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-2068">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2068">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-2069">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2069">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-2070">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-2070">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-2071">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-2071">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-2072">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2072">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-2073">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-2073">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2074">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-2074">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2075">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-2075">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-2076">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2076">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2077">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-2077">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2078">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-2078">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-2079">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-2079">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-2080">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-2080">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-2081">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-2081">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-2082">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-2082">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-2083">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2083">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-2084">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2084">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-2085">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2085">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-2086">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-2086">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-2087">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-2087">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_snormsupfnssup-37"></a><span data-ttu-id="92888-2088">DXGI_FORMAT_R16G16 \_ SNORM<sup>FNS</sup> (37)</span><span class="sxs-lookup"><span data-stu-id="92888-2088">DXGI_FORMAT_R16G16\_SNORM<sup>FNS</sup> (37)</span></span>
| <span data-ttu-id="92888-2089">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-2089">Target</span></span> | <span data-ttu-id="92888-2090">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-2090">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-2091">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-2091">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-2092">32</span><span class="sxs-lookup"><span data-stu-id="92888-2092">32</span></span> |
| <span data-ttu-id="92888-2093">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-2093">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-2095">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-2095">Buffer</span></span> | \- |
| <span data-ttu-id="92888-2096">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2096">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-2098">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2098">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-2099">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-2099">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-2100">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-2100">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-2101">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-2101">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-2103">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-2103">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-2104">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-2104">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-2105">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-2105">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-2107">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-2107">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-2108">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-2108">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-2109">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-2109">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-2110">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-2110">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-2111">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-2111">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-2112">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2112">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-2114">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2114">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-2115">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2115">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2116">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-2116">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2117">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-2117">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-2118">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-2118">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-2119">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-2119">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2120">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-2120">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2121">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-2121">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-2122">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2122">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-2123">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2123">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-2124">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2124">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-2125">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-2125">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-2126">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-2126">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-2127">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2127">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-2128">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-2128">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2129">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-2129">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2130">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-2130">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-2132">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2132">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2133">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-2133">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2134">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-2134">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-2135">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-2135">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-2136">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-2136">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-2137">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-2137">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-2138">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-2138">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-2139">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2139">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-2140">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2140">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-2141">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2141">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-2142">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-2142">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-2143">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-2143">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_sintsupfnssup-38"></a><span data-ttu-id="92888-2144">DXGI_FORMAT_R16G16 \_ Santo<sup>FNS</sup> (38)</span><span class="sxs-lookup"><span data-stu-id="92888-2144">DXGI_FORMAT_R16G16\_SINT<sup>FNS</sup> (38)</span></span>
| <span data-ttu-id="92888-2145">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-2145">Target</span></span> | <span data-ttu-id="92888-2146">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-2146">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-2147">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-2147">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-2148">32</span><span class="sxs-lookup"><span data-stu-id="92888-2148">32</span></span> |
| <span data-ttu-id="92888-2149">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-2149">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-2151">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-2151">Buffer</span></span> | \- |
| <span data-ttu-id="92888-2152">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2152">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-2154">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2154">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-2155">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-2155">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-2156">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-2156">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-2157">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-2157">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-2158">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-2158">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-2159">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-2159">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-2160">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-2160">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-2161">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-2161">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-2162">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-2162">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-2163">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-2163">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-2164">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-2164">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-2165">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-2165">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-2166">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2166">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-2167">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2167">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-2168">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2168">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2169">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-2169">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2170">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-2170">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-2171">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-2171">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-2172">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-2172">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2173">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-2173">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2174">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-2174">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-2175">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2175">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-2176">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2176">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-2177">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2177">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-2178">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-2178">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-2179">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-2179">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-2180">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2180">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-2181">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-2181">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2182">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-2182">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2183">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-2183">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-2184">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2184">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2185">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-2185">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2186">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-2186">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-2187">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-2187">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-2188">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-2188">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-2189">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-2189">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-2190">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-2190">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-2191">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2191">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-2192">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2192">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-2193">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2193">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-2194">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-2194">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-2195">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-2195">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="92888-2196">DXGI_FORMAT_R32 \_ <sup>PCs</sup> não tipados (39)</span><span class="sxs-lookup"><span data-stu-id="92888-2196">DXGI_FORMAT_R32\_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="92888-2197">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-2197">Target</span></span> | <span data-ttu-id="92888-2198">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-2198">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-2199">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-2199">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-2200">32</span><span class="sxs-lookup"><span data-stu-id="92888-2200">32</span></span> |
| <span data-ttu-id="92888-2201">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-2201">Format Support</span></span> | \- |
| <span data-ttu-id="92888-2202">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-2202">Buffer</span></span> | \- |
| <span data-ttu-id="92888-2203">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2203">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-2204">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2204">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-2205">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-2205">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-2206">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-2206">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-2207">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-2207">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-2208">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-2208">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-2209">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-2209">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-2210">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-2210">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-2211">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-2211">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-2212">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-2212">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-2213">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-2213">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-2214">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-2214">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-2215">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-2215">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-2216">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2216">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-2217">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2217">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-2218">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2218">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2219">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-2219">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2220">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-2220">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-2221">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-2221">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-2222">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-2222">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2223">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-2223">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2224">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-2224">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-2225">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2225">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-2226">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2226">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-2227">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2227">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-2228">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-2228">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-2229">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-2229">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-2230">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2230">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-2231">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-2231">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2232">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-2232">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2233">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-2233">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-2234">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2234">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2235">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-2235">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2236">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-2236">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-2237">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-2237">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-2238">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-2238">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-2239">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-2239">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-2240">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-2240">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-2241">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2241">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-2242">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2242">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-2243">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2243">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-2244">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-2244">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-2245">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-2245">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_floatsupfnssup-40"></a><span data-ttu-id="92888-2246">DXGI_FORMAT_D32 \_ float<sup>FNS</sup> (40)</span><span class="sxs-lookup"><span data-stu-id="92888-2246">DXGI_FORMAT_D32\_FLOAT<sup>FNS</sup> (40)</span></span>
| <span data-ttu-id="92888-2247">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-2247">Target</span></span> | <span data-ttu-id="92888-2248">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-2248">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-2249">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-2249">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-2250">32</span><span class="sxs-lookup"><span data-stu-id="92888-2250">32</span></span> |
| <span data-ttu-id="92888-2251">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-2251">Format Support</span></span> | \- |
| <span data-ttu-id="92888-2252">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-2252">Buffer</span></span> | \- |
| <span data-ttu-id="92888-2253">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2253">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-2254">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2254">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-2255">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-2255">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-2256">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-2256">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-2257">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-2257">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-2258">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-2258">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-2259">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-2259">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-2260">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-2260">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-2261">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-2261">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-2262">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-2262">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-2263">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-2263">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-2264">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-2264">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-2265">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-2265">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-2266">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2266">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-2267">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2267">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-2268">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2268">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2269">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-2269">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2270">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-2270">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-2271">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-2271">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-2272">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-2272">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2273">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-2273">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2274">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-2274">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-2275">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2275">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-2276">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2276">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-2277">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2277">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-2278">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-2278">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-2279">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-2279">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-2280">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2280">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-2281">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-2281">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2282">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-2282">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2283">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-2283">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-2284">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2284">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2285">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-2285">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2286">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-2286">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-2287">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-2287">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-2288">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-2288">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-2289">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-2289">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-2290">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-2290">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-2291">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2291">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-2292">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2292">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-2293">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2293">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-2294">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-2294">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-2295">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-2295">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_floatsupfnssup-41"></a><span data-ttu-id="92888-2296">DXGI_FORMAT_R32 \_ float<sup>FNS</sup> (41)</span><span class="sxs-lookup"><span data-stu-id="92888-2296">DXGI_FORMAT_R32\_FLOAT<sup>FNS</sup> (41)</span></span>
| <span data-ttu-id="92888-2297">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-2297">Target</span></span> | <span data-ttu-id="92888-2298">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-2298">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-2299">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-2299">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-2300">32</span><span class="sxs-lookup"><span data-stu-id="92888-2300">32</span></span> |
| <span data-ttu-id="92888-2301">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-2301">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-2303">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-2303">Buffer</span></span> | \- |
| <span data-ttu-id="92888-2304">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2304">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-2306">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2306">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-2307">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-2307">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-2308">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-2308">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-2309">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-2309">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-2310">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-2310">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-2311">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-2311">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-2312">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-2312">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-2313">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-2313">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-2314">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-2314">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-2315">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-2315">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-2316">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-2316">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-2317">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-2317">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-2318">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2318">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-2319">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2319">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-2320">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2320">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2321">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-2321">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2322">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-2322">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-2323">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-2323">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-2324">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-2324">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2325">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-2325">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2326">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-2326">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-2327">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2327">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-2328">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2328">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-2329">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2329">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-2330">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-2330">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-2331">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-2331">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-2332">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2332">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-2333">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-2333">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2334">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-2334">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2335">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-2335">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-2336">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2336">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2337">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-2337">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2338">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-2338">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-2339">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-2339">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-2340">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-2340">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-2341">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-2341">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-2342">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-2342">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-2343">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2343">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-2344">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2344">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-2345">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2345">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-2346">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-2346">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-2347">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-2347">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_uintsupfnssup-42"></a><span data-ttu-id="92888-2348">DXGI_FORMAT_R32 \_ uint<sup>FNS</sup> (42)</span><span class="sxs-lookup"><span data-stu-id="92888-2348">DXGI_FORMAT_R32\_UINT<sup>FNS</sup> (42)</span></span>
| <span data-ttu-id="92888-2349">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-2349">Target</span></span> | <span data-ttu-id="92888-2350">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-2350">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-2351">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-2351">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-2352">32</span><span class="sxs-lookup"><span data-stu-id="92888-2352">32</span></span> |
| <span data-ttu-id="92888-2353">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-2353">Format Support</span></span> | \- |
| <span data-ttu-id="92888-2354">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-2354">Buffer</span></span> | \- |
| <span data-ttu-id="92888-2355">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2355">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-2356">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2356">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-2357">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-2357">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-2358">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-2358">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-2359">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-2359">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-2360">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-2360">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-2361">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-2361">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-2362">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-2362">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-2363">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-2363">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-2364">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-2364">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-2365">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-2365">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-2366">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-2366">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-2367">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-2367">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-2368">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2368">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-2369">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2369">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-2370">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2370">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2371">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-2371">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2372">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-2372">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-2373">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-2373">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-2374">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-2374">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2375">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-2375">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2376">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-2376">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-2377">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2377">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-2378">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2378">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-2379">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2379">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-2380">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-2380">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-2381">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-2381">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-2382">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2382">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-2383">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-2383">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2384">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-2384">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2385">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-2385">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-2386">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2386">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2387">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-2387">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2388">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-2388">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-2389">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-2389">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-2390">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-2390">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-2391">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-2391">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-2392">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-2392">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-2393">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2393">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-2394">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2394">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-2395">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2395">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-2396">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-2396">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-2397">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-2397">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_sintsupfnssup-43"></a><span data-ttu-id="92888-2398">DXGI_FORMAT_R32 \_ Santo<sup>FNS</sup> (43)</span><span class="sxs-lookup"><span data-stu-id="92888-2398">DXGI_FORMAT_R32\_SINT<sup>FNS</sup> (43)</span></span>
| <span data-ttu-id="92888-2399">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-2399">Target</span></span> | <span data-ttu-id="92888-2400">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-2400">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-2401">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-2401">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-2402">32</span><span class="sxs-lookup"><span data-stu-id="92888-2402">32</span></span> |
| <span data-ttu-id="92888-2403">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-2403">Format Support</span></span> | \- |
| <span data-ttu-id="92888-2404">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-2404">Buffer</span></span> | \- |
| <span data-ttu-id="92888-2405">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2405">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-2406">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2406">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-2407">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-2407">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-2408">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-2408">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-2409">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-2409">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-2410">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-2410">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-2411">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-2411">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-2412">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-2412">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-2413">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-2413">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-2414">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-2414">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-2415">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-2415">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-2416">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-2416">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-2417">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-2417">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-2418">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2418">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-2419">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2419">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-2420">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2420">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2421">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-2421">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2422">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-2422">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-2423">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-2423">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-2424">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-2424">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2425">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-2425">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2426">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-2426">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-2427">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2427">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-2428">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2428">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-2429">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2429">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-2430">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-2430">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-2431">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-2431">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-2432">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2432">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-2433">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-2433">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2434">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-2434">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2435">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-2435">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-2436">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2436">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2437">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-2437">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2438">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-2438">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-2439">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-2439">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-2440">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-2440">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-2441">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-2441">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-2442">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-2442">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-2443">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2443">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-2444">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2444">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-2445">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2445">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-2446">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-2446">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-2447">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-2447">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a><span data-ttu-id="92888-2448">DXGI_FORMAT_R24G8 \_ <sup>PCs</sup> não tipados (44)</span><span class="sxs-lookup"><span data-stu-id="92888-2448">DXGI_FORMAT_R24G8\_TYPELESS<sup>PCS</sup> (44)</span></span>
| <span data-ttu-id="92888-2449">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-2449">Target</span></span> | <span data-ttu-id="92888-2450">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-2450">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-2451">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-2451">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-2452">32</span><span class="sxs-lookup"><span data-stu-id="92888-2452">32</span></span> |
| <span data-ttu-id="92888-2453">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-2453">Format Support</span></span> | \- |
| <span data-ttu-id="92888-2454">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-2454">Buffer</span></span> | \- |
| <span data-ttu-id="92888-2455">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2455">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-2456">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2456">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-2457">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-2457">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-2458">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-2458">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-2459">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-2459">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-2460">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-2460">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-2461">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-2461">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-2462">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-2462">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-2463">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-2463">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-2464">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-2464">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-2465">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-2465">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-2466">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-2466">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-2467">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-2467">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-2468">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2468">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-2469">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2469">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-2470">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2470">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2471">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-2471">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2472">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-2472">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-2473">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-2473">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-2474">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-2474">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2475">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-2475">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2476">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-2476">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-2477">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2477">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-2478">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2478">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-2479">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2479">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-2480">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-2480">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-2481">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-2481">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-2482">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2482">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-2483">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-2483">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2484">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-2484">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2485">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-2485">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-2486">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2486">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2487">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-2487">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2488">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-2488">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-2489">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-2489">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-2490">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-2490">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-2491">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-2491">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-2492">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-2492">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-2493">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2493">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-2494">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2494">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-2495">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2495">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-2496">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-2496">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-2497">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-2497">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfnssup-45"></a><span data-ttu-id="92888-2498">DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT<sup>FNS</sup> (45)</span><span class="sxs-lookup"><span data-stu-id="92888-2498">DXGI_FORMAT_D24\_UNORM\_S8\_UINT<sup>FNS</sup> (45)</span></span>
| <span data-ttu-id="92888-2499">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-2499">Target</span></span> | <span data-ttu-id="92888-2500">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-2500">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-2501">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-2501">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-2502">32</span><span class="sxs-lookup"><span data-stu-id="92888-2502">32</span></span> |
| <span data-ttu-id="92888-2503">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-2503">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-2505">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-2505">Buffer</span></span> | \- |
| <span data-ttu-id="92888-2506">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2506">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-2507">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2507">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-2508">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-2508">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-2509">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-2509">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-2510">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-2510">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-2512">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-2512">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-2513">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-2513">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-2514">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-2514">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-2515">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-2515">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-2516">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-2516">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-2517">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-2517">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-2518">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-2518">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-2519">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-2519">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-2520">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2520">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-2521">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2521">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-2522">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2522">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2523">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-2523">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2524">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-2524">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-2525">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-2525">Depth/Stencil Target</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-2527">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-2527">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2528">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-2528">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2529">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-2529">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-2530">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2530">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-2531">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2531">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-2532">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2532">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-2533">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-2533">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-2534">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-2534">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-2535">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2535">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-2536">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-2536">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2537">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-2537">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2538">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-2538">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-2539">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2539">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-2541">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-2541">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-2543">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-2543">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-2545">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-2545">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-2546">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-2546">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-2547">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-2547">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-2548">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-2548">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-2549">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2549">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-2550">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2550">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-2551">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2551">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-2552">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-2552">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-2553">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-2553">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfnssup-46"></a><span data-ttu-id="92888-2554">FNS UNORM x8 tipo não-suDXGI_FORMAT_R24do \_ \_ \_ (46)<sup></sup></span><span class="sxs-lookup"><span data-stu-id="92888-2554">DXGI_FORMAT_R24\_UNORM\_X8\_TYPELESS<sup>FNS</sup> (46)</span></span>
| <span data-ttu-id="92888-2555">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-2555">Target</span></span> | <span data-ttu-id="92888-2556">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-2556">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-2557">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-2557">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-2558">32</span><span class="sxs-lookup"><span data-stu-id="92888-2558">32</span></span> |
| <span data-ttu-id="92888-2559">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-2559">Format Support</span></span> | \- |
| <span data-ttu-id="92888-2560">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-2560">Buffer</span></span> | \- |
| <span data-ttu-id="92888-2561">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2561">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-2562">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2562">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-2563">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-2563">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-2564">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-2564">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-2565">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-2565">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-2566">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-2566">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-2567">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-2567">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-2568">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-2568">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-2569">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-2569">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-2570">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-2570">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-2571">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-2571">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-2572">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-2572">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-2573">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-2573">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-2574">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2574">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-2575">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2575">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-2576">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2576">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2577">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-2577">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2578">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-2578">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-2579">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-2579">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-2580">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-2580">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2581">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-2581">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2582">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-2582">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-2583">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2583">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-2584">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2584">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-2585">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2585">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-2586">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-2586">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-2587">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-2587">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-2588">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2588">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-2589">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-2589">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2590">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-2590">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2591">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-2591">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-2592">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2592">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2593">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-2593">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2594">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-2594">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-2595">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-2595">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-2596">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-2596">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-2597">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-2597">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-2598">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-2598">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-2599">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2599">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-2600">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2600">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-2601">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2601">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-2602">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-2602">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-2603">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-2603">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfnssup-47"></a><span data-ttu-id="92888-2604">DXGI_FORMAT_X24 \_ \_ \_ <sup>FNS</sup> de G8 UINT não tipado (47)</span><span class="sxs-lookup"><span data-stu-id="92888-2604">DXGI_FORMAT_X24\_TYPELESS\_G8\_UINT<sup>FNS</sup> (47)</span></span>
| <span data-ttu-id="92888-2605">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-2605">Target</span></span> | <span data-ttu-id="92888-2606">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-2606">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-2607">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-2607">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-2608">32</span><span class="sxs-lookup"><span data-stu-id="92888-2608">32</span></span> |
| <span data-ttu-id="92888-2609">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-2609">Format Support</span></span> | \- |
| <span data-ttu-id="92888-2610">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-2610">Buffer</span></span> | \- |
| <span data-ttu-id="92888-2611">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2611">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-2612">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2612">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-2613">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-2613">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-2614">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-2614">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-2615">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-2615">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-2616">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-2616">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-2617">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-2617">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-2618">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-2618">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-2619">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-2619">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-2620">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-2620">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-2621">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-2621">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-2622">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-2622">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-2623">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-2623">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-2624">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2624">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-2625">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2625">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-2626">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2626">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2627">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-2627">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2628">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-2628">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-2629">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-2629">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-2630">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-2630">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2631">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-2631">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2632">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-2632">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-2633">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2633">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-2634">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2634">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-2635">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2635">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-2636">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-2636">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-2637">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-2637">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-2638">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2638">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-2639">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-2639">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2640">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-2640">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2641">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-2641">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-2642">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2642">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2643">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-2643">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2644">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-2644">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-2645">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-2645">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-2646">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-2646">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-2647">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-2647">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-2648">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-2648">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-2649">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2649">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-2650">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2650">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-2651">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2651">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-2652">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-2652">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-2653">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-2653">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="92888-2654">DXGI_FORMAT_R8G8 \_ <sup>PCs</sup> não tipados (48)</span><span class="sxs-lookup"><span data-stu-id="92888-2654">DXGI_FORMAT_R8G8\_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="92888-2655">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-2655">Target</span></span> | <span data-ttu-id="92888-2656">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-2656">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-2657">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-2657">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-2658">16</span><span class="sxs-lookup"><span data-stu-id="92888-2658">16</span></span> |
| <span data-ttu-id="92888-2659">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-2659">Format Support</span></span> | \- |
| <span data-ttu-id="92888-2660">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-2660">Buffer</span></span> | \- |
| <span data-ttu-id="92888-2661">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2661">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-2662">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2662">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-2663">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-2663">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-2664">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-2664">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-2665">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-2665">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-2666">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-2666">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-2667">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-2667">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-2668">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-2668">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-2669">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-2669">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-2670">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-2670">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-2671">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-2671">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-2672">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-2672">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-2673">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-2673">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-2674">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2674">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-2675">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2675">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-2676">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2676">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2677">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-2677">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2678">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-2678">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-2679">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-2679">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-2680">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-2680">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2681">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-2681">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2682">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-2682">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-2683">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2683">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-2684">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2684">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-2685">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2685">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-2686">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-2686">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-2687">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-2687">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-2688">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2688">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-2689">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-2689">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2690">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-2690">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2691">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-2691">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-2692">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2692">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2693">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-2693">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2694">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-2694">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-2695">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-2695">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-2696">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-2696">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-2697">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-2697">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-2698">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-2698">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-2699">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2699">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-2700">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2700">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-2701">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2701">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-2702">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-2702">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-2703">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-2703">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_unormsupfnssup-49"></a><span data-ttu-id="92888-2704">DXGI_FORMAT_R8G8 \_ UNORM<sup>FNS</sup> (49)</span><span class="sxs-lookup"><span data-stu-id="92888-2704">DXGI_FORMAT_R8G8\_UNORM<sup>FNS</sup> (49)</span></span>
| <span data-ttu-id="92888-2705">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-2705">Target</span></span> | <span data-ttu-id="92888-2706">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-2706">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-2707">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-2707">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-2708">16</span><span class="sxs-lookup"><span data-stu-id="92888-2708">16</span></span> |
| <span data-ttu-id="92888-2709">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-2709">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-2711">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-2711">Buffer</span></span> | \- |
| <span data-ttu-id="92888-2712">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2712">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-2713">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2713">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-2714">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-2714">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-2715">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-2715">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-2716">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-2716">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-2718">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-2718">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-2719">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-2719">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-2720">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-2720">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-2722">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-2722">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-2724">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-2724">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-2725">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-2725">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-2726">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-2726">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-2727">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-2727">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-2728">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2728">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-2729">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2729">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-2730">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2730">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-2732">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-2732">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-2734">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-2734">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-2735">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-2735">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-2736">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-2736">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2737">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-2737">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2738">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-2738">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-2739">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2739">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-2740">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2740">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-2741">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2741">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-2742">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-2742">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-2743">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-2743">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-2744">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2744">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-2745">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-2745">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2746">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-2746">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2747">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-2747">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-2749">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2749">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2750">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-2750">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2751">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-2751">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-2752">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-2752">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-2753">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-2753">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-2754">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-2754">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-2755">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-2755">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-2756">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2756">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-2757">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2757">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-2758">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2758">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-2759">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-2759">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-2761">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-2761">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_uintsupfnssup-50"></a><span data-ttu-id="92888-2762">DXGI_FORMAT_R8G8 \_ uint<sup>FNS</sup> (50)</span><span class="sxs-lookup"><span data-stu-id="92888-2762">DXGI_FORMAT_R8G8\_UINT<sup>FNS</sup> (50)</span></span>
| <span data-ttu-id="92888-2763">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-2763">Target</span></span> | <span data-ttu-id="92888-2764">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-2764">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-2765">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-2765">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-2766">16</span><span class="sxs-lookup"><span data-stu-id="92888-2766">16</span></span> |
| <span data-ttu-id="92888-2767">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-2767">Format Support</span></span> | \- |
| <span data-ttu-id="92888-2768">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-2768">Buffer</span></span> | \- |
| <span data-ttu-id="92888-2769">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2769">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-2770">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2770">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-2771">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-2771">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-2772">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-2772">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-2773">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-2773">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-2774">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-2774">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-2775">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-2775">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-2776">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-2776">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-2777">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-2777">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-2778">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-2778">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-2779">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-2779">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-2780">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-2780">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-2781">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-2781">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-2782">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2782">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-2783">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2783">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-2784">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2784">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2785">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-2785">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2786">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-2786">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-2787">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-2787">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-2788">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-2788">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2789">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-2789">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2790">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-2790">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-2791">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2791">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-2792">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2792">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-2793">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2793">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-2794">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-2794">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-2795">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-2795">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-2796">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2796">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-2797">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-2797">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2798">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-2798">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2799">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-2799">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-2800">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2800">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2801">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-2801">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2802">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-2802">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-2803">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-2803">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-2804">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-2804">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-2805">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-2805">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-2806">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-2806">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-2807">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2807">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-2808">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2808">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-2809">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2809">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-2810">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-2810">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-2811">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-2811">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_snormsupfnssup-51"></a><span data-ttu-id="92888-2812">DXGI_FORMAT_R8G8 \_ SNORM<sup>FNS</sup> (51)</span><span class="sxs-lookup"><span data-stu-id="92888-2812">DXGI_FORMAT_R8G8\_SNORM<sup>FNS</sup> (51)</span></span>
| <span data-ttu-id="92888-2813">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-2813">Target</span></span> | <span data-ttu-id="92888-2814">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-2814">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-2815">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-2815">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-2816">16</span><span class="sxs-lookup"><span data-stu-id="92888-2816">16</span></span> |
| <span data-ttu-id="92888-2817">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-2817">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-2819">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-2819">Buffer</span></span> | \- |
| <span data-ttu-id="92888-2820">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2820">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-2821">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2821">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-2822">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-2822">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-2823">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-2823">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-2824">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-2824">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-2826">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-2826">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-2827">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-2827">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-2828">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-2828">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-2830">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-2830">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-2832">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-2832">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-2833">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-2833">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-2834">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-2834">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-2835">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-2835">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-2836">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2836">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-2838">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2838">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-2839">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2839">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2840">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-2840">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2841">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-2841">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-2842">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-2842">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-2843">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-2843">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2844">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-2844">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2845">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-2845">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-2846">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2846">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-2847">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2847">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-2848">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2848">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-2849">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-2849">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-2850">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-2850">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-2851">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2851">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-2852">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-2852">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2853">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-2853">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2854">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-2854">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-2856">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2856">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2857">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-2857">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2858">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-2858">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-2859">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-2859">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-2860">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-2860">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-2861">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-2861">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-2862">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-2862">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-2863">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2863">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-2864">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2864">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-2865">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2865">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-2866">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-2866">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-2867">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-2867">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_sintsupfnssup-52"></a><span data-ttu-id="92888-2868">DXGI_FORMAT_R8G8 \_ Santo<sup>FNS</sup> (52)</span><span class="sxs-lookup"><span data-stu-id="92888-2868">DXGI_FORMAT_R8G8\_SINT<sup>FNS</sup> (52)</span></span>
| <span data-ttu-id="92888-2869">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-2869">Target</span></span> | <span data-ttu-id="92888-2870">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-2870">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-2871">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-2871">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-2872">16</span><span class="sxs-lookup"><span data-stu-id="92888-2872">16</span></span> |
| <span data-ttu-id="92888-2873">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-2873">Format Support</span></span> | \- |
| <span data-ttu-id="92888-2874">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-2874">Buffer</span></span> | \- |
| <span data-ttu-id="92888-2875">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2875">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-2876">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2876">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-2877">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-2877">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-2878">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-2878">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-2879">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-2879">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-2880">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-2880">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-2881">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-2881">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-2882">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-2882">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-2883">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-2883">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-2884">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-2884">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-2885">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-2885">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-2886">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-2886">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-2887">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-2887">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-2888">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2888">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-2889">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2889">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-2890">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2890">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2891">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-2891">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2892">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-2892">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-2893">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-2893">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-2894">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-2894">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2895">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-2895">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2896">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-2896">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-2897">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2897">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-2898">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2898">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-2899">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2899">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-2900">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-2900">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-2901">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-2901">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-2902">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2902">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-2903">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-2903">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2904">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-2904">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2905">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-2905">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-2906">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2906">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2907">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-2907">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2908">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-2908">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-2909">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-2909">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-2910">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-2910">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-2911">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-2911">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-2912">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-2912">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-2913">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2913">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-2914">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2914">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-2915">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2915">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-2916">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-2916">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-2917">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-2917">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="92888-2918">DXGI_FORMAT_R16 \_ <sup>PCs</sup> não tipados (53)</span><span class="sxs-lookup"><span data-stu-id="92888-2918">DXGI_FORMAT_R16\_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="92888-2919">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-2919">Target</span></span> | <span data-ttu-id="92888-2920">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-2920">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-2921">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-2921">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-2922">16</span><span class="sxs-lookup"><span data-stu-id="92888-2922">16</span></span> |
| <span data-ttu-id="92888-2923">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-2923">Format Support</span></span> | \- |
| <span data-ttu-id="92888-2924">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-2924">Buffer</span></span> | \- |
| <span data-ttu-id="92888-2925">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2925">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-2926">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2926">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-2927">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-2927">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-2928">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-2928">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-2929">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-2929">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-2930">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-2930">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-2931">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-2931">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-2932">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-2932">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-2933">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-2933">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-2934">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-2934">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-2935">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-2935">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-2936">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-2936">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-2937">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-2937">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-2938">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2938">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-2939">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2939">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-2940">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2940">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2941">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-2941">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2942">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-2942">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-2943">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-2943">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-2944">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-2944">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2945">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-2945">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2946">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-2946">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-2947">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2947">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-2948">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2948">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-2949">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2949">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-2950">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-2950">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-2951">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-2951">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-2952">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2952">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-2953">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-2953">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2954">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-2954">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-2955">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-2955">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-2956">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2956">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2957">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-2957">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2958">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-2958">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-2959">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-2959">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-2960">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-2960">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-2961">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-2961">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-2962">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-2962">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-2963">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2963">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-2964">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2964">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-2965">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-2965">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-2966">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-2966">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-2967">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-2967">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_floatsupfnssup-54"></a><span data-ttu-id="92888-2968">DXGI_FORMAT_R16 \_ float<sup>FNS</sup> (54)</span><span class="sxs-lookup"><span data-stu-id="92888-2968">DXGI_FORMAT_R16\_FLOAT<sup>FNS</sup> (54)</span></span>
| <span data-ttu-id="92888-2969">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-2969">Target</span></span> | <span data-ttu-id="92888-2970">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-2970">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-2971">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-2971">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-2972">16</span><span class="sxs-lookup"><span data-stu-id="92888-2972">16</span></span> |
| <span data-ttu-id="92888-2973">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-2973">Format Support</span></span> | \- |
| <span data-ttu-id="92888-2974">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-2974">Buffer</span></span> | \- |
| <span data-ttu-id="92888-2975">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2975">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-2976">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-2976">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-2977">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-2977">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-2978">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-2978">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-2979">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-2979">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-2980">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-2980">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-2981">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-2981">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-2982">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-2982">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-2983">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-2983">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-2984">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-2984">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-2985">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-2985">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-2986">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-2986">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-2987">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-2987">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-2988">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2988">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-2989">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-2989">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-2990">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-2990">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2991">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-2991">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-2992">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-2992">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-2993">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-2993">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-2994">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-2994">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2995">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-2995">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-2996">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-2996">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-2997">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2997">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-2998">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2998">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-2999">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-2999">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-3000">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-3000">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-3001">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-3001">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-3002">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3002">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-3003">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-3003">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3004">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-3004">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3005">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-3005">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-3006">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3006">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3007">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-3007">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3008">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-3008">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-3009">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-3009">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-3010">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-3010">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-3011">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-3011">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-3012">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-3012">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-3013">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3013">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-3014">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3014">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-3015">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3015">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-3016">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-3016">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-3017">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-3017">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d16_unormsupfnssup-55"></a><span data-ttu-id="92888-3018">DXGI_FORMAT_D16 \_ UNORM<sup>FNS</sup> (55)</span><span class="sxs-lookup"><span data-stu-id="92888-3018">DXGI_FORMAT_D16\_UNORM<sup>FNS</sup> (55)</span></span>
| <span data-ttu-id="92888-3019">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-3019">Target</span></span> | <span data-ttu-id="92888-3020">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-3020">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-3021">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-3021">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-3022">16</span><span class="sxs-lookup"><span data-stu-id="92888-3022">16</span></span> |
| <span data-ttu-id="92888-3023">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-3023">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3025">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-3025">Buffer</span></span> | \- |
| <span data-ttu-id="92888-3026">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3026">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-3027">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3027">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-3028">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-3028">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-3029">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-3029">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-3030">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-3030">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3032">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-3032">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-3033">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-3033">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-3034">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-3034">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-3035">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-3035">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-3036">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-3036">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-3037">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-3037">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-3038">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-3038">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-3039">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-3039">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-3040">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3040">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-3041">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3041">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-3042">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3042">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3043">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-3043">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3044">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-3044">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-3045">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-3045">Depth/Stencil Target</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3047">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-3047">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3048">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-3048">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3049">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-3049">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-3050">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3050">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-3051">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3051">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-3052">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3052">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-3053">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-3053">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-3054">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-3054">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-3055">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3055">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-3056">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-3056">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3057">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-3057">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3058">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-3058">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-3059">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3059">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-3061">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-3061">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-3063">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-3063">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-3065">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-3065">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-3066">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-3066">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-3067">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-3067">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-3068">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-3068">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-3069">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3069">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-3070">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3070">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-3071">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3071">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-3072">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-3072">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-3073">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-3073">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_unormsupfnssup-56"></a><span data-ttu-id="92888-3074">DXGI_FORMAT_R16 \_ UNORM<sup>FNS</sup> (56)</span><span class="sxs-lookup"><span data-stu-id="92888-3074">DXGI_FORMAT_R16\_UNORM<sup>FNS</sup> (56)</span></span>
| <span data-ttu-id="92888-3075">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-3075">Target</span></span> | <span data-ttu-id="92888-3076">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-3076">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-3077">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-3077">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-3078">16</span><span class="sxs-lookup"><span data-stu-id="92888-3078">16</span></span> |
| <span data-ttu-id="92888-3079">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-3079">Format Support</span></span> | \- |
| <span data-ttu-id="92888-3080">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-3080">Buffer</span></span> | \- |
| <span data-ttu-id="92888-3081">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3081">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-3082">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3082">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-3083">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-3083">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-3084">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-3084">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-3085">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-3085">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-3086">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-3086">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-3087">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-3087">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-3088">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-3088">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-3089">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-3089">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-3090">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-3090">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-3091">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-3091">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-3092">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-3092">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-3093">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-3093">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-3094">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3094">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-3095">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3095">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-3096">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3096">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3097">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-3097">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3098">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-3098">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-3099">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-3099">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-3100">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-3100">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3101">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-3101">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3102">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-3102">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-3103">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3103">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-3104">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3104">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-3105">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3105">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-3106">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-3106">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-3107">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-3107">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-3108">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3108">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-3109">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-3109">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3110">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-3110">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3111">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-3111">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-3112">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3112">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3113">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-3113">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3114">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-3114">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-3115">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-3115">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-3116">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-3116">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-3117">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-3117">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-3118">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-3118">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-3119">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3119">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-3120">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3120">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-3121">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3121">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-3122">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-3122">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-3123">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-3123">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_uintsupfnssup-57"></a><span data-ttu-id="92888-3124">DXGI_FORMAT_R16 \_ uint<sup>FNS</sup> (57)</span><span class="sxs-lookup"><span data-stu-id="92888-3124">DXGI_FORMAT_R16\_UINT<sup>FNS</sup> (57)</span></span>
| <span data-ttu-id="92888-3125">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-3125">Target</span></span> | <span data-ttu-id="92888-3126">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-3126">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-3127">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-3127">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-3128">16</span><span class="sxs-lookup"><span data-stu-id="92888-3128">16</span></span> |
| <span data-ttu-id="92888-3129">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-3129">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3131">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-3131">Buffer</span></span> | \- |
| <span data-ttu-id="92888-3132">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3132">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-3133">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3133">Input Assembler Index Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3135">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-3135">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-3136">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-3136">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-3137">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-3137">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-3138">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-3138">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-3139">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-3139">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-3140">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-3140">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-3141">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-3141">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-3142">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-3142">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-3143">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-3143">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-3144">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-3144">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-3145">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-3145">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-3146">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3146">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-3147">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3147">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-3148">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3148">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3149">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-3149">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3150">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-3150">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-3151">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-3151">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-3152">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-3152">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3153">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-3153">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3154">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-3154">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-3155">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3155">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-3156">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3156">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-3157">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3157">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-3158">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-3158">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-3159">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-3159">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-3160">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3160">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-3161">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-3161">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3162">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-3162">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3163">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-3163">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-3164">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3164">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3165">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-3165">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3166">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-3166">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-3167">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-3167">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-3168">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-3168">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-3169">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-3169">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-3170">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-3170">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-3171">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3171">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-3172">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3172">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-3173">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3173">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-3174">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-3174">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-3175">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-3175">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_snormsupfnssup-58"></a><span data-ttu-id="92888-3176">DXGI_FORMAT_R16 \_ SNORM<sup>FNS</sup> (58)</span><span class="sxs-lookup"><span data-stu-id="92888-3176">DXGI_FORMAT_R16\_SNORM<sup>FNS</sup> (58)</span></span>
| <span data-ttu-id="92888-3177">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-3177">Target</span></span> | <span data-ttu-id="92888-3178">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-3178">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-3179">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-3179">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-3180">16</span><span class="sxs-lookup"><span data-stu-id="92888-3180">16</span></span> |
| <span data-ttu-id="92888-3181">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-3181">Format Support</span></span> | \- |
| <span data-ttu-id="92888-3182">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-3182">Buffer</span></span> | \- |
| <span data-ttu-id="92888-3183">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3183">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-3184">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3184">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-3185">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-3185">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-3186">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-3186">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-3187">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-3187">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-3188">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-3188">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-3189">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-3189">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-3190">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-3190">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-3191">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-3191">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-3192">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-3192">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-3193">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-3193">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-3194">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-3194">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-3195">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-3195">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-3196">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3196">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-3197">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3197">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-3198">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3198">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3199">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-3199">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3200">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-3200">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-3201">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-3201">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-3202">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-3202">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3203">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-3203">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3204">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-3204">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-3205">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3205">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-3206">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3206">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-3207">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3207">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-3208">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-3208">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-3209">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-3209">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-3210">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3210">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-3211">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-3211">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3212">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-3212">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3213">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-3213">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-3214">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3214">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3215">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-3215">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3216">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-3216">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-3217">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-3217">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-3218">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-3218">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-3219">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-3219">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-3220">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-3220">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-3221">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3221">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-3222">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3222">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-3223">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3223">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-3224">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-3224">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-3225">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-3225">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_sintsupfnssup-59"></a><span data-ttu-id="92888-3226">DXGI_FORMAT_R16 \_ Santo<sup>FNS</sup> (59)</span><span class="sxs-lookup"><span data-stu-id="92888-3226">DXGI_FORMAT_R16\_SINT<sup>FNS</sup> (59)</span></span>
| <span data-ttu-id="92888-3227">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-3227">Target</span></span> | <span data-ttu-id="92888-3228">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-3228">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-3229">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-3229">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-3230">16</span><span class="sxs-lookup"><span data-stu-id="92888-3230">16</span></span> |
| <span data-ttu-id="92888-3231">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-3231">Format Support</span></span> | \- |
| <span data-ttu-id="92888-3232">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-3232">Buffer</span></span> | \- |
| <span data-ttu-id="92888-3233">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3233">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-3234">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3234">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-3235">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-3235">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-3236">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-3236">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-3237">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-3237">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-3238">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-3238">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-3239">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-3239">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-3240">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-3240">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-3241">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-3241">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-3242">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-3242">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-3243">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-3243">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-3244">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-3244">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-3245">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-3245">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-3246">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3246">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-3247">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3247">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-3248">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3248">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3249">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-3249">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3250">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-3250">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-3251">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-3251">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-3252">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-3252">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3253">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-3253">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3254">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-3254">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-3255">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3255">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-3256">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3256">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-3257">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3257">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-3258">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-3258">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-3259">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-3259">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-3260">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3260">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-3261">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-3261">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3262">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-3262">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3263">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-3263">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-3264">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3264">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3265">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-3265">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3266">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-3266">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-3267">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-3267">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-3268">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-3268">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-3269">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-3269">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-3270">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-3270">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-3271">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3271">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-3272">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3272">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-3273">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3273">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-3274">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-3274">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-3275">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-3275">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="92888-3276">DXGI_FORMAT_R8 \_ <sup>PCs</sup> não tipados (60)</span><span class="sxs-lookup"><span data-stu-id="92888-3276">DXGI_FORMAT_R8\_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="92888-3277">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-3277">Target</span></span> | <span data-ttu-id="92888-3278">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-3278">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-3279">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-3279">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-3280">8</span><span class="sxs-lookup"><span data-stu-id="92888-3280">8</span></span> |
| <span data-ttu-id="92888-3281">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-3281">Format Support</span></span> | \- |
| <span data-ttu-id="92888-3282">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-3282">Buffer</span></span> | \- |
| <span data-ttu-id="92888-3283">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3283">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-3284">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3284">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-3285">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-3285">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-3286">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-3286">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-3287">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-3287">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-3288">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-3288">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-3289">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-3289">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-3290">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-3290">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-3291">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-3291">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-3292">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-3292">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-3293">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-3293">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-3294">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-3294">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-3295">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-3295">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-3296">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3296">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-3297">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3297">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-3298">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3298">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3299">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-3299">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3300">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-3300">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-3301">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-3301">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-3302">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-3302">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3303">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-3303">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3304">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-3304">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-3305">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3305">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-3306">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3306">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-3307">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3307">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-3308">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-3308">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-3309">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-3309">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-3310">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3310">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-3311">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-3311">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3312">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-3312">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3313">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-3313">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-3314">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3314">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3315">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-3315">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3316">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-3316">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-3317">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-3317">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-3318">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-3318">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-3319">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-3319">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-3320">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-3320">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-3321">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3321">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-3322">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3322">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-3323">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3323">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-3324">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-3324">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-3325">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-3325">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_unormsupfnssup-61"></a><span data-ttu-id="92888-3326">DXGI_FORMAT_R8 \_ UNORM<sup>FNS</sup> (61)</span><span class="sxs-lookup"><span data-stu-id="92888-3326">DXGI_FORMAT_R8\_UNORM<sup>FNS</sup> (61)</span></span>
| <span data-ttu-id="92888-3327">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-3327">Target</span></span> | <span data-ttu-id="92888-3328">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-3328">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-3329">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-3329">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-3330">8</span><span class="sxs-lookup"><span data-stu-id="92888-3330">8</span></span> |
| <span data-ttu-id="92888-3331">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-3331">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3333">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-3333">Buffer</span></span> | \- |
| <span data-ttu-id="92888-3334">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3334">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-3335">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3335">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-3336">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-3336">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-3337">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-3337">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-3338">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-3338">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3340">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-3340">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3342">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-3342">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3344">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-3344">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3346">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-3346">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3348">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-3348">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-3349">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-3349">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-3350">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-3350">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-3351">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-3351">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-3352">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3352">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3354">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3354">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-3355">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3355">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3357">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-3357">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3359">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-3359">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-3360">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-3360">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-3361">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-3361">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3362">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-3362">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3363">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-3363">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-3364">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3364">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-3365">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3365">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-3366">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3366">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-3367">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-3367">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-3368">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-3368">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-3369">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3369">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-3370">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-3370">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3371">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-3371">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3372">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-3372">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3374">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3374">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3375">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-3375">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3376">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-3376">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-3377">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-3377">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-3378">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-3378">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-3379">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-3379">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-3380">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-3380">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-3381">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3381">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-3382">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3382">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-3383">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3383">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-3384">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-3384">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3386">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-3386">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_uintsupfnssup-62"></a><span data-ttu-id="92888-3387">DXGI_FORMAT_R8 \_ uint<sup>FNS</sup> (62)</span><span class="sxs-lookup"><span data-stu-id="92888-3387">DXGI_FORMAT_R8\_UINT<sup>FNS</sup> (62)</span></span>
| <span data-ttu-id="92888-3388">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-3388">Target</span></span> | <span data-ttu-id="92888-3389">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-3389">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-3390">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-3390">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-3391">8</span><span class="sxs-lookup"><span data-stu-id="92888-3391">8</span></span> |
| <span data-ttu-id="92888-3392">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-3392">Format Support</span></span> | \- |
| <span data-ttu-id="92888-3393">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-3393">Buffer</span></span> | \- |
| <span data-ttu-id="92888-3394">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3394">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-3395">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3395">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-3396">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-3396">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-3397">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-3397">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-3398">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-3398">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-3399">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-3399">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-3400">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-3400">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-3401">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-3401">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-3402">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-3402">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-3403">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-3403">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-3404">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-3404">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-3405">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-3405">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-3406">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-3406">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-3407">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3407">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-3408">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3408">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-3409">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3409">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3410">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-3410">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3411">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-3411">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-3412">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-3412">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-3413">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-3413">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3414">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-3414">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3415">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-3415">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-3416">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3416">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-3417">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3417">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-3418">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3418">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-3419">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-3419">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-3420">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-3420">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-3421">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3421">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-3422">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-3422">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3423">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-3423">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3424">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-3424">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-3425">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3425">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3426">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-3426">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3427">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-3427">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-3428">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-3428">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-3429">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-3429">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-3430">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-3430">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-3431">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-3431">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-3432">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3432">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-3433">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3433">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-3434">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3434">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-3435">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-3435">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-3436">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-3436">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_snormsupfnssup-63"></a><span data-ttu-id="92888-3437">DXGI_FORMAT_R8 \_ SNORM<sup>FNS</sup> (63)</span><span class="sxs-lookup"><span data-stu-id="92888-3437">DXGI_FORMAT_R8\_SNORM<sup>FNS</sup> (63)</span></span>
| <span data-ttu-id="92888-3438">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-3438">Target</span></span> | <span data-ttu-id="92888-3439">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-3439">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-3440">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-3440">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-3441">8</span><span class="sxs-lookup"><span data-stu-id="92888-3441">8</span></span> |
| <span data-ttu-id="92888-3442">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-3442">Format Support</span></span> | \- |
| <span data-ttu-id="92888-3443">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-3443">Buffer</span></span> | \- |
| <span data-ttu-id="92888-3444">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3444">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-3445">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3445">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-3446">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-3446">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-3447">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-3447">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-3448">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-3448">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-3449">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-3449">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-3450">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-3450">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-3451">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-3451">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-3452">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-3452">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-3453">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-3453">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-3454">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-3454">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-3455">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-3455">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-3456">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-3456">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-3457">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3457">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-3458">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3458">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-3459">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3459">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3460">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-3460">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3461">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-3461">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-3462">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-3462">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-3463">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-3463">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3464">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-3464">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3465">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-3465">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-3466">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3466">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-3467">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3467">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-3468">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3468">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-3469">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-3469">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-3470">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-3470">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-3471">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3471">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-3472">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-3472">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3473">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-3473">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3474">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-3474">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-3475">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3475">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3476">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-3476">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3477">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-3477">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-3478">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-3478">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-3479">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-3479">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-3480">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-3480">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-3481">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-3481">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-3482">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3482">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-3483">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3483">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-3484">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3484">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-3485">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-3485">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-3486">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-3486">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_sintsupfnssup-64"></a><span data-ttu-id="92888-3487">DXGI_FORMAT_R8 \_ Santo<sup>FNS</sup> (64)</span><span class="sxs-lookup"><span data-stu-id="92888-3487">DXGI_FORMAT_R8\_SINT<sup>FNS</sup> (64)</span></span>
| <span data-ttu-id="92888-3488">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-3488">Target</span></span> | <span data-ttu-id="92888-3489">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-3489">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-3490">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-3490">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-3491">8</span><span class="sxs-lookup"><span data-stu-id="92888-3491">8</span></span> |
| <span data-ttu-id="92888-3492">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-3492">Format Support</span></span> | \- |
| <span data-ttu-id="92888-3493">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-3493">Buffer</span></span> | \- |
| <span data-ttu-id="92888-3494">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3494">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-3495">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3495">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-3496">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-3496">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-3497">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-3497">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-3498">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-3498">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-3499">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-3499">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-3500">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-3500">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-3501">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-3501">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-3502">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-3502">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-3503">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-3503">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-3504">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-3504">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-3505">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-3505">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-3506">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-3506">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-3507">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3507">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-3508">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3508">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-3509">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3509">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3510">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-3510">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3511">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-3511">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-3512">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-3512">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-3513">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-3513">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3514">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-3514">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3515">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-3515">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-3516">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3516">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-3517">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3517">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-3518">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3518">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-3519">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-3519">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-3520">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-3520">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-3521">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3521">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-3522">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-3522">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3523">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-3523">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3524">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-3524">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-3525">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3525">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3526">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-3526">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3527">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-3527">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-3528">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-3528">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-3529">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-3529">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-3530">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-3530">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-3531">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-3531">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-3532">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3532">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-3533">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3533">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-3534">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3534">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-3535">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-3535">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-3536">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-3536">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="92888-3537">DXGI_FORMAT_A8 \_ UNORM<sup>FNS</sup> (65)</span><span class="sxs-lookup"><span data-stu-id="92888-3537">DXGI_FORMAT_A8\_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="92888-3538">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-3538">Target</span></span> | <span data-ttu-id="92888-3539">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-3539">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-3540">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-3540">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-3541">8</span><span class="sxs-lookup"><span data-stu-id="92888-3541">8</span></span> |
| <span data-ttu-id="92888-3542">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-3542">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3544">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-3544">Buffer</span></span> | \- |
| <span data-ttu-id="92888-3545">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3545">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-3546">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3546">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-3547">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-3547">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-3548">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-3548">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-3549">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-3549">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3551">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-3551">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-3552">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-3552">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-3553">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-3553">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3555">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-3555">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3557">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-3557">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-3558">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-3558">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-3559">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-3559">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-3560">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-3560">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-3561">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3561">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-3562">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3562">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-3563">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3563">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3565">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-3565">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3567">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-3567">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-3568">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-3568">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-3569">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-3569">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3570">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-3570">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3571">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-3571">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-3572">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3572">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-3573">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3573">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-3574">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3574">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-3575">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-3575">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-3576">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-3576">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-3577">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3577">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-3578">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-3578">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3579">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-3579">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3580">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-3580">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3582">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3582">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3583">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-3583">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3584">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-3584">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-3585">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-3585">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-3586">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-3586">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-3587">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-3587">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-3588">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-3588">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-3589">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3589">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-3590">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3590">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-3591">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3591">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-3592">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-3592">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3594">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-3594">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="92888-3595">DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67)</span><span class="sxs-lookup"><span data-stu-id="92888-3595">DXGI_FORMAT_R9G9B9E5\_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="92888-3596">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-3596">Target</span></span> | <span data-ttu-id="92888-3597">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-3597">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-3598">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-3598">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-3599">32</span><span class="sxs-lookup"><span data-stu-id="92888-3599">32</span></span> |
| <span data-ttu-id="92888-3600">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-3600">Format Support</span></span> | \- |
| <span data-ttu-id="92888-3601">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-3601">Buffer</span></span> | \- |
| <span data-ttu-id="92888-3602">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3602">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-3603">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3603">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-3604">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-3604">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-3605">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-3605">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-3606">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-3606">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-3607">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-3607">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-3608">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-3608">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-3609">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-3609">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-3610">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-3610">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-3611">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-3611">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-3612">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-3612">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-3613">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-3613">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-3614">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-3614">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-3615">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3615">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-3616">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3616">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-3617">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3617">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3618">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-3618">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3619">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-3619">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-3620">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-3620">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-3621">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-3621">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3622">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-3622">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3623">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-3623">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-3624">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3624">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-3625">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3625">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-3626">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3626">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-3627">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-3627">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-3628">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-3628">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-3629">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3629">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-3630">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-3630">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3631">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-3631">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3632">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-3632">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-3633">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3633">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3634">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-3634">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3635">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-3635">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-3636">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-3636">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-3637">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-3637">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-3638">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-3638">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-3639">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-3639">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-3640">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3640">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-3641">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3641">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-3642">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3642">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-3643">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-3643">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-3644">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-3644">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="92888-3645">DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68)</span><span class="sxs-lookup"><span data-stu-id="92888-3645">DXGI_FORMAT_R8G8\_B8G8\_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="92888-3646">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-3646">Target</span></span> | <span data-ttu-id="92888-3647">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-3647">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-3648">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-3648">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-3649">16</span><span class="sxs-lookup"><span data-stu-id="92888-3649">16</span></span> |
| <span data-ttu-id="92888-3650">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-3650">Format Support</span></span> | \- |
| <span data-ttu-id="92888-3651">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-3651">Buffer</span></span> | \- |
| <span data-ttu-id="92888-3652">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3652">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-3653">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3653">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-3654">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-3654">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-3655">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-3655">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-3656">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-3656">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-3657">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-3657">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-3658">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-3658">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-3659">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-3659">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-3660">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-3660">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-3661">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-3661">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-3662">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-3662">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-3663">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-3663">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-3664">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-3664">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-3665">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3665">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-3666">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3666">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-3667">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3667">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3668">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-3668">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3669">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-3669">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-3670">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-3670">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-3671">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-3671">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3672">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-3672">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3673">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-3673">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-3674">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3674">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-3675">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3675">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-3676">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3676">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-3677">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-3677">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-3678">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-3678">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-3679">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3679">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-3680">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-3680">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3681">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-3681">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3682">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-3682">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-3683">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3683">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3684">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-3684">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3685">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-3685">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-3686">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-3686">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-3687">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-3687">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-3688">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-3688">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-3689">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-3689">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-3690">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3690">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-3691">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3691">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-3692">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3692">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-3693">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-3693">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-3694">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-3694">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="92888-3695">DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>FNC</sup> (69)</span><span class="sxs-lookup"><span data-stu-id="92888-3695">DXGI_FORMAT_G8R8\_G8B8\_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="92888-3696">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-3696">Target</span></span> | <span data-ttu-id="92888-3697">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-3697">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-3698">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-3698">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-3699">16</span><span class="sxs-lookup"><span data-stu-id="92888-3699">16</span></span> |
| <span data-ttu-id="92888-3700">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-3700">Format Support</span></span> | \- |
| <span data-ttu-id="92888-3701">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-3701">Buffer</span></span> | \- |
| <span data-ttu-id="92888-3702">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3702">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-3703">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3703">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-3704">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-3704">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-3705">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-3705">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-3706">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-3706">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-3707">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-3707">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-3708">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-3708">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-3709">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-3709">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-3710">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-3710">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-3711">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-3711">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-3712">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-3712">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-3713">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-3713">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-3714">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-3714">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-3715">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3715">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-3716">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3716">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-3717">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3717">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3718">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-3718">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3719">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-3719">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-3720">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-3720">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-3721">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-3721">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3722">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-3722">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3723">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-3723">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-3724">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3724">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-3725">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3725">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-3726">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3726">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-3727">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-3727">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-3728">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-3728">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-3729">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3729">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-3730">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-3730">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3731">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-3731">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3732">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-3732">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-3733">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3733">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3734">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-3734">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3735">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-3735">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-3736">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-3736">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-3737">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-3737">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-3738">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-3738">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-3739">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-3739">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-3740">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3740">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-3741">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3741">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-3742">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3742">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-3743">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-3743">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-3744">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-3744">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="92888-3745">DXGI_FORMAT_BC1 \_ <sup>PCC</sup> de tipo (70)</span><span class="sxs-lookup"><span data-stu-id="92888-3745">DXGI_FORMAT_BC1\_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="92888-3746">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-3746">Target</span></span> | <span data-ttu-id="92888-3747">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-3747">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-3748">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-3748">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-3749">4</span><span class="sxs-lookup"><span data-stu-id="92888-3749">4</span></span> |
| <span data-ttu-id="92888-3750">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-3750">Format Support</span></span> | \- |
| <span data-ttu-id="92888-3751">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-3751">Buffer</span></span> | \- |
| <span data-ttu-id="92888-3752">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3752">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-3753">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3753">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-3754">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-3754">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-3755">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-3755">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-3756">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-3756">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-3757">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-3757">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-3758">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-3758">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-3759">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-3759">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-3760">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-3760">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-3761">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-3761">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-3762">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-3762">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-3763">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-3763">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-3764">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-3764">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-3765">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3765">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-3766">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3766">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-3767">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3767">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3768">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-3768">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3769">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-3769">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-3770">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-3770">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-3771">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-3771">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3772">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-3772">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3773">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-3773">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-3774">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3774">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-3775">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3775">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-3776">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3776">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-3777">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-3777">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-3778">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-3778">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-3779">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3779">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-3780">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-3780">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3781">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-3781">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3782">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-3782">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-3783">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3783">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3784">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-3784">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3785">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-3785">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-3786">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-3786">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-3787">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-3787">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-3788">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-3788">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-3789">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-3789">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-3790">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3790">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-3791">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3791">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-3792">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3792">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-3793">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-3793">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-3794">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-3794">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unormsupfncsup-71"></a><span data-ttu-id="92888-3795">DXGI_FORMAT_BC1 \_ UNORM<sup>FNC</sup> (71)</span><span class="sxs-lookup"><span data-stu-id="92888-3795">DXGI_FORMAT_BC1\_UNORM<sup>FNC</sup> (71)</span></span>
| <span data-ttu-id="92888-3796">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-3796">Target</span></span> | <span data-ttu-id="92888-3797">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-3797">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-3798">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-3798">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-3799">4</span><span class="sxs-lookup"><span data-stu-id="92888-3799">4</span></span> |
| <span data-ttu-id="92888-3800">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-3800">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3802">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-3802">Buffer</span></span> | \- |
| <span data-ttu-id="92888-3803">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3803">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-3804">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3804">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-3805">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-3805">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-3806">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-3806">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-3807">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-3807">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3809">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-3809">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-3810">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-3810">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3812">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-3812">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3814">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-3814">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3816">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-3816">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-3817">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-3817">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-3818">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-3818">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-3819">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-3819">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-3820">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3820">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3822">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3822">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-3823">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3823">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3824">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-3824">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3825">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-3825">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-3826">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-3826">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-3827">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-3827">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3828">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-3828">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3829">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-3829">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-3830">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3830">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-3831">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3831">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-3832">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3832">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-3833">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-3833">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-3834">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-3834">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-3835">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3835">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-3836">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-3836">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3837">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-3837">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3838">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-3838">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3840">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3840">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3841">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-3841">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3842">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-3842">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-3843">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-3843">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-3844">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-3844">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-3845">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-3845">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-3846">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-3846">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-3847">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3847">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-3848">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3848">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-3849">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3849">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-3850">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-3850">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3852">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-3852">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfncsup-72"></a><span data-ttu-id="92888-3853">DXGI_FORMAT_BC1 \_ UNORM \_ sRGB<sup>FNC</sup> (72)</span><span class="sxs-lookup"><span data-stu-id="92888-3853">DXGI_FORMAT_BC1\_UNORM\_SRGB<sup>FNC</sup> (72)</span></span>
| <span data-ttu-id="92888-3854">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-3854">Target</span></span> | <span data-ttu-id="92888-3855">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-3855">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-3856">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-3856">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-3857">4</span><span class="sxs-lookup"><span data-stu-id="92888-3857">4</span></span> |
| <span data-ttu-id="92888-3858">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-3858">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3860">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-3860">Buffer</span></span> | \- |
| <span data-ttu-id="92888-3861">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3861">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-3862">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3862">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-3863">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-3863">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-3864">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-3864">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-3865">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-3865">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3867">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-3867">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-3868">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-3868">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3870">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-3870">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3872">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-3872">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3874">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-3874">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-3875">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-3875">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-3876">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-3876">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-3877">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-3877">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-3878">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3878">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3880">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3880">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-3881">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3881">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3882">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-3882">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3883">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-3883">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-3884">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-3884">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-3885">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-3885">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3886">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-3886">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3887">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-3887">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-3888">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3888">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-3889">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3889">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-3890">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3890">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-3891">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-3891">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-3892">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-3892">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-3893">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3893">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-3894">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-3894">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3895">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-3895">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3896">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-3896">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3898">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3898">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3899">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-3899">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3900">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-3900">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-3901">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-3901">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-3902">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-3902">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-3903">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-3903">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-3904">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-3904">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-3905">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3905">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-3906">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3906">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-3907">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3907">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-3908">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-3908">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3910">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-3910">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="92888-3911">DXGI_FORMAT_BC2 \_ <sup>PCC</sup> de tipo (73)</span><span class="sxs-lookup"><span data-stu-id="92888-3911">DXGI_FORMAT_BC2\_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="92888-3912">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-3912">Target</span></span> | <span data-ttu-id="92888-3913">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-3913">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-3914">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-3914">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-3915">8</span><span class="sxs-lookup"><span data-stu-id="92888-3915">8</span></span> |
| <span data-ttu-id="92888-3916">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-3916">Format Support</span></span> | \- |
| <span data-ttu-id="92888-3917">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-3917">Buffer</span></span> | \- |
| <span data-ttu-id="92888-3918">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3918">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-3919">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3919">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-3920">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-3920">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-3921">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-3921">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-3922">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-3922">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-3923">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-3923">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-3924">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-3924">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-3925">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-3925">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-3926">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-3926">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-3927">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-3927">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-3928">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-3928">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-3929">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-3929">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-3930">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-3930">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-3931">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3931">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-3932">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3932">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-3933">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3933">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3934">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-3934">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3935">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-3935">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-3936">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-3936">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-3937">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-3937">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3938">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-3938">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3939">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-3939">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-3940">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3940">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-3941">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3941">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-3942">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3942">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-3943">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-3943">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-3944">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-3944">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-3945">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3945">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-3946">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-3946">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3947">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-3947">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-3948">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-3948">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-3949">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3949">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3950">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-3950">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3951">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-3951">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-3952">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-3952">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-3953">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-3953">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-3954">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-3954">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-3955">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-3955">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-3956">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3956">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-3957">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3957">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-3958">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-3958">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-3959">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-3959">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-3960">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-3960">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unormsupfncsup-74"></a><span data-ttu-id="92888-3961">DXGI_FORMAT_BC2 \_ UNORM<sup>FNC</sup> (74)</span><span class="sxs-lookup"><span data-stu-id="92888-3961">DXGI_FORMAT_BC2\_UNORM<sup>FNC</sup> (74)</span></span>
| <span data-ttu-id="92888-3962">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-3962">Target</span></span> | <span data-ttu-id="92888-3963">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-3963">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-3964">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-3964">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-3965">8</span><span class="sxs-lookup"><span data-stu-id="92888-3965">8</span></span> |
| <span data-ttu-id="92888-3966">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-3966">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3968">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-3968">Buffer</span></span> | \- |
| <span data-ttu-id="92888-3969">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3969">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-3970">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-3970">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-3971">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-3971">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-3972">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-3972">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-3973">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-3973">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3975">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-3975">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-3976">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-3976">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3978">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-3978">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3980">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-3980">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3982">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-3982">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-3983">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-3983">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-3984">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-3984">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-3985">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-3985">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-3986">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3986">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-3988">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-3988">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-3989">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-3989">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3990">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-3990">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-3991">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-3991">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-3992">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-3992">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-3993">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-3993">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3994">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-3994">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-3995">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-3995">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-3996">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3996">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-3997">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3997">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-3998">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-3998">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-3999">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-3999">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-4000">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-4000">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-4001">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4001">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-4002">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-4002">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4003">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-4003">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4004">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-4004">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4006">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4006">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4007">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-4007">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4008">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-4008">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-4009">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-4009">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-4010">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-4010">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-4011">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-4011">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-4012">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-4012">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-4013">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4013">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-4014">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4014">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-4015">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4015">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-4016">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-4016">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4018">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-4018">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfncsup-75"></a><span data-ttu-id="92888-4019">DXGI_FORMAT_BC2 \_ UNORM \_ sRGB<sup>FNC</sup> (75)</span><span class="sxs-lookup"><span data-stu-id="92888-4019">DXGI_FORMAT_BC2\_UNORM\_SRGB<sup>FNC</sup> (75)</span></span>
| <span data-ttu-id="92888-4020">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-4020">Target</span></span> | <span data-ttu-id="92888-4021">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-4021">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-4022">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-4022">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-4023">8</span><span class="sxs-lookup"><span data-stu-id="92888-4023">8</span></span> |
| <span data-ttu-id="92888-4024">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-4024">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4026">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-4026">Buffer</span></span> | \- |
| <span data-ttu-id="92888-4027">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4027">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-4028">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4028">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-4029">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-4029">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-4030">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-4030">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-4031">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-4031">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4033">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-4033">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-4034">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-4034">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4036">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-4036">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4038">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-4038">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4040">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-4040">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-4041">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-4041">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-4042">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-4042">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-4043">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-4043">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-4044">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4044">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4046">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4046">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-4047">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4047">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4048">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-4048">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4049">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-4049">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-4050">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-4050">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-4051">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-4051">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4052">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-4052">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4053">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-4053">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-4054">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4054">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-4055">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4055">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-4056">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4056">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-4057">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-4057">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-4058">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-4058">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-4059">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4059">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-4060">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-4060">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4061">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-4061">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4062">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-4062">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4064">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4064">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4065">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-4065">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4066">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-4066">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-4067">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-4067">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-4068">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-4068">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-4069">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-4069">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-4070">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-4070">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-4071">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4071">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-4072">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4072">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-4073">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4073">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-4074">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-4074">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4076">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-4076">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="92888-4077">DXGI_FORMAT_BC3 \_ <sup>PCC</sup> de tipo (76)</span><span class="sxs-lookup"><span data-stu-id="92888-4077">DXGI_FORMAT_BC3\_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="92888-4078">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-4078">Target</span></span> | <span data-ttu-id="92888-4079">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-4079">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-4080">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-4080">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-4081">8</span><span class="sxs-lookup"><span data-stu-id="92888-4081">8</span></span> |
| <span data-ttu-id="92888-4082">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-4082">Format Support</span></span> | \- |
| <span data-ttu-id="92888-4083">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-4083">Buffer</span></span> | \- |
| <span data-ttu-id="92888-4084">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4084">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-4085">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4085">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-4086">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-4086">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-4087">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-4087">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-4088">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-4088">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-4089">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-4089">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-4090">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-4090">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-4091">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-4091">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-4092">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-4092">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-4093">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-4093">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-4094">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-4094">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-4095">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-4095">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-4096">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-4096">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-4097">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4097">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-4098">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4098">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-4099">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4099">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4100">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-4100">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4101">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-4101">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-4102">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-4102">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-4103">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-4103">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4104">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-4104">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4105">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-4105">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-4106">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4106">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-4107">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4107">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-4108">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4108">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-4109">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-4109">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-4110">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-4110">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-4111">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4111">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-4112">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-4112">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4113">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-4113">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4114">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-4114">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-4115">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4115">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4116">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-4116">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4117">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-4117">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-4118">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-4118">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-4119">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-4119">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-4120">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-4120">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-4121">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-4121">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-4122">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4122">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-4123">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4123">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-4124">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4124">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-4125">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-4125">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-4126">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-4126">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unormsupfncsup-77"></a><span data-ttu-id="92888-4127">DXGI_FORMAT_BC3 \_ UNORM<sup>FNC</sup> (77)</span><span class="sxs-lookup"><span data-stu-id="92888-4127">DXGI_FORMAT_BC3\_UNORM<sup>FNC</sup> (77)</span></span>
| <span data-ttu-id="92888-4128">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-4128">Target</span></span> | <span data-ttu-id="92888-4129">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-4129">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-4130">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-4130">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-4131">8</span><span class="sxs-lookup"><span data-stu-id="92888-4131">8</span></span> |
| <span data-ttu-id="92888-4132">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-4132">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4134">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-4134">Buffer</span></span> | \- |
| <span data-ttu-id="92888-4135">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4135">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-4136">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4136">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-4137">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-4137">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-4138">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-4138">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-4139">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-4139">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4141">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-4141">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-4142">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-4142">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4144">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-4144">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4146">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-4146">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4148">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-4148">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-4149">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-4149">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-4150">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-4150">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-4151">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-4151">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-4152">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4152">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4154">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4154">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-4155">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4155">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4156">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-4156">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4157">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-4157">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-4158">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-4158">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-4159">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-4159">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4160">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-4160">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4161">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-4161">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-4162">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4162">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-4163">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4163">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-4164">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4164">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-4165">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-4165">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-4166">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-4166">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-4167">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4167">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-4168">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-4168">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4169">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-4169">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4170">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-4170">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4172">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4172">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4173">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-4173">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4174">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-4174">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-4175">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-4175">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-4176">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-4176">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-4177">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-4177">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-4178">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-4178">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-4179">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4179">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-4180">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4180">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-4181">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4181">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-4182">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-4182">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4184">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-4184">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfncsup-78"></a><span data-ttu-id="92888-4185">DXGI_FORMAT_BC3 \_ UNORM \_ sRGB<sup>FNC</sup> (78)</span><span class="sxs-lookup"><span data-stu-id="92888-4185">DXGI_FORMAT_BC3\_UNORM\_SRGB<sup>FNC</sup> (78)</span></span>
| <span data-ttu-id="92888-4186">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-4186">Target</span></span> | <span data-ttu-id="92888-4187">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-4187">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-4188">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-4188">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-4189">8</span><span class="sxs-lookup"><span data-stu-id="92888-4189">8</span></span> |
| <span data-ttu-id="92888-4190">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-4190">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4192">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-4192">Buffer</span></span> | \- |
| <span data-ttu-id="92888-4193">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4193">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-4194">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4194">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-4195">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-4195">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-4196">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-4196">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-4197">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-4197">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4199">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-4199">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-4200">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-4200">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4202">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-4202">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4204">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-4204">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4206">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-4206">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-4207">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-4207">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-4208">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-4208">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-4209">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-4209">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-4210">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4210">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4212">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4212">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-4213">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4213">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4214">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-4214">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4215">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-4215">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-4216">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-4216">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-4217">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-4217">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4218">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-4218">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4219">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-4219">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-4220">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4220">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-4221">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4221">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-4222">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4222">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-4223">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-4223">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-4224">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-4224">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-4225">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4225">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-4226">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-4226">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4227">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-4227">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4228">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-4228">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4230">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4230">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4231">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-4231">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4232">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-4232">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-4233">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-4233">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-4234">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-4234">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-4235">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-4235">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-4236">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-4236">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-4237">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4237">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-4238">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4238">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-4239">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4239">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-4240">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-4240">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4242">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-4242">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="92888-4243">DXGI_FORMAT_BC4 \_ <sup>PCC</sup> de tipo (79)</span><span class="sxs-lookup"><span data-stu-id="92888-4243">DXGI_FORMAT_BC4\_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="92888-4244">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-4244">Target</span></span> | <span data-ttu-id="92888-4245">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-4245">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-4246">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-4246">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-4247">4</span><span class="sxs-lookup"><span data-stu-id="92888-4247">4</span></span> |
| <span data-ttu-id="92888-4248">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-4248">Format Support</span></span> | \- |
| <span data-ttu-id="92888-4249">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-4249">Buffer</span></span> | \- |
| <span data-ttu-id="92888-4250">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4250">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-4251">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4251">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-4252">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-4252">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-4253">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-4253">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-4254">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-4254">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-4255">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-4255">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-4256">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-4256">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-4257">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-4257">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-4258">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-4258">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-4259">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-4259">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-4260">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-4260">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-4261">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-4261">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-4262">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-4262">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-4263">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4263">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-4264">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4264">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-4265">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4265">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4266">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-4266">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4267">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-4267">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-4268">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-4268">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-4269">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-4269">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4270">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-4270">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4271">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-4271">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-4272">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4272">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-4273">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4273">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-4274">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4274">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-4275">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-4275">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-4276">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-4276">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-4277">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4277">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-4278">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-4278">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4279">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-4279">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4280">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-4280">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-4281">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4281">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4282">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-4282">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4283">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-4283">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-4284">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-4284">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-4285">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-4285">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-4286">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-4286">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-4287">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-4287">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-4288">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4288">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-4289">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4289">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-4290">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4290">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-4291">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-4291">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-4292">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-4292">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_unormsupfncsup-80"></a><span data-ttu-id="92888-4293">DXGI_FORMAT_BC4 \_ UNORM<sup>FNC</sup> (80)</span><span class="sxs-lookup"><span data-stu-id="92888-4293">DXGI_FORMAT_BC4\_UNORM<sup>FNC</sup> (80)</span></span>
| <span data-ttu-id="92888-4294">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-4294">Target</span></span> | <span data-ttu-id="92888-4295">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-4295">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-4296">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-4296">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-4297">4</span><span class="sxs-lookup"><span data-stu-id="92888-4297">4</span></span> |
| <span data-ttu-id="92888-4298">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-4298">Format Support</span></span> | \- |
| <span data-ttu-id="92888-4299">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-4299">Buffer</span></span> | \- |
| <span data-ttu-id="92888-4300">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4300">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-4301">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4301">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-4302">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-4302">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-4303">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-4303">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-4304">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-4304">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-4305">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-4305">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-4306">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-4306">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-4307">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-4307">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-4308">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-4308">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-4309">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-4309">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-4310">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-4310">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-4311">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-4311">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-4312">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-4312">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-4313">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4313">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-4314">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4314">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-4315">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4315">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4316">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-4316">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4317">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-4317">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-4318">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-4318">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-4319">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-4319">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4320">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-4320">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4321">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-4321">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-4322">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4322">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-4323">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4323">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-4324">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4324">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-4325">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-4325">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-4326">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-4326">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-4327">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4327">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-4328">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-4328">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4329">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-4329">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4330">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-4330">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-4331">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4331">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4332">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-4332">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4333">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-4333">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-4334">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-4334">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-4335">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-4335">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-4336">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-4336">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-4337">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-4337">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-4338">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4338">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-4339">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4339">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-4340">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4340">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-4341">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-4341">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-4342">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-4342">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_snormsupfncsup-81"></a><span data-ttu-id="92888-4343">DXGI_FORMAT_BC4 \_ SNORM<sup>FNC</sup> (81)</span><span class="sxs-lookup"><span data-stu-id="92888-4343">DXGI_FORMAT_BC4\_SNORM<sup>FNC</sup> (81)</span></span>
| <span data-ttu-id="92888-4344">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-4344">Target</span></span> | <span data-ttu-id="92888-4345">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-4345">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-4346">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-4346">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-4347">4</span><span class="sxs-lookup"><span data-stu-id="92888-4347">4</span></span> |
| <span data-ttu-id="92888-4348">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-4348">Format Support</span></span> | \- |
| <span data-ttu-id="92888-4349">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-4349">Buffer</span></span> | \- |
| <span data-ttu-id="92888-4350">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4350">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-4351">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4351">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-4352">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-4352">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-4353">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-4353">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-4354">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-4354">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-4355">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-4355">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-4356">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-4356">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-4357">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-4357">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-4358">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-4358">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-4359">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-4359">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-4360">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-4360">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-4361">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-4361">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-4362">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-4362">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-4363">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4363">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-4364">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4364">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-4365">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4365">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4366">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-4366">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4367">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-4367">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-4368">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-4368">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-4369">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-4369">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4370">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-4370">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4371">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-4371">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-4372">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4372">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-4373">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4373">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-4374">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4374">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-4375">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-4375">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-4376">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-4376">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-4377">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4377">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-4378">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-4378">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4379">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-4379">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4380">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-4380">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-4381">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4381">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4382">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-4382">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4383">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-4383">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-4384">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-4384">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-4385">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-4385">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-4386">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-4386">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-4387">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-4387">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-4388">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4388">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-4389">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4389">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-4390">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4390">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-4391">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-4391">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-4392">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-4392">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="92888-4393">DXGI_FORMAT_BC5 \_ <sup>PCC</sup> de tipo (82)</span><span class="sxs-lookup"><span data-stu-id="92888-4393">DXGI_FORMAT_BC5\_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="92888-4394">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-4394">Target</span></span> | <span data-ttu-id="92888-4395">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-4395">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-4396">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-4396">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-4397">8</span><span class="sxs-lookup"><span data-stu-id="92888-4397">8</span></span> |
| <span data-ttu-id="92888-4398">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-4398">Format Support</span></span> | \- |
| <span data-ttu-id="92888-4399">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-4399">Buffer</span></span> | \- |
| <span data-ttu-id="92888-4400">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4400">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-4401">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4401">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-4402">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-4402">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-4403">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-4403">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-4404">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-4404">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-4405">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-4405">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-4406">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-4406">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-4407">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-4407">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-4408">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-4408">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-4409">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-4409">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-4410">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-4410">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-4411">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-4411">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-4412">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-4412">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-4413">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4413">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-4414">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4414">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-4415">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4415">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4416">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-4416">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4417">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-4417">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-4418">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-4418">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-4419">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-4419">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4420">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-4420">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4421">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-4421">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-4422">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4422">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-4423">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4423">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-4424">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4424">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-4425">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-4425">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-4426">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-4426">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-4427">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4427">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-4428">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-4428">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4429">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-4429">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4430">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-4430">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-4431">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4431">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4432">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-4432">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4433">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-4433">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-4434">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-4434">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-4435">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-4435">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-4436">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-4436">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-4437">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-4437">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-4438">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4438">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-4439">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4439">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-4440">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4440">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-4441">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-4441">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-4442">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-4442">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_unormsupfncsup-83"></a><span data-ttu-id="92888-4443">DXGI_FORMAT_BC5 \_ UNORM<sup>FNC</sup> (83)</span><span class="sxs-lookup"><span data-stu-id="92888-4443">DXGI_FORMAT_BC5\_UNORM<sup>FNC</sup> (83)</span></span>
| <span data-ttu-id="92888-4444">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-4444">Target</span></span> | <span data-ttu-id="92888-4445">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-4445">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-4446">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-4446">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-4447">8</span><span class="sxs-lookup"><span data-stu-id="92888-4447">8</span></span> |
| <span data-ttu-id="92888-4448">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-4448">Format Support</span></span> | \- |
| <span data-ttu-id="92888-4449">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-4449">Buffer</span></span> | \- |
| <span data-ttu-id="92888-4450">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4450">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-4451">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4451">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-4452">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-4452">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-4453">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-4453">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-4454">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-4454">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-4455">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-4455">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-4456">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-4456">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-4457">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-4457">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-4458">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-4458">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-4459">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-4459">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-4460">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-4460">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-4461">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-4461">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-4462">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-4462">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-4463">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4463">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-4464">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4464">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-4465">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4465">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4466">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-4466">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4467">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-4467">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-4468">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-4468">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-4469">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-4469">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4470">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-4470">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4471">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-4471">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-4472">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4472">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-4473">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4473">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-4474">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4474">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-4475">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-4475">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-4476">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-4476">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-4477">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4477">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-4478">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-4478">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4479">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-4479">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4480">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-4480">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-4481">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4481">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4482">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-4482">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4483">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-4483">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-4484">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-4484">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-4485">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-4485">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-4486">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-4486">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-4487">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-4487">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-4488">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4488">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-4489">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4489">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-4490">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4490">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-4491">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-4491">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-4492">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-4492">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_snormsupfncsup-84"></a><span data-ttu-id="92888-4493">DXGI_FORMAT_BC5 \_ SNORM<sup>FNC</sup> (84)</span><span class="sxs-lookup"><span data-stu-id="92888-4493">DXGI_FORMAT_BC5\_SNORM<sup>FNC</sup> (84)</span></span>
| <span data-ttu-id="92888-4494">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-4494">Target</span></span> | <span data-ttu-id="92888-4495">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-4495">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-4496">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-4496">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-4497">8</span><span class="sxs-lookup"><span data-stu-id="92888-4497">8</span></span> |
| <span data-ttu-id="92888-4498">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-4498">Format Support</span></span> | \- |
| <span data-ttu-id="92888-4499">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-4499">Buffer</span></span> | \- |
| <span data-ttu-id="92888-4500">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4500">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-4501">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4501">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-4502">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-4502">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-4503">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-4503">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-4504">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-4504">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-4505">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-4505">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-4506">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-4506">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-4507">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-4507">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-4508">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-4508">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-4509">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-4509">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-4510">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-4510">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-4511">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-4511">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-4512">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-4512">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-4513">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4513">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-4514">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4514">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-4515">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4515">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4516">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-4516">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4517">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-4517">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-4518">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-4518">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-4519">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-4519">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4520">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-4520">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4521">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-4521">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-4522">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4522">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-4523">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4523">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-4524">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4524">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-4525">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-4525">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-4526">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-4526">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-4527">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4527">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-4528">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-4528">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4529">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-4529">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4530">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-4530">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-4531">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4531">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4532">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-4532">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4533">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-4533">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-4534">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-4534">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-4535">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-4535">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-4536">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-4536">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-4537">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-4537">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-4538">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4538">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-4539">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4539">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-4540">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4540">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-4541">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-4541">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-4542">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-4542">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="92888-4543">DXGI_FORMAT_B5G6R5 \_ UNORM<sup>FNS</sup> (85)</span><span class="sxs-lookup"><span data-stu-id="92888-4543">DXGI_FORMAT_B5G6R5\_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="92888-4544">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-4544">Target</span></span> | <span data-ttu-id="92888-4545">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-4545">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-4546">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-4546">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-4547">16</span><span class="sxs-lookup"><span data-stu-id="92888-4547">16</span></span> |
| <span data-ttu-id="92888-4548">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-4548">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4550">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-4550">Buffer</span></span> | \- |
| <span data-ttu-id="92888-4551">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4551">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-4552">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4552">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-4553">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-4553">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-4554">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-4554">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-4555">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-4555">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4557">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-4557">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-4558">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-4558">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4560">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-4560">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4562">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-4562">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4564">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-4564">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-4565">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-4565">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-4566">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-4566">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-4567">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-4567">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-4568">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4568">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4570">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4570">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4572">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4572">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4574">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-4574">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4576">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-4576">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-4577">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-4577">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-4578">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-4578">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4579">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-4579">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4580">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-4580">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-4581">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4581">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-4582">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4582">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-4583">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4583">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-4584">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-4584">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-4585">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-4585">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-4586">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4586">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-4587">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-4587">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4588">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-4588">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4589">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-4589">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4591">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4591">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-4593">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-4593">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-4595">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-4595">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-4597">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-4597">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4599">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-4599">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-4600">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-4600">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-4601">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-4601">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-4602">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4602">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-4603">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4603">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-4604">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4604">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-4605">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-4605">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-4606">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-4606">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="92888-4607">DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>FNS</sup> (86)</span><span class="sxs-lookup"><span data-stu-id="92888-4607">DXGI_FORMAT_B5G5R5A1\_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="92888-4608">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-4608">Target</span></span> | <span data-ttu-id="92888-4609">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-4609">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-4610">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-4610">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-4611">16</span><span class="sxs-lookup"><span data-stu-id="92888-4611">16</span></span> |
| <span data-ttu-id="92888-4612">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-4612">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4614">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-4614">Buffer</span></span> | \- |
| <span data-ttu-id="92888-4615">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4615">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-4616">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4616">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-4617">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-4617">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-4618">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-4618">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-4619">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-4619">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4621">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-4621">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-4622">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-4622">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4624">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-4624">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4626">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-4626">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4628">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-4628">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-4629">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-4629">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-4630">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-4630">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-4631">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-4631">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-4632">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4632">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4634">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4634">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-4635">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4635">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4636">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-4636">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4637">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-4637">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-4638">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-4638">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-4639">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-4639">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4640">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-4640">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4641">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-4641">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-4642">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4642">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-4643">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4643">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-4644">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4644">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-4645">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-4645">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-4646">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-4646">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-4647">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4647">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-4648">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-4648">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4649">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-4649">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4650">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-4650">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4652">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4652">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4653">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-4653">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4654">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-4654">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-4655">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-4655">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-4656">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-4656">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-4657">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-4657">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-4658">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-4658">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-4659">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4659">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-4660">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4660">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-4661">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4661">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-4662">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-4662">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-4663">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-4663">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="92888-4664">DXGI_FORMAT_B8G8R8A8 \_ <sup>PCs</sup> não tipados (90)</span><span class="sxs-lookup"><span data-stu-id="92888-4664">DXGI_FORMAT_B8G8R8A8\_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="92888-4665">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-4665">Target</span></span> | <span data-ttu-id="92888-4666">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-4666">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-4667">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-4667">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-4668">32</span><span class="sxs-lookup"><span data-stu-id="92888-4668">32</span></span> |
| <span data-ttu-id="92888-4669">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-4669">Format Support</span></span> | \- |
| <span data-ttu-id="92888-4670">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-4670">Buffer</span></span> | \- |
| <span data-ttu-id="92888-4671">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4671">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-4672">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4672">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-4673">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-4673">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-4674">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-4674">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-4675">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-4675">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-4676">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-4676">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-4677">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-4677">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-4678">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-4678">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-4679">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-4679">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-4680">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-4680">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-4681">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-4681">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-4682">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-4682">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-4683">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-4683">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-4684">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4684">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-4685">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4685">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-4686">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4686">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4687">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-4687">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4688">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-4688">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-4689">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-4689">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-4690">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-4690">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4691">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-4691">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4692">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-4692">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-4693">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4693">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-4694">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4694">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-4695">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4695">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-4696">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-4696">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-4697">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-4697">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-4698">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4698">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-4699">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-4699">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4700">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-4700">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4701">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-4701">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-4702">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4702">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4703">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-4703">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4704">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-4704">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-4705">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-4705">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-4706">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-4706">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-4707">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-4707">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-4708">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-4708">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-4709">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4709">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-4710">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4710">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-4711">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4711">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-4712">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-4712">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-4713">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-4713">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfnssup-87"></a><span data-ttu-id="92888-4714">DXGI_FORMAT_B8G8R8A8 \_ UNORM<sup>FNS</sup> (87)</span><span class="sxs-lookup"><span data-stu-id="92888-4714">DXGI_FORMAT_B8G8R8A8\_UNORM<sup>FNS</sup> (87)</span></span>
| <span data-ttu-id="92888-4715">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-4715">Target</span></span> | <span data-ttu-id="92888-4716">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-4716">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-4717">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-4717">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-4718">32</span><span class="sxs-lookup"><span data-stu-id="92888-4718">32</span></span> |
| <span data-ttu-id="92888-4719">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-4719">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4721">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-4721">Buffer</span></span> | \- |
| <span data-ttu-id="92888-4722">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4722">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-4723">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4723">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-4724">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-4724">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-4725">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-4725">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-4726">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-4726">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4728">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-4728">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4730">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-4730">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4732">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-4732">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4734">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-4734">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4736">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-4736">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-4737">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-4737">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-4738">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-4738">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-4739">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-4739">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-4740">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4740">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4742">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4742">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4744">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4744">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4746">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-4746">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4748">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-4748">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-4749">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-4749">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-4750">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-4750">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4751">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-4751">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4752">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-4752">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-4753">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4753">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-4754">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4754">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-4755">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4755">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-4756">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-4756">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-4757">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-4757">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-4758">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4758">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-4759">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-4759">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4760">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-4760">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4761">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-4761">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4763">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4763">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-4765">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-4765">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-4767">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-4767">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-4769">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-4769">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4771">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-4771">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-4772">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-4772">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4774">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-4774">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-4775">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4775">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-4776">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4776">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-4778">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4778">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4780">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-4780">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4782">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-4782">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfnssup-91"></a><span data-ttu-id="92888-4783">DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ sRGB<sup>FNS</sup> (91)</span><span class="sxs-lookup"><span data-stu-id="92888-4783">DXGI_FORMAT_B8G8R8A8\_UNORM\_SRGB<sup>FNS</sup> (91)</span></span>
| <span data-ttu-id="92888-4784">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-4784">Target</span></span> | <span data-ttu-id="92888-4785">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-4785">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-4786">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-4786">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-4787">32</span><span class="sxs-lookup"><span data-stu-id="92888-4787">32</span></span> |
| <span data-ttu-id="92888-4788">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-4788">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4790">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-4790">Buffer</span></span> | \- |
| <span data-ttu-id="92888-4791">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4791">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-4792">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4792">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-4793">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-4793">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-4794">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-4794">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-4795">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-4795">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4797">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-4797">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4799">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-4799">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4801">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-4801">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4803">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-4803">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4805">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-4805">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-4806">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-4806">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-4807">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-4807">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-4808">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-4808">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-4809">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4809">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4811">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4811">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4813">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4813">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4815">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-4815">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4817">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-4817">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-4818">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-4818">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-4819">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-4819">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4820">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-4820">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4821">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-4821">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-4822">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4822">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-4823">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4823">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-4824">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4824">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-4825">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-4825">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-4826">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-4826">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-4827">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4827">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-4828">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-4828">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4829">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-4829">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4830">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-4830">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4832">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4832">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-4834">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-4834">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-4836">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-4836">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-4838">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-4838">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4840">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-4840">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-4841">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-4841">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4843">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-4843">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-4844">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4844">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-4845">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4845">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-4847">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4847">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4849">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-4849">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4851">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-4851">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="92888-4852">DXGI_FORMAT_B8G8R8X8 \_ <sup>PCs</sup> não tipados (92)</span><span class="sxs-lookup"><span data-stu-id="92888-4852">DXGI_FORMAT_B8G8R8X8\_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="92888-4853">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-4853">Target</span></span> | <span data-ttu-id="92888-4854">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-4854">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-4855">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-4855">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-4856">32</span><span class="sxs-lookup"><span data-stu-id="92888-4856">32</span></span> |
| <span data-ttu-id="92888-4857">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-4857">Format Support</span></span> | \- |
| <span data-ttu-id="92888-4858">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-4858">Buffer</span></span> | \- |
| <span data-ttu-id="92888-4859">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4859">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-4860">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4860">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-4861">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-4861">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-4862">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-4862">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-4863">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-4863">Texture2D</span></span> | \- |
| <span data-ttu-id="92888-4864">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-4864">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-4865">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-4865">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-4866">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-4866">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-4867">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-4867">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-4868">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-4868">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-4869">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-4869">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-4870">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-4870">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-4871">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-4871">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-4872">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4872">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-4873">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4873">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-4874">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4874">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4875">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-4875">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4876">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-4876">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-4877">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-4877">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-4878">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-4878">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4879">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-4879">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4880">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-4880">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-4881">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4881">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-4882">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4882">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-4883">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4883">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-4884">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-4884">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-4885">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-4885">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-4886">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4886">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-4887">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-4887">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4888">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-4888">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4889">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-4889">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-4890">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4890">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4891">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-4891">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-4892">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-4892">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-4893">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-4893">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-4894">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-4894">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-4895">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-4895">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-4896">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-4896">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-4897">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4897">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-4898">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4898">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-4899">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4899">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-4900">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-4900">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-4901">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-4901">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfnssup-88"></a><span data-ttu-id="92888-4902">DXGI_FORMAT_B8G8R8X8 \_ UNORM<sup>FNS</sup> (88)</span><span class="sxs-lookup"><span data-stu-id="92888-4902">DXGI_FORMAT_B8G8R8X8\_UNORM<sup>FNS</sup> (88)</span></span>
| <span data-ttu-id="92888-4903">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-4903">Target</span></span> | <span data-ttu-id="92888-4904">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-4904">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-4905">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-4905">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-4906">32</span><span class="sxs-lookup"><span data-stu-id="92888-4906">32</span></span> |
| <span data-ttu-id="92888-4907">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-4907">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4909">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-4909">Buffer</span></span> | \- |
| <span data-ttu-id="92888-4910">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4910">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-4911">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4911">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-4912">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-4912">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-4913">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-4913">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-4914">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-4914">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4916">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-4916">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4918">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-4918">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4920">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-4920">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4922">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-4922">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4924">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-4924">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-4925">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-4925">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-4926">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-4926">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-4927">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-4927">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-4928">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4928">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4930">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4930">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4932">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4932">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4934">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-4934">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4936">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-4936">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-4937">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-4937">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-4938">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-4938">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4939">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-4939">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-4940">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-4940">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-4941">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4941">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-4942">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4942">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-4943">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4943">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-4944">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-4944">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-4945">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-4945">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-4946">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-4946">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-4947">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-4947">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4948">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-4948">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-4949">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-4949">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4951">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-4951">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-4953">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-4953">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-4955">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-4955">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-4957">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-4957">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4959">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-4959">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-4960">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-4960">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-4961">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-4961">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-4962">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4962">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-4963">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4963">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-4965">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-4965">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-4967">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-4967">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4969">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-4969">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfnssup-93"></a><span data-ttu-id="92888-4970">DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ sRGB<sup>FNS</sup> (93)</span><span class="sxs-lookup"><span data-stu-id="92888-4970">DXGI_FORMAT_B8G8R8X8\_UNORM\_SRGB<sup>FNS</sup> (93)</span></span>
| <span data-ttu-id="92888-4971">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-4971">Target</span></span> | <span data-ttu-id="92888-4972">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-4972">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-4973">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-4973">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-4974">32</span><span class="sxs-lookup"><span data-stu-id="92888-4974">32</span></span> |
| <span data-ttu-id="92888-4975">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-4975">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4977">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-4977">Buffer</span></span> | \- |
| <span data-ttu-id="92888-4978">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4978">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-4979">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-4979">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-4980">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-4980">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-4981">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-4981">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-4982">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-4982">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4984">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-4984">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4986">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-4986">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4988">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-4988">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4990">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-4990">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4992">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-4992">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-4993">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-4993">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-4994">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-4994">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-4995">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-4995">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-4996">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4996">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-4998">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-4998">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5000">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5000">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5002">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-5002">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5004">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-5004">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-5005">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-5005">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-5006">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-5006">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5007">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-5007">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5008">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-5008">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-5009">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5009">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-5010">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5010">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-5011">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5011">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-5012">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-5012">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-5013">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-5013">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-5014">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5014">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-5015">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-5015">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5016">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-5016">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5017">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-5017">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5019">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5019">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5021">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-5021">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5023">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-5023">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5025">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-5025">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5027">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-5027">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-5028">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-5028">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-5029">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-5029">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-5030">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5030">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-5031">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5031">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-5032">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5032">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-5033">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-5033">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5035">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-5035">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="92888-5036">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span><span class="sxs-lookup"><span data-stu-id="92888-5036">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="92888-5037">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-5037">Target</span></span> | <span data-ttu-id="92888-5038">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-5038">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-5039">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-5039">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-5040">32</span><span class="sxs-lookup"><span data-stu-id="92888-5040">32</span></span> |
| <span data-ttu-id="92888-5041">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-5041">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5043">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-5043">Buffer</span></span> | \- |
| <span data-ttu-id="92888-5044">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5044">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-5045">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5045">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-5046">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-5046">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-5047">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-5047">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-5048">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-5048">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5050">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-5050">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-5051">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-5051">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-5052">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-5052">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-5053">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-5053">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-5054">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-5054">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-5055">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-5055">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-5056">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-5056">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-5057">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-5057">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-5058">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5058">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-5059">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5059">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-5060">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5060">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5061">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-5061">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5062">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-5062">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-5063">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-5063">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-5064">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-5064">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5065">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-5065">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5066">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-5066">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-5067">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5067">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-5068">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5068">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-5069">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5069">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-5070">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-5070">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-5071">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-5071">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-5072">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5072">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-5073">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-5073">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5074">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-5074">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5075">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-5075">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5077">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5077">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5078">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-5078">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5079">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-5079">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-5080">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-5080">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-5081">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-5081">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-5082">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-5082">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-5083">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-5083">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-5084">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5084">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5086">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5086">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5088">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5088">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5090">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-5090">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-5091">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-5091">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="92888-5092">DXGI_FORMAT_Y410<sup>V</sup> (101)</span><span class="sxs-lookup"><span data-stu-id="92888-5092">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="92888-5093">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-5093">Target</span></span> | <span data-ttu-id="92888-5094">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-5094">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-5095">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-5095">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-5096">32</span><span class="sxs-lookup"><span data-stu-id="92888-5096">32</span></span> |
| <span data-ttu-id="92888-5097">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-5097">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5099">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-5099">Buffer</span></span> | \- |
| <span data-ttu-id="92888-5100">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5100">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-5101">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5101">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-5102">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-5102">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-5103">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-5103">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-5104">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-5104">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5106">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-5106">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-5107">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-5107">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-5108">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-5108">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-5109">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-5109">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-5110">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-5110">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-5111">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-5111">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-5112">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-5112">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-5113">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-5113">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-5114">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5114">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-5115">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5115">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-5116">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5116">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5117">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-5117">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5118">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-5118">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-5119">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-5119">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-5120">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-5120">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5121">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-5121">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5122">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-5122">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-5123">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5123">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-5124">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5124">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-5125">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5125">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-5126">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-5126">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-5127">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-5127">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-5128">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5128">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-5129">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-5129">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5130">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-5130">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5131">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-5131">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5133">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5133">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5134">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-5134">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5135">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-5135">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-5136">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-5136">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-5137">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-5137">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-5138">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-5138">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-5139">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-5139">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-5140">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5140">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5142">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5142">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5144">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5144">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5146">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-5146">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-5147">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-5147">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="92888-5148">DXGI_FORMAT_Y416<sup>V</sup> (102)</span><span class="sxs-lookup"><span data-stu-id="92888-5148">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="92888-5149">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-5149">Target</span></span> | <span data-ttu-id="92888-5150">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-5150">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-5151">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-5151">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-5152">64</span><span class="sxs-lookup"><span data-stu-id="92888-5152">64</span></span> |
| <span data-ttu-id="92888-5153">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-5153">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5155">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-5155">Buffer</span></span> | \- |
| <span data-ttu-id="92888-5156">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5156">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-5157">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5157">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-5158">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-5158">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-5159">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-5159">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-5160">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-5160">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5162">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-5162">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-5163">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-5163">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-5164">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-5164">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-5165">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-5165">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-5166">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-5166">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-5167">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-5167">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-5168">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-5168">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-5169">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-5169">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-5170">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5170">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-5171">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5171">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-5172">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5172">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5173">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-5173">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5174">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-5174">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-5175">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-5175">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-5176">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-5176">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5177">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-5177">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5178">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-5178">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-5179">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5179">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-5180">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5180">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-5181">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5181">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-5182">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-5182">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-5183">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-5183">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-5184">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5184">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-5185">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-5185">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5186">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-5186">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5187">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-5187">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5189">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5189">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5190">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-5190">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5191">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-5191">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-5192">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-5192">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-5193">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-5193">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-5194">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-5194">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-5195">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-5195">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-5196">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5196">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5198">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5198">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5200">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5200">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5202">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-5202">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-5203">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-5203">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="92888-5204">DXGI_FORMAT_NV12<sup>V</sup> (103)</span><span class="sxs-lookup"><span data-stu-id="92888-5204">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="92888-5205">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-5205">Target</span></span> | <span data-ttu-id="92888-5206">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-5206">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-5207">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-5207">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-5208">8</span><span class="sxs-lookup"><span data-stu-id="92888-5208">8</span></span> |
| <span data-ttu-id="92888-5209">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-5209">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5211">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-5211">Buffer</span></span> | \- |
| <span data-ttu-id="92888-5212">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5212">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-5213">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5213">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-5214">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-5214">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-5215">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-5215">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-5216">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-5216">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5218">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-5218">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-5219">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-5219">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-5220">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-5220">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-5221">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-5221">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-5222">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-5222">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-5223">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-5223">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-5224">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-5224">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-5225">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-5225">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-5226">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5226">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-5227">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5227">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-5228">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5228">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5229">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-5229">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5230">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-5230">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-5231">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-5231">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-5232">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-5232">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5233">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-5233">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5234">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-5234">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-5235">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5235">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-5236">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5236">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-5237">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5237">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-5238">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-5238">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-5239">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-5239">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-5240">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5240">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-5241">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-5241">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5242">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-5242">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5243">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-5243">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5245">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5245">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5246">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-5246">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5247">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-5247">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-5248">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-5248">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-5249">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-5249">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-5250">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-5250">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-5251">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-5251">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-5252">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5252">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5254">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5254">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5256">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5256">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5258">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-5258">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-5259">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-5259">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="92888-5260">DXGI_FORMAT_P010<sup>V</sup> (104)</span><span class="sxs-lookup"><span data-stu-id="92888-5260">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="92888-5261">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-5261">Target</span></span> | <span data-ttu-id="92888-5262">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-5262">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-5263">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-5263">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-5264">16</span><span class="sxs-lookup"><span data-stu-id="92888-5264">16</span></span> |
| <span data-ttu-id="92888-5265">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-5265">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5267">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-5267">Buffer</span></span> | \- |
| <span data-ttu-id="92888-5268">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5268">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-5269">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5269">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-5270">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-5270">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-5271">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-5271">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-5272">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-5272">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5274">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-5274">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-5275">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-5275">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-5276">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-5276">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-5277">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-5277">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-5278">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-5278">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-5279">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-5279">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-5280">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-5280">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-5281">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-5281">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-5282">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5282">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-5283">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5283">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-5284">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5284">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5285">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-5285">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5286">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-5286">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-5287">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-5287">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-5288">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-5288">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5289">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-5289">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5290">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-5290">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-5291">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5291">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-5292">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5292">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-5293">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5293">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-5294">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-5294">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-5295">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-5295">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-5296">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5296">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-5297">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-5297">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5298">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-5298">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5299">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-5299">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5301">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5301">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5302">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-5302">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5303">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-5303">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-5304">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-5304">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-5305">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-5305">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-5306">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-5306">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-5307">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-5307">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-5308">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5308">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5310">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5310">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5312">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5312">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5314">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-5314">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-5315">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-5315">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="92888-5316">DXGI_FORMAT_P016<sup>V</sup> (105)</span><span class="sxs-lookup"><span data-stu-id="92888-5316">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="92888-5317">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-5317">Target</span></span> | <span data-ttu-id="92888-5318">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-5318">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-5319">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-5319">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-5320">16</span><span class="sxs-lookup"><span data-stu-id="92888-5320">16</span></span> |
| <span data-ttu-id="92888-5321">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-5321">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5323">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-5323">Buffer</span></span> | \- |
| <span data-ttu-id="92888-5324">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5324">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-5325">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5325">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-5326">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-5326">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-5327">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-5327">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-5328">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-5328">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5330">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-5330">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-5331">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-5331">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-5332">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-5332">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-5333">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-5333">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-5334">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-5334">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-5335">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-5335">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-5336">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-5336">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-5337">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-5337">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-5338">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5338">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-5339">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5339">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-5340">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5340">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5341">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-5341">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5342">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-5342">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-5343">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-5343">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-5344">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-5344">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5345">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-5345">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5346">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-5346">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-5347">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5347">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-5348">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5348">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-5349">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5349">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-5350">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-5350">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-5351">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-5351">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-5352">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5352">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-5353">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-5353">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5354">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-5354">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5355">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-5355">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5357">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5357">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5358">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-5358">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5359">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-5359">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-5360">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-5360">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-5361">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-5361">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-5362">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-5362">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-5363">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-5363">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-5364">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5364">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5366">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5366">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5368">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5368">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5370">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-5370">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-5371">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-5371">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="92888-5372">DXGI_FORMAT_420 \_ opaco<sup>V</sup> (106)</span><span class="sxs-lookup"><span data-stu-id="92888-5372">DXGI_FORMAT_420\_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="92888-5373">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-5373">Target</span></span> | <span data-ttu-id="92888-5374">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-5374">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-5375">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-5375">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-5376">8</span><span class="sxs-lookup"><span data-stu-id="92888-5376">8</span></span> |
| <span data-ttu-id="92888-5377">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-5377">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5379">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-5379">Buffer</span></span> | \- |
| <span data-ttu-id="92888-5380">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5380">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-5381">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5381">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-5382">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-5382">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-5383">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-5383">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-5384">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-5384">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5386">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-5386">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-5387">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-5387">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-5388">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-5388">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-5389">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-5389">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-5390">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-5390">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-5391">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-5391">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-5392">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-5392">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-5393">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-5393">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-5394">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5394">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-5395">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5395">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-5396">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5396">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5397">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-5397">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5398">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-5398">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-5399">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-5399">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-5400">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-5400">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5401">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-5401">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5402">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-5402">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-5403">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5403">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-5404">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5404">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-5405">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5405">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-5406">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-5406">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-5407">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-5407">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-5408">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5408">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-5409">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-5409">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5410">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-5410">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5411">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-5411">CPU Lockable</span></span> | \- |
| <span data-ttu-id="92888-5412">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5412">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5413">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-5413">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5414">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-5414">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-5415">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-5415">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-5416">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-5416">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-5417">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-5417">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-5418">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-5418">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-5419">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5419">Video Decoder Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5421">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5421">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5423">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5423">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5425">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-5425">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-5426">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-5426">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="92888-5427">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span><span class="sxs-lookup"><span data-stu-id="92888-5427">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="92888-5428">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-5428">Target</span></span> | <span data-ttu-id="92888-5429">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-5429">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-5430">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-5430">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-5431">16</span><span class="sxs-lookup"><span data-stu-id="92888-5431">16</span></span> |
| <span data-ttu-id="92888-5432">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-5432">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5434">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-5434">Buffer</span></span> | \- |
| <span data-ttu-id="92888-5435">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5435">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-5436">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5436">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-5437">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-5437">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-5438">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-5438">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-5439">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-5439">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5441">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-5441">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-5442">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-5442">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-5443">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-5443">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-5444">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-5444">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-5445">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-5445">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-5446">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-5446">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-5447">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-5447">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-5448">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-5448">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-5449">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5449">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-5450">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5450">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-5451">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5451">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5452">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-5452">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5453">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-5453">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-5454">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-5454">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-5455">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-5455">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5456">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-5456">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5457">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-5457">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-5458">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5458">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-5459">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5459">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-5460">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5460">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-5461">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-5461">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-5462">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-5462">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-5463">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5463">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-5464">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-5464">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5465">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-5465">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5466">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-5466">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5468">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5468">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5469">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-5469">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5470">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-5470">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-5471">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-5471">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-5472">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-5472">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-5473">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-5473">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-5474">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-5474">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-5475">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5475">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5477">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5477">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5479">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5479">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5481">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-5481">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-5482">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-5482">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="92888-5483">DXGI_FORMAT_Y210<sup>V</sup> (108)</span><span class="sxs-lookup"><span data-stu-id="92888-5483">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="92888-5484">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-5484">Target</span></span> | <span data-ttu-id="92888-5485">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-5485">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-5486">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-5486">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-5487">32</span><span class="sxs-lookup"><span data-stu-id="92888-5487">32</span></span> |
| <span data-ttu-id="92888-5488">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-5488">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5490">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-5490">Buffer</span></span> | \- |
| <span data-ttu-id="92888-5491">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5491">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-5492">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5492">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-5493">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-5493">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-5494">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-5494">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-5495">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-5495">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5497">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-5497">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-5498">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-5498">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-5499">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-5499">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-5500">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-5500">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-5501">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-5501">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-5502">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-5502">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-5503">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-5503">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-5504">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-5504">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-5505">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5505">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-5506">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5506">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-5507">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5507">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5508">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-5508">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5509">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-5509">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-5510">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-5510">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-5511">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-5511">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5512">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-5512">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5513">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-5513">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-5514">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5514">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-5515">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5515">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-5516">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5516">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-5517">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-5517">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-5518">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-5518">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-5519">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5519">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-5520">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-5520">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5521">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-5521">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5522">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-5522">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5524">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5524">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5525">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-5525">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5526">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-5526">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-5527">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-5527">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-5528">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-5528">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-5529">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-5529">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-5530">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-5530">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-5531">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5531">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5533">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5533">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5535">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5535">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5537">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-5537">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-5538">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-5538">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="92888-5539">DXGI_FORMAT_Y216<sup>V</sup> (109)</span><span class="sxs-lookup"><span data-stu-id="92888-5539">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="92888-5540">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-5540">Target</span></span> | <span data-ttu-id="92888-5541">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-5541">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-5542">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-5542">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-5543">32</span><span class="sxs-lookup"><span data-stu-id="92888-5543">32</span></span> |
| <span data-ttu-id="92888-5544">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-5544">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5546">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-5546">Buffer</span></span> | \- |
| <span data-ttu-id="92888-5547">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5547">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-5548">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5548">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-5549">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-5549">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-5550">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-5550">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-5551">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-5551">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5553">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-5553">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-5554">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-5554">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-5555">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-5555">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-5556">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-5556">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-5557">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-5557">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-5558">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-5558">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-5559">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-5559">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-5560">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-5560">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-5561">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5561">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-5562">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5562">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-5563">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5563">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5564">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-5564">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5565">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-5565">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-5566">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-5566">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-5567">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-5567">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5568">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-5568">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5569">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-5569">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-5570">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5570">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-5571">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5571">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-5572">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5572">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-5573">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-5573">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-5574">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-5574">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-5575">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5575">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-5576">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-5576">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5577">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-5577">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5578">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-5578">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5580">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5580">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5581">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-5581">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5582">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-5582">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-5583">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-5583">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-5584">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-5584">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-5585">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-5585">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-5586">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-5586">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-5587">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5587">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5589">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5589">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5591">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5591">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5593">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-5593">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-5594">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-5594">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="92888-5595">DXGI_FORMAT_NV11<sup>V</sup> (110)</span><span class="sxs-lookup"><span data-stu-id="92888-5595">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="92888-5596">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-5596">Target</span></span> | <span data-ttu-id="92888-5597">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-5597">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-5598">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-5598">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-5599">8</span><span class="sxs-lookup"><span data-stu-id="92888-5599">8</span></span> |
| <span data-ttu-id="92888-5600">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-5600">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5602">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-5602">Buffer</span></span> | \- |
| <span data-ttu-id="92888-5603">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5603">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-5604">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5604">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-5605">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-5605">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-5606">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-5606">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-5607">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-5607">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5609">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-5609">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-5610">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-5610">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-5611">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-5611">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-5612">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-5612">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-5613">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-5613">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-5614">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-5614">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-5615">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-5615">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-5616">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-5616">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-5617">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5617">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-5618">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5618">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-5619">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5619">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5620">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-5620">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5621">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-5621">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-5622">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-5622">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-5623">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-5623">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5624">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-5624">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5625">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-5625">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-5626">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5626">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-5627">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5627">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-5628">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5628">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-5629">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-5629">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-5630">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-5630">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-5631">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5631">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-5632">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-5632">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5633">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-5633">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5634">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-5634">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5636">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5636">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5637">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-5637">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5638">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-5638">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-5639">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-5639">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-5640">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-5640">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-5641">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-5641">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-5642">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-5642">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-5643">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5643">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5645">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5645">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5647">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5647">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5649">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-5649">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-5650">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-5650">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="92888-5651">DXGI_FORMAT_AI44<sup>V</sup> (111)</span><span class="sxs-lookup"><span data-stu-id="92888-5651">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="92888-5652">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-5652">Target</span></span> | <span data-ttu-id="92888-5653">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-5653">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-5654">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-5654">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-5655">8</span><span class="sxs-lookup"><span data-stu-id="92888-5655">8</span></span> |
| <span data-ttu-id="92888-5656">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-5656">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5658">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-5658">Buffer</span></span> | \- |
| <span data-ttu-id="92888-5659">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5659">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-5660">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5660">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-5661">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-5661">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-5662">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-5662">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-5663">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-5663">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5665">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-5665">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-5666">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-5666">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-5667">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-5667">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-5668">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-5668">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-5669">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-5669">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-5670">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-5670">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-5671">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-5671">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-5672">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-5672">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-5673">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5673">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-5674">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5674">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-5675">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5675">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5676">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-5676">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5677">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-5677">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-5678">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-5678">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-5679">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-5679">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5680">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-5680">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5681">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-5681">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-5682">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5682">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-5683">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5683">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-5684">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5684">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-5685">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-5685">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-5686">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-5686">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-5687">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5687">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-5688">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-5688">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5689">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-5689">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5690">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-5690">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5692">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5692">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5693">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-5693">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5694">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-5694">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-5695">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-5695">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-5696">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-5696">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-5697">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-5697">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-5698">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-5698">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-5699">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5699">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-5700">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5700">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5702">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5702">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-5703">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-5703">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-5704">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-5704">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="92888-5705">DXGI_FORMAT_IA44<sup>V</sup> (112)</span><span class="sxs-lookup"><span data-stu-id="92888-5705">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="92888-5706">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-5706">Target</span></span> | <span data-ttu-id="92888-5707">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-5707">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-5708">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-5708">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-5709">8</span><span class="sxs-lookup"><span data-stu-id="92888-5709">8</span></span> |
| <span data-ttu-id="92888-5710">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-5710">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5712">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-5712">Buffer</span></span> | \- |
| <span data-ttu-id="92888-5713">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5713">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-5714">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5714">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-5715">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-5715">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-5716">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-5716">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-5717">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-5717">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5719">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-5719">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-5720">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-5720">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-5721">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-5721">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-5722">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-5722">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-5723">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-5723">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-5724">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-5724">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-5725">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-5725">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-5726">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-5726">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-5727">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5727">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-5728">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5728">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-5729">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5729">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5730">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-5730">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5731">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-5731">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-5732">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-5732">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-5733">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-5733">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5734">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-5734">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5735">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-5735">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-5736">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5736">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-5737">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5737">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-5738">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5738">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-5739">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-5739">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-5740">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-5740">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-5741">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5741">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-5742">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-5742">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5743">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-5743">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5744">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-5744">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5746">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5746">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5747">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-5747">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5748">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-5748">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-5749">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-5749">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-5750">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-5750">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-5751">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-5751">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-5752">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-5752">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-5753">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5753">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-5754">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5754">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5756">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5756">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-5757">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-5757">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-5758">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-5758">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="92888-5759">DXGI_FORMAT_P8<sup>V</sup> (113)</span><span class="sxs-lookup"><span data-stu-id="92888-5759">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="92888-5760">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-5760">Target</span></span> | <span data-ttu-id="92888-5761">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-5761">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-5762">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-5762">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-5763">8</span><span class="sxs-lookup"><span data-stu-id="92888-5763">8</span></span> |
| <span data-ttu-id="92888-5764">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-5764">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5766">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-5766">Buffer</span></span> | \- |
| <span data-ttu-id="92888-5767">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5767">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-5768">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5768">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-5769">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-5769">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-5770">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-5770">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-5771">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-5771">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5773">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-5773">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-5774">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-5774">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-5775">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-5775">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-5776">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-5776">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-5777">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-5777">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-5778">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-5778">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-5779">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-5779">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-5780">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-5780">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-5781">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5781">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-5782">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5782">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-5783">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5783">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5784">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-5784">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5785">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-5785">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-5786">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-5786">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-5787">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-5787">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5788">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-5788">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5789">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-5789">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-5790">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5790">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-5791">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5791">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-5792">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5792">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-5793">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-5793">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-5794">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-5794">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-5795">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5795">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-5796">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-5796">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5797">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-5797">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5798">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-5798">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5800">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5800">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5801">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-5801">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5802">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-5802">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-5803">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-5803">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-5804">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-5804">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-5805">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-5805">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-5806">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-5806">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-5807">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5807">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-5808">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5808">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5810">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5810">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-5811">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-5811">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-5812">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-5812">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="92888-5813">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span><span class="sxs-lookup"><span data-stu-id="92888-5813">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="92888-5814">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-5814">Target</span></span> | <span data-ttu-id="92888-5815">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-5815">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-5816">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-5816">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-5817">16</span><span class="sxs-lookup"><span data-stu-id="92888-5817">16</span></span> |
| <span data-ttu-id="92888-5818">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-5818">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="92888-5820">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-5820">Buffer</span></span> | \- |
| <span data-ttu-id="92888-5821">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5821">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-5822">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5822">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-5823">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-5823">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-5824">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-5824">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-5825">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-5825">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5827">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-5827">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-5828">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-5828">TextureCube</span></span> | \- |
| <span data-ttu-id="92888-5829">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-5829">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="92888-5830">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-5830">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="92888-5831">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-5831">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-5832">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-5832">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-5833">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-5833">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-5834">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-5834">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-5835">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5835">Mipmap</span></span> | \- |
| <span data-ttu-id="92888-5836">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5836">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-5837">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5837">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5838">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-5838">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5839">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-5839">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-5840">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-5840">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-5841">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-5841">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5842">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-5842">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5843">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-5843">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-5844">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5844">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-5845">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5845">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-5846">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5846">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-5847">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-5847">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-5848">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-5848">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-5849">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5849">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-5850">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-5850">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5851">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-5851">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5852">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-5852">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5854">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5854">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5855">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-5855">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5856">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-5856">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-5857">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-5857">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-5858">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-5858">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-5859">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-5859">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-5860">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-5860">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-5861">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5861">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-5862">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5862">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5864">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5864">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-5865">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-5865">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-5866">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-5866">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a><span data-ttu-id="92888-5867">DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>FNS</sup> (115)</span><span class="sxs-lookup"><span data-stu-id="92888-5867">DXGI_FORMAT_B4G4R4A4\_UNORM<sup>FNS</sup> (115)</span></span>
| <span data-ttu-id="92888-5868">Destino</span><span class="sxs-lookup"><span data-stu-id="92888-5868">Target</span></span> | <span data-ttu-id="92888-5869">Suporte</span><span class="sxs-lookup"><span data-stu-id="92888-5869">Support</span></span> |
| - | - |
| <span data-ttu-id="92888-5870">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="92888-5870">Bits Per Element (BPE)</span></span> | <span data-ttu-id="92888-5871">16</span><span class="sxs-lookup"><span data-stu-id="92888-5871">16</span></span> |
| <span data-ttu-id="92888-5872">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="92888-5872">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5874">Buffer</span><span class="sxs-lookup"><span data-stu-id="92888-5874">Buffer</span></span> | \- |
| <span data-ttu-id="92888-5875">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5875">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="92888-5876">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="92888-5876">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="92888-5877">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="92888-5877">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="92888-5878">Texture1D</span><span class="sxs-lookup"><span data-stu-id="92888-5878">Texture1D</span></span> | \- |
| <span data-ttu-id="92888-5879">Texture2D</span><span class="sxs-lookup"><span data-stu-id="92888-5879">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5881">Texture3D</span><span class="sxs-lookup"><span data-stu-id="92888-5881">Texture3D</span></span> | \- |
| <span data-ttu-id="92888-5882">TextureCube</span><span class="sxs-lookup"><span data-stu-id="92888-5882">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5884">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="92888-5884">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5886">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="92888-5886">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5888">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="92888-5888">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="92888-5889">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="92888-5889">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="92888-5890">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="92888-5890">Shader gather4</span></span> | \- |
| <span data-ttu-id="92888-5891">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="92888-5891">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="92888-5892">Mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5892">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5894">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="92888-5894">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="92888-5895">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5895">RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5896">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="92888-5896">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5897">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="92888-5897">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="92888-5898">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="92888-5898">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="92888-5899">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="92888-5899">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5900">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="92888-5900">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="92888-5901">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="92888-5901">Typed UAV</span></span> | \- |
| <span data-ttu-id="92888-5902">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5902">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="92888-5903">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5903">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="92888-5904">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5904">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="92888-5905">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="92888-5905">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="92888-5906">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="92888-5906">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="92888-5907">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="92888-5907">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="92888-5908">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="92888-5908">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5909">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="92888-5909">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="92888-5910">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="92888-5910">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="92888-5912">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="92888-5912">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5913">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="92888-5913">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="92888-5914">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="92888-5914">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="92888-5915">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="92888-5915">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="92888-5916">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="92888-5916">Multisample Load</span></span> | \- |
| <span data-ttu-id="92888-5917">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="92888-5917">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="92888-5918">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="92888-5918">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="92888-5919">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5919">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="92888-5920">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5920">Video Processor Input</span></span> | \- |
| <span data-ttu-id="92888-5921">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5921">Video Processor Output</span></span> | \- |
| <span data-ttu-id="92888-5922">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="92888-5922">Shared Resource</span></span> | \- |
| <span data-ttu-id="92888-5923">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="92888-5923">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="92888-5924">Observações de formato</span><span class="sxs-lookup"><span data-stu-id="92888-5924">Format notes</span></span>

<span data-ttu-id="92888-5925">A finalidade do formato pode mudar de um nível de recurso de hardware para o próximo.</span><span class="sxs-lookup"><span data-stu-id="92888-5925">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="92888-5926"><sup>L</sup> : formato de tipo informativo</span><span class="sxs-lookup"><span data-stu-id="92888-5926"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="92888-5927"><sup>PCs</sup> : layout de tipo parcial, convertido e simples</span><span class="sxs-lookup"><span data-stu-id="92888-5927"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="92888-5928"><sup>FCS</sup> : layout totalmente tipado, convertido e simples</span><span class="sxs-lookup"><span data-stu-id="92888-5928"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="92888-5929"><sup>FNS</sup> : layout totalmente tipado, não-convertido e simples</span><span class="sxs-lookup"><span data-stu-id="92888-5929"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="92888-5930"><sup>PCC</sup> : layout complexo, convertido e de tipo parcial</span><span class="sxs-lookup"><span data-stu-id="92888-5930"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="92888-5931"><sup>FCC</sup> : layout totalmente tipado, convertido e complexo</span><span class="sxs-lookup"><span data-stu-id="92888-5931"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="92888-5932"><sup>FNC</sup> : layout totalmente tipado, não-convertido e complexo</span><span class="sxs-lookup"><span data-stu-id="92888-5932"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="92888-5933"><sup>V</sup> : formato de vídeo</span><span class="sxs-lookup"><span data-stu-id="92888-5933"><sup>V</sup> : video format</span></span>
</dt> </dl>

## <a name="related-topics"></a><span data-ttu-id="92888-5934">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="92888-5934">Related topics</span></span>

[<span data-ttu-id="92888-5935">Níveis de recursos de hardware do D3D12</span><span class="sxs-lookup"><span data-stu-id="92888-5935">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

<span data-ttu-id="92888-5936">[Implementando buffers de sombra para o nível de recurso do Direct3D 9](/previous-versions/windows/apps/jj262110(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="92888-5936">[Implementing shadow buffers for Direct3D feature level 9](/previous-versions/windows/apps/jj262110(v=win.10))</span></span>

[<span data-ttu-id="92888-5937">Mapeando formatos herdados</span><span class="sxs-lookup"><span data-stu-id="92888-5937">Mapping Legacy Formats</span></span>](../direct3d10/d3d10-graphics-programming-guide-resources-legacy-formats.md)

[<span data-ttu-id="92888-5938">Guia de programação para DXGI</span><span class="sxs-lookup"><span data-stu-id="92888-5938">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
