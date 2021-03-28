---
title: Referência do modo de formato BC7
description: Esta documentação contém uma lista de 8 modos de bloqueio e alocações de bits para blocos de formato de compactação de textura BC7.
ms.assetid: B1CEB729-6694-49BF-ACB9-FD1EFAB0B0D1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719a223e6ac057b949d5e1222582058f637ec526
ms.sourcegitcommit: 62e758931c610782807c7c9fad284921a6c56232
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/22/2020
ms.locfileid: "104365420"
---
# <a name="bc7-format-mode-reference"></a><span data-ttu-id="ebc05-103">Referência do modo de formato BC7</span><span class="sxs-lookup"><span data-stu-id="ebc05-103">BC7 Format Mode Reference</span></span>

<span data-ttu-id="ebc05-104">Esta documentação contém uma lista de 8 modos de bloqueio e alocações de bits para blocos de formato de compactação de textura BC7.</span><span class="sxs-lookup"><span data-stu-id="ebc05-104">This documentation contains a list of the 8 block modes and bit allocations for BC7 texture compression format blocks.</span></span>

<span data-ttu-id="ebc05-105">As cores para cada subconjunto dentro de um bloco são representadas por duas cores de ponto de extremidade explícitas e um conjunto de cores interpoladas entre elas.</span><span class="sxs-lookup"><span data-stu-id="ebc05-105">The colors for each subset within a block are represented by two explicit endpoint colors and a set of interpolated colors between them.</span></span> <span data-ttu-id="ebc05-106">Dependendo da precisão de índice do bloco, cada subconjunto pode ter 4, 8 ou 16 cores possíveis.</span><span class="sxs-lookup"><span data-stu-id="ebc05-106">Depending on the block's index precision, each subset can have 4, 8 or 16 possible colors.</span></span>

