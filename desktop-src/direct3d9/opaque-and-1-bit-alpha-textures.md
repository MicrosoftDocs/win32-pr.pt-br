---
description: O formato de textura DXT1 é para texturas que são opacas ou têm uma única cor transparente.
ms.assetid: a890ed0a-1f68-45b8-93cb-b621d1908d9f
title: Texturas opacas e de 1 bit alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f629eff594d28d9a807021c0b9df0bd05ea66c3
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104566823"
---
# <a name="opaque-and-1-bit-alpha-textures-direct3d-9"></a><span data-ttu-id="0efb8-103">Texturas opacas e de 1 bit alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0efb8-103">Opaque and 1-Bit Alpha Textures (Direct3D 9)</span></span>

<span data-ttu-id="0efb8-104">O formato de textura DXT1 é para texturas que são opacas ou têm uma única cor transparente.</span><span class="sxs-lookup"><span data-stu-id="0efb8-104">Texture format DXT1 is for textures that are opaque or have a single transparent color.</span></span>

<span data-ttu-id="0efb8-105">Para cada bloco opaco ou de alfa de 1 bit são armazenados dois valores de 16 bits (formato RGB 5:6:5) e um bitmap de 4 x 4 com 2 bits por pixel.</span><span class="sxs-lookup"><span data-stu-id="0efb8-105">For each opaque or 1-bit alpha block, two 16-bit values (RGB 5:6:5 format) and a 4x4 bitmap with 2 bits per pixel are stored.</span></span> <span data-ttu-id="0efb8-106">Isso resulta em um total de 64 bits de 16 texels ou quatro bits por texel.</span><span class="sxs-lookup"><span data-stu-id="0efb8-106">This totals 64 bits for 16 texels, or four bits per texel.</span></span> <span data-ttu-id="0efb8-107">No bitmap de bloco, há 2 bits por texel para selecionar entre as quatro cores, dois dos quais são armazenados em dados codificados.</span><span class="sxs-lookup"><span data-stu-id="0efb8-107">In the block bitmap, there are 2 bits per texel to select between the four colors, two of which are stored in the encoded data.</span></span> <span data-ttu-id="0efb8-108">As outras duas cores são derivadas dessas cores armazenadas por interpolação linear.</span><span class="sxs-lookup"><span data-stu-id="0efb8-108">The other two colors are derived from these stored colors by linear interpolation.</span></span> <span data-ttu-id="0efb8-109">Esse layout está ilustrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="0efb8-109">This layout is shown in the following diagram.</span></span>

![diagrama do layout de bitmap](images/colors1.png)

<span data-ttu-id="0efb8-111">O formato de alfa de 1 bit é diferenciado do formato opaco ao comparar os dois valores de cor de 16 bits armazenados no bloco.</span><span class="sxs-lookup"><span data-stu-id="0efb8-111">The 1-bit alpha format is distinguished from the opaque format by comparing the two 16-bit color values stored in the block.</span></span> <span data-ttu-id="0efb8-112">Eles são tratados como inteiros não designados.</span><span class="sxs-lookup"><span data-stu-id="0efb8-112">They are treated as unsigned integers.</span></span> <span data-ttu-id="0efb8-113">Se a primeira cor for maior que a segunda, isso significa que somente texels opacos estão definidos.</span><span class="sxs-lookup"><span data-stu-id="0efb8-113">If the first color is greater than the second, it implies that only opaque texels are defined.</span></span> <span data-ttu-id="0efb8-114">Isso significa que as quatro cores são usadas para representar os texels.</span><span class="sxs-lookup"><span data-stu-id="0efb8-114">This means four colors are used to represent the texels.</span></span> <span data-ttu-id="0efb8-115">Na codificação de quatro cores, existem duas cores derivadas e todas as quatro cores são distribuídas igualmente no espaço de cores RGB.</span><span class="sxs-lookup"><span data-stu-id="0efb8-115">In four-color encoding, there are two derived colors and all four colors are equally distributed in RGB color space.</span></span> <span data-ttu-id="0efb8-116">Esse formato é análogo ao RGB 5:6:5.</span><span class="sxs-lookup"><span data-stu-id="0efb8-116">This format is analogous to RGB 5:6:5 format.</span></span> <span data-ttu-id="0efb8-117">Caso contrário, para a transparência alfa de 1 bit, as três cores são usadas e a quarta é reservada para representar texels transparentes.</span><span class="sxs-lookup"><span data-stu-id="0efb8-117">Otherwise, for 1-bit alpha transparency, three colors are used and the fourth is reserved to represent transparent texels.</span></span>

