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
# <a name="format-support-for-direct3d-feature-10level9-91-hardware"></a><span data-ttu-id="bf787-103">Suporte de formato para hardware 9.1 do Nível de 10Recursos9 do Direct3D</span><span class="sxs-lookup"><span data-stu-id="bf787-103">Format support for Direct3D Feature 10Level9 9.1 hardware</span></span>

<span data-ttu-id="bf787-104">Esta seção especifica os formatos ([_\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valores) que têm suporte no hardware do recurso Direct3D 10Level9 9,1.</span><span class="sxs-lookup"><span data-stu-id="bf787-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature 10Level9 9.1 hardware.</span></span>

<span data-ttu-id="bf787-105">A tabela resume o suporte a recursos, usando a chave a seguir.</span><span class="sxs-lookup"><span data-stu-id="bf787-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="bf787-106">Símbolo</span><span class="sxs-lookup"><span data-stu-id="bf787-106">Symbol</span></span>                            | <span data-ttu-id="bf787-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf787-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="bf787-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="bf787-108">_ *-*\*</span></span>                             | <span data-ttu-id="bf787-109">Não permitido ou não disponível.</span><span class="sxs-lookup"><span data-stu-id="bf787-109">Disallowed or not available.</span></span>                                                  |
| ![exigido](images/letter-r.jpg)  | <span data-ttu-id="bf787-111">O suporte a hardware é necessário.</span><span class="sxs-lookup"><span data-stu-id="bf787-111">Hardware support is required.</span></span>                                                 |
| ![opcionais](images/letter-o.jpg)  | <span data-ttu-id="bf787-113">Suporte a hardware opcional, o formato pode ou não ser acelerado por hardware.</span><span class="sxs-lookup"><span data-stu-id="bf787-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![dependentes](images/letter-d.jpg) | <span data-ttu-id="bf787-115">Necessário se houver suporte para o recurso opcional relacionado.</span><span class="sxs-lookup"><span data-stu-id="bf787-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="bf787-116">Este tópico contém uma seção por formato.</span><span class="sxs-lookup"><span data-stu-id="bf787-116">This topic contains a section per format.</span></span> <span data-ttu-id="bf787-117">Um *destino* de formato (as tabelas contêm uma linha por destino) pode ser um tipo de recurso, uma função intrínseca HLSL ou uma funcionalidade específica que depende de um formato específico.</span><span class="sxs-lookup"><span data-stu-id="bf787-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="bf787-118">Para verificar programaticamente o suporte a Format em D3D11 e D3D12, consulte [verificando o suporte a recursos de hardware](checking-hardware-feature-support.md).</span><span class="sxs-lookup"><span data-stu-id="bf787-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="bf787-119">Os números dos formatos são principalmente, mas nem todos, em ordem numérica crescente &mdash; alguns estão fora de ordem numérica e listados junto com outros formatos relevantes.</span><span class="sxs-lookup"><span data-stu-id="bf787-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="bf787-120">Observe também que sem *tipo* em um nome de formato pode significar digitação *parcial* e não estritamente tipado (consulte a seção [observações de formato](#format-notes) no final do tópico).</span><span class="sxs-lookup"><span data-stu-id="bf787-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>

// 

## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="bf787-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span><span class="sxs-lookup"><span data-stu-id="bf787-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="bf787-122">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-122">Target</span></span> | <span data-ttu-id="bf787-123">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-123">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-124">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-125">0</span><span class="sxs-lookup"><span data-stu-id="bf787-125">0</span></span> |
| <span data-ttu-id="bf787-126">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-126">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-127">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-127">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-128">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-128">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-129">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-129">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-130">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-130">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-131">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-131">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-132">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-132">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-133">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-133">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-134">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-134">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-135">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-135">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-136">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-136">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-137">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-137">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-138">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-138">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-139">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-139">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-140">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-140">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-141">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-141">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-142">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-142">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-143">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-143">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-144">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-144">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-145">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-145">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-146">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-146">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-147">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-147">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-148">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-148">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-149">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-149">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-150">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-150">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-151">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-151">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-152">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-152">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-153">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-153">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-154">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-154">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-155">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-155">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-156">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-156">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-157">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-157">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-158">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-158">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-159">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-159">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-160">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-160">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-161">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-161">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-162">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-162">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-163">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-163">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-164">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-164">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-165">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-165">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-166">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-166">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-167">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-167">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-168">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-168">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-169">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-169">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-170">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-170">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="bf787-171">DXGI_FORMAT_R32G32B32A32 \_ <sup>PCs</sup> não tipados (1)</span><span class="sxs-lookup"><span data-stu-id="bf787-171">DXGI_FORMAT_R32G32B32A32\_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="bf787-172">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-172">Target</span></span> | <span data-ttu-id="bf787-173">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-173">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-174">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-174">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-175">128</span><span class="sxs-lookup"><span data-stu-id="bf787-175">128</span></span> |
| <span data-ttu-id="bf787-176">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-176">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-177">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-177">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-178">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-178">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-179">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-179">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-180">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-180">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-181">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-181">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-182">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-182">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-183">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-183">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-184">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-184">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-185">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-185">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-186">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-186">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-187">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-187">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-188">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-188">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-189">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-189">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-190">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-190">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-191">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-191">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-192">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-192">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-193">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-193">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-194">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-194">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-195">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-195">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-196">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-196">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-197">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-197">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-198">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-198">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-199">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-199">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-200">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-200">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-201">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-201">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-202">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-202">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-203">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-203">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-204">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-204">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-205">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-205">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-206">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-206">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-207">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-207">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-208">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-208">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-209">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-209">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-210">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-210">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-211">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-211">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-212">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-212">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-213">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-213">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-214">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-214">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-215">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-215">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-216">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-216">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-217">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-217">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-218">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-218">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-219">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-219">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-220">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-220">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfnssup-2"></a><span data-ttu-id="bf787-221">DXGI_FORMAT_R32G32B32A32 \_ float<sup>FNS</sup> (2)</span><span class="sxs-lookup"><span data-stu-id="bf787-221">DXGI_FORMAT_R32G32B32A32\_FLOAT<sup>FNS</sup> (2)</span></span>
| <span data-ttu-id="bf787-222">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-222">Target</span></span> | <span data-ttu-id="bf787-223">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-223">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-224">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-224">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-225">128</span><span class="sxs-lookup"><span data-stu-id="bf787-225">128</span></span> |
| <span data-ttu-id="bf787-226">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-226">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-228">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-228">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-229">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-229">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-231">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-231">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-232">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-232">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-233">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-233">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-234">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-234">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-235">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-235">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-236">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-236">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-237">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-237">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-238">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-238">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-239">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-239">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-240">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-240">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-241">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-241">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-242">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-242">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-243">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-243">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-244">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-244">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-245">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-245">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-246">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-246">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-247">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-247">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-248">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-248">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-249">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-249">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-250">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-250">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-251">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-251">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-252">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-252">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-253">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-253">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-254">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-254">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-255">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-255">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-256">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-256">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-257">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-257">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-258">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-258">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-259">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-259">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-260">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-260">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-261">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-261">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-262">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-262">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-263">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-263">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-264">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-264">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-265">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-265">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-266">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-266">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-267">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-267">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-268">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-268">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-269">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-269">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-270">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-270">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-271">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-271">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-272">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-272">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfnssup-3"></a><span data-ttu-id="bf787-273">DXGI_FORMAT_R32G32B32A32 \_ uint<sup>FNS</sup> (3)</span><span class="sxs-lookup"><span data-stu-id="bf787-273">DXGI_FORMAT_R32G32B32A32\_UINT<sup>FNS</sup> (3)</span></span>
| <span data-ttu-id="bf787-274">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-274">Target</span></span> | <span data-ttu-id="bf787-275">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-275">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-276">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-276">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-277">128</span><span class="sxs-lookup"><span data-stu-id="bf787-277">128</span></span> |
| <span data-ttu-id="bf787-278">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-278">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-279">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-279">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-280">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-280">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-281">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-281">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-282">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-282">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-283">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-283">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-284">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-284">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-285">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-285">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-286">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-286">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-287">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-287">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-288">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-288">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-289">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-289">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-290">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-290">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-291">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-291">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-292">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-292">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-293">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-293">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-294">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-294">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-295">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-295">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-296">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-296">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-297">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-297">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-298">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-298">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-299">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-299">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-300">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-300">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-301">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-301">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-302">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-302">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-303">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-303">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-304">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-304">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-305">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-305">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-306">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-306">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-307">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-307">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-308">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-308">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-309">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-309">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-310">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-310">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-311">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-311">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-312">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-312">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-313">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-313">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-314">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-314">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-315">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-315">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-316">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-316">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-317">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-317">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-318">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-318">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-319">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-319">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-320">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-320">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-321">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-321">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-322">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-322">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfnssup-4"></a><span data-ttu-id="bf787-323">DXGI_FORMAT_R32G32B32A32 \_ Santo<sup>FNS</sup> (4)</span><span class="sxs-lookup"><span data-stu-id="bf787-323">DXGI_FORMAT_R32G32B32A32\_SINT<sup>FNS</sup> (4)</span></span>
| <span data-ttu-id="bf787-324">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-324">Target</span></span> | <span data-ttu-id="bf787-325">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-325">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-326">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-326">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-327">128</span><span class="sxs-lookup"><span data-stu-id="bf787-327">128</span></span> |
| <span data-ttu-id="bf787-328">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-328">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-329">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-329">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-330">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-330">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-331">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-331">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-332">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-332">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-333">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-333">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-334">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-334">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-335">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-335">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-336">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-336">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-337">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-337">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-338">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-338">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-339">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-339">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-340">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-340">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-341">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-341">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-342">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-342">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-343">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-343">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-344">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-344">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-345">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-345">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-346">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-346">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-347">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-347">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-348">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-348">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-349">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-349">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-350">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-350">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-351">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-351">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-352">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-352">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-353">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-353">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-354">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-354">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-355">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-355">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-356">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-356">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-357">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-357">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-358">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-358">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-359">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-359">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-360">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-360">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-361">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-361">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-362">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-362">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-363">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-363">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-364">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-364">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-365">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-365">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-366">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-366">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-367">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-367">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-368">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-368">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-369">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-369">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-370">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-370">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-371">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-371">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-372">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-372">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="bf787-373">DXGI_FORMAT_R32G32B32 \_ <sup>PCs</sup> não tipados (5)</span><span class="sxs-lookup"><span data-stu-id="bf787-373">DXGI_FORMAT_R32G32B32\_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="bf787-374">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-374">Target</span></span> | <span data-ttu-id="bf787-375">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-375">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-376">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-376">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-377">96</span><span class="sxs-lookup"><span data-stu-id="bf787-377">96</span></span> |
| <span data-ttu-id="bf787-378">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-378">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-379">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-379">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-380">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-380">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-381">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-381">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-382">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-382">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-383">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-383">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-384">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-384">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-385">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-385">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-386">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-386">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-387">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-387">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-388">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-388">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-389">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-389">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-390">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-390">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-391">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-391">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-392">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-392">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-393">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-393">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-394">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-394">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-395">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-395">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-396">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-396">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-397">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-397">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-398">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-398">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-399">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-399">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-400">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-400">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-401">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-401">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-402">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-402">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-403">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-403">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-404">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-404">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-405">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-405">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-406">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-406">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-407">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-407">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-408">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-408">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-409">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-409">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-410">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-410">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-411">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-411">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-412">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-412">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-413">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-413">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-414">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-414">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-415">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-415">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-416">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-416">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-417">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-417">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-418">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-418">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-419">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-419">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-420">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-420">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-421">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-421">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-422">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-422">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfnssup-6"></a><span data-ttu-id="bf787-423">DXGI_FORMAT_R32G32B32 \_ float<sup>FNS</sup> (6)</span><span class="sxs-lookup"><span data-stu-id="bf787-423">DXGI_FORMAT_R32G32B32\_FLOAT<sup>FNS</sup> (6)</span></span>
| <span data-ttu-id="bf787-424">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-424">Target</span></span> | <span data-ttu-id="bf787-425">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-425">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-426">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-426">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-427">96</span><span class="sxs-lookup"><span data-stu-id="bf787-427">96</span></span> |
| <span data-ttu-id="bf787-428">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-428">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-430">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-430">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-431">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-431">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-433">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-433">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-434">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-434">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-435">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-435">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-436">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-436">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-437">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-437">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-438">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-438">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-439">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-439">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-440">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-440">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-441">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-441">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-442">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-442">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-443">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-443">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-444">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-444">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-445">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-445">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-446">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-446">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-447">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-447">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-448">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-448">Blendable RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="bf787-450">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-450">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-451">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-451">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-452">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-452">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-453">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-453">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-454">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-454">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-455">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-455">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-456">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-456">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-457">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-457">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-458">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-458">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-459">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-459">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-460">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-460">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-461">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-461">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-462">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-462">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-463">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-463">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-464">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-464">4x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="bf787-466">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-466">8x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="bf787-468">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-468">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-469">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-469">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-470">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-470">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-471">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-471">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-472">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-472">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-473">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-473">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-474">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-474">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-475">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-475">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-476">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-476">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-477">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-477">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfnssup-7"></a><span data-ttu-id="bf787-478">DXGI_FORMAT_R32G32B32 \_ uint<sup>FNS</sup> (7)</span><span class="sxs-lookup"><span data-stu-id="bf787-478">DXGI_FORMAT_R32G32B32\_UINT<sup>FNS</sup> (7)</span></span>
| <span data-ttu-id="bf787-479">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-479">Target</span></span> | <span data-ttu-id="bf787-480">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-480">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-481">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-481">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-482">96</span><span class="sxs-lookup"><span data-stu-id="bf787-482">96</span></span> |
| <span data-ttu-id="bf787-483">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-483">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-484">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-484">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-485">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-485">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-486">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-486">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-487">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-487">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-488">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-488">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-489">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-489">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-490">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-490">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-491">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-491">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-492">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-492">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-493">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-493">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-494">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-494">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-495">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-495">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-496">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-496">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-497">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-497">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-498">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-498">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-499">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-499">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-500">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-500">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-501">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-501">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-502">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-502">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-503">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-503">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-504">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-504">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-505">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-505">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-506">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-506">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-507">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-507">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-508">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-508">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-509">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-509">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-510">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-510">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-511">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-511">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-512">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-512">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-513">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-513">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-514">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-514">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-515">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-515">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-516">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-516">4x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="bf787-518">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-518">8x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="bf787-520">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-520">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-521">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-521">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-522">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-522">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-523">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-523">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-524">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-524">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-525">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-525">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-526">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-526">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-527">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-527">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-528">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-528">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-529">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-529">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfnssup-8"></a><span data-ttu-id="bf787-530">DXGI_FORMAT_R32G32B32 \_ Santo<sup>FNS</sup> (8)</span><span class="sxs-lookup"><span data-stu-id="bf787-530">DXGI_FORMAT_R32G32B32\_SINT<sup>FNS</sup> (8)</span></span>
| <span data-ttu-id="bf787-531">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-531">Target</span></span> | <span data-ttu-id="bf787-532">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-532">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-533">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-533">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-534">96</span><span class="sxs-lookup"><span data-stu-id="bf787-534">96</span></span> |
| <span data-ttu-id="bf787-535">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-535">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-536">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-536">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-537">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-537">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-538">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-538">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-539">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-539">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-540">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-540">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-541">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-541">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-542">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-542">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-543">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-543">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-544">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-544">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-545">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-545">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-546">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-546">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-547">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-547">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-548">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-548">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-549">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-549">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-550">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-550">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-551">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-551">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-552">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-552">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-553">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-553">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-554">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-554">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-555">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-555">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-556">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-556">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-557">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-557">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-558">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-558">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-559">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-559">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-560">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-560">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-561">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-561">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-562">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-562">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-563">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-563">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-564">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-564">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-565">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-565">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-566">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-566">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-567">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-567">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-568">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-568">4x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="bf787-570">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-570">8x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="bf787-572">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-572">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-573">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-573">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-574">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-574">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-575">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-575">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-576">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-576">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-577">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-577">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-578">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-578">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-579">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-579">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-580">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-580">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-581">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-581">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="bf787-582">DXGI_FORMAT_R16G16B16A16 \_ <sup>PCs</sup> não tipados (9)</span><span class="sxs-lookup"><span data-stu-id="bf787-582">DXGI_FORMAT_R16G16B16A16\_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="bf787-583">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-583">Target</span></span> | <span data-ttu-id="bf787-584">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-584">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-585">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-585">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-586">64</span><span class="sxs-lookup"><span data-stu-id="bf787-586">64</span></span> |
| <span data-ttu-id="bf787-587">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-587">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-588">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-588">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-589">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-589">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-590">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-590">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-591">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-591">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-592">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-592">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-593">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-593">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-594">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-594">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-595">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-595">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-596">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-596">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-597">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-597">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-598">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-598">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-599">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-599">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-600">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-600">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-601">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-601">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-602">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-602">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-603">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-603">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-604">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-604">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-605">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-605">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-606">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-606">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-607">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-607">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-608">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-608">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-609">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-609">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-610">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-610">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-611">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-611">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-612">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-612">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-613">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-613">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-614">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-614">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-615">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-615">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-616">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-616">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-617">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-617">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-618">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-618">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-619">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-619">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-620">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-620">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-621">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-621">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-622">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-622">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-623">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-623">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-624">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-624">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-625">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-625">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-626">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-626">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-627">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-627">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-628">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-628">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-629">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-629">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-630">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-630">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-631">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-631">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfnssup-10"></a><span data-ttu-id="bf787-632">DXGI_FORMAT_R16G16B16A16 \_ float<sup>FNS</sup> (10)</span><span class="sxs-lookup"><span data-stu-id="bf787-632">DXGI_FORMAT_R16G16B16A16\_FLOAT<sup>FNS</sup> (10)</span></span>
| <span data-ttu-id="bf787-633">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-633">Target</span></span> | <span data-ttu-id="bf787-634">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-634">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-635">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-635">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-636">64</span><span class="sxs-lookup"><span data-stu-id="bf787-636">64</span></span> |
| <span data-ttu-id="bf787-637">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-637">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-638">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-638">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-639">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-639">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-640">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-640">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-641">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-641">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-642">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-642">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-643">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-643">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-644">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-644">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-645">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-645">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-646">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-646">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-647">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-647">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-648">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-648">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-649">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-649">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-650">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-650">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-651">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-651">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-652">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-652">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-653">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-653">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-654">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-654">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-655">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-655">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-656">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-656">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-657">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-657">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-658">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-658">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-659">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-659">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-660">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-660">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-661">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-661">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-662">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-662">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-663">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-663">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-664">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-664">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-665">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-665">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-666">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-666">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-667">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-667">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-668">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-668">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-669">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-669">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-670">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-670">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-671">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-671">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-672">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-672">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-673">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-673">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-674">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-674">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-675">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-675">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-676">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-676">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-677">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-677">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-678">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-678">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-679">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-679">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-680">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-680">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-682">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-682">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfnssup-11"></a><span data-ttu-id="bf787-683">DXGI_FORMAT_R16G16B16A16 \_ UNORM<sup>FNS</sup> (11)</span><span class="sxs-lookup"><span data-stu-id="bf787-683">DXGI_FORMAT_R16G16B16A16\_UNORM<sup>FNS</sup> (11)</span></span>
| <span data-ttu-id="bf787-684">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-684">Target</span></span> | <span data-ttu-id="bf787-685">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-685">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-686">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-686">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-687">64</span><span class="sxs-lookup"><span data-stu-id="bf787-687">64</span></span> |
| <span data-ttu-id="bf787-688">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-688">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-689">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-689">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-690">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-690">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-691">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-691">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-692">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-692">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-693">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-693">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-694">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-694">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-695">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-695">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-696">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-696">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-697">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-697">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-698">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-698">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-699">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-699">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-700">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-700">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-701">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-701">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-702">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-702">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-703">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-703">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-704">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-704">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-705">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-705">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-706">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-706">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-707">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-707">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-708">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-708">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-709">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-709">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-710">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-710">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-711">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-711">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-712">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-712">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-713">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-713">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-714">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-714">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-715">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-715">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-716">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-716">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-717">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-717">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-718">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-718">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-719">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-719">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-720">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-720">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-721">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-721">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-722">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-722">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-723">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-723">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-724">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-724">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-725">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-725">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-726">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-726">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-727">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-727">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-728">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-728">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-729">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-729">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-730">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-730">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-731">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-731">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-732">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-732">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfnssup-12"></a><span data-ttu-id="bf787-733">DXGI_FORMAT_R16G16B16A16 \_ uint<sup>FNS</sup> (12)</span><span class="sxs-lookup"><span data-stu-id="bf787-733">DXGI_FORMAT_R16G16B16A16\_UINT<sup>FNS</sup> (12)</span></span>
| <span data-ttu-id="bf787-734">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-734">Target</span></span> | <span data-ttu-id="bf787-735">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-735">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-736">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-736">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-737">64</span><span class="sxs-lookup"><span data-stu-id="bf787-737">64</span></span> |
| <span data-ttu-id="bf787-738">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-738">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-739">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-739">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-740">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-740">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-741">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-741">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-742">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-742">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-743">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-743">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-744">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-744">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-745">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-745">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-746">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-746">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-747">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-747">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-748">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-748">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-749">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-749">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-750">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-750">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-751">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-751">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-752">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-752">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-753">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-753">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-754">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-754">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-755">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-755">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-756">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-756">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-757">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-757">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-758">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-758">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-759">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-759">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-760">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-760">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-761">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-761">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-762">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-762">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-763">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-763">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-764">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-764">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-765">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-765">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-766">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-766">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-767">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-767">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-768">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-768">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-769">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-769">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-770">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-770">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-771">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-771">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-772">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-772">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-773">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-773">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-774">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-774">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-775">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-775">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-776">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-776">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-777">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-777">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-778">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-778">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-779">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-779">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-780">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-780">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-781">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-781">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-782">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-782">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfnssup-13"></a><span data-ttu-id="bf787-783">DXGI_FORMAT_R16G16B16A16 \_ SNORM<sup>FNS</sup> (13)</span><span class="sxs-lookup"><span data-stu-id="bf787-783">DXGI_FORMAT_R16G16B16A16\_SNORM<sup>FNS</sup> (13)</span></span>
| <span data-ttu-id="bf787-784">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-784">Target</span></span> | <span data-ttu-id="bf787-785">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-785">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-786">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-786">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-787">64</span><span class="sxs-lookup"><span data-stu-id="bf787-787">64</span></span> |
| <span data-ttu-id="bf787-788">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-788">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-790">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-790">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-791">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-791">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-793">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-793">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-794">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-794">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-795">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-795">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-796">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-796">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-797">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-797">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-798">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-798">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-799">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-799">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-800">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-800">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-801">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-801">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-802">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-802">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-803">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-803">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-804">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-804">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-805">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-805">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-806">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-806">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-807">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-807">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-808">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-808">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-809">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-809">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-810">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-810">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-811">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-811">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-812">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-812">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-813">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-813">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-814">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-814">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-815">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-815">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-816">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-816">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-817">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-817">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-818">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-818">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-819">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-819">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-820">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-820">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-821">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-821">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-822">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-822">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-823">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-823">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-824">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-824">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-825">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-825">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-826">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-826">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-827">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-827">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-828">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-828">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-829">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-829">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-830">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-830">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-831">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-831">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-832">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-832">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-833">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-833">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-834">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-834">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfnssup-14"></a><span data-ttu-id="bf787-835">DXGI_FORMAT_R16G16B16A16 \_ Santo<sup>FNS</sup> (14)</span><span class="sxs-lookup"><span data-stu-id="bf787-835">DXGI_FORMAT_R16G16B16A16\_SINT<sup>FNS</sup> (14)</span></span>
| <span data-ttu-id="bf787-836">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-836">Target</span></span> | <span data-ttu-id="bf787-837">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-837">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-838">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-838">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-839">64</span><span class="sxs-lookup"><span data-stu-id="bf787-839">64</span></span> |
| <span data-ttu-id="bf787-840">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-840">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-842">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-842">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-843">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-843">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-845">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-845">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-846">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-846">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-847">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-847">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-848">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-848">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-849">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-849">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-850">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-850">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-851">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-851">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-852">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-852">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-853">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-853">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-854">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-854">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-855">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-855">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-856">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-856">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-857">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-857">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-858">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-858">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-859">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-859">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-860">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-860">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-861">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-861">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-862">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-862">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-863">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-863">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-864">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-864">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-865">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-865">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-866">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-866">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-867">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-867">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-868">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-868">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-869">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-869">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-870">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-870">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-871">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-871">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-872">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-872">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-873">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-873">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-874">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-874">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-875">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-875">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-876">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-876">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-877">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-877">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-878">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-878">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-879">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-879">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-880">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-880">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-881">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-881">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-882">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-882">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-883">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-883">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-884">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-884">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-885">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-885">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-886">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-886">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="bf787-887">DXGI_FORMAT_R32G32 \_ <sup>PCs</sup> não tipados (15)</span><span class="sxs-lookup"><span data-stu-id="bf787-887">DXGI_FORMAT_R32G32\_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="bf787-888">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-888">Target</span></span> | <span data-ttu-id="bf787-889">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-889">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-890">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-890">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-891">64</span><span class="sxs-lookup"><span data-stu-id="bf787-891">64</span></span> |
| <span data-ttu-id="bf787-892">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-892">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-893">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-893">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-894">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-894">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-895">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-895">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-896">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-896">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-897">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-897">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-898">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-898">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-899">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-899">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-900">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-900">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-901">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-901">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-902">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-902">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-903">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-903">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-904">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-904">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-905">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-905">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-906">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-906">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-907">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-907">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-908">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-908">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-909">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-909">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-910">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-910">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-911">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-911">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-912">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-912">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-913">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-913">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-914">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-914">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-915">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-915">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-916">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-916">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-917">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-917">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-918">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-918">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-919">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-919">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-920">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-920">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-921">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-921">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-922">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-922">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-923">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-923">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-924">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-924">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-925">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-925">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-926">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-926">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-927">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-927">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-928">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-928">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-929">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-929">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-930">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-930">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-931">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-931">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-932">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-932">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-933">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-933">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-934">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-934">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-935">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-935">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-936">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-936">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_floatsupfnssup-16"></a><span data-ttu-id="bf787-937">DXGI_FORMAT_R32G32 \_ float<sup>FNS</sup> (16)</span><span class="sxs-lookup"><span data-stu-id="bf787-937">DXGI_FORMAT_R32G32\_FLOAT<sup>FNS</sup> (16)</span></span>
| <span data-ttu-id="bf787-938">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-938">Target</span></span> | <span data-ttu-id="bf787-939">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-939">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-940">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-940">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-941">64</span><span class="sxs-lookup"><span data-stu-id="bf787-941">64</span></span> |
| <span data-ttu-id="bf787-942">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-942">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-944">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-944">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-945">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-945">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-947">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-947">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-948">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-948">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-949">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-949">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-950">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-950">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-951">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-951">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-952">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-952">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-953">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-953">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-954">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-954">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-955">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-955">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-956">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-956">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-957">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-957">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-958">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-958">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-959">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-959">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-960">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-960">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-961">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-961">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-962">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-962">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-963">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-963">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-964">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-964">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-965">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-965">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-966">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-966">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-967">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-967">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-968">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-968">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-969">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-969">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-970">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-970">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-971">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-971">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-972">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-972">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-973">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-973">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-974">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-974">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-975">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-975">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-976">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-976">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-977">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-977">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-978">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-978">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-979">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-979">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-980">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-980">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-981">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-981">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-982">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-982">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-983">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-983">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-984">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-984">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-985">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-985">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-986">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-986">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-987">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-987">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-988">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-988">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_uintsupfnssup-17"></a><span data-ttu-id="bf787-989">DXGI_FORMAT_R32G32 \_ uint<sup>FNS</sup> (17)</span><span class="sxs-lookup"><span data-stu-id="bf787-989">DXGI_FORMAT_R32G32\_UINT<sup>FNS</sup> (17)</span></span>
| <span data-ttu-id="bf787-990">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-990">Target</span></span> | <span data-ttu-id="bf787-991">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-991">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-992">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-992">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-993">64</span><span class="sxs-lookup"><span data-stu-id="bf787-993">64</span></span> |
| <span data-ttu-id="bf787-994">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-994">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-995">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-995">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-996">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-996">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-997">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-997">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-998">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-998">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-999">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-999">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-1000">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-1000">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-1001">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-1001">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-1002">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-1002">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-1003">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-1003">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-1004">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-1004">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-1005">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-1005">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-1006">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-1006">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-1007">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-1007">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-1008">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-1008">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-1009">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1009">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-1010">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1010">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-1011">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1011">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1012">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-1012">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1013">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-1013">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-1014">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-1014">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-1015">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-1015">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1016">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-1016">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1017">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-1017">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-1018">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1018">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-1019">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1019">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-1020">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1020">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-1021">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-1021">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-1022">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-1022">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-1023">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1023">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-1024">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-1024">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1025">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-1025">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1026">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-1026">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-1027">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1027">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1028">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-1028">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1029">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-1029">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-1030">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-1030">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-1031">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-1031">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-1032">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-1032">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-1033">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-1033">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-1034">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1034">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-1035">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1035">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-1036">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1036">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-1037">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-1037">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-1038">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-1038">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_sintsupfnssup-18"></a><span data-ttu-id="bf787-1039">DXGI_FORMAT_R32G32 \_ Santo<sup>FNS</sup> (18)</span><span class="sxs-lookup"><span data-stu-id="bf787-1039">DXGI_FORMAT_R32G32\_SINT<sup>FNS</sup> (18)</span></span>
| <span data-ttu-id="bf787-1040">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-1040">Target</span></span> | <span data-ttu-id="bf787-1041">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-1041">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-1042">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-1042">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-1043">64</span><span class="sxs-lookup"><span data-stu-id="bf787-1043">64</span></span> |
| <span data-ttu-id="bf787-1044">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-1044">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-1045">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-1045">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1046">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1046">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1047">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1047">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1048">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-1048">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1049">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-1049">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-1050">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-1050">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-1051">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-1051">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-1052">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-1052">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-1053">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-1053">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-1054">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-1054">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-1055">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-1055">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-1056">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-1056">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-1057">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-1057">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-1058">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-1058">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-1059">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1059">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-1060">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1060">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-1061">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1061">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1062">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-1062">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1063">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-1063">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-1064">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-1064">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-1065">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-1065">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1066">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-1066">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1067">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-1067">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-1068">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1068">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-1069">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1069">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-1070">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1070">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-1071">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-1071">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-1072">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-1072">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-1073">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1073">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-1074">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-1074">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1075">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-1075">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1076">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-1076">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-1077">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1077">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1078">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-1078">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1079">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-1079">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-1080">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-1080">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-1081">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-1081">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-1082">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-1082">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-1083">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-1083">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-1084">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1084">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-1085">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1085">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-1086">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1086">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-1087">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-1087">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-1088">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-1088">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a><span data-ttu-id="bf787-1089">DXGI_FORMAT_R32G8X24 \_ <sup>PCs</sup> não tipados (19)</span><span class="sxs-lookup"><span data-stu-id="bf787-1089">DXGI_FORMAT_R32G8X24\_TYPELESS<sup>PCS</sup> (19)</span></span>
| <span data-ttu-id="bf787-1090">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-1090">Target</span></span> | <span data-ttu-id="bf787-1091">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-1091">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-1092">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-1092">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-1093">64</span><span class="sxs-lookup"><span data-stu-id="bf787-1093">64</span></span> |
| <span data-ttu-id="bf787-1094">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-1094">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-1095">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-1095">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1096">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1096">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1097">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1097">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1098">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-1098">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1099">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-1099">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-1100">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-1100">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-1101">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-1101">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-1102">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-1102">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-1103">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-1103">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-1104">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-1104">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-1105">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-1105">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-1106">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-1106">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-1107">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-1107">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-1108">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-1108">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-1109">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1109">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-1110">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1110">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-1111">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1111">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1112">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-1112">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1113">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-1113">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-1114">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-1114">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-1115">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-1115">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1116">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-1116">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1117">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-1117">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-1118">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1118">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-1119">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1119">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-1120">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1120">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-1121">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-1121">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-1122">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-1122">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-1123">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1123">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-1124">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-1124">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1125">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-1125">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1126">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-1126">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-1127">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1127">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1128">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-1128">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1129">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-1129">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-1130">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-1130">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-1131">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-1131">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-1132">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-1132">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-1133">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-1133">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-1134">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1134">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-1135">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1135">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-1136">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1136">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-1137">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-1137">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-1138">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-1138">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfnssup-20"></a><span data-ttu-id="bf787-1139">DXGI_FORMAT_D32 \_ float \_ S8X24 \_ uint<sup>FNS</sup> (20)</span><span class="sxs-lookup"><span data-stu-id="bf787-1139">DXGI_FORMAT_D32\_FLOAT\_S8X24\_UINT<sup>FNS</sup> (20)</span></span>
| <span data-ttu-id="bf787-1140">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-1140">Target</span></span> | <span data-ttu-id="bf787-1141">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-1141">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-1142">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-1142">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-1143">64</span><span class="sxs-lookup"><span data-stu-id="bf787-1143">64</span></span> |
| <span data-ttu-id="bf787-1144">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-1144">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-1145">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-1145">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1146">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1146">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1147">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1147">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1148">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-1148">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1149">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-1149">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-1150">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-1150">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-1151">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-1151">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-1152">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-1152">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-1153">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-1153">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-1154">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-1154">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-1155">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-1155">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-1156">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-1156">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-1157">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-1157">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-1158">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-1158">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-1159">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1159">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-1160">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1160">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-1161">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1161">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1162">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-1162">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1163">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-1163">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-1164">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-1164">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-1165">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-1165">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1166">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-1166">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1167">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-1167">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-1168">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1168">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-1169">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1169">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-1170">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1170">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-1171">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-1171">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-1172">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-1172">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-1173">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1173">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-1174">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-1174">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1175">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-1175">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1176">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-1176">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-1177">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1177">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1178">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-1178">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1179">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-1179">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-1180">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-1180">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-1181">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-1181">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-1182">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-1182">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-1183">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-1183">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-1184">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1184">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-1185">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1185">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-1186">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1186">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-1187">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-1187">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-1188">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-1188">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfnssup-21"></a><span data-ttu-id="bf787-1189">DXGI_FORMAT_R32 \_ float \_ X8X24 \_ <sup>FNS</sup> (21)</span><span class="sxs-lookup"><span data-stu-id="bf787-1189">DXGI_FORMAT_R32\_FLOAT\_X8X24\_TYPELESS<sup>FNS</sup> (21)</span></span>
| <span data-ttu-id="bf787-1190">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-1190">Target</span></span> | <span data-ttu-id="bf787-1191">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-1191">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-1192">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-1192">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-1193">64</span><span class="sxs-lookup"><span data-stu-id="bf787-1193">64</span></span> |
| <span data-ttu-id="bf787-1194">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-1194">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-1195">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-1195">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1196">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1196">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1197">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1197">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1198">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-1198">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1199">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-1199">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-1200">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-1200">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-1201">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-1201">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-1202">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-1202">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-1203">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-1203">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-1204">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-1204">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-1205">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-1205">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-1206">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-1206">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-1207">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-1207">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-1208">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-1208">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-1209">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1209">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-1210">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1210">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-1211">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1211">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1212">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-1212">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1213">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-1213">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-1214">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-1214">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-1215">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-1215">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1216">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-1216">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1217">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-1217">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-1218">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1218">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-1219">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1219">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-1220">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1220">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-1221">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-1221">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-1222">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-1222">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-1223">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1223">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-1224">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-1224">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1225">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-1225">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1226">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-1226">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-1227">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1227">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1228">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-1228">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1229">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-1229">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-1230">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-1230">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-1231">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-1231">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-1232">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-1232">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-1233">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-1233">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-1234">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1234">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-1235">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1235">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-1236">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1236">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-1237">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-1237">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-1238">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-1238">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfnssup-22"></a><span data-ttu-id="bf787-1239">DXGI_FORMAT_X32 \_ \_ \_ <sup>FNS</sup> uintless G8X24 (22)</span><span class="sxs-lookup"><span data-stu-id="bf787-1239">DXGI_FORMAT_X32\_TYPELESS\_G8X24\_UINT<sup>FNS</sup> (22)</span></span>
| <span data-ttu-id="bf787-1240">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-1240">Target</span></span> | <span data-ttu-id="bf787-1241">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-1241">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-1242">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-1242">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-1243">64</span><span class="sxs-lookup"><span data-stu-id="bf787-1243">64</span></span> |
| <span data-ttu-id="bf787-1244">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-1244">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-1245">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-1245">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1246">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1246">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1247">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1247">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1248">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-1248">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1249">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-1249">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-1250">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-1250">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-1251">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-1251">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-1252">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-1252">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-1253">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-1253">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-1254">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-1254">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-1255">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-1255">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-1256">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-1256">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-1257">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-1257">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-1258">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-1258">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-1259">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1259">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-1260">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1260">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-1261">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1261">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1262">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-1262">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1263">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-1263">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-1264">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-1264">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-1265">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-1265">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1266">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-1266">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1267">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-1267">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-1268">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1268">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-1269">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1269">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-1270">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1270">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-1271">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-1271">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-1272">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-1272">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-1273">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1273">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-1274">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-1274">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1275">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-1275">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1276">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-1276">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-1277">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1277">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1278">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-1278">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1279">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-1279">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-1280">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-1280">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-1281">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-1281">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-1282">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-1282">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-1283">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-1283">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-1284">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1284">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-1285">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1285">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-1286">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1286">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-1287">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-1287">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-1288">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-1288">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="bf787-1289">DXGI_FORMAT_R10G10B10A2 \_ <sup>PCs</sup> não tipados (23)</span><span class="sxs-lookup"><span data-stu-id="bf787-1289">DXGI_FORMAT_R10G10B10A2\_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="bf787-1290">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-1290">Target</span></span> | <span data-ttu-id="bf787-1291">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-1291">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-1292">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-1292">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-1293">32</span><span class="sxs-lookup"><span data-stu-id="bf787-1293">32</span></span> |
| <span data-ttu-id="bf787-1294">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-1294">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-1295">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-1295">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1296">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1296">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1297">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1297">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1298">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-1298">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1299">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-1299">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-1300">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-1300">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-1301">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-1301">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-1302">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-1302">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-1303">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-1303">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-1304">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-1304">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-1305">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-1305">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-1306">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-1306">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-1307">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-1307">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-1308">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-1308">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-1309">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1309">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-1310">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1310">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-1311">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1311">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1312">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-1312">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1313">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-1313">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-1314">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-1314">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-1315">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-1315">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1316">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-1316">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1317">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-1317">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-1318">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1318">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-1319">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1319">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-1320">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1320">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-1321">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-1321">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-1322">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-1322">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-1323">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1323">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-1324">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-1324">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1325">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-1325">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1326">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-1326">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-1327">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1327">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1328">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-1328">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1329">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-1329">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-1330">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-1330">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-1331">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-1331">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-1332">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-1332">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-1333">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-1333">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-1334">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1334">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-1335">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1335">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-1336">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1336">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-1337">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-1337">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-1338">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-1338">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfnssup-24"></a><span data-ttu-id="bf787-1339">DXGI_FORMAT_R10G10B10A2 \_ UNORM<sup>FNS</sup> (24)</span><span class="sxs-lookup"><span data-stu-id="bf787-1339">DXGI_FORMAT_R10G10B10A2\_UNORM<sup>FNS</sup> (24)</span></span>
| <span data-ttu-id="bf787-1340">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-1340">Target</span></span> | <span data-ttu-id="bf787-1341">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-1341">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-1342">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-1342">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-1343">32</span><span class="sxs-lookup"><span data-stu-id="bf787-1343">32</span></span> |
| <span data-ttu-id="bf787-1344">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-1344">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-1345">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-1345">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1346">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1346">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1347">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1347">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1348">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-1348">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1349">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-1349">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-1350">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-1350">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-1351">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-1351">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-1352">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-1352">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-1353">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-1353">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-1354">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-1354">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-1355">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-1355">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-1356">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-1356">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-1357">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-1357">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-1358">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-1358">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-1359">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1359">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-1360">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1360">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-1361">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1361">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1362">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-1362">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1363">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-1363">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-1364">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-1364">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-1365">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-1365">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1366">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-1366">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1367">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-1367">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-1368">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1368">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-1369">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1369">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-1370">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1370">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-1371">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-1371">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-1372">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-1372">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-1373">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1373">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-1374">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-1374">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1375">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-1375">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1376">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-1376">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-1377">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1377">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1378">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-1378">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1379">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-1379">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-1380">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-1380">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-1381">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-1381">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-1382">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-1382">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-1383">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-1383">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-1384">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1384">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-1385">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1385">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-1386">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1386">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-1387">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-1387">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1389">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-1389">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfnssup-25"></a><span data-ttu-id="bf787-1390">DXGI_FORMAT_R10G10B10A2 \_ uint<sup>FNS</sup> (25)</span><span class="sxs-lookup"><span data-stu-id="bf787-1390">DXGI_FORMAT_R10G10B10A2\_UINT<sup>FNS</sup> (25)</span></span>
| <span data-ttu-id="bf787-1391">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-1391">Target</span></span> | <span data-ttu-id="bf787-1392">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-1392">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-1393">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-1393">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-1394">32</span><span class="sxs-lookup"><span data-stu-id="bf787-1394">32</span></span> |
| <span data-ttu-id="bf787-1395">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-1395">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-1396">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-1396">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1397">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1397">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1398">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1398">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1399">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-1399">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1400">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-1400">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-1401">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-1401">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-1402">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-1402">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-1403">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-1403">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-1404">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-1404">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-1405">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-1405">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-1406">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-1406">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-1407">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-1407">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-1408">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-1408">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-1409">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-1409">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-1410">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1410">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-1411">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1411">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-1412">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1412">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1413">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-1413">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1414">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-1414">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-1415">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-1415">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-1416">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-1416">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1417">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-1417">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1418">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-1418">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-1419">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1419">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-1420">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1420">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-1421">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1421">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-1422">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-1422">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-1423">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-1423">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-1424">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1424">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-1425">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-1425">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1426">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-1426">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1427">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-1427">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-1428">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1428">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1429">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-1429">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1430">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-1430">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-1431">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-1431">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-1432">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-1432">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-1433">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-1433">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-1434">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-1434">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-1435">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1435">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-1436">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1436">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-1437">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1437">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-1438">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-1438">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-1439">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-1439">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfnssup-89"></a><span data-ttu-id="bf787-1440">DXGI_FORMAT_R10G10B10 \_ XR \_ Bias \_ a2 \_ UNORM<sup>FNS</sup> (89)</span><span class="sxs-lookup"><span data-stu-id="bf787-1440">DXGI_FORMAT_R10G10B10\_XR\_BIAS\_A2\_UNORM<sup>FNS</sup> (89)</span></span>
| <span data-ttu-id="bf787-1441">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-1441">Target</span></span> | <span data-ttu-id="bf787-1442">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-1442">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-1443">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-1443">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-1444">32</span><span class="sxs-lookup"><span data-stu-id="bf787-1444">32</span></span> |
| <span data-ttu-id="bf787-1445">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-1445">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-1446">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-1446">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1447">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1447">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1448">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1448">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1449">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-1449">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1450">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-1450">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-1451">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-1451">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-1452">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-1452">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-1453">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-1453">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-1454">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-1454">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-1455">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-1455">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-1456">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-1456">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-1457">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-1457">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-1458">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-1458">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-1459">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-1459">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-1460">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1460">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-1461">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1461">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-1462">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1462">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1463">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-1463">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1464">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-1464">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-1465">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-1465">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-1466">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-1466">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1467">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-1467">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1468">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-1468">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-1469">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1469">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-1470">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1470">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-1471">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1471">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-1472">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-1472">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-1473">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-1473">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-1474">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1474">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-1475">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-1475">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1476">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-1476">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1477">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-1477">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-1478">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1478">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1479">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-1479">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1480">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-1480">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-1481">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-1481">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-1482">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-1482">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-1483">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-1483">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-1484">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-1484">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-1485">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1485">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-1486">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1486">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-1487">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1487">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-1488">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-1488">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-1489">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-1489">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="bf787-1490">DXGI_FORMAT_R11G11B10 \_ float<sup>FNS</sup> (26)</span><span class="sxs-lookup"><span data-stu-id="bf787-1490">DXGI_FORMAT_R11G11B10\_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="bf787-1491">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-1491">Target</span></span> | <span data-ttu-id="bf787-1492">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-1492">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-1493">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-1493">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-1494">32</span><span class="sxs-lookup"><span data-stu-id="bf787-1494">32</span></span> |
| <span data-ttu-id="bf787-1495">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-1495">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-1496">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-1496">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1497">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1497">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1498">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1498">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1499">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-1499">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1500">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-1500">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-1501">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-1501">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-1502">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-1502">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-1503">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-1503">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-1504">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-1504">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-1505">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-1505">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-1506">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-1506">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-1507">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-1507">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-1508">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-1508">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-1509">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-1509">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-1510">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1510">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-1511">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1511">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-1512">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1512">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1513">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-1513">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1514">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-1514">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-1515">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-1515">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-1516">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-1516">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1517">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-1517">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1518">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-1518">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-1519">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1519">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-1520">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1520">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-1521">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1521">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-1522">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-1522">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-1523">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-1523">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-1524">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1524">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-1525">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-1525">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1526">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-1526">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1527">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-1527">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-1528">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1528">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1529">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-1529">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1530">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-1530">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-1531">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-1531">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-1532">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-1532">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-1533">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-1533">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-1534">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-1534">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-1535">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1535">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-1536">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1536">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-1537">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1537">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-1538">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-1538">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-1539">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-1539">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="bf787-1540">DXGI_FORMAT_R8G8B8A8 \_ <sup>PCs</sup> não tipados (27)</span><span class="sxs-lookup"><span data-stu-id="bf787-1540">DXGI_FORMAT_R8G8B8A8\_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="bf787-1541">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-1541">Target</span></span> | <span data-ttu-id="bf787-1542">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-1542">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-1543">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-1543">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-1544">32</span><span class="sxs-lookup"><span data-stu-id="bf787-1544">32</span></span> |
| <span data-ttu-id="bf787-1545">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-1545">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-1546">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-1546">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1547">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1547">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1548">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1548">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1549">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-1549">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1550">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-1550">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-1551">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-1551">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-1552">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-1552">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-1553">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-1553">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-1554">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-1554">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-1555">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-1555">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-1556">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-1556">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-1557">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-1557">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-1558">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-1558">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-1559">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-1559">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-1560">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1560">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-1561">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1561">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-1562">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1562">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1563">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-1563">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1564">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-1564">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-1565">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-1565">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-1566">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-1566">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1567">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-1567">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1568">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-1568">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-1569">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1569">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-1570">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1570">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-1571">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1571">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-1572">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-1572">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-1573">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-1573">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-1574">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1574">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-1575">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-1575">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1576">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-1576">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1577">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-1577">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-1578">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1578">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1579">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-1579">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1580">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-1580">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-1581">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-1581">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-1582">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-1582">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-1583">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-1583">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-1584">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-1584">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-1585">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1585">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-1586">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1586">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-1587">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1587">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-1588">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-1588">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-1589">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-1589">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfnssup-28"></a><span data-ttu-id="bf787-1590">DXGI_FORMAT_R8G8B8A8 \_ UNORM<sup>FNS</sup> (28)</span><span class="sxs-lookup"><span data-stu-id="bf787-1590">DXGI_FORMAT_R8G8B8A8\_UNORM<sup>FNS</sup> (28)</span></span>
| <span data-ttu-id="bf787-1591">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-1591">Target</span></span> | <span data-ttu-id="bf787-1592">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-1592">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-1593">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-1593">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-1594">32</span><span class="sxs-lookup"><span data-stu-id="bf787-1594">32</span></span> |
| <span data-ttu-id="bf787-1595">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-1595">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1597">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-1597">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1598">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1598">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1600">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1600">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1601">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-1601">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1602">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-1602">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-1603">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-1603">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1605">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-1605">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1607">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-1607">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1609">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-1609">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1611">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-1611">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1613">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-1613">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-1614">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-1614">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-1615">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-1615">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-1616">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-1616">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-1617">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1617">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1619">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1619">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1621">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1621">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1623">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-1623">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1625">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-1625">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-1626">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-1626">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-1627">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-1627">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1628">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-1628">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1629">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-1629">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-1630">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1630">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-1631">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1631">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-1632">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1632">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-1633">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-1633">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-1634">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-1634">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-1635">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1635">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-1636">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-1636">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1637">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-1637">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1638">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-1638">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1640">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1640">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-1642">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-1642">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-1644">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-1644">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-1646">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-1646">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1648">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-1648">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-1649">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-1649">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1651">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-1651">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-1652">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1652">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-1653">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1653">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-1655">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1655">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1657">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-1657">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1659">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-1659">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfnssup-29"></a><span data-ttu-id="bf787-1660">DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ sRGB<sup>FNS</sup> (29)</span><span class="sxs-lookup"><span data-stu-id="bf787-1660">DXGI_FORMAT_R8G8B8A8\_UNORM\_SRGB<sup>FNS</sup> (29)</span></span>
| <span data-ttu-id="bf787-1661">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-1661">Target</span></span> | <span data-ttu-id="bf787-1662">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-1662">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-1663">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-1663">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-1664">32</span><span class="sxs-lookup"><span data-stu-id="bf787-1664">32</span></span> |
| <span data-ttu-id="bf787-1665">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-1665">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1667">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-1667">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1668">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1668">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1669">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1669">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1670">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-1670">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1671">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-1671">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-1672">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-1672">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1674">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-1674">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1676">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-1676">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1678">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-1678">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1680">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-1680">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1682">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-1682">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-1683">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-1683">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-1684">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-1684">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-1685">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-1685">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-1686">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1686">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1688">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1688">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1690">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1690">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1692">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-1692">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1694">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-1694">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-1695">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-1695">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-1696">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-1696">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1697">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-1697">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1698">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-1698">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-1699">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1699">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-1700">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1700">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-1701">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1701">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-1702">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-1702">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-1703">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-1703">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-1704">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1704">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-1705">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-1705">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1706">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-1706">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1707">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-1707">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1709">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1709">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-1711">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-1711">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-1713">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-1713">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-1715">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-1715">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1717">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-1717">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-1718">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-1718">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1720">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-1720">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-1721">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1721">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-1722">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1722">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-1724">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1724">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1726">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-1726">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1728">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-1728">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfnssup-30"></a><span data-ttu-id="bf787-1729">DXGI_FORMAT_R8G8B8A8 \_ uint<sup>FNS</sup> (30)</span><span class="sxs-lookup"><span data-stu-id="bf787-1729">DXGI_FORMAT_R8G8B8A8\_UINT<sup>FNS</sup> (30)</span></span>
| <span data-ttu-id="bf787-1730">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-1730">Target</span></span> | <span data-ttu-id="bf787-1731">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-1731">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-1732">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-1732">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-1733">32</span><span class="sxs-lookup"><span data-stu-id="bf787-1733">32</span></span> |
| <span data-ttu-id="bf787-1734">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-1734">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1736">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-1736">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1737">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1737">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1739">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1739">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1740">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-1740">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1741">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-1741">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-1742">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-1742">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-1743">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-1743">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-1744">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-1744">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-1745">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-1745">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-1746">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-1746">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-1747">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-1747">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-1748">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-1748">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-1749">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-1749">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-1750">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-1750">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-1751">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1751">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-1752">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1752">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-1753">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1753">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1754">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-1754">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1755">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-1755">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-1756">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-1756">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-1757">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-1757">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1758">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-1758">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1759">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-1759">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-1760">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1760">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-1761">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1761">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-1762">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1762">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-1763">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-1763">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-1764">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-1764">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-1765">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1765">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-1766">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-1766">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1767">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-1767">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1768">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-1768">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-1769">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1769">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1770">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-1770">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1771">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-1771">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-1772">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-1772">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-1773">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-1773">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-1774">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-1774">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-1775">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-1775">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-1776">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1776">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-1777">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1777">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-1778">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1778">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-1779">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-1779">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-1780">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-1780">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfnssup-31"></a><span data-ttu-id="bf787-1781">DXGI_FORMAT_R8G8B8A8 \_ SNORM<sup>FNS</sup> (31)</span><span class="sxs-lookup"><span data-stu-id="bf787-1781">DXGI_FORMAT_R8G8B8A8\_SNORM<sup>FNS</sup> (31)</span></span>
| <span data-ttu-id="bf787-1782">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-1782">Target</span></span> | <span data-ttu-id="bf787-1783">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-1783">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-1784">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-1784">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-1785">32</span><span class="sxs-lookup"><span data-stu-id="bf787-1785">32</span></span> |
| <span data-ttu-id="bf787-1786">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-1786">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1788">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-1788">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1789">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1789">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1790">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1790">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1791">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-1791">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1792">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-1792">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-1793">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-1793">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1795">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-1795">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-1796">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-1796">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1798">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-1798">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1800">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-1800">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1802">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-1802">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-1803">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-1803">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-1804">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-1804">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-1805">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-1805">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-1806">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1806">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1808">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1808">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-1809">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1809">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1810">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-1810">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1811">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-1811">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-1812">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-1812">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-1813">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-1813">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1814">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-1814">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1815">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-1815">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-1816">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1816">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-1817">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1817">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-1818">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1818">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-1819">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-1819">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-1820">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-1820">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-1821">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1821">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-1822">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-1822">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1823">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-1823">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1824">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-1824">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-1826">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1826">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1827">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-1827">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1828">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-1828">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-1829">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-1829">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-1830">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-1830">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-1831">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-1831">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-1832">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-1832">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-1833">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1833">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-1834">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1834">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-1835">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1835">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-1836">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-1836">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-1837">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-1837">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfnssup-32"></a><span data-ttu-id="bf787-1838">DXGI_FORMAT_R8G8B8A8 \_ Santo<sup>FNS</sup> (32)</span><span class="sxs-lookup"><span data-stu-id="bf787-1838">DXGI_FORMAT_R8G8B8A8\_SINT<sup>FNS</sup> (32)</span></span>
| <span data-ttu-id="bf787-1839">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-1839">Target</span></span> | <span data-ttu-id="bf787-1840">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-1840">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-1841">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-1841">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-1842">32</span><span class="sxs-lookup"><span data-stu-id="bf787-1842">32</span></span> |
| <span data-ttu-id="bf787-1843">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-1843">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-1844">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-1844">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1845">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1845">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1846">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1846">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1847">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-1847">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1848">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-1848">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-1849">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-1849">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-1850">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-1850">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-1851">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-1851">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-1852">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-1852">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-1853">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-1853">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-1854">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-1854">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-1855">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-1855">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-1856">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-1856">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-1857">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-1857">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-1858">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1858">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-1859">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1859">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-1860">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1860">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1861">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-1861">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1862">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-1862">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-1863">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-1863">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-1864">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-1864">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1865">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-1865">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1866">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-1866">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-1867">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1867">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-1868">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1868">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-1869">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1869">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-1870">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-1870">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-1871">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-1871">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-1872">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1872">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-1873">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-1873">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1874">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-1874">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1875">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-1875">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-1876">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1876">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1877">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-1877">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1878">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-1878">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-1879">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-1879">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-1880">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-1880">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-1881">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-1881">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-1882">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-1882">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-1883">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1883">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-1884">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1884">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-1885">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1885">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-1886">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-1886">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-1887">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-1887">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="bf787-1888">DXGI_FORMAT_R16G16 \_ <sup>PCs</sup> não tipados (33)</span><span class="sxs-lookup"><span data-stu-id="bf787-1888">DXGI_FORMAT_R16G16\_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="bf787-1889">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-1889">Target</span></span> | <span data-ttu-id="bf787-1890">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-1890">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-1891">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-1891">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-1892">32</span><span class="sxs-lookup"><span data-stu-id="bf787-1892">32</span></span> |
| <span data-ttu-id="bf787-1893">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-1893">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-1894">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-1894">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1895">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1895">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1896">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1896">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1897">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-1897">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1898">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-1898">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-1899">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-1899">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-1900">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-1900">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-1901">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-1901">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-1902">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-1902">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-1903">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-1903">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-1904">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-1904">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-1905">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-1905">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-1906">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-1906">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-1907">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-1907">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-1908">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1908">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-1909">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1909">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-1910">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1910">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1911">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-1911">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1912">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-1912">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-1913">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-1913">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-1914">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-1914">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1915">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-1915">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1916">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-1916">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-1917">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1917">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-1918">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1918">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-1919">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1919">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-1920">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-1920">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-1921">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-1921">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-1922">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1922">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-1923">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-1923">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1924">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-1924">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1925">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-1925">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-1926">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1926">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1927">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-1927">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1928">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-1928">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-1929">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-1929">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-1930">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-1930">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-1931">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-1931">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-1932">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-1932">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-1933">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1933">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-1934">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1934">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-1935">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1935">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-1936">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-1936">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-1937">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-1937">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_floatsupfnssup-34"></a><span data-ttu-id="bf787-1938">DXGI_FORMAT_R16G16 \_ float<sup>FNS</sup> (34)</span><span class="sxs-lookup"><span data-stu-id="bf787-1938">DXGI_FORMAT_R16G16\_FLOAT<sup>FNS</sup> (34)</span></span>
| <span data-ttu-id="bf787-1939">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-1939">Target</span></span> | <span data-ttu-id="bf787-1940">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-1940">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-1941">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-1941">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-1942">32</span><span class="sxs-lookup"><span data-stu-id="bf787-1942">32</span></span> |
| <span data-ttu-id="bf787-1943">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-1943">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-1944">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-1944">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1945">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1945">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1946">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1946">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1947">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-1947">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1948">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-1948">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-1949">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-1949">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-1950">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-1950">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-1951">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-1951">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-1952">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-1952">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-1953">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-1953">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-1954">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-1954">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-1955">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-1955">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-1956">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-1956">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-1957">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-1957">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-1958">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1958">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-1959">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-1959">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-1960">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1960">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1961">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-1961">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1962">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-1962">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-1963">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-1963">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-1964">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-1964">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1965">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-1965">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-1966">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-1966">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-1967">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1967">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-1968">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1968">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-1969">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1969">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-1970">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-1970">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-1971">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-1971">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-1972">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-1972">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-1973">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-1973">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1974">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-1974">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-1975">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-1975">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-1976">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-1976">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1977">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-1977">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-1978">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-1978">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-1979">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-1979">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-1980">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-1980">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-1981">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-1981">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-1982">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-1982">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-1983">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1983">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-1984">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1984">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-1985">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-1985">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-1986">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-1986">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-1987">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-1987">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_unormsupfnssup-35"></a><span data-ttu-id="bf787-1988">DXGI_FORMAT_R16G16 \_ UNORM<sup>FNS</sup> (35)</span><span class="sxs-lookup"><span data-stu-id="bf787-1988">DXGI_FORMAT_R16G16\_UNORM<sup>FNS</sup> (35)</span></span>
| <span data-ttu-id="bf787-1989">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-1989">Target</span></span> | <span data-ttu-id="bf787-1990">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-1990">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-1991">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-1991">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-1992">32</span><span class="sxs-lookup"><span data-stu-id="bf787-1992">32</span></span> |
| <span data-ttu-id="bf787-1993">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-1993">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-1994">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-1994">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1995">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1995">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1996">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-1996">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1997">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-1997">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-1998">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-1998">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-1999">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-1999">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-2000">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-2000">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-2001">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-2001">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-2002">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-2002">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-2003">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-2003">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-2004">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-2004">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-2005">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-2005">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-2006">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-2006">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-2007">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-2007">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-2008">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2008">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-2009">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2009">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-2010">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2010">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2011">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-2011">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2012">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-2012">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-2013">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-2013">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-2014">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-2014">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2015">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-2015">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2016">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-2016">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-2017">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2017">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-2018">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2018">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-2019">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2019">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-2020">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-2020">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-2021">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-2021">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-2022">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2022">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-2023">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-2023">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2024">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-2024">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2025">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-2025">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-2026">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2026">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2027">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-2027">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2028">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-2028">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-2029">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-2029">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-2030">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-2030">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-2031">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-2031">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-2032">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-2032">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-2033">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2033">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-2034">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2034">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-2035">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2035">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-2036">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-2036">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-2037">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-2037">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_uintsupfnssup-36"></a><span data-ttu-id="bf787-2038">DXGI_FORMAT_R16G16 \_ uint<sup>FNS</sup> (36)</span><span class="sxs-lookup"><span data-stu-id="bf787-2038">DXGI_FORMAT_R16G16\_UINT<sup>FNS</sup> (36)</span></span>
| <span data-ttu-id="bf787-2039">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-2039">Target</span></span> | <span data-ttu-id="bf787-2040">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-2040">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-2041">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-2041">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-2042">32</span><span class="sxs-lookup"><span data-stu-id="bf787-2042">32</span></span> |
| <span data-ttu-id="bf787-2043">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-2043">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-2044">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-2044">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2045">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2045">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2046">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2046">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2047">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-2047">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2048">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-2048">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-2049">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-2049">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-2050">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-2050">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-2051">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-2051">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-2052">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-2052">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-2053">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-2053">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-2054">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-2054">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-2055">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-2055">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-2056">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-2056">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-2057">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-2057">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-2058">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2058">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-2059">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2059">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-2060">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2060">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2061">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-2061">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2062">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-2062">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-2063">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-2063">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-2064">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-2064">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2065">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-2065">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2066">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-2066">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-2067">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2067">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-2068">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2068">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-2069">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2069">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-2070">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-2070">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-2071">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-2071">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-2072">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2072">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-2073">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-2073">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2074">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-2074">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2075">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-2075">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-2076">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2076">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2077">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-2077">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2078">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-2078">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-2079">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-2079">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-2080">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-2080">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-2081">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-2081">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-2082">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-2082">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-2083">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2083">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-2084">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2084">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-2085">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2085">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-2086">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-2086">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-2087">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-2087">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_snormsupfnssup-37"></a><span data-ttu-id="bf787-2088">DXGI_FORMAT_R16G16 \_ SNORM<sup>FNS</sup> (37)</span><span class="sxs-lookup"><span data-stu-id="bf787-2088">DXGI_FORMAT_R16G16\_SNORM<sup>FNS</sup> (37)</span></span>
| <span data-ttu-id="bf787-2089">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-2089">Target</span></span> | <span data-ttu-id="bf787-2090">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-2090">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-2091">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-2091">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-2092">32</span><span class="sxs-lookup"><span data-stu-id="bf787-2092">32</span></span> |
| <span data-ttu-id="bf787-2093">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-2093">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-2095">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-2095">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2096">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2096">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-2098">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2098">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2099">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-2099">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2100">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-2100">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-2101">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-2101">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-2103">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-2103">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-2104">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-2104">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-2105">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-2105">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-2107">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-2107">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-2108">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-2108">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-2109">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-2109">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-2110">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-2110">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-2111">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-2111">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-2112">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2112">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-2114">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2114">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-2115">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2115">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2116">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-2116">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2117">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-2117">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-2118">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-2118">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-2119">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-2119">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2120">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-2120">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2121">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-2121">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-2122">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2122">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-2123">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2123">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-2124">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2124">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-2125">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-2125">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-2126">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-2126">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-2127">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2127">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-2128">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-2128">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2129">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-2129">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2130">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-2130">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-2132">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2132">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2133">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-2133">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2134">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-2134">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-2135">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-2135">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-2136">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-2136">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-2137">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-2137">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-2138">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-2138">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-2139">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2139">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-2140">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2140">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-2141">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2141">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-2142">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-2142">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-2143">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-2143">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_sintsupfnssup-38"></a><span data-ttu-id="bf787-2144">DXGI_FORMAT_R16G16 \_ Santo<sup>FNS</sup> (38)</span><span class="sxs-lookup"><span data-stu-id="bf787-2144">DXGI_FORMAT_R16G16\_SINT<sup>FNS</sup> (38)</span></span>
| <span data-ttu-id="bf787-2145">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-2145">Target</span></span> | <span data-ttu-id="bf787-2146">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-2146">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-2147">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-2147">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-2148">32</span><span class="sxs-lookup"><span data-stu-id="bf787-2148">32</span></span> |
| <span data-ttu-id="bf787-2149">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-2149">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-2151">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-2151">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2152">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2152">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-2154">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2154">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2155">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-2155">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2156">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-2156">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-2157">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-2157">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-2158">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-2158">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-2159">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-2159">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-2160">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-2160">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-2161">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-2161">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-2162">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-2162">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-2163">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-2163">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-2164">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-2164">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-2165">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-2165">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-2166">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2166">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-2167">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2167">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-2168">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2168">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2169">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-2169">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2170">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-2170">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-2171">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-2171">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-2172">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-2172">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2173">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-2173">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2174">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-2174">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-2175">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2175">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-2176">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2176">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-2177">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2177">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-2178">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-2178">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-2179">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-2179">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-2180">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2180">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-2181">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-2181">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2182">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-2182">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2183">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-2183">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-2184">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2184">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2185">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-2185">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2186">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-2186">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-2187">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-2187">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-2188">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-2188">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-2189">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-2189">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-2190">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-2190">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-2191">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2191">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-2192">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2192">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-2193">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2193">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-2194">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-2194">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-2195">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-2195">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="bf787-2196">DXGI_FORMAT_R32 \_ <sup>PCs</sup> não tipados (39)</span><span class="sxs-lookup"><span data-stu-id="bf787-2196">DXGI_FORMAT_R32\_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="bf787-2197">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-2197">Target</span></span> | <span data-ttu-id="bf787-2198">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-2198">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-2199">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-2199">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-2200">32</span><span class="sxs-lookup"><span data-stu-id="bf787-2200">32</span></span> |
| <span data-ttu-id="bf787-2201">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-2201">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-2202">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-2202">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2203">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2203">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2204">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2204">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2205">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-2205">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2206">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-2206">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-2207">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-2207">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-2208">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-2208">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-2209">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-2209">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-2210">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-2210">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-2211">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-2211">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-2212">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-2212">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-2213">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-2213">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-2214">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-2214">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-2215">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-2215">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-2216">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2216">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-2217">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2217">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-2218">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2218">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2219">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-2219">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2220">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-2220">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-2221">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-2221">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-2222">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-2222">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2223">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-2223">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2224">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-2224">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-2225">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2225">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-2226">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2226">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-2227">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2227">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-2228">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-2228">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-2229">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-2229">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-2230">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2230">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-2231">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-2231">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2232">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-2232">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2233">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-2233">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-2234">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2234">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2235">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-2235">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2236">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-2236">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-2237">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-2237">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-2238">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-2238">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-2239">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-2239">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-2240">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-2240">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-2241">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2241">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-2242">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2242">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-2243">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2243">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-2244">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-2244">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-2245">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-2245">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_floatsupfnssup-40"></a><span data-ttu-id="bf787-2246">DXGI_FORMAT_D32 \_ float<sup>FNS</sup> (40)</span><span class="sxs-lookup"><span data-stu-id="bf787-2246">DXGI_FORMAT_D32\_FLOAT<sup>FNS</sup> (40)</span></span>
| <span data-ttu-id="bf787-2247">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-2247">Target</span></span> | <span data-ttu-id="bf787-2248">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-2248">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-2249">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-2249">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-2250">32</span><span class="sxs-lookup"><span data-stu-id="bf787-2250">32</span></span> |
| <span data-ttu-id="bf787-2251">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-2251">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-2252">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-2252">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2253">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2253">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2254">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2254">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2255">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-2255">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2256">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-2256">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-2257">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-2257">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-2258">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-2258">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-2259">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-2259">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-2260">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-2260">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-2261">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-2261">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-2262">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-2262">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-2263">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-2263">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-2264">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-2264">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-2265">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-2265">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-2266">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2266">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-2267">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2267">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-2268">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2268">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2269">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-2269">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2270">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-2270">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-2271">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-2271">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-2272">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-2272">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2273">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-2273">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2274">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-2274">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-2275">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2275">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-2276">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2276">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-2277">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2277">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-2278">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-2278">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-2279">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-2279">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-2280">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2280">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-2281">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-2281">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2282">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-2282">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2283">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-2283">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-2284">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2284">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2285">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-2285">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2286">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-2286">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-2287">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-2287">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-2288">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-2288">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-2289">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-2289">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-2290">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-2290">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-2291">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2291">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-2292">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2292">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-2293">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2293">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-2294">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-2294">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-2295">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-2295">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_floatsupfnssup-41"></a><span data-ttu-id="bf787-2296">DXGI_FORMAT_R32 \_ float<sup>FNS</sup> (41)</span><span class="sxs-lookup"><span data-stu-id="bf787-2296">DXGI_FORMAT_R32\_FLOAT<sup>FNS</sup> (41)</span></span>
| <span data-ttu-id="bf787-2297">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-2297">Target</span></span> | <span data-ttu-id="bf787-2298">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-2298">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-2299">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-2299">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-2300">32</span><span class="sxs-lookup"><span data-stu-id="bf787-2300">32</span></span> |
| <span data-ttu-id="bf787-2301">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-2301">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-2303">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-2303">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2304">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2304">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-2306">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2306">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2307">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-2307">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2308">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-2308">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-2309">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-2309">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-2310">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-2310">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-2311">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-2311">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-2312">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-2312">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-2313">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-2313">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-2314">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-2314">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-2315">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-2315">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-2316">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-2316">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-2317">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-2317">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-2318">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2318">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-2319">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2319">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-2320">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2320">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2321">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-2321">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2322">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-2322">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-2323">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-2323">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-2324">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-2324">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2325">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-2325">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2326">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-2326">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-2327">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2327">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-2328">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2328">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-2329">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2329">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-2330">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-2330">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-2331">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-2331">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-2332">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2332">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-2333">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-2333">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2334">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-2334">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2335">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-2335">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-2336">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2336">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2337">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-2337">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2338">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-2338">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-2339">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-2339">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-2340">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-2340">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-2341">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-2341">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-2342">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-2342">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-2343">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2343">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-2344">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2344">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-2345">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2345">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-2346">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-2346">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-2347">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-2347">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_uintsupfnssup-42"></a><span data-ttu-id="bf787-2348">DXGI_FORMAT_R32 \_ uint<sup>FNS</sup> (42)</span><span class="sxs-lookup"><span data-stu-id="bf787-2348">DXGI_FORMAT_R32\_UINT<sup>FNS</sup> (42)</span></span>
| <span data-ttu-id="bf787-2349">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-2349">Target</span></span> | <span data-ttu-id="bf787-2350">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-2350">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-2351">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-2351">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-2352">32</span><span class="sxs-lookup"><span data-stu-id="bf787-2352">32</span></span> |
| <span data-ttu-id="bf787-2353">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-2353">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-2354">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-2354">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2355">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2355">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2356">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2356">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2357">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-2357">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2358">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-2358">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-2359">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-2359">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-2360">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-2360">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-2361">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-2361">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-2362">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-2362">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-2363">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-2363">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-2364">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-2364">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-2365">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-2365">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-2366">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-2366">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-2367">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-2367">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-2368">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2368">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-2369">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2369">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-2370">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2370">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2371">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-2371">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2372">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-2372">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-2373">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-2373">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-2374">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-2374">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2375">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-2375">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2376">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-2376">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-2377">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2377">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-2378">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2378">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-2379">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2379">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-2380">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-2380">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-2381">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-2381">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-2382">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2382">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-2383">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-2383">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2384">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-2384">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2385">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-2385">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-2386">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2386">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2387">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-2387">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2388">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-2388">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-2389">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-2389">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-2390">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-2390">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-2391">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-2391">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-2392">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-2392">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-2393">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2393">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-2394">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2394">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-2395">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2395">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-2396">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-2396">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-2397">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-2397">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_sintsupfnssup-43"></a><span data-ttu-id="bf787-2398">DXGI_FORMAT_R32 \_ Santo<sup>FNS</sup> (43)</span><span class="sxs-lookup"><span data-stu-id="bf787-2398">DXGI_FORMAT_R32\_SINT<sup>FNS</sup> (43)</span></span>
| <span data-ttu-id="bf787-2399">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-2399">Target</span></span> | <span data-ttu-id="bf787-2400">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-2400">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-2401">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-2401">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-2402">32</span><span class="sxs-lookup"><span data-stu-id="bf787-2402">32</span></span> |
| <span data-ttu-id="bf787-2403">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-2403">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-2404">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-2404">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2405">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2405">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2406">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2406">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2407">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-2407">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2408">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-2408">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-2409">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-2409">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-2410">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-2410">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-2411">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-2411">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-2412">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-2412">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-2413">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-2413">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-2414">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-2414">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-2415">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-2415">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-2416">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-2416">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-2417">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-2417">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-2418">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2418">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-2419">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2419">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-2420">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2420">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2421">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-2421">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2422">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-2422">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-2423">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-2423">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-2424">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-2424">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2425">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-2425">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2426">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-2426">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-2427">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2427">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-2428">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2428">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-2429">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2429">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-2430">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-2430">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-2431">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-2431">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-2432">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2432">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-2433">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-2433">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2434">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-2434">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2435">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-2435">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-2436">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2436">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2437">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-2437">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2438">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-2438">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-2439">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-2439">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-2440">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-2440">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-2441">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-2441">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-2442">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-2442">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-2443">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2443">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-2444">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2444">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-2445">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2445">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-2446">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-2446">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-2447">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-2447">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a><span data-ttu-id="bf787-2448">DXGI_FORMAT_R24G8 \_ <sup>PCs</sup> não tipados (44)</span><span class="sxs-lookup"><span data-stu-id="bf787-2448">DXGI_FORMAT_R24G8\_TYPELESS<sup>PCS</sup> (44)</span></span>
| <span data-ttu-id="bf787-2449">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-2449">Target</span></span> | <span data-ttu-id="bf787-2450">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-2450">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-2451">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-2451">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-2452">32</span><span class="sxs-lookup"><span data-stu-id="bf787-2452">32</span></span> |
| <span data-ttu-id="bf787-2453">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-2453">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-2454">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-2454">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2455">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2455">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2456">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2456">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2457">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-2457">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2458">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-2458">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-2459">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-2459">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-2460">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-2460">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-2461">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-2461">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-2462">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-2462">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-2463">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-2463">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-2464">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-2464">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-2465">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-2465">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-2466">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-2466">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-2467">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-2467">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-2468">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2468">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-2469">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2469">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-2470">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2470">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2471">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-2471">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2472">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-2472">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-2473">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-2473">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-2474">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-2474">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2475">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-2475">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2476">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-2476">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-2477">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2477">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-2478">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2478">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-2479">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2479">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-2480">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-2480">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-2481">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-2481">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-2482">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2482">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-2483">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-2483">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2484">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-2484">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2485">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-2485">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-2486">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2486">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2487">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-2487">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2488">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-2488">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-2489">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-2489">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-2490">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-2490">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-2491">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-2491">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-2492">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-2492">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-2493">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2493">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-2494">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2494">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-2495">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2495">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-2496">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-2496">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-2497">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-2497">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfnssup-45"></a><span data-ttu-id="bf787-2498">DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT<sup>FNS</sup> (45)</span><span class="sxs-lookup"><span data-stu-id="bf787-2498">DXGI_FORMAT_D24\_UNORM\_S8\_UINT<sup>FNS</sup> (45)</span></span>
| <span data-ttu-id="bf787-2499">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-2499">Target</span></span> | <span data-ttu-id="bf787-2500">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-2500">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-2501">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-2501">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-2502">32</span><span class="sxs-lookup"><span data-stu-id="bf787-2502">32</span></span> |
| <span data-ttu-id="bf787-2503">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-2503">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-2505">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-2505">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2506">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2506">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2507">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2507">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2508">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-2508">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2509">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-2509">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-2510">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-2510">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-2512">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-2512">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-2513">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-2513">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-2514">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-2514">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-2515">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-2515">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-2516">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-2516">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-2517">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-2517">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-2518">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-2518">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-2519">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-2519">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-2520">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2520">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-2521">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2521">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-2522">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2522">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2523">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-2523">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2524">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-2524">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-2525">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-2525">Depth/Stencil Target</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-2527">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-2527">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2528">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-2528">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2529">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-2529">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-2530">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2530">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-2531">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2531">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-2532">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2532">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-2533">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-2533">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-2534">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-2534">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-2535">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2535">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-2536">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-2536">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2537">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-2537">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2538">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-2538">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-2539">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2539">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-2541">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-2541">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-2543">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-2543">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-2545">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-2545">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-2546">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-2546">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-2547">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-2547">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-2548">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-2548">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-2549">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2549">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-2550">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2550">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-2551">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2551">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-2552">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-2552">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-2553">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-2553">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfnssup-46"></a><span data-ttu-id="bf787-2554">FNS UNORM x8 tipo não-suDXGI_FORMAT_R24do \_ \_ \_ (46)<sup></sup></span><span class="sxs-lookup"><span data-stu-id="bf787-2554">DXGI_FORMAT_R24\_UNORM\_X8\_TYPELESS<sup>FNS</sup> (46)</span></span>
| <span data-ttu-id="bf787-2555">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-2555">Target</span></span> | <span data-ttu-id="bf787-2556">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-2556">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-2557">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-2557">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-2558">32</span><span class="sxs-lookup"><span data-stu-id="bf787-2558">32</span></span> |
| <span data-ttu-id="bf787-2559">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-2559">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-2560">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-2560">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2561">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2561">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2562">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2562">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2563">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-2563">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2564">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-2564">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-2565">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-2565">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-2566">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-2566">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-2567">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-2567">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-2568">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-2568">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-2569">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-2569">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-2570">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-2570">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-2571">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-2571">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-2572">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-2572">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-2573">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-2573">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-2574">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2574">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-2575">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2575">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-2576">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2576">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2577">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-2577">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2578">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-2578">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-2579">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-2579">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-2580">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-2580">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2581">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-2581">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2582">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-2582">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-2583">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2583">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-2584">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2584">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-2585">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2585">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-2586">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-2586">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-2587">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-2587">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-2588">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2588">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-2589">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-2589">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2590">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-2590">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2591">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-2591">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-2592">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2592">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2593">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-2593">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2594">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-2594">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-2595">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-2595">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-2596">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-2596">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-2597">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-2597">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-2598">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-2598">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-2599">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2599">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-2600">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2600">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-2601">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2601">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-2602">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-2602">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-2603">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-2603">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfnssup-47"></a><span data-ttu-id="bf787-2604">DXGI_FORMAT_X24 \_ \_ \_ <sup>FNS</sup> de G8 UINT não tipado (47)</span><span class="sxs-lookup"><span data-stu-id="bf787-2604">DXGI_FORMAT_X24\_TYPELESS\_G8\_UINT<sup>FNS</sup> (47)</span></span>
| <span data-ttu-id="bf787-2605">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-2605">Target</span></span> | <span data-ttu-id="bf787-2606">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-2606">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-2607">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-2607">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-2608">32</span><span class="sxs-lookup"><span data-stu-id="bf787-2608">32</span></span> |
| <span data-ttu-id="bf787-2609">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-2609">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-2610">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-2610">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2611">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2611">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2612">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2612">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2613">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-2613">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2614">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-2614">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-2615">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-2615">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-2616">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-2616">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-2617">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-2617">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-2618">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-2618">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-2619">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-2619">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-2620">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-2620">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-2621">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-2621">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-2622">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-2622">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-2623">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-2623">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-2624">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2624">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-2625">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2625">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-2626">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2626">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2627">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-2627">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2628">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-2628">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-2629">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-2629">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-2630">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-2630">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2631">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-2631">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2632">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-2632">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-2633">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2633">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-2634">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2634">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-2635">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2635">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-2636">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-2636">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-2637">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-2637">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-2638">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2638">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-2639">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-2639">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2640">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-2640">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2641">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-2641">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-2642">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2642">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2643">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-2643">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2644">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-2644">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-2645">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-2645">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-2646">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-2646">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-2647">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-2647">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-2648">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-2648">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-2649">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2649">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-2650">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2650">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-2651">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2651">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-2652">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-2652">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-2653">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-2653">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="bf787-2654">DXGI_FORMAT_R8G8 \_ <sup>PCs</sup> não tipados (48)</span><span class="sxs-lookup"><span data-stu-id="bf787-2654">DXGI_FORMAT_R8G8\_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="bf787-2655">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-2655">Target</span></span> | <span data-ttu-id="bf787-2656">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-2656">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-2657">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-2657">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-2658">16</span><span class="sxs-lookup"><span data-stu-id="bf787-2658">16</span></span> |
| <span data-ttu-id="bf787-2659">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-2659">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-2660">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-2660">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2661">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2661">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2662">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2662">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2663">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-2663">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2664">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-2664">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-2665">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-2665">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-2666">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-2666">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-2667">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-2667">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-2668">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-2668">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-2669">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-2669">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-2670">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-2670">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-2671">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-2671">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-2672">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-2672">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-2673">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-2673">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-2674">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2674">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-2675">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2675">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-2676">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2676">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2677">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-2677">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2678">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-2678">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-2679">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-2679">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-2680">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-2680">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2681">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-2681">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2682">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-2682">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-2683">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2683">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-2684">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2684">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-2685">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2685">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-2686">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-2686">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-2687">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-2687">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-2688">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2688">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-2689">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-2689">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2690">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-2690">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2691">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-2691">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-2692">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2692">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2693">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-2693">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2694">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-2694">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-2695">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-2695">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-2696">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-2696">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-2697">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-2697">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-2698">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-2698">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-2699">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2699">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-2700">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2700">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-2701">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2701">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-2702">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-2702">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-2703">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-2703">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_unormsupfnssup-49"></a><span data-ttu-id="bf787-2704">DXGI_FORMAT_R8G8 \_ UNORM<sup>FNS</sup> (49)</span><span class="sxs-lookup"><span data-stu-id="bf787-2704">DXGI_FORMAT_R8G8\_UNORM<sup>FNS</sup> (49)</span></span>
| <span data-ttu-id="bf787-2705">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-2705">Target</span></span> | <span data-ttu-id="bf787-2706">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-2706">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-2707">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-2707">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-2708">16</span><span class="sxs-lookup"><span data-stu-id="bf787-2708">16</span></span> |
| <span data-ttu-id="bf787-2709">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-2709">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-2711">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-2711">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2712">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2712">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2713">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2713">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2714">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-2714">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2715">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-2715">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-2716">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-2716">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-2718">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-2718">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-2719">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-2719">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-2720">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-2720">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-2722">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-2722">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-2724">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-2724">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-2725">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-2725">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-2726">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-2726">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-2727">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-2727">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-2728">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2728">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-2729">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2729">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-2730">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2730">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-2732">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-2732">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-2734">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-2734">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-2735">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-2735">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-2736">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-2736">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2737">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-2737">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2738">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-2738">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-2739">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2739">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-2740">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2740">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-2741">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2741">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-2742">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-2742">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-2743">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-2743">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-2744">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2744">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-2745">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-2745">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2746">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-2746">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2747">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-2747">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-2749">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2749">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2750">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-2750">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2751">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-2751">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-2752">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-2752">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-2753">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-2753">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-2754">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-2754">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-2755">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-2755">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-2756">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2756">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-2757">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2757">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-2758">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2758">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-2759">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-2759">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-2761">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-2761">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_uintsupfnssup-50"></a><span data-ttu-id="bf787-2762">DXGI_FORMAT_R8G8 \_ uint<sup>FNS</sup> (50)</span><span class="sxs-lookup"><span data-stu-id="bf787-2762">DXGI_FORMAT_R8G8\_UINT<sup>FNS</sup> (50)</span></span>
| <span data-ttu-id="bf787-2763">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-2763">Target</span></span> | <span data-ttu-id="bf787-2764">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-2764">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-2765">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-2765">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-2766">16</span><span class="sxs-lookup"><span data-stu-id="bf787-2766">16</span></span> |
| <span data-ttu-id="bf787-2767">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-2767">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-2768">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-2768">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2769">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2769">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2770">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2770">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2771">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-2771">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2772">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-2772">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-2773">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-2773">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-2774">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-2774">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-2775">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-2775">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-2776">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-2776">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-2777">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-2777">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-2778">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-2778">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-2779">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-2779">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-2780">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-2780">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-2781">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-2781">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-2782">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2782">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-2783">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2783">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-2784">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2784">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2785">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-2785">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2786">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-2786">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-2787">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-2787">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-2788">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-2788">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2789">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-2789">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2790">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-2790">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-2791">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2791">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-2792">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2792">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-2793">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2793">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-2794">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-2794">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-2795">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-2795">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-2796">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2796">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-2797">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-2797">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2798">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-2798">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2799">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-2799">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-2800">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2800">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2801">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-2801">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2802">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-2802">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-2803">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-2803">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-2804">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-2804">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-2805">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-2805">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-2806">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-2806">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-2807">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2807">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-2808">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2808">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-2809">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2809">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-2810">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-2810">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-2811">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-2811">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_snormsupfnssup-51"></a><span data-ttu-id="bf787-2812">DXGI_FORMAT_R8G8 \_ SNORM<sup>FNS</sup> (51)</span><span class="sxs-lookup"><span data-stu-id="bf787-2812">DXGI_FORMAT_R8G8\_SNORM<sup>FNS</sup> (51)</span></span>
| <span data-ttu-id="bf787-2813">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-2813">Target</span></span> | <span data-ttu-id="bf787-2814">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-2814">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-2815">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-2815">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-2816">16</span><span class="sxs-lookup"><span data-stu-id="bf787-2816">16</span></span> |
| <span data-ttu-id="bf787-2817">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-2817">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-2819">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-2819">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2820">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2820">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2821">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2821">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2822">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-2822">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2823">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-2823">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-2824">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-2824">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-2826">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-2826">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-2827">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-2827">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-2828">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-2828">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-2830">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-2830">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-2832">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-2832">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-2833">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-2833">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-2834">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-2834">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-2835">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-2835">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-2836">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2836">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-2838">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2838">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-2839">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2839">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2840">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-2840">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2841">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-2841">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-2842">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-2842">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-2843">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-2843">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2844">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-2844">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2845">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-2845">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-2846">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2846">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-2847">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2847">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-2848">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2848">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-2849">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-2849">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-2850">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-2850">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-2851">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2851">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-2852">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-2852">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2853">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-2853">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2854">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-2854">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-2856">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2856">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2857">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-2857">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2858">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-2858">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-2859">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-2859">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-2860">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-2860">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-2861">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-2861">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-2862">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-2862">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-2863">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2863">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-2864">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2864">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-2865">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2865">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-2866">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-2866">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-2867">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-2867">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_sintsupfnssup-52"></a><span data-ttu-id="bf787-2868">DXGI_FORMAT_R8G8 \_ Santo<sup>FNS</sup> (52)</span><span class="sxs-lookup"><span data-stu-id="bf787-2868">DXGI_FORMAT_R8G8\_SINT<sup>FNS</sup> (52)</span></span>
| <span data-ttu-id="bf787-2869">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-2869">Target</span></span> | <span data-ttu-id="bf787-2870">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-2870">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-2871">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-2871">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-2872">16</span><span class="sxs-lookup"><span data-stu-id="bf787-2872">16</span></span> |
| <span data-ttu-id="bf787-2873">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-2873">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-2874">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-2874">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2875">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2875">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2876">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2876">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2877">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-2877">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2878">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-2878">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-2879">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-2879">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-2880">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-2880">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-2881">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-2881">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-2882">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-2882">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-2883">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-2883">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-2884">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-2884">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-2885">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-2885">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-2886">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-2886">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-2887">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-2887">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-2888">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2888">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-2889">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2889">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-2890">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2890">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2891">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-2891">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2892">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-2892">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-2893">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-2893">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-2894">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-2894">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2895">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-2895">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2896">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-2896">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-2897">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2897">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-2898">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2898">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-2899">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2899">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-2900">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-2900">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-2901">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-2901">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-2902">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2902">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-2903">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-2903">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2904">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-2904">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2905">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-2905">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-2906">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2906">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2907">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-2907">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2908">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-2908">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-2909">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-2909">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-2910">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-2910">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-2911">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-2911">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-2912">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-2912">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-2913">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2913">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-2914">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2914">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-2915">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2915">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-2916">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-2916">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-2917">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-2917">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="bf787-2918">DXGI_FORMAT_R16 \_ <sup>PCs</sup> não tipados (53)</span><span class="sxs-lookup"><span data-stu-id="bf787-2918">DXGI_FORMAT_R16\_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="bf787-2919">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-2919">Target</span></span> | <span data-ttu-id="bf787-2920">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-2920">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-2921">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-2921">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-2922">16</span><span class="sxs-lookup"><span data-stu-id="bf787-2922">16</span></span> |
| <span data-ttu-id="bf787-2923">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-2923">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-2924">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-2924">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2925">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2925">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2926">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2926">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2927">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-2927">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2928">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-2928">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-2929">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-2929">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-2930">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-2930">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-2931">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-2931">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-2932">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-2932">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-2933">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-2933">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-2934">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-2934">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-2935">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-2935">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-2936">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-2936">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-2937">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-2937">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-2938">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2938">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-2939">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2939">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-2940">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2940">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2941">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-2941">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2942">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-2942">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-2943">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-2943">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-2944">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-2944">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2945">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-2945">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2946">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-2946">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-2947">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2947">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-2948">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2948">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-2949">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2949">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-2950">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-2950">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-2951">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-2951">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-2952">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2952">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-2953">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-2953">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2954">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-2954">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-2955">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-2955">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-2956">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2956">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2957">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-2957">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2958">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-2958">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-2959">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-2959">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-2960">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-2960">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-2961">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-2961">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-2962">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-2962">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-2963">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2963">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-2964">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2964">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-2965">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-2965">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-2966">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-2966">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-2967">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-2967">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_floatsupfnssup-54"></a><span data-ttu-id="bf787-2968">DXGI_FORMAT_R16 \_ float<sup>FNS</sup> (54)</span><span class="sxs-lookup"><span data-stu-id="bf787-2968">DXGI_FORMAT_R16\_FLOAT<sup>FNS</sup> (54)</span></span>
| <span data-ttu-id="bf787-2969">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-2969">Target</span></span> | <span data-ttu-id="bf787-2970">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-2970">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-2971">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-2971">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-2972">16</span><span class="sxs-lookup"><span data-stu-id="bf787-2972">16</span></span> |
| <span data-ttu-id="bf787-2973">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-2973">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-2974">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-2974">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2975">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2975">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2976">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-2976">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2977">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-2977">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-2978">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-2978">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-2979">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-2979">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-2980">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-2980">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-2981">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-2981">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-2982">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-2982">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-2983">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-2983">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-2984">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-2984">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-2985">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-2985">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-2986">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-2986">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-2987">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-2987">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-2988">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2988">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-2989">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-2989">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-2990">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-2990">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2991">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-2991">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-2992">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-2992">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-2993">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-2993">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-2994">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-2994">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2995">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-2995">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-2996">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-2996">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-2997">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2997">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-2998">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2998">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-2999">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-2999">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-3000">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-3000">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-3001">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-3001">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-3002">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3002">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-3003">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-3003">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3004">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-3004">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3005">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-3005">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-3006">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3006">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3007">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-3007">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3008">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-3008">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-3009">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-3009">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-3010">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-3010">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-3011">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-3011">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-3012">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-3012">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-3013">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3013">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-3014">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3014">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-3015">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3015">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-3016">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-3016">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-3017">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-3017">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d16_unormsupfnssup-55"></a><span data-ttu-id="bf787-3018">DXGI_FORMAT_D16 \_ UNORM<sup>FNS</sup> (55)</span><span class="sxs-lookup"><span data-stu-id="bf787-3018">DXGI_FORMAT_D16\_UNORM<sup>FNS</sup> (55)</span></span>
| <span data-ttu-id="bf787-3019">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-3019">Target</span></span> | <span data-ttu-id="bf787-3020">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-3020">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-3021">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-3021">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-3022">16</span><span class="sxs-lookup"><span data-stu-id="bf787-3022">16</span></span> |
| <span data-ttu-id="bf787-3023">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-3023">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3025">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-3025">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3026">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3026">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3027">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3027">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3028">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-3028">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3029">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-3029">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-3030">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-3030">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3032">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-3032">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-3033">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-3033">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-3034">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-3034">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-3035">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-3035">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-3036">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-3036">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-3037">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-3037">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-3038">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-3038">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-3039">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-3039">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-3040">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3040">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-3041">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3041">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-3042">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3042">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3043">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-3043">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3044">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-3044">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-3045">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-3045">Depth/Stencil Target</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3047">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-3047">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3048">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-3048">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3049">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-3049">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-3050">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3050">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-3051">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3051">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-3052">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3052">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-3053">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-3053">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-3054">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-3054">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-3055">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3055">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-3056">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-3056">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3057">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-3057">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3058">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-3058">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-3059">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3059">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-3061">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-3061">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-3063">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-3063">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-3065">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-3065">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-3066">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-3066">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-3067">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-3067">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-3068">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-3068">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-3069">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3069">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-3070">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3070">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-3071">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3071">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-3072">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-3072">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-3073">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-3073">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_unormsupfnssup-56"></a><span data-ttu-id="bf787-3074">DXGI_FORMAT_R16 \_ UNORM<sup>FNS</sup> (56)</span><span class="sxs-lookup"><span data-stu-id="bf787-3074">DXGI_FORMAT_R16\_UNORM<sup>FNS</sup> (56)</span></span>
| <span data-ttu-id="bf787-3075">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-3075">Target</span></span> | <span data-ttu-id="bf787-3076">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-3076">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-3077">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-3077">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-3078">16</span><span class="sxs-lookup"><span data-stu-id="bf787-3078">16</span></span> |
| <span data-ttu-id="bf787-3079">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-3079">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-3080">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-3080">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3081">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3081">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3082">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3082">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3083">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-3083">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3084">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-3084">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-3085">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-3085">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-3086">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-3086">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-3087">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-3087">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-3088">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-3088">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-3089">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-3089">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-3090">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-3090">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-3091">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-3091">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-3092">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-3092">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-3093">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-3093">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-3094">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3094">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-3095">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3095">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-3096">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3096">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3097">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-3097">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3098">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-3098">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-3099">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-3099">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-3100">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-3100">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3101">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-3101">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3102">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-3102">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-3103">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3103">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-3104">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3104">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-3105">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3105">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-3106">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-3106">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-3107">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-3107">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-3108">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3108">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-3109">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-3109">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3110">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-3110">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3111">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-3111">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-3112">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3112">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3113">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-3113">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3114">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-3114">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-3115">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-3115">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-3116">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-3116">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-3117">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-3117">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-3118">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-3118">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-3119">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3119">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-3120">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3120">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-3121">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3121">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-3122">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-3122">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-3123">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-3123">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_uintsupfnssup-57"></a><span data-ttu-id="bf787-3124">DXGI_FORMAT_R16 \_ uint<sup>FNS</sup> (57)</span><span class="sxs-lookup"><span data-stu-id="bf787-3124">DXGI_FORMAT_R16\_UINT<sup>FNS</sup> (57)</span></span>
| <span data-ttu-id="bf787-3125">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-3125">Target</span></span> | <span data-ttu-id="bf787-3126">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-3126">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-3127">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-3127">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-3128">16</span><span class="sxs-lookup"><span data-stu-id="bf787-3128">16</span></span> |
| <span data-ttu-id="bf787-3129">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-3129">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3131">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-3131">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3132">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3132">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3133">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3133">Input Assembler Index Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3135">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-3135">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3136">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-3136">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-3137">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-3137">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-3138">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-3138">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-3139">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-3139">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-3140">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-3140">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-3141">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-3141">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-3142">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-3142">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-3143">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-3143">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-3144">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-3144">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-3145">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-3145">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-3146">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3146">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-3147">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3147">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-3148">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3148">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3149">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-3149">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3150">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-3150">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-3151">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-3151">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-3152">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-3152">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3153">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-3153">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3154">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-3154">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-3155">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3155">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-3156">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3156">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-3157">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3157">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-3158">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-3158">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-3159">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-3159">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-3160">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3160">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-3161">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-3161">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3162">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-3162">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3163">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-3163">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-3164">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3164">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3165">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-3165">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3166">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-3166">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-3167">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-3167">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-3168">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-3168">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-3169">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-3169">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-3170">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-3170">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-3171">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3171">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-3172">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3172">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-3173">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3173">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-3174">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-3174">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-3175">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-3175">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_snormsupfnssup-58"></a><span data-ttu-id="bf787-3176">DXGI_FORMAT_R16 \_ SNORM<sup>FNS</sup> (58)</span><span class="sxs-lookup"><span data-stu-id="bf787-3176">DXGI_FORMAT_R16\_SNORM<sup>FNS</sup> (58)</span></span>
| <span data-ttu-id="bf787-3177">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-3177">Target</span></span> | <span data-ttu-id="bf787-3178">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-3178">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-3179">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-3179">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-3180">16</span><span class="sxs-lookup"><span data-stu-id="bf787-3180">16</span></span> |
| <span data-ttu-id="bf787-3181">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-3181">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-3182">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-3182">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3183">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3183">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3184">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3184">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3185">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-3185">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3186">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-3186">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-3187">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-3187">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-3188">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-3188">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-3189">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-3189">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-3190">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-3190">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-3191">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-3191">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-3192">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-3192">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-3193">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-3193">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-3194">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-3194">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-3195">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-3195">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-3196">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3196">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-3197">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3197">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-3198">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3198">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3199">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-3199">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3200">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-3200">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-3201">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-3201">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-3202">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-3202">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3203">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-3203">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3204">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-3204">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-3205">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3205">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-3206">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3206">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-3207">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3207">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-3208">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-3208">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-3209">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-3209">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-3210">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3210">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-3211">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-3211">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3212">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-3212">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3213">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-3213">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-3214">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3214">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3215">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-3215">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3216">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-3216">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-3217">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-3217">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-3218">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-3218">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-3219">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-3219">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-3220">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-3220">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-3221">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3221">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-3222">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3222">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-3223">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3223">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-3224">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-3224">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-3225">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-3225">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_sintsupfnssup-59"></a><span data-ttu-id="bf787-3226">DXGI_FORMAT_R16 \_ Santo<sup>FNS</sup> (59)</span><span class="sxs-lookup"><span data-stu-id="bf787-3226">DXGI_FORMAT_R16\_SINT<sup>FNS</sup> (59)</span></span>
| <span data-ttu-id="bf787-3227">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-3227">Target</span></span> | <span data-ttu-id="bf787-3228">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-3228">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-3229">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-3229">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-3230">16</span><span class="sxs-lookup"><span data-stu-id="bf787-3230">16</span></span> |
| <span data-ttu-id="bf787-3231">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-3231">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-3232">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-3232">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3233">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3233">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3234">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3234">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3235">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-3235">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3236">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-3236">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-3237">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-3237">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-3238">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-3238">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-3239">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-3239">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-3240">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-3240">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-3241">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-3241">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-3242">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-3242">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-3243">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-3243">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-3244">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-3244">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-3245">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-3245">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-3246">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3246">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-3247">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3247">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-3248">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3248">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3249">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-3249">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3250">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-3250">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-3251">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-3251">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-3252">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-3252">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3253">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-3253">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3254">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-3254">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-3255">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3255">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-3256">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3256">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-3257">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3257">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-3258">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-3258">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-3259">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-3259">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-3260">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3260">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-3261">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-3261">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3262">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-3262">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3263">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-3263">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-3264">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3264">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3265">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-3265">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3266">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-3266">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-3267">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-3267">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-3268">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-3268">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-3269">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-3269">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-3270">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-3270">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-3271">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3271">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-3272">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3272">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-3273">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3273">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-3274">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-3274">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-3275">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-3275">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="bf787-3276">DXGI_FORMAT_R8 \_ <sup>PCs</sup> não tipados (60)</span><span class="sxs-lookup"><span data-stu-id="bf787-3276">DXGI_FORMAT_R8\_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="bf787-3277">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-3277">Target</span></span> | <span data-ttu-id="bf787-3278">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-3278">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-3279">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-3279">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-3280">8</span><span class="sxs-lookup"><span data-stu-id="bf787-3280">8</span></span> |
| <span data-ttu-id="bf787-3281">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-3281">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-3282">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-3282">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3283">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3283">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3284">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3284">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3285">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-3285">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3286">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-3286">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-3287">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-3287">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-3288">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-3288">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-3289">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-3289">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-3290">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-3290">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-3291">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-3291">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-3292">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-3292">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-3293">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-3293">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-3294">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-3294">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-3295">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-3295">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-3296">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3296">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-3297">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3297">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-3298">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3298">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3299">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-3299">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3300">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-3300">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-3301">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-3301">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-3302">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-3302">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3303">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-3303">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3304">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-3304">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-3305">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3305">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-3306">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3306">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-3307">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3307">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-3308">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-3308">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-3309">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-3309">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-3310">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3310">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-3311">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-3311">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3312">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-3312">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3313">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-3313">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-3314">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3314">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3315">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-3315">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3316">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-3316">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-3317">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-3317">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-3318">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-3318">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-3319">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-3319">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-3320">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-3320">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-3321">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3321">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-3322">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3322">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-3323">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3323">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-3324">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-3324">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-3325">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-3325">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_unormsupfnssup-61"></a><span data-ttu-id="bf787-3326">DXGI_FORMAT_R8 \_ UNORM<sup>FNS</sup> (61)</span><span class="sxs-lookup"><span data-stu-id="bf787-3326">DXGI_FORMAT_R8\_UNORM<sup>FNS</sup> (61)</span></span>
| <span data-ttu-id="bf787-3327">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-3327">Target</span></span> | <span data-ttu-id="bf787-3328">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-3328">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-3329">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-3329">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-3330">8</span><span class="sxs-lookup"><span data-stu-id="bf787-3330">8</span></span> |
| <span data-ttu-id="bf787-3331">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-3331">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3333">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-3333">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3334">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3334">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3335">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3335">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3336">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-3336">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3337">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-3337">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-3338">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-3338">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3340">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-3340">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3342">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-3342">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3344">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-3344">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3346">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-3346">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3348">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-3348">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-3349">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-3349">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-3350">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-3350">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-3351">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-3351">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-3352">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3352">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3354">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3354">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-3355">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3355">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3357">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-3357">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3359">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-3359">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-3360">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-3360">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-3361">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-3361">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3362">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-3362">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3363">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-3363">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-3364">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3364">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-3365">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3365">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-3366">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3366">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-3367">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-3367">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-3368">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-3368">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-3369">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3369">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-3370">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-3370">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3371">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-3371">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3372">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-3372">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3374">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3374">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3375">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-3375">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3376">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-3376">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-3377">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-3377">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-3378">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-3378">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-3379">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-3379">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-3380">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-3380">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-3381">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3381">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-3382">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3382">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-3383">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3383">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-3384">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-3384">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3386">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-3386">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_uintsupfnssup-62"></a><span data-ttu-id="bf787-3387">DXGI_FORMAT_R8 \_ uint<sup>FNS</sup> (62)</span><span class="sxs-lookup"><span data-stu-id="bf787-3387">DXGI_FORMAT_R8\_UINT<sup>FNS</sup> (62)</span></span>
| <span data-ttu-id="bf787-3388">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-3388">Target</span></span> | <span data-ttu-id="bf787-3389">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-3389">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-3390">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-3390">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-3391">8</span><span class="sxs-lookup"><span data-stu-id="bf787-3391">8</span></span> |
| <span data-ttu-id="bf787-3392">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-3392">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-3393">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-3393">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3394">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3394">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3395">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3395">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3396">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-3396">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3397">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-3397">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-3398">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-3398">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-3399">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-3399">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-3400">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-3400">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-3401">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-3401">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-3402">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-3402">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-3403">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-3403">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-3404">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-3404">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-3405">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-3405">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-3406">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-3406">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-3407">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3407">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-3408">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3408">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-3409">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3409">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3410">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-3410">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3411">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-3411">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-3412">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-3412">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-3413">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-3413">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3414">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-3414">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3415">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-3415">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-3416">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3416">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-3417">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3417">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-3418">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3418">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-3419">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-3419">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-3420">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-3420">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-3421">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3421">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-3422">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-3422">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3423">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-3423">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3424">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-3424">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-3425">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3425">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3426">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-3426">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3427">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-3427">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-3428">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-3428">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-3429">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-3429">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-3430">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-3430">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-3431">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-3431">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-3432">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3432">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-3433">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3433">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-3434">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3434">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-3435">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-3435">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-3436">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-3436">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_snormsupfnssup-63"></a><span data-ttu-id="bf787-3437">DXGI_FORMAT_R8 \_ SNORM<sup>FNS</sup> (63)</span><span class="sxs-lookup"><span data-stu-id="bf787-3437">DXGI_FORMAT_R8\_SNORM<sup>FNS</sup> (63)</span></span>
| <span data-ttu-id="bf787-3438">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-3438">Target</span></span> | <span data-ttu-id="bf787-3439">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-3439">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-3440">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-3440">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-3441">8</span><span class="sxs-lookup"><span data-stu-id="bf787-3441">8</span></span> |
| <span data-ttu-id="bf787-3442">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-3442">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-3443">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-3443">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3444">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3444">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3445">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3445">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3446">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-3446">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3447">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-3447">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-3448">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-3448">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-3449">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-3449">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-3450">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-3450">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-3451">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-3451">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-3452">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-3452">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-3453">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-3453">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-3454">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-3454">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-3455">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-3455">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-3456">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-3456">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-3457">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3457">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-3458">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3458">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-3459">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3459">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3460">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-3460">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3461">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-3461">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-3462">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-3462">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-3463">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-3463">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3464">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-3464">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3465">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-3465">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-3466">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3466">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-3467">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3467">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-3468">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3468">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-3469">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-3469">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-3470">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-3470">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-3471">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3471">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-3472">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-3472">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3473">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-3473">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3474">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-3474">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-3475">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3475">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3476">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-3476">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3477">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-3477">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-3478">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-3478">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-3479">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-3479">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-3480">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-3480">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-3481">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-3481">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-3482">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3482">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-3483">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3483">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-3484">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3484">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-3485">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-3485">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-3486">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-3486">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_sintsupfnssup-64"></a><span data-ttu-id="bf787-3487">DXGI_FORMAT_R8 \_ Santo<sup>FNS</sup> (64)</span><span class="sxs-lookup"><span data-stu-id="bf787-3487">DXGI_FORMAT_R8\_SINT<sup>FNS</sup> (64)</span></span>
| <span data-ttu-id="bf787-3488">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-3488">Target</span></span> | <span data-ttu-id="bf787-3489">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-3489">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-3490">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-3490">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-3491">8</span><span class="sxs-lookup"><span data-stu-id="bf787-3491">8</span></span> |
| <span data-ttu-id="bf787-3492">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-3492">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-3493">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-3493">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3494">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3494">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3495">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3495">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3496">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-3496">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3497">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-3497">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-3498">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-3498">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-3499">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-3499">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-3500">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-3500">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-3501">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-3501">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-3502">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-3502">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-3503">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-3503">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-3504">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-3504">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-3505">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-3505">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-3506">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-3506">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-3507">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3507">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-3508">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3508">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-3509">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3509">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3510">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-3510">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3511">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-3511">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-3512">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-3512">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-3513">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-3513">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3514">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-3514">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3515">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-3515">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-3516">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3516">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-3517">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3517">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-3518">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3518">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-3519">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-3519">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-3520">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-3520">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-3521">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3521">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-3522">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-3522">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3523">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-3523">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3524">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-3524">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-3525">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3525">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3526">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-3526">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3527">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-3527">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-3528">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-3528">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-3529">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-3529">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-3530">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-3530">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-3531">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-3531">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-3532">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3532">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-3533">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3533">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-3534">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3534">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-3535">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-3535">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-3536">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-3536">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="bf787-3537">DXGI_FORMAT_A8 \_ UNORM<sup>FNS</sup> (65)</span><span class="sxs-lookup"><span data-stu-id="bf787-3537">DXGI_FORMAT_A8\_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="bf787-3538">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-3538">Target</span></span> | <span data-ttu-id="bf787-3539">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-3539">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-3540">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-3540">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-3541">8</span><span class="sxs-lookup"><span data-stu-id="bf787-3541">8</span></span> |
| <span data-ttu-id="bf787-3542">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-3542">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3544">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-3544">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3545">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3545">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3546">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3546">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3547">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-3547">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3548">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-3548">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-3549">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-3549">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3551">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-3551">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-3552">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-3552">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-3553">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-3553">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3555">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-3555">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3557">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-3557">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-3558">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-3558">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-3559">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-3559">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-3560">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-3560">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-3561">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3561">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-3562">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3562">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-3563">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3563">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3565">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-3565">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3567">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-3567">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-3568">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-3568">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-3569">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-3569">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3570">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-3570">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3571">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-3571">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-3572">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3572">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-3573">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3573">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-3574">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3574">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-3575">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-3575">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-3576">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-3576">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-3577">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3577">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-3578">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-3578">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3579">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-3579">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3580">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-3580">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3582">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3582">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3583">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-3583">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3584">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-3584">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-3585">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-3585">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-3586">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-3586">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-3587">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-3587">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-3588">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-3588">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-3589">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3589">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-3590">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3590">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-3591">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3591">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-3592">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-3592">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3594">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-3594">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="bf787-3595">DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67)</span><span class="sxs-lookup"><span data-stu-id="bf787-3595">DXGI_FORMAT_R9G9B9E5\_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="bf787-3596">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-3596">Target</span></span> | <span data-ttu-id="bf787-3597">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-3597">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-3598">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-3598">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-3599">32</span><span class="sxs-lookup"><span data-stu-id="bf787-3599">32</span></span> |
| <span data-ttu-id="bf787-3600">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-3600">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-3601">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-3601">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3602">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3602">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3603">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3603">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3604">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-3604">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3605">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-3605">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-3606">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-3606">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-3607">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-3607">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-3608">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-3608">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-3609">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-3609">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-3610">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-3610">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-3611">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-3611">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-3612">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-3612">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-3613">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-3613">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-3614">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-3614">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-3615">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3615">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-3616">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3616">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-3617">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3617">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3618">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-3618">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3619">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-3619">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-3620">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-3620">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-3621">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-3621">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3622">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-3622">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3623">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-3623">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-3624">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3624">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-3625">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3625">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-3626">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3626">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-3627">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-3627">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-3628">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-3628">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-3629">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3629">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-3630">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-3630">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3631">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-3631">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3632">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-3632">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-3633">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3633">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3634">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-3634">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3635">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-3635">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-3636">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-3636">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-3637">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-3637">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-3638">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-3638">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-3639">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-3639">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-3640">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3640">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-3641">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3641">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-3642">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3642">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-3643">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-3643">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-3644">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-3644">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="bf787-3645">DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68)</span><span class="sxs-lookup"><span data-stu-id="bf787-3645">DXGI_FORMAT_R8G8\_B8G8\_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="bf787-3646">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-3646">Target</span></span> | <span data-ttu-id="bf787-3647">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-3647">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-3648">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-3648">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-3649">16</span><span class="sxs-lookup"><span data-stu-id="bf787-3649">16</span></span> |
| <span data-ttu-id="bf787-3650">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-3650">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-3651">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-3651">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3652">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3652">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3653">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3653">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3654">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-3654">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3655">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-3655">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-3656">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-3656">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-3657">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-3657">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-3658">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-3658">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-3659">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-3659">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-3660">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-3660">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-3661">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-3661">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-3662">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-3662">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-3663">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-3663">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-3664">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-3664">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-3665">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3665">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-3666">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3666">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-3667">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3667">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3668">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-3668">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3669">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-3669">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-3670">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-3670">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-3671">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-3671">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3672">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-3672">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3673">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-3673">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-3674">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3674">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-3675">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3675">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-3676">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3676">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-3677">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-3677">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-3678">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-3678">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-3679">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3679">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-3680">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-3680">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3681">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-3681">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3682">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-3682">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-3683">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3683">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3684">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-3684">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3685">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-3685">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-3686">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-3686">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-3687">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-3687">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-3688">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-3688">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-3689">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-3689">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-3690">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3690">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-3691">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3691">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-3692">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3692">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-3693">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-3693">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-3694">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-3694">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="bf787-3695">DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>FNC</sup> (69)</span><span class="sxs-lookup"><span data-stu-id="bf787-3695">DXGI_FORMAT_G8R8\_G8B8\_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="bf787-3696">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-3696">Target</span></span> | <span data-ttu-id="bf787-3697">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-3697">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-3698">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-3698">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-3699">16</span><span class="sxs-lookup"><span data-stu-id="bf787-3699">16</span></span> |
| <span data-ttu-id="bf787-3700">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-3700">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-3701">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-3701">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3702">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3702">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3703">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3703">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3704">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-3704">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3705">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-3705">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-3706">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-3706">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-3707">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-3707">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-3708">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-3708">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-3709">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-3709">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-3710">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-3710">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-3711">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-3711">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-3712">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-3712">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-3713">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-3713">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-3714">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-3714">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-3715">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3715">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-3716">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3716">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-3717">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3717">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3718">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-3718">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3719">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-3719">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-3720">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-3720">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-3721">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-3721">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3722">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-3722">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3723">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-3723">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-3724">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3724">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-3725">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3725">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-3726">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3726">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-3727">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-3727">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-3728">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-3728">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-3729">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3729">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-3730">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-3730">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3731">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-3731">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3732">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-3732">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-3733">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3733">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3734">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-3734">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3735">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-3735">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-3736">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-3736">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-3737">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-3737">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-3738">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-3738">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-3739">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-3739">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-3740">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3740">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-3741">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3741">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-3742">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3742">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-3743">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-3743">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-3744">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-3744">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="bf787-3745">DXGI_FORMAT_BC1 \_ <sup>PCC</sup> de tipo (70)</span><span class="sxs-lookup"><span data-stu-id="bf787-3745">DXGI_FORMAT_BC1\_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="bf787-3746">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-3746">Target</span></span> | <span data-ttu-id="bf787-3747">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-3747">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-3748">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-3748">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-3749">4</span><span class="sxs-lookup"><span data-stu-id="bf787-3749">4</span></span> |
| <span data-ttu-id="bf787-3750">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-3750">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-3751">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-3751">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3752">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3752">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3753">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3753">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3754">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-3754">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3755">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-3755">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-3756">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-3756">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-3757">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-3757">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-3758">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-3758">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-3759">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-3759">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-3760">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-3760">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-3761">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-3761">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-3762">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-3762">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-3763">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-3763">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-3764">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-3764">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-3765">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3765">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-3766">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3766">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-3767">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3767">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3768">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-3768">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3769">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-3769">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-3770">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-3770">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-3771">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-3771">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3772">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-3772">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3773">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-3773">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-3774">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3774">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-3775">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3775">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-3776">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3776">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-3777">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-3777">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-3778">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-3778">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-3779">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3779">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-3780">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-3780">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3781">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-3781">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3782">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-3782">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-3783">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3783">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3784">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-3784">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3785">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-3785">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-3786">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-3786">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-3787">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-3787">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-3788">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-3788">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-3789">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-3789">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-3790">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3790">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-3791">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3791">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-3792">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3792">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-3793">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-3793">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-3794">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-3794">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unormsupfncsup-71"></a><span data-ttu-id="bf787-3795">DXGI_FORMAT_BC1 \_ UNORM<sup>FNC</sup> (71)</span><span class="sxs-lookup"><span data-stu-id="bf787-3795">DXGI_FORMAT_BC1\_UNORM<sup>FNC</sup> (71)</span></span>
| <span data-ttu-id="bf787-3796">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-3796">Target</span></span> | <span data-ttu-id="bf787-3797">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-3797">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-3798">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-3798">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-3799">4</span><span class="sxs-lookup"><span data-stu-id="bf787-3799">4</span></span> |
| <span data-ttu-id="bf787-3800">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-3800">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3802">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-3802">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3803">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3803">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3804">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3804">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3805">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-3805">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3806">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-3806">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-3807">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-3807">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3809">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-3809">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-3810">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-3810">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3812">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-3812">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3814">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-3814">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3816">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-3816">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-3817">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-3817">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-3818">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-3818">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-3819">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-3819">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-3820">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3820">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3822">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3822">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-3823">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3823">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3824">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-3824">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3825">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-3825">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-3826">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-3826">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-3827">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-3827">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3828">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-3828">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3829">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-3829">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-3830">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3830">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-3831">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3831">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-3832">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3832">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-3833">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-3833">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-3834">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-3834">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-3835">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3835">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-3836">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-3836">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3837">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-3837">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3838">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-3838">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3840">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3840">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3841">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-3841">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3842">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-3842">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-3843">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-3843">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-3844">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-3844">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-3845">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-3845">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-3846">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-3846">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-3847">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3847">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-3848">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3848">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-3849">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3849">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-3850">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-3850">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3852">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-3852">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfncsup-72"></a><span data-ttu-id="bf787-3853">DXGI_FORMAT_BC1 \_ UNORM \_ sRGB<sup>FNC</sup> (72)</span><span class="sxs-lookup"><span data-stu-id="bf787-3853">DXGI_FORMAT_BC1\_UNORM\_SRGB<sup>FNC</sup> (72)</span></span>
| <span data-ttu-id="bf787-3854">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-3854">Target</span></span> | <span data-ttu-id="bf787-3855">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-3855">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-3856">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-3856">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-3857">4</span><span class="sxs-lookup"><span data-stu-id="bf787-3857">4</span></span> |
| <span data-ttu-id="bf787-3858">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-3858">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3860">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-3860">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3861">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3861">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3862">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3862">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3863">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-3863">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3864">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-3864">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-3865">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-3865">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3867">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-3867">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-3868">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-3868">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3870">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-3870">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3872">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-3872">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3874">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-3874">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-3875">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-3875">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-3876">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-3876">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-3877">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-3877">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-3878">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3878">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3880">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3880">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-3881">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3881">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3882">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-3882">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3883">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-3883">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-3884">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-3884">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-3885">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-3885">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3886">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-3886">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3887">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-3887">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-3888">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3888">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-3889">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3889">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-3890">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3890">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-3891">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-3891">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-3892">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-3892">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-3893">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3893">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-3894">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-3894">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3895">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-3895">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3896">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-3896">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3898">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3898">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3899">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-3899">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3900">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-3900">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-3901">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-3901">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-3902">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-3902">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-3903">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-3903">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-3904">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-3904">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-3905">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3905">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-3906">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3906">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-3907">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3907">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-3908">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-3908">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3910">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-3910">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="bf787-3911">DXGI_FORMAT_BC2 \_ <sup>PCC</sup> de tipo (73)</span><span class="sxs-lookup"><span data-stu-id="bf787-3911">DXGI_FORMAT_BC2\_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="bf787-3912">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-3912">Target</span></span> | <span data-ttu-id="bf787-3913">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-3913">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-3914">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-3914">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-3915">8</span><span class="sxs-lookup"><span data-stu-id="bf787-3915">8</span></span> |
| <span data-ttu-id="bf787-3916">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-3916">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-3917">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-3917">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3918">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3918">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3919">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3919">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3920">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-3920">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3921">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-3921">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-3922">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-3922">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-3923">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-3923">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-3924">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-3924">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-3925">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-3925">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-3926">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-3926">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-3927">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-3927">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-3928">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-3928">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-3929">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-3929">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-3930">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-3930">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-3931">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3931">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-3932">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3932">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-3933">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3933">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3934">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-3934">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3935">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-3935">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-3936">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-3936">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-3937">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-3937">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3938">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-3938">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3939">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-3939">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-3940">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3940">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-3941">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3941">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-3942">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3942">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-3943">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-3943">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-3944">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-3944">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-3945">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3945">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-3946">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-3946">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3947">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-3947">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-3948">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-3948">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-3949">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3949">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3950">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-3950">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3951">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-3951">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-3952">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-3952">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-3953">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-3953">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-3954">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-3954">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-3955">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-3955">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-3956">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3956">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-3957">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3957">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-3958">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-3958">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-3959">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-3959">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-3960">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-3960">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unormsupfncsup-74"></a><span data-ttu-id="bf787-3961">DXGI_FORMAT_BC2 \_ UNORM<sup>FNC</sup> (74)</span><span class="sxs-lookup"><span data-stu-id="bf787-3961">DXGI_FORMAT_BC2\_UNORM<sup>FNC</sup> (74)</span></span>
| <span data-ttu-id="bf787-3962">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-3962">Target</span></span> | <span data-ttu-id="bf787-3963">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-3963">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-3964">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-3964">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-3965">8</span><span class="sxs-lookup"><span data-stu-id="bf787-3965">8</span></span> |
| <span data-ttu-id="bf787-3966">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-3966">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3968">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-3968">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3969">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3969">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3970">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-3970">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3971">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-3971">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-3972">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-3972">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-3973">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-3973">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3975">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-3975">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-3976">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-3976">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3978">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-3978">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3980">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-3980">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3982">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-3982">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-3983">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-3983">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-3984">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-3984">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-3985">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-3985">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-3986">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3986">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-3988">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-3988">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-3989">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-3989">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3990">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-3990">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-3991">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-3991">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-3992">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-3992">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-3993">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-3993">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3994">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-3994">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-3995">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-3995">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-3996">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3996">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-3997">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3997">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-3998">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-3998">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-3999">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-3999">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-4000">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-4000">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-4001">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4001">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-4002">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-4002">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4003">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-4003">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4004">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-4004">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4006">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4006">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4007">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-4007">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4008">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-4008">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-4009">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-4009">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-4010">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-4010">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-4011">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-4011">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-4012">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-4012">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-4013">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4013">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-4014">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4014">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-4015">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4015">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-4016">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-4016">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4018">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-4018">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfncsup-75"></a><span data-ttu-id="bf787-4019">DXGI_FORMAT_BC2 \_ UNORM \_ sRGB<sup>FNC</sup> (75)</span><span class="sxs-lookup"><span data-stu-id="bf787-4019">DXGI_FORMAT_BC2\_UNORM\_SRGB<sup>FNC</sup> (75)</span></span>
| <span data-ttu-id="bf787-4020">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-4020">Target</span></span> | <span data-ttu-id="bf787-4021">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-4021">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-4022">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-4022">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-4023">8</span><span class="sxs-lookup"><span data-stu-id="bf787-4023">8</span></span> |
| <span data-ttu-id="bf787-4024">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-4024">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4026">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-4026">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4027">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4027">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4028">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4028">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4029">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-4029">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4030">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-4030">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-4031">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-4031">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4033">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-4033">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-4034">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-4034">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4036">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-4036">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4038">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-4038">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4040">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-4040">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-4041">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-4041">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-4042">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-4042">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-4043">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-4043">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-4044">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4044">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4046">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4046">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-4047">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4047">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4048">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-4048">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4049">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-4049">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-4050">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-4050">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-4051">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-4051">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4052">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-4052">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4053">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-4053">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-4054">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4054">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-4055">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4055">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-4056">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4056">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-4057">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-4057">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-4058">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-4058">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-4059">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4059">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-4060">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-4060">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4061">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-4061">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4062">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-4062">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4064">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4064">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4065">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-4065">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4066">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-4066">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-4067">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-4067">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-4068">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-4068">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-4069">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-4069">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-4070">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-4070">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-4071">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4071">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-4072">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4072">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-4073">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4073">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-4074">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-4074">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4076">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-4076">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="bf787-4077">DXGI_FORMAT_BC3 \_ <sup>PCC</sup> de tipo (76)</span><span class="sxs-lookup"><span data-stu-id="bf787-4077">DXGI_FORMAT_BC3\_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="bf787-4078">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-4078">Target</span></span> | <span data-ttu-id="bf787-4079">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-4079">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-4080">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-4080">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-4081">8</span><span class="sxs-lookup"><span data-stu-id="bf787-4081">8</span></span> |
| <span data-ttu-id="bf787-4082">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-4082">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-4083">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-4083">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4084">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4084">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4085">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4085">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4086">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-4086">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4087">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-4087">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-4088">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-4088">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-4089">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-4089">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-4090">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-4090">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-4091">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-4091">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-4092">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-4092">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-4093">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-4093">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-4094">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-4094">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-4095">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-4095">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-4096">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-4096">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-4097">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4097">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-4098">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4098">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-4099">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4099">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4100">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-4100">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4101">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-4101">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-4102">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-4102">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-4103">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-4103">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4104">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-4104">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4105">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-4105">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-4106">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4106">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-4107">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4107">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-4108">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4108">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-4109">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-4109">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-4110">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-4110">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-4111">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4111">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-4112">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-4112">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4113">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-4113">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4114">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-4114">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-4115">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4115">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4116">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-4116">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4117">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-4117">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-4118">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-4118">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-4119">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-4119">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-4120">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-4120">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-4121">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-4121">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-4122">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4122">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-4123">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4123">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-4124">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4124">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-4125">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-4125">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-4126">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-4126">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unormsupfncsup-77"></a><span data-ttu-id="bf787-4127">DXGI_FORMAT_BC3 \_ UNORM<sup>FNC</sup> (77)</span><span class="sxs-lookup"><span data-stu-id="bf787-4127">DXGI_FORMAT_BC3\_UNORM<sup>FNC</sup> (77)</span></span>
| <span data-ttu-id="bf787-4128">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-4128">Target</span></span> | <span data-ttu-id="bf787-4129">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-4129">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-4130">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-4130">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-4131">8</span><span class="sxs-lookup"><span data-stu-id="bf787-4131">8</span></span> |
| <span data-ttu-id="bf787-4132">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-4132">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4134">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-4134">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4135">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4135">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4136">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4136">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4137">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-4137">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4138">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-4138">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-4139">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-4139">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4141">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-4141">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-4142">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-4142">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4144">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-4144">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4146">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-4146">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4148">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-4148">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-4149">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-4149">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-4150">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-4150">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-4151">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-4151">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-4152">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4152">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4154">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4154">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-4155">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4155">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4156">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-4156">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4157">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-4157">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-4158">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-4158">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-4159">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-4159">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4160">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-4160">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4161">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-4161">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-4162">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4162">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-4163">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4163">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-4164">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4164">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-4165">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-4165">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-4166">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-4166">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-4167">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4167">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-4168">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-4168">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4169">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-4169">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4170">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-4170">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4172">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4172">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4173">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-4173">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4174">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-4174">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-4175">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-4175">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-4176">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-4176">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-4177">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-4177">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-4178">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-4178">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-4179">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4179">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-4180">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4180">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-4181">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4181">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-4182">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-4182">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4184">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-4184">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfncsup-78"></a><span data-ttu-id="bf787-4185">DXGI_FORMAT_BC3 \_ UNORM \_ sRGB<sup>FNC</sup> (78)</span><span class="sxs-lookup"><span data-stu-id="bf787-4185">DXGI_FORMAT_BC3\_UNORM\_SRGB<sup>FNC</sup> (78)</span></span>
| <span data-ttu-id="bf787-4186">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-4186">Target</span></span> | <span data-ttu-id="bf787-4187">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-4187">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-4188">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-4188">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-4189">8</span><span class="sxs-lookup"><span data-stu-id="bf787-4189">8</span></span> |
| <span data-ttu-id="bf787-4190">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-4190">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4192">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-4192">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4193">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4193">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4194">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4194">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4195">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-4195">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4196">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-4196">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-4197">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-4197">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4199">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-4199">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-4200">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-4200">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4202">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-4202">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4204">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-4204">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4206">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-4206">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-4207">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-4207">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-4208">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-4208">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-4209">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-4209">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-4210">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4210">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4212">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4212">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-4213">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4213">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4214">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-4214">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4215">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-4215">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-4216">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-4216">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-4217">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-4217">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4218">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-4218">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4219">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-4219">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-4220">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4220">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-4221">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4221">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-4222">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4222">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-4223">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-4223">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-4224">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-4224">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-4225">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4225">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-4226">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-4226">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4227">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-4227">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4228">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-4228">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4230">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4230">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4231">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-4231">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4232">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-4232">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-4233">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-4233">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-4234">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-4234">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-4235">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-4235">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-4236">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-4236">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-4237">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4237">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-4238">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4238">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-4239">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4239">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-4240">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-4240">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4242">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-4242">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="bf787-4243">DXGI_FORMAT_BC4 \_ <sup>PCC</sup> de tipo (79)</span><span class="sxs-lookup"><span data-stu-id="bf787-4243">DXGI_FORMAT_BC4\_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="bf787-4244">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-4244">Target</span></span> | <span data-ttu-id="bf787-4245">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-4245">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-4246">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-4246">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-4247">4</span><span class="sxs-lookup"><span data-stu-id="bf787-4247">4</span></span> |
| <span data-ttu-id="bf787-4248">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-4248">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-4249">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-4249">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4250">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4250">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4251">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4251">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4252">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-4252">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4253">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-4253">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-4254">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-4254">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-4255">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-4255">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-4256">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-4256">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-4257">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-4257">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-4258">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-4258">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-4259">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-4259">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-4260">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-4260">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-4261">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-4261">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-4262">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-4262">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-4263">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4263">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-4264">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4264">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-4265">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4265">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4266">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-4266">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4267">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-4267">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-4268">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-4268">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-4269">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-4269">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4270">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-4270">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4271">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-4271">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-4272">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4272">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-4273">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4273">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-4274">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4274">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-4275">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-4275">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-4276">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-4276">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-4277">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4277">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-4278">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-4278">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4279">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-4279">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4280">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-4280">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-4281">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4281">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4282">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-4282">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4283">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-4283">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-4284">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-4284">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-4285">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-4285">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-4286">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-4286">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-4287">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-4287">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-4288">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4288">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-4289">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4289">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-4290">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4290">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-4291">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-4291">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-4292">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-4292">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_unormsupfncsup-80"></a><span data-ttu-id="bf787-4293">DXGI_FORMAT_BC4 \_ UNORM<sup>FNC</sup> (80)</span><span class="sxs-lookup"><span data-stu-id="bf787-4293">DXGI_FORMAT_BC4\_UNORM<sup>FNC</sup> (80)</span></span>
| <span data-ttu-id="bf787-4294">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-4294">Target</span></span> | <span data-ttu-id="bf787-4295">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-4295">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-4296">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-4296">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-4297">4</span><span class="sxs-lookup"><span data-stu-id="bf787-4297">4</span></span> |
| <span data-ttu-id="bf787-4298">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-4298">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-4299">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-4299">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4300">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4300">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4301">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4301">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4302">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-4302">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4303">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-4303">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-4304">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-4304">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-4305">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-4305">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-4306">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-4306">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-4307">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-4307">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-4308">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-4308">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-4309">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-4309">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-4310">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-4310">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-4311">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-4311">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-4312">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-4312">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-4313">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4313">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-4314">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4314">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-4315">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4315">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4316">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-4316">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4317">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-4317">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-4318">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-4318">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-4319">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-4319">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4320">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-4320">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4321">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-4321">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-4322">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4322">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-4323">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4323">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-4324">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4324">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-4325">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-4325">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-4326">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-4326">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-4327">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4327">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-4328">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-4328">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4329">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-4329">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4330">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-4330">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-4331">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4331">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4332">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-4332">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4333">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-4333">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-4334">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-4334">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-4335">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-4335">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-4336">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-4336">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-4337">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-4337">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-4338">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4338">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-4339">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4339">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-4340">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4340">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-4341">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-4341">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-4342">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-4342">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_snormsupfncsup-81"></a><span data-ttu-id="bf787-4343">DXGI_FORMAT_BC4 \_ SNORM<sup>FNC</sup> (81)</span><span class="sxs-lookup"><span data-stu-id="bf787-4343">DXGI_FORMAT_BC4\_SNORM<sup>FNC</sup> (81)</span></span>
| <span data-ttu-id="bf787-4344">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-4344">Target</span></span> | <span data-ttu-id="bf787-4345">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-4345">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-4346">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-4346">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-4347">4</span><span class="sxs-lookup"><span data-stu-id="bf787-4347">4</span></span> |
| <span data-ttu-id="bf787-4348">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-4348">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-4349">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-4349">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4350">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4350">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4351">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4351">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4352">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-4352">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4353">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-4353">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-4354">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-4354">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-4355">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-4355">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-4356">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-4356">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-4357">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-4357">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-4358">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-4358">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-4359">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-4359">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-4360">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-4360">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-4361">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-4361">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-4362">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-4362">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-4363">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4363">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-4364">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4364">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-4365">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4365">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4366">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-4366">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4367">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-4367">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-4368">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-4368">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-4369">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-4369">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4370">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-4370">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4371">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-4371">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-4372">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4372">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-4373">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4373">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-4374">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4374">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-4375">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-4375">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-4376">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-4376">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-4377">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4377">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-4378">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-4378">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4379">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-4379">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4380">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-4380">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-4381">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4381">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4382">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-4382">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4383">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-4383">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-4384">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-4384">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-4385">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-4385">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-4386">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-4386">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-4387">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-4387">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-4388">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4388">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-4389">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4389">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-4390">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4390">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-4391">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-4391">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-4392">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-4392">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="bf787-4393">DXGI_FORMAT_BC5 \_ <sup>PCC</sup> de tipo (82)</span><span class="sxs-lookup"><span data-stu-id="bf787-4393">DXGI_FORMAT_BC5\_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="bf787-4394">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-4394">Target</span></span> | <span data-ttu-id="bf787-4395">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-4395">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-4396">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-4396">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-4397">8</span><span class="sxs-lookup"><span data-stu-id="bf787-4397">8</span></span> |
| <span data-ttu-id="bf787-4398">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-4398">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-4399">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-4399">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4400">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4400">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4401">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4401">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4402">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-4402">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4403">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-4403">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-4404">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-4404">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-4405">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-4405">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-4406">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-4406">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-4407">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-4407">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-4408">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-4408">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-4409">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-4409">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-4410">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-4410">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-4411">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-4411">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-4412">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-4412">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-4413">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4413">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-4414">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4414">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-4415">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4415">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4416">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-4416">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4417">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-4417">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-4418">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-4418">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-4419">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-4419">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4420">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-4420">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4421">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-4421">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-4422">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4422">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-4423">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4423">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-4424">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4424">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-4425">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-4425">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-4426">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-4426">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-4427">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4427">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-4428">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-4428">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4429">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-4429">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4430">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-4430">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-4431">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4431">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4432">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-4432">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4433">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-4433">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-4434">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-4434">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-4435">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-4435">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-4436">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-4436">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-4437">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-4437">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-4438">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4438">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-4439">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4439">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-4440">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4440">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-4441">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-4441">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-4442">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-4442">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_unormsupfncsup-83"></a><span data-ttu-id="bf787-4443">DXGI_FORMAT_BC5 \_ UNORM<sup>FNC</sup> (83)</span><span class="sxs-lookup"><span data-stu-id="bf787-4443">DXGI_FORMAT_BC5\_UNORM<sup>FNC</sup> (83)</span></span>
| <span data-ttu-id="bf787-4444">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-4444">Target</span></span> | <span data-ttu-id="bf787-4445">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-4445">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-4446">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-4446">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-4447">8</span><span class="sxs-lookup"><span data-stu-id="bf787-4447">8</span></span> |
| <span data-ttu-id="bf787-4448">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-4448">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-4449">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-4449">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4450">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4450">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4451">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4451">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4452">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-4452">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4453">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-4453">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-4454">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-4454">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-4455">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-4455">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-4456">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-4456">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-4457">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-4457">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-4458">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-4458">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-4459">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-4459">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-4460">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-4460">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-4461">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-4461">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-4462">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-4462">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-4463">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4463">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-4464">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4464">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-4465">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4465">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4466">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-4466">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4467">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-4467">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-4468">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-4468">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-4469">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-4469">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4470">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-4470">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4471">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-4471">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-4472">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4472">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-4473">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4473">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-4474">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4474">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-4475">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-4475">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-4476">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-4476">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-4477">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4477">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-4478">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-4478">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4479">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-4479">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4480">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-4480">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-4481">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4481">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4482">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-4482">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4483">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-4483">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-4484">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-4484">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-4485">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-4485">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-4486">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-4486">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-4487">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-4487">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-4488">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4488">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-4489">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4489">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-4490">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4490">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-4491">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-4491">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-4492">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-4492">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_snormsupfncsup-84"></a><span data-ttu-id="bf787-4493">DXGI_FORMAT_BC5 \_ SNORM<sup>FNC</sup> (84)</span><span class="sxs-lookup"><span data-stu-id="bf787-4493">DXGI_FORMAT_BC5\_SNORM<sup>FNC</sup> (84)</span></span>
| <span data-ttu-id="bf787-4494">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-4494">Target</span></span> | <span data-ttu-id="bf787-4495">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-4495">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-4496">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-4496">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-4497">8</span><span class="sxs-lookup"><span data-stu-id="bf787-4497">8</span></span> |
| <span data-ttu-id="bf787-4498">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-4498">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-4499">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-4499">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4500">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4500">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4501">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4501">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4502">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-4502">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4503">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-4503">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-4504">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-4504">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-4505">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-4505">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-4506">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-4506">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-4507">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-4507">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-4508">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-4508">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-4509">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-4509">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-4510">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-4510">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-4511">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-4511">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-4512">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-4512">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-4513">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4513">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-4514">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4514">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-4515">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4515">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4516">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-4516">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4517">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-4517">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-4518">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-4518">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-4519">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-4519">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4520">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-4520">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4521">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-4521">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-4522">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4522">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-4523">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4523">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-4524">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4524">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-4525">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-4525">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-4526">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-4526">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-4527">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4527">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-4528">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-4528">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4529">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-4529">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4530">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-4530">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-4531">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4531">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4532">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-4532">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4533">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-4533">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-4534">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-4534">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-4535">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-4535">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-4536">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-4536">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-4537">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-4537">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-4538">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4538">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-4539">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4539">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-4540">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4540">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-4541">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-4541">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-4542">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-4542">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="bf787-4543">DXGI_FORMAT_B5G6R5 \_ UNORM<sup>FNS</sup> (85)</span><span class="sxs-lookup"><span data-stu-id="bf787-4543">DXGI_FORMAT_B5G6R5\_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="bf787-4544">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-4544">Target</span></span> | <span data-ttu-id="bf787-4545">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-4545">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-4546">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-4546">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-4547">16</span><span class="sxs-lookup"><span data-stu-id="bf787-4547">16</span></span> |
| <span data-ttu-id="bf787-4548">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-4548">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4550">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-4550">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4551">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4551">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4552">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4552">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4553">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-4553">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4554">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-4554">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-4555">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-4555">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4557">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-4557">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-4558">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-4558">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4560">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-4560">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4562">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-4562">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4564">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-4564">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-4565">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-4565">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-4566">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-4566">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-4567">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-4567">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-4568">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4568">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4570">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4570">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4572">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4572">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4574">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-4574">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4576">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-4576">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-4577">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-4577">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-4578">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-4578">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4579">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-4579">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4580">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-4580">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-4581">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4581">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-4582">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4582">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-4583">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4583">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-4584">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-4584">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-4585">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-4585">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-4586">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4586">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-4587">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-4587">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4588">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-4588">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4589">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-4589">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4591">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4591">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-4593">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-4593">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-4595">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-4595">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-4597">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-4597">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4599">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-4599">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-4600">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-4600">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-4601">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-4601">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-4602">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4602">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-4603">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4603">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-4604">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4604">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-4605">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-4605">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-4606">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-4606">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="bf787-4607">DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>FNS</sup> (86)</span><span class="sxs-lookup"><span data-stu-id="bf787-4607">DXGI_FORMAT_B5G5R5A1\_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="bf787-4608">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-4608">Target</span></span> | <span data-ttu-id="bf787-4609">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-4609">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-4610">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-4610">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-4611">16</span><span class="sxs-lookup"><span data-stu-id="bf787-4611">16</span></span> |
| <span data-ttu-id="bf787-4612">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-4612">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4614">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-4614">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4615">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4615">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4616">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4616">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4617">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-4617">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4618">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-4618">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-4619">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-4619">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4621">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-4621">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-4622">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-4622">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4624">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-4624">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4626">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-4626">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4628">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-4628">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-4629">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-4629">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-4630">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-4630">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-4631">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-4631">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-4632">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4632">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4634">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4634">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-4635">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4635">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4636">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-4636">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4637">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-4637">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-4638">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-4638">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-4639">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-4639">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4640">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-4640">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4641">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-4641">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-4642">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4642">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-4643">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4643">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-4644">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4644">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-4645">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-4645">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-4646">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-4646">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-4647">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4647">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-4648">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-4648">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4649">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-4649">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4650">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-4650">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4652">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4652">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4653">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-4653">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4654">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-4654">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-4655">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-4655">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-4656">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-4656">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-4657">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-4657">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-4658">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-4658">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-4659">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4659">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-4660">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4660">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-4661">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4661">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-4662">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-4662">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-4663">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-4663">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="bf787-4664">DXGI_FORMAT_B8G8R8A8 \_ <sup>PCs</sup> não tipados (90)</span><span class="sxs-lookup"><span data-stu-id="bf787-4664">DXGI_FORMAT_B8G8R8A8\_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="bf787-4665">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-4665">Target</span></span> | <span data-ttu-id="bf787-4666">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-4666">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-4667">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-4667">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-4668">32</span><span class="sxs-lookup"><span data-stu-id="bf787-4668">32</span></span> |
| <span data-ttu-id="bf787-4669">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-4669">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-4670">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-4670">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4671">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4671">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4672">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4672">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4673">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-4673">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4674">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-4674">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-4675">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-4675">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-4676">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-4676">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-4677">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-4677">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-4678">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-4678">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-4679">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-4679">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-4680">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-4680">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-4681">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-4681">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-4682">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-4682">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-4683">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-4683">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-4684">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4684">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-4685">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4685">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-4686">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4686">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4687">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-4687">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4688">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-4688">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-4689">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-4689">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-4690">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-4690">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4691">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-4691">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4692">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-4692">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-4693">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4693">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-4694">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4694">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-4695">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4695">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-4696">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-4696">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-4697">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-4697">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-4698">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4698">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-4699">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-4699">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4700">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-4700">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4701">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-4701">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-4702">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4702">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4703">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-4703">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4704">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-4704">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-4705">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-4705">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-4706">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-4706">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-4707">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-4707">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-4708">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-4708">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-4709">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4709">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-4710">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4710">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-4711">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4711">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-4712">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-4712">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-4713">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-4713">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfnssup-87"></a><span data-ttu-id="bf787-4714">DXGI_FORMAT_B8G8R8A8 \_ UNORM<sup>FNS</sup> (87)</span><span class="sxs-lookup"><span data-stu-id="bf787-4714">DXGI_FORMAT_B8G8R8A8\_UNORM<sup>FNS</sup> (87)</span></span>
| <span data-ttu-id="bf787-4715">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-4715">Target</span></span> | <span data-ttu-id="bf787-4716">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-4716">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-4717">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-4717">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-4718">32</span><span class="sxs-lookup"><span data-stu-id="bf787-4718">32</span></span> |
| <span data-ttu-id="bf787-4719">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-4719">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4721">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-4721">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4722">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4722">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4723">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4723">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4724">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-4724">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4725">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-4725">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-4726">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-4726">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4728">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-4728">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4730">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-4730">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4732">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-4732">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4734">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-4734">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4736">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-4736">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-4737">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-4737">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-4738">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-4738">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-4739">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-4739">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-4740">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4740">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4742">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4742">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4744">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4744">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4746">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-4746">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4748">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-4748">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-4749">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-4749">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-4750">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-4750">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4751">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-4751">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4752">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-4752">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-4753">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4753">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-4754">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4754">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-4755">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4755">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-4756">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-4756">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-4757">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-4757">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-4758">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4758">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-4759">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-4759">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4760">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-4760">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4761">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-4761">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4763">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4763">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-4765">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-4765">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-4767">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-4767">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-4769">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-4769">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4771">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-4771">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-4772">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-4772">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4774">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-4774">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-4775">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4775">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-4776">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4776">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-4778">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4778">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4780">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-4780">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4782">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-4782">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfnssup-91"></a><span data-ttu-id="bf787-4783">DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ sRGB<sup>FNS</sup> (91)</span><span class="sxs-lookup"><span data-stu-id="bf787-4783">DXGI_FORMAT_B8G8R8A8\_UNORM\_SRGB<sup>FNS</sup> (91)</span></span>
| <span data-ttu-id="bf787-4784">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-4784">Target</span></span> | <span data-ttu-id="bf787-4785">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-4785">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-4786">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-4786">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-4787">32</span><span class="sxs-lookup"><span data-stu-id="bf787-4787">32</span></span> |
| <span data-ttu-id="bf787-4788">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-4788">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4790">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-4790">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4791">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4791">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4792">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4792">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4793">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-4793">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4794">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-4794">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-4795">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-4795">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4797">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-4797">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4799">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-4799">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4801">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-4801">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4803">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-4803">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4805">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-4805">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-4806">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-4806">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-4807">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-4807">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-4808">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-4808">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-4809">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4809">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4811">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4811">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4813">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4813">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4815">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-4815">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4817">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-4817">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-4818">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-4818">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-4819">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-4819">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4820">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-4820">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4821">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-4821">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-4822">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4822">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-4823">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4823">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-4824">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4824">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-4825">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-4825">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-4826">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-4826">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-4827">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4827">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-4828">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-4828">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4829">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-4829">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4830">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-4830">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4832">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4832">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-4834">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-4834">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-4836">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-4836">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-4838">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-4838">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4840">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-4840">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-4841">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-4841">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4843">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-4843">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-4844">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4844">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-4845">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4845">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-4847">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4847">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4849">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-4849">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4851">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-4851">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="bf787-4852">DXGI_FORMAT_B8G8R8X8 \_ <sup>PCs</sup> não tipados (92)</span><span class="sxs-lookup"><span data-stu-id="bf787-4852">DXGI_FORMAT_B8G8R8X8\_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="bf787-4853">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-4853">Target</span></span> | <span data-ttu-id="bf787-4854">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-4854">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-4855">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-4855">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-4856">32</span><span class="sxs-lookup"><span data-stu-id="bf787-4856">32</span></span> |
| <span data-ttu-id="bf787-4857">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-4857">Format Support</span></span> | \- |
| <span data-ttu-id="bf787-4858">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-4858">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4859">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4859">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4860">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4860">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4861">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-4861">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4862">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-4862">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-4863">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-4863">Texture2D</span></span> | \- |
| <span data-ttu-id="bf787-4864">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-4864">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-4865">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-4865">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-4866">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-4866">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-4867">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-4867">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-4868">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-4868">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-4869">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-4869">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-4870">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-4870">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-4871">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-4871">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-4872">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4872">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-4873">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4873">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-4874">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4874">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4875">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-4875">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4876">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-4876">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-4877">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-4877">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-4878">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-4878">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4879">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-4879">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4880">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-4880">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-4881">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4881">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-4882">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4882">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-4883">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4883">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-4884">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-4884">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-4885">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-4885">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-4886">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4886">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-4887">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-4887">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4888">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-4888">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4889">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-4889">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-4890">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4890">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4891">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-4891">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-4892">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-4892">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-4893">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-4893">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-4894">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-4894">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-4895">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-4895">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-4896">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-4896">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-4897">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4897">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-4898">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4898">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-4899">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4899">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-4900">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-4900">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-4901">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-4901">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfnssup-88"></a><span data-ttu-id="bf787-4902">DXGI_FORMAT_B8G8R8X8 \_ UNORM<sup>FNS</sup> (88)</span><span class="sxs-lookup"><span data-stu-id="bf787-4902">DXGI_FORMAT_B8G8R8X8\_UNORM<sup>FNS</sup> (88)</span></span>
| <span data-ttu-id="bf787-4903">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-4903">Target</span></span> | <span data-ttu-id="bf787-4904">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-4904">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-4905">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-4905">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-4906">32</span><span class="sxs-lookup"><span data-stu-id="bf787-4906">32</span></span> |
| <span data-ttu-id="bf787-4907">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-4907">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4909">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-4909">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4910">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4910">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4911">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4911">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4912">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-4912">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4913">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-4913">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-4914">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-4914">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4916">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-4916">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4918">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-4918">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4920">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-4920">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4922">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-4922">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4924">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-4924">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-4925">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-4925">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-4926">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-4926">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-4927">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-4927">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-4928">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4928">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4930">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4930">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4932">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4932">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4934">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-4934">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4936">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-4936">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-4937">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-4937">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-4938">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-4938">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4939">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-4939">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-4940">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-4940">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-4941">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4941">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-4942">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4942">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-4943">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4943">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-4944">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-4944">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-4945">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-4945">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-4946">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-4946">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-4947">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-4947">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4948">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-4948">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-4949">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-4949">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4951">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-4951">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-4953">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-4953">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-4955">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-4955">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-4957">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-4957">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4959">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-4959">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-4960">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-4960">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-4961">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-4961">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-4962">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4962">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-4963">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4963">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-4965">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-4965">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-4967">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-4967">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4969">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-4969">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfnssup-93"></a><span data-ttu-id="bf787-4970">DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ sRGB<sup>FNS</sup> (93)</span><span class="sxs-lookup"><span data-stu-id="bf787-4970">DXGI_FORMAT_B8G8R8X8\_UNORM\_SRGB<sup>FNS</sup> (93)</span></span>
| <span data-ttu-id="bf787-4971">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-4971">Target</span></span> | <span data-ttu-id="bf787-4972">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-4972">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-4973">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-4973">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-4974">32</span><span class="sxs-lookup"><span data-stu-id="bf787-4974">32</span></span> |
| <span data-ttu-id="bf787-4975">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-4975">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4977">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-4977">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4978">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4978">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4979">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-4979">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4980">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-4980">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-4981">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-4981">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-4982">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-4982">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4984">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-4984">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4986">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-4986">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4988">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-4988">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4990">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-4990">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4992">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-4992">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-4993">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-4993">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-4994">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-4994">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-4995">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-4995">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-4996">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4996">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-4998">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-4998">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5000">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5000">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5002">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-5002">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5004">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-5004">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-5005">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-5005">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-5006">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-5006">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5007">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-5007">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5008">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-5008">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-5009">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5009">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-5010">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5010">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-5011">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5011">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-5012">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-5012">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-5013">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-5013">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-5014">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5014">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-5015">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-5015">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5016">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-5016">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5017">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-5017">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5019">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5019">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5021">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-5021">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5023">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-5023">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5025">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-5025">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5027">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-5027">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-5028">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-5028">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-5029">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-5029">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-5030">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5030">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-5031">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5031">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-5032">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5032">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-5033">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-5033">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5035">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-5035">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="bf787-5036">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span><span class="sxs-lookup"><span data-stu-id="bf787-5036">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="bf787-5037">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-5037">Target</span></span> | <span data-ttu-id="bf787-5038">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-5038">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-5039">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-5039">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-5040">32</span><span class="sxs-lookup"><span data-stu-id="bf787-5040">32</span></span> |
| <span data-ttu-id="bf787-5041">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-5041">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5043">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-5043">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5044">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5044">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5045">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5045">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5046">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-5046">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5047">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-5047">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-5048">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-5048">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5050">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-5050">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-5051">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-5051">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-5052">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-5052">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-5053">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-5053">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-5054">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-5054">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-5055">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-5055">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-5056">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-5056">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-5057">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-5057">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-5058">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5058">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-5059">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5059">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-5060">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5060">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5061">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-5061">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5062">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-5062">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-5063">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-5063">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-5064">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-5064">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5065">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-5065">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5066">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-5066">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-5067">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5067">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-5068">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5068">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-5069">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5069">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-5070">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-5070">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-5071">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-5071">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-5072">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5072">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-5073">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-5073">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5074">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-5074">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5075">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-5075">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5077">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5077">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5078">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-5078">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5079">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-5079">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-5080">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-5080">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-5081">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-5081">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-5082">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-5082">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-5083">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-5083">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-5084">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5084">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5086">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5086">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5088">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5088">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5090">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-5090">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-5091">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-5091">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="bf787-5092">DXGI_FORMAT_Y410<sup>V</sup> (101)</span><span class="sxs-lookup"><span data-stu-id="bf787-5092">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="bf787-5093">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-5093">Target</span></span> | <span data-ttu-id="bf787-5094">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-5094">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-5095">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-5095">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-5096">32</span><span class="sxs-lookup"><span data-stu-id="bf787-5096">32</span></span> |
| <span data-ttu-id="bf787-5097">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-5097">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5099">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-5099">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5100">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5100">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5101">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5101">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5102">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-5102">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5103">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-5103">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-5104">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-5104">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5106">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-5106">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-5107">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-5107">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-5108">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-5108">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-5109">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-5109">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-5110">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-5110">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-5111">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-5111">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-5112">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-5112">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-5113">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-5113">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-5114">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5114">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-5115">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5115">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-5116">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5116">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5117">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-5117">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5118">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-5118">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-5119">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-5119">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-5120">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-5120">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5121">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-5121">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5122">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-5122">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-5123">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5123">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-5124">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5124">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-5125">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5125">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-5126">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-5126">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-5127">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-5127">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-5128">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5128">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-5129">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-5129">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5130">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-5130">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5131">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-5131">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5133">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5133">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5134">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-5134">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5135">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-5135">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-5136">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-5136">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-5137">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-5137">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-5138">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-5138">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-5139">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-5139">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-5140">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5140">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5142">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5142">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5144">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5144">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5146">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-5146">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-5147">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-5147">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="bf787-5148">DXGI_FORMAT_Y416<sup>V</sup> (102)</span><span class="sxs-lookup"><span data-stu-id="bf787-5148">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="bf787-5149">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-5149">Target</span></span> | <span data-ttu-id="bf787-5150">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-5150">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-5151">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-5151">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-5152">64</span><span class="sxs-lookup"><span data-stu-id="bf787-5152">64</span></span> |
| <span data-ttu-id="bf787-5153">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-5153">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5155">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-5155">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5156">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5156">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5157">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5157">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5158">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-5158">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5159">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-5159">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-5160">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-5160">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5162">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-5162">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-5163">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-5163">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-5164">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-5164">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-5165">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-5165">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-5166">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-5166">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-5167">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-5167">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-5168">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-5168">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-5169">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-5169">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-5170">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5170">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-5171">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5171">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-5172">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5172">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5173">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-5173">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5174">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-5174">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-5175">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-5175">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-5176">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-5176">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5177">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-5177">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5178">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-5178">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-5179">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5179">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-5180">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5180">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-5181">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5181">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-5182">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-5182">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-5183">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-5183">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-5184">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5184">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-5185">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-5185">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5186">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-5186">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5187">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-5187">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5189">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5189">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5190">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-5190">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5191">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-5191">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-5192">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-5192">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-5193">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-5193">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-5194">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-5194">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-5195">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-5195">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-5196">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5196">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5198">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5198">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5200">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5200">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5202">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-5202">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-5203">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-5203">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="bf787-5204">DXGI_FORMAT_NV12<sup>V</sup> (103)</span><span class="sxs-lookup"><span data-stu-id="bf787-5204">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="bf787-5205">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-5205">Target</span></span> | <span data-ttu-id="bf787-5206">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-5206">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-5207">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-5207">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-5208">8</span><span class="sxs-lookup"><span data-stu-id="bf787-5208">8</span></span> |
| <span data-ttu-id="bf787-5209">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-5209">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5211">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-5211">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5212">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5212">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5213">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5213">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5214">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-5214">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5215">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-5215">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-5216">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-5216">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5218">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-5218">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-5219">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-5219">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-5220">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-5220">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-5221">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-5221">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-5222">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-5222">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-5223">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-5223">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-5224">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-5224">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-5225">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-5225">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-5226">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5226">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-5227">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5227">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-5228">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5228">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5229">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-5229">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5230">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-5230">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-5231">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-5231">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-5232">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-5232">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5233">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-5233">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5234">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-5234">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-5235">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5235">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-5236">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5236">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-5237">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5237">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-5238">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-5238">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-5239">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-5239">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-5240">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5240">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-5241">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-5241">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5242">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-5242">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5243">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-5243">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5245">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5245">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5246">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-5246">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5247">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-5247">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-5248">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-5248">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-5249">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-5249">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-5250">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-5250">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-5251">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-5251">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-5252">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5252">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5254">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5254">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5256">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5256">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5258">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-5258">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-5259">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-5259">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="bf787-5260">DXGI_FORMAT_P010<sup>V</sup> (104)</span><span class="sxs-lookup"><span data-stu-id="bf787-5260">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="bf787-5261">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-5261">Target</span></span> | <span data-ttu-id="bf787-5262">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-5262">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-5263">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-5263">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-5264">16</span><span class="sxs-lookup"><span data-stu-id="bf787-5264">16</span></span> |
| <span data-ttu-id="bf787-5265">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-5265">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5267">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-5267">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5268">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5268">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5269">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5269">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5270">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-5270">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5271">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-5271">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-5272">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-5272">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5274">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-5274">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-5275">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-5275">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-5276">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-5276">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-5277">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-5277">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-5278">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-5278">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-5279">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-5279">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-5280">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-5280">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-5281">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-5281">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-5282">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5282">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-5283">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5283">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-5284">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5284">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5285">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-5285">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5286">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-5286">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-5287">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-5287">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-5288">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-5288">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5289">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-5289">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5290">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-5290">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-5291">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5291">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-5292">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5292">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-5293">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5293">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-5294">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-5294">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-5295">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-5295">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-5296">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5296">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-5297">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-5297">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5298">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-5298">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5299">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-5299">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5301">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5301">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5302">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-5302">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5303">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-5303">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-5304">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-5304">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-5305">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-5305">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-5306">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-5306">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-5307">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-5307">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-5308">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5308">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5310">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5310">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5312">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5312">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5314">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-5314">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-5315">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-5315">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="bf787-5316">DXGI_FORMAT_P016<sup>V</sup> (105)</span><span class="sxs-lookup"><span data-stu-id="bf787-5316">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="bf787-5317">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-5317">Target</span></span> | <span data-ttu-id="bf787-5318">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-5318">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-5319">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-5319">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-5320">16</span><span class="sxs-lookup"><span data-stu-id="bf787-5320">16</span></span> |
| <span data-ttu-id="bf787-5321">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-5321">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5323">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-5323">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5324">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5324">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5325">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5325">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5326">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-5326">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5327">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-5327">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-5328">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-5328">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5330">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-5330">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-5331">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-5331">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-5332">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-5332">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-5333">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-5333">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-5334">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-5334">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-5335">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-5335">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-5336">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-5336">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-5337">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-5337">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-5338">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5338">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-5339">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5339">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-5340">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5340">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5341">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-5341">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5342">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-5342">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-5343">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-5343">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-5344">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-5344">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5345">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-5345">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5346">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-5346">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-5347">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5347">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-5348">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5348">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-5349">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5349">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-5350">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-5350">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-5351">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-5351">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-5352">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5352">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-5353">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-5353">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5354">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-5354">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5355">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-5355">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5357">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5357">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5358">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-5358">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5359">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-5359">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-5360">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-5360">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-5361">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-5361">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-5362">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-5362">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-5363">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-5363">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-5364">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5364">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5366">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5366">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5368">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5368">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5370">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-5370">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-5371">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-5371">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="bf787-5372">DXGI_FORMAT_420 \_ opaco<sup>V</sup> (106)</span><span class="sxs-lookup"><span data-stu-id="bf787-5372">DXGI_FORMAT_420\_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="bf787-5373">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-5373">Target</span></span> | <span data-ttu-id="bf787-5374">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-5374">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-5375">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-5375">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-5376">8</span><span class="sxs-lookup"><span data-stu-id="bf787-5376">8</span></span> |
| <span data-ttu-id="bf787-5377">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-5377">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5379">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-5379">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5380">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5380">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5381">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5381">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5382">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-5382">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5383">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-5383">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-5384">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-5384">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5386">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-5386">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-5387">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-5387">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-5388">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-5388">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-5389">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-5389">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-5390">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-5390">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-5391">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-5391">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-5392">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-5392">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-5393">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-5393">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-5394">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5394">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-5395">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5395">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-5396">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5396">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5397">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-5397">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5398">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-5398">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-5399">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-5399">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-5400">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-5400">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5401">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-5401">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5402">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-5402">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-5403">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5403">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-5404">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5404">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-5405">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5405">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-5406">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-5406">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-5407">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-5407">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-5408">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5408">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-5409">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-5409">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5410">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-5410">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5411">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-5411">CPU Lockable</span></span> | \- |
| <span data-ttu-id="bf787-5412">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5412">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5413">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-5413">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5414">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-5414">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-5415">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-5415">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-5416">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-5416">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-5417">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-5417">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-5418">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-5418">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-5419">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5419">Video Decoder Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5421">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5421">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5423">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5423">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5425">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-5425">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-5426">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-5426">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="bf787-5427">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span><span class="sxs-lookup"><span data-stu-id="bf787-5427">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="bf787-5428">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-5428">Target</span></span> | <span data-ttu-id="bf787-5429">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-5429">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-5430">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-5430">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-5431">16</span><span class="sxs-lookup"><span data-stu-id="bf787-5431">16</span></span> |
| <span data-ttu-id="bf787-5432">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-5432">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5434">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-5434">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5435">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5435">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5436">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5436">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5437">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-5437">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5438">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-5438">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-5439">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-5439">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5441">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-5441">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-5442">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-5442">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-5443">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-5443">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-5444">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-5444">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-5445">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-5445">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-5446">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-5446">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-5447">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-5447">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-5448">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-5448">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-5449">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5449">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-5450">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5450">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-5451">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5451">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5452">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-5452">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5453">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-5453">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-5454">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-5454">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-5455">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-5455">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5456">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-5456">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5457">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-5457">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-5458">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5458">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-5459">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5459">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-5460">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5460">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-5461">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-5461">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-5462">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-5462">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-5463">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5463">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-5464">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-5464">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5465">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-5465">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5466">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-5466">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5468">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5468">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5469">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-5469">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5470">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-5470">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-5471">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-5471">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-5472">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-5472">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-5473">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-5473">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-5474">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-5474">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-5475">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5475">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5477">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5477">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5479">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5479">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5481">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-5481">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-5482">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-5482">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="bf787-5483">DXGI_FORMAT_Y210<sup>V</sup> (108)</span><span class="sxs-lookup"><span data-stu-id="bf787-5483">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="bf787-5484">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-5484">Target</span></span> | <span data-ttu-id="bf787-5485">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-5485">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-5486">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-5486">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-5487">32</span><span class="sxs-lookup"><span data-stu-id="bf787-5487">32</span></span> |
| <span data-ttu-id="bf787-5488">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-5488">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5490">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-5490">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5491">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5491">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5492">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5492">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5493">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-5493">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5494">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-5494">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-5495">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-5495">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5497">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-5497">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-5498">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-5498">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-5499">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-5499">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-5500">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-5500">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-5501">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-5501">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-5502">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-5502">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-5503">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-5503">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-5504">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-5504">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-5505">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5505">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-5506">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5506">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-5507">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5507">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5508">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-5508">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5509">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-5509">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-5510">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-5510">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-5511">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-5511">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5512">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-5512">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5513">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-5513">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-5514">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5514">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-5515">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5515">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-5516">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5516">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-5517">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-5517">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-5518">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-5518">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-5519">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5519">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-5520">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-5520">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5521">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-5521">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5522">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-5522">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5524">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5524">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5525">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-5525">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5526">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-5526">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-5527">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-5527">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-5528">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-5528">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-5529">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-5529">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-5530">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-5530">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-5531">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5531">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5533">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5533">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5535">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5535">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5537">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-5537">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-5538">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-5538">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="bf787-5539">DXGI_FORMAT_Y216<sup>V</sup> (109)</span><span class="sxs-lookup"><span data-stu-id="bf787-5539">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="bf787-5540">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-5540">Target</span></span> | <span data-ttu-id="bf787-5541">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-5541">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-5542">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-5542">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-5543">32</span><span class="sxs-lookup"><span data-stu-id="bf787-5543">32</span></span> |
| <span data-ttu-id="bf787-5544">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-5544">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5546">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-5546">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5547">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5547">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5548">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5548">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5549">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-5549">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5550">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-5550">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-5551">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-5551">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5553">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-5553">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-5554">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-5554">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-5555">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-5555">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-5556">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-5556">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-5557">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-5557">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-5558">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-5558">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-5559">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-5559">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-5560">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-5560">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-5561">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5561">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-5562">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5562">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-5563">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5563">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5564">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-5564">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5565">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-5565">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-5566">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-5566">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-5567">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-5567">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5568">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-5568">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5569">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-5569">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-5570">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5570">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-5571">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5571">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-5572">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5572">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-5573">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-5573">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-5574">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-5574">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-5575">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5575">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-5576">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-5576">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5577">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-5577">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5578">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-5578">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5580">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5580">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5581">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-5581">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5582">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-5582">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-5583">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-5583">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-5584">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-5584">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-5585">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-5585">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-5586">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-5586">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-5587">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5587">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5589">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5589">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5591">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5591">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5593">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-5593">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-5594">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-5594">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="bf787-5595">DXGI_FORMAT_NV11<sup>V</sup> (110)</span><span class="sxs-lookup"><span data-stu-id="bf787-5595">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="bf787-5596">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-5596">Target</span></span> | <span data-ttu-id="bf787-5597">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-5597">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-5598">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-5598">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-5599">8</span><span class="sxs-lookup"><span data-stu-id="bf787-5599">8</span></span> |
| <span data-ttu-id="bf787-5600">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-5600">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5602">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-5602">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5603">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5603">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5604">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5604">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5605">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-5605">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5606">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-5606">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-5607">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-5607">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5609">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-5609">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-5610">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-5610">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-5611">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-5611">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-5612">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-5612">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-5613">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-5613">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-5614">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-5614">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-5615">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-5615">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-5616">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-5616">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-5617">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5617">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-5618">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5618">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-5619">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5619">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5620">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-5620">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5621">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-5621">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-5622">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-5622">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-5623">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-5623">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5624">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-5624">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5625">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-5625">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-5626">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5626">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-5627">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5627">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-5628">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5628">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-5629">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-5629">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-5630">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-5630">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-5631">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5631">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-5632">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-5632">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5633">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-5633">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5634">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-5634">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5636">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5636">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5637">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-5637">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5638">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-5638">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-5639">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-5639">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-5640">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-5640">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-5641">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-5641">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-5642">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-5642">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-5643">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5643">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5645">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5645">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5647">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5647">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5649">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-5649">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-5650">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-5650">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="bf787-5651">DXGI_FORMAT_AI44<sup>V</sup> (111)</span><span class="sxs-lookup"><span data-stu-id="bf787-5651">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="bf787-5652">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-5652">Target</span></span> | <span data-ttu-id="bf787-5653">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-5653">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-5654">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-5654">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-5655">8</span><span class="sxs-lookup"><span data-stu-id="bf787-5655">8</span></span> |
| <span data-ttu-id="bf787-5656">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-5656">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5658">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-5658">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5659">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5659">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5660">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5660">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5661">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-5661">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5662">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-5662">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-5663">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-5663">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5665">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-5665">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-5666">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-5666">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-5667">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-5667">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-5668">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-5668">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-5669">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-5669">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-5670">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-5670">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-5671">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-5671">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-5672">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-5672">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-5673">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5673">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-5674">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5674">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-5675">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5675">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5676">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-5676">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5677">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-5677">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-5678">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-5678">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-5679">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-5679">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5680">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-5680">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5681">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-5681">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-5682">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5682">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-5683">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5683">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-5684">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5684">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-5685">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-5685">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-5686">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-5686">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-5687">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5687">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-5688">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-5688">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5689">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-5689">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5690">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-5690">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5692">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5692">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5693">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-5693">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5694">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-5694">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-5695">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-5695">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-5696">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-5696">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-5697">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-5697">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-5698">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-5698">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-5699">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5699">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-5700">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5700">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5702">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5702">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-5703">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-5703">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-5704">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-5704">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="bf787-5705">DXGI_FORMAT_IA44<sup>V</sup> (112)</span><span class="sxs-lookup"><span data-stu-id="bf787-5705">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="bf787-5706">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-5706">Target</span></span> | <span data-ttu-id="bf787-5707">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-5707">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-5708">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-5708">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-5709">8</span><span class="sxs-lookup"><span data-stu-id="bf787-5709">8</span></span> |
| <span data-ttu-id="bf787-5710">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-5710">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5712">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-5712">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5713">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5713">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5714">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5714">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5715">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-5715">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5716">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-5716">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-5717">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-5717">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5719">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-5719">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-5720">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-5720">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-5721">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-5721">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-5722">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-5722">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-5723">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-5723">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-5724">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-5724">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-5725">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-5725">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-5726">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-5726">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-5727">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5727">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-5728">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5728">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-5729">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5729">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5730">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-5730">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5731">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-5731">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-5732">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-5732">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-5733">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-5733">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5734">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-5734">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5735">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-5735">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-5736">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5736">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-5737">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5737">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-5738">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5738">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-5739">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-5739">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-5740">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-5740">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-5741">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5741">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-5742">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-5742">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5743">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-5743">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5744">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-5744">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5746">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5746">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5747">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-5747">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5748">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-5748">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-5749">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-5749">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-5750">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-5750">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-5751">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-5751">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-5752">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-5752">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-5753">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5753">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-5754">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5754">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5756">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5756">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-5757">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-5757">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-5758">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-5758">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="bf787-5759">DXGI_FORMAT_P8<sup>V</sup> (113)</span><span class="sxs-lookup"><span data-stu-id="bf787-5759">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="bf787-5760">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-5760">Target</span></span> | <span data-ttu-id="bf787-5761">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-5761">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-5762">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-5762">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-5763">8</span><span class="sxs-lookup"><span data-stu-id="bf787-5763">8</span></span> |
| <span data-ttu-id="bf787-5764">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-5764">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5766">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-5766">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5767">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5767">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5768">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5768">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5769">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-5769">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5770">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-5770">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-5771">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-5771">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5773">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-5773">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-5774">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-5774">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-5775">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-5775">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-5776">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-5776">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-5777">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-5777">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-5778">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-5778">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-5779">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-5779">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-5780">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-5780">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-5781">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5781">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-5782">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5782">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-5783">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5783">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5784">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-5784">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5785">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-5785">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-5786">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-5786">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-5787">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-5787">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5788">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-5788">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5789">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-5789">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-5790">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5790">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-5791">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5791">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-5792">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5792">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-5793">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-5793">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-5794">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-5794">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-5795">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5795">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-5796">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-5796">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5797">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-5797">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5798">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-5798">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5800">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5800">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5801">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-5801">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5802">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-5802">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-5803">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-5803">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-5804">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-5804">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-5805">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-5805">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-5806">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-5806">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-5807">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5807">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-5808">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5808">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5810">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5810">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-5811">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-5811">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-5812">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-5812">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="bf787-5813">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span><span class="sxs-lookup"><span data-stu-id="bf787-5813">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="bf787-5814">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-5814">Target</span></span> | <span data-ttu-id="bf787-5815">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-5815">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-5816">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-5816">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-5817">16</span><span class="sxs-lookup"><span data-stu-id="bf787-5817">16</span></span> |
| <span data-ttu-id="bf787-5818">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-5818">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="bf787-5820">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-5820">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5821">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5821">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5822">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5822">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5823">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-5823">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5824">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-5824">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-5825">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-5825">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5827">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-5827">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-5828">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-5828">TextureCube</span></span> | \- |
| <span data-ttu-id="bf787-5829">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-5829">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="bf787-5830">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-5830">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="bf787-5831">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-5831">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-5832">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-5832">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-5833">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-5833">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-5834">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-5834">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-5835">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5835">Mipmap</span></span> | \- |
| <span data-ttu-id="bf787-5836">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5836">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-5837">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5837">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5838">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-5838">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5839">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-5839">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-5840">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-5840">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-5841">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-5841">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5842">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-5842">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5843">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-5843">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-5844">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5844">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-5845">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5845">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-5846">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5846">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-5847">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-5847">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-5848">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-5848">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-5849">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5849">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-5850">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-5850">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5851">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-5851">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5852">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-5852">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5854">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5854">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5855">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-5855">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5856">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-5856">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-5857">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-5857">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-5858">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-5858">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-5859">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-5859">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-5860">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-5860">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-5861">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5861">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-5862">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5862">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5864">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5864">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-5865">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-5865">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-5866">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-5866">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a><span data-ttu-id="bf787-5867">DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>FNS</sup> (115)</span><span class="sxs-lookup"><span data-stu-id="bf787-5867">DXGI_FORMAT_B4G4R4A4\_UNORM<sup>FNS</sup> (115)</span></span>
| <span data-ttu-id="bf787-5868">Destino</span><span class="sxs-lookup"><span data-stu-id="bf787-5868">Target</span></span> | <span data-ttu-id="bf787-5869">Suporte</span><span class="sxs-lookup"><span data-stu-id="bf787-5869">Support</span></span> |
| - | - |
| <span data-ttu-id="bf787-5870">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="bf787-5870">Bits Per Element (BPE)</span></span> | <span data-ttu-id="bf787-5871">16</span><span class="sxs-lookup"><span data-stu-id="bf787-5871">16</span></span> |
| <span data-ttu-id="bf787-5872">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-5872">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5874">Buffer</span><span class="sxs-lookup"><span data-stu-id="bf787-5874">Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5875">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5875">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5876">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="bf787-5876">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5877">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="bf787-5877">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="bf787-5878">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf787-5878">Texture1D</span></span> | \- |
| <span data-ttu-id="bf787-5879">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf787-5879">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5881">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf787-5881">Texture3D</span></span> | \- |
| <span data-ttu-id="bf787-5882">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf787-5882">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5884">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="bf787-5884">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5886">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="bf787-5886">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5888">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="bf787-5888">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="bf787-5889">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="bf787-5889">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="bf787-5890">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="bf787-5890">Shader gather4</span></span> | \- |
| <span data-ttu-id="bf787-5891">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="bf787-5891">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="bf787-5892">Mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5892">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5894">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="bf787-5894">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="bf787-5895">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5895">RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5896">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="bf787-5896">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5897">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="bf787-5897">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="bf787-5898">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="bf787-5898">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="bf787-5899">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="bf787-5899">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5900">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="bf787-5900">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="bf787-5901">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="bf787-5901">Typed UAV</span></span> | \- |
| <span data-ttu-id="bf787-5902">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5902">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="bf787-5903">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5903">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="bf787-5904">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5904">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="bf787-5905">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="bf787-5905">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="bf787-5906">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="bf787-5906">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="bf787-5907">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="bf787-5907">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="bf787-5908">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="bf787-5908">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5909">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="bf787-5909">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="bf787-5910">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="bf787-5910">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="bf787-5912">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="bf787-5912">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5913">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="bf787-5913">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="bf787-5914">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="bf787-5914">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="bf787-5915">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="bf787-5915">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="bf787-5916">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="bf787-5916">Multisample Load</span></span> | \- |
| <span data-ttu-id="bf787-5917">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="bf787-5917">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="bf787-5918">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="bf787-5918">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="bf787-5919">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5919">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="bf787-5920">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5920">Video Processor Input</span></span> | \- |
| <span data-ttu-id="bf787-5921">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5921">Video Processor Output</span></span> | \- |
| <span data-ttu-id="bf787-5922">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="bf787-5922">Shared Resource</span></span> | \- |
| <span data-ttu-id="bf787-5923">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="bf787-5923">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="bf787-5924">Observações de formato</span><span class="sxs-lookup"><span data-stu-id="bf787-5924">Format notes</span></span>

<span data-ttu-id="bf787-5925">A finalidade do formato pode mudar de um nível de recurso de hardware para o próximo.</span><span class="sxs-lookup"><span data-stu-id="bf787-5925">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="bf787-5926"><sup>L</sup> : formato de tipo informativo</span><span class="sxs-lookup"><span data-stu-id="bf787-5926"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="bf787-5927"><sup>PCs</sup> : layout de tipo parcial, convertido e simples</span><span class="sxs-lookup"><span data-stu-id="bf787-5927"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="bf787-5928"><sup>FCS</sup> : layout totalmente tipado, convertido e simples</span><span class="sxs-lookup"><span data-stu-id="bf787-5928"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="bf787-5929"><sup>FNS</sup> : layout totalmente tipado, não-convertido e simples</span><span class="sxs-lookup"><span data-stu-id="bf787-5929"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="bf787-5930"><sup>PCC</sup> : layout complexo, convertido e de tipo parcial</span><span class="sxs-lookup"><span data-stu-id="bf787-5930"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="bf787-5931"><sup>FCC</sup> : layout totalmente tipado, convertido e complexo</span><span class="sxs-lookup"><span data-stu-id="bf787-5931"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="bf787-5932"><sup>FNC</sup> : layout totalmente tipado, não-convertido e complexo</span><span class="sxs-lookup"><span data-stu-id="bf787-5932"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="bf787-5933"><sup>V</sup> : formato de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf787-5933"><sup>V</sup> : video format</span></span>
</dt> </dl>

## <a name="related-topics"></a><span data-ttu-id="bf787-5934">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bf787-5934">Related topics</span></span>

[<span data-ttu-id="bf787-5935">Níveis de recursos de hardware do D3D12</span><span class="sxs-lookup"><span data-stu-id="bf787-5935">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

<span data-ttu-id="bf787-5936">[Implementando buffers de sombra para o nível de recurso do Direct3D 9](/previous-versions/windows/apps/jj262110(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="bf787-5936">[Implementing shadow buffers for Direct3D feature level 9](/previous-versions/windows/apps/jj262110(v=win.10))</span></span>

[<span data-ttu-id="bf787-5937">Mapeando formatos herdados</span><span class="sxs-lookup"><span data-stu-id="bf787-5937">Mapping Legacy Formats</span></span>](../direct3d10/d3d10-graphics-programming-guide-resources-legacy-formats.md)

[<span data-ttu-id="bf787-5938">Guia de programação para DXGI</span><span class="sxs-lookup"><span data-stu-id="bf787-5938">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
