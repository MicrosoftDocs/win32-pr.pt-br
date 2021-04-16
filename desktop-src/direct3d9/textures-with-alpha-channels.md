---
description: Há duas maneiras de codificar mapas de textura que exibem transparência mais complexa.
ms.assetid: cae788f6-60f1-4987-8f06-bf4256bccd9b
title: Texturas com canais alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c361b0335ef4f36b4efc9c90c71270e855f5db
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104558871"
---
# <a name="textures-with-alpha-channels-direct3d-9"></a><span data-ttu-id="7430c-103">Texturas com canais alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7430c-103">Textures with Alpha Channels (Direct3D 9)</span></span>

<span data-ttu-id="7430c-104">Há duas maneiras de codificar mapas de textura que exibem transparência mais complexa.</span><span class="sxs-lookup"><span data-stu-id="7430c-104">There are two ways to encode texture maps that exhibit more complex transparency.</span></span> <span data-ttu-id="7430c-105">Em cada caso, um bloco que descreve a transparência precede o bloco de 64 bits já descrito.</span><span class="sxs-lookup"><span data-stu-id="7430c-105">In each case, a block that describes the transparency precedes the 64-bit block already described.</span></span> <span data-ttu-id="7430c-106">A transparência é representada como um bitmap de 4 x 4 com 4 bits por pixel (codificação explícita), ou com menos bits e interpolação linear parecida com a que é usada para a codificação de cores.</span><span class="sxs-lookup"><span data-stu-id="7430c-106">The transparency is either represented as a 4x4 bitmap with 4 bits per pixel (explicit encoding), or with fewer bits and linear interpolation that is analogous to what is used for color encoding.</span></span>

<span data-ttu-id="7430c-107">O bloco de transparência e o bloco de cores são organizados conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7430c-107">The transparency block and the color block are arranged as shown in the following table.</span></span>



| <span data-ttu-id="7430c-108">Endereço da palavra</span><span class="sxs-lookup"><span data-stu-id="7430c-108">Word address</span></span> | <span data-ttu-id="7430c-109">Bloco de 64 bits</span><span class="sxs-lookup"><span data-stu-id="7430c-109">64-bit block</span></span>                      |
|--------------|-----------------------------------|
| <span data-ttu-id="7430c-110">3:0</span><span class="sxs-lookup"><span data-stu-id="7430c-110">3:0</span></span>          | <span data-ttu-id="7430c-111">Bloco de transparência</span><span class="sxs-lookup"><span data-stu-id="7430c-111">Transparency block</span></span>                |
| <span data-ttu-id="7430c-112">7:4</span><span class="sxs-lookup"><span data-stu-id="7430c-112">7:4</span></span>          | <span data-ttu-id="7430c-113">Bloco de 64 bits descrito anteriormente</span><span class="sxs-lookup"><span data-stu-id="7430c-113">Previously described 64-bit block</span></span> |



 

## <a name="explicit-texture-encoding"></a><span data-ttu-id="7430c-114">Codificação de textura explícita</span><span class="sxs-lookup"><span data-stu-id="7430c-114">Explicit Texture Encoding</span></span>

<span data-ttu-id="7430c-115">Para a codificação de textura explícita (formatos DXT2 e DXT3), os componentes alfa do texels que descrevem a transparência são codificados em um bitmap 4x4 com 4 bits por Texel.</span><span class="sxs-lookup"><span data-stu-id="7430c-115">For explicit texture encoding (DXT2 and DXT3 formats), the alpha components of the texels that describe transparency are encoded in a 4x4 bitmap with 4 bits per texel.</span></span> <span data-ttu-id="7430c-116">Esses quatro bits podem ser alcançados por uma variedade de meios, como pontilhado ou usando os quatro bits mais significativos dos dados alfa.</span><span class="sxs-lookup"><span data-stu-id="7430c-116">These four bits can be achieved through a variety of means such as dithering or by using the four most significant bits of the alpha data.</span></span> <span data-ttu-id="7430c-117">Independentemente de como são produzidos, eles são usados como estão, sem qualquer forma de interpolação.</span><span class="sxs-lookup"><span data-stu-id="7430c-117">However they are produced, they are used just as they are, without any form of interpolation.</span></span>