<span data-ttu-id="0efb8-118">Na codificação de três cores, há uma cor derivada e o quarto código de 2 bits é reservado para indicar um texel transparente (informações de alfa).</span><span class="sxs-lookup"><span data-stu-id="0efb8-118">In three-color encoding, there is one derived color and the fourth 2-bit code is reserved to indicate a transparent texel (alpha information).</span></span> <span data-ttu-id="0efb8-119">Esse formato é análogo ao RGBA 5:5:5:1, onde a parte final é usada para codificar a máscara alfa.</span><span class="sxs-lookup"><span data-stu-id="0efb8-119">This format is analogous to RGBA 5:5:5:1, where the final bit is used for encoding the alpha mask.</span></span>

<span data-ttu-id="0efb8-120">O exemplo de código a seguir ilustra o algoritmo para decidir se a codificação de três ou quatro cores está selecionada:</span><span class="sxs-lookup"><span data-stu-id="0efb8-120">The following code example illustrates the algorithm for deciding whether three- or four-color encoding is selected:</span></span>


```
if (color_0 > color_1) 
{
    // Four-color block: derive the other two colors.    
    // 00 = color_0, 01 = color_1, 10 = color_2, 11 = color_3
    // These 2-bit codes correspond to the 2-bit fields 
    // stored in the 64-bit block.
    color_2 = (2 * color_0 + color_1 + 1) / 3;
    color_3 = (color_0 + 2 * color_1 + 1) / 3;
}    
else
{ 
    // Three-color block: derive the other color.
    // 00 = color_0,  01 = color_1,  10 = color_2,  
    // 11 = transparent.
    // These 2-bit codes correspond to the 2-bit fields 
    // stored in the 64-bit block. 
    color_2 = (color_0 + color_1) / 2;    
    color_3 = transparent;    

}
```



<span data-ttu-id="0efb8-121">É recomendável que você defina os componentes RGBA do pixel transparência como zero antes da mesclagem.</span><span class="sxs-lookup"><span data-stu-id="0efb8-121">It is recommended that you set the RGBA components of the transparency pixel to zero before blending.</span></span>

<span data-ttu-id="0efb8-122">As tabelas a seguir mostram o layout de memória para o bloco de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="0efb8-122">The following tables show the memory layout for the 8-byte block.</span></span> <span data-ttu-id="0efb8-123">Presume-se que o primeiro índice corresponde à coordenada y e o segundo à coordenada x.</span><span class="sxs-lookup"><span data-stu-id="0efb8-123">It is assumed that the first index corresponds to the y-coordinate and the second corresponds to the x-coordinate.</span></span> <span data-ttu-id="0efb8-124">Por exemplo, Texel \[ 1 \] \[ 2 \] refere-se ao mapa de textura pixel em (x, y) = (2, 1).</span><span class="sxs-lookup"><span data-stu-id="0efb8-124">For example, Texel\[1\]\[2\] refers to the texture map pixel at (x,y) = (2,1).</span></span>

<span data-ttu-id="0efb8-125">Esta tabela contém o layout de memória para o bloco de 8 bytes (64 bits).</span><span class="sxs-lookup"><span data-stu-id="0efb8-125">This table contains the memory layout for the 8-byte (64-bit) block.</span></span>



| <span data-ttu-id="0efb8-126">Endereço da palavra</span><span class="sxs-lookup"><span data-stu-id="0efb8-126">Word address</span></span> | <span data-ttu-id="0efb8-127">palavra de 16 bits</span><span class="sxs-lookup"><span data-stu-id="0efb8-127">16-bit word</span></span>    |
|--------------|----------------|
| <span data-ttu-id="0efb8-128">0</span><span class="sxs-lookup"><span data-stu-id="0efb8-128">0</span></span>            | <span data-ttu-id="0efb8-129">Cor \_ 0</span><span class="sxs-lookup"><span data-stu-id="0efb8-129">Color\_0</span></span>       |
| <span data-ttu-id="0efb8-130">1</span><span class="sxs-lookup"><span data-stu-id="0efb8-130">1</span></span>            | <span data-ttu-id="0efb8-131">Cor \_ 1</span><span class="sxs-lookup"><span data-stu-id="0efb8-131">Color\_1</span></span>       |
| <span data-ttu-id="0efb8-132">2</span><span class="sxs-lookup"><span data-stu-id="0efb8-132">2</span></span>            | <span data-ttu-id="0efb8-133">Bitmap de palavra \_ 0</span><span class="sxs-lookup"><span data-stu-id="0efb8-133">Bitmap Word\_0</span></span> |
| <span data-ttu-id="0efb8-134">3</span><span class="sxs-lookup"><span data-stu-id="0efb8-134">3</span></span>            | <span data-ttu-id="0efb8-135">Texto de bitmap \_ 1</span><span class="sxs-lookup"><span data-stu-id="0efb8-135">Bitmap Word\_1</span></span> |



 

