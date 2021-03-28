---
description: Esta seção lista os códigos de operação de rasterização binários usados pelas funções GetROP2 e SetROP2. Os códigos de operação de rasterização definem como a GDI combina os bits da caneta selecionada com os bits no bitmap de destino.
ms.assetid: 9a3a5b5d-b41f-4859-8830-98272983a635
title: Operações de rasterização binárias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8a70030b1940c31d036505a80a6b1868aececd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091224"
---
# <a name="binary-raster-operations"></a><span data-ttu-id="0a14e-104">Operações de rasterização binárias</span><span class="sxs-lookup"><span data-stu-id="0a14e-104">Binary Raster Operations</span></span>

<span data-ttu-id="0a14e-105">Esta seção lista os códigos de operação de rasterização binários usados pelas funções [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) e [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) .</span><span class="sxs-lookup"><span data-stu-id="0a14e-105">This section lists the binary raster-operation codes used by the [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) and [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) functions.</span></span> <span data-ttu-id="0a14e-106">Os códigos de operação de rasterização definem como a GDI combina os bits da caneta selecionada com os bits no bitmap de destino.</span><span class="sxs-lookup"><span data-stu-id="0a14e-106">Raster-operation codes define how GDI combines the bits from the selected pen with the bits in the destination bitmap.</span></span>

<span data-ttu-id="0a14e-107">Cada código de operação de rasterização representa uma operação booliana na qual os valores dos pixels na caneta selecionada e no bitmap de destino são combinados.</span><span class="sxs-lookup"><span data-stu-id="0a14e-107">Each raster-operation code represents a Boolean operation in which the values of the pixels in the selected pen and the destination bitmap are combined.</span></span> <span data-ttu-id="0a14e-108">A seguir estão os dois operandos usados nessas operações.</span><span class="sxs-lookup"><span data-stu-id="0a14e-108">The following are the two operands used in these operations.</span></span>



| <span data-ttu-id="0a14e-109">Operando</span><span class="sxs-lookup"><span data-stu-id="0a14e-109">Operand</span></span> | <span data-ttu-id="0a14e-110">Significado</span><span class="sxs-lookup"><span data-stu-id="0a14e-110">Meaning</span></span>            |
|---------|--------------------|
| <span data-ttu-id="0a14e-111">P</span><span class="sxs-lookup"><span data-stu-id="0a14e-111">P</span></span>       | <span data-ttu-id="0a14e-112">Caneta selecionada</span><span class="sxs-lookup"><span data-stu-id="0a14e-112">Selected pen</span></span>       |
| <span data-ttu-id="0a14e-113">D</span><span class="sxs-lookup"><span data-stu-id="0a14e-113">D</span></span>       | <span data-ttu-id="0a14e-114">Bitmap de destino</span><span class="sxs-lookup"><span data-stu-id="0a14e-114">Destination bitmap</span></span> |



 

<span data-ttu-id="0a14e-115">Os operadores boolianos usados nessas operações são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="0a14e-115">The Boolean operators used in these operations follow.</span></span>



| <span data-ttu-id="0a14e-116">Operador</span><span class="sxs-lookup"><span data-stu-id="0a14e-116">Operator</span></span> | <span data-ttu-id="0a14e-117">Significado</span><span class="sxs-lookup"><span data-stu-id="0a14e-117">Meaning</span></span>                    |
|----------|----------------------------|
| <span data-ttu-id="0a14e-118">um</span><span class="sxs-lookup"><span data-stu-id="0a14e-118">a</span></span>        | <span data-ttu-id="0a14e-119">AND bit a bit</span><span class="sxs-lookup"><span data-stu-id="0a14e-119">Bitwise AND</span></span>                |
| <span data-ttu-id="0a14e-120">n</span><span class="sxs-lookup"><span data-stu-id="0a14e-120">n</span></span>        | <span data-ttu-id="0a14e-121">Não-bit (inverso)</span><span class="sxs-lookup"><span data-stu-id="0a14e-121">Bitwise NOT (inverse)</span></span>      |
| <span data-ttu-id="0a14e-122">o</span><span class="sxs-lookup"><span data-stu-id="0a14e-122">o</span></span>        | <span data-ttu-id="0a14e-123">OR bit a bit</span><span class="sxs-lookup"><span data-stu-id="0a14e-123">Bitwise OR</span></span>                 |
| <span data-ttu-id="0a14e-124">x</span><span class="sxs-lookup"><span data-stu-id="0a14e-124">x</span></span>        | <span data-ttu-id="0a14e-125">Or exclusivo de bit (XOR)</span><span class="sxs-lookup"><span data-stu-id="0a14e-125">Bitwise exclusive OR (XOR)</span></span> |



 

