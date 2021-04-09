---
description: Este tópico descreve os formatos YUV de 10 e 16 bits que são recomendados para capturar, processar e exibir vídeo no sistema operacional Microsoft Windows.
ms.assetid: fcaaaa6f-f886-4f6e-9c3c-e513ccc90d37
title: Formatos de vídeo YUV de 10 e 16 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bbc357653848cd51ce6f56ebd8a1da3e5f60403
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090576"
---
# <a name="10-bit-and-16-bit-yuv-video-formats"></a><span data-ttu-id="c4bbe-103">Formatos de vídeo YUV de 10 e 16 bits</span><span class="sxs-lookup"><span data-stu-id="c4bbe-103">10-bit and 16-bit YUV Video Formats</span></span>

<span data-ttu-id="c4bbe-104">Este tópico descreve os formatos YUV de 10 e 16 bits que são recomendados para capturar, processar e exibir vídeo no sistema operacional Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-104">This topic describes the 10- and 16-bit YUV formats that are recommended for capturing, processing, and displaying video in the Microsoft Windows operating system.</span></span>

<span data-ttu-id="c4bbe-105">Este tópico contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="c4bbe-105">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="c4bbe-106">Visão geral</span><span class="sxs-lookup"><span data-stu-id="c4bbe-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="c4bbe-107">Códigos FOURCC para YUV de 10 e 16 bits</span><span class="sxs-lookup"><span data-stu-id="c4bbe-107">FOURCC Codes For 10-Bit and 16-Bit YUV</span></span>](#fourcc-codes-for-10-bit-and-16-bit-yuv)
-   [<span data-ttu-id="c4bbe-108">Definições de superfície</span><span class="sxs-lookup"><span data-stu-id="c4bbe-108">Surface Definitions</span></span>](#surface-definitions)
    -   [<span data-ttu-id="c4bbe-109">4:2:0 formatos</span><span class="sxs-lookup"><span data-stu-id="c4bbe-109">4:2:0 Formats</span></span>](#420-formats)
    -   [<span data-ttu-id="c4bbe-110">4:2:2 formatos</span><span class="sxs-lookup"><span data-stu-id="c4bbe-110">4:2:2 Formats</span></span>](#422-formats)
    -   [<span data-ttu-id="c4bbe-111">4:4:4 formatos</span><span class="sxs-lookup"><span data-stu-id="c4bbe-111">4:4:4 Formats</span></span>](#444-formats)
-   [<span data-ttu-id="c4bbe-112">Formatos YUV preferenciais</span><span class="sxs-lookup"><span data-stu-id="c4bbe-112">Preferred YUV Formats</span></span>](#preferred-yuv-formats)
-   [<span data-ttu-id="c4bbe-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c4bbe-113">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="c4bbe-114">Visão geral</span><span class="sxs-lookup"><span data-stu-id="c4bbe-114">Overview</span></span>

<span data-ttu-id="c4bbe-115">Esses formatos usam uma representação de ponto fixo para os canais Luma Channel e croma (C'b e C'r).</span><span class="sxs-lookup"><span data-stu-id="c4bbe-115">These formats use a fixed-point representation for both the luma channel and the chroma (C'b and C'r) channels.</span></span> <span data-ttu-id="c4bbe-116">Os valores de exemplo são dimensionados em valores de 8 bits, usando um fator de dimensionamento de 2 ^ (n − 8), em que n é 10 ou 16, de acordo com as seções 7.7-7.8 e 7.11-7.12 de SMPTE 274M.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-116">Sample values are scaled 8-bit values, using a scaling factor of 2^(n − 8), where n is either 10 or 16, as per sections 7.7-7.8 and 7.11-7.12 of SMPTE 274M.</span></span> <span data-ttu-id="c4bbe-117">Conversões de precisão podem ser executadas usando turnos de bits simples.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-117">Precision conversions can be performed using simple bit shifts.</span></span> <span data-ttu-id="c4bbe-118">Por exemplo, se o ponto branco de um formato de 8 bits for 235, o formato de 10 bits correspondente terá um ponto branco em 940 (235 × 4).</span><span class="sxs-lookup"><span data-stu-id="c4bbe-118">For example, if the white point of an 8-bit format is 235, the corresponding 10-bit format has a white point at 940 (235 × 4).</span></span>

<span data-ttu-id="c4bbe-119">As representações de 16 bits descritas aqui usam valores de **palavra** little-endian para cada canal.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-119">The 16-bit representations described here use little-endian **WORD** values for each channel.</span></span> <span data-ttu-id="c4bbe-120">Os formatos de 10 bits também usam 16 bits para cada canal, com os 6 bits mais baixos definidos como zero, conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-120">The 10-bit formats also use 16 bits for each channel, with the lowest 6 bits set to zero, as shown in the following diagram.</span></span>

![diagrama mostrando a representação de 10 bits](images/ee3aae23-4f0a-47d0-a46c-f3d7d94205e6.gif)

<span data-ttu-id="c4bbe-122">Como as representações de 10 e 16 bits do mesmo formato YUV têm o mesmo layout de memória, é possível converter uma representação de 10 bits em uma representação 16 sem perda de precisão.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-122">Because the 10-bit and 16-bit representations of the same YUV format have the same memory layout, it is possible to cast a 10-bit representation to a 16-representation with no loss of precision.</span></span> <span data-ttu-id="c4bbe-123">Também é possível converter uma representação de 16 bits em uma representação de 10 bits.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-123">It is also possible to cast a 16-bit representation down to a 10-bit representation.</span></span> <span data-ttu-id="c4bbe-124">(Os formatos Y416 e Y410 são uma exceção a essa regra geral, no entanto, porque eles não compartilham o mesmo layout de memória.)</span><span class="sxs-lookup"><span data-stu-id="c4bbe-124">(The Y416 and Y410 formats are an exception to this general rule, however, because they do not share the same memory layout.)</span></span>

<span data-ttu-id="c4bbe-125">Quando o hardware de gráficos lê uma superfície que contém uma representação de 10 bits, ele deve ignorar os 6 bits de ordem inferior de cada canal.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-125">When the graphics hardware reads a surface that contains a 10-bit representation, it should ignore the low-order 6 bits of each channel.</span></span> <span data-ttu-id="c4bbe-126">No entanto, se uma superfície contiver dados de 16 bits válidos, ela deverá ser identificada como uma superfície de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-126">If a surface contains valid 16-bit data, however, it should be identified as a 16-bit surface.</span></span>

<span data-ttu-id="c4bbe-127">Nos formatos que contêm alfa, um pixel completamente transparente tem um valor alfa de zero e um pixel completamente opaco tem um valor alfa de (2 ^ n) – 1, em que n é o número de bits alfa.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-127">In the formats that contain alpha, a completely transparent pixel has an alpha value of zero, and a completely opaque pixel has an alpha value of (2^n) – 1, where n is the number of alpha bits.</span></span> <span data-ttu-id="c4bbe-128">Alfa é considerado um valor linear que é aplicado a cada componente depois que o componente é convertido em seu formato linear normalizado.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-128">Alpha is assumed to be a linear value that is applied to each component after the component has been converted into its normalized linear form.</span></span>

<span data-ttu-id="c4bbe-129">Para imagens na memória de vídeo, o driver de gráficos seleciona o alinhamento de memória da superfície.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-129">For images in video memory, the graphics driver selects the memory alignment of the surface.</span></span> <span data-ttu-id="c4bbe-130">A superfície deve ser alinhada em **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="c4bbe-130">The surface must be **DWORD** aligned.</span></span> <span data-ttu-id="c4bbe-131">Ou seja, as linhas individuais dentro de uma superfície têm garantia de começar em um limite de 32 bits, embora o alinhamento possa ser maior que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-131">That is, individual lines within a surface are guaranteed to start at a 32-bit boundary, although the alignment can be larger than 32 bits.</span></span> <span data-ttu-id="c4bbe-132">A origem (0, 0) é sempre o canto superior esquerdo da superfície.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-132">The origin (0,0) is always the upper-left corner of the surface.</span></span>

<span data-ttu-id="c4bbe-133">Para os fins desta documentação, o termo *U* é equivalente a *CB* e o termo *V* é equivalente a *CR*.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-133">For the purposes of this documentation, the term *U* is equivalent to *Cb*, and the term *V* is equivalent to *Cr*.</span></span>

## <a name="fourcc-codes-for-10-bit-and-16-bit-yuv"></a><span data-ttu-id="c4bbe-134">Códigos FOURCC para YUV de 10 e 16 bits</span><span class="sxs-lookup"><span data-stu-id="c4bbe-134">FOURCC Codes For 10-Bit and 16-Bit YUV</span></span>

<span data-ttu-id="c4bbe-135">Os códigos FOURCC para os formatos descritos aqui usam a seguinte convenção:</span><span class="sxs-lookup"><span data-stu-id="c4bbe-135">The FOURCC codes for the formats described here use the following convention:</span></span>

-   <span data-ttu-id="c4bbe-136">Se o formato for planar, o primeiro caractere no código FOURCC será ' P '.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-136">If the format is planar, the first character in the FOURCC code is 'P'.</span></span> <span data-ttu-id="c4bbe-137">Se o formato for empacotado, o primeiro caractere será ' Y '.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-137">If the format is packed, the first character is 'Y'.</span></span>
-   <span data-ttu-id="c4bbe-138">O segundo caractere no código FOURCC é determinado pela amostragem de croma, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-138">The second character in the FOURCC code is determined by the chroma sampling, as shown in the following table.</span></span>

    

    | <span data-ttu-id="c4bbe-139">Amostragem de croma</span><span class="sxs-lookup"><span data-stu-id="c4bbe-139">Chroma sampling</span></span> | <span data-ttu-id="c4bbe-140">Letra de código FOURCC</span><span class="sxs-lookup"><span data-stu-id="c4bbe-140">FOURCC code letter</span></span> |
    |-----------------|--------------------|
    | <span data-ttu-id="c4bbe-141">4:4:4</span><span class="sxs-lookup"><span data-stu-id="c4bbe-141">4:4:4</span></span>           | <span data-ttu-id="c4bbe-142">quatro</span><span class="sxs-lookup"><span data-stu-id="c4bbe-142">'4'</span></span>                |
    | <span data-ttu-id="c4bbe-143">4:2:2</span><span class="sxs-lookup"><span data-stu-id="c4bbe-143">4:2:2</span></span>           | <span data-ttu-id="c4bbe-144">2</span><span class="sxs-lookup"><span data-stu-id="c4bbe-144">'2'</span></span>                |
    | <span data-ttu-id="c4bbe-145">4:2:1</span><span class="sxs-lookup"><span data-stu-id="c4bbe-145">4:2:1</span></span>           | <span data-ttu-id="c4bbe-146">'1'</span><span class="sxs-lookup"><span data-stu-id="c4bbe-146">'1'</span></span>                |
    | <span data-ttu-id="c4bbe-147">4:2:0</span><span class="sxs-lookup"><span data-stu-id="c4bbe-147">4:2:0</span></span>           | <span data-ttu-id="c4bbe-148">'0'</span><span class="sxs-lookup"><span data-stu-id="c4bbe-148">'0'</span></span>                |

    

     

-   <span data-ttu-id="c4bbe-149">Os dois últimos caracteres no FOURCC indicam o número de bits por canal, um ' 16 ' para 16 bits ou ' 10 ' para 10 bits.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-149">The final two characters in the FOURCC indicate the number of bits per channel, either '16' for 16 bits or '10' for 10 bits.</span></span>

<span data-ttu-id="c4bbe-150">Usando esse esquema, os códigos FOURCC a seguir foram definidos.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-150">Using this scheme, the following FOURCC codes have been defined.</span></span> <span data-ttu-id="c4bbe-151">Nenhum formato 4:2:1 para YUV de 10 ou 16 bits foi definido neste momento.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-151">No 4:2:1 formats for 10-bit or 16-bit YUV have been defined at this time.</span></span>



| <span data-ttu-id="c4bbe-152">FOURCC</span><span class="sxs-lookup"><span data-stu-id="c4bbe-152">FOURCC</span></span> | <span data-ttu-id="c4bbe-153">Descrição</span><span class="sxs-lookup"><span data-stu-id="c4bbe-153">Description</span></span>            |
|--------|------------------------|
| <span data-ttu-id="c4bbe-154">P016</span><span class="sxs-lookup"><span data-stu-id="c4bbe-154">P016</span></span>   | <span data-ttu-id="c4bbe-155">Planar, 4:2:0, 16 bits.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-155">Planar, 4:2:0, 16-bit.</span></span> |
| <span data-ttu-id="c4bbe-156">P010</span><span class="sxs-lookup"><span data-stu-id="c4bbe-156">P010</span></span>   | <span data-ttu-id="c4bbe-157">Planar, 4:2:0, 10 bits.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-157">Planar, 4:2:0, 10-bit.</span></span> |
| <span data-ttu-id="c4bbe-158">P216</span><span class="sxs-lookup"><span data-stu-id="c4bbe-158">P216</span></span>   | <span data-ttu-id="c4bbe-159">Planar, 4:2:2, 16 bits.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-159">Planar, 4:2:2, 16-bit.</span></span> |
| <span data-ttu-id="c4bbe-160">P210</span><span class="sxs-lookup"><span data-stu-id="c4bbe-160">P210</span></span>   | <span data-ttu-id="c4bbe-161">Planar, 4:2:2, 10 bits.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-161">Planar, 4:2:2, 10-bit.</span></span> |
| <span data-ttu-id="c4bbe-162">Y216</span><span class="sxs-lookup"><span data-stu-id="c4bbe-162">Y216</span></span>   | <span data-ttu-id="c4bbe-163">Embalado, 4:2:2, 16 bits.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-163">Packed, 4:2:2, 16-bit.</span></span> |
| <span data-ttu-id="c4bbe-164">Y210</span><span class="sxs-lookup"><span data-stu-id="c4bbe-164">Y210</span></span>   | <span data-ttu-id="c4bbe-165">Embalado, 4:2:2, 10 bits.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-165">Packed, 4:2:2, 10-bit.</span></span> |
| <span data-ttu-id="c4bbe-166">Y416</span><span class="sxs-lookup"><span data-stu-id="c4bbe-166">Y416</span></span>   | <span data-ttu-id="c4bbe-167">Embalado, 4:4:4, 16 bits</span><span class="sxs-lookup"><span data-stu-id="c4bbe-167">Packed, 4:4:4, 16-bit</span></span>  |
| <span data-ttu-id="c4bbe-168">Y410</span><span class="sxs-lookup"><span data-stu-id="c4bbe-168">Y410</span></span>   | <span data-ttu-id="c4bbe-169">Embalado, 4:4:4, 10 bits.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-169">Packed, 4:4:4, 10-bit.</span></span> |



 

<span data-ttu-id="c4bbe-170">Os GUIDs de subtipo também foram definidos a partir destes FOURCC; consulte [GUIDs de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="c4bbe-170">Subtype GUIDs have also been defined from these FOURCCs; see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="surface-definitions"></a><span data-ttu-id="c4bbe-171">Definições de superfície</span><span class="sxs-lookup"><span data-stu-id="c4bbe-171">Surface Definitions</span></span>

<span data-ttu-id="c4bbe-172">Esta seção descreve o layout de memória de cada formato.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-172">This section describes the memory layout of each format.</span></span> <span data-ttu-id="c4bbe-173">Nas descrições a seguir, o termo **Word** refere-se a um valor de 16 bits little-endian e o termo **DWORD** refere-se a um valor de 32 bits little-endian.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-173">In the descriptions that follow, the term **WORD** refers to a little-endian 16-bit value, and the term **DWORD** refers to a little-endian 32-bit value.</span></span>

### <a name="420-formats"></a><span data-ttu-id="c4bbe-174">4:2:0 formatos</span><span class="sxs-lookup"><span data-stu-id="c4bbe-174">4:2:0 Formats</span></span>

<span data-ttu-id="c4bbe-175">Dois formatos 4:2:0 são definidos, com os códigos FOURCC P016 e P010.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-175">Two 4:2:0 formats are defined, with the FOURCC codes P016 and P010.</span></span> <span data-ttu-id="c4bbe-176">Eles compartilham o mesmo layout de memória, mas o P016 usa 16 bits por canal e o P010 usa 10 bits por canal.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-176">They share the same memory layout, but P016 uses 16 bits per channel and P010 uses 10 bits per channel.</span></span>

### <a name="p016-and-p010"></a><span data-ttu-id="c4bbe-177">P016 e P010</span><span class="sxs-lookup"><span data-stu-id="c4bbe-177">P016 and P010</span></span>

<span data-ttu-id="c4bbe-178">Nesses dois formatos, todas as amostras Y aparecem primeiro na memória como uma matriz da **palavra** s com um número par de linhas.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-178">In these two formats, all Y samples appear first in memory as an array of **WORD** s with an even number of lines.</span></span> <span data-ttu-id="c4bbe-179">A distância da superfície pode ser maior que a largura do plano Y.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-179">The surface stride can be larger than the width of the Y plane.</span></span> <span data-ttu-id="c4bbe-180">Essa matriz é seguida imediatamente por uma matriz de **palavras** que contém exemplos intercalados de você e V, conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-180">This array is followed immediately by an array of **WORD** s that contains interleaved U and V samples, as shown in the following diagram.</span></span>

![diagrama mostrando P016 e layout de pixel P010](images/1e1c4d66-6172-4d3a-bd25-4b5caa67edcd.gif)

<span data-ttu-id="c4bbe-182">Se a matriz de U-V combinada for endereçada como uma matriz de **DWORD** s, a palavra menos significativa (LSW) conterá o valor U e a palavra mais significativa (MSW) conterá o valor V.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-182">If the combined U-V array is addressed as an array of **DWORD** s, the least significant word (LSW) contains the U value and the most significant word (MSW) contains the V value.</span></span> <span data-ttu-id="c4bbe-183">O stride do plano U-V combinado é igual ao Stride do plano Y.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-183">The stride of the combined U-V plane is equal to the stride of the Y plane.</span></span> <span data-ttu-id="c4bbe-184">O plano U-V tem metade da quantidade de linhas que o plano Y.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-184">The U-V plane has half as many lines as the Y plane.</span></span>

<span data-ttu-id="c4bbe-185">Esses dois formatos são os formatos de pixel do planar 4:2:0 preferenciais para representações de maior precisão.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-185">These two formats are the preferred 4:2:0 planar pixel formats for higher precision YUV representations.</span></span> <span data-ttu-id="c4bbe-186">Espera-se que sejam um requisito de termo intermediário para aceleradores de DXVA (DirectX Video Acceleration) que dão suporte a vídeo 4:2:0 de 10 ou 16 bits.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-186">They are expected to be an intermediate-term requirement for DirectX Video Acceleration (DXVA) accelerators that support 10-bit or 16-bit 4:2:0 video.</span></span>

### <a name="422-formats"></a><span data-ttu-id="c4bbe-187">4:2:2 formatos</span><span class="sxs-lookup"><span data-stu-id="c4bbe-187">4:2:2 Formats</span></span>

<span data-ttu-id="c4bbe-188">São definidos quatro formatos 4:2:2, dois planar e dois compactados.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-188">Four 4:2:2 formats are defined, two planar and two packed.</span></span> <span data-ttu-id="c4bbe-189">Eles têm os seguintes códigos FOURCC:</span><span class="sxs-lookup"><span data-stu-id="c4bbe-189">They have the following FOURCC codes:</span></span>

-   <span data-ttu-id="c4bbe-190">P216</span><span class="sxs-lookup"><span data-stu-id="c4bbe-190">P216</span></span>
-   <span data-ttu-id="c4bbe-191">P210</span><span class="sxs-lookup"><span data-stu-id="c4bbe-191">P210</span></span>
-   <span data-ttu-id="c4bbe-192">Y216</span><span class="sxs-lookup"><span data-stu-id="c4bbe-192">Y216</span></span>
-   <span data-ttu-id="c4bbe-193">Y210</span><span class="sxs-lookup"><span data-stu-id="c4bbe-193">Y210</span></span>

### <a name="p216-and-p210"></a><span data-ttu-id="c4bbe-194">P216 e P210</span><span class="sxs-lookup"><span data-stu-id="c4bbe-194">P216 and P210</span></span>

<span data-ttu-id="c4bbe-195">Nesses dois formatos planar, todas as amostras Y aparecem primeiro na memória como uma matriz da **palavra** s com um número par de linhas.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-195">In these two planar formats, all Y samples appear first in memory as an array of **WORD** s with an even number of lines.</span></span> <span data-ttu-id="c4bbe-196">A distância da superfície pode ser maior que a largura do plano Y.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-196">The surface stride can be larger than the width of the Y plane.</span></span> <span data-ttu-id="c4bbe-197">Essa matriz é seguida imediatamente por uma matriz de **palavras** que contém exemplos intercalados de você e V, conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-197">This array is followed immediately by an array of **WORD** s that contains interleaved U and V samples, as shown in the following diagram.</span></span>

![diagrama mostrando P216 e layout de pixel P210](images/ff672fef-218f-4722-b806-d06c77fe8cfa.gif)

<span data-ttu-id="c4bbe-199">Se a matriz de U-V combinada for endereçada como uma matriz de **DWORD** s, o LSW conterá o valor U e o MSW conterá o valor V.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-199">If the combined U-V array is addressed as an array of **DWORD** s, the LSW contains the U value and the MSW contains the V value.</span></span> <span data-ttu-id="c4bbe-200">O stride do plano U-V combinado é igual ao Stride do plano Y.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-200">The stride of the combined U-V plane is equal to the stride of the Y plane.</span></span> <span data-ttu-id="c4bbe-201">O plano U-V tem o mesmo número de linhas que o plano Y.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-201">The U-V plane has the same number of lines as the Y plane.</span></span>

<span data-ttu-id="c4bbe-202">Esses dois formatos são os formatos de pixel do planar 4:2:2 preferenciais para representações de maior precisão.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-202">These two formats are the preferred 4:2:2 planar pixel formats for higher precision YUV representations.</span></span> <span data-ttu-id="c4bbe-203">Espera-se que sejam um requisito de termo intermediário para aceleradores de DXVA (DirectX Video Acceleration) que dão suporte a vídeo 4:2:2 de 10 ou 16 bits.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-203">They are expected to be an intermediate-term requirement for DirectX Video Acceleration (DXVA) accelerators that support 10-bit or 16-bit 4:2:2 video.</span></span>

### <a name="y216-and-y210"></a><span data-ttu-id="c4bbe-204">Y216 e Y210</span><span class="sxs-lookup"><span data-stu-id="c4bbe-204">Y216 and Y210</span></span>

<span data-ttu-id="c4bbe-205">Nesses dois formatos compactados, cada par de pixels é armazenado como uma matriz de quatro **palavras** s, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-205">In these two packed formats, each pair of pixels is stored as an array of four **WORD** s, as shown in the following illustration.</span></span>

![diagrama mostrando o layout de pixel y216 e y210.](images/6f68aeeb-18ca-48ee-82c4-5b79d5510e9f.gif)

<span data-ttu-id="c4bbe-207">A primeira **palavra** na matriz contém a primeira amostra y do par, a segunda **palavra** contém a amostra U, a terceira **palavra** contém a segunda amostra y e a quarta **palavra** contém a amostra V.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-207">The first **WORD** in the array contains the first Y sample in the pair, the second **WORD** contains the U sample, the third **WORD** contains the second Y sample, and the fourth **WORD** contains the V sample.</span></span>

<span data-ttu-id="c4bbe-208">Y210 é idêntico a Y216, exceto que cada amostra contém apenas 10 bits de dados significativos.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-208">Y210 is identical to Y216 except that each sample contains only 10 bits of significant data.</span></span> <span data-ttu-id="c4bbe-209">Os 6 bits menos significativos são definidos como zero, conforme descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-209">The least significant 6 bits are set to zero, as described previously.</span></span>

### <a name="444-formats"></a><span data-ttu-id="c4bbe-210">4:4:4 formatos</span><span class="sxs-lookup"><span data-stu-id="c4bbe-210">4:4:4 Formats</span></span>

<span data-ttu-id="c4bbe-211">Dois formatos 4:4:4 são definidos, com os códigos FOURCC Y410 e Y416.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-211">Two 4:4:4 formats are defined, with the FOURCC codes Y410 and Y416.</span></span> <span data-ttu-id="c4bbe-212">Ambos são formatos empacotados.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-212">Both are packed formats.</span></span>

### <a name="y410"></a><span data-ttu-id="c4bbe-213">Y410</span><span class="sxs-lookup"><span data-stu-id="c4bbe-213">Y410</span></span>

<span data-ttu-id="c4bbe-214">Esse formato é uma representação empacotada de 10 bits que inclui 2 bits de alfa.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-214">This format is a packed 10-bit representation that includes 2 bits of alpha.</span></span> <span data-ttu-id="c4bbe-215">Cada pixel é codificado como uma única **DWORD** com o layout de memória mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-215">Each pixel is encoded as a single **DWORD** with the memory layout shown in the following diagram.</span></span>

![diagrama mostrando o layout de pixel Y410.](images/f8a71437-e3f1-4331-be30-f766c028d648.gif)

<span data-ttu-id="c4bbe-217">Os bits 0-9 contêm a amostra U, o bits 10-19 contém o exemplo Y, os bits 20-29 contêm a amostra V e os bits 30-31 contêm o valor alfa.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-217">Bits 0-9 contain the U sample, bits 10-19 contain the Y sample, bits 20-29 contain the V sample, and bits 30-31 contain the alpha value.</span></span> <span data-ttu-id="c4bbe-218">Para indicar que um pixel é totalmente opaco, um aplicativo deve definir os dois bits alfa iguais a 0x03.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-218">To indicate that a pixel is fully opaque, an application must set the two alpha bits equal to 0x03.</span></span>

### <a name="y416"></a><span data-ttu-id="c4bbe-219">Y416</span><span class="sxs-lookup"><span data-stu-id="c4bbe-219">Y416</span></span>

<span data-ttu-id="c4bbe-220">Esse formato é uma representação de 16 bits empacotada que inclui 16 bits de alfa.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-220">This format is a packed 16-bit representation that includes 16 bits of alpha.</span></span> <span data-ttu-id="c4bbe-221">Cada pixel é codificado como um par de **DWORD** s, como mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-221">Each pixel is encoded as a pair of **DWORD** s, as shown in the following illustration.</span></span>

![diagrama mostrando o layout de pixel y416.](images/c928523a-25d3-4712-9aec-5b492b51435f.gif)

<span data-ttu-id="c4bbe-223">Os bits 0-15 contêm a amostra U, o bits 16-31 contém o exemplo Y, os bits 32-47 contêm a amostra V e os bits 48-63 contêm o valor alfa.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-223">Bits 0-15 contain the U sample, bits 16-31 contain the Y sample, bits 32-47 contain the V sample, and bits 48-63 contain the alpha value.</span></span>

<span data-ttu-id="c4bbe-224">Para indicar que um pixel é totalmente opaco, um aplicativo deve definir os dois bits alfa iguais a 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-224">To indicate that a pixel is fully opaque, an application must set the two alpha bits equal to 0xFFFF.</span></span> <span data-ttu-id="c4bbe-225">Esse formato destina-se principalmente a um formato intermediário durante o processamento da imagem para evitar o acúmulo de erros.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-225">This format is intended primarily as an intermediate format during image processing to avoid the accumulation of errors.</span></span>

## <a name="preferred-yuv-formats"></a><span data-ttu-id="c4bbe-226">Formatos YUV preferenciais</span><span class="sxs-lookup"><span data-stu-id="c4bbe-226">Preferred YUV Formats</span></span>

<span data-ttu-id="c4bbe-227">A tabela a seguir lista os formatos YUV preferenciais, incluindo formatos de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-227">The following table lists the preferred YUV formats, including 8-bit formats.</span></span>



| <span data-ttu-id="c4bbe-228">Formatar</span><span class="sxs-lookup"><span data-stu-id="c4bbe-228">Format</span></span> | <span data-ttu-id="c4bbe-229">Amostragem de croma</span><span class="sxs-lookup"><span data-stu-id="c4bbe-229">Chroma sampling</span></span> | <span data-ttu-id="c4bbe-230">Embalado ou planar</span><span class="sxs-lookup"><span data-stu-id="c4bbe-230">Packed or planar</span></span> | <span data-ttu-id="c4bbe-231">Bits por canal</span><span class="sxs-lookup"><span data-stu-id="c4bbe-231">Bits per channel</span></span> |
|--------|-----------------|------------------|------------------|
| <span data-ttu-id="c4bbe-232">AYUV</span><span class="sxs-lookup"><span data-stu-id="c4bbe-232">AYUV</span></span>   | <span data-ttu-id="c4bbe-233">4:4:4</span><span class="sxs-lookup"><span data-stu-id="c4bbe-233">4:4:4</span></span>           | <span data-ttu-id="c4bbe-234">Colocado</span><span class="sxs-lookup"><span data-stu-id="c4bbe-234">Packed</span></span>           | <span data-ttu-id="c4bbe-235">8</span><span class="sxs-lookup"><span data-stu-id="c4bbe-235">8</span></span>                |
| <span data-ttu-id="c4bbe-236">Y410</span><span class="sxs-lookup"><span data-stu-id="c4bbe-236">Y410</span></span>   | <span data-ttu-id="c4bbe-237">4:4:4</span><span class="sxs-lookup"><span data-stu-id="c4bbe-237">4:4:4</span></span>           | <span data-ttu-id="c4bbe-238">Colocado</span><span class="sxs-lookup"><span data-stu-id="c4bbe-238">Packed</span></span>           | <span data-ttu-id="c4bbe-239">10</span><span class="sxs-lookup"><span data-stu-id="c4bbe-239">10</span></span>               |
| <span data-ttu-id="c4bbe-240">Y416</span><span class="sxs-lookup"><span data-stu-id="c4bbe-240">Y416</span></span>   | <span data-ttu-id="c4bbe-241">4:4:4</span><span class="sxs-lookup"><span data-stu-id="c4bbe-241">4:4:4</span></span>           | <span data-ttu-id="c4bbe-242">Colocado</span><span class="sxs-lookup"><span data-stu-id="c4bbe-242">Packed</span></span>           | <span data-ttu-id="c4bbe-243">16</span><span class="sxs-lookup"><span data-stu-id="c4bbe-243">16</span></span>               |
| <span data-ttu-id="c4bbe-244">AI44</span><span class="sxs-lookup"><span data-stu-id="c4bbe-244">AI44</span></span>   | <span data-ttu-id="c4bbe-245">4:4:4</span><span class="sxs-lookup"><span data-stu-id="c4bbe-245">4:4:4</span></span>           | <span data-ttu-id="c4bbe-246">Colocado</span><span class="sxs-lookup"><span data-stu-id="c4bbe-246">Packed</span></span>           | <span data-ttu-id="c4bbe-247">Palettized</span><span class="sxs-lookup"><span data-stu-id="c4bbe-247">Palettized</span></span>       |
| <span data-ttu-id="c4bbe-248">YUY2</span><span class="sxs-lookup"><span data-stu-id="c4bbe-248">YUY2</span></span>   | <span data-ttu-id="c4bbe-249">4:2:2</span><span class="sxs-lookup"><span data-stu-id="c4bbe-249">4:2:2</span></span>           | <span data-ttu-id="c4bbe-250">Colocado</span><span class="sxs-lookup"><span data-stu-id="c4bbe-250">Packed</span></span>           | <span data-ttu-id="c4bbe-251">8</span><span class="sxs-lookup"><span data-stu-id="c4bbe-251">8</span></span>                |
| <span data-ttu-id="c4bbe-252">Y210</span><span class="sxs-lookup"><span data-stu-id="c4bbe-252">Y210</span></span>   | <span data-ttu-id="c4bbe-253">4:2:2</span><span class="sxs-lookup"><span data-stu-id="c4bbe-253">4:2:2</span></span>           | <span data-ttu-id="c4bbe-254">Colocado</span><span class="sxs-lookup"><span data-stu-id="c4bbe-254">Packed</span></span>           | <span data-ttu-id="c4bbe-255">10</span><span class="sxs-lookup"><span data-stu-id="c4bbe-255">10</span></span>               |
| <span data-ttu-id="c4bbe-256">Y216</span><span class="sxs-lookup"><span data-stu-id="c4bbe-256">Y216</span></span>   | <span data-ttu-id="c4bbe-257">4:2:2</span><span class="sxs-lookup"><span data-stu-id="c4bbe-257">4:2:2</span></span>           | <span data-ttu-id="c4bbe-258">Colocado</span><span class="sxs-lookup"><span data-stu-id="c4bbe-258">Packed</span></span>           | <span data-ttu-id="c4bbe-259">16</span><span class="sxs-lookup"><span data-stu-id="c4bbe-259">16</span></span>               |
| <span data-ttu-id="c4bbe-260">P210</span><span class="sxs-lookup"><span data-stu-id="c4bbe-260">P210</span></span>   | <span data-ttu-id="c4bbe-261">4:2:2</span><span class="sxs-lookup"><span data-stu-id="c4bbe-261">4:2:2</span></span>           | <span data-ttu-id="c4bbe-262">Planar</span><span class="sxs-lookup"><span data-stu-id="c4bbe-262">Planar</span></span>           | <span data-ttu-id="c4bbe-263">10</span><span class="sxs-lookup"><span data-stu-id="c4bbe-263">10</span></span>               |
| <span data-ttu-id="c4bbe-264">P216</span><span class="sxs-lookup"><span data-stu-id="c4bbe-264">P216</span></span>   | <span data-ttu-id="c4bbe-265">4:2:2</span><span class="sxs-lookup"><span data-stu-id="c4bbe-265">4:2:2</span></span>           | <span data-ttu-id="c4bbe-266">Planar</span><span class="sxs-lookup"><span data-stu-id="c4bbe-266">Planar</span></span>           | <span data-ttu-id="c4bbe-267">16</span><span class="sxs-lookup"><span data-stu-id="c4bbe-267">16</span></span>               |
| <span data-ttu-id="c4bbe-268">NV12</span><span class="sxs-lookup"><span data-stu-id="c4bbe-268">NV12</span></span>   | <span data-ttu-id="c4bbe-269">4:2:0</span><span class="sxs-lookup"><span data-stu-id="c4bbe-269">4:2:0</span></span>           | <span data-ttu-id="c4bbe-270">Planar</span><span class="sxs-lookup"><span data-stu-id="c4bbe-270">Planar</span></span>           | <span data-ttu-id="c4bbe-271">8</span><span class="sxs-lookup"><span data-stu-id="c4bbe-271">8</span></span>                |
| <span data-ttu-id="c4bbe-272">P010</span><span class="sxs-lookup"><span data-stu-id="c4bbe-272">P010</span></span>   | <span data-ttu-id="c4bbe-273">4:2:0</span><span class="sxs-lookup"><span data-stu-id="c4bbe-273">4:2:0</span></span>           | <span data-ttu-id="c4bbe-274">Planar</span><span class="sxs-lookup"><span data-stu-id="c4bbe-274">Planar</span></span>           | <span data-ttu-id="c4bbe-275">10</span><span class="sxs-lookup"><span data-stu-id="c4bbe-275">10</span></span>               |
| <span data-ttu-id="c4bbe-276">P016</span><span class="sxs-lookup"><span data-stu-id="c4bbe-276">P016</span></span>   | <span data-ttu-id="c4bbe-277">4:2:0</span><span class="sxs-lookup"><span data-stu-id="c4bbe-277">4:2:0</span></span>           | <span data-ttu-id="c4bbe-278">Planar</span><span class="sxs-lookup"><span data-stu-id="c4bbe-278">Planar</span></span>           | <span data-ttu-id="c4bbe-279">16</span><span class="sxs-lookup"><span data-stu-id="c4bbe-279">16</span></span>               |
| <span data-ttu-id="c4bbe-280">NV11</span><span class="sxs-lookup"><span data-stu-id="c4bbe-280">NV11</span></span>   | <span data-ttu-id="c4bbe-281">4:1:1</span><span class="sxs-lookup"><span data-stu-id="c4bbe-281">4:1:1</span></span>           | <span data-ttu-id="c4bbe-282">Planar</span><span class="sxs-lookup"><span data-stu-id="c4bbe-282">Planar</span></span>           | <span data-ttu-id="c4bbe-283">8</span><span class="sxs-lookup"><span data-stu-id="c4bbe-283">8</span></span>                |



 

<span data-ttu-id="c4bbe-284">É recomendável que, se um objeto der suporte a uma determinada profundidade de bits e esquema de amostragem croma, ele deve dar suporte aos formatos YUV correspondentes listados nesta tabela.</span><span class="sxs-lookup"><span data-stu-id="c4bbe-284">It is recommended that if an object supports a given bit depth and chroma sampling scheme, it should support the corresponding YUV formats listed in this table.</span></span> <span data-ttu-id="c4bbe-285">(Os objetos podem dar suporte a formatos adicionais não listados aqui.)</span><span class="sxs-lookup"><span data-stu-id="c4bbe-285">(Objects might support additional formats not listed here.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4bbe-286">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c4bbe-286">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4bbe-287">Formatos de YUV de 8 bits recomendados para renderização de vídeo</span><span class="sxs-lookup"><span data-stu-id="c4bbe-287">Recommended 8-Bit YUV Formats for Video Rendering</span></span>](recommended-8-bit-yuv-formats-for-video-rendering.md)
</dt> <dt>

[<span data-ttu-id="c4bbe-288">GUIDs de subtipo de vídeo</span><span class="sxs-lookup"><span data-stu-id="c4bbe-288">Video Subtype GUIDs</span></span>](video-subtype-guids.md)
</dt> <dt>

[<span data-ttu-id="c4bbe-289">Tipos de mídia de vídeo</span><span class="sxs-lookup"><span data-stu-id="c4bbe-289">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 