<span data-ttu-id="0efb8-136">Cor \_ 0 e cor \_ 1, as cores nos dois extremos são dispostos da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="0efb8-136">Color\_0 and Color\_1, the colors at the two extremes, are laid out as follows:</span></span>



| <span data-ttu-id="0efb8-137">Bits</span><span class="sxs-lookup"><span data-stu-id="0efb8-137">Bits</span></span>        | <span data-ttu-id="0efb8-138">Cor</span><span class="sxs-lookup"><span data-stu-id="0efb8-138">Color</span></span>                 |
|-------------|-----------------------|
| <span data-ttu-id="0efb8-139">4:0 (LSB \* )</span><span class="sxs-lookup"><span data-stu-id="0efb8-139">4:0 (LSB\*)</span></span> | <span data-ttu-id="0efb8-140">Componente de cor azul</span><span class="sxs-lookup"><span data-stu-id="0efb8-140">Blue color component</span></span>  |
| <span data-ttu-id="0efb8-141">10:5</span><span class="sxs-lookup"><span data-stu-id="0efb8-141">10:5</span></span>        | <span data-ttu-id="0efb8-142">Componente de cor verde</span><span class="sxs-lookup"><span data-stu-id="0efb8-142">Green color component</span></span> |
| <span data-ttu-id="0efb8-143">15:11</span><span class="sxs-lookup"><span data-stu-id="0efb8-143">15:11</span></span>       | <span data-ttu-id="0efb8-144">Componente de cor vermelha</span><span class="sxs-lookup"><span data-stu-id="0efb8-144">Red color component</span></span>   |



 

<span data-ttu-id="0efb8-145">\*bit menos significativo</span><span class="sxs-lookup"><span data-stu-id="0efb8-145">\*least-significant bit</span></span>

<span data-ttu-id="0efb8-146">O bitmap Word \_ 0 é apresentado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="0efb8-146">Bitmap Word\_0 is laid out as follows:</span></span>