<span data-ttu-id="0a14e-126">Todas as operações boolianas são apresentadas em notação de polonês reverso.</span><span class="sxs-lookup"><span data-stu-id="0a14e-126">All Boolean operations are presented in reverse Polish notation.</span></span> <span data-ttu-id="0a14e-127">Por exemplo, a operação a seguir substitui os valores dos pixels no bitmap de destino por uma combinação dos valores de pixel da caneta e do pincel selecionado:</span><span class="sxs-lookup"><span data-stu-id="0a14e-127">For example, the following operation replaces the values of the pixels in the destination bitmap with a combination of the pixel values of the pen and the selected brush:</span></span>


```C++
DPo 
```



<span data-ttu-id="0a14e-128">Cada código de operação de rasterização é um inteiro de 32 bits cuja palavra de ordem superior é um índice de operação booliano e cuja palavra de ordem inferior é o código de operação.</span><span class="sxs-lookup"><span data-stu-id="0a14e-128">Each raster-operation code is a 32-bit integer whose high-order word is a Boolean operation index and whose low-order word is the operation code.</span></span> <span data-ttu-id="0a14e-129">O índice de operação de 16 bits é um valor de 8 bits com extensão zero que representa todos os resultados possíveis resultantes da operação booliana em dois parâmetros (nesse caso, os valores de caneta e de destino).</span><span class="sxs-lookup"><span data-stu-id="0a14e-129">The 16-bit operation index is a zero-extended 8-bit value that represents all possible outcomes resulting from the Boolean operation on two parameters (in this case, the pen and destination values).</span></span> <span data-ttu-id="0a14e-130">Por exemplo, os índices de operação para as operações DPo e DPan são mostrados na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="0a14e-130">For example, the operation indexes for the DPo and DPan operations are shown in the following list.</span></span>



