---
description: Esta seção especifica os formatos ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valores) que têm suporte no hardware do recurso Direct3D 10Level9 9,3.
ms.assetid: B2A843D5-6A6B-4180-8B94-D032B1322798
title: Suporte de formato para hardware 9.3 do Nível de 10Recursos9 do Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79185ddb360fe9359371671e3722372c3a1615f9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104009924"
---
# <a name="format-support-for-direct3d-feature-10level9-93-hardware"></a><span data-ttu-id="f42ab-103">Suporte de formato para hardware 9.3 do Nível de 10Recursos9 do Direct3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-103">Format support for Direct3D Feature 10Level9 9.3 hardware</span></span>

<span data-ttu-id="f42ab-104">Esta seção especifica os formatos ([_\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valores) que têm suporte no hardware do recurso Direct3D 10Level9 9,3.</span><span class="sxs-lookup"><span data-stu-id="f42ab-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature 10Level9 9.3 hardware.</span></span>

<span data-ttu-id="f42ab-105">A tabela resume o suporte a recursos, usando a chave a seguir.</span><span class="sxs-lookup"><span data-stu-id="f42ab-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="f42ab-106">Símbolo</span><span class="sxs-lookup"><span data-stu-id="f42ab-106">Symbol</span></span>                            | <span data-ttu-id="f42ab-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f42ab-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="f42ab-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="f42ab-108">_ *-*\*</span></span>                             | <span data-ttu-id="f42ab-109">Não permitido ou não disponível.</span><span class="sxs-lookup"><span data-stu-id="f42ab-109">Disallowed or not available.</span></span>                                                  |
| ![exigido](images/letter-r.jpg)  | <span data-ttu-id="f42ab-111">O suporte a hardware é necessário.</span><span class="sxs-lookup"><span data-stu-id="f42ab-111">Hardware support is required.</span></span>                                                 |
| ![opcionais](images/letter-o.jpg)  | <span data-ttu-id="f42ab-113">Suporte a hardware opcional, o formato pode ou não ser acelerado por hardware.</span><span class="sxs-lookup"><span data-stu-id="f42ab-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![dependentes](images/letter-d.jpg) | <span data-ttu-id="f42ab-115">Necessário se houver suporte para o recurso opcional relacionado.</span><span class="sxs-lookup"><span data-stu-id="f42ab-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="f42ab-116">Este tópico contém uma seção por formato.</span><span class="sxs-lookup"><span data-stu-id="f42ab-116">This topic contains a section per format.</span></span> <span data-ttu-id="f42ab-117">Um *destino* de formato (as tabelas contêm uma linha por destino) pode ser um tipo de recurso, uma função intrínseca HLSL ou uma funcionalidade específica que depende de um formato específico.</span><span class="sxs-lookup"><span data-stu-id="f42ab-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="f42ab-118">Para verificar programaticamente o suporte a Format em D3D11 e D3D12, consulte [verificando o suporte a recursos de hardware](checking-hardware-feature-support.md).</span><span class="sxs-lookup"><span data-stu-id="f42ab-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="f42ab-119">Os números dos formatos são principalmente, mas nem todos, em ordem numérica crescente &mdash; alguns estão fora de ordem numérica e listados junto com outros formatos relevantes.</span><span class="sxs-lookup"><span data-stu-id="f42ab-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="f42ab-120">Observe também que sem *tipo* em um nome de formato pode significar digitação *parcial* e não estritamente tipado (consulte a seção [observações de formato](#format-notes) no final do tópico).</span><span class="sxs-lookup"><span data-stu-id="f42ab-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>

## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="f42ab-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span><span class="sxs-lookup"><span data-stu-id="f42ab-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="f42ab-122">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-122">Target</span></span> | <span data-ttu-id="f42ab-123">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-123">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-124">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-125">0</span><span class="sxs-lookup"><span data-stu-id="f42ab-125">0</span></span> |
| <span data-ttu-id="f42ab-126">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-126">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-127">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-127">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-128">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-128">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-129">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-129">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-130">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-130">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-131">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-131">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-132">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-132">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-133">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-133">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-134">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-134">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-135">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-135">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-136">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-136">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-137">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-137">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-138">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-138">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-139">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-139">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-140">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-140">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-141">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-141">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-142">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-142">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-143">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-143">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-144">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-144">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-145">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-145">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-146">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-146">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-147">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-147">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-148">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-148">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-149">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-149">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-150">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-150">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-151">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-151">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-152">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-152">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-153">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-153">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-154">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-154">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-155">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-155">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-156">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-156">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-157">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-157">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-158">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-158">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-159">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-159">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-160">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-160">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-161">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-161">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-162">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-162">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-163">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-163">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-164">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-164">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-165">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-165">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-166">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-166">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-167">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-167">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-168">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-168">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-169">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-169">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-170">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-170">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="f42ab-171">DXGI_FORMAT_R32G32B32A32 \_ <sup>PCs</sup> não tipados (1)</span><span class="sxs-lookup"><span data-stu-id="f42ab-171">DXGI_FORMAT_R32G32B32A32\_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="f42ab-172">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-172">Target</span></span> | <span data-ttu-id="f42ab-173">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-173">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-174">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-174">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-175">128</span><span class="sxs-lookup"><span data-stu-id="f42ab-175">128</span></span> |
| <span data-ttu-id="f42ab-176">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-176">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-177">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-177">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-178">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-178">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-179">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-179">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-180">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-180">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-181">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-181">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-182">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-182">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-183">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-183">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-184">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-184">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-185">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-185">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-186">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-186">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-187">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-187">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-188">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-188">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-189">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-189">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-190">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-190">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-191">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-191">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-192">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-192">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-193">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-193">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-194">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-194">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-195">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-195">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-196">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-196">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-197">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-197">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-198">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-198">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-199">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-199">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-200">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-200">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-201">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-201">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-202">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-202">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-203">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-203">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-204">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-204">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-205">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-205">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-206">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-206">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-207">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-207">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-208">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-208">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-209">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-209">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-210">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-210">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-211">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-211">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-212">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-212">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-213">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-213">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-214">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-214">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-215">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-215">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-216">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-216">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-217">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-217">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-218">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-218">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-219">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-219">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-220">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-220">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfnssup-2"></a><span data-ttu-id="f42ab-221">DXGI_FORMAT_R32G32B32A32 \_ float<sup>FNS</sup> (2)</span><span class="sxs-lookup"><span data-stu-id="f42ab-221">DXGI_FORMAT_R32G32B32A32\_FLOAT<sup>FNS</sup> (2)</span></span>
| <span data-ttu-id="f42ab-222">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-222">Target</span></span> | <span data-ttu-id="f42ab-223">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-223">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-224">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-224">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-225">128</span><span class="sxs-lookup"><span data-stu-id="f42ab-225">128</span></span> |
| <span data-ttu-id="f42ab-226">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-226">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-228">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-228">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-229">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-229">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-231">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-231">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-232">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-232">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-233">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-233">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-234">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-234">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-236">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-236">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-238">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-238">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-240">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-240">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-242">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-242">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-243">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-243">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-244">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-244">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-245">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-245">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-246">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-246">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-247">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-247">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-249">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-249">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-251">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-251">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-253">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-253">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-254">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-254">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-255">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-255">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-256">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-256">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-257">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-257">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-258">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-258">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-259">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-259">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-260">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-260">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-261">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-261">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-262">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-262">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-263">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-263">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-264">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-264">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-265">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-265">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-266">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-266">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-267">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-267">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-269">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-269">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-271">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-271">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-273">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-273">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-275">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-275">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-277">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-277">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-278">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-278">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-279">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-279">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-280">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-280">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-281">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-281">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-282">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-282">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-283">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-283">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-284">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-284">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfnssup-3"></a><span data-ttu-id="f42ab-285">DXGI_FORMAT_R32G32B32A32 \_ uint<sup>FNS</sup> (3)</span><span class="sxs-lookup"><span data-stu-id="f42ab-285">DXGI_FORMAT_R32G32B32A32\_UINT<sup>FNS</sup> (3)</span></span>
| <span data-ttu-id="f42ab-286">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-286">Target</span></span> | <span data-ttu-id="f42ab-287">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-287">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-288">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-288">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-289">128</span><span class="sxs-lookup"><span data-stu-id="f42ab-289">128</span></span> |
| <span data-ttu-id="f42ab-290">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-290">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-291">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-291">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-292">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-292">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-293">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-293">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-294">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-294">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-295">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-295">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-296">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-296">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-297">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-297">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-298">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-298">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-299">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-299">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-300">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-300">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-301">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-301">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-302">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-302">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-303">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-303">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-304">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-304">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-305">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-305">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-306">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-306">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-307">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-307">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-308">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-308">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-309">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-309">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-310">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-310">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-311">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-311">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-312">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-312">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-313">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-313">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-314">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-314">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-315">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-315">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-316">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-316">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-317">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-317">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-318">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-318">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-319">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-319">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-320">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-320">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-321">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-321">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-322">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-322">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-323">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-323">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-324">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-324">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-325">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-325">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-326">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-326">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-327">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-327">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-328">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-328">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-329">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-329">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-330">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-330">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-331">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-331">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-332">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-332">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-333">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-333">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-334">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-334">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfnssup-4"></a><span data-ttu-id="f42ab-335">DXGI_FORMAT_R32G32B32A32 \_ Santo<sup>FNS</sup> (4)</span><span class="sxs-lookup"><span data-stu-id="f42ab-335">DXGI_FORMAT_R32G32B32A32\_SINT<sup>FNS</sup> (4)</span></span>
| <span data-ttu-id="f42ab-336">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-336">Target</span></span> | <span data-ttu-id="f42ab-337">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-337">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-338">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-338">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-339">128</span><span class="sxs-lookup"><span data-stu-id="f42ab-339">128</span></span> |
| <span data-ttu-id="f42ab-340">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-340">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-341">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-341">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-342">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-342">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-343">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-343">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-344">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-344">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-345">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-345">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-346">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-346">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-347">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-347">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-348">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-348">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-349">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-349">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-350">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-350">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-351">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-351">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-352">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-352">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-353">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-353">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-354">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-354">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-355">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-355">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-356">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-356">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-357">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-357">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-358">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-358">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-359">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-359">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-360">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-360">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-361">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-361">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-362">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-362">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-363">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-363">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-364">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-364">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-365">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-365">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-366">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-366">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-367">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-367">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-368">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-368">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-369">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-369">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-370">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-370">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-371">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-371">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-372">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-372">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-373">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-373">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-374">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-374">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-375">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-375">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-376">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-376">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-377">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-377">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-378">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-378">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-379">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-379">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-380">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-380">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-381">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-381">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-382">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-382">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-383">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-383">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-384">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-384">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="f42ab-385">DXGI_FORMAT_R32G32B32 \_ <sup>PCs</sup> não tipados (5)</span><span class="sxs-lookup"><span data-stu-id="f42ab-385">DXGI_FORMAT_R32G32B32\_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="f42ab-386">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-386">Target</span></span> | <span data-ttu-id="f42ab-387">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-387">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-388">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-388">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-389">96</span><span class="sxs-lookup"><span data-stu-id="f42ab-389">96</span></span> |
| <span data-ttu-id="f42ab-390">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-390">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-391">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-391">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-392">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-392">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-393">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-393">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-394">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-394">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-395">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-395">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-396">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-396">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-397">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-397">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-398">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-398">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-399">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-399">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-400">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-400">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-401">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-401">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-402">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-402">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-403">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-403">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-404">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-404">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-405">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-405">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-406">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-406">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-407">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-407">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-408">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-408">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-409">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-409">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-410">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-410">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-411">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-411">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-412">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-412">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-413">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-413">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-414">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-414">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-415">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-415">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-416">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-416">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-417">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-417">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-418">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-418">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-419">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-419">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-420">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-420">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-421">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-421">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-422">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-422">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-423">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-423">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-424">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-424">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-425">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-425">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-426">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-426">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-427">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-427">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-428">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-428">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-429">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-429">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-430">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-430">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-431">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-431">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-432">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-432">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-433">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-433">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-434">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-434">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfnssup-6"></a><span data-ttu-id="f42ab-435">DXGI_FORMAT_R32G32B32 \_ float<sup>FNS</sup> (6)</span><span class="sxs-lookup"><span data-stu-id="f42ab-435">DXGI_FORMAT_R32G32B32\_FLOAT<sup>FNS</sup> (6)</span></span>
| <span data-ttu-id="f42ab-436">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-436">Target</span></span> | <span data-ttu-id="f42ab-437">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-437">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-438">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-438">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-439">96</span><span class="sxs-lookup"><span data-stu-id="f42ab-439">96</span></span> |
| <span data-ttu-id="f42ab-440">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-440">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-442">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-442">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-443">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-443">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-445">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-445">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-446">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-446">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-447">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-447">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-448">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-448">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-449">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-449">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-450">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-450">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-451">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-451">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-452">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-452">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-453">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-453">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-454">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-454">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-455">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-455">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-456">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-456">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-457">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-457">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-458">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-458">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-459">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-459">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-460">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-460">Blendable RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="f42ab-462">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-462">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-463">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-463">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-464">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-464">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-465">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-465">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-466">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-466">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-467">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-467">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-468">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-468">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-469">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-469">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-470">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-470">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-471">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-471">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-472">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-472">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-473">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-473">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-474">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-474">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-475">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-475">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-476">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-476">4x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="f42ab-478">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-478">8x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="f42ab-480">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-480">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-481">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-481">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-482">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-482">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-483">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-483">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-484">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-484">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-485">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-485">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-486">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-486">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-487">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-487">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-488">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-488">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-489">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-489">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfnssup-7"></a><span data-ttu-id="f42ab-490">DXGI_FORMAT_R32G32B32 \_ uint<sup>FNS</sup> (7)</span><span class="sxs-lookup"><span data-stu-id="f42ab-490">DXGI_FORMAT_R32G32B32\_UINT<sup>FNS</sup> (7)</span></span>
| <span data-ttu-id="f42ab-491">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-491">Target</span></span> | <span data-ttu-id="f42ab-492">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-492">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-493">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-493">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-494">96</span><span class="sxs-lookup"><span data-stu-id="f42ab-494">96</span></span> |
| <span data-ttu-id="f42ab-495">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-495">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-496">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-496">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-497">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-497">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-498">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-498">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-499">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-499">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-500">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-500">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-501">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-501">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-502">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-502">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-503">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-503">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-504">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-504">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-505">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-505">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-506">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-506">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-507">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-507">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-508">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-508">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-509">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-509">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-510">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-510">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-511">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-511">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-512">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-512">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-513">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-513">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-514">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-514">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-515">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-515">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-516">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-516">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-517">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-517">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-518">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-518">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-519">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-519">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-520">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-520">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-521">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-521">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-522">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-522">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-523">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-523">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-524">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-524">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-525">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-525">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-526">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-526">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-527">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-527">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-528">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-528">4x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="f42ab-530">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-530">8x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="f42ab-532">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-532">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-533">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-533">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-534">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-534">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-535">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-535">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-536">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-536">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-537">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-537">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-538">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-538">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-539">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-539">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-540">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-540">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-541">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-541">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfnssup-8"></a><span data-ttu-id="f42ab-542">DXGI_FORMAT_R32G32B32 \_ Santo<sup>FNS</sup> (8)</span><span class="sxs-lookup"><span data-stu-id="f42ab-542">DXGI_FORMAT_R32G32B32\_SINT<sup>FNS</sup> (8)</span></span>
| <span data-ttu-id="f42ab-543">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-543">Target</span></span> | <span data-ttu-id="f42ab-544">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-544">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-545">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-545">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-546">96</span><span class="sxs-lookup"><span data-stu-id="f42ab-546">96</span></span> |
| <span data-ttu-id="f42ab-547">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-547">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-548">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-548">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-549">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-549">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-550">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-550">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-551">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-551">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-552">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-552">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-553">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-553">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-554">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-554">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-555">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-555">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-556">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-556">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-557">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-557">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-558">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-558">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-559">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-559">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-560">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-560">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-561">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-561">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-562">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-562">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-563">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-563">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-564">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-564">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-565">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-565">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-566">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-566">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-567">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-567">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-568">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-568">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-569">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-569">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-570">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-570">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-571">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-571">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-572">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-572">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-573">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-573">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-574">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-574">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-575">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-575">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-576">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-576">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-577">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-577">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-578">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-578">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-579">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-579">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-580">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-580">4x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="f42ab-582">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-582">8x Multisample RenderTarget</span></span> | ![dependentes](images/letter-d.jpg) |
| <span data-ttu-id="f42ab-584">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-584">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-585">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-585">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-586">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-586">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-587">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-587">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-588">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-588">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-589">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-589">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-590">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-590">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-591">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-591">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-592">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-592">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-593">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-593">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="f42ab-594">DXGI_FORMAT_R16G16B16A16 \_ <sup>PCs</sup> não tipados (9)</span><span class="sxs-lookup"><span data-stu-id="f42ab-594">DXGI_FORMAT_R16G16B16A16\_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="f42ab-595">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-595">Target</span></span> | <span data-ttu-id="f42ab-596">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-596">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-597">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-597">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-598">64</span><span class="sxs-lookup"><span data-stu-id="f42ab-598">64</span></span> |
| <span data-ttu-id="f42ab-599">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-599">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-600">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-600">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-601">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-601">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-602">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-602">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-603">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-603">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-604">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-604">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-605">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-605">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-606">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-606">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-607">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-607">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-608">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-608">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-609">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-609">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-610">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-610">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-611">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-611">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-612">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-612">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-613">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-613">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-614">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-614">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-615">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-615">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-616">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-616">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-617">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-617">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-618">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-618">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-619">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-619">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-620">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-620">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-621">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-621">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-622">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-622">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-623">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-623">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-624">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-624">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-625">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-625">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-626">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-626">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-627">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-627">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-628">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-628">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-629">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-629">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-630">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-630">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-631">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-631">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-632">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-632">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-633">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-633">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-634">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-634">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-635">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-635">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-636">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-636">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-637">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-637">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-638">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-638">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-639">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-639">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-640">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-640">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-641">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-641">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-642">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-642">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-643">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-643">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfnssup-10"></a><span data-ttu-id="f42ab-644">DXGI_FORMAT_R16G16B16A16 \_ float<sup>FNS</sup> (10)</span><span class="sxs-lookup"><span data-stu-id="f42ab-644">DXGI_FORMAT_R16G16B16A16\_FLOAT<sup>FNS</sup> (10)</span></span>
| <span data-ttu-id="f42ab-645">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-645">Target</span></span> | <span data-ttu-id="f42ab-646">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-646">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-647">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-647">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-648">64</span><span class="sxs-lookup"><span data-stu-id="f42ab-648">64</span></span> |
| <span data-ttu-id="f42ab-649">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-649">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-651">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-651">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-652">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-652">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-654">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-654">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-655">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-655">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-656">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-656">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-657">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-657">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-659">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-659">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-661">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-661">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-663">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-663">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-665">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-665">Shader sample (any filter)</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-667">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-667">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-668">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-668">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-669">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-669">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-670">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-670">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-671">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-671">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-673">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-673">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-675">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-675">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-677">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-677">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-679">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-679">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-680">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-680">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-681">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-681">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-682">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-682">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-683">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-683">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-684">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-684">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-685">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-685">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-686">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-686">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-687">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-687">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-688">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-688">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-689">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-689">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-690">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-690">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-691">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-691">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-692">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-692">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-694">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-694">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-696">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-696">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-698">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-698">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-700">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-700">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-702">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-702">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-703">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-703">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-704">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-704">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-705">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-705">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-706">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-706">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-707">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-707">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-708">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-708">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-710">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-710">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfnssup-11"></a><span data-ttu-id="f42ab-711">DXGI_FORMAT_R16G16B16A16 \_ UNORM<sup>FNS</sup> (11)</span><span class="sxs-lookup"><span data-stu-id="f42ab-711">DXGI_FORMAT_R16G16B16A16\_UNORM<sup>FNS</sup> (11)</span></span>
| <span data-ttu-id="f42ab-712">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-712">Target</span></span> | <span data-ttu-id="f42ab-713">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-713">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-714">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-714">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-715">64</span><span class="sxs-lookup"><span data-stu-id="f42ab-715">64</span></span> |
| <span data-ttu-id="f42ab-716">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-716">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-718">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-718">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-719">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-719">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-720">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-720">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-721">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-721">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-722">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-722">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-723">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-723">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-725">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-725">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-727">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-727">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-729">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-729">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-731">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-731">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-733">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-733">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-734">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-734">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-735">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-735">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-736">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-736">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-737">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-737">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-739">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-739">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-741">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-741">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-743">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-743">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-744">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-744">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-745">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-745">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-746">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-746">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-747">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-747">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-748">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-748">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-749">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-749">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-750">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-750">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-751">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-751">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-752">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-752">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-753">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-753">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-754">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-754">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-755">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-755">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-756">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-756">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-757">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-757">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-759">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-759">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-761">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-761">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-763">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-763">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-765">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-765">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-767">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-767">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-768">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-768">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-769">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-769">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-770">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-770">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-771">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-771">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-772">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-772">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-773">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-773">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-774">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-774">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfnssup-12"></a><span data-ttu-id="f42ab-775">DXGI_FORMAT_R16G16B16A16 \_ uint<sup>FNS</sup> (12)</span><span class="sxs-lookup"><span data-stu-id="f42ab-775">DXGI_FORMAT_R16G16B16A16\_UINT<sup>FNS</sup> (12)</span></span>
| <span data-ttu-id="f42ab-776">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-776">Target</span></span> | <span data-ttu-id="f42ab-777">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-777">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-778">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-778">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-779">64</span><span class="sxs-lookup"><span data-stu-id="f42ab-779">64</span></span> |
| <span data-ttu-id="f42ab-780">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-780">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-781">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-781">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-782">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-782">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-783">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-783">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-784">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-784">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-785">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-785">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-786">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-786">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-787">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-787">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-788">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-788">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-789">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-789">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-790">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-790">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-791">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-791">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-792">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-792">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-793">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-793">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-794">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-794">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-795">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-795">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-796">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-796">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-797">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-797">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-798">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-798">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-799">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-799">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-800">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-800">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-801">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-801">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-802">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-802">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-803">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-803">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-804">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-804">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-805">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-805">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-806">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-806">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-807">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-807">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-808">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-808">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-809">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-809">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-810">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-810">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-811">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-811">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-812">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-812">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-813">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-813">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-814">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-814">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-815">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-815">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-816">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-816">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-817">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-817">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-818">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-818">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-819">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-819">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-820">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-820">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-821">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-821">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-822">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-822">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-823">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-823">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-824">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-824">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfnssup-13"></a><span data-ttu-id="f42ab-825">DXGI_FORMAT_R16G16B16A16 \_ SNORM<sup>FNS</sup> (13)</span><span class="sxs-lookup"><span data-stu-id="f42ab-825">DXGI_FORMAT_R16G16B16A16\_SNORM<sup>FNS</sup> (13)</span></span>
| <span data-ttu-id="f42ab-826">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-826">Target</span></span> | <span data-ttu-id="f42ab-827">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-827">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-828">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-828">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-829">64</span><span class="sxs-lookup"><span data-stu-id="f42ab-829">64</span></span> |
| <span data-ttu-id="f42ab-830">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-830">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-832">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-832">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-833">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-833">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-835">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-835">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-836">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-836">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-837">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-837">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-838">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-838">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-839">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-839">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-840">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-840">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-841">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-841">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-842">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-842">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-843">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-843">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-844">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-844">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-845">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-845">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-846">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-846">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-847">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-847">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-848">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-848">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-849">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-849">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-850">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-850">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-851">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-851">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-852">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-852">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-853">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-853">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-854">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-854">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-855">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-855">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-856">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-856">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-857">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-857">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-858">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-858">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-859">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-859">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-860">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-860">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-861">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-861">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-862">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-862">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-863">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-863">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-864">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-864">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-865">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-865">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-866">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-866">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-867">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-867">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-868">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-868">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-869">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-869">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-870">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-870">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-871">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-871">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-872">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-872">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-873">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-873">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-874">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-874">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-875">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-875">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-876">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-876">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfnssup-14"></a><span data-ttu-id="f42ab-877">DXGI_FORMAT_R16G16B16A16 \_ Santo<sup>FNS</sup> (14)</span><span class="sxs-lookup"><span data-stu-id="f42ab-877">DXGI_FORMAT_R16G16B16A16\_SINT<sup>FNS</sup> (14)</span></span>
| <span data-ttu-id="f42ab-878">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-878">Target</span></span> | <span data-ttu-id="f42ab-879">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-879">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-880">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-880">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-881">64</span><span class="sxs-lookup"><span data-stu-id="f42ab-881">64</span></span> |
| <span data-ttu-id="f42ab-882">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-882">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-884">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-884">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-885">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-885">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-887">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-887">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-888">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-888">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-889">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-889">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-890">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-890">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-891">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-891">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-892">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-892">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-893">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-893">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-894">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-894">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-895">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-895">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-896">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-896">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-897">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-897">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-898">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-898">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-899">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-899">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-900">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-900">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-901">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-901">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-902">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-902">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-903">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-903">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-904">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-904">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-905">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-905">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-906">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-906">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-907">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-907">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-908">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-908">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-909">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-909">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-910">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-910">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-911">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-911">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-912">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-912">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-913">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-913">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-914">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-914">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-915">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-915">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-916">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-916">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-917">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-917">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-918">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-918">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-919">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-919">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-920">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-920">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-921">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-921">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-922">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-922">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-923">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-923">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-924">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-924">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-925">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-925">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-926">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-926">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-927">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-927">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-928">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-928">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="f42ab-929">DXGI_FORMAT_R32G32 \_ <sup>PCs</sup> não tipados (15)</span><span class="sxs-lookup"><span data-stu-id="f42ab-929">DXGI_FORMAT_R32G32\_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="f42ab-930">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-930">Target</span></span> | <span data-ttu-id="f42ab-931">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-931">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-932">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-932">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-933">64</span><span class="sxs-lookup"><span data-stu-id="f42ab-933">64</span></span> |
| <span data-ttu-id="f42ab-934">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-934">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-935">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-935">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-936">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-936">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-937">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-937">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-938">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-938">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-939">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-939">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-940">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-940">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-941">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-941">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-942">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-942">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-943">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-943">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-944">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-944">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-945">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-945">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-946">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-946">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-947">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-947">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-948">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-948">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-949">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-949">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-950">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-950">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-951">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-951">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-952">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-952">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-953">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-953">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-954">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-954">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-955">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-955">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-956">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-956">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-957">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-957">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-958">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-958">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-959">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-959">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-960">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-960">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-961">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-961">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-962">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-962">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-963">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-963">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-964">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-964">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-965">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-965">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-966">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-966">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-967">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-967">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-968">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-968">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-969">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-969">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-970">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-970">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-971">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-971">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-972">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-972">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-973">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-973">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-974">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-974">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-975">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-975">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-976">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-976">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-977">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-977">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-978">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-978">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_floatsupfnssup-16"></a><span data-ttu-id="f42ab-979">DXGI_FORMAT_R32G32 \_ float<sup>FNS</sup> (16)</span><span class="sxs-lookup"><span data-stu-id="f42ab-979">DXGI_FORMAT_R32G32\_FLOAT<sup>FNS</sup> (16)</span></span>
| <span data-ttu-id="f42ab-980">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-980">Target</span></span> | <span data-ttu-id="f42ab-981">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-981">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-982">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-982">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-983">64</span><span class="sxs-lookup"><span data-stu-id="f42ab-983">64</span></span> |
| <span data-ttu-id="f42ab-984">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-984">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-986">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-986">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-987">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-987">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-989">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-989">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-990">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-990">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-991">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-991">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-992">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-992">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-994">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-994">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-996">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-996">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-998">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-998">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1000">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1000">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1001">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1001">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1002">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1002">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1003">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-1003">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-1004">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-1004">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-1005">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1005">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-1006">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1006">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-1007">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1007">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1009">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-1009">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1010">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-1010">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-1011">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-1011">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-1012">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-1012">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1013">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1013">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1014">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1014">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-1015">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1015">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-1016">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1016">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-1017">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1017">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-1018">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-1018">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-1019">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-1019">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-1020">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1020">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-1021">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-1021">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1022">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1022">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1023">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-1023">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1025">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1025">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-1027">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-1027">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-1029">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-1029">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-1031">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-1031">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1033">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-1033">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-1034">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-1034">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-1035">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-1035">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-1036">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1036">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-1037">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1037">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-1038">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1038">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-1039">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1039">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-1040">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-1040">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_uintsupfnssup-17"></a><span data-ttu-id="f42ab-1041">DXGI_FORMAT_R32G32 \_ uint<sup>FNS</sup> (17)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1041">DXGI_FORMAT_R32G32\_UINT<sup>FNS</sup> (17)</span></span>
| <span data-ttu-id="f42ab-1042">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-1042">Target</span></span> | <span data-ttu-id="f42ab-1043">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-1043">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-1044">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1044">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-1045">64</span><span class="sxs-lookup"><span data-stu-id="f42ab-1045">64</span></span> |
| <span data-ttu-id="f42ab-1046">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-1046">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-1047">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-1047">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1048">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1048">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1049">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1049">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1050">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1050">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1051">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1051">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-1052">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1052">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-1053">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1053">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-1054">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-1054">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-1055">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1055">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-1056">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1056">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1057">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1057">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1058">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1058">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1059">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-1059">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-1060">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-1060">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-1061">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1061">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-1062">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1062">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-1063">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1063">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1064">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-1064">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1065">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-1065">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-1066">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-1066">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-1067">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-1067">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1068">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1068">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1069">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1069">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-1070">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1070">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-1071">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1071">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-1072">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1072">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-1073">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-1073">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-1074">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-1074">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-1075">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1075">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-1076">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-1076">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1077">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1077">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1078">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-1078">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-1079">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1079">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1080">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-1080">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1081">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-1081">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-1082">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-1082">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-1083">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-1083">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-1084">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-1084">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-1085">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-1085">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-1086">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1086">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-1087">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1087">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-1088">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1088">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-1089">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1089">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-1090">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-1090">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_sintsupfnssup-18"></a><span data-ttu-id="f42ab-1091">DXGI_FORMAT_R32G32 \_ Santo<sup>FNS</sup> (18)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1091">DXGI_FORMAT_R32G32\_SINT<sup>FNS</sup> (18)</span></span>
| <span data-ttu-id="f42ab-1092">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-1092">Target</span></span> | <span data-ttu-id="f42ab-1093">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-1093">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-1094">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1094">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-1095">64</span><span class="sxs-lookup"><span data-stu-id="f42ab-1095">64</span></span> |
| <span data-ttu-id="f42ab-1096">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-1096">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-1097">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-1097">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1098">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1098">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1099">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1099">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1100">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1100">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1101">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1101">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-1102">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1102">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-1103">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1103">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-1104">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-1104">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-1105">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1105">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-1106">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1106">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1107">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1107">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1108">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1108">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1109">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-1109">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-1110">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-1110">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-1111">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1111">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-1112">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1112">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-1113">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1113">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1114">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-1114">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1115">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-1115">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-1116">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-1116">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-1117">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-1117">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1118">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1118">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1119">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1119">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-1120">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1120">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-1121">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1121">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-1122">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1122">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-1123">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-1123">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-1124">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-1124">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-1125">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1125">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-1126">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-1126">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1127">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1127">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1128">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-1128">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-1129">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1129">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1130">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-1130">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1131">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-1131">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-1132">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-1132">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-1133">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-1133">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-1134">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-1134">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-1135">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-1135">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-1136">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1136">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-1137">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1137">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-1138">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1138">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-1139">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1139">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-1140">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-1140">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a><span data-ttu-id="f42ab-1141">DXGI_FORMAT_R32G8X24 \_ <sup>PCs</sup> não tipados (19)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1141">DXGI_FORMAT_R32G8X24\_TYPELESS<sup>PCS</sup> (19)</span></span>
| <span data-ttu-id="f42ab-1142">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-1142">Target</span></span> | <span data-ttu-id="f42ab-1143">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-1143">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-1144">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1144">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-1145">64</span><span class="sxs-lookup"><span data-stu-id="f42ab-1145">64</span></span> |
| <span data-ttu-id="f42ab-1146">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-1146">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-1147">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-1147">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1148">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1148">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1149">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1149">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1150">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1150">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1151">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1151">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-1152">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1152">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-1153">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1153">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-1154">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-1154">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-1155">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1155">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-1156">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1156">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1157">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1157">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1158">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1158">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1159">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-1159">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-1160">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-1160">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-1161">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1161">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-1162">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1162">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-1163">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1163">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1164">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-1164">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1165">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-1165">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-1166">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-1166">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-1167">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-1167">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1168">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1168">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1169">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1169">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-1170">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1170">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-1171">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1171">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-1172">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1172">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-1173">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-1173">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-1174">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-1174">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-1175">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1175">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-1176">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-1176">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1177">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1177">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1178">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-1178">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-1179">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1179">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1180">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-1180">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1181">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-1181">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-1182">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-1182">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-1183">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-1183">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-1184">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-1184">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-1185">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-1185">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-1186">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1186">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-1187">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1187">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-1188">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1188">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-1189">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1189">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-1190">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-1190">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfnssup-20"></a><span data-ttu-id="f42ab-1191">DXGI_FORMAT_D32 \_ float \_ S8X24 \_ uint<sup>FNS</sup> (20)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1191">DXGI_FORMAT_D32\_FLOAT\_S8X24\_UINT<sup>FNS</sup> (20)</span></span>
| <span data-ttu-id="f42ab-1192">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-1192">Target</span></span> | <span data-ttu-id="f42ab-1193">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-1193">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-1194">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1194">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-1195">64</span><span class="sxs-lookup"><span data-stu-id="f42ab-1195">64</span></span> |
| <span data-ttu-id="f42ab-1196">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-1196">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-1197">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-1197">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1198">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1198">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1199">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1199">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1200">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1200">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1201">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1201">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-1202">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1202">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-1203">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1203">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-1204">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-1204">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-1205">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1205">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-1206">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1206">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1207">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1207">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1208">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1208">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1209">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-1209">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-1210">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-1210">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-1211">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1211">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-1212">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1212">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-1213">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1213">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1214">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-1214">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1215">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-1215">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-1216">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-1216">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-1217">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-1217">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1218">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1218">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1219">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1219">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-1220">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1220">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-1221">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1221">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-1222">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1222">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-1223">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-1223">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-1224">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-1224">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-1225">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1225">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-1226">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-1226">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1227">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1227">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1228">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-1228">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-1229">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1229">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1230">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-1230">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1231">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-1231">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-1232">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-1232">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-1233">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-1233">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-1234">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-1234">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-1235">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-1235">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-1236">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1236">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-1237">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1237">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-1238">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1238">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-1239">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1239">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-1240">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-1240">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfnssup-21"></a><span data-ttu-id="f42ab-1241">DXGI_FORMAT_R32 \_ float \_ X8X24 \_ <sup>FNS</sup> (21)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1241">DXGI_FORMAT_R32\_FLOAT\_X8X24\_TYPELESS<sup>FNS</sup> (21)</span></span>
| <span data-ttu-id="f42ab-1242">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-1242">Target</span></span> | <span data-ttu-id="f42ab-1243">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-1243">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-1244">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1244">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-1245">64</span><span class="sxs-lookup"><span data-stu-id="f42ab-1245">64</span></span> |
| <span data-ttu-id="f42ab-1246">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-1246">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-1247">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-1247">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1248">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1248">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1249">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1249">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1250">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1250">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1251">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1251">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-1252">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1252">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-1253">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1253">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-1254">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-1254">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-1255">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1255">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-1256">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1256">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1257">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1257">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1258">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1258">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1259">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-1259">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-1260">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-1260">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-1261">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1261">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-1262">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1262">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-1263">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1263">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1264">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-1264">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1265">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-1265">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-1266">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-1266">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-1267">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-1267">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1268">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1268">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1269">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1269">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-1270">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1270">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-1271">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1271">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-1272">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1272">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-1273">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-1273">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-1274">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-1274">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-1275">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1275">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-1276">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-1276">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1277">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1277">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1278">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-1278">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-1279">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1279">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1280">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-1280">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1281">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-1281">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-1282">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-1282">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-1283">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-1283">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-1284">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-1284">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-1285">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-1285">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-1286">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1286">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-1287">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1287">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-1288">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1288">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-1289">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1289">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-1290">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-1290">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfnssup-22"></a><span data-ttu-id="f42ab-1291">DXGI_FORMAT_X32 \_ \_ \_ <sup>FNS</sup> uintless G8X24 (22)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1291">DXGI_FORMAT_X32\_TYPELESS\_G8X24\_UINT<sup>FNS</sup> (22)</span></span>
| <span data-ttu-id="f42ab-1292">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-1292">Target</span></span> | <span data-ttu-id="f42ab-1293">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-1293">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-1294">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1294">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-1295">64</span><span class="sxs-lookup"><span data-stu-id="f42ab-1295">64</span></span> |
| <span data-ttu-id="f42ab-1296">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-1296">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-1297">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-1297">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1298">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1298">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1299">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1299">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1300">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1300">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1301">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1301">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-1302">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1302">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-1303">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1303">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-1304">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-1304">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-1305">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1305">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-1306">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1306">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1307">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1307">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1308">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1308">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1309">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-1309">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-1310">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-1310">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-1311">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1311">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-1312">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1312">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-1313">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1313">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1314">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-1314">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1315">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-1315">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-1316">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-1316">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-1317">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-1317">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1318">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1318">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1319">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1319">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-1320">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1320">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-1321">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1321">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-1322">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1322">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-1323">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-1323">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-1324">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-1324">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-1325">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1325">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-1326">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-1326">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1327">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1327">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1328">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-1328">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-1329">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1329">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1330">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-1330">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1331">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-1331">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-1332">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-1332">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-1333">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-1333">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-1334">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-1334">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-1335">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-1335">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-1336">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1336">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-1337">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1337">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-1338">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1338">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-1339">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1339">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-1340">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-1340">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="f42ab-1341">DXGI_FORMAT_R10G10B10A2 \_ <sup>PCs</sup> não tipados (23)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1341">DXGI_FORMAT_R10G10B10A2\_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="f42ab-1342">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-1342">Target</span></span> | <span data-ttu-id="f42ab-1343">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-1343">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-1344">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1344">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-1345">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-1345">32</span></span> |
| <span data-ttu-id="f42ab-1346">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-1346">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-1347">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-1347">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1348">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1348">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1349">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1349">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1350">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1350">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1351">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1351">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-1352">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1352">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-1353">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1353">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-1354">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-1354">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-1355">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1355">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-1356">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1356">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1357">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1357">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1358">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1358">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1359">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-1359">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-1360">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-1360">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-1361">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1361">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-1362">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1362">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-1363">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1363">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1364">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-1364">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1365">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-1365">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-1366">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-1366">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-1367">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-1367">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1368">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1368">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1369">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1369">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-1370">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1370">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-1371">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1371">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-1372">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1372">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-1373">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-1373">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-1374">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-1374">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-1375">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1375">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-1376">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-1376">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1377">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1377">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1378">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-1378">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-1379">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1379">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1380">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-1380">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1381">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-1381">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-1382">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-1382">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-1383">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-1383">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-1384">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-1384">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-1385">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-1385">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-1386">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1386">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-1387">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1387">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-1388">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1388">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-1389">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1389">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-1390">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-1390">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfnssup-24"></a><span data-ttu-id="f42ab-1391">DXGI_FORMAT_R10G10B10A2 \_ UNORM<sup>FNS</sup> (24)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1391">DXGI_FORMAT_R10G10B10A2\_UNORM<sup>FNS</sup> (24)</span></span>
| <span data-ttu-id="f42ab-1392">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-1392">Target</span></span> | <span data-ttu-id="f42ab-1393">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-1393">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-1394">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1394">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-1395">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-1395">32</span></span> |
| <span data-ttu-id="f42ab-1396">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-1396">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-1397">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-1397">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1398">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1398">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1399">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1399">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1400">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1400">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1401">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1401">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-1402">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1402">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-1403">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1403">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-1404">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-1404">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-1405">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1405">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-1406">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1406">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1407">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1407">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1408">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1408">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1409">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-1409">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-1410">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-1410">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-1411">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1411">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-1412">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1412">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-1413">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1413">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1414">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-1414">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1415">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-1415">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-1416">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-1416">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-1417">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-1417">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1418">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1418">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1419">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1419">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-1420">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1420">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-1421">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1421">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-1422">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1422">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-1423">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-1423">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-1424">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-1424">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-1425">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1425">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-1426">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-1426">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1427">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1427">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1428">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-1428">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-1429">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1429">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1430">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-1430">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1431">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-1431">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-1432">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-1432">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-1433">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-1433">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-1434">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-1434">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-1435">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-1435">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-1436">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1436">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-1437">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1437">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-1438">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1438">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-1439">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1439">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1441">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-1441">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfnssup-25"></a><span data-ttu-id="f42ab-1442">DXGI_FORMAT_R10G10B10A2 \_ uint<sup>FNS</sup> (25)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1442">DXGI_FORMAT_R10G10B10A2\_UINT<sup>FNS</sup> (25)</span></span>
| <span data-ttu-id="f42ab-1443">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-1443">Target</span></span> | <span data-ttu-id="f42ab-1444">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-1444">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-1445">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1445">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-1446">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-1446">32</span></span> |
| <span data-ttu-id="f42ab-1447">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-1447">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-1448">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-1448">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1449">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1449">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1450">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1450">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1451">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1451">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1452">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1452">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-1453">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1453">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-1454">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1454">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-1455">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-1455">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-1456">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1456">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-1457">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1457">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1458">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1458">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1459">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1459">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1460">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-1460">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-1461">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-1461">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-1462">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1462">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-1463">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1463">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-1464">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1464">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1465">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-1465">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1466">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-1466">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-1467">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-1467">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-1468">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-1468">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1469">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1469">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1470">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1470">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-1471">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1471">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-1472">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1472">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-1473">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1473">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-1474">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-1474">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-1475">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-1475">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-1476">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1476">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-1477">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-1477">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1478">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1478">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1479">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-1479">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-1480">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1480">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1481">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-1481">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1482">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-1482">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-1483">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-1483">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-1484">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-1484">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-1485">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-1485">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-1486">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-1486">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-1487">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1487">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-1488">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1488">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-1489">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1489">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-1490">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1490">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-1491">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-1491">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfnssup-89"></a><span data-ttu-id="f42ab-1492">DXGI_FORMAT_R10G10B10 \_ XR \_ Bias \_ a2 \_ UNORM<sup>FNS</sup> (89)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1492">DXGI_FORMAT_R10G10B10\_XR\_BIAS\_A2\_UNORM<sup>FNS</sup> (89)</span></span>
| <span data-ttu-id="f42ab-1493">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-1493">Target</span></span> | <span data-ttu-id="f42ab-1494">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-1494">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-1495">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1495">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-1496">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-1496">32</span></span> |
| <span data-ttu-id="f42ab-1497">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-1497">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-1498">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-1498">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1499">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1499">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1500">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1500">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1501">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1501">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1502">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1502">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-1503">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1503">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-1504">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1504">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-1505">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-1505">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-1506">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1506">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-1507">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1507">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1508">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1508">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1509">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1509">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1510">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-1510">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-1511">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-1511">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-1512">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1512">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-1513">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1513">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-1514">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1514">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1515">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-1515">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1516">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-1516">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-1517">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-1517">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-1518">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-1518">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1519">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1519">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1520">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1520">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-1521">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1521">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-1522">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1522">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-1523">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1523">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-1524">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-1524">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-1525">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-1525">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-1526">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1526">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-1527">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-1527">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1528">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1528">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1529">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-1529">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-1530">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1530">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1531">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-1531">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1532">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-1532">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-1533">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-1533">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-1534">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-1534">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-1535">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-1535">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-1536">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-1536">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-1537">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1537">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-1538">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1538">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-1539">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1539">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-1540">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1540">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-1541">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-1541">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="f42ab-1542">DXGI_FORMAT_R11G11B10 \_ float<sup>FNS</sup> (26)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1542">DXGI_FORMAT_R11G11B10\_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="f42ab-1543">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-1543">Target</span></span> | <span data-ttu-id="f42ab-1544">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-1544">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-1545">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1545">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-1546">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-1546">32</span></span> |
| <span data-ttu-id="f42ab-1547">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-1547">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-1548">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-1548">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1549">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1549">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1550">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1550">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1551">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1551">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1552">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1552">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-1553">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1553">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-1554">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1554">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-1555">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-1555">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-1556">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1556">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-1557">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1557">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1558">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1558">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1559">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1559">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1560">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-1560">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-1561">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-1561">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-1562">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1562">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-1563">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1563">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-1564">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1564">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1565">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-1565">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1566">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-1566">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-1567">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-1567">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-1568">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-1568">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1569">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1569">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1570">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1570">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-1571">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1571">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-1572">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1572">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-1573">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1573">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-1574">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-1574">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-1575">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-1575">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-1576">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1576">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-1577">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-1577">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1578">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1578">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1579">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-1579">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-1580">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1580">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1581">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-1581">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1582">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-1582">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-1583">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-1583">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-1584">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-1584">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-1585">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-1585">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-1586">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-1586">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-1587">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1587">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-1588">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1588">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-1589">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1589">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-1590">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1590">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-1591">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-1591">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="f42ab-1592">DXGI_FORMAT_R8G8B8A8 \_ <sup>PCs</sup> não tipados (27)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1592">DXGI_FORMAT_R8G8B8A8\_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="f42ab-1593">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-1593">Target</span></span> | <span data-ttu-id="f42ab-1594">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-1594">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-1595">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1595">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-1596">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-1596">32</span></span> |
| <span data-ttu-id="f42ab-1597">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-1597">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-1598">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-1598">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1599">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1599">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1600">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1600">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1601">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1601">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1602">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1602">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-1603">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1603">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-1604">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1604">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-1605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-1605">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-1606">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1606">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-1607">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1607">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1608">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1608">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1609">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1609">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1610">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-1610">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-1611">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-1611">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-1612">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1612">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-1613">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1613">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-1614">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1614">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1615">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-1615">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1616">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-1616">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-1617">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-1617">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-1618">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-1618">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1619">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1619">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1620">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1620">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-1621">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1621">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-1622">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1622">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-1623">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1623">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-1624">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-1624">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-1625">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-1625">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-1626">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1626">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-1627">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-1627">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1628">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1628">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1629">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-1629">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-1630">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1630">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1631">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-1631">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1632">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-1632">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-1633">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-1633">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-1634">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-1634">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-1635">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-1635">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-1636">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-1636">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-1637">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1637">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-1638">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1638">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-1639">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1639">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-1640">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1640">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-1641">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-1641">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfnssup-28"></a><span data-ttu-id="f42ab-1642">DXGI_FORMAT_R8G8B8A8 \_ UNORM<sup>FNS</sup> (28)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1642">DXGI_FORMAT_R8G8B8A8\_UNORM<sup>FNS</sup> (28)</span></span>
| <span data-ttu-id="f42ab-1643">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-1643">Target</span></span> | <span data-ttu-id="f42ab-1644">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-1644">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-1645">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1645">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-1646">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-1646">32</span></span> |
| <span data-ttu-id="f42ab-1647">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-1647">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1649">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-1649">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1650">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1650">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1652">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1652">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1653">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1653">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1654">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1654">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-1655">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1655">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1657">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1657">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1659">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-1659">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1661">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1661">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1663">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1663">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1665">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1665">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1666">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1666">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1667">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-1667">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-1668">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-1668">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-1669">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1669">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1671">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1671">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1673">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1673">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1675">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-1675">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1677">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-1677">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-1678">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-1678">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-1679">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-1679">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1680">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1680">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1681">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1681">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-1682">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1682">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-1683">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1683">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-1684">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1684">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-1685">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-1685">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-1686">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-1686">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-1687">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1687">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-1688">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-1688">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1689">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1689">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1690">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-1690">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1692">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1692">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-1694">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-1694">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-1696">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-1696">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-1698">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-1698">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1700">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-1700">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-1701">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-1701">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1703">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-1703">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-1704">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1704">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-1705">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1705">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-1707">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1707">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1709">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1709">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1711">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-1711">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfnssup-29"></a><span data-ttu-id="f42ab-1712">DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ sRGB<sup>FNS</sup> (29)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1712">DXGI_FORMAT_R8G8B8A8\_UNORM\_SRGB<sup>FNS</sup> (29)</span></span>
| <span data-ttu-id="f42ab-1713">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-1713">Target</span></span> | <span data-ttu-id="f42ab-1714">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-1714">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-1715">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1715">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-1716">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-1716">32</span></span> |
| <span data-ttu-id="f42ab-1717">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-1717">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1719">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-1719">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1720">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1720">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1721">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1721">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1722">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1722">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1723">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1723">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-1724">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1724">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1726">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1726">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1728">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-1728">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1730">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1730">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1732">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1732">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1734">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1734">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1735">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1735">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1736">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-1736">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-1737">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-1737">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-1738">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1738">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1740">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1740">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1742">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1742">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1744">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-1744">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1746">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-1746">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-1747">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-1747">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-1748">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-1748">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1749">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1749">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1750">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1750">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-1751">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1751">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-1752">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1752">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-1753">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1753">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-1754">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-1754">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-1755">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-1755">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-1756">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1756">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-1757">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-1757">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1758">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1758">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1759">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-1759">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1761">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1761">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-1763">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-1763">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-1765">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-1765">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-1767">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-1767">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1769">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-1769">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-1770">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-1770">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1772">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-1772">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-1773">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1773">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-1774">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1774">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-1776">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1776">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1778">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1778">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1780">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-1780">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfnssup-30"></a><span data-ttu-id="f42ab-1781">DXGI_FORMAT_R8G8B8A8 \_ uint<sup>FNS</sup> (30)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1781">DXGI_FORMAT_R8G8B8A8\_UINT<sup>FNS</sup> (30)</span></span>
| <span data-ttu-id="f42ab-1782">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-1782">Target</span></span> | <span data-ttu-id="f42ab-1783">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-1783">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-1784">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1784">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-1785">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-1785">32</span></span> |
| <span data-ttu-id="f42ab-1786">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-1786">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1788">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-1788">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1789">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1789">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1791">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1791">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1792">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1792">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1793">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1793">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-1794">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1794">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-1795">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1795">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-1796">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-1796">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-1797">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1797">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-1798">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1798">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1799">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1799">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1800">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1800">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1801">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-1801">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-1802">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-1802">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-1803">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1803">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-1804">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1804">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-1805">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1805">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1806">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-1806">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1807">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-1807">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-1808">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-1808">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-1809">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-1809">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1810">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1810">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1811">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1811">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-1812">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1812">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-1813">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1813">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-1814">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1814">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-1815">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-1815">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-1816">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-1816">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-1817">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1817">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-1818">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-1818">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1819">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1819">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1820">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-1820">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-1821">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1821">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1822">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-1822">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1823">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-1823">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-1824">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-1824">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-1825">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-1825">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-1826">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-1826">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-1827">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-1827">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-1828">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1828">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-1829">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1829">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-1830">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1830">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-1831">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1831">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-1832">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-1832">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfnssup-31"></a><span data-ttu-id="f42ab-1833">DXGI_FORMAT_R8G8B8A8 \_ SNORM<sup>FNS</sup> (31)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1833">DXGI_FORMAT_R8G8B8A8\_SNORM<sup>FNS</sup> (31)</span></span>
| <span data-ttu-id="f42ab-1834">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-1834">Target</span></span> | <span data-ttu-id="f42ab-1835">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-1835">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-1836">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1836">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-1837">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-1837">32</span></span> |
| <span data-ttu-id="f42ab-1838">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-1838">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1840">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-1840">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1841">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1841">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1842">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1842">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1843">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1843">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1844">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1844">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-1845">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1845">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1847">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1847">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-1848">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-1848">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1850">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1850">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1852">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1852">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1854">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1854">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1855">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1855">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1856">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-1856">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-1857">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-1857">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-1858">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1858">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1860">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1860">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-1861">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1861">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1862">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-1862">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1863">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-1863">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-1864">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-1864">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-1865">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-1865">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1866">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1866">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1867">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1867">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-1868">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1868">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-1869">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1869">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-1870">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1870">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-1871">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-1871">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-1872">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-1872">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-1873">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1873">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-1874">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-1874">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1875">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1875">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1876">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-1876">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1878">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1878">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1879">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-1879">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1880">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-1880">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-1881">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-1881">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-1882">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-1882">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-1883">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-1883">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-1884">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-1884">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-1885">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1885">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-1886">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1886">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-1887">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1887">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-1888">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1888">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-1889">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-1889">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfnssup-32"></a><span data-ttu-id="f42ab-1890">DXGI_FORMAT_R8G8B8A8 \_ Santo<sup>FNS</sup> (32)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1890">DXGI_FORMAT_R8G8B8A8\_SINT<sup>FNS</sup> (32)</span></span>
| <span data-ttu-id="f42ab-1891">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-1891">Target</span></span> | <span data-ttu-id="f42ab-1892">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-1892">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-1893">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1893">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-1894">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-1894">32</span></span> |
| <span data-ttu-id="f42ab-1895">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-1895">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-1896">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-1896">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1897">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1897">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1898">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1898">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1899">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1899">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1900">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1900">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-1901">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1901">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-1902">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1902">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-1903">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-1903">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-1904">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1904">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-1905">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1905">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1906">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1906">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1907">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1907">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1908">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-1908">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-1909">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-1909">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-1910">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1910">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-1911">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1911">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-1912">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1912">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1913">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-1913">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1914">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-1914">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-1915">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-1915">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-1916">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-1916">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1917">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1917">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1918">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1918">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-1919">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1919">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-1920">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1920">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-1921">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1921">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-1922">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-1922">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-1923">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-1923">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-1924">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1924">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-1925">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-1925">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1926">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1926">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1927">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-1927">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-1928">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1928">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1929">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-1929">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1930">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-1930">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-1931">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-1931">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-1932">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-1932">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-1933">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-1933">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-1934">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-1934">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-1935">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1935">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-1936">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1936">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-1937">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1937">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-1938">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1938">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-1939">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-1939">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="f42ab-1940">DXGI_FORMAT_R16G16 \_ <sup>PCs</sup> não tipados (33)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1940">DXGI_FORMAT_R16G16\_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="f42ab-1941">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-1941">Target</span></span> | <span data-ttu-id="f42ab-1942">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-1942">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-1943">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1943">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-1944">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-1944">32</span></span> |
| <span data-ttu-id="f42ab-1945">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-1945">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-1946">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-1946">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1947">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1947">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1948">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1948">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1949">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1949">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1950">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1950">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-1951">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1951">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-1952">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-1952">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-1953">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-1953">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-1954">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1954">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-1955">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1955">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1956">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1956">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1957">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1957">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-1958">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-1958">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-1959">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-1959">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-1960">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1960">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-1961">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-1961">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-1962">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1962">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1963">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-1963">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1964">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-1964">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-1965">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-1965">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-1966">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-1966">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1967">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1967">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-1968">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1968">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-1969">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1969">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-1970">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1970">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-1971">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1971">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-1972">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-1972">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-1973">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-1973">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-1974">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-1974">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-1975">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-1975">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1976">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1976">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-1977">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-1977">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-1978">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-1978">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1979">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-1979">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-1980">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-1980">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-1981">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-1981">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-1982">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-1982">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-1983">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-1983">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-1984">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-1984">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-1985">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1985">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-1986">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1986">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-1987">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-1987">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-1988">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-1988">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-1989">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-1989">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_floatsupfnssup-34"></a><span data-ttu-id="f42ab-1990">DXGI_FORMAT_R16G16 \_ float<sup>FNS</sup> (34)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1990">DXGI_FORMAT_R16G16\_FLOAT<sup>FNS</sup> (34)</span></span>
| <span data-ttu-id="f42ab-1991">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-1991">Target</span></span> | <span data-ttu-id="f42ab-1992">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-1992">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-1993">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-1993">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-1994">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-1994">32</span></span> |
| <span data-ttu-id="f42ab-1995">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-1995">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-1997">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-1997">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-1998">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-1998">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2000">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2000">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2001">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2001">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2002">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2002">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-2003">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2003">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2005">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2005">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2007">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-2007">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2009">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2009">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2011">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2011">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2012">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2012">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2013">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2013">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2014">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-2014">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-2015">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-2015">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-2016">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2016">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2018">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2018">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2020">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2020">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2022">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-2022">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2023">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-2023">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-2024">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-2024">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-2025">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-2025">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2026">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2026">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2027">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2027">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-2028">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2028">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-2029">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2029">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-2030">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2030">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-2031">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-2031">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-2032">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-2032">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-2033">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2033">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-2034">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-2034">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2035">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2035">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2036">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-2036">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2038">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2038">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-2040">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-2040">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-2042">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-2042">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-2044">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-2044">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2046">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-2046">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-2047">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-2047">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-2048">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-2048">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-2049">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2049">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-2050">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2050">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-2051">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2051">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-2052">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2052">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-2053">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-2053">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_unormsupfnssup-35"></a><span data-ttu-id="f42ab-2054">DXGI_FORMAT_R16G16 \_ UNORM<sup>FNS</sup> (35)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2054">DXGI_FORMAT_R16G16\_UNORM<sup>FNS</sup> (35)</span></span>
| <span data-ttu-id="f42ab-2055">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-2055">Target</span></span> | <span data-ttu-id="f42ab-2056">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-2056">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-2057">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2057">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-2058">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-2058">32</span></span> |
| <span data-ttu-id="f42ab-2059">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-2059">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2061">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-2061">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2062">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2062">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2063">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2063">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2064">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2064">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2065">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2065">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-2066">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2066">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2068">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2068">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2070">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-2070">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2072">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2072">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2074">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2074">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2076">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2076">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2077">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2077">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2078">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-2078">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-2079">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-2079">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-2080">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2080">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2082">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2082">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2084">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2084">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2086">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-2086">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2087">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-2087">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-2088">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-2088">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-2089">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-2089">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2090">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2090">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2091">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2091">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-2092">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2092">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-2093">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2093">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-2094">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2094">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-2095">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-2095">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-2096">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-2096">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-2097">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2097">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-2098">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-2098">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2099">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2099">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2100">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-2100">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2102">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2102">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-2104">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-2104">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-2106">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-2106">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-2108">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-2108">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2110">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-2110">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-2111">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-2111">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-2112">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-2112">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-2113">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2113">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-2114">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2114">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-2115">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2115">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-2116">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2116">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-2117">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-2117">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_uintsupfnssup-36"></a><span data-ttu-id="f42ab-2118">DXGI_FORMAT_R16G16 \_ uint<sup>FNS</sup> (36)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2118">DXGI_FORMAT_R16G16\_UINT<sup>FNS</sup> (36)</span></span>
| <span data-ttu-id="f42ab-2119">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-2119">Target</span></span> | <span data-ttu-id="f42ab-2120">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-2120">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-2121">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2121">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-2122">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-2122">32</span></span> |
| <span data-ttu-id="f42ab-2123">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-2123">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-2124">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-2124">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2125">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2125">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2126">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2126">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2127">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2127">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2128">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2128">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-2129">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2129">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-2130">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2130">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-2131">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-2131">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-2132">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2132">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-2133">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2133">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2134">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2134">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2135">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2135">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2136">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-2136">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-2137">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-2137">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-2138">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2138">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-2139">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2139">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-2140">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2140">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2141">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-2141">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2142">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-2142">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-2143">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-2143">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-2144">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-2144">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2145">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2145">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2146">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2146">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-2147">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2147">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-2148">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2148">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-2149">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2149">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-2150">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-2150">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-2151">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-2151">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-2152">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2152">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-2153">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-2153">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2154">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2154">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2155">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-2155">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-2156">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2156">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2157">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-2157">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2158">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-2158">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-2159">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-2159">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-2160">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-2160">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-2161">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-2161">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-2162">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-2162">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-2163">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2163">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-2164">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2164">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-2165">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2165">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-2166">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2166">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-2167">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-2167">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_snormsupfnssup-37"></a><span data-ttu-id="f42ab-2168">DXGI_FORMAT_R16G16 \_ SNORM<sup>FNS</sup> (37)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2168">DXGI_FORMAT_R16G16\_SNORM<sup>FNS</sup> (37)</span></span>
| <span data-ttu-id="f42ab-2169">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-2169">Target</span></span> | <span data-ttu-id="f42ab-2170">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-2170">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-2171">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2171">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-2172">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-2172">32</span></span> |
| <span data-ttu-id="f42ab-2173">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-2173">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2175">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-2175">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2176">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2176">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2178">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2178">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2179">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2179">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2180">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2180">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-2181">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2181">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2183">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2183">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2185">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-2185">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2187">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2187">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2189">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2189">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2191">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2191">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2192">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2192">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2193">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-2193">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-2194">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-2194">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-2195">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2195">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2197">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2197">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-2198">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2198">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2199">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-2199">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2200">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-2200">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-2201">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-2201">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-2202">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-2202">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2203">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2203">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2204">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2204">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-2205">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2205">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-2206">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2206">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-2207">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2207">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-2208">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-2208">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-2209">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-2209">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-2210">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2210">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-2211">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-2211">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2212">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2212">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2213">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-2213">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2215">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2215">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2216">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-2216">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2217">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-2217">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-2218">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-2218">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-2219">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-2219">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-2220">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-2220">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-2221">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-2221">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-2222">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2222">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-2223">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2223">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-2224">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2224">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-2225">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2225">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-2226">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-2226">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_sintsupfnssup-38"></a><span data-ttu-id="f42ab-2227">DXGI_FORMAT_R16G16 \_ Santo<sup>FNS</sup> (38)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2227">DXGI_FORMAT_R16G16\_SINT<sup>FNS</sup> (38)</span></span>
| <span data-ttu-id="f42ab-2228">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-2228">Target</span></span> | <span data-ttu-id="f42ab-2229">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-2229">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-2230">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2230">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-2231">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-2231">32</span></span> |
| <span data-ttu-id="f42ab-2232">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-2232">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2234">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-2234">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2235">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2235">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2237">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2237">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2238">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2238">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2239">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2239">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-2240">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2240">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-2241">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2241">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-2242">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-2242">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-2243">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2243">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-2244">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2244">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2245">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2245">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2246">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2246">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2247">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-2247">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-2248">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-2248">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-2249">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2249">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-2250">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2250">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-2251">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2251">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2252">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-2252">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2253">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-2253">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-2254">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-2254">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-2255">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-2255">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2256">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2256">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2257">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2257">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-2258">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2258">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-2259">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2259">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-2260">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2260">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-2261">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-2261">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-2262">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-2262">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-2263">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2263">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-2264">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-2264">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2265">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2265">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2266">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-2266">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-2267">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2267">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2268">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-2268">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2269">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-2269">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-2270">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-2270">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-2271">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-2271">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-2272">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-2272">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-2273">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-2273">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-2274">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2274">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-2275">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2275">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-2276">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2276">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-2277">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2277">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-2278">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-2278">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="f42ab-2279">DXGI_FORMAT_R32 \_ <sup>PCs</sup> não tipados (39)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2279">DXGI_FORMAT_R32\_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="f42ab-2280">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-2280">Target</span></span> | <span data-ttu-id="f42ab-2281">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-2281">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-2282">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2282">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-2283">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-2283">32</span></span> |
| <span data-ttu-id="f42ab-2284">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-2284">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-2285">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-2285">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2286">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2286">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2287">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2287">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2288">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2288">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2289">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2289">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-2290">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2290">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-2291">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2291">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-2292">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-2292">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-2293">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2293">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-2294">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2294">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2295">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2295">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2296">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2296">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2297">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-2297">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-2298">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-2298">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-2299">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2299">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-2300">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2300">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-2301">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2301">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2302">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-2302">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2303">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-2303">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-2304">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-2304">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-2305">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-2305">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2306">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2306">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2307">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2307">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-2308">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2308">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-2309">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2309">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-2310">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2310">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-2311">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-2311">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-2312">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-2312">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-2313">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2313">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-2314">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-2314">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2315">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2315">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2316">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-2316">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-2317">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2317">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2318">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-2318">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2319">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-2319">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-2320">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-2320">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-2321">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-2321">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-2322">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-2322">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-2323">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-2323">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-2324">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2324">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-2325">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2325">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-2326">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2326">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-2327">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2327">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-2328">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-2328">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_floatsupfnssup-40"></a><span data-ttu-id="f42ab-2329">DXGI_FORMAT_D32 \_ float<sup>FNS</sup> (40)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2329">DXGI_FORMAT_D32\_FLOAT<sup>FNS</sup> (40)</span></span>
| <span data-ttu-id="f42ab-2330">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-2330">Target</span></span> | <span data-ttu-id="f42ab-2331">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-2331">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-2332">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2332">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-2333">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-2333">32</span></span> |
| <span data-ttu-id="f42ab-2334">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-2334">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-2335">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-2335">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2336">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2336">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2337">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2337">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2338">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2338">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2339">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2339">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-2340">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2340">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-2341">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2341">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-2342">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-2342">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-2343">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2343">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-2344">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2344">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2345">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2345">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2346">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2346">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2347">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-2347">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-2348">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-2348">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-2349">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2349">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-2350">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2350">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-2351">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2351">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2352">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-2352">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2353">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-2353">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-2354">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-2354">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-2355">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-2355">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2356">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2356">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2357">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2357">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-2358">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2358">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-2359">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2359">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-2360">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2360">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-2361">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-2361">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-2362">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-2362">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-2363">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2363">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-2364">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-2364">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2365">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2365">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2366">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-2366">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-2367">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2367">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2368">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-2368">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2369">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-2369">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-2370">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-2370">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-2371">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-2371">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-2372">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-2372">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-2373">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-2373">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-2374">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2374">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-2375">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2375">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-2376">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2376">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-2377">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2377">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-2378">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-2378">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_floatsupfnssup-41"></a><span data-ttu-id="f42ab-2379">DXGI_FORMAT_R32 \_ float<sup>FNS</sup> (41)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2379">DXGI_FORMAT_R32\_FLOAT<sup>FNS</sup> (41)</span></span>
| <span data-ttu-id="f42ab-2380">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-2380">Target</span></span> | <span data-ttu-id="f42ab-2381">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-2381">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-2382">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2382">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-2383">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-2383">32</span></span> |
| <span data-ttu-id="f42ab-2384">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-2384">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2386">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-2386">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2387">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2387">Input Assembler Vertex Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2389">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2389">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2390">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2390">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2391">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2391">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-2392">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2392">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2394">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2394">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2396">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-2396">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2398">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2398">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2400">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2400">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2401">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2401">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2402">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2402">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2403">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-2403">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-2404">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-2404">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-2405">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2405">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2407">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2407">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2409">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2409">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2411">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-2411">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2412">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-2412">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-2413">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-2413">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-2414">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-2414">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2415">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2415">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2416">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2416">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-2417">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2417">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-2418">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2418">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-2419">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2419">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-2420">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-2420">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-2421">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-2421">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-2422">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2422">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-2423">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-2423">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2424">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2424">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2425">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-2425">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2427">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2427">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-2429">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-2429">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-2431">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-2431">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-2433">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-2433">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2435">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-2435">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-2436">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-2436">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-2437">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-2437">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-2438">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2438">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-2439">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2439">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-2440">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2440">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-2441">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2441">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-2442">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-2442">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_uintsupfnssup-42"></a><span data-ttu-id="f42ab-2443">DXGI_FORMAT_R32 \_ uint<sup>FNS</sup> (42)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2443">DXGI_FORMAT_R32\_UINT<sup>FNS</sup> (42)</span></span>
| <span data-ttu-id="f42ab-2444">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-2444">Target</span></span> | <span data-ttu-id="f42ab-2445">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-2445">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-2446">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2446">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-2447">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-2447">32</span></span> |
| <span data-ttu-id="f42ab-2448">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-2448">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2450">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-2450">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2451">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2451">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2452">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2452">Input Assembler Index Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2454">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2454">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2455">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2455">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-2456">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2456">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-2457">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2457">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-2458">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-2458">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-2459">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2459">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-2460">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2460">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2461">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2461">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2462">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2462">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2463">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-2463">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-2464">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-2464">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-2465">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2465">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-2466">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2466">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-2467">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2467">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2468">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-2468">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2469">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-2469">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-2470">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-2470">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-2471">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-2471">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2472">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2472">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2473">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2473">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-2474">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2474">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-2475">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2475">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-2476">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2476">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-2477">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-2477">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-2478">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-2478">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-2479">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2479">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-2480">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-2480">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2481">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2481">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2482">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-2482">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-2483">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2483">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2484">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-2484">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2485">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-2485">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-2486">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-2486">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-2487">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-2487">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-2488">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-2488">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-2489">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-2489">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-2490">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2490">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-2491">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2491">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-2492">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2492">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-2493">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2493">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-2494">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-2494">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_sintsupfnssup-43"></a><span data-ttu-id="f42ab-2495">DXGI_FORMAT_R32 \_ Santo<sup>FNS</sup> (43)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2495">DXGI_FORMAT_R32\_SINT<sup>FNS</sup> (43)</span></span>
| <span data-ttu-id="f42ab-2496">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-2496">Target</span></span> | <span data-ttu-id="f42ab-2497">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-2497">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-2498">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2498">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-2499">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-2499">32</span></span> |
| <span data-ttu-id="f42ab-2500">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-2500">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-2501">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-2501">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2502">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2502">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2503">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2503">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2504">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2504">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2505">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2505">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-2506">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2506">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-2507">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2507">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-2508">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-2508">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-2509">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2509">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-2510">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2510">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2511">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2511">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2512">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2512">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2513">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-2513">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-2514">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-2514">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-2515">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2515">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-2516">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2516">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-2517">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2517">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2518">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-2518">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2519">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-2519">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-2520">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-2520">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-2521">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-2521">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2522">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2522">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2523">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2523">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-2524">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2524">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-2525">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2525">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-2526">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2526">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-2527">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-2527">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-2528">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-2528">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-2529">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2529">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-2530">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-2530">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2531">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2531">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2532">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-2532">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-2533">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2533">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2534">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-2534">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2535">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-2535">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-2536">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-2536">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-2537">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-2537">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-2538">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-2538">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-2539">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-2539">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-2540">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2540">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-2541">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2541">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-2542">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2542">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-2543">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2543">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-2544">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-2544">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a><span data-ttu-id="f42ab-2545">DXGI_FORMAT_R24G8 \_ <sup>PCs</sup> não tipados (44)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2545">DXGI_FORMAT_R24G8\_TYPELESS<sup>PCS</sup> (44)</span></span>
| <span data-ttu-id="f42ab-2546">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-2546">Target</span></span> | <span data-ttu-id="f42ab-2547">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-2547">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-2548">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2548">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-2549">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-2549">32</span></span> |
| <span data-ttu-id="f42ab-2550">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-2550">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-2551">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-2551">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2552">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2552">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2553">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2553">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2554">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2554">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2555">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2555">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-2556">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2556">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-2557">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2557">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-2558">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-2558">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-2559">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2559">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-2560">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2560">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2561">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2561">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2562">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2562">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2563">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-2563">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-2564">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-2564">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-2565">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2565">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-2566">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2566">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-2567">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2567">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2568">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-2568">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2569">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-2569">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-2570">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-2570">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-2571">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-2571">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2572">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2572">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2573">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2573">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-2574">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2574">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-2575">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2575">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-2576">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2576">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-2577">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-2577">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-2578">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-2578">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-2579">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2579">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-2580">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-2580">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2581">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2581">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2582">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-2582">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-2583">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2583">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2584">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-2584">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2585">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-2585">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-2586">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-2586">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-2587">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-2587">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-2588">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-2588">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-2589">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-2589">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-2590">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2590">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-2591">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2591">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-2592">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2592">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-2593">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2593">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-2594">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-2594">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfnssup-45"></a><span data-ttu-id="f42ab-2595">DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT<sup>FNS</sup> (45)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2595">DXGI_FORMAT_D24\_UNORM\_S8\_UINT<sup>FNS</sup> (45)</span></span>
| <span data-ttu-id="f42ab-2596">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-2596">Target</span></span> | <span data-ttu-id="f42ab-2597">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-2597">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-2598">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2598">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-2599">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-2599">32</span></span> |
| <span data-ttu-id="f42ab-2600">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-2600">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2602">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-2602">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2603">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2603">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2604">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2604">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2605">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2605">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2606">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2606">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-2607">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2607">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2609">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2609">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-2610">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-2610">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-2611">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2611">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-2612">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2612">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2613">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2613">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2614">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2614">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2615">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-2615">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-2616">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-2616">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-2617">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2617">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-2618">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2618">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-2619">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2619">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2620">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-2620">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2621">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-2621">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-2622">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-2622">Depth/Stencil Target</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2624">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-2624">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2625">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2625">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2626">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2626">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-2627">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2627">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-2628">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2628">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-2629">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2629">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-2630">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-2630">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-2631">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-2631">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-2632">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2632">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-2633">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-2633">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2634">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2634">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2635">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-2635">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-2636">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2636">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-2638">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-2638">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-2640">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-2640">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-2642">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-2642">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-2643">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-2643">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-2644">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-2644">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-2645">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-2645">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-2646">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2646">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-2647">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2647">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-2648">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2648">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-2649">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2649">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-2650">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-2650">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfnssup-46"></a><span data-ttu-id="f42ab-2651">FNS UNORM x8 tipo não-suDXGI_FORMAT_R24do \_ \_ \_ (46)<sup></sup></span><span class="sxs-lookup"><span data-stu-id="f42ab-2651">DXGI_FORMAT_R24\_UNORM\_X8\_TYPELESS<sup>FNS</sup> (46)</span></span>
| <span data-ttu-id="f42ab-2652">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-2652">Target</span></span> | <span data-ttu-id="f42ab-2653">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-2653">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-2654">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2654">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-2655">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-2655">32</span></span> |
| <span data-ttu-id="f42ab-2656">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-2656">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-2657">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-2657">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2658">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2658">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2659">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2659">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2660">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2660">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2661">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2661">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-2662">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2662">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-2663">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2663">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-2664">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-2664">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-2665">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2665">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-2666">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2666">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2667">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2667">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2668">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2668">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2669">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-2669">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-2670">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-2670">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-2671">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2671">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-2672">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2672">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-2673">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2673">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2674">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-2674">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2675">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-2675">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-2676">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-2676">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-2677">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-2677">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2678">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2678">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2679">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2679">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-2680">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2680">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-2681">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2681">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-2682">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2682">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-2683">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-2683">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-2684">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-2684">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-2685">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2685">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-2686">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-2686">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2687">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2687">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2688">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-2688">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-2689">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2689">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2690">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-2690">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2691">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-2691">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-2692">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-2692">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-2693">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-2693">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-2694">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-2694">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-2695">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-2695">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-2696">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2696">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-2697">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2697">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-2698">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2698">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-2699">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2699">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-2700">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-2700">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfnssup-47"></a><span data-ttu-id="f42ab-2701">DXGI_FORMAT_X24 \_ \_ \_ <sup>FNS</sup> de G8 UINT não tipado (47)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2701">DXGI_FORMAT_X24\_TYPELESS\_G8\_UINT<sup>FNS</sup> (47)</span></span>
| <span data-ttu-id="f42ab-2702">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-2702">Target</span></span> | <span data-ttu-id="f42ab-2703">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-2703">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-2704">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2704">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-2705">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-2705">32</span></span> |
| <span data-ttu-id="f42ab-2706">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-2706">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-2707">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-2707">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2708">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2708">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2709">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2709">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2710">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2710">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2711">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2711">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-2712">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2712">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-2713">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2713">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-2714">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-2714">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-2715">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2715">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-2716">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2716">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2717">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2717">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2718">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2718">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2719">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-2719">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-2720">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-2720">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-2721">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2721">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-2722">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2722">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-2723">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2723">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2724">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-2724">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2725">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-2725">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-2726">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-2726">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-2727">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-2727">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2728">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2728">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2729">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2729">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-2730">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2730">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-2731">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2731">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-2732">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2732">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-2733">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-2733">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-2734">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-2734">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-2735">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2735">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-2736">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-2736">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2737">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2737">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2738">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-2738">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-2739">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2739">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2740">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-2740">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2741">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-2741">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-2742">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-2742">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-2743">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-2743">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-2744">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-2744">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-2745">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-2745">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-2746">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2746">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-2747">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2747">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-2748">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2748">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-2749">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2749">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-2750">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-2750">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="f42ab-2751">DXGI_FORMAT_R8G8 \_ <sup>PCs</sup> não tipados (48)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2751">DXGI_FORMAT_R8G8\_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="f42ab-2752">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-2752">Target</span></span> | <span data-ttu-id="f42ab-2753">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-2753">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-2754">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2754">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-2755">16</span><span class="sxs-lookup"><span data-stu-id="f42ab-2755">16</span></span> |
| <span data-ttu-id="f42ab-2756">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-2756">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-2757">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-2757">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2758">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2758">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2759">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2759">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2760">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2760">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2761">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2761">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-2762">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2762">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-2763">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2763">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-2764">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-2764">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-2765">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2765">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-2766">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2766">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2767">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2767">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2768">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2768">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2769">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-2769">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-2770">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-2770">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-2771">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2771">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-2772">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2772">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-2773">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2773">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2774">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-2774">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2775">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-2775">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-2776">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-2776">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-2777">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-2777">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2778">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2778">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2779">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2779">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-2780">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2780">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-2781">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2781">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-2782">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2782">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-2783">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-2783">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-2784">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-2784">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-2785">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2785">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-2786">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-2786">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2787">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2787">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2788">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-2788">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-2789">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2789">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2790">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-2790">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2791">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-2791">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-2792">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-2792">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-2793">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-2793">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-2794">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-2794">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-2795">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-2795">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-2796">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2796">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-2797">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2797">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-2798">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2798">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-2799">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2799">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-2800">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-2800">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_unormsupfnssup-49"></a><span data-ttu-id="f42ab-2801">DXGI_FORMAT_R8G8 \_ UNORM<sup>FNS</sup> (49)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2801">DXGI_FORMAT_R8G8\_UNORM<sup>FNS</sup> (49)</span></span>
| <span data-ttu-id="f42ab-2802">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-2802">Target</span></span> | <span data-ttu-id="f42ab-2803">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-2803">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-2804">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2804">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-2805">16</span><span class="sxs-lookup"><span data-stu-id="f42ab-2805">16</span></span> |
| <span data-ttu-id="f42ab-2806">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-2806">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2808">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-2808">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2809">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2809">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2810">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2810">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2811">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2811">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2812">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2812">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-2813">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2813">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2815">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2815">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-2816">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-2816">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-2817">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2817">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2819">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2819">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2821">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2821">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2822">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2822">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2823">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-2823">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-2824">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-2824">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-2825">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2825">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-2826">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2826">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-2827">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2827">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2829">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-2829">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2831">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-2831">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-2832">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-2832">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-2833">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-2833">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2834">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2834">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2835">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2835">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-2836">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2836">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-2837">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2837">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-2838">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2838">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-2839">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-2839">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-2840">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-2840">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-2841">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2841">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-2842">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-2842">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2843">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2843">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2844">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-2844">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2846">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2846">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2847">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-2847">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2848">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-2848">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-2849">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-2849">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-2850">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-2850">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-2851">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-2851">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-2852">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-2852">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-2853">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2853">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-2854">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2854">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-2855">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2855">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-2856">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2856">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2858">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-2858">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_uintsupfnssup-50"></a><span data-ttu-id="f42ab-2859">DXGI_FORMAT_R8G8 \_ uint<sup>FNS</sup> (50)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2859">DXGI_FORMAT_R8G8\_UINT<sup>FNS</sup> (50)</span></span>
| <span data-ttu-id="f42ab-2860">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-2860">Target</span></span> | <span data-ttu-id="f42ab-2861">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-2861">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-2862">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2862">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-2863">16</span><span class="sxs-lookup"><span data-stu-id="f42ab-2863">16</span></span> |
| <span data-ttu-id="f42ab-2864">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-2864">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-2865">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-2865">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2866">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2866">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2867">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2867">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2868">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2868">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2869">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2869">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-2870">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2870">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-2871">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2871">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-2872">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-2872">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-2873">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2873">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-2874">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2874">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2875">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2875">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2876">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2876">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2877">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-2877">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-2878">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-2878">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-2879">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2879">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-2880">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2880">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-2881">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2881">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2882">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-2882">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2883">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-2883">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-2884">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-2884">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-2885">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-2885">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2886">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2886">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2887">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2887">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-2888">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2888">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-2889">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2889">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-2890">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2890">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-2891">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-2891">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-2892">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-2892">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-2893">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2893">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-2894">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-2894">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2895">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2895">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2896">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-2896">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-2897">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2897">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2898">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-2898">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2899">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-2899">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-2900">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-2900">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-2901">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-2901">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-2902">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-2902">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-2903">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-2903">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-2904">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2904">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-2905">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2905">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-2906">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2906">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-2907">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2907">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-2908">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-2908">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_snormsupfnssup-51"></a><span data-ttu-id="f42ab-2909">DXGI_FORMAT_R8G8 \_ SNORM<sup>FNS</sup> (51)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2909">DXGI_FORMAT_R8G8\_SNORM<sup>FNS</sup> (51)</span></span>
| <span data-ttu-id="f42ab-2910">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-2910">Target</span></span> | <span data-ttu-id="f42ab-2911">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-2911">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-2912">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2912">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-2913">16</span><span class="sxs-lookup"><span data-stu-id="f42ab-2913">16</span></span> |
| <span data-ttu-id="f42ab-2914">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-2914">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2916">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-2916">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2917">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2917">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2918">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2918">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2919">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2919">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2920">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2920">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-2921">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2921">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2923">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2923">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-2924">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-2924">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-2925">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2925">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2927">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2927">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2929">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2929">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2930">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2930">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2931">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-2931">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-2932">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-2932">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-2933">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2933">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2935">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2935">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-2936">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2936">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2937">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-2937">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2938">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-2938">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-2939">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-2939">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-2940">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-2940">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2941">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2941">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2942">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2942">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-2943">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2943">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-2944">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2944">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-2945">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2945">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-2946">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-2946">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-2947">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-2947">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-2948">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2948">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-2949">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-2949">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2950">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2950">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-2951">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-2951">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-2953">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2953">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2954">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-2954">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2955">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-2955">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-2956">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-2956">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-2957">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-2957">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-2958">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-2958">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-2959">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-2959">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-2960">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2960">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-2961">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2961">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-2962">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2962">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-2963">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2963">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-2964">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-2964">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_sintsupfnssup-52"></a><span data-ttu-id="f42ab-2965">DXGI_FORMAT_R8G8 \_ Santo<sup>FNS</sup> (52)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2965">DXGI_FORMAT_R8G8\_SINT<sup>FNS</sup> (52)</span></span>
| <span data-ttu-id="f42ab-2966">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-2966">Target</span></span> | <span data-ttu-id="f42ab-2967">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-2967">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-2968">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2968">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-2969">16</span><span class="sxs-lookup"><span data-stu-id="f42ab-2969">16</span></span> |
| <span data-ttu-id="f42ab-2970">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-2970">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-2971">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-2971">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2972">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2972">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2973">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-2973">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2974">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-2974">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-2975">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2975">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-2976">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2976">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-2977">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-2977">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-2978">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-2978">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-2979">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2979">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-2980">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2980">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2981">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2981">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2982">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-2982">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-2983">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-2983">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-2984">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-2984">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-2985">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2985">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-2986">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-2986">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-2987">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-2987">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2988">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-2988">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-2989">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-2989">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-2990">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-2990">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-2991">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-2991">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2992">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2992">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-2993">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-2993">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-2994">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2994">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-2995">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2995">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-2996">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2996">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-2997">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-2997">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-2998">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-2998">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-2999">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-2999">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-3000">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-3000">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3001">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3001">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3002">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-3002">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-3003">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3003">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3004">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-3004">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3005">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-3005">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-3006">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-3006">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-3007">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-3007">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-3008">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-3008">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-3009">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-3009">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-3010">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3010">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-3011">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3011">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-3012">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3012">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-3013">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3013">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-3014">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-3014">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="f42ab-3015">DXGI_FORMAT_R16 \_ <sup>PCs</sup> não tipados (53)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3015">DXGI_FORMAT_R16\_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="f42ab-3016">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-3016">Target</span></span> | <span data-ttu-id="f42ab-3017">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-3017">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-3018">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3018">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-3019">16</span><span class="sxs-lookup"><span data-stu-id="f42ab-3019">16</span></span> |
| <span data-ttu-id="f42ab-3020">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-3020">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-3021">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-3021">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3022">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3022">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3023">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3023">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3024">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3024">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3025">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3025">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-3026">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3026">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-3027">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3027">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-3028">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-3028">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-3029">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3029">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-3030">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3030">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3031">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3031">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3032">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3032">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3033">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-3033">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-3034">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-3034">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-3035">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3035">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-3036">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3036">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-3037">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3037">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3038">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-3038">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3039">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-3039">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-3040">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-3040">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-3041">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-3041">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3042">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3042">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3043">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3043">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-3044">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3044">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-3045">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3045">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-3046">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3046">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-3047">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-3047">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-3048">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-3048">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-3049">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3049">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-3050">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-3050">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3051">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3051">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3052">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-3052">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-3053">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3053">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3054">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-3054">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3055">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-3055">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-3056">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-3056">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-3057">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-3057">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-3058">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-3058">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-3059">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-3059">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-3060">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3060">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-3061">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3061">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-3062">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3062">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-3063">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3063">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-3064">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-3064">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_floatsupfnssup-54"></a><span data-ttu-id="f42ab-3065">DXGI_FORMAT_R16 \_ float<sup>FNS</sup> (54)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3065">DXGI_FORMAT_R16\_FLOAT<sup>FNS</sup> (54)</span></span>
| <span data-ttu-id="f42ab-3066">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-3066">Target</span></span> | <span data-ttu-id="f42ab-3067">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-3067">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-3068">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3068">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-3069">16</span><span class="sxs-lookup"><span data-stu-id="f42ab-3069">16</span></span> |
| <span data-ttu-id="f42ab-3070">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-3070">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-3071">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-3071">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3072">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3072">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3073">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3073">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3074">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3074">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3075">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3075">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-3076">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3076">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-3077">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3077">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-3078">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-3078">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-3079">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3079">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-3080">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3080">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3081">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3081">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3082">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3082">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3083">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-3083">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-3084">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-3084">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-3085">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3085">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-3086">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3086">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-3087">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3087">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3088">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-3088">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3089">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-3089">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-3090">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-3090">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-3091">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-3091">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3092">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3092">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3093">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3093">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-3094">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3094">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-3095">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3095">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-3096">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3096">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-3097">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-3097">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-3098">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-3098">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-3099">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3099">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-3100">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-3100">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3101">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3101">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3102">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-3102">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-3103">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3103">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3104">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-3104">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3105">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-3105">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-3106">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-3106">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-3107">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-3107">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-3108">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-3108">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-3109">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-3109">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-3110">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3110">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-3111">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3111">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-3112">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3112">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-3113">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3113">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-3114">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-3114">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d16_unormsupfnssup-55"></a><span data-ttu-id="f42ab-3115">DXGI_FORMAT_D16 \_ UNORM<sup>FNS</sup> (55)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3115">DXGI_FORMAT_D16\_UNORM<sup>FNS</sup> (55)</span></span>
| <span data-ttu-id="f42ab-3116">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-3116">Target</span></span> | <span data-ttu-id="f42ab-3117">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-3117">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-3118">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3118">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-3119">16</span><span class="sxs-lookup"><span data-stu-id="f42ab-3119">16</span></span> |
| <span data-ttu-id="f42ab-3120">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-3120">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3122">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-3122">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3123">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3123">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3124">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3124">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3125">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3125">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3126">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3126">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-3127">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3127">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3129">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3129">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-3130">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-3130">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-3131">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3131">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-3132">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3132">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3133">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3133">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3134">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3134">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3135">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-3135">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-3136">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-3136">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-3137">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3137">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-3138">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3138">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-3139">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3139">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3140">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-3140">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3141">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-3141">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-3142">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-3142">Depth/Stencil Target</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3144">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-3144">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3145">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3145">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3146">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3146">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-3147">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3147">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-3148">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3148">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-3149">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3149">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-3150">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-3150">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-3151">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-3151">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-3152">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3152">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-3153">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-3153">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3154">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3154">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3155">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-3155">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-3156">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3156">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-3158">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-3158">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-3160">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-3160">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-3162">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-3162">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-3163">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-3163">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-3164">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-3164">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-3165">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-3165">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-3166">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3166">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-3167">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3167">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-3168">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3168">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-3169">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3169">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-3170">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-3170">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_unormsupfnssup-56"></a><span data-ttu-id="f42ab-3171">DXGI_FORMAT_R16 \_ UNORM<sup>FNS</sup> (56)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3171">DXGI_FORMAT_R16\_UNORM<sup>FNS</sup> (56)</span></span>
| <span data-ttu-id="f42ab-3172">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-3172">Target</span></span> | <span data-ttu-id="f42ab-3173">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-3173">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-3174">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3174">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-3175">16</span><span class="sxs-lookup"><span data-stu-id="f42ab-3175">16</span></span> |
| <span data-ttu-id="f42ab-3176">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-3176">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3178">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-3178">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3179">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3179">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3180">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3180">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3181">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3181">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3182">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3182">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-3183">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3183">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3185">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3185">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3187">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-3187">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3189">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3189">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3191">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3191">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3193">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3193">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3194">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3194">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3195">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-3195">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-3196">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-3196">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-3197">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3197">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3199">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3199">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-3200">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3200">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3201">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-3201">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3202">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-3202">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-3203">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-3203">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-3204">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-3204">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3205">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3205">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3206">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3206">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-3207">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3207">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-3208">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3208">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-3209">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3209">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-3210">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-3210">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-3211">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-3211">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-3212">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3212">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-3213">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-3213">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3214">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3214">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3215">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-3215">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3217">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3217">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3218">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-3218">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3219">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-3219">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-3220">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-3220">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-3221">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-3221">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-3222">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-3222">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-3223">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-3223">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-3224">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3224">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-3225">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3225">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-3226">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3226">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-3227">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3227">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-3228">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-3228">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_uintsupfnssup-57"></a><span data-ttu-id="f42ab-3229">DXGI_FORMAT_R16 \_ uint<sup>FNS</sup> (57)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3229">DXGI_FORMAT_R16\_UINT<sup>FNS</sup> (57)</span></span>
| <span data-ttu-id="f42ab-3230">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-3230">Target</span></span> | <span data-ttu-id="f42ab-3231">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-3231">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-3232">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3232">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-3233">16</span><span class="sxs-lookup"><span data-stu-id="f42ab-3233">16</span></span> |
| <span data-ttu-id="f42ab-3234">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-3234">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3236">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-3236">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3237">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3237">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3238">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3238">Input Assembler Index Buffer</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3240">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3240">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3241">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3241">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-3242">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3242">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-3243">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3243">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-3244">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-3244">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-3245">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3245">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-3246">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3246">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3247">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3247">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3248">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3248">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3249">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-3249">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-3250">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-3250">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-3251">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3251">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-3252">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3252">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-3253">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3253">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3254">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-3254">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3255">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-3255">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-3256">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-3256">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-3257">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-3257">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3258">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3258">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3259">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3259">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-3260">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3260">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-3261">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3261">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-3262">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3262">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-3263">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-3263">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-3264">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-3264">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-3265">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3265">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-3266">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-3266">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3267">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3267">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3268">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-3268">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-3269">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3269">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3270">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-3270">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3271">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-3271">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-3272">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-3272">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-3273">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-3273">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-3274">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-3274">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-3275">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-3275">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-3276">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3276">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-3277">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3277">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-3278">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3278">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-3279">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3279">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-3280">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-3280">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_snormsupfnssup-58"></a><span data-ttu-id="f42ab-3281">DXGI_FORMAT_R16 \_ SNORM<sup>FNS</sup> (58)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3281">DXGI_FORMAT_R16\_SNORM<sup>FNS</sup> (58)</span></span>
| <span data-ttu-id="f42ab-3282">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-3282">Target</span></span> | <span data-ttu-id="f42ab-3283">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-3283">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-3284">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3284">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-3285">16</span><span class="sxs-lookup"><span data-stu-id="f42ab-3285">16</span></span> |
| <span data-ttu-id="f42ab-3286">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-3286">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-3287">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-3287">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3288">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3288">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3289">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3289">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3290">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3290">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3291">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3291">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-3292">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3292">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-3293">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3293">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-3294">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-3294">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-3295">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3295">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-3296">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3296">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3297">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3297">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3298">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3298">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3299">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-3299">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-3300">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-3300">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-3301">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3301">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-3302">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3302">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-3303">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3303">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3304">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-3304">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3305">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-3305">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-3306">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-3306">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-3307">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-3307">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3308">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3308">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3309">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3309">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-3310">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3310">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-3311">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3311">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-3312">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3312">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-3313">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-3313">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-3314">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-3314">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-3315">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3315">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-3316">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-3316">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3317">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3317">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3318">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-3318">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-3319">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3319">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3320">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-3320">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3321">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-3321">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-3322">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-3322">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-3323">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-3323">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-3324">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-3324">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-3325">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-3325">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-3326">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3326">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-3327">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3327">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-3328">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3328">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-3329">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3329">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-3330">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-3330">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_sintsupfnssup-59"></a><span data-ttu-id="f42ab-3331">DXGI_FORMAT_R16 \_ Santo<sup>FNS</sup> (59)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3331">DXGI_FORMAT_R16\_SINT<sup>FNS</sup> (59)</span></span>
| <span data-ttu-id="f42ab-3332">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-3332">Target</span></span> | <span data-ttu-id="f42ab-3333">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-3333">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-3334">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3334">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-3335">16</span><span class="sxs-lookup"><span data-stu-id="f42ab-3335">16</span></span> |
| <span data-ttu-id="f42ab-3336">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-3336">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-3337">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-3337">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3338">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3338">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3339">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3339">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3340">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3340">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3341">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3341">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-3342">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3342">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-3343">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3343">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-3344">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-3344">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-3345">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3345">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-3346">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3346">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3347">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3347">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3348">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3348">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3349">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-3349">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-3350">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-3350">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-3351">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3351">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-3352">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3352">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-3353">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3353">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3354">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-3354">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3355">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-3355">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-3356">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-3356">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-3357">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-3357">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3358">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3358">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3359">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3359">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-3360">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3360">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-3361">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3361">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-3362">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3362">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-3363">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-3363">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-3364">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-3364">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-3365">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3365">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-3366">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-3366">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3367">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3367">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3368">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-3368">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-3369">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3369">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3370">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-3370">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3371">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-3371">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-3372">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-3372">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-3373">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-3373">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-3374">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-3374">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-3375">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-3375">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-3376">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3376">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-3377">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3377">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-3378">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3378">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-3379">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3379">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-3380">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-3380">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="f42ab-3381">DXGI_FORMAT_R8 \_ <sup>PCs</sup> não tipados (60)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3381">DXGI_FORMAT_R8\_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="f42ab-3382">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-3382">Target</span></span> | <span data-ttu-id="f42ab-3383">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-3383">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-3384">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3384">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-3385">8</span><span class="sxs-lookup"><span data-stu-id="f42ab-3385">8</span></span> |
| <span data-ttu-id="f42ab-3386">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-3386">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-3387">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-3387">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3388">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3388">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3389">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3389">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3390">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3390">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3391">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3391">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-3392">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3392">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-3393">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3393">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-3394">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-3394">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-3395">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3395">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-3396">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3396">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3397">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3397">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3398">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3398">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3399">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-3399">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-3400">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-3400">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-3401">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3401">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-3402">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3402">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-3403">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3403">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3404">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-3404">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3405">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-3405">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-3406">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-3406">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-3407">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-3407">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3408">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3408">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3409">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3409">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-3410">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3410">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-3411">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3411">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-3412">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3412">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-3413">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-3413">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-3414">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-3414">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-3415">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3415">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-3416">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-3416">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3417">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3417">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3418">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-3418">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-3419">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3419">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3420">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-3420">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3421">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-3421">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-3422">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-3422">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-3423">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-3423">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-3424">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-3424">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-3425">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-3425">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-3426">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3426">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-3427">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3427">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-3428">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3428">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-3429">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3429">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-3430">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-3430">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_unormsupfnssup-61"></a><span data-ttu-id="f42ab-3431">DXGI_FORMAT_R8 \_ UNORM<sup>FNS</sup> (61)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3431">DXGI_FORMAT_R8\_UNORM<sup>FNS</sup> (61)</span></span>
| <span data-ttu-id="f42ab-3432">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-3432">Target</span></span> | <span data-ttu-id="f42ab-3433">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-3433">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-3434">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3434">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-3435">8</span><span class="sxs-lookup"><span data-stu-id="f42ab-3435">8</span></span> |
| <span data-ttu-id="f42ab-3436">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-3436">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3438">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-3438">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3439">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3439">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3440">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3440">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3441">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3441">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3442">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3442">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-3443">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3443">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3445">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3445">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3447">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-3447">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3449">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3449">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3451">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3451">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3453">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3453">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3454">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3454">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3455">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-3455">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-3456">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-3456">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-3457">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3457">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3459">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3459">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-3460">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3460">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3462">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-3462">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3464">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-3464">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-3465">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-3465">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-3466">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-3466">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3467">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3467">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3468">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3468">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-3469">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3469">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-3470">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3470">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-3471">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3471">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-3472">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-3472">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-3473">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-3473">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-3474">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3474">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-3475">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-3475">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3476">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3476">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3477">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-3477">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3479">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3479">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3480">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-3480">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3481">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-3481">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-3482">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-3482">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-3483">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-3483">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-3484">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-3484">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-3485">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-3485">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-3486">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3486">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-3487">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3487">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-3488">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3488">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-3489">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3489">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3491">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-3491">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_uintsupfnssup-62"></a><span data-ttu-id="f42ab-3492">DXGI_FORMAT_R8 \_ uint<sup>FNS</sup> (62)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3492">DXGI_FORMAT_R8\_UINT<sup>FNS</sup> (62)</span></span>
| <span data-ttu-id="f42ab-3493">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-3493">Target</span></span> | <span data-ttu-id="f42ab-3494">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-3494">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-3495">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3495">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-3496">8</span><span class="sxs-lookup"><span data-stu-id="f42ab-3496">8</span></span> |
| <span data-ttu-id="f42ab-3497">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-3497">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-3498">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-3498">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3499">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3499">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3500">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3500">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3501">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3501">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3502">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3502">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-3503">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3503">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-3504">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3504">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-3505">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-3505">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-3506">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3506">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-3507">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3507">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3508">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3508">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3509">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3509">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3510">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-3510">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-3511">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-3511">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-3512">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3512">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-3513">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3513">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-3514">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3514">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3515">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-3515">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3516">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-3516">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-3517">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-3517">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-3518">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-3518">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3519">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3519">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3520">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3520">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-3521">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3521">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-3522">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3522">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-3523">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3523">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-3524">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-3524">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-3525">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-3525">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-3526">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3526">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-3527">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-3527">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3528">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3528">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3529">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-3529">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-3530">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3530">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3531">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-3531">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3532">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-3532">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-3533">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-3533">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-3534">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-3534">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-3535">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-3535">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-3536">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-3536">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-3537">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3537">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-3538">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3538">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-3539">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3539">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-3540">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3540">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-3541">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-3541">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_snormsupfnssup-63"></a><span data-ttu-id="f42ab-3542">DXGI_FORMAT_R8 \_ SNORM<sup>FNS</sup> (63)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3542">DXGI_FORMAT_R8\_SNORM<sup>FNS</sup> (63)</span></span>
| <span data-ttu-id="f42ab-3543">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-3543">Target</span></span> | <span data-ttu-id="f42ab-3544">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-3544">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-3545">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3545">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-3546">8</span><span class="sxs-lookup"><span data-stu-id="f42ab-3546">8</span></span> |
| <span data-ttu-id="f42ab-3547">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-3547">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-3548">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-3548">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3549">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3549">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3550">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3550">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3551">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3551">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3552">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3552">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-3553">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3553">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-3554">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3554">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-3555">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-3555">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-3556">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3556">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-3557">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3557">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3558">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3558">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3559">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3559">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3560">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-3560">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-3561">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-3561">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-3562">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3562">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-3563">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3563">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-3564">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3564">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3565">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-3565">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3566">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-3566">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-3567">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-3567">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-3568">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-3568">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3569">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3569">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3570">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3570">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-3571">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3571">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-3572">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3572">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-3573">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3573">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-3574">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-3574">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-3575">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-3575">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-3576">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3576">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-3577">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-3577">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3578">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3578">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3579">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-3579">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-3580">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3580">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3581">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-3581">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3582">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-3582">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-3583">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-3583">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-3584">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-3584">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-3585">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-3585">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-3586">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-3586">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-3587">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3587">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-3588">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3588">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-3589">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3589">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-3590">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3590">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-3591">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-3591">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_sintsupfnssup-64"></a><span data-ttu-id="f42ab-3592">DXGI_FORMAT_R8 \_ Santo<sup>FNS</sup> (64)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3592">DXGI_FORMAT_R8\_SINT<sup>FNS</sup> (64)</span></span>
| <span data-ttu-id="f42ab-3593">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-3593">Target</span></span> | <span data-ttu-id="f42ab-3594">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-3594">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-3595">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3595">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-3596">8</span><span class="sxs-lookup"><span data-stu-id="f42ab-3596">8</span></span> |
| <span data-ttu-id="f42ab-3597">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-3597">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-3598">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-3598">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3599">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3599">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3600">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3600">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3601">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3601">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3602">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3602">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-3603">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3603">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-3604">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3604">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-3605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-3605">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-3606">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3606">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-3607">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3607">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3608">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3608">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3609">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3609">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3610">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-3610">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-3611">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-3611">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-3612">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3612">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-3613">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3613">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-3614">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3614">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3615">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-3615">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3616">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-3616">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-3617">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-3617">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-3618">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-3618">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3619">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3619">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3620">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3620">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-3621">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3621">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-3622">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3622">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-3623">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3623">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-3624">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-3624">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-3625">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-3625">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-3626">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3626">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-3627">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-3627">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3628">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3628">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3629">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-3629">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-3630">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3630">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3631">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-3631">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3632">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-3632">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-3633">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-3633">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-3634">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-3634">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-3635">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-3635">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-3636">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-3636">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-3637">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3637">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-3638">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3638">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-3639">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3639">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-3640">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3640">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-3641">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-3641">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="f42ab-3642">DXGI_FORMAT_A8 \_ UNORM<sup>FNS</sup> (65)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3642">DXGI_FORMAT_A8\_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="f42ab-3643">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-3643">Target</span></span> | <span data-ttu-id="f42ab-3644">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-3644">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-3645">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3645">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-3646">8</span><span class="sxs-lookup"><span data-stu-id="f42ab-3646">8</span></span> |
| <span data-ttu-id="f42ab-3647">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-3647">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3649">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-3649">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3650">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3650">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3651">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3651">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3652">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3652">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3653">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3653">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-3654">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3654">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3656">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3656">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3658">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-3658">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3660">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3660">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3662">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3662">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3664">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3664">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3665">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3665">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3666">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-3666">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-3667">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-3667">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-3668">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3668">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-3669">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3669">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-3670">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3670">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3672">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-3672">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3674">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-3674">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-3675">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-3675">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-3676">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-3676">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3677">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3677">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3678">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3678">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-3679">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3679">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-3680">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3680">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-3681">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3681">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-3682">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-3682">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-3683">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-3683">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-3684">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3684">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-3685">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-3685">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3686">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3686">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3687">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-3687">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3689">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3689">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3690">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-3690">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3691">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-3691">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-3692">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-3692">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-3693">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-3693">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-3694">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-3694">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-3695">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-3695">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-3696">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3696">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-3697">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3697">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-3698">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3698">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-3699">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3699">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3701">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-3701">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="f42ab-3702">DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3702">DXGI_FORMAT_R9G9B9E5\_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="f42ab-3703">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-3703">Target</span></span> | <span data-ttu-id="f42ab-3704">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-3704">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-3705">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3705">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-3706">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-3706">32</span></span> |
| <span data-ttu-id="f42ab-3707">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-3707">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-3708">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-3708">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3709">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3709">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3710">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3710">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3711">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3711">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3712">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3712">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-3713">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3713">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-3714">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3714">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-3715">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-3715">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-3716">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3716">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-3717">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3717">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3718">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3718">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3719">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3719">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3720">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-3720">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-3721">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-3721">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-3722">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3722">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-3723">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3723">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-3724">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3724">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3725">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-3725">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3726">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-3726">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-3727">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-3727">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-3728">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-3728">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3729">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3729">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3730">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3730">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-3731">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3731">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-3732">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3732">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-3733">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3733">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-3734">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-3734">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-3735">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-3735">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-3736">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3736">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-3737">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-3737">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3738">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3738">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3739">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-3739">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-3740">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3740">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3741">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-3741">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3742">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-3742">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-3743">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-3743">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-3744">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-3744">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-3745">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-3745">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-3746">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-3746">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-3747">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3747">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-3748">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3748">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-3749">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3749">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-3750">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3750">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-3751">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-3751">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="f42ab-3752">DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3752">DXGI_FORMAT_R8G8\_B8G8\_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="f42ab-3753">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-3753">Target</span></span> | <span data-ttu-id="f42ab-3754">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-3754">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-3755">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3755">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-3756">16</span><span class="sxs-lookup"><span data-stu-id="f42ab-3756">16</span></span> |
| <span data-ttu-id="f42ab-3757">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-3757">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-3758">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-3758">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3759">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3759">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3760">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3760">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3761">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3761">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3762">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3762">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-3763">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3763">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-3764">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3764">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-3765">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-3765">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-3766">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3766">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-3767">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3767">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3768">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3768">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3769">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3769">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3770">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-3770">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-3771">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-3771">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-3772">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3772">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-3773">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3773">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-3774">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3774">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3775">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-3775">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3776">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-3776">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-3777">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-3777">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-3778">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-3778">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3779">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3779">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3780">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3780">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-3781">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3781">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-3782">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3782">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-3783">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3783">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-3784">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-3784">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-3785">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-3785">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-3786">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3786">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-3787">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-3787">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3788">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3788">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3789">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-3789">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-3790">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3790">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3791">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-3791">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3792">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-3792">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-3793">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-3793">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-3794">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-3794">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-3795">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-3795">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-3796">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-3796">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-3797">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3797">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-3798">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3798">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-3799">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3799">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-3800">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3800">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-3801">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-3801">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="f42ab-3802">DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>FNC</sup> (69)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3802">DXGI_FORMAT_G8R8\_G8B8\_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="f42ab-3803">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-3803">Target</span></span> | <span data-ttu-id="f42ab-3804">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-3804">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-3805">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3805">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-3806">16</span><span class="sxs-lookup"><span data-stu-id="f42ab-3806">16</span></span> |
| <span data-ttu-id="f42ab-3807">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-3807">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-3808">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-3808">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3809">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3809">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3810">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3810">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3811">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3811">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3812">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3812">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-3813">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3813">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-3814">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3814">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-3815">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-3815">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-3816">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3816">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-3817">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3817">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3818">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3818">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3819">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3819">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3820">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-3820">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-3821">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-3821">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-3822">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3822">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-3823">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3823">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-3824">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3824">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3825">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-3825">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3826">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-3826">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-3827">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-3827">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-3828">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-3828">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3829">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3829">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3830">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3830">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-3831">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3831">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-3832">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3832">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-3833">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3833">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-3834">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-3834">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-3835">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-3835">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-3836">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3836">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-3837">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-3837">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3838">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3838">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3839">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-3839">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-3840">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3840">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3841">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-3841">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3842">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-3842">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-3843">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-3843">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-3844">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-3844">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-3845">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-3845">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-3846">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-3846">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-3847">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3847">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-3848">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3848">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-3849">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3849">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-3850">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3850">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-3851">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-3851">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="f42ab-3852">DXGI_FORMAT_BC1 \_ <sup>PCC</sup> de tipo (70)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3852">DXGI_FORMAT_BC1\_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="f42ab-3853">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-3853">Target</span></span> | <span data-ttu-id="f42ab-3854">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-3854">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-3855">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3855">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-3856">4</span><span class="sxs-lookup"><span data-stu-id="f42ab-3856">4</span></span> |
| <span data-ttu-id="f42ab-3857">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-3857">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-3858">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-3858">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3859">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3859">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3860">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3860">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3861">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3861">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3862">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3862">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-3863">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3863">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-3864">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3864">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-3865">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-3865">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-3866">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3866">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-3867">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3867">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3868">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3868">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3869">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3869">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3870">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-3870">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-3871">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-3871">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-3872">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3872">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-3873">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3873">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-3874">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3874">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3875">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-3875">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3876">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-3876">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-3877">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-3877">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-3878">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-3878">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3879">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3879">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3880">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3880">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-3881">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3881">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-3882">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3882">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-3883">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3883">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-3884">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-3884">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-3885">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-3885">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-3886">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3886">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-3887">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-3887">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3888">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3888">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3889">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-3889">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-3890">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3890">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3891">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-3891">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3892">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-3892">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-3893">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-3893">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-3894">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-3894">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-3895">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-3895">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-3896">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-3896">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-3897">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3897">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-3898">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3898">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-3899">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3899">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-3900">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3900">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-3901">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-3901">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unormsupfncsup-71"></a><span data-ttu-id="f42ab-3902">DXGI_FORMAT_BC1 \_ UNORM<sup>FNC</sup> (71)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3902">DXGI_FORMAT_BC1\_UNORM<sup>FNC</sup> (71)</span></span>
| <span data-ttu-id="f42ab-3903">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-3903">Target</span></span> | <span data-ttu-id="f42ab-3904">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-3904">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-3905">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3905">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-3906">4</span><span class="sxs-lookup"><span data-stu-id="f42ab-3906">4</span></span> |
| <span data-ttu-id="f42ab-3907">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-3907">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3909">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-3909">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3910">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3910">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3911">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3911">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3912">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3912">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3913">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3913">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-3914">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3914">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3916">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3916">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-3917">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-3917">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3919">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3919">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3921">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3921">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3923">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3923">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3924">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3924">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3925">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-3925">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-3926">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-3926">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-3927">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3927">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3929">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3929">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-3930">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3930">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3931">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-3931">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3932">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-3932">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-3933">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-3933">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-3934">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-3934">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3935">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3935">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3936">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3936">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-3937">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3937">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-3938">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3938">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-3939">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3939">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-3940">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-3940">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-3941">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-3941">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-3942">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3942">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-3943">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-3943">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3944">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3944">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-3945">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-3945">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3947">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3947">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3948">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-3948">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3949">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-3949">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-3950">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-3950">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-3951">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-3951">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-3952">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-3952">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-3953">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-3953">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-3954">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3954">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-3955">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3955">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-3956">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3956">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-3957">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3957">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3959">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-3959">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfncsup-72"></a><span data-ttu-id="f42ab-3960">DXGI_FORMAT_BC1 \_ UNORM \_ sRGB<sup>FNC</sup> (72)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3960">DXGI_FORMAT_BC1\_UNORM\_SRGB<sup>FNC</sup> (72)</span></span>
| <span data-ttu-id="f42ab-3961">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-3961">Target</span></span> | <span data-ttu-id="f42ab-3962">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-3962">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-3963">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3963">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-3964">4</span><span class="sxs-lookup"><span data-stu-id="f42ab-3964">4</span></span> |
| <span data-ttu-id="f42ab-3965">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-3965">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3967">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-3967">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3968">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3968">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3969">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-3969">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3970">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-3970">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-3971">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3971">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-3972">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3972">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3974">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-3974">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-3975">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-3975">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3977">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3977">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3979">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3979">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3981">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3981">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3982">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-3982">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-3983">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-3983">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-3984">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-3984">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-3985">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3985">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-3987">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-3987">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-3988">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-3988">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3989">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-3989">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-3990">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-3990">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-3991">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-3991">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-3992">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-3992">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3993">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3993">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-3994">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-3994">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-3995">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3995">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-3996">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3996">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-3997">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-3997">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-3998">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-3998">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-3999">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-3999">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-4000">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4000">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-4001">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-4001">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4002">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4002">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4003">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-4003">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4005">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4005">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4006">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-4006">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4007">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-4007">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-4008">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-4008">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-4009">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-4009">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-4010">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-4010">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-4011">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-4011">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-4012">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4012">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-4013">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4013">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-4014">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4014">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-4015">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4015">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4017">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-4017">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="f42ab-4018">DXGI_FORMAT_BC2 \_ <sup>PCC</sup> de tipo (73)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4018">DXGI_FORMAT_BC2\_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="f42ab-4019">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-4019">Target</span></span> | <span data-ttu-id="f42ab-4020">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-4020">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-4021">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4021">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-4022">8</span><span class="sxs-lookup"><span data-stu-id="f42ab-4022">8</span></span> |
| <span data-ttu-id="f42ab-4023">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-4023">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-4024">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-4024">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4025">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4025">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4026">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4026">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4027">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4027">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4028">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4028">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-4029">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4029">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-4030">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4030">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-4031">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-4031">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-4032">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4032">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-4033">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4033">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4034">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4034">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4035">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4035">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4036">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-4036">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-4037">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-4037">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-4038">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4038">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-4039">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4039">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-4040">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4040">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4041">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-4041">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4042">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-4042">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-4043">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-4043">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-4044">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-4044">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4045">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4045">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4046">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4046">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-4047">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4047">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-4048">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4048">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-4049">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4049">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-4050">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-4050">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-4051">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-4051">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-4052">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4052">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-4053">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-4053">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4054">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4054">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4055">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-4055">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-4056">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4056">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4057">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-4057">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4058">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-4058">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-4059">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-4059">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-4060">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-4060">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-4061">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-4061">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-4062">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-4062">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-4063">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4063">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-4064">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4064">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-4065">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4065">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-4066">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4066">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-4067">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-4067">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unormsupfncsup-74"></a><span data-ttu-id="f42ab-4068">DXGI_FORMAT_BC2 \_ UNORM<sup>FNC</sup> (74)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4068">DXGI_FORMAT_BC2\_UNORM<sup>FNC</sup> (74)</span></span>
| <span data-ttu-id="f42ab-4069">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-4069">Target</span></span> | <span data-ttu-id="f42ab-4070">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-4070">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-4071">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4071">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-4072">8</span><span class="sxs-lookup"><span data-stu-id="f42ab-4072">8</span></span> |
| <span data-ttu-id="f42ab-4073">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-4073">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4075">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-4075">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4076">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4076">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4077">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4077">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4078">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4078">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4079">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4079">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-4080">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4080">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4082">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4082">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-4083">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-4083">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4085">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4085">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4087">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4087">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4089">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4089">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4090">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4090">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4091">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-4091">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-4092">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-4092">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-4093">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4093">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4095">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4095">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-4096">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4096">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4097">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-4097">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4098">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-4098">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-4099">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-4099">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-4100">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-4100">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4101">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4101">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4102">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4102">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-4103">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4103">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-4104">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4104">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-4105">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4105">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-4106">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-4106">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-4107">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-4107">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-4108">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4108">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-4109">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-4109">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4110">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4110">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4111">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-4111">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4113">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4113">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4114">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-4114">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4115">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-4115">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-4116">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-4116">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-4117">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-4117">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-4118">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-4118">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-4119">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-4119">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-4120">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4120">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-4121">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4121">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-4122">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4122">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-4123">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4123">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4125">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-4125">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfncsup-75"></a><span data-ttu-id="f42ab-4126">DXGI_FORMAT_BC2 \_ UNORM \_ sRGB<sup>FNC</sup> (75)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4126">DXGI_FORMAT_BC2\_UNORM\_SRGB<sup>FNC</sup> (75)</span></span>
| <span data-ttu-id="f42ab-4127">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-4127">Target</span></span> | <span data-ttu-id="f42ab-4128">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-4128">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-4129">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4129">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-4130">8</span><span class="sxs-lookup"><span data-stu-id="f42ab-4130">8</span></span> |
| <span data-ttu-id="f42ab-4131">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-4131">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4133">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-4133">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4134">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4134">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4135">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4135">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4136">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4136">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4137">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4137">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-4138">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4138">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4140">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4140">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-4141">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-4141">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4143">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4143">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4145">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4145">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4147">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4147">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4148">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4148">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4149">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-4149">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-4150">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-4150">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-4151">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4151">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4153">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4153">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-4154">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4154">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4155">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-4155">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4156">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-4156">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-4157">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-4157">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-4158">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-4158">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4159">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4159">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4160">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4160">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-4161">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4161">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-4162">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4162">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-4163">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4163">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-4164">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-4164">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-4165">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-4165">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-4166">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4166">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-4167">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-4167">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4168">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4168">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4169">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-4169">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4171">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4171">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4172">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-4172">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4173">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-4173">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-4174">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-4174">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-4175">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-4175">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-4176">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-4176">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-4177">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-4177">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-4178">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4178">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-4179">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4179">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-4180">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4180">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-4181">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4181">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4183">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-4183">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="f42ab-4184">DXGI_FORMAT_BC3 \_ <sup>PCC</sup> de tipo (76)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4184">DXGI_FORMAT_BC3\_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="f42ab-4185">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-4185">Target</span></span> | <span data-ttu-id="f42ab-4186">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-4186">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-4187">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4187">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-4188">8</span><span class="sxs-lookup"><span data-stu-id="f42ab-4188">8</span></span> |
| <span data-ttu-id="f42ab-4189">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-4189">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-4190">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-4190">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4191">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4191">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4192">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4192">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4193">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4193">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4194">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4194">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-4195">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4195">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-4196">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4196">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-4197">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-4197">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-4198">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4198">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-4199">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4199">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4200">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4200">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4201">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4201">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4202">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-4202">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-4203">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-4203">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-4204">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4204">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-4205">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4205">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-4206">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4206">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4207">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-4207">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4208">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-4208">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-4209">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-4209">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-4210">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-4210">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4211">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4211">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4212">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4212">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-4213">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4213">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-4214">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4214">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-4215">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4215">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-4216">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-4216">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-4217">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-4217">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-4218">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4218">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-4219">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-4219">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4220">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4220">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4221">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-4221">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-4222">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4222">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4223">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-4223">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4224">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-4224">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-4225">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-4225">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-4226">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-4226">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-4227">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-4227">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-4228">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-4228">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-4229">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4229">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-4230">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4230">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-4231">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4231">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-4232">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4232">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-4233">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-4233">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unormsupfncsup-77"></a><span data-ttu-id="f42ab-4234">DXGI_FORMAT_BC3 \_ UNORM<sup>FNC</sup> (77)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4234">DXGI_FORMAT_BC3\_UNORM<sup>FNC</sup> (77)</span></span>
| <span data-ttu-id="f42ab-4235">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-4235">Target</span></span> | <span data-ttu-id="f42ab-4236">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-4236">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-4237">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4237">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-4238">8</span><span class="sxs-lookup"><span data-stu-id="f42ab-4238">8</span></span> |
| <span data-ttu-id="f42ab-4239">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-4239">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4241">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-4241">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4242">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4242">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4243">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4243">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4244">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4244">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4245">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4245">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-4246">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4246">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4248">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4248">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-4249">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-4249">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4251">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4251">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4253">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4253">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4255">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4255">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4256">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4256">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4257">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-4257">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-4258">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-4258">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-4259">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4259">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4261">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4261">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-4262">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4262">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4263">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-4263">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4264">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-4264">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-4265">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-4265">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-4266">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-4266">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4267">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4267">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4268">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4268">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-4269">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4269">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-4270">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4270">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-4271">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4271">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-4272">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-4272">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-4273">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-4273">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-4274">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4274">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-4275">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-4275">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4276">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4276">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4277">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-4277">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4279">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4279">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4280">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-4280">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4281">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-4281">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-4282">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-4282">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-4283">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-4283">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-4284">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-4284">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-4285">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-4285">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-4286">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4286">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-4287">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4287">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-4288">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4288">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-4289">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4289">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4291">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-4291">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfncsup-78"></a><span data-ttu-id="f42ab-4292">DXGI_FORMAT_BC3 \_ UNORM \_ sRGB<sup>FNC</sup> (78)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4292">DXGI_FORMAT_BC3\_UNORM\_SRGB<sup>FNC</sup> (78)</span></span>
| <span data-ttu-id="f42ab-4293">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-4293">Target</span></span> | <span data-ttu-id="f42ab-4294">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-4294">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-4295">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4295">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-4296">8</span><span class="sxs-lookup"><span data-stu-id="f42ab-4296">8</span></span> |
| <span data-ttu-id="f42ab-4297">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-4297">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4299">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-4299">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4300">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4300">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4301">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4301">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4302">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4302">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4303">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4303">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-4304">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4304">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4306">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4306">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-4307">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-4307">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4309">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4309">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4311">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4311">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4313">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4313">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4314">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4314">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4315">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-4315">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-4316">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-4316">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-4317">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4317">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4319">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4319">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-4320">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4320">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4321">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-4321">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4322">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-4322">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-4323">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-4323">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-4324">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-4324">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4325">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4325">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4326">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4326">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-4327">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4327">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-4328">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4328">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-4329">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4329">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-4330">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-4330">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-4331">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-4331">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-4332">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4332">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-4333">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-4333">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4334">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4334">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4335">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-4335">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4337">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4337">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4338">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-4338">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4339">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-4339">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-4340">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-4340">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-4341">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-4341">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-4342">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-4342">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-4343">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-4343">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-4344">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4344">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-4345">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4345">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-4346">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4346">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-4347">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4347">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4349">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-4349">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="f42ab-4350">DXGI_FORMAT_BC4 \_ <sup>PCC</sup> de tipo (79)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4350">DXGI_FORMAT_BC4\_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="f42ab-4351">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-4351">Target</span></span> | <span data-ttu-id="f42ab-4352">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-4352">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-4353">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4353">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-4354">4</span><span class="sxs-lookup"><span data-stu-id="f42ab-4354">4</span></span> |
| <span data-ttu-id="f42ab-4355">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-4355">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-4356">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-4356">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4357">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4357">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4358">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4358">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4359">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4359">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4360">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4360">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-4361">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4361">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-4362">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4362">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-4363">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-4363">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-4364">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4364">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-4365">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4365">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4366">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4366">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4367">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4367">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4368">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-4368">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-4369">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-4369">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-4370">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4370">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-4371">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4371">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-4372">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4372">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4373">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-4373">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4374">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-4374">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-4375">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-4375">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-4376">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-4376">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4377">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4377">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4378">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4378">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-4379">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4379">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-4380">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4380">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-4381">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4381">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-4382">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-4382">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-4383">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-4383">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-4384">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4384">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-4385">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-4385">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4386">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4386">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4387">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-4387">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-4388">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4388">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4389">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-4389">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4390">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-4390">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-4391">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-4391">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-4392">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-4392">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-4393">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-4393">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-4394">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-4394">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-4395">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4395">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-4396">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4396">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-4397">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4397">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-4398">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4398">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-4399">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-4399">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_unormsupfncsup-80"></a><span data-ttu-id="f42ab-4400">DXGI_FORMAT_BC4 \_ UNORM<sup>FNC</sup> (80)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4400">DXGI_FORMAT_BC4\_UNORM<sup>FNC</sup> (80)</span></span>
| <span data-ttu-id="f42ab-4401">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-4401">Target</span></span> | <span data-ttu-id="f42ab-4402">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-4402">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-4403">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4403">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-4404">4</span><span class="sxs-lookup"><span data-stu-id="f42ab-4404">4</span></span> |
| <span data-ttu-id="f42ab-4405">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-4405">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-4406">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-4406">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4407">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4407">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4408">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4408">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4409">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4409">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4410">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4410">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-4411">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4411">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-4412">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4412">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-4413">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-4413">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-4414">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4414">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-4415">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4415">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4416">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4416">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4417">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4417">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4418">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-4418">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-4419">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-4419">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-4420">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4420">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-4421">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4421">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-4422">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4422">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4423">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-4423">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4424">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-4424">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-4425">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-4425">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-4426">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-4426">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4427">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4427">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4428">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4428">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-4429">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4429">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-4430">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4430">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-4431">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4431">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-4432">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-4432">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-4433">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-4433">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-4434">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4434">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-4435">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-4435">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4436">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4436">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4437">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-4437">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-4438">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4438">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4439">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-4439">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4440">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-4440">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-4441">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-4441">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-4442">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-4442">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-4443">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-4443">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-4444">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-4444">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-4445">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4445">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-4446">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4446">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-4447">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4447">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-4448">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4448">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-4449">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-4449">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_snormsupfncsup-81"></a><span data-ttu-id="f42ab-4450">DXGI_FORMAT_BC4 \_ SNORM<sup>FNC</sup> (81)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4450">DXGI_FORMAT_BC4\_SNORM<sup>FNC</sup> (81)</span></span>
| <span data-ttu-id="f42ab-4451">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-4451">Target</span></span> | <span data-ttu-id="f42ab-4452">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-4452">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-4453">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4453">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-4454">4</span><span class="sxs-lookup"><span data-stu-id="f42ab-4454">4</span></span> |
| <span data-ttu-id="f42ab-4455">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-4455">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-4456">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-4456">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4457">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4457">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4458">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4458">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4459">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4459">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4460">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4460">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-4461">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4461">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-4462">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4462">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-4463">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-4463">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-4464">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4464">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-4465">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4465">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4466">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4466">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4467">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4467">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4468">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-4468">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-4469">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-4469">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-4470">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4470">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-4471">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4471">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-4472">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4472">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4473">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-4473">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4474">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-4474">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-4475">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-4475">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-4476">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-4476">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4477">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4477">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4478">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4478">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-4479">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4479">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-4480">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4480">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-4481">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4481">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-4482">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-4482">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-4483">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-4483">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-4484">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4484">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-4485">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-4485">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4486">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4486">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4487">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-4487">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-4488">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4488">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4489">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-4489">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4490">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-4490">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-4491">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-4491">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-4492">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-4492">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-4493">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-4493">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-4494">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-4494">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-4495">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4495">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-4496">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4496">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-4497">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4497">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-4498">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4498">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-4499">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-4499">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="f42ab-4500">DXGI_FORMAT_BC5 \_ <sup>PCC</sup> de tipo (82)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4500">DXGI_FORMAT_BC5\_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="f42ab-4501">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-4501">Target</span></span> | <span data-ttu-id="f42ab-4502">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-4502">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-4503">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4503">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-4504">8</span><span class="sxs-lookup"><span data-stu-id="f42ab-4504">8</span></span> |
| <span data-ttu-id="f42ab-4505">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-4505">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-4506">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-4506">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4507">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4507">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4508">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4508">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4509">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4509">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4510">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4510">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-4511">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4511">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-4512">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4512">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-4513">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-4513">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-4514">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4514">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-4515">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4515">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4516">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4516">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4517">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4517">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4518">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-4518">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-4519">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-4519">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-4520">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4520">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-4521">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4521">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-4522">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4522">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4523">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-4523">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4524">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-4524">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-4525">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-4525">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-4526">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-4526">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4527">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4527">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4528">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4528">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-4529">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4529">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-4530">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4530">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-4531">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4531">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-4532">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-4532">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-4533">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-4533">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-4534">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4534">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-4535">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-4535">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4536">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4536">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4537">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-4537">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-4538">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4538">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4539">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-4539">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4540">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-4540">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-4541">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-4541">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-4542">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-4542">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-4543">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-4543">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-4544">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-4544">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-4545">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4545">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-4546">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4546">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-4547">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4547">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-4548">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4548">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-4549">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-4549">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_unormsupfncsup-83"></a><span data-ttu-id="f42ab-4550">DXGI_FORMAT_BC5 \_ UNORM<sup>FNC</sup> (83)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4550">DXGI_FORMAT_BC5\_UNORM<sup>FNC</sup> (83)</span></span>
| <span data-ttu-id="f42ab-4551">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-4551">Target</span></span> | <span data-ttu-id="f42ab-4552">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-4552">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-4553">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4553">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-4554">8</span><span class="sxs-lookup"><span data-stu-id="f42ab-4554">8</span></span> |
| <span data-ttu-id="f42ab-4555">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-4555">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-4556">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-4556">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4557">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4557">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4558">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4558">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4559">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4559">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4560">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4560">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-4561">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4561">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-4562">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4562">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-4563">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-4563">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-4564">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4564">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-4565">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4565">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4566">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4566">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4567">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4567">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4568">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-4568">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-4569">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-4569">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-4570">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4570">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-4571">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4571">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-4572">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4572">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4573">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-4573">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4574">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-4574">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-4575">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-4575">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-4576">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-4576">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4577">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4577">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4578">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4578">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-4579">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4579">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-4580">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4580">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-4581">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4581">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-4582">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-4582">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-4583">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-4583">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-4584">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4584">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-4585">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-4585">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4586">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4586">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4587">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-4587">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-4588">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4588">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4589">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-4589">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4590">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-4590">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-4591">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-4591">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-4592">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-4592">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-4593">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-4593">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-4594">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-4594">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-4595">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4595">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-4596">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4596">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-4597">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4597">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-4598">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4598">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-4599">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-4599">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_snormsupfncsup-84"></a><span data-ttu-id="f42ab-4600">DXGI_FORMAT_BC5 \_ SNORM<sup>FNC</sup> (84)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4600">DXGI_FORMAT_BC5\_SNORM<sup>FNC</sup> (84)</span></span>
| <span data-ttu-id="f42ab-4601">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-4601">Target</span></span> | <span data-ttu-id="f42ab-4602">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-4602">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-4603">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4603">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-4604">8</span><span class="sxs-lookup"><span data-stu-id="f42ab-4604">8</span></span> |
| <span data-ttu-id="f42ab-4605">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-4605">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-4606">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-4606">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4607">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4607">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4608">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4608">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4609">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4609">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4610">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4610">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-4611">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4611">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-4612">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4612">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-4613">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-4613">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-4614">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4614">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-4615">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4615">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4616">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4616">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4617">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4617">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4618">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-4618">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-4619">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-4619">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-4620">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4620">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-4621">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4621">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-4622">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4622">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4623">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-4623">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4624">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-4624">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-4625">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-4625">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-4626">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-4626">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4627">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4627">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4628">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4628">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-4629">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4629">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-4630">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4630">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-4631">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4631">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-4632">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-4632">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-4633">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-4633">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-4634">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4634">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-4635">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-4635">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4636">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4636">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4637">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-4637">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-4638">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4638">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4639">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-4639">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4640">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-4640">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-4641">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-4641">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-4642">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-4642">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-4643">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-4643">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-4644">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-4644">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-4645">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4645">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-4646">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4646">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-4647">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4647">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-4648">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4648">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-4649">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-4649">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="f42ab-4650">DXGI_FORMAT_B5G6R5 \_ UNORM<sup>FNS</sup> (85)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4650">DXGI_FORMAT_B5G6R5\_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="f42ab-4651">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-4651">Target</span></span> | <span data-ttu-id="f42ab-4652">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-4652">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-4653">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4653">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-4654">16</span><span class="sxs-lookup"><span data-stu-id="f42ab-4654">16</span></span> |
| <span data-ttu-id="f42ab-4655">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-4655">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4657">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-4657">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4658">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4658">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4659">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4659">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4660">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4660">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4661">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4661">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-4662">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4662">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4664">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4664">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-4665">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-4665">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4667">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4667">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4669">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4669">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4671">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4671">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4672">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4672">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4673">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-4673">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-4674">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-4674">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-4675">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4675">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4677">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4677">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4679">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4679">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4681">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-4681">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4683">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-4683">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-4684">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-4684">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-4685">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-4685">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4686">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4686">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4687">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4687">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-4688">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4688">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-4689">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4689">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-4690">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4690">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-4691">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-4691">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-4692">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-4692">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-4693">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4693">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-4694">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-4694">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4695">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4695">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4696">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-4696">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4698">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4698">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-4700">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-4700">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-4702">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-4702">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-4704">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-4704">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4706">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-4706">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-4707">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-4707">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-4708">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-4708">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-4709">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4709">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-4710">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4710">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-4711">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4711">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-4712">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4712">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-4713">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-4713">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="f42ab-4714">DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>FNS</sup> (86)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4714">DXGI_FORMAT_B5G5R5A1\_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="f42ab-4715">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-4715">Target</span></span> | <span data-ttu-id="f42ab-4716">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-4716">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-4717">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4717">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-4718">16</span><span class="sxs-lookup"><span data-stu-id="f42ab-4718">16</span></span> |
| <span data-ttu-id="f42ab-4719">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-4719">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4721">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-4721">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4722">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4722">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4723">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4723">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4724">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4724">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4725">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4725">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-4726">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4726">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4728">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4728">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-4729">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-4729">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4731">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4731">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4733">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4733">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4735">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4735">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4736">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4736">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4737">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-4737">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-4738">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-4738">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-4739">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4739">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4741">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4741">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-4742">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4742">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4743">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-4743">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4744">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-4744">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-4745">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-4745">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-4746">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-4746">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4747">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4747">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4748">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4748">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-4749">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4749">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-4750">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4750">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-4751">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4751">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-4752">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-4752">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-4753">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-4753">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-4754">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4754">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-4755">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-4755">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4756">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4756">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4757">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-4757">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4759">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4759">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4760">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-4760">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4761">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-4761">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-4762">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-4762">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-4763">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-4763">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-4764">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-4764">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-4765">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-4765">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-4766">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4766">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-4767">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4767">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-4768">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4768">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-4769">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4769">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-4770">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-4770">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="f42ab-4771">DXGI_FORMAT_B8G8R8A8 \_ <sup>PCs</sup> não tipados (90)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4771">DXGI_FORMAT_B8G8R8A8\_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="f42ab-4772">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-4772">Target</span></span> | <span data-ttu-id="f42ab-4773">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-4773">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-4774">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4774">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-4775">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-4775">32</span></span> |
| <span data-ttu-id="f42ab-4776">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-4776">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-4777">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-4777">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4778">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4778">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4779">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4779">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4780">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4780">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4781">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4781">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-4782">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4782">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-4783">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4783">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-4784">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-4784">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-4785">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4785">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-4786">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4786">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4787">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4787">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4788">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4788">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4789">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-4789">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-4790">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-4790">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-4791">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4791">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-4792">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4792">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-4793">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4793">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4794">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-4794">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4795">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-4795">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-4796">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-4796">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-4797">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-4797">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4798">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4798">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4799">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4799">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-4800">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4800">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-4801">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4801">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-4802">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4802">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-4803">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-4803">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-4804">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-4804">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-4805">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4805">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-4806">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-4806">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4807">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4807">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4808">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-4808">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-4809">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4809">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4810">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-4810">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4811">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-4811">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-4812">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-4812">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-4813">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-4813">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-4814">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-4814">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-4815">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-4815">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-4816">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4816">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-4817">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4817">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-4818">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4818">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-4819">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4819">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-4820">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-4820">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfnssup-87"></a><span data-ttu-id="f42ab-4821">DXGI_FORMAT_B8G8R8A8 \_ UNORM<sup>FNS</sup> (87)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4821">DXGI_FORMAT_B8G8R8A8\_UNORM<sup>FNS</sup> (87)</span></span>
| <span data-ttu-id="f42ab-4822">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-4822">Target</span></span> | <span data-ttu-id="f42ab-4823">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-4823">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-4824">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4824">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-4825">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-4825">32</span></span> |
| <span data-ttu-id="f42ab-4826">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-4826">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4828">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-4828">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4829">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4829">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4830">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4830">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4831">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4831">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4832">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4832">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-4833">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4833">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4835">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4835">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4837">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-4837">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4839">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4839">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4841">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4841">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4843">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4843">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4844">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4844">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4845">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-4845">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-4846">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-4846">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-4847">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4847">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4849">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4849">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4851">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4851">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4853">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-4853">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4855">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-4855">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-4856">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-4856">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-4857">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-4857">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4858">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4858">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4859">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4859">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-4860">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4860">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-4861">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4861">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-4862">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4862">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-4863">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-4863">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-4864">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-4864">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-4865">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4865">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-4866">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-4866">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4867">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4867">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4868">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-4868">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4870">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4870">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-4872">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-4872">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-4874">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-4874">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-4876">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-4876">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4878">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-4878">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-4879">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-4879">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4881">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-4881">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-4882">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4882">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-4883">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4883">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-4885">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4885">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4887">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4887">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4889">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-4889">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfnssup-91"></a><span data-ttu-id="f42ab-4890">DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ sRGB<sup>FNS</sup> (91)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4890">DXGI_FORMAT_B8G8R8A8\_UNORM\_SRGB<sup>FNS</sup> (91)</span></span>
| <span data-ttu-id="f42ab-4891">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-4891">Target</span></span> | <span data-ttu-id="f42ab-4892">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-4892">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-4893">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4893">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-4894">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-4894">32</span></span> |
| <span data-ttu-id="f42ab-4895">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-4895">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4897">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-4897">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4898">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4898">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4899">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4899">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4900">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4900">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4901">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4901">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-4902">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4902">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4904">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4904">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4906">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-4906">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4908">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4908">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4910">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4910">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4912">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4912">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4913">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4913">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4914">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-4914">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-4915">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-4915">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-4916">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4916">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4918">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4918">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4920">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4920">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4922">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-4922">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4924">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-4924">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-4925">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-4925">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-4926">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-4926">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4927">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4927">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4928">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4928">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-4929">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4929">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-4930">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4930">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-4931">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4931">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-4932">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-4932">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-4933">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-4933">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-4934">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4934">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-4935">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-4935">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4936">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4936">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4937">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-4937">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4939">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4939">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-4941">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-4941">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-4943">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-4943">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-4945">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-4945">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4947">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-4947">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-4948">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-4948">Display Scan-Out</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4950">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-4950">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-4951">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4951">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-4952">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4952">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-4954">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4954">Video Processor Output</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4956">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4956">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-4958">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-4958">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="f42ab-4959">DXGI_FORMAT_B8G8R8X8 \_ <sup>PCs</sup> não tipados (92)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4959">DXGI_FORMAT_B8G8R8X8\_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="f42ab-4960">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-4960">Target</span></span> | <span data-ttu-id="f42ab-4961">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-4961">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-4962">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4962">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-4963">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-4963">32</span></span> |
| <span data-ttu-id="f42ab-4964">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-4964">Format Support</span></span> | \- |
| <span data-ttu-id="f42ab-4965">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-4965">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4966">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4966">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4967">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-4967">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4968">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4968">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-4969">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4969">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-4970">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4970">Texture2D</span></span> | \- |
| <span data-ttu-id="f42ab-4971">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-4971">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-4972">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-4972">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-4973">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4973">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-4974">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4974">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4975">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4975">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4976">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-4976">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-4977">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-4977">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-4978">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-4978">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-4979">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4979">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-4980">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-4980">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-4981">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4981">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4982">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-4982">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4983">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-4983">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-4984">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-4984">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-4985">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-4985">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4986">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4986">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-4987">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-4987">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-4988">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4988">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-4989">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4989">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-4990">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4990">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-4991">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-4991">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-4992">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-4992">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-4993">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-4993">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-4994">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-4994">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4995">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-4995">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-4996">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-4996">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-4997">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-4997">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4998">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-4998">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-4999">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-4999">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-5000">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-5000">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-5001">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-5001">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-5002">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-5002">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-5003">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-5003">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-5004">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5004">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-5005">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5005">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-5006">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5006">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-5007">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5007">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-5008">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-5008">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfnssup-88"></a><span data-ttu-id="f42ab-5009">DXGI_FORMAT_B8G8R8X8 \_ UNORM<sup>FNS</sup> (88)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5009">DXGI_FORMAT_B8G8R8X8\_UNORM<sup>FNS</sup> (88)</span></span>
| <span data-ttu-id="f42ab-5010">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-5010">Target</span></span> | <span data-ttu-id="f42ab-5011">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-5011">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-5012">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5012">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-5013">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-5013">32</span></span> |
| <span data-ttu-id="f42ab-5014">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-5014">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5016">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-5016">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5017">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5017">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5018">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5018">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5019">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5019">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5020">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5020">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-5021">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5021">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5023">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5023">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5025">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-5025">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5027">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5027">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5029">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5029">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5031">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5031">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5032">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5032">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5033">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-5033">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-5034">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-5034">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-5035">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5035">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5037">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5037">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5039">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5039">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5041">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-5041">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5043">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-5043">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-5044">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-5044">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-5045">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-5045">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5046">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5046">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5047">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5047">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-5048">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5048">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-5049">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5049">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-5050">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5050">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-5051">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-5051">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-5052">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-5052">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-5053">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5053">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-5054">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-5054">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5055">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5055">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5056">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-5056">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5058">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5058">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5060">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-5060">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5062">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-5062">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5064">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-5064">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5066">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-5066">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-5067">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-5067">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-5068">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-5068">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-5069">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5069">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-5070">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5070">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5072">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5072">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5074">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5074">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5076">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-5076">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfnssup-93"></a><span data-ttu-id="f42ab-5077">DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ sRGB<sup>FNS</sup> (93)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5077">DXGI_FORMAT_B8G8R8X8\_UNORM\_SRGB<sup>FNS</sup> (93)</span></span>
| <span data-ttu-id="f42ab-5078">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-5078">Target</span></span> | <span data-ttu-id="f42ab-5079">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-5079">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-5080">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5080">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-5081">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-5081">32</span></span> |
| <span data-ttu-id="f42ab-5082">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-5082">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5084">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-5084">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5085">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5085">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5086">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5086">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5087">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5087">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5088">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5088">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-5089">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5089">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5091">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5091">Texture3D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5093">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-5093">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5095">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5095">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5097">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5097">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5099">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5099">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5100">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5100">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5101">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-5101">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-5102">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-5102">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-5103">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5103">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5105">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5105">Mipmap Auto-Generation</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5107">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5107">RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5109">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-5109">Blendable RenderTarget</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5111">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-5111">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-5112">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-5112">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-5113">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-5113">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5114">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5114">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5115">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5115">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-5116">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5116">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-5117">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5117">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-5118">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5118">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-5119">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-5119">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-5120">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-5120">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-5121">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5121">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-5122">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-5122">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5123">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5123">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5124">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-5124">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5126">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5126">4x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5128">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-5128">8x Multisample RenderTarget</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5130">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-5130">Other Multisample Count RT</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5132">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-5132">Multisample Resolve</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5134">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-5134">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-5135">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-5135">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-5136">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-5136">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-5137">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5137">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-5138">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5138">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-5139">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5139">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-5140">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5140">Shared Resource</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5142">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-5142">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="f42ab-5143">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5143">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="f42ab-5144">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-5144">Target</span></span> | <span data-ttu-id="f42ab-5145">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-5145">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-5146">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5146">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-5147">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-5147">32</span></span> |
| <span data-ttu-id="f42ab-5148">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-5148">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5150">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-5150">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5151">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5151">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5152">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5152">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5153">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5153">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5154">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5154">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-5155">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5155">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5157">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5157">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-5158">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-5158">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-5159">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5159">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-5160">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5160">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5161">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5161">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5162">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5162">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5163">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-5163">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-5164">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-5164">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-5165">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5165">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-5166">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5166">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-5167">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5167">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5168">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-5168">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5169">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-5169">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-5170">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-5170">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-5171">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-5171">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5172">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5172">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5173">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5173">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-5174">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5174">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-5175">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5175">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-5176">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5176">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-5177">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-5177">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-5178">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-5178">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-5179">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5179">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-5180">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-5180">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5181">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5181">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5182">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-5182">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5184">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5184">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5185">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-5185">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5186">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-5186">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-5187">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-5187">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-5188">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-5188">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-5189">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-5189">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-5190">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-5190">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-5191">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5191">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5193">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5193">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5195">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5195">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5197">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5197">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-5198">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-5198">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="f42ab-5199">DXGI_FORMAT_Y410<sup>V</sup> (101)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5199">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="f42ab-5200">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-5200">Target</span></span> | <span data-ttu-id="f42ab-5201">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-5201">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-5202">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5202">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-5203">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-5203">32</span></span> |
| <span data-ttu-id="f42ab-5204">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-5204">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5206">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-5206">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5207">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5207">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5208">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5208">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5209">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5209">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5210">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5210">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-5211">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5211">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5213">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5213">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-5214">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-5214">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-5215">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5215">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-5216">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5216">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5217">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5217">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5218">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5218">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5219">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-5219">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-5220">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-5220">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-5221">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5221">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-5222">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5222">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-5223">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5223">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5224">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-5224">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5225">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-5225">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-5226">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-5226">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-5227">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-5227">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5228">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5228">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5229">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5229">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-5230">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5230">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-5231">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5231">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-5232">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5232">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-5233">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-5233">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-5234">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-5234">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-5235">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5235">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-5236">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-5236">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5237">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5237">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5238">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-5238">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5240">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5240">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5241">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-5241">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5242">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-5242">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-5243">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-5243">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-5244">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-5244">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-5245">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-5245">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-5246">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-5246">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-5247">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5247">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5249">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5249">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5251">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5251">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5253">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5253">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-5254">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-5254">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="f42ab-5255">DXGI_FORMAT_Y416<sup>V</sup> (102)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5255">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="f42ab-5256">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-5256">Target</span></span> | <span data-ttu-id="f42ab-5257">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-5257">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-5258">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5258">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-5259">64</span><span class="sxs-lookup"><span data-stu-id="f42ab-5259">64</span></span> |
| <span data-ttu-id="f42ab-5260">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-5260">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5262">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-5262">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5263">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5263">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5264">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5264">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5265">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5265">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5266">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5266">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-5267">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5267">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5269">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5269">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-5270">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-5270">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-5271">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5271">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-5272">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5272">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5273">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5273">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5274">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5274">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5275">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-5275">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-5276">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-5276">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-5277">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5277">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-5278">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5278">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-5279">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5279">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5280">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-5280">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5281">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-5281">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-5282">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-5282">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-5283">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-5283">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5284">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5284">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5285">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5285">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-5286">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5286">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-5287">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5287">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-5288">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5288">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-5289">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-5289">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-5290">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-5290">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-5291">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5291">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-5292">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-5292">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5293">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5293">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5294">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-5294">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5296">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5296">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5297">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-5297">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5298">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-5298">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-5299">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-5299">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-5300">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-5300">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-5301">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-5301">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-5302">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-5302">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-5303">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5303">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5305">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5305">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5307">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5307">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5309">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5309">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-5310">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-5310">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="f42ab-5311">DXGI_FORMAT_NV12<sup>V</sup> (103)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5311">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="f42ab-5312">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-5312">Target</span></span> | <span data-ttu-id="f42ab-5313">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-5313">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-5314">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5314">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-5315">8</span><span class="sxs-lookup"><span data-stu-id="f42ab-5315">8</span></span> |
| <span data-ttu-id="f42ab-5316">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-5316">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5318">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-5318">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5319">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5319">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5320">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5320">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5321">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5321">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5322">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5322">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-5323">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5323">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5325">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5325">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-5326">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-5326">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-5327">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5327">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-5328">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5328">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5329">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5329">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5330">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5330">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5331">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-5331">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-5332">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-5332">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-5333">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5333">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-5334">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5334">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-5335">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5335">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5336">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-5336">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5337">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-5337">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-5338">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-5338">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-5339">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-5339">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5340">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5340">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5341">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5341">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-5342">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5342">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-5343">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5343">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-5344">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5344">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-5345">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-5345">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-5346">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-5346">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-5347">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5347">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-5348">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-5348">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5349">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5349">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5350">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-5350">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5352">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5352">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5353">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-5353">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5354">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-5354">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-5355">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-5355">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-5356">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-5356">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-5357">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-5357">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-5358">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-5358">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-5359">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5359">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5361">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5361">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5363">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5363">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5365">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5365">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-5366">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-5366">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="f42ab-5367">DXGI_FORMAT_P010<sup>V</sup> (104)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5367">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="f42ab-5368">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-5368">Target</span></span> | <span data-ttu-id="f42ab-5369">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-5369">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-5370">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5370">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-5371">16</span><span class="sxs-lookup"><span data-stu-id="f42ab-5371">16</span></span> |
| <span data-ttu-id="f42ab-5372">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-5372">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5374">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-5374">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5375">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5375">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5376">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5376">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5377">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5377">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5378">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5378">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-5379">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5379">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5381">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5381">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-5382">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-5382">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-5383">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5383">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-5384">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5384">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5385">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5385">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5386">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5386">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5387">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-5387">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-5388">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-5388">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-5389">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5389">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-5390">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5390">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-5391">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5391">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5392">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-5392">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5393">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-5393">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-5394">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-5394">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-5395">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-5395">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5396">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5396">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5397">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5397">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-5398">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5398">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-5399">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5399">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-5400">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5400">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-5401">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-5401">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-5402">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-5402">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-5403">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5403">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-5404">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-5404">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5405">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5405">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5406">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-5406">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5408">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5408">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5409">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-5409">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5410">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-5410">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-5411">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-5411">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-5412">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-5412">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-5413">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-5413">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-5414">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-5414">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-5415">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5415">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5417">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5417">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5419">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5419">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5421">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5421">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-5422">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-5422">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="f42ab-5423">DXGI_FORMAT_P016<sup>V</sup> (105)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5423">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="f42ab-5424">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-5424">Target</span></span> | <span data-ttu-id="f42ab-5425">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-5425">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-5426">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5426">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-5427">16</span><span class="sxs-lookup"><span data-stu-id="f42ab-5427">16</span></span> |
| <span data-ttu-id="f42ab-5428">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-5428">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5430">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-5430">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5431">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5431">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5432">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5432">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5433">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5433">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5434">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5434">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-5435">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5435">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5437">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5437">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-5438">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-5438">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-5439">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5439">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-5440">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5440">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5441">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5441">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5442">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5442">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5443">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-5443">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-5444">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-5444">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-5445">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5445">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-5446">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5446">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-5447">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5447">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5448">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-5448">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5449">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-5449">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-5450">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-5450">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-5451">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-5451">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5452">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5452">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5453">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5453">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-5454">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5454">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-5455">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5455">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-5456">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5456">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-5457">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-5457">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-5458">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-5458">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-5459">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5459">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-5460">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-5460">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5461">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5461">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5462">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-5462">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5464">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5464">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5465">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-5465">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5466">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-5466">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-5467">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-5467">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-5468">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-5468">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-5469">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-5469">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-5470">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-5470">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-5471">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5471">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5473">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5473">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5475">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5475">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5477">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5477">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-5478">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-5478">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="f42ab-5479">DXGI_FORMAT_420 \_ opaco<sup>V</sup> (106)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5479">DXGI_FORMAT_420\_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="f42ab-5480">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-5480">Target</span></span> | <span data-ttu-id="f42ab-5481">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-5481">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-5482">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5482">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-5483">8</span><span class="sxs-lookup"><span data-stu-id="f42ab-5483">8</span></span> |
| <span data-ttu-id="f42ab-5484">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-5484">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5486">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-5486">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5487">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5487">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5488">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5488">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5489">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5489">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5490">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5490">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-5491">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5491">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5493">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5493">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-5494">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-5494">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-5495">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5495">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-5496">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5496">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5497">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5497">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5498">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5498">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5499">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-5499">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-5500">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-5500">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-5501">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5501">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-5502">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5502">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-5503">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5503">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5504">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-5504">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5505">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-5505">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-5506">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-5506">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-5507">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-5507">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5508">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5508">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5509">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5509">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-5510">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5510">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-5511">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5511">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-5512">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5512">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-5513">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-5513">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-5514">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-5514">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-5515">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5515">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-5516">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-5516">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5517">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5517">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5518">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-5518">CPU Lockable</span></span> | \- |
| <span data-ttu-id="f42ab-5519">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5519">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5520">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-5520">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5521">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-5521">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-5522">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-5522">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-5523">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-5523">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-5524">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-5524">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-5525">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-5525">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-5526">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5526">Video Decoder Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5528">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5528">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5530">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5530">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5532">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5532">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-5533">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-5533">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="f42ab-5534">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5534">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="f42ab-5535">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-5535">Target</span></span> | <span data-ttu-id="f42ab-5536">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-5536">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-5537">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5537">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-5538">16</span><span class="sxs-lookup"><span data-stu-id="f42ab-5538">16</span></span> |
| <span data-ttu-id="f42ab-5539">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-5539">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5541">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-5541">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5542">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5542">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5543">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5543">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5544">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5544">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5545">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5545">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-5546">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5546">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5548">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5548">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-5549">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-5549">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-5550">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5550">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-5551">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5551">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5552">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5552">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5553">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5553">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5554">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-5554">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-5555">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-5555">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-5556">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5556">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-5557">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5557">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-5558">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5558">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5559">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-5559">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5560">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-5560">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-5561">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-5561">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-5562">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-5562">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5563">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5563">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5564">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5564">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-5565">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5565">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-5566">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5566">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-5567">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5567">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-5568">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-5568">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-5569">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-5569">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-5570">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5570">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-5571">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-5571">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5572">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5572">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5573">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-5573">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5575">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5575">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5576">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-5576">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5577">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-5577">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-5578">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-5578">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-5579">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-5579">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-5580">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-5580">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-5581">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-5581">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-5582">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5582">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5584">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5584">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5586">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5586">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5588">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5588">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-5589">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-5589">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="f42ab-5590">DXGI_FORMAT_Y210<sup>V</sup> (108)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5590">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="f42ab-5591">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-5591">Target</span></span> | <span data-ttu-id="f42ab-5592">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-5592">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-5593">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5593">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-5594">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-5594">32</span></span> |
| <span data-ttu-id="f42ab-5595">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-5595">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5597">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-5597">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5598">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5598">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5599">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5599">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5600">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5600">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5601">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5601">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-5602">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5602">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5604">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5604">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-5605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-5605">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-5606">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5606">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-5607">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5607">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5608">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5608">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5609">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5609">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5610">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-5610">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-5611">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-5611">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-5612">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5612">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-5613">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5613">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-5614">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5614">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5615">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-5615">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5616">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-5616">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-5617">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-5617">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-5618">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-5618">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5619">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5619">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5620">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5620">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-5621">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5621">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-5622">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5622">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-5623">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5623">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-5624">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-5624">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-5625">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-5625">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-5626">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5626">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-5627">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-5627">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5628">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5628">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5629">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-5629">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5631">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5631">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5632">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-5632">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5633">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-5633">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-5634">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-5634">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-5635">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-5635">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-5636">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-5636">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-5637">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-5637">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-5638">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5638">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5640">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5640">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5642">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5642">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5644">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5644">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-5645">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-5645">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="f42ab-5646">DXGI_FORMAT_Y216<sup>V</sup> (109)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5646">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="f42ab-5647">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-5647">Target</span></span> | <span data-ttu-id="f42ab-5648">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-5648">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-5649">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5649">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-5650">32</span><span class="sxs-lookup"><span data-stu-id="f42ab-5650">32</span></span> |
| <span data-ttu-id="f42ab-5651">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-5651">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5653">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-5653">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5654">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5654">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5655">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5655">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5656">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5656">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5657">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5657">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-5658">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5658">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5660">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5660">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-5661">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-5661">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-5662">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5662">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-5663">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5663">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5664">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5664">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5665">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5665">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5666">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-5666">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-5667">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-5667">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-5668">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5668">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-5669">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5669">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-5670">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5670">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5671">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-5671">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5672">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-5672">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-5673">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-5673">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-5674">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-5674">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5675">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5675">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5676">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5676">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-5677">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5677">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-5678">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5678">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-5679">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5679">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-5680">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-5680">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-5681">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-5681">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-5682">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5682">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-5683">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-5683">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5684">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5684">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5685">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-5685">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5687">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5687">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5688">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-5688">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5689">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-5689">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-5690">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-5690">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-5691">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-5691">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-5692">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-5692">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-5693">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-5693">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-5694">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5694">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5696">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5696">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5698">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5698">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5700">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5700">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-5701">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-5701">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="f42ab-5702">DXGI_FORMAT_NV11<sup>V</sup> (110)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5702">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="f42ab-5703">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-5703">Target</span></span> | <span data-ttu-id="f42ab-5704">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-5704">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-5705">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5705">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-5706">8</span><span class="sxs-lookup"><span data-stu-id="f42ab-5706">8</span></span> |
| <span data-ttu-id="f42ab-5707">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-5707">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5709">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-5709">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5710">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5710">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5711">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5711">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5712">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5712">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5713">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5713">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-5714">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5714">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5716">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5716">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-5717">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-5717">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-5718">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5718">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-5719">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5719">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5720">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5720">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5721">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5721">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5722">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-5722">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-5723">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-5723">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-5724">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5724">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-5725">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5725">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-5726">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5726">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5727">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-5727">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5728">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-5728">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-5729">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-5729">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-5730">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-5730">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5731">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5731">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5732">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5732">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-5733">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5733">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-5734">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5734">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-5735">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5735">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-5736">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-5736">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-5737">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-5737">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-5738">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5738">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-5739">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-5739">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5740">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5740">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5741">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-5741">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5743">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5743">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5744">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-5744">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5745">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-5745">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-5746">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-5746">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-5747">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-5747">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-5748">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-5748">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-5749">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-5749">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-5750">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5750">Video Decoder Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5752">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5752">Video Processor Input</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5754">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5754">Video Processor Output</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5756">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5756">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-5757">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-5757">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="f42ab-5758">DXGI_FORMAT_AI44<sup>V</sup> (111)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5758">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="f42ab-5759">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-5759">Target</span></span> | <span data-ttu-id="f42ab-5760">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-5760">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-5761">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5761">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-5762">8</span><span class="sxs-lookup"><span data-stu-id="f42ab-5762">8</span></span> |
| <span data-ttu-id="f42ab-5763">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-5763">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5765">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-5765">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5766">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5766">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5767">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5767">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5768">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5768">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5769">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5769">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-5770">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5770">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5772">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5772">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-5773">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-5773">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-5774">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5774">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-5775">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5775">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5776">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5776">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5777">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5777">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5778">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-5778">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-5779">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-5779">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-5780">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5780">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-5781">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5781">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-5782">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5782">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5783">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-5783">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5784">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-5784">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-5785">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-5785">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-5786">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-5786">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5787">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5787">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5788">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5788">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-5789">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5789">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-5790">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5790">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-5791">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5791">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-5792">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-5792">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-5793">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-5793">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-5794">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5794">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-5795">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-5795">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5796">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5796">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5797">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-5797">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5799">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5799">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5800">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-5800">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5801">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-5801">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-5802">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-5802">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-5803">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-5803">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-5804">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-5804">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-5805">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-5805">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-5806">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5806">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-5807">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5807">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5809">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5809">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-5810">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5810">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-5811">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-5811">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="f42ab-5812">DXGI_FORMAT_IA44<sup>V</sup> (112)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5812">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="f42ab-5813">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-5813">Target</span></span> | <span data-ttu-id="f42ab-5814">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-5814">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-5815">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5815">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-5816">8</span><span class="sxs-lookup"><span data-stu-id="f42ab-5816">8</span></span> |
| <span data-ttu-id="f42ab-5817">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-5817">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5819">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-5819">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5820">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5820">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5821">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5821">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5822">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5822">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5823">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5823">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-5824">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5824">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5826">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5826">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-5827">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-5827">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-5828">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5828">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-5829">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5829">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5830">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5830">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5831">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5831">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5832">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-5832">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-5833">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-5833">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-5834">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5834">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-5835">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5835">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-5836">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5836">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5837">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-5837">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5838">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-5838">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-5839">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-5839">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-5840">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-5840">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5841">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5841">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5842">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5842">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-5843">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5843">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-5844">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5844">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-5845">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5845">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-5846">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-5846">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-5847">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-5847">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-5848">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5848">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-5849">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-5849">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5850">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5850">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5851">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-5851">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5853">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5853">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5854">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-5854">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5855">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-5855">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-5856">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-5856">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-5857">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-5857">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-5858">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-5858">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-5859">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-5859">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-5860">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5860">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-5861">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5861">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5863">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5863">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-5864">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5864">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-5865">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-5865">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="f42ab-5866">DXGI_FORMAT_P8<sup>V</sup> (113)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5866">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="f42ab-5867">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-5867">Target</span></span> | <span data-ttu-id="f42ab-5868">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-5868">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-5869">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5869">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-5870">8</span><span class="sxs-lookup"><span data-stu-id="f42ab-5870">8</span></span> |
| <span data-ttu-id="f42ab-5871">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-5871">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5873">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-5873">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5874">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5874">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5875">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5875">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5876">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5876">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5877">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5877">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-5878">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5878">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5880">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5880">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-5881">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-5881">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-5882">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5882">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-5883">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5883">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5884">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5884">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5885">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5885">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5886">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-5886">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-5887">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-5887">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-5888">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5888">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-5889">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5889">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-5890">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5890">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5891">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-5891">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5892">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-5892">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-5893">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-5893">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-5894">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-5894">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5895">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5895">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5896">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5896">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-5897">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5897">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-5898">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5898">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-5899">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5899">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-5900">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-5900">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-5901">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-5901">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-5902">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5902">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-5903">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-5903">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5904">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5904">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5905">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-5905">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5907">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5907">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5908">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-5908">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5909">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-5909">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-5910">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-5910">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-5911">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-5911">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-5912">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-5912">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-5913">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-5913">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-5914">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5914">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-5915">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5915">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5917">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5917">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-5918">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5918">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-5919">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-5919">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="f42ab-5920">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5920">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="f42ab-5921">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-5921">Target</span></span> | <span data-ttu-id="f42ab-5922">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-5922">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-5923">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5923">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-5924">16</span><span class="sxs-lookup"><span data-stu-id="f42ab-5924">16</span></span> |
| <span data-ttu-id="f42ab-5925">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-5925">Format Support</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-5927">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-5927">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5928">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5928">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5929">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5929">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5930">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5930">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5931">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5931">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-5932">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5932">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5934">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5934">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-5935">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-5935">TextureCube</span></span> | \- |
| <span data-ttu-id="f42ab-5936">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5936">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="f42ab-5937">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5937">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5938">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5938">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5939">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5939">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5940">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-5940">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-5941">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-5941">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-5942">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5942">Mipmap</span></span> | \- |
| <span data-ttu-id="f42ab-5943">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5943">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="f42ab-5944">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5944">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5945">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-5945">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5946">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-5946">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-5947">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-5947">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-5948">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-5948">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5949">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5949">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-5950">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5950">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-5951">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5951">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-5952">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5952">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-5953">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5953">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-5954">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-5954">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-5955">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-5955">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-5956">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-5956">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-5957">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-5957">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5958">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5958">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-5959">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-5959">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5961">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-5961">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5962">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-5962">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-5963">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-5963">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-5964">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-5964">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-5965">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-5965">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-5966">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-5966">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-5967">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-5967">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-5968">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5968">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-5969">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5969">Video Processor Input</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5971">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5971">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-5972">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-5972">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-5973">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-5973">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a><span data-ttu-id="f42ab-5974">DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>FNS</sup> (115)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5974">DXGI_FORMAT_B4G4R4A4\_UNORM<sup>FNS</sup> (115)</span></span>
| <span data-ttu-id="f42ab-5975">Destino</span><span class="sxs-lookup"><span data-stu-id="f42ab-5975">Target</span></span> | <span data-ttu-id="f42ab-5976">Suporte</span><span class="sxs-lookup"><span data-stu-id="f42ab-5976">Support</span></span> |
| - | - |
| <span data-ttu-id="f42ab-5977">Bits por elemento (BPE)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5977">Bits Per Element (BPE)</span></span> | <span data-ttu-id="f42ab-5978">16</span><span class="sxs-lookup"><span data-stu-id="f42ab-5978">16</span></span> |
| <span data-ttu-id="f42ab-5979">Suporte de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-5979">Format Support</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5981">Buffer</span><span class="sxs-lookup"><span data-stu-id="f42ab-5981">Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5982">Buffer de vértice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5982">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5983">Buffer de índice do assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f42ab-5983">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5984">Buffer de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="f42ab-5984">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="f42ab-5985">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5985">Texture1D</span></span> | \- |
| <span data-ttu-id="f42ab-5986">Texture2D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5986">Texture2D</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5988">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f42ab-5988">Texture3D</span></span> | \- |
| <span data-ttu-id="f42ab-5989">TextureCube</span><span class="sxs-lookup"><span data-stu-id="f42ab-5989">TextureCube</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5991">Amostra de sombreador (somente de ponto de amostra)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5991">Shader sample (point sample only)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5993">Amostra de sombreador (qualquer filtro)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5993">Shader sample (any filter)</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-5995">Exemplo de sombreador \_ c (filtro de comparação)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5995">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5996">Amostra de sombreador (filtro mono de 1 bit)</span><span class="sxs-lookup"><span data-stu-id="f42ab-5996">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="f42ab-5997">Gather4 do sombreador</span><span class="sxs-lookup"><span data-stu-id="f42ab-5997">Shader gather4</span></span> | \- |
| <span data-ttu-id="f42ab-5998">Sombreador gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="f42ab-5998">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="f42ab-5999">Mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-5999">Mipmap</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-6001">Geração automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="f42ab-6001">Mipmap Auto-Generation</span></span> | ![opcionais](images/letter-o.jpg) |
| <span data-ttu-id="f42ab-6003">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-6003">RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-6004">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="f42ab-6004">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-6005">Operação lógica de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f42ab-6005">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="f42ab-6006">Destino de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="f42ab-6006">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="f42ab-6007">UAV e SRV brutos</span><span class="sxs-lookup"><span data-stu-id="f42ab-6007">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-6008">UAV estruturado e SRV</span><span class="sxs-lookup"><span data-stu-id="f42ab-6008">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="f42ab-6009">UAV digitado</span><span class="sxs-lookup"><span data-stu-id="f42ab-6009">Typed UAV</span></span> | \- |
| <span data-ttu-id="f42ab-6010">Armazenamento digitado UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-6010">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="f42ab-6011">Carga digitada UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-6011">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="f42ab-6012">Adição atômica de UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-6012">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="f42ab-6013">Ops bits UAV atômicas</span><span class="sxs-lookup"><span data-stu-id="f42ab-6013">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="f42ab-6014">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="f42ab-6014">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="f42ab-6015">Troca atômica UAV</span><span class="sxs-lookup"><span data-stu-id="f42ab-6015">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="f42ab-6016">UAV com sinal mínimo ou máximo de Atomic</span><span class="sxs-lookup"><span data-stu-id="f42ab-6016">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-6017">UAV atômica não assinado mínimo ou máximo</span><span class="sxs-lookup"><span data-stu-id="f42ab-6017">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="f42ab-6018">Bloqueáveis de CPU</span><span class="sxs-lookup"><span data-stu-id="f42ab-6018">CPU Lockable</span></span> | ![exigido](images/letter-r.jpg) |
| <span data-ttu-id="f42ab-6020">4x multiamostrar RenderTarget</span><span class="sxs-lookup"><span data-stu-id="f42ab-6020">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-6021">RenderTarget de multiamostra 8x</span><span class="sxs-lookup"><span data-stu-id="f42ab-6021">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="f42ab-6022">Outros RT de contagem multiamostrais</span><span class="sxs-lookup"><span data-stu-id="f42ab-6022">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="f42ab-6023">Resolução de multiamostras</span><span class="sxs-lookup"><span data-stu-id="f42ab-6023">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="f42ab-6024">Carga de multiamostra</span><span class="sxs-lookup"><span data-stu-id="f42ab-6024">Multisample Load</span></span> | \- |
| <span data-ttu-id="f42ab-6025">Exibir Scan-Out</span><span class="sxs-lookup"><span data-stu-id="f42ab-6025">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="f42ab-6026">Converter no layout de bit</span><span class="sxs-lookup"><span data-stu-id="f42ab-6026">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="f42ab-6027">Suporte a decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-6027">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="f42ab-6028">Entrada do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-6028">Video Processor Input</span></span> | \- |
| <span data-ttu-id="f42ab-6029">Saída do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-6029">Video Processor Output</span></span> | \- |
| <span data-ttu-id="f42ab-6030">Recurso Compartilhado</span><span class="sxs-lookup"><span data-stu-id="f42ab-6030">Shared Resource</span></span> | \- |
| <span data-ttu-id="f42ab-6031">Recurso em ladrilho</span><span class="sxs-lookup"><span data-stu-id="f42ab-6031">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="f42ab-6032">Observações de formato</span><span class="sxs-lookup"><span data-stu-id="f42ab-6032">Format notes</span></span>

<span data-ttu-id="f42ab-6033">A finalidade do formato pode mudar de um nível de recurso de hardware para o próximo.</span><span class="sxs-lookup"><span data-stu-id="f42ab-6033">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="f42ab-6034"><sup>L</sup> : formato de tipo informativo</span><span class="sxs-lookup"><span data-stu-id="f42ab-6034"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="f42ab-6035"><sup>PCs</sup> : layout de tipo parcial, convertido e simples</span><span class="sxs-lookup"><span data-stu-id="f42ab-6035"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="f42ab-6036"><sup>FCS</sup> : layout totalmente tipado, convertido e simples</span><span class="sxs-lookup"><span data-stu-id="f42ab-6036"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="f42ab-6037"><sup>FNS</sup> : layout totalmente tipado, não-convertido e simples</span><span class="sxs-lookup"><span data-stu-id="f42ab-6037"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="f42ab-6038"><sup>PCC</sup> : layout complexo, convertido e de tipo parcial</span><span class="sxs-lookup"><span data-stu-id="f42ab-6038"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="f42ab-6039"><sup>FCC</sup> : layout totalmente tipado, convertido e complexo</span><span class="sxs-lookup"><span data-stu-id="f42ab-6039"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="f42ab-6040"><sup>FNC</sup> : layout totalmente tipado, não-convertido e complexo</span><span class="sxs-lookup"><span data-stu-id="f42ab-6040"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="f42ab-6041"><sup>V</sup> : formato de vídeo</span><span class="sxs-lookup"><span data-stu-id="f42ab-6041"><sup>V</sup> : video format</span></span>
</dt> </dl>

## <a name="related-topics"></a><span data-ttu-id="f42ab-6042">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f42ab-6042">Related topics</span></span>

[<span data-ttu-id="f42ab-6043">Níveis de recursos de hardware do D3D12</span><span class="sxs-lookup"><span data-stu-id="f42ab-6043">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

<span data-ttu-id="f42ab-6044">[Implementando buffers de sombra para o nível de recurso do Direct3D 9](/previous-versions/windows/apps/jj262110(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="f42ab-6044">[Implementing shadow buffers for Direct3D feature level 9](/previous-versions/windows/apps/jj262110(v=win.10))</span></span>

[<span data-ttu-id="f42ab-6045">Mapeando formatos herdados</span><span class="sxs-lookup"><span data-stu-id="f42ab-6045">Mapping Legacy Formats</span></span>](../direct3d10/d3d10-graphics-programming-guide-resources-legacy-formats.md)

[<span data-ttu-id="f42ab-6046">Guia de programação para DXGI</span><span class="sxs-lookup"><span data-stu-id="f42ab-6046">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