| <span data-ttu-id="0efb8-147">Bits</span><span class="sxs-lookup"><span data-stu-id="0efb8-147">Bits</span></span>          | <span data-ttu-id="0efb8-148">Texel</span><span class="sxs-lookup"><span data-stu-id="0efb8-148">Texel</span></span>           |
|---------------|-----------------|
| <span data-ttu-id="0efb8-149">1:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="0efb8-149">1:0 (LSB)</span></span>     | <span data-ttu-id="0efb8-150">Texel \[ 0 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="0efb8-150">Texel\[0\]\[0\]</span></span> |
| <span data-ttu-id="0efb8-151">3:2</span><span class="sxs-lookup"><span data-stu-id="0efb8-151">3:2</span></span>           | <span data-ttu-id="0efb8-152">Texel \[ 0 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="0efb8-152">Texel\[0\]\[1\]</span></span> |
| <span data-ttu-id="0efb8-153">5:4</span><span class="sxs-lookup"><span data-stu-id="0efb8-153">5:4</span></span>           | <span data-ttu-id="0efb8-154">Texel \[ 0 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="0efb8-154">Texel\[0\]\[2\]</span></span> |
| <span data-ttu-id="0efb8-155">7:6</span><span class="sxs-lookup"><span data-stu-id="0efb8-155">7:6</span></span>           | <span data-ttu-id="0efb8-156">Texel \[ 0 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="0efb8-156">Texel\[0\]\[3\]</span></span> |
| <span data-ttu-id="0efb8-157">9:8</span><span class="sxs-lookup"><span data-stu-id="0efb8-157">9:8</span></span>           | <span data-ttu-id="0efb8-158">Texel \[ 1 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="0efb8-158">Texel\[1\]\[0\]</span></span> |
| <span data-ttu-id="0efb8-159">11:10</span><span class="sxs-lookup"><span data-stu-id="0efb8-159">11:10</span></span>         | <span data-ttu-id="0efb8-160">Texel \[ 1 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="0efb8-160">Texel\[1\]\[1\]</span></span> |
| <span data-ttu-id="0efb8-161">13:12</span><span class="sxs-lookup"><span data-stu-id="0efb8-161">13:12</span></span>         | <span data-ttu-id="0efb8-162">Texel \[ 1 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="0efb8-162">Texel\[1\]\[2\]</span></span> |
| <span data-ttu-id="0efb8-163">15:14 (MSB \* )</span><span class="sxs-lookup"><span data-stu-id="0efb8-163">15:14 (MSB\*)</span></span> | <span data-ttu-id="0efb8-164">Texel \[ 1 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="0efb8-164">Texel\[1\]\[3\]</span></span> |



 

<span data-ttu-id="0efb8-165">\*bit mais significativo (MSB)</span><span class="sxs-lookup"><span data-stu-id="0efb8-165">\*most significant bit (MSB)</span></span>

<span data-ttu-id="0efb8-166">O bitmap Word \_ 1 é apresentado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="0efb8-166">Bitmap Word\_1 is laid out as follows:</span></span>



| <span data-ttu-id="0efb8-167">Bits</span><span class="sxs-lookup"><span data-stu-id="0efb8-167">Bits</span></span>        | <span data-ttu-id="0efb8-168">Texel</span><span class="sxs-lookup"><span data-stu-id="0efb8-168">Texel</span></span>           |
|-------------|-----------------|
| <span data-ttu-id="0efb8-169">1:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="0efb8-169">1:0 (LSB)</span></span>   | <span data-ttu-id="0efb8-170">Texel \[ 2 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="0efb8-170">Texel\[2\]\[0\]</span></span> |
| <span data-ttu-id="0efb8-171">3:2</span><span class="sxs-lookup"><span data-stu-id="0efb8-171">3:2</span></span>         | <span data-ttu-id="0efb8-172">Texel \[ 2 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="0efb8-172">Texel\[2\]\[1\]</span></span> |
| <span data-ttu-id="0efb8-173">5:4</span><span class="sxs-lookup"><span data-stu-id="0efb8-173">5:4</span></span>         | <span data-ttu-id="0efb8-174">Texel \[ 2 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="0efb8-174">Texel\[2\]\[2\]</span></span> |
| <span data-ttu-id="0efb8-175">7:6</span><span class="sxs-lookup"><span data-stu-id="0efb8-175">7:6</span></span>         | <span data-ttu-id="0efb8-176">Texel \[ 2 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="0efb8-176">Texel\[2\]\[3\]</span></span> |
| <span data-ttu-id="0efb8-177">9:8</span><span class="sxs-lookup"><span data-stu-id="0efb8-177">9:8</span></span>         | <span data-ttu-id="0efb8-178">Texel \[ 3 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="0efb8-178">Texel\[3\]\[0\]</span></span> |
| <span data-ttu-id="0efb8-179">11:10</span><span class="sxs-lookup"><span data-stu-id="0efb8-179">11:10</span></span>       | <span data-ttu-id="0efb8-180">Texel \[ 3 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="0efb8-180">Texel\[3\]\[1\]</span></span> |
| <span data-ttu-id="0efb8-181">13:12</span><span class="sxs-lookup"><span data-stu-id="0efb8-181">13:12</span></span>       | <span data-ttu-id="0efb8-182">Texel \[ 3 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="0efb8-182">Texel\[3\]\[2\]</span></span> |
| <span data-ttu-id="0efb8-183">15:14 (MSB)</span><span class="sxs-lookup"><span data-stu-id="0efb8-183">15:14 (MSB)</span></span> | <span data-ttu-id="0efb8-184">Texel \[ 3 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="0efb8-184">Texel\[3\]\[3\]</span></span> |



 

## <a name="example-of-opaque-color-encoding"></a><span data-ttu-id="0efb8-185">Exemplo de codificação de cor opaca</span><span class="sxs-lookup"><span data-stu-id="0efb8-185">Example of Opaque Color Encoding</span></span>

<span data-ttu-id="0efb8-186">Como um exemplo de codificação opaca, considere que as cores vermelho e preto são os extremos.</span><span class="sxs-lookup"><span data-stu-id="0efb8-186">As an example of opaque encoding, assume that the colors red and black are at the extremes.</span></span> <span data-ttu-id="0efb8-187">Vermelho é cor \_ 0 e preto é a cor \_ 1.</span><span class="sxs-lookup"><span data-stu-id="0efb8-187">Red is color\_0, and black is color\_1.</span></span> <span data-ttu-id="0efb8-188">Existem quatro cores interpoladas que formam o gradiente distribuído uniformemente entre elas.</span><span class="sxs-lookup"><span data-stu-id="0efb8-188">There are four interpolated colors that form the uniformly distributed gradient between them.</span></span> <span data-ttu-id="0efb8-189">Para determinar os valores do bitmap de 4 x 4, os seguintes cálculos são usados:</span><span class="sxs-lookup"><span data-stu-id="0efb8-189">To determine the values for the 4x4 bitmap, the following calculations are used:</span></span>


```
00 ? color_0
01 ? color_1
10 ? 2/3 color_0 + 1/3 color_1
11 ? 1/3 color_0 + 2/3 color_1
```



<span data-ttu-id="0efb8-190">Em seguida, o bitmap se parece com o diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="0efb8-190">The bitmap then looks like the following diagram.</span></span>

![Diagrama que mostra o layout de bitmap expandido.](images/colors2.png)

<span data-ttu-id="0efb8-192">Isso é semelhante à seguinte série ilustrada de cores.</span><span class="sxs-lookup"><span data-stu-id="0efb8-192">This looks like the following illustrated series of colors.</span></span>

> [!Note]  
> <span data-ttu-id="0efb8-193">Em uma imagem, pixel (0, 0) aparece na parte superior esquerda.</span><span class="sxs-lookup"><span data-stu-id="0efb8-193">In an image, pixel (0,0) appears on the top left.</span></span>

 

![ilustração de um gradiente codificado opaco](images/redsquares.png)

## <a name="example-of-1-bit-alpha-encoding"></a><span data-ttu-id="0efb8-195">Exemplo de codificação alfa de 1 bit</span><span class="sxs-lookup"><span data-stu-id="0efb8-195">Example of 1-Bit Alpha Encoding</span></span>

<span data-ttu-id="0efb8-196">Esse formato é selecionado quando o inteiro de 16 bits não atribuído, cor \_ 0, é menor que o inteiro de 16 bits não assinado, cor \_ 1.</span><span class="sxs-lookup"><span data-stu-id="0efb8-196">This format is selected when the unsigned 16-bit integer, color\_0, is less than the unsigned 16-bit integer, color\_1.</span></span> <span data-ttu-id="0efb8-197">Um exemplo de onde esse formato pode ser usado é em folhas em uma árvore, mostrado em comparação a um céu azul.</span><span class="sxs-lookup"><span data-stu-id="0efb8-197">An example of where this format can be used is leaves on a tree, shown against a blue sky.</span></span> <span data-ttu-id="0efb8-198">Alguns texels pode ser marcados como transparentes enquanto três tons de verde ainda estão disponíveis para as folhas.</span><span class="sxs-lookup"><span data-stu-id="0efb8-198">Some texels can be marked as transparent while three shades of green are still available for the leaves.</span></span> <span data-ttu-id="0efb8-199">Duas cores corrigem os extremos e a terceira é uma cor interpolada.</span><span class="sxs-lookup"><span data-stu-id="0efb8-199">Two colors fix the extremes, and the third is an interpolated color.</span></span>

<span data-ttu-id="0efb8-200">A ilustração a seguir é um exemplo dessa imagem.</span><span class="sxs-lookup"><span data-stu-id="0efb8-200">The following illustration is an example of such a picture.</span></span>

![ilustração de codificação alfa de 1 bit](images/greenthing.png)

<span data-ttu-id="0efb8-202">Observe que, onde a imagem é mostrada como branco, o Texel seria codificado como transparente.</span><span class="sxs-lookup"><span data-stu-id="0efb8-202">Note that where the image is shown as white, the texel would be encoded as transparent.</span></span> <span data-ttu-id="0efb8-203">Observe também que os componentes RGBA do texels transparente devem ser definidos como zero antes da mesclagem.</span><span class="sxs-lookup"><span data-stu-id="0efb8-203">Also note that the RGBA components of the transparent texels should be set to zero before blending.</span></span>

<span data-ttu-id="0efb8-204">A codificação de bitmap para as cores e a transparência é determinada usando os seguintes cálculos.</span><span class="sxs-lookup"><span data-stu-id="0efb8-204">The bitmap encoding for the colors and the transparency is determined using the following calculations.</span></span>


```
00 ? color_0
01 ? color_1
10 ? 1/2 color_0 + 1/2 color_1
11   ?   Transparent
```



<span data-ttu-id="0efb8-205">Em seguida, o bitmap se parece com o diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="0efb8-205">The bitmap then looks like the following diagram.</span></span>

![diagrama do layout expandido do bitmap](images/colors3.png)

## <a name="related-topics"></a><span data-ttu-id="0efb8-207">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0efb8-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0efb8-208">Recursos de textura compactados</span><span class="sxs-lookup"><span data-stu-id="0efb8-208">Compressed Texture Resources</span></span>](compressed-texture-resources.md)
</dt> </dl>

 

 