| <span data-ttu-id="0a14e-131">P</span><span class="sxs-lookup"><span data-stu-id="0a14e-131">P</span></span>   | <span data-ttu-id="0a14e-132">D</span><span class="sxs-lookup"><span data-stu-id="0a14e-132">D</span></span>   | <span data-ttu-id="0a14e-133">DPo</span><span class="sxs-lookup"><span data-stu-id="0a14e-133">DPo</span></span> | <span data-ttu-id="0a14e-134">Dpan</span><span class="sxs-lookup"><span data-stu-id="0a14e-134">Dpan</span></span> |
|-----|-----|-----|------|
| <span data-ttu-id="0a14e-135">0</span><span class="sxs-lookup"><span data-stu-id="0a14e-135">0</span></span>   | <span data-ttu-id="0a14e-136">0</span><span class="sxs-lookup"><span data-stu-id="0a14e-136">0</span></span>   | <span data-ttu-id="0a14e-137">0</span><span class="sxs-lookup"><span data-stu-id="0a14e-137">0</span></span>   | <span data-ttu-id="0a14e-138">1</span><span class="sxs-lookup"><span data-stu-id="0a14e-138">1</span></span>    |
| <span data-ttu-id="0a14e-139">0</span><span class="sxs-lookup"><span data-stu-id="0a14e-139">0</span></span>   | <span data-ttu-id="0a14e-140">1</span><span class="sxs-lookup"><span data-stu-id="0a14e-140">1</span></span>   | <span data-ttu-id="0a14e-141">1</span><span class="sxs-lookup"><span data-stu-id="0a14e-141">1</span></span>   | <span data-ttu-id="0a14e-142">1</span><span class="sxs-lookup"><span data-stu-id="0a14e-142">1</span></span>    |
| <span data-ttu-id="0a14e-143">1</span><span class="sxs-lookup"><span data-stu-id="0a14e-143">1</span></span>   | <span data-ttu-id="0a14e-144">0</span><span class="sxs-lookup"><span data-stu-id="0a14e-144">0</span></span>   | <span data-ttu-id="0a14e-145">1</span><span class="sxs-lookup"><span data-stu-id="0a14e-145">1</span></span>   | <span data-ttu-id="0a14e-146">1</span><span class="sxs-lookup"><span data-stu-id="0a14e-146">1</span></span>    |
| <span data-ttu-id="0a14e-147">1</span><span class="sxs-lookup"><span data-stu-id="0a14e-147">1</span></span>   | <span data-ttu-id="0a14e-148">1</span><span class="sxs-lookup"><span data-stu-id="0a14e-148">1</span></span>   | <span data-ttu-id="0a14e-149">1</span><span class="sxs-lookup"><span data-stu-id="0a14e-149">1</span></span>   | <span data-ttu-id="0a14e-150">0</span><span class="sxs-lookup"><span data-stu-id="0a14e-150">0</span></span>    |



 

<span data-ttu-id="0a14e-151">A lista a seguir descreve os modos de desenho e as operações boolianas que eles representam.</span><span class="sxs-lookup"><span data-stu-id="0a14e-151">The following list outlines the drawing modes and the Boolean operations that they represent.</span></span>