-   [<span data-ttu-id="ebc05-107">Modo 0</span><span class="sxs-lookup"><span data-stu-id="ebc05-107">Mode 0</span></span>](#mode-0)
-   [<span data-ttu-id="ebc05-108">Modo 1</span><span class="sxs-lookup"><span data-stu-id="ebc05-108">Mode 1</span></span>](#mode-1)
-   [<span data-ttu-id="ebc05-109">Modo 2</span><span class="sxs-lookup"><span data-stu-id="ebc05-109">Mode 2</span></span>](#mode-2)
-   [<span data-ttu-id="ebc05-110">Modo 3</span><span class="sxs-lookup"><span data-stu-id="ebc05-110">Mode 3</span></span>](#mode-3)
-   [<span data-ttu-id="ebc05-111">Modo 4</span><span class="sxs-lookup"><span data-stu-id="ebc05-111">Mode 4</span></span>](#mode-4)
-   [<span data-ttu-id="ebc05-112">Modo 5</span><span class="sxs-lookup"><span data-stu-id="ebc05-112">Mode 5</span></span>](#mode-5)
-   [<span data-ttu-id="ebc05-113">Modo 6</span><span class="sxs-lookup"><span data-stu-id="ebc05-113">Mode 6</span></span>](#mode-6)
-   [<span data-ttu-id="ebc05-114">Modo 7</span><span class="sxs-lookup"><span data-stu-id="ebc05-114">Mode 7</span></span>](#mode-7)
-   [<span data-ttu-id="ebc05-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ebc05-115">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="ebc05-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ebc05-116">Related topics</span></span>](#related-topics)

## <a name="mode-0"></a><span data-ttu-id="ebc05-117">Modo 0</span><span class="sxs-lookup"><span data-stu-id="ebc05-117">Mode 0</span></span>

<span data-ttu-id="ebc05-118">O modo 0 do BC7 tem as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="ebc05-118">BC7 Mode 0 has the following characteristics:</span></span>

-   <span data-ttu-id="ebc05-119">Componentes de cor apenas (nenhum alfa)</span><span class="sxs-lookup"><span data-stu-id="ebc05-119">Color components only (no alpha)</span></span>
-   <span data-ttu-id="ebc05-120">3 subconjuntos por bloco</span><span class="sxs-lookup"><span data-stu-id="ebc05-120">3 subsets per block</span></span>
-   <span data-ttu-id="ebc05-121">Pontos de extremidade RGBP 4.4.4.1 com um bit P exclusivo por ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="ebc05-121">RGBP 4.4.4.1 endpoints with a unique P-bit per endpoint</span></span>
-   <span data-ttu-id="ebc05-122">índices de 3 bits</span><span class="sxs-lookup"><span data-stu-id="ebc05-122">3-bit indices</span></span>
-   <span data-ttu-id="ebc05-123">16 partições</span><span class="sxs-lookup"><span data-stu-id="ebc05-123">16 partitions</span></span>

![Layout de bit do modo 0](images/bc7-mode0.png)

## <a name="mode-1"></a><span data-ttu-id="ebc05-125">Modo 1</span><span class="sxs-lookup"><span data-stu-id="ebc05-125">Mode 1</span></span>

<span data-ttu-id="ebc05-126">O modo 1 do BC7 tem as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="ebc05-126">BC7 Mode 1 has the following characteristics:</span></span>

-   <span data-ttu-id="ebc05-127">Componentes de cor apenas (nenhum alfa)</span><span class="sxs-lookup"><span data-stu-id="ebc05-127">Color components only (no alpha)</span></span>
-   <span data-ttu-id="ebc05-128">2 subconjuntos por bloco</span><span class="sxs-lookup"><span data-stu-id="ebc05-128">2 subsets per block</span></span>
-   <span data-ttu-id="ebc05-129">Pontos de extremidade RGBP 6.6.6.1 com um bit P compartilhado por subconjunto)</span><span class="sxs-lookup"><span data-stu-id="ebc05-129">RGBP 6.6.6.1 endpoints with a shared P-bit per subset)</span></span>
-   <span data-ttu-id="ebc05-130">índices de 3 bits</span><span class="sxs-lookup"><span data-stu-id="ebc05-130">3-bit indices</span></span>
-   <span data-ttu-id="ebc05-131">64 partições</span><span class="sxs-lookup"><span data-stu-id="ebc05-131">64 partitions</span></span>

![Layout de bit do modo 1](images/bc7-mode1.png)

## <a name="mode-2"></a><span data-ttu-id="ebc05-133">Modo 2</span><span class="sxs-lookup"><span data-stu-id="ebc05-133">Mode 2</span></span>

<span data-ttu-id="ebc05-134">O modo 2 do BC7 tem as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="ebc05-134">BC7 Mode 2 has the following characteristics:</span></span>

-   <span data-ttu-id="ebc05-135">Componentes de cor apenas (nenhum alfa)</span><span class="sxs-lookup"><span data-stu-id="ebc05-135">Color components only (no alpha)</span></span>
-   <span data-ttu-id="ebc05-136">3 subconjuntos por bloco</span><span class="sxs-lookup"><span data-stu-id="ebc05-136">3 subsets per block</span></span>
-   <span data-ttu-id="ebc05-137">Pontos de extremidade RGB 5.5.5</span><span class="sxs-lookup"><span data-stu-id="ebc05-137">RGB 5.5.5 endpoints</span></span>
-   <span data-ttu-id="ebc05-138">índices de 2 bits</span><span class="sxs-lookup"><span data-stu-id="ebc05-138">2-bit indices</span></span>
-   <span data-ttu-id="ebc05-139">64 partições</span><span class="sxs-lookup"><span data-stu-id="ebc05-139">64 partitions</span></span>

![Layout de bit do modo 2](images/bc7-mode2.png)

## <a name="mode-3"></a><span data-ttu-id="ebc05-141">Modo 3</span><span class="sxs-lookup"><span data-stu-id="ebc05-141">Mode 3</span></span>

<span data-ttu-id="ebc05-142">O modo 3 do BC7 tem as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="ebc05-142">BC7 Mode 3 has the following characteristics:</span></span>

-   <span data-ttu-id="ebc05-143">Componentes de cor apenas (nenhum alfa)</span><span class="sxs-lookup"><span data-stu-id="ebc05-143">Color components only (no alpha)</span></span>
-   <span data-ttu-id="ebc05-144">2 subconjuntos por bloco</span><span class="sxs-lookup"><span data-stu-id="ebc05-144">2 subsets per block</span></span>
-   <span data-ttu-id="ebc05-145">Pontos de extremidade RGBP 7.7.7.1 com um bit P único por subconjunto)</span><span class="sxs-lookup"><span data-stu-id="ebc05-145">RGBP 7.7.7.1 endpoints with a unique P-bit per subset)</span></span>
-   <span data-ttu-id="ebc05-146">índices de 2 bits</span><span class="sxs-lookup"><span data-stu-id="ebc05-146">2-bit indices</span></span>
-   <span data-ttu-id="ebc05-147">64 partições</span><span class="sxs-lookup"><span data-stu-id="ebc05-147">64 partitions</span></span>

![Layout de bit do modo 3](images/bc7-mode3.png)

## <a name="mode-4"></a><span data-ttu-id="ebc05-149">Modo 4</span><span class="sxs-lookup"><span data-stu-id="ebc05-149">Mode 4</span></span>

<span data-ttu-id="ebc05-150">O modo 4 do BC7 tem as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="ebc05-150">BC7 Mode 4 has the following characteristics:</span></span>

-   <span data-ttu-id="ebc05-151">Componentes de cor com o componente alfa separado</span><span class="sxs-lookup"><span data-stu-id="ebc05-151">Color components with separate alpha component</span></span>
-   <span data-ttu-id="ebc05-152">1 subconjunto por bloco</span><span class="sxs-lookup"><span data-stu-id="ebc05-152">1 subset per block</span></span>
-   <span data-ttu-id="ebc05-153">pontos de extremidade de cor RGB 5.5.5</span><span class="sxs-lookup"><span data-stu-id="ebc05-153">RGB 5.5.5 color endpoints</span></span>
-   <span data-ttu-id="ebc05-154">pontos de extremidade alfa 6 bits</span><span class="sxs-lookup"><span data-stu-id="ebc05-154">6-bit alpha endpoints</span></span>
-   <span data-ttu-id="ebc05-155">índices de 16 x 2 bits</span><span class="sxs-lookup"><span data-stu-id="ebc05-155">16 x 2-bit indices</span></span>
-   <span data-ttu-id="ebc05-156">índices de 16 x 3 bits</span><span class="sxs-lookup"><span data-stu-id="ebc05-156">16 x 3-bit indices</span></span>
-   <span data-ttu-id="ebc05-157">rotação de componente de 2 bits</span><span class="sxs-lookup"><span data-stu-id="ebc05-157">2-bit component rotation</span></span>
-   <span data-ttu-id="ebc05-158">seletor de índice de 1 bit (se os índices de 2 ou 3 bits forem usados)</span><span class="sxs-lookup"><span data-stu-id="ebc05-158">1-bit index selector (whether the 2- or 3-bit indices are used)</span></span>

![layout de bit do modo 4](images/bc7-mode4.png)

## <a name="mode-5"></a><span data-ttu-id="ebc05-160">Modo 5</span><span class="sxs-lookup"><span data-stu-id="ebc05-160">Mode 5</span></span>

<span data-ttu-id="ebc05-161">O modo 5 do BC7 tem as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="ebc05-161">BC7 Mode 5 has the following characteristics:</span></span>

-   <span data-ttu-id="ebc05-162">Componentes de cor com o componente alfa separado</span><span class="sxs-lookup"><span data-stu-id="ebc05-162">Color components with separate alpha component</span></span>
-   <span data-ttu-id="ebc05-163">1 subconjunto por bloco</span><span class="sxs-lookup"><span data-stu-id="ebc05-163">1 subset per block</span></span>
-   <span data-ttu-id="ebc05-164">pontos de extremidade de cor RGB 7.7.7</span><span class="sxs-lookup"><span data-stu-id="ebc05-164">RGB 7.7.7 color endpoints</span></span>
-   <span data-ttu-id="ebc05-165">pontos de extremidade alfa de 8 bits</span><span class="sxs-lookup"><span data-stu-id="ebc05-165">8-bit alpha endpoints</span></span>
-   <span data-ttu-id="ebc05-166">índices de cores de 16 x 2 bits</span><span class="sxs-lookup"><span data-stu-id="ebc05-166">16 x 2-bit color indices</span></span>
-   <span data-ttu-id="ebc05-167">índices alfa de 16 x 2 bits</span><span class="sxs-lookup"><span data-stu-id="ebc05-167">16 x 2-bit alpha indices</span></span>
-   <span data-ttu-id="ebc05-168">rotação de componente de 2 bits</span><span class="sxs-lookup"><span data-stu-id="ebc05-168">2-bit component rotation</span></span>

![Layout de bit do modo 5](images/bc7-mode5.png)

## <a name="mode-6"></a><span data-ttu-id="ebc05-170">Modo 6</span><span class="sxs-lookup"><span data-stu-id="ebc05-170">Mode 6</span></span>

<span data-ttu-id="ebc05-171">O modo 6 do BC7 tem as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="ebc05-171">BC7 Mode 6 has the following characteristics:</span></span>

-   <span data-ttu-id="ebc05-172">Componentes de cor e alfa combinados</span><span class="sxs-lookup"><span data-stu-id="ebc05-172">Combined color and alpha components</span></span>
-   <span data-ttu-id="ebc05-173">Um subconjunto por bloco</span><span class="sxs-lookup"><span data-stu-id="ebc05-173">One subset per block</span></span>
-   <span data-ttu-id="ebc05-174">Pontos de extremidade de cor RGBAP 7.7.7.7.1 (e alfa) (bit P exclusivo por ponto de extremidade)</span><span class="sxs-lookup"><span data-stu-id="ebc05-174">RGBAP 7.7.7.7.1 color (and alpha) endpoints (unique P-bit per endpoint)</span></span>
-   <span data-ttu-id="ebc05-175">índices de 16 x 4 bits</span><span class="sxs-lookup"><span data-stu-id="ebc05-175">16 x 4-bit indices</span></span>

![layout de bit do modo 6](images/bc7-mode6.png)

## <a name="mode-7"></a><span data-ttu-id="ebc05-177">Modo 7</span><span class="sxs-lookup"><span data-stu-id="ebc05-177">Mode 7</span></span>

<span data-ttu-id="ebc05-178">O modo 7 do BC7 tem as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="ebc05-178">BC7 Mode 7 has the following characteristics:</span></span>

-   <span data-ttu-id="ebc05-179">Componentes de cor e alfa combinados</span><span class="sxs-lookup"><span data-stu-id="ebc05-179">Combined color and alpha components</span></span>
-   <span data-ttu-id="ebc05-180">2 subconjuntos por bloco</span><span class="sxs-lookup"><span data-stu-id="ebc05-180">2 subsets per block</span></span>
-   <span data-ttu-id="ebc05-181">Pontos de extremidade de cor RGBAP 5.5.5.5.1 (e alfa) (bit P exclusivo por ponto de extremidade)</span><span class="sxs-lookup"><span data-stu-id="ebc05-181">RGBAP 5.5.5.5.1 color (and alpha) endpoints (unique P-bit per endpoint)</span></span>
-   <span data-ttu-id="ebc05-182">índices de 2 bits</span><span class="sxs-lookup"><span data-stu-id="ebc05-182">2-bit indices</span></span>
-   <span data-ttu-id="ebc05-183">64 partições</span><span class="sxs-lookup"><span data-stu-id="ebc05-183">64 partitions</span></span>

![layout de bit do modo 7](images/bc7-mode7.png)

## <a name="remarks"></a><span data-ttu-id="ebc05-185">Comentários</span><span class="sxs-lookup"><span data-stu-id="ebc05-185">Remarks</span></span>

<span data-ttu-id="ebc05-186">O modo 8 (o byte menos significativo está definido como 0x00) é reservado.</span><span class="sxs-lookup"><span data-stu-id="ebc05-186">Mode 8 (the least significant byte is set to 0x00) is reserved.</span></span> <span data-ttu-id="ebc05-187">Não use-o em seu codificador.</span><span class="sxs-lookup"><span data-stu-id="ebc05-187">Don't use it in your encoder.</span></span> <span data-ttu-id="ebc05-188">Se você passar esse modo para o hardware, será retornado um bloco inicializado para todos os zeros.</span><span class="sxs-lookup"><span data-stu-id="ebc05-188">If you pass this mode to the hardware, a block initialized to all zeroes is returned.</span></span>

<span data-ttu-id="ebc05-189">No BC7, você pode codificar o componente alfa de uma das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="ebc05-189">In BC7, you can encode the alpha component in one of the following ways:</span></span>

-   <span data-ttu-id="ebc05-190">Tipos de bloco sem codificação explícita de componente alfa.</span><span class="sxs-lookup"><span data-stu-id="ebc05-190">Block types without explicit alpha component encoding.</span></span> <span data-ttu-id="ebc05-191">Nesses blocos, os pontos de extremidade de cor têm uma codificação somente RGB, com o componente alfa decodificado em 1.0 para todos os texels.</span><span class="sxs-lookup"><span data-stu-id="ebc05-191">In these blocks, the color endpoints have an RGB-only encoding, with the alpha component decoded to 1.0 for all texels.</span></span>
-   <span data-ttu-id="ebc05-192">Os tipos de bloco com componentes de cor e alfa combinados.</span><span class="sxs-lookup"><span data-stu-id="ebc05-192">Block types with combined color and alpha components.</span></span> <span data-ttu-id="ebc05-193">Nesses blocos, os valores de cor de ponto de extremidade são especificados no formato RGBA, e os valores de componente alfa são interpolados juntamente com os valores de cor.</span><span class="sxs-lookup"><span data-stu-id="ebc05-193">In these blocks, the endpoint color values are specified in the RGBA format, and the alpha component values are interpolated along with the color values.</span></span>
-   <span data-ttu-id="ebc05-194">Os tipos de bloco com componentes de cor e alfa separados.</span><span class="sxs-lookup"><span data-stu-id="ebc05-194">Block types with separated color and alpha components.</span></span> <span data-ttu-id="ebc05-195">Nesses blocos, os valores de cor e alfa são especificados separadamente, cada um com seu próprio conjunto de índices.</span><span class="sxs-lookup"><span data-stu-id="ebc05-195">In these blocks the color and alpha values are specified separately, each with their own set of indices.</span></span> <span data-ttu-id="ebc05-196">Como resultado, eles têm um vetor efetivo e um canal escalar com codificação separada, em que o vetor normalmente especifica os canais de cor \[ R, G, B \] e escalar especifica o canal alfa \[ a \] .</span><span class="sxs-lookup"><span data-stu-id="ebc05-196">As a result, they have an effective vector and a scalar channel separately encoded, where the vector commonly specifies the color channels \[R, G, B\] and the scalar specifies the alpha channel \[A\].</span></span> <span data-ttu-id="ebc05-197">Para dar suporte a essa abordagem, um campo de 2 bits separado é fornecido na codificação, que permite a especificação da codificação de canal separado como um valor escalar.</span><span class="sxs-lookup"><span data-stu-id="ebc05-197">To support this approach, a separate 2-bit field is provided in the encoding, which permits the specification of the separate channel encoding as a scalar value.</span></span> <span data-ttu-id="ebc05-198">Como resultado, o bloco pode ter uma das quatro representações diferentes a seguir dessa codificação alfa (conforme indicado pelo campo de 2 bits):</span><span class="sxs-lookup"><span data-stu-id="ebc05-198">As a result, the block can have one of the following four different representations of this alpha encoding (as indicated by the 2-bit field):</span></span>
    -   <span data-ttu-id="ebc05-199">RGB \| A: canal alfa separado</span><span class="sxs-lookup"><span data-stu-id="ebc05-199">RGB\|A: alpha channel separate</span></span>
    -   <span data-ttu-id="ebc05-200">AGB \| R: canal de cores "vermelho" separado</span><span class="sxs-lookup"><span data-stu-id="ebc05-200">AGB\|R: "red" color channel separate</span></span>
    -   <span data-ttu-id="ebc05-201">RAB \| G: canal de cores "verde" separado</span><span class="sxs-lookup"><span data-stu-id="ebc05-201">RAB\|G: "green" color channel separate</span></span>
    -   <span data-ttu-id="ebc05-202">RGA \| B: canal de cores "azul" separado</span><span class="sxs-lookup"><span data-stu-id="ebc05-202">RGA\|B: "blue" color channel separate</span></span>

    <span data-ttu-id="ebc05-203">O decodificador reordena a ordem de canal para RGBA após a decodificação, portanto, o formato de bloco interno é invisível para o desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="ebc05-203">The decoder reorders the channel order back to RGBA after decoding, so the internal block format is invisible to the developer.</span></span> <span data-ttu-id="ebc05-204">Tons de preto com cor separada e componentes alfa também têm dois conjuntos de dados de índice: um para o conjunto em vetor de canais e outro para o canal escalar.</span><span class="sxs-lookup"><span data-stu-id="ebc05-204">Blacks with separate color and alpha components also have two sets of index data: one for the vectored set of channels, and one for the scalar channel.</span></span> <span data-ttu-id="ebc05-205">(No caso do modo 4, esses índices têm larguras diferentes de \[ 2 ou 3 bits \] .</span><span class="sxs-lookup"><span data-stu-id="ebc05-205">(In the case of Mode 4, these indices are of differing widths \[2 or 3 bits\].</span></span> <span data-ttu-id="ebc05-206">O modo 4 também contém um seletor de 1 bit que especifica se o vetor ou o canal escalar usa os índices de 3 bits.)</span><span class="sxs-lookup"><span data-stu-id="ebc05-206">Mode 4 also contains a 1-bit selector that specifies whether the vector or the scalar channel uses the 3-bit indices.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="ebc05-207">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ebc05-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebc05-208">Formato BC7</span><span class="sxs-lookup"><span data-stu-id="ebc05-208">BC7 Format</span></span>](bc7-format.md)
</dt> </dl>

 

 