<span data-ttu-id="7430c-118">O diagrama a seguir mostra um bloco de transparência de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7430c-118">The following diagram shows a 64-bit transparency block.</span></span>

![diagrama de um bloco de transparência de 64 bits](images/colors4.png)

> [!Note]  
> <span data-ttu-id="7430c-120">O método de compactação do Direct3D usa os quatro bits mais significativos.</span><span class="sxs-lookup"><span data-stu-id="7430c-120">The compression method of Direct3D uses the four most significant bits.</span></span>

 

<span data-ttu-id="7430c-121">As tabelas a seguir ilustram como as informações alfa são dispostas na memória, para cada palavra de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="7430c-121">The following tables illustrate how the alpha information is laid out in memory, for each 16-bit word.</span></span>

<span data-ttu-id="7430c-122">Esta tabela contém o layout para o Word 0.</span><span class="sxs-lookup"><span data-stu-id="7430c-122">This table contains the layout for word 0.</span></span>



| <span data-ttu-id="7430c-123">Bits</span><span class="sxs-lookup"><span data-stu-id="7430c-123">Bits</span></span>          | <span data-ttu-id="7430c-124">Alpha</span><span class="sxs-lookup"><span data-stu-id="7430c-124">Alpha</span></span>      |
|---------------|------------|
| <span data-ttu-id="7430c-125">3:0 (LSB \* )</span><span class="sxs-lookup"><span data-stu-id="7430c-125">3:0 (LSB\*)</span></span>   | <span data-ttu-id="7430c-126">\[0 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="7430c-126">\[0\]\[0\]</span></span> |
| <span data-ttu-id="7430c-127">7:4</span><span class="sxs-lookup"><span data-stu-id="7430c-127">7:4</span></span>           | <span data-ttu-id="7430c-128">\[0 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="7430c-128">\[0\]\[1\]</span></span> |
| <span data-ttu-id="7430c-129">11:8</span><span class="sxs-lookup"><span data-stu-id="7430c-129">11:8</span></span>          | <span data-ttu-id="7430c-130">\[0 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="7430c-130">\[0\]\[2\]</span></span> |
| <span data-ttu-id="7430c-131">15:12 (MSB \* )</span><span class="sxs-lookup"><span data-stu-id="7430c-131">15:12 (MSB\*)</span></span> | <span data-ttu-id="7430c-132">\[0 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="7430c-132">\[0\]\[3\]</span></span> |



 

<span data-ttu-id="7430c-133">\*bit menos significativo, bit mais significativo (MSB)</span><span class="sxs-lookup"><span data-stu-id="7430c-133">\*least-significant bit, most significant bit (MSB)</span></span>

<span data-ttu-id="7430c-134">Esta tabela contém o layout para o Word 1.</span><span class="sxs-lookup"><span data-stu-id="7430c-134">This table contains the layout for word 1.</span></span>



| <span data-ttu-id="7430c-135">Bits</span><span class="sxs-lookup"><span data-stu-id="7430c-135">Bits</span></span>        | <span data-ttu-id="7430c-136">Alpha</span><span class="sxs-lookup"><span data-stu-id="7430c-136">Alpha</span></span>      |
|-------------|------------|
| <span data-ttu-id="7430c-137">3:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="7430c-137">3:0 (LSB)</span></span>   | <span data-ttu-id="7430c-138">\[1 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="7430c-138">\[1\]\[0\]</span></span> |
| <span data-ttu-id="7430c-139">7:4</span><span class="sxs-lookup"><span data-stu-id="7430c-139">7:4</span></span>         | <span data-ttu-id="7430c-140">\[1 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="7430c-140">\[1\]\[1\]</span></span> |
| <span data-ttu-id="7430c-141">11:8</span><span class="sxs-lookup"><span data-stu-id="7430c-141">11:8</span></span>        | <span data-ttu-id="7430c-142">\[1 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="7430c-142">\[1\]\[2\]</span></span> |
| <span data-ttu-id="7430c-143">15:12 (MSB)</span><span class="sxs-lookup"><span data-stu-id="7430c-143">15:12 (MSB)</span></span> | <span data-ttu-id="7430c-144">\[1 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="7430c-144">\[1\]\[3\]</span></span> |



 

<span data-ttu-id="7430c-145">Esta tabela contém o layout para o Word 2.</span><span class="sxs-lookup"><span data-stu-id="7430c-145">This table contains the layout for word 2.</span></span>



| <span data-ttu-id="7430c-146">Bits</span><span class="sxs-lookup"><span data-stu-id="7430c-146">Bits</span></span>        | <span data-ttu-id="7430c-147">Alpha</span><span class="sxs-lookup"><span data-stu-id="7430c-147">Alpha</span></span>      |
|-------------|------------|
| <span data-ttu-id="7430c-148">3:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="7430c-148">3:0 (LSB)</span></span>   | <span data-ttu-id="7430c-149">\[2 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="7430c-149">\[2\]\[0\]</span></span> |
| <span data-ttu-id="7430c-150">7:4</span><span class="sxs-lookup"><span data-stu-id="7430c-150">7:4</span></span>         | <span data-ttu-id="7430c-151">\[2 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="7430c-151">\[2\]\[1\]</span></span> |
| <span data-ttu-id="7430c-152">11:8</span><span class="sxs-lookup"><span data-stu-id="7430c-152">11:8</span></span>        | <span data-ttu-id="7430c-153">\[2 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="7430c-153">\[2\]\[2\]</span></span> |
| <span data-ttu-id="7430c-154">15:12 (MSB)</span><span class="sxs-lookup"><span data-stu-id="7430c-154">15:12 (MSB)</span></span> | <span data-ttu-id="7430c-155">\[2 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="7430c-155">\[2\]\[3\]</span></span> |



 

<span data-ttu-id="7430c-156">Esta tabela contém o layout para o Word 3.</span><span class="sxs-lookup"><span data-stu-id="7430c-156">This table contains the layout for word 3.</span></span>



| <span data-ttu-id="7430c-157">Bits</span><span class="sxs-lookup"><span data-stu-id="7430c-157">Bits</span></span>        | <span data-ttu-id="7430c-158">Alpha</span><span class="sxs-lookup"><span data-stu-id="7430c-158">Alpha</span></span>      |
|-------------|------------|
| <span data-ttu-id="7430c-159">3:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="7430c-159">3:0 (LSB)</span></span>   | <span data-ttu-id="7430c-160">\[3 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="7430c-160">\[3\]\[0\]</span></span> |
| <span data-ttu-id="7430c-161">7:4</span><span class="sxs-lookup"><span data-stu-id="7430c-161">7:4</span></span>         | <span data-ttu-id="7430c-162">\[3 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="7430c-162">\[3\]\[1\]</span></span> |
| <span data-ttu-id="7430c-163">11:8</span><span class="sxs-lookup"><span data-stu-id="7430c-163">11:8</span></span>        | <span data-ttu-id="7430c-164">\[3 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="7430c-164">\[3\]\[2\]</span></span> |
| <span data-ttu-id="7430c-165">15:12 (MSB)</span><span class="sxs-lookup"><span data-stu-id="7430c-165">15:12 (MSB)</span></span> | <span data-ttu-id="7430c-166">\[3 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="7430c-166">\[3\]\[3\]</span></span> |



 

<span data-ttu-id="7430c-167">A diferença entre DXT2 e DXT3 é que, no formato DXT2, supõe-se que os dados de cor foram contramultiplicados por alfa.</span><span class="sxs-lookup"><span data-stu-id="7430c-167">The difference between DXT2 and DXT3 are that, in the DXT2 format, it is assumed that the color data has been premultiplied by alpha.</span></span> <span data-ttu-id="7430c-168">No formato DXT3, supõe-se que a cor não seja contramultiplicada por alfa.</span><span class="sxs-lookup"><span data-stu-id="7430c-168">In the DXT3 format, it is assumed that the color is not premultiplied by alpha.</span></span> <span data-ttu-id="7430c-169">Esses dois formatos são necessários porque, na maioria dos casos, no momento em que uma textura é usada, apenas examinar os dados não é suficiente para determinar se os valores de cor foram multiplicados por alfa.</span><span class="sxs-lookup"><span data-stu-id="7430c-169">These two formats are needed because, in most cases, by the time a texture is used, just examining the data is not sufficient to determine if the color values have been multiplied by alpha.</span></span> <span data-ttu-id="7430c-170">Como essas informações são necessárias em tempo de execução, os dois códigos FOURCC são usados para diferenciar esses casos.</span><span class="sxs-lookup"><span data-stu-id="7430c-170">Because this information is needed at run time, the two FOURCC codes are used to differentiate these cases.</span></span> <span data-ttu-id="7430c-171">No entanto, os dados e o método de interpolação usados para esses dois formatos são idênticos.</span><span class="sxs-lookup"><span data-stu-id="7430c-171">However, the data and interpolation method used for these two formats is identical.</span></span>

<span data-ttu-id="7430c-172">A comparação de cores usada em DXT1 para determinar se Texel é transparente não é usada neste formato.</span><span class="sxs-lookup"><span data-stu-id="7430c-172">The color compare used in DXT1 to determine if the texel is transparent is not used in this format.</span></span> <span data-ttu-id="7430c-173">Presume-se que, sem a comparação de cores, os dados de cor sejam sempre tratados como se estivessem modo de 4 cores.</span><span class="sxs-lookup"><span data-stu-id="7430c-173">It is assumed that without the color compare the color data is always treated as if in 4-color mode.</span></span> <span data-ttu-id="7430c-174">Em outras palavras, a instrução If na parte superior do código DXT1 deve ser a seguinte:</span><span class="sxs-lookup"><span data-stu-id="7430c-174">In other words, the if statement at the top of the DXT1 code should be the following:</span></span>


```
if ((color_0 > color_1) OR !DXT1) {
```



## <a name="three-bit-linear-alpha-interpolation"></a><span data-ttu-id="7430c-175">Interpolação alfa Three-Bit linear</span><span class="sxs-lookup"><span data-stu-id="7430c-175">Three-Bit Linear Alpha Interpolation</span></span>

<span data-ttu-id="7430c-176">A codificação de transparência para os formatos DXT4 e DXT5 é baseada em um conceito semelhante à codificação linear usada para a cor.</span><span class="sxs-lookup"><span data-stu-id="7430c-176">The encoding of transparency for the DXT4 and DXT5 formats is based on a concept similar to the linear encoding used for color.</span></span> <span data-ttu-id="7430c-177">Dois valores alfa de 8 bits e um bitmap 4x4 com três bits por pixel são armazenados nos primeiros oito bytes do bloco.</span><span class="sxs-lookup"><span data-stu-id="7430c-177">Two 8-bit alpha values and a 4x4 bitmap with three bits per pixel are stored in the first eight bytes of the block.</span></span> <span data-ttu-id="7430c-178">Os valores alfa representativos são usados para interpolar os valores alfa intermediários.</span><span class="sxs-lookup"><span data-stu-id="7430c-178">The representative alpha values are used to interpolate intermediate alpha values.</span></span> <span data-ttu-id="7430c-179">Há mais informações disponíveis sobre como os dois valores alfa são armazenados.</span><span class="sxs-lookup"><span data-stu-id="7430c-179">Additional information is available in the way the two alpha values are stored.</span></span> <span data-ttu-id="7430c-180">Se alfa \_ 0 for maior que alfa \_ 1, seis valores Alfa intermediários serão criados pela interpolação.</span><span class="sxs-lookup"><span data-stu-id="7430c-180">If alpha\_0 is greater than alpha\_1, then six intermediate alpha values are created by the interpolation.</span></span> <span data-ttu-id="7430c-181">Caso contrário, os quatro valores alfa intermediários são interpolados entre os extremos alfa especificados.</span><span class="sxs-lookup"><span data-stu-id="7430c-181">Otherwise, four intermediate alpha values are interpolated between the specified alpha extremes.</span></span> <span data-ttu-id="7430c-182">Os dois valores alfa implícitos adicionais são 0 (totalmente transparente) e 255 (totalmente opaco).</span><span class="sxs-lookup"><span data-stu-id="7430c-182">The two additional implicit alpha values are 0 (fully transparent) and 255 (fully opaque).</span></span>

<span data-ttu-id="7430c-183">O exemplo de código a seguir ilustra esse algoritmo.</span><span class="sxs-lookup"><span data-stu-id="7430c-183">The following code example illustrates this algorithm.</span></span>


```
// 8-alpha or 6-alpha block?    
if (alpha_0 > alpha_1) {    
    // 8-alpha block:  derive the other six alphas.    
    // Bit code 000 = alpha_0, 001 = alpha_1, others are interpolated.
    alpha_2 = (6 * alpha_0 + 1 * alpha_1 + 3) / 7;    // bit code 010
    alpha_3 = (5 * alpha_0 + 2 * alpha_1 + 3) / 7;    // bit code 011
    alpha_4 = (4 * alpha_0 + 3 * alpha_1 + 3) / 7;    // bit code 100
    alpha_5 = (3 * alpha_0 + 4 * alpha_1 + 3) / 7;    // bit code 101
    alpha_6 = (2 * alpha_0 + 5 * alpha_1 + 3) / 7;    // bit code 110
    alpha_7 = (1 * alpha_0 + 6 * alpha_1 + 3) / 7;    // bit code 111  
}    
else {  
    // 6-alpha block.    
    // Bit code 000 = alpha_0, 001 = alpha_1, others are interpolated.
    alpha_2 = (4 * alpha_0 + 1 * alpha_1 + 2) / 5;    // Bit code 010
    alpha_3 = (3 * alpha_0 + 2 * alpha_1 + 2) / 5;    // Bit code 011
    alpha_4 = (2 * alpha_0 + 3 * alpha_1 + 2) / 5;    // Bit code 100
    alpha_5 = (1 * alpha_0 + 4 * alpha_1 + 2) / 5;    // Bit code 101
    alpha_6 = 0;                                      // Bit code 110
    alpha_7 = 255;                                    // Bit code 111
}
```



<span data-ttu-id="7430c-184">O layout da memória do bloco de alfa é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="7430c-184">The memory layout of the alpha block is as follows:</span></span>



| <span data-ttu-id="7430c-185">Byte</span><span class="sxs-lookup"><span data-stu-id="7430c-185">Byte</span></span> | <span data-ttu-id="7430c-186">Alpha</span><span class="sxs-lookup"><span data-stu-id="7430c-186">Alpha</span></span>                                                          |
|------|----------------------------------------------------------------|
| <span data-ttu-id="7430c-187">0</span><span class="sxs-lookup"><span data-stu-id="7430c-187">0</span></span>    | <span data-ttu-id="7430c-188">Alfa \_ 0</span><span class="sxs-lookup"><span data-stu-id="7430c-188">Alpha\_0</span></span>                                                       |
| <span data-ttu-id="7430c-189">1</span><span class="sxs-lookup"><span data-stu-id="7430c-189">1</span></span>    | <span data-ttu-id="7430c-190">Alfa \_ 1</span><span class="sxs-lookup"><span data-stu-id="7430c-190">Alpha\_1</span></span>                                                       |
| <span data-ttu-id="7430c-191">2</span><span class="sxs-lookup"><span data-stu-id="7430c-191">2</span></span>    | <span data-ttu-id="7430c-192">\[0 \] \[ 2 \] (2 MSBs), \[ 0 \] \[ 1 \] , \[ 0 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="7430c-192">\[0\]\[2\] (2 MSBs), \[0\]\[1\], \[0\]\[0\]</span></span>                    |
| <span data-ttu-id="7430c-193">3</span><span class="sxs-lookup"><span data-stu-id="7430c-193">3</span></span>    | <span data-ttu-id="7430c-194">\[1 \] \[ 1 \] (1 MSB), \[ 1 \] \[ 0 \] , \[ 0 \] \[ 3 \] , \[ 0 \] \[ 2 \] (1 LSB)</span><span class="sxs-lookup"><span data-stu-id="7430c-194">\[1\]\[1\] (1 MSB), \[1\]\[0\], \[0\]\[3\], \[0\]\[2\] (1 LSB)</span></span> |
| <span data-ttu-id="7430c-195">4</span><span class="sxs-lookup"><span data-stu-id="7430c-195">4</span></span>    | <span data-ttu-id="7430c-196">\[1 \] \[ 3 \] , \[ 1 \] \[ 2 \] , \[ 1 \] \[ 1 \] (2 LSBs)</span><span class="sxs-lookup"><span data-stu-id="7430c-196">\[1\]\[3\], \[1\]\[2\], \[1\]\[1\] (2 LSBs)</span></span>                    |
| <span data-ttu-id="7430c-197">5</span><span class="sxs-lookup"><span data-stu-id="7430c-197">5</span></span>    | <span data-ttu-id="7430c-198">\[2 \] \[ 2 \] (2 MSBs), \[ 2 \] \[ 1 \] , \[ 2 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="7430c-198">\[2\]\[2\] (2 MSBs), \[2\]\[1\], \[2\]\[0\]</span></span>                    |
| <span data-ttu-id="7430c-199">6</span><span class="sxs-lookup"><span data-stu-id="7430c-199">6</span></span>    | <span data-ttu-id="7430c-200">\[3 \] \[ 1 \] (1 MSB), \[ 3 \] \[ 0 \] , \[ 2 \] \[ 3 \] , \[ 2 \] \[ 2 \] (1 LSB)</span><span class="sxs-lookup"><span data-stu-id="7430c-200">\[3\]\[1\] (1 MSB), \[3\]\[0\], \[2\]\[3\], \[2\]\[2\] (1 LSB)</span></span> |
| <span data-ttu-id="7430c-201">7</span><span class="sxs-lookup"><span data-stu-id="7430c-201">7</span></span>    | <span data-ttu-id="7430c-202">\[3 \] \[ 3 \] , \[ 3 \] \[ 2 \] , \[ 3 \] \[ 1 \] (2 LSBs)</span><span class="sxs-lookup"><span data-stu-id="7430c-202">\[3\]\[3\], \[3\]\[2\], \[3\]\[1\] (2 LSBs)</span></span>                    |



 

<span data-ttu-id="7430c-203">A diferença entre DXT4 e DXT5 é que, no formato DXT4, supõe-se que os dados de cor foram contramultiplicados por alfa.</span><span class="sxs-lookup"><span data-stu-id="7430c-203">The difference between DXT4 and DXT5 is that in the DXT4 format it is assumed that the color data has been premultiplied by alpha.</span></span> <span data-ttu-id="7430c-204">No formato DXT5, presume-se que a cor não seja contramultiplicada por alfa.</span><span class="sxs-lookup"><span data-stu-id="7430c-204">In the DXT5 format, it is assumed the color is not premultiplied by alpha.</span></span> <span data-ttu-id="7430c-205">Esses dois formatos são necessários porque, na maioria dos casos, no momento em que uma textura é usada, apenas examinar os dados não é suficiente para determinar se os valores de cor foram multiplicados por alfa.</span><span class="sxs-lookup"><span data-stu-id="7430c-205">These two formats are needed because, in most cases, by the time a texture is used, just examining the data is not sufficient to determine if the color values have been multiplied by alpha.</span></span> <span data-ttu-id="7430c-206">Como essas informações são necessárias em tempo de execução, os dois códigos FOURCC são usados para diferenciar esses casos.</span><span class="sxs-lookup"><span data-stu-id="7430c-206">Because this information is needed at run time, the two FOURCC codes are used to differentiate these cases.</span></span> <span data-ttu-id="7430c-207">No entanto, os dados e o método de interpolação usados para esses dois formatos são idênticos.</span><span class="sxs-lookup"><span data-stu-id="7430c-207">However, the data and interpolation method used for these two formats is identical.</span></span>

<span data-ttu-id="7430c-208">A comparação de cores usada em DXT1 para determinar se o Texel é transparente não é usado com esses formatos.</span><span class="sxs-lookup"><span data-stu-id="7430c-208">The color compare used in DXT1 to determine if the texel is transparent is not used with these formats.</span></span> <span data-ttu-id="7430c-209">Presume-se que, sem a comparação de cores, os dados de cor sejam sempre tratados como se estivessem modo de 4 cores.</span><span class="sxs-lookup"><span data-stu-id="7430c-209">It is assumed that without the color compare the color data is always treated as if in 4-color mode.</span></span> <span data-ttu-id="7430c-210">Em outras palavras, a instrução If na parte superior do código DXT1 deve ser:</span><span class="sxs-lookup"><span data-stu-id="7430c-210">In other words, the if statement at the top of the DXT1 code should be:</span></span>


```
if ((color_0 > color_1) OR !DXT1) {
```



## <a name="related-topics"></a><span data-ttu-id="7430c-211">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7430c-211">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7430c-212">Recursos de textura compactados</span><span class="sxs-lookup"><span data-stu-id="7430c-212">Compressed Texture Resources</span></span>](compressed-texture-resources.md)
</dt> </dl>

 

 