| <span data-ttu-id="0a14e-152">Operação de varredura</span><span class="sxs-lookup"><span data-stu-id="0a14e-152">Raster operation</span></span> | <span data-ttu-id="0a14e-153">Operação booliana</span><span class="sxs-lookup"><span data-stu-id="0a14e-153">Boolean operation</span></span> |
|------------------|-------------------|
| <span data-ttu-id="0a14e-154">R2 \_ preto</span><span class="sxs-lookup"><span data-stu-id="0a14e-154">R2\_BLACK</span></span>        | <span data-ttu-id="0a14e-155">0</span><span class="sxs-lookup"><span data-stu-id="0a14e-155">0</span></span>                 |
| <span data-ttu-id="0a14e-156">\_COPYPEN R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-156">R2\_COPYPEN</span></span>      | <span data-ttu-id="0a14e-157">P</span><span class="sxs-lookup"><span data-stu-id="0a14e-157">P</span></span>                 |
| <span data-ttu-id="0a14e-158">\_MASKNOTPEN R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-158">R2\_MASKNOTPEN</span></span>   | <span data-ttu-id="0a14e-159">DPna</span><span class="sxs-lookup"><span data-stu-id="0a14e-159">DPna</span></span>              |
| <span data-ttu-id="0a14e-160">\_MASKPEN R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-160">R2\_MASKPEN</span></span>      | <span data-ttu-id="0a14e-161">DPa</span><span class="sxs-lookup"><span data-stu-id="0a14e-161">DPa</span></span>               |
| <span data-ttu-id="0a14e-162">\_MASKPENNOT R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-162">R2\_MASKPENNOT</span></span>   | <span data-ttu-id="0a14e-163">PDna</span><span class="sxs-lookup"><span data-stu-id="0a14e-163">PDna</span></span>              |
| <span data-ttu-id="0a14e-164">\_MERGENOTPEN R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-164">R2\_MERGENOTPEN</span></span>  | <span data-ttu-id="0a14e-165">DPno</span><span class="sxs-lookup"><span data-stu-id="0a14e-165">DPno</span></span>              |
| <span data-ttu-id="0a14e-166">\_MERGEPEN R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-166">R2\_MERGEPEN</span></span>     | <span data-ttu-id="0a14e-167">DPo</span><span class="sxs-lookup"><span data-stu-id="0a14e-167">DPo</span></span>               |
| <span data-ttu-id="0a14e-168">\_MERGEPENNOT R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-168">R2\_MERGEPENNOT</span></span>  | <span data-ttu-id="0a14e-169">PDno</span><span class="sxs-lookup"><span data-stu-id="0a14e-169">PDno</span></span>              |
| <span data-ttu-id="0a14e-170">\_Nop R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-170">R2\_NOP</span></span>          | <span data-ttu-id="0a14e-171">D</span><span class="sxs-lookup"><span data-stu-id="0a14e-171">D</span></span>                 |
| <span data-ttu-id="0a14e-172">R2 \_ não</span><span class="sxs-lookup"><span data-stu-id="0a14e-172">R2\_NOT</span></span>          | <span data-ttu-id="0a14e-173">Dn</span><span class="sxs-lookup"><span data-stu-id="0a14e-173">Dn</span></span>                |
| <span data-ttu-id="0a14e-174">\_NOTCOPYPEN R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-174">R2\_NOTCOPYPEN</span></span>   | <span data-ttu-id="0a14e-175">NP</span><span class="sxs-lookup"><span data-stu-id="0a14e-175">Pn</span></span>                |
| <span data-ttu-id="0a14e-176">\_NOTMASKPEN R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-176">R2\_NOTMASKPEN</span></span>   | <span data-ttu-id="0a14e-177">DPan</span><span class="sxs-lookup"><span data-stu-id="0a14e-177">DPan</span></span>              |
| <span data-ttu-id="0a14e-178">\_NOTMERGEPEN R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-178">R2\_NOTMERGEPEN</span></span>  | <span data-ttu-id="0a14e-179">DPon</span><span class="sxs-lookup"><span data-stu-id="0a14e-179">DPon</span></span>              |
| <span data-ttu-id="0a14e-180">\_NOTXORPEN R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-180">R2\_NOTXORPEN</span></span>    | <span data-ttu-id="0a14e-181">DPxn</span><span class="sxs-lookup"><span data-stu-id="0a14e-181">DPxn</span></span>              |
| <span data-ttu-id="0a14e-182">R2 \_ branco</span><span class="sxs-lookup"><span data-stu-id="0a14e-182">R2\_WHITE</span></span>        | <span data-ttu-id="0a14e-183">1</span><span class="sxs-lookup"><span data-stu-id="0a14e-183">1</span></span>                 |
| <span data-ttu-id="0a14e-184">\_XORPEN R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-184">R2\_XORPEN</span></span>       | <span data-ttu-id="0a14e-185">DPx</span><span class="sxs-lookup"><span data-stu-id="0a14e-185">DPx</span></span>               |



 

<span data-ttu-id="0a14e-186">Para um dispositivo monocromático, o GDI mapeia o valor zero para preto e o valor de 1 a branco.</span><span class="sxs-lookup"><span data-stu-id="0a14e-186">For a monochrome device, GDI maps the value zero to black and the value 1 to white.</span></span> <span data-ttu-id="0a14e-187">Se um aplicativo tentar desenhar com uma caneta preta em um destino branco usando as operações de varredura binária disponíveis, ocorrerão os resultados a seguir.</span><span class="sxs-lookup"><span data-stu-id="0a14e-187">If an application attempts to draw with a black pen on a white destination by using the available binary raster operations, the following results occur.</span></span>



| <span data-ttu-id="0a14e-188">Operação de varredura</span><span class="sxs-lookup"><span data-stu-id="0a14e-188">Raster operation</span></span> | <span data-ttu-id="0a14e-189">Resultado</span><span class="sxs-lookup"><span data-stu-id="0a14e-189">Result</span></span>             |
|------------------|--------------------|
| <span data-ttu-id="0a14e-190">R2 \_ preto</span><span class="sxs-lookup"><span data-stu-id="0a14e-190">R2\_BLACK</span></span>        | <span data-ttu-id="0a14e-191">Linha preta visível</span><span class="sxs-lookup"><span data-stu-id="0a14e-191">Visible black line</span></span> |
| <span data-ttu-id="0a14e-192">\_COPYPEN R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-192">R2\_COPYPEN</span></span>      | <span data-ttu-id="0a14e-193">Linha preta visível</span><span class="sxs-lookup"><span data-stu-id="0a14e-193">Visible black line</span></span> |
| <span data-ttu-id="0a14e-194">\_MASKNOTPEN R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-194">R2\_MASKNOTPEN</span></span>   | <span data-ttu-id="0a14e-195">Nenhuma linha visível</span><span class="sxs-lookup"><span data-stu-id="0a14e-195">No visible line</span></span>    |
| <span data-ttu-id="0a14e-196">\_MASKPEN R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-196">R2\_MASKPEN</span></span>      | <span data-ttu-id="0a14e-197">Linha preta visível</span><span class="sxs-lookup"><span data-stu-id="0a14e-197">Visible black line</span></span> |
| <span data-ttu-id="0a14e-198">\_MASKPENNOT R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-198">R2\_MASKPENNOT</span></span>   | <span data-ttu-id="0a14e-199">Linha preta visível</span><span class="sxs-lookup"><span data-stu-id="0a14e-199">Visible black line</span></span> |
| <span data-ttu-id="0a14e-200">\_MERGENOTPEN R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-200">R2\_MERGENOTPEN</span></span>  | <span data-ttu-id="0a14e-201">Nenhuma linha visível</span><span class="sxs-lookup"><span data-stu-id="0a14e-201">No visible line</span></span>    |
| <span data-ttu-id="0a14e-202">\_MERGEPEN R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-202">R2\_MERGEPEN</span></span>     | <span data-ttu-id="0a14e-203">Linha preta visível</span><span class="sxs-lookup"><span data-stu-id="0a14e-203">Visible black line</span></span> |
| <span data-ttu-id="0a14e-204">\_MERGEPENNOT R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-204">R2\_MERGEPENNOT</span></span>  | <span data-ttu-id="0a14e-205">Linha preta visível</span><span class="sxs-lookup"><span data-stu-id="0a14e-205">Visible black line</span></span> |
| <span data-ttu-id="0a14e-206">\_Nop R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-206">R2\_NOP</span></span>          | <span data-ttu-id="0a14e-207">Nenhuma linha visível</span><span class="sxs-lookup"><span data-stu-id="0a14e-207">No visible line</span></span>    |
| <span data-ttu-id="0a14e-208">R2 \_ não</span><span class="sxs-lookup"><span data-stu-id="0a14e-208">R2\_NOT</span></span>          | <span data-ttu-id="0a14e-209">Linha preta visível</span><span class="sxs-lookup"><span data-stu-id="0a14e-209">Visible black line</span></span> |
| <span data-ttu-id="0a14e-210">\_NOTCOPYPEN R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-210">R2\_NOTCOPYPEN</span></span>   | <span data-ttu-id="0a14e-211">Nenhuma linha visível</span><span class="sxs-lookup"><span data-stu-id="0a14e-211">No visible line</span></span>    |
| <span data-ttu-id="0a14e-212">\_NOTMASKPEN R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-212">R2\_NOTMASKPEN</span></span>   | <span data-ttu-id="0a14e-213">Nenhuma linha visível</span><span class="sxs-lookup"><span data-stu-id="0a14e-213">No visible line</span></span>    |
| <span data-ttu-id="0a14e-214">\_NOTMERGEPEN R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-214">R2\_NOTMERGEPEN</span></span>  | <span data-ttu-id="0a14e-215">Linha preta visível</span><span class="sxs-lookup"><span data-stu-id="0a14e-215">Visible black line</span></span> |
| <span data-ttu-id="0a14e-216">\_NOTXORPEN R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-216">R2\_NOTXORPEN</span></span>    | <span data-ttu-id="0a14e-217">Linha preta visível</span><span class="sxs-lookup"><span data-stu-id="0a14e-217">Visible black line</span></span> |
| <span data-ttu-id="0a14e-218">R2 \_ branco</span><span class="sxs-lookup"><span data-stu-id="0a14e-218">R2\_WHITE</span></span>        | <span data-ttu-id="0a14e-219">Nenhuma linha visível</span><span class="sxs-lookup"><span data-stu-id="0a14e-219">No visible line</span></span>    |
| <span data-ttu-id="0a14e-220">\_XORPEN R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-220">R2\_XORPEN</span></span>       | <span data-ttu-id="0a14e-221">Nenhuma linha visível</span><span class="sxs-lookup"><span data-stu-id="0a14e-221">No visible line</span></span>    |



 

<span data-ttu-id="0a14e-222">Para um dispositivo de cores, o GDI usa valores RGB para representar as cores da caneta e o destino.</span><span class="sxs-lookup"><span data-stu-id="0a14e-222">For a color device, GDI uses RGB values to represent the colors of the pen and the destination.</span></span> <span data-ttu-id="0a14e-223">Um valor de cor RGB é um inteiro longo que contém um campo de cor vermelho, verde e azul, cada um especificando a intensidade da cor especificada.</span><span class="sxs-lookup"><span data-stu-id="0a14e-223">An RGB color value is a long integer that contains a red, a green, and a blue color field, each specifying the intensity of the specified color.</span></span> <span data-ttu-id="0a14e-224">As intensidades variam de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="0a14e-224">Intensities range from 0 through 255.</span></span> <span data-ttu-id="0a14e-225">Os valores são empacotados nos três bytes de ordem baixa do inteiro longo.</span><span class="sxs-lookup"><span data-stu-id="0a14e-225">The values are packed in the three low-order bytes of the long integer.</span></span> <span data-ttu-id="0a14e-226">A cor de uma caneta é sempre uma cor sólida, mas a cor do destino pode ser uma mistura de duas ou três cores.</span><span class="sxs-lookup"><span data-stu-id="0a14e-226">The color of a pen is always a solid color, but the color of the destination may be a mixture of any two or three colors.</span></span> <span data-ttu-id="0a14e-227">Se um aplicativo tentar desenhar com uma caneta branca em um destino azul usando as operações de varredura binária disponíveis, ocorrerão os resultados a seguir.</span><span class="sxs-lookup"><span data-stu-id="0a14e-227">If an application attempts to draw with a white pen on a blue destination by using the available binary raster operations, the following results occur.</span></span>



| <span data-ttu-id="0a14e-228">Operação de varredura</span><span class="sxs-lookup"><span data-stu-id="0a14e-228">Raster operation</span></span> | <span data-ttu-id="0a14e-229">Resultado</span><span class="sxs-lookup"><span data-stu-id="0a14e-229">Result</span></span>                 |
|------------------|------------------------|
| <span data-ttu-id="0a14e-230">R2 \_ preto</span><span class="sxs-lookup"><span data-stu-id="0a14e-230">R2\_BLACK</span></span>        | <span data-ttu-id="0a14e-231">Linha preta visível</span><span class="sxs-lookup"><span data-stu-id="0a14e-231">Visible black line</span></span>     |
| <span data-ttu-id="0a14e-232">\_COPYPEN R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-232">R2\_COPYPEN</span></span>      | <span data-ttu-id="0a14e-233">Linha branca visível</span><span class="sxs-lookup"><span data-stu-id="0a14e-233">Visible white line</span></span>     |
| <span data-ttu-id="0a14e-234">\_MASKNOTPEN R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-234">R2\_MASKNOTPEN</span></span>   | <span data-ttu-id="0a14e-235">Linha preta visível</span><span class="sxs-lookup"><span data-stu-id="0a14e-235">Visible black line</span></span>     |
| <span data-ttu-id="0a14e-236">\_MASKPEN R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-236">R2\_MASKPEN</span></span>      | <span data-ttu-id="0a14e-237">Linha azul invisível</span><span class="sxs-lookup"><span data-stu-id="0a14e-237">Invisible blue line</span></span>    |
| <span data-ttu-id="0a14e-238">\_MASKPENNOT R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-238">R2\_MASKPENNOT</span></span>   | <span data-ttu-id="0a14e-239">Linha vermelha/verde visível</span><span class="sxs-lookup"><span data-stu-id="0a14e-239">Visible red/green line</span></span> |
| <span data-ttu-id="0a14e-240">\_MERGENOTPEN R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-240">R2\_MERGENOTPEN</span></span>  | <span data-ttu-id="0a14e-241">Linha azul invisível</span><span class="sxs-lookup"><span data-stu-id="0a14e-241">Invisible blue line</span></span>    |
| <span data-ttu-id="0a14e-242">\_MERGEPEN R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-242">R2\_MERGEPEN</span></span>     | <span data-ttu-id="0a14e-243">Linha branca visível</span><span class="sxs-lookup"><span data-stu-id="0a14e-243">Visible white line</span></span>     |
| <span data-ttu-id="0a14e-244">\_MERGEPENNOT R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-244">R2\_MERGEPENNOT</span></span>  | <span data-ttu-id="0a14e-245">Linha branca visível</span><span class="sxs-lookup"><span data-stu-id="0a14e-245">Visible white line</span></span>     |
| <span data-ttu-id="0a14e-246">\_Nop R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-246">R2\_NOP</span></span>          | <span data-ttu-id="0a14e-247">Linha azul invisível</span><span class="sxs-lookup"><span data-stu-id="0a14e-247">Invisible blue line</span></span>    |
| <span data-ttu-id="0a14e-248">R2 \_ não</span><span class="sxs-lookup"><span data-stu-id="0a14e-248">R2\_NOT</span></span>          | <span data-ttu-id="0a14e-249">Linha vermelha/verde visível</span><span class="sxs-lookup"><span data-stu-id="0a14e-249">Visible red/green line</span></span> |
| <span data-ttu-id="0a14e-250">\_NOTCOPYPEN R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-250">R2\_NOTCOPYPEN</span></span>   | <span data-ttu-id="0a14e-251">Linha preta visível</span><span class="sxs-lookup"><span data-stu-id="0a14e-251">Visible black line</span></span>     |
| <span data-ttu-id="0a14e-252">\_NOTMASKPEN R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-252">R2\_NOTMASKPEN</span></span>   | <span data-ttu-id="0a14e-253">Linha vermelha/verde visível</span><span class="sxs-lookup"><span data-stu-id="0a14e-253">Visible red/green line</span></span> |
| <span data-ttu-id="0a14e-254">\_NOTMERGEPEN R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-254">R2\_NOTMERGEPEN</span></span>  | <span data-ttu-id="0a14e-255">Linha preta visível</span><span class="sxs-lookup"><span data-stu-id="0a14e-255">Visible black line</span></span>     |
| <span data-ttu-id="0a14e-256">\_NOTXORPEN R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-256">R2\_NOTXORPEN</span></span>    | <span data-ttu-id="0a14e-257">Linha azul invisível</span><span class="sxs-lookup"><span data-stu-id="0a14e-257">Invisible blue line</span></span>    |
| <span data-ttu-id="0a14e-258">R2 \_ branco</span><span class="sxs-lookup"><span data-stu-id="0a14e-258">R2\_WHITE</span></span>        | <span data-ttu-id="0a14e-259">Linha branca visível</span><span class="sxs-lookup"><span data-stu-id="0a14e-259">Visible white line</span></span>     |
| <span data-ttu-id="0a14e-260">\_XORPEN R2</span><span class="sxs-lookup"><span data-stu-id="0a14e-260">R2\_XORPEN</span></span>       | <span data-ttu-id="0a14e-261">Linha vermelha/verde visível</span><span class="sxs-lookup"><span data-stu-id="0a14e-261">Visible red/green line</span></span> |



 

 

 



