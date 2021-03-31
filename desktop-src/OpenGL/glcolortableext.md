---
title: função glColorTableEXT (GL. h)
description: A função glColorTableEXT especifica o formato e o tamanho de uma paleta para texturas de paletas de destino.
ms.assetid: f3d7b1a1-97a5-47ef-a0ca-5e58acb86bb4
keywords:
- função glColorTableEXT OpenGL
topic_type:
- apiref
api_name:
- glColorTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd0d5fd5c848e787f480e3e1893b9b25e4bbd3de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644827"
---
# <a name="glcolortableext-function"></a><span data-ttu-id="5c9bb-104">função glColorTableEXT</span><span class="sxs-lookup"><span data-stu-id="5c9bb-104">glColorTableEXT function</span></span>

<span data-ttu-id="5c9bb-105">A função **glColorTableEXT** especifica o formato e o tamanho de uma paleta para texturas de paletas de destino.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-105">The **glColorTableEXT** function specifies the format and size of a palette for targeted paletted textures.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c9bb-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5c9bb-106">Syntax</span></span>


```C++
void WINAPI glColorTableEXT(
         GLenum  target,
         GLenum  internalFormat,
         GLsizei width,
         GLenum  format,
         GLenum  type,
   const GLvoid  *data
);
```



## <a name="parameters"></a><span data-ttu-id="5c9bb-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5c9bb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c9bb-108">*destino*</span><span class="sxs-lookup"><span data-stu-id="5c9bb-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="5c9bb-109">A textura de destino que deve ter sua paleta alterada.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-109">The target texture that is to have its palette changed.</span></span> <span data-ttu-id="5c9bb-110">Deve ser a textura \_ 1D, a textura \_ 2D, a \_ textura \_ de proxy 1D ou a textura de proxy \_ \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-110">Must be TEXTURE\_1D, TEXTURE\_2D, PROXY\_TEXTURE\_1D, or PROXY\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="5c9bb-111">*internalFormat*</span><span class="sxs-lookup"><span data-stu-id="5c9bb-111">*internalFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="5c9bb-112">O formato interno e a resolução da paleta.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-112">The internal format and resolution of the palette.</span></span> <span data-ttu-id="5c9bb-113">Esse parâmetro pode assumir um dos seguintes valores simbólicos.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-113">This parameter can assume one of the following symbolic values.</span></span>



| <span data-ttu-id="5c9bb-114">Constante</span><span class="sxs-lookup"><span data-stu-id="5c9bb-114">Constant</span></span>       | <span data-ttu-id="5c9bb-115">Formato base</span><span class="sxs-lookup"><span data-stu-id="5c9bb-115">Base Format</span></span> | <span data-ttu-id="5c9bb-116">Bits de R</span><span class="sxs-lookup"><span data-stu-id="5c9bb-116">R Bits</span></span> | <span data-ttu-id="5c9bb-117">G bits</span><span class="sxs-lookup"><span data-stu-id="5c9bb-117">G Bits</span></span> | <span data-ttu-id="5c9bb-118">Bits B</span><span class="sxs-lookup"><span data-stu-id="5c9bb-118">B Bits</span></span> | <span data-ttu-id="5c9bb-119">Um bits</span><span class="sxs-lookup"><span data-stu-id="5c9bb-119">A Bits</span></span> |
|----------------|-------------|--------|--------|--------|--------|
| <span data-ttu-id="5c9bb-120">GL \_ R3 \_ G3 \_ B2</span><span class="sxs-lookup"><span data-stu-id="5c9bb-120">GL\_R3\_G3\_B2</span></span> | <span data-ttu-id="5c9bb-121">GL em \_ RGB</span><span class="sxs-lookup"><span data-stu-id="5c9bb-121">GL\_RGB</span></span>     | <span data-ttu-id="5c9bb-122">3</span><span class="sxs-lookup"><span data-stu-id="5c9bb-122">3</span></span>      | <span data-ttu-id="5c9bb-123">3</span><span class="sxs-lookup"><span data-stu-id="5c9bb-123">3</span></span>      | <span data-ttu-id="5c9bb-124">2</span><span class="sxs-lookup"><span data-stu-id="5c9bb-124">2</span></span>      |        |
| <span data-ttu-id="5c9bb-125">\_RGB4 GL</span><span class="sxs-lookup"><span data-stu-id="5c9bb-125">GL\_RGB4</span></span>       | <span data-ttu-id="5c9bb-126">GL em \_ RGB</span><span class="sxs-lookup"><span data-stu-id="5c9bb-126">GL\_RGB</span></span>     | <span data-ttu-id="5c9bb-127">4</span><span class="sxs-lookup"><span data-stu-id="5c9bb-127">4</span></span>      | <span data-ttu-id="5c9bb-128">4</span><span class="sxs-lookup"><span data-stu-id="5c9bb-128">4</span></span>      | <span data-ttu-id="5c9bb-129">4</span><span class="sxs-lookup"><span data-stu-id="5c9bb-129">4</span></span>      |        |
| <span data-ttu-id="5c9bb-130">\_RGB5 GL</span><span class="sxs-lookup"><span data-stu-id="5c9bb-130">GL\_RGB5</span></span>       | <span data-ttu-id="5c9bb-131">GL em \_ RGB</span><span class="sxs-lookup"><span data-stu-id="5c9bb-131">GL\_RGB</span></span>     | <span data-ttu-id="5c9bb-132">5</span><span class="sxs-lookup"><span data-stu-id="5c9bb-132">5</span></span>      | <span data-ttu-id="5c9bb-133">5</span><span class="sxs-lookup"><span data-stu-id="5c9bb-133">5</span></span>      | <span data-ttu-id="5c9bb-134">5</span><span class="sxs-lookup"><span data-stu-id="5c9bb-134">5</span></span>      |        |
| <span data-ttu-id="5c9bb-135">\_RGB8 GL</span><span class="sxs-lookup"><span data-stu-id="5c9bb-135">GL\_RGB8</span></span>       | <span data-ttu-id="5c9bb-136">GL em \_ RGB</span><span class="sxs-lookup"><span data-stu-id="5c9bb-136">GL\_RGB</span></span>     | <span data-ttu-id="5c9bb-137">8</span><span class="sxs-lookup"><span data-stu-id="5c9bb-137">8</span></span>      | <span data-ttu-id="5c9bb-138">8</span><span class="sxs-lookup"><span data-stu-id="5c9bb-138">8</span></span>      | <span data-ttu-id="5c9bb-139">8</span><span class="sxs-lookup"><span data-stu-id="5c9bb-139">8</span></span>      |        |
| <span data-ttu-id="5c9bb-140">\_RGB10 GL</span><span class="sxs-lookup"><span data-stu-id="5c9bb-140">GL\_RGB10</span></span>      | <span data-ttu-id="5c9bb-141">GL em \_ RGB</span><span class="sxs-lookup"><span data-stu-id="5c9bb-141">GL\_RGB</span></span>     | <span data-ttu-id="5c9bb-142">10</span><span class="sxs-lookup"><span data-stu-id="5c9bb-142">10</span></span>     | <span data-ttu-id="5c9bb-143">10</span><span class="sxs-lookup"><span data-stu-id="5c9bb-143">10</span></span>     | <span data-ttu-id="5c9bb-144">10</span><span class="sxs-lookup"><span data-stu-id="5c9bb-144">10</span></span>     |        |
| <span data-ttu-id="5c9bb-145">\_RGB12 GL</span><span class="sxs-lookup"><span data-stu-id="5c9bb-145">GL\_RGB12</span></span>      | <span data-ttu-id="5c9bb-146">GL em \_ RGB</span><span class="sxs-lookup"><span data-stu-id="5c9bb-146">GL\_RGB</span></span>     | <span data-ttu-id="5c9bb-147">12</span><span class="sxs-lookup"><span data-stu-id="5c9bb-147">12</span></span>     | <span data-ttu-id="5c9bb-148">12</span><span class="sxs-lookup"><span data-stu-id="5c9bb-148">12</span></span>     | <span data-ttu-id="5c9bb-149">12</span><span class="sxs-lookup"><span data-stu-id="5c9bb-149">12</span></span>     |        |
| <span data-ttu-id="5c9bb-150">\_RGB16 GL</span><span class="sxs-lookup"><span data-stu-id="5c9bb-150">GL\_RGB16</span></span>      | <span data-ttu-id="5c9bb-151">GL em \_ RGB</span><span class="sxs-lookup"><span data-stu-id="5c9bb-151">GL\_RGB</span></span>     | <span data-ttu-id="5c9bb-152">16</span><span class="sxs-lookup"><span data-stu-id="5c9bb-152">16</span></span>     | <span data-ttu-id="5c9bb-153">16</span><span class="sxs-lookup"><span data-stu-id="5c9bb-153">16</span></span>     | <span data-ttu-id="5c9bb-154">16</span><span class="sxs-lookup"><span data-stu-id="5c9bb-154">16</span></span>     |        |
| <span data-ttu-id="5c9bb-155">\_RGBA2 GL</span><span class="sxs-lookup"><span data-stu-id="5c9bb-155">GL\_RGBA2</span></span>      | <span data-ttu-id="5c9bb-156">Se \_ RGBA</span><span class="sxs-lookup"><span data-stu-id="5c9bb-156">GL\_RGBA</span></span>    | <span data-ttu-id="5c9bb-157">2</span><span class="sxs-lookup"><span data-stu-id="5c9bb-157">2</span></span>      | <span data-ttu-id="5c9bb-158">2</span><span class="sxs-lookup"><span data-stu-id="5c9bb-158">2</span></span>      | <span data-ttu-id="5c9bb-159">2</span><span class="sxs-lookup"><span data-stu-id="5c9bb-159">2</span></span>      | <span data-ttu-id="5c9bb-160">2</span><span class="sxs-lookup"><span data-stu-id="5c9bb-160">2</span></span>      |
| <span data-ttu-id="5c9bb-161">\_RGBA4 GL</span><span class="sxs-lookup"><span data-stu-id="5c9bb-161">GL\_RGBA4</span></span>      | <span data-ttu-id="5c9bb-162">Se \_ RGBA</span><span class="sxs-lookup"><span data-stu-id="5c9bb-162">GL\_RGBA</span></span>    | <span data-ttu-id="5c9bb-163">4</span><span class="sxs-lookup"><span data-stu-id="5c9bb-163">4</span></span>      | <span data-ttu-id="5c9bb-164">4</span><span class="sxs-lookup"><span data-stu-id="5c9bb-164">4</span></span>      | <span data-ttu-id="5c9bb-165">4</span><span class="sxs-lookup"><span data-stu-id="5c9bb-165">4</span></span>      | <span data-ttu-id="5c9bb-166">4</span><span class="sxs-lookup"><span data-stu-id="5c9bb-166">4</span></span>      |
| <span data-ttu-id="5c9bb-167">GL \_ RGB5 \_ a1</span><span class="sxs-lookup"><span data-stu-id="5c9bb-167">GL\_RGB5\_A1</span></span>   | <span data-ttu-id="5c9bb-168">Se \_ RGBA</span><span class="sxs-lookup"><span data-stu-id="5c9bb-168">GL\_RGBA</span></span>    | <span data-ttu-id="5c9bb-169">5</span><span class="sxs-lookup"><span data-stu-id="5c9bb-169">5</span></span>      | <span data-ttu-id="5c9bb-170">5</span><span class="sxs-lookup"><span data-stu-id="5c9bb-170">5</span></span>      | <span data-ttu-id="5c9bb-171">5</span><span class="sxs-lookup"><span data-stu-id="5c9bb-171">5</span></span>      | <span data-ttu-id="5c9bb-172">1</span><span class="sxs-lookup"><span data-stu-id="5c9bb-172">1</span></span>      |
| <span data-ttu-id="5c9bb-173">\_RGBA8 GL</span><span class="sxs-lookup"><span data-stu-id="5c9bb-173">GL\_RGBA8</span></span>      | <span data-ttu-id="5c9bb-174">Se \_ RGBA</span><span class="sxs-lookup"><span data-stu-id="5c9bb-174">GL\_RGBA</span></span>    | <span data-ttu-id="5c9bb-175">8</span><span class="sxs-lookup"><span data-stu-id="5c9bb-175">8</span></span>      | <span data-ttu-id="5c9bb-176">8</span><span class="sxs-lookup"><span data-stu-id="5c9bb-176">8</span></span>      | <span data-ttu-id="5c9bb-177">8</span><span class="sxs-lookup"><span data-stu-id="5c9bb-177">8</span></span>      | <span data-ttu-id="5c9bb-178">8</span><span class="sxs-lookup"><span data-stu-id="5c9bb-178">8</span></span>      |
| <span data-ttu-id="5c9bb-179">GL \_ RG10 \_ a2</span><span class="sxs-lookup"><span data-stu-id="5c9bb-179">GL\_RG10\_A2</span></span>   | <span data-ttu-id="5c9bb-180">Se \_ RGBA</span><span class="sxs-lookup"><span data-stu-id="5c9bb-180">GL\_RGBA</span></span>    | <span data-ttu-id="5c9bb-181">10</span><span class="sxs-lookup"><span data-stu-id="5c9bb-181">10</span></span>     | <span data-ttu-id="5c9bb-182">10</span><span class="sxs-lookup"><span data-stu-id="5c9bb-182">10</span></span>     | <span data-ttu-id="5c9bb-183">10</span><span class="sxs-lookup"><span data-stu-id="5c9bb-183">10</span></span>     | <span data-ttu-id="5c9bb-184">2</span><span class="sxs-lookup"><span data-stu-id="5c9bb-184">2</span></span>      |
| <span data-ttu-id="5c9bb-185">\_RGB12 GL</span><span class="sxs-lookup"><span data-stu-id="5c9bb-185">GL\_RGB12</span></span>      | <span data-ttu-id="5c9bb-186">Se \_ RGBA</span><span class="sxs-lookup"><span data-stu-id="5c9bb-186">GL\_RGBA</span></span>    | <span data-ttu-id="5c9bb-187">12</span><span class="sxs-lookup"><span data-stu-id="5c9bb-187">12</span></span>     | <span data-ttu-id="5c9bb-188">12</span><span class="sxs-lookup"><span data-stu-id="5c9bb-188">12</span></span>     | <span data-ttu-id="5c9bb-189">12</span><span class="sxs-lookup"><span data-stu-id="5c9bb-189">12</span></span>     | <span data-ttu-id="5c9bb-190">12</span><span class="sxs-lookup"><span data-stu-id="5c9bb-190">12</span></span>     |
| <span data-ttu-id="5c9bb-191">\_RGBA16 GL</span><span class="sxs-lookup"><span data-stu-id="5c9bb-191">GL\_RGBA16</span></span>     | <span data-ttu-id="5c9bb-192">Se \_ RGBA</span><span class="sxs-lookup"><span data-stu-id="5c9bb-192">GL\_RGBA</span></span>    | <span data-ttu-id="5c9bb-193">16</span><span class="sxs-lookup"><span data-stu-id="5c9bb-193">16</span></span>     | <span data-ttu-id="5c9bb-194">16</span><span class="sxs-lookup"><span data-stu-id="5c9bb-194">16</span></span>     | <span data-ttu-id="5c9bb-195">16</span><span class="sxs-lookup"><span data-stu-id="5c9bb-195">16</span></span>     | <span data-ttu-id="5c9bb-196">16</span><span class="sxs-lookup"><span data-stu-id="5c9bb-196">16</span></span>     |



 

</dd> <dt>

<span data-ttu-id="5c9bb-197">*width*</span><span class="sxs-lookup"><span data-stu-id="5c9bb-197">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="5c9bb-198">O tamanho da paleta.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-198">The size of the palette.</span></span> <span data-ttu-id="5c9bb-199">Deve ser 2n = 1 para um inteiro *n*.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-199">Must be 2n = 1 for some integer *n*.</span></span>

</dd> <dt>

<span data-ttu-id="5c9bb-200">*format*</span><span class="sxs-lookup"><span data-stu-id="5c9bb-200">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="5c9bb-201">O formato dos dados de pixel.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-201">The format of the pixel data.</span></span> <span data-ttu-id="5c9bb-202">As constantes simbólicas a seguir são aceitas.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-202">The following symbolic constants are accepted.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5c9bb-203">Valor</span><span class="sxs-lookup"><span data-stu-id="5c9bb-203">Value</span></span></th>
<th><span data-ttu-id="5c9bb-204">Significado</span><span class="sxs-lookup"><span data-stu-id="5c9bb-204">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="5c9bb-205"><dt><strong>GL_RGBA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5c9bb-205"><dt><strong>GL_RGBA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="5c9bb-206">Cada pixel é um grupo de quatro componentes nesta ordem: vermelho, verde, azul, alfa.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-206">Each pixel is a group of four components in this order: red, green, blue, alpha.</span></span> <span data-ttu-id="5c9bb-207">O formato RGBA é determinado dessa maneira:</span><span class="sxs-lookup"><span data-stu-id="5c9bb-207">The RGBA format is determined in this way:</span></span> <br/>
<ol>
<li><span data-ttu-id="5c9bb-208">A função <strong>glColorTableEXT</strong> converte valores de ponto flutuante diretamente em um formato interno com precisão não especificada.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-208">The <strong>glColorTableEXT</strong> function converts floating-point values directly to an internal format with unspecified precision.</span></span> <span data-ttu-id="5c9bb-209">Valores inteiros assinados são mapeados linearmente para o formato interno, de modo que o valor inteiro representável mais positivo seja mapeado para 1,0 e o valor inteiro reapresentável mais negativo seja mapeado para-1,0.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-209">Signed integer values are mapped linearly to the internal format such that the most positive representable integer value maps to 1.0, and the most negative representable integer value maps to -1.0.</span></span> <span data-ttu-id="5c9bb-210">Os dados inteiros não assinados são mapeados da mesma forma: o maior valor inteiro é mapeado para 1,0 e zero é mapeado para 0,0.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-210">Unsigned integer data is mapped similarly: the largest integer value maps to 1.0, and zero maps to 0.0.</span></span></li>
<li><span data-ttu-id="5c9bb-211">A função <strong>glColorTableEXT</strong> multiplica os valores de cor resultantes por GL_c_SCALE e os adiciona ao GL_c_BIAS, em que <em>c</em> é vermelho, verde, azul e alfa para os respectivos componentes de cor.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-211">The <strong>glColorTableEXT</strong> function multiplies the resulting color values by GL_c_SCALE and adds them to GL_c_BIAS, where <em>c</em> is RED, GREEN, BLUE, and ALPHA for the respective color components.</span></span> <span data-ttu-id="5c9bb-212">Os resultados são clamped para o intervalo [0, 1].</span><span class="sxs-lookup"><span data-stu-id="5c9bb-212">The results are clamped to the range [0,1].</span></span></li>
<li><span data-ttu-id="5c9bb-213">Se GL_MAP_COLOR for <strong>true</strong>, <strong>glColorTableEXT</strong> dimensionará cada componente de cor pelo tamanho da tabela de pesquisa GL_PIXEL_MAP_c_TO_c e, em seguida, substituirá o componente pelo valor que ele faz referência a essa tabela; <em>c</em> é R, G, B ou A, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-213">If GL_MAP_COLOR is <strong>TRUE</strong>, <strong>glColorTableEXT</strong> scales each color component by the size of lookup table GL_PIXEL_MAP_c_TO_c, then replaces the component by the value that it references in that table; <em>c</em> is R, G, B, or A, respectively.</span></span></li>
<li><span data-ttu-id="5c9bb-214">A função <strong>glColorTableEXT</strong> converte as cores de RGBA resultantes em fragmentos anexando as coordenadas de coordenadas <em>z</em>e de textura atuais a cada pixel e, em seguida, atribuindo coordenadas de janela <em>x</em> e <em>y</em> ao <em>n</em>º de fragmento como<em>x</em>?</span><span class="sxs-lookup"><span data-stu-id="5c9bb-214">The <strong>glColorTableEXT</strong> function converts the resulting RGBA colors to fragments by attaching the current raster position <em>z</em>-coordinate and texture coordinates to each pixel, then assigning <em>x</em> and <em>y</em> window coordinates to the <em>n</em>th fragment such that<em>x</em>?</span></span><span data-ttu-id="5c9bb-215"> = <em>largura</em> <em>x</em><sub>r</sub> + <em>n</em> mod</span><span class="sxs-lookup"><span data-stu-id="5c9bb-215"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>width</em></span></span><br/> <span data-ttu-id="5c9bb-216"><em></em>Iar?</span><span class="sxs-lookup"><span data-stu-id="5c9bb-216"><em></em>y?</span></span><span data-ttu-id="5c9bb-217"> = <em>y</em><sub>r</sub> +<em>n/largura</em></span><span class="sxs-lookup"><span data-stu-id="5c9bb-217"> = <em>y</em><sub>r</sub> +<em>n / width</em></span></span><br/> <span data-ttu-id="5c9bb-218">onde (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) é a posição atual da varredura.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-218">where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position.</span></span><br/></li>
<li><span data-ttu-id="5c9bb-219">Esses fragmentos de pixel são tratados exatamente como os fragmentos gerados pela rasterização de pontos, linhas ou polígonos.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-219">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="5c9bb-220">A função <strong>glColorTableEXT</strong> aplica o mapeamento de textura, sombra e todas as operações de fragmento antes de gravar os fragmentos no framebuffer.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-220">The <strong>glColorTableEXT</strong> function applies texture mapping, fog, and all the fragment operations before writing the fragments to the framebuffer.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="5c9bb-221"><dt><strong>GL_RED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5c9bb-221"><dt><strong>GL_RED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="5c9bb-222">Cada pixel é um único componente vermelho.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-222">Each pixel is a single red component.</span></span><br/> <span data-ttu-id="5c9bb-223">A função <strong>glColorTableEXT</strong> converte esse componente no formato interno da mesma maneira que o componente vermelho de um pixel RGBA, em seguida, converte-o em um pixel RGBA com verde e azul definido como 0,0 e alfa definido como 1,0.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-223">The <strong>glColorTableEXT</strong> function converts this component to the internal format in the same way that the red component of an RGBA pixel is, then converts it to an RGBA pixel with green and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="5c9bb-224">Após essa conversão, o pixel é tratado da mesma forma como se tivesse sido lido como um pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-224">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="5c9bb-225"><dt><strong>GL_GREEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5c9bb-225"><dt><strong>GL_GREEN</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="5c9bb-226">Cada pixel é um único componente verde.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-226">Each pixel is a single green component.</span></span><br/> <span data-ttu-id="5c9bb-227">A função <strong>glColorTableEXT</strong> converte esse componente no formato interno da mesma forma que o componente verde de um pixel RGBA e, em seguida, converte-o em um pixel RGBA com vermelho e azul definido como 0,0 e alfa definido como 1,0.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-227">The <strong>glColorTableEXT</strong> function converts this component to the internal format in the same way that the green component of an RGBA pixel is, and then converts it to an RGBA pixel with red and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="5c9bb-228">Após essa conversão, o pixel é tratado da mesma forma como se tivesse sido lido como um pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-228">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="5c9bb-229"><dt><strong>GL_BLUE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5c9bb-229"><dt><strong>GL_BLUE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="5c9bb-230">Cada pixel é um único componente azul.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-230">Each pixel is a single blue component.</span></span><br/> <span data-ttu-id="5c9bb-231">A função <strong>glColorTableEXT</strong> converte esse componente no formato interno da mesma forma que o componente azul de um pixel RGBA e, em seguida, converte-o em um pixel RGBA com vermelho e verde definido como 0,0 e alfa definido como 1,0.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-231">The <strong>glColorTableEXT</strong> function converts this component to the internal format in the same way that the blue component of an RGBA pixel is, and then converts it to an RGBA pixel with red and green set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="5c9bb-232">Após essa conversão, o pixel é tratado da mesma forma como se tivesse sido lido como um pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-232">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="5c9bb-233"><dt><strong>GL_ALPHA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5c9bb-233"><dt><strong>GL_ALPHA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="5c9bb-234">Cada pixel é um único componente alfa.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-234">Each pixel is a single alpha component.</span></span><br/> <span data-ttu-id="5c9bb-235">A função <strong>glColorTableEXT</strong> converte esse componente no formato interno da mesma forma que o componente alfa de um pixel RGBA e, em seguida, converte-o em um pixel RGBA com vermelho, verde e azul definido como 0,0.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-235">The <strong>glColorTableEXT</strong> function converts this component to the internal format in the same way that the alpha component of an RGBA pixel is, and then converts it to an RGBA pixel with red, green, and blue set to 0.0.</span></span> <span data-ttu-id="5c9bb-236">Após essa conversão, o pixel é tratado da mesma forma como se tivesse sido lido como um pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-236">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="5c9bb-237"><dt><strong>GL_RGB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5c9bb-237"><dt><strong>GL_RGB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="5c9bb-238">Cada pixel é um grupo de três componentes nesta ordem: vermelho, verde, azul.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-238">Each pixel is a group of three components in this order: red, green, blue.</span></span><br/> <span data-ttu-id="5c9bb-239">A função <strong>glColorTableEXT</strong> converte cada componente no formato interno da mesma maneira que os componentes vermelho, verde e azul de um pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-239">The <strong>glColorTableEXT</strong> function converts each component to the internal format in the same way that the red, green, and blue components of an RGBA pixel are.</span></span> <span data-ttu-id="5c9bb-240">A cor tripla é convertida em um pixel RGBA com alfa definido como 1,0.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-240">The color triple is converted to an RGBA pixel with alpha set to 1.0.</span></span> <span data-ttu-id="5c9bb-241">Após essa conversão, o pixel é tratado da mesma forma como se tivesse sido lido como um pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-241">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="5c9bb-242"><dt><strong>GL_BGR_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5c9bb-242"><dt><strong>GL_BGR_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="5c9bb-243">Cada pixel é um grupo de três componentes nesta ordem: azul, verde e vermelho.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-243">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="5c9bb-244">GL_BGR_EXT fornece um formato que corresponde ao layout de memória dos bitmaps independentes de dispositivo do Windows (DIBs).</span><span class="sxs-lookup"><span data-stu-id="5c9bb-244">GL_BGR_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="5c9bb-245">Assim, seus aplicativos podem usar os mesmos dados com chamadas de função do Windows e chamadas de função de pixel OpenGL.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-245">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="5c9bb-246"><dt><strong>GL_BGRA_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5c9bb-246"><dt><strong>GL_BGRA_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="5c9bb-247">Cada pixel é um grupo de quatro componentes nesta ordem: azul, verde, vermelho, alfa.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-247">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span><br/> <span data-ttu-id="5c9bb-248">GL_BGRA_EXT fornece um formato que corresponde ao layout de memória dos bitmaps independentes de dispositivo do Windows (DIBs).</span><span class="sxs-lookup"><span data-stu-id="5c9bb-248">GL_BGRA_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="5c9bb-249">Assim, seus aplicativos podem usar os mesmos dados com chamadas de função do Windows e chamadas de função de pixel OpenGL.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-249">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="5c9bb-250">*tipo*</span><span class="sxs-lookup"><span data-stu-id="5c9bb-250">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="5c9bb-251">O tipo de dados para *dados*.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-251">The data type for *data*.</span></span> <span data-ttu-id="5c9bb-252">As constantes simbólicas a seguir são aceitas: GL \_ não assinado \_ byte, GL \_ byte, GL \_ não assinado \_ curto, GL \_ curto, GL \_ não assinado \_ int, GL \_ int e GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-252">The following symbolic constants are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

<span data-ttu-id="5c9bb-253">A tabela a seguir resume o significado das constantes válidas para o parâmetro de *tipo* .</span><span class="sxs-lookup"><span data-stu-id="5c9bb-253">The following table summarizes the meaning of the valid constants for the *type* parameter.</span></span>



| <span data-ttu-id="5c9bb-254">Valor</span><span class="sxs-lookup"><span data-stu-id="5c9bb-254">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="5c9bb-255">Significado</span><span class="sxs-lookup"><span data-stu-id="5c9bb-255">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <span data-ttu-id="5c9bb-256"><dt>**\_byte não assinado GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5c9bb-256"><dt>**GL\_UNSIGNED\_BYTE**</dt></span></span> </dl>    | <span data-ttu-id="5c9bb-257">Inteiro de 8 bits sem sinal</span><span class="sxs-lookup"><span data-stu-id="5c9bb-257">Unsigned 8-bit integer</span></span><br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <span data-ttu-id="5c9bb-258"><dt>**\_byte GL**</dt></span><span class="sxs-lookup"><span data-stu-id="5c9bb-258"><dt>**GL\_BYTE**</dt></span></span> </dl>                                | <span data-ttu-id="5c9bb-259">Inteiro de 8 bits com sinal</span><span class="sxs-lookup"><span data-stu-id="5c9bb-259">Signed 8-bit integer</span></span><br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <span data-ttu-id="5c9bb-260"><dt>**GL \_ não assinado \_ curto**</dt></span><span class="sxs-lookup"><span data-stu-id="5c9bb-260"><dt>**GL\_UNSIGNED\_SHORT**</dt></span></span> </dl> | <span data-ttu-id="5c9bb-261">Inteiro de 16 bits sem sinal</span><span class="sxs-lookup"><span data-stu-id="5c9bb-261">Unsigned 16-bit integer</span></span><br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <span data-ttu-id="5c9bb-262"><dt>**GL \_ curto**</dt></span><span class="sxs-lookup"><span data-stu-id="5c9bb-262"><dt>**GL\_SHORT**</dt></span></span> </dl>                             | <span data-ttu-id="5c9bb-263">Inteiro de 16 bits com sinal</span><span class="sxs-lookup"><span data-stu-id="5c9bb-263">Signed 16-bit integer</span></span><br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <span data-ttu-id="5c9bb-264"><dt>**GL \_ não assinado \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="5c9bb-264"><dt>**GL\_UNSIGNED\_INT**</dt></span></span> </dl>       | <span data-ttu-id="5c9bb-265">Inteiro de 32 bits sem sinal</span><span class="sxs-lookup"><span data-stu-id="5c9bb-265">Unsigned 32-bit integer</span></span><br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <span data-ttu-id="5c9bb-266"><dt>**RAZÃO \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="5c9bb-266"><dt>**GL\_INT**</dt></span></span> </dl>                                   | <span data-ttu-id="5c9bb-267">Inteiro de 32 bits</span><span class="sxs-lookup"><span data-stu-id="5c9bb-267">32-bit integer</span></span><br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <span data-ttu-id="5c9bb-268"><dt>**GL \_ float**</dt></span><span class="sxs-lookup"><span data-stu-id="5c9bb-268"><dt>**GL\_FLOAT**</dt></span></span> </dl>                             | <span data-ttu-id="5c9bb-269">Valor do ponto flutuante de precisão simples</span><span class="sxs-lookup"><span data-stu-id="5c9bb-269">Single-precision floating-point value</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5c9bb-270">*data*</span><span class="sxs-lookup"><span data-stu-id="5c9bb-270">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="5c9bb-271">Um ponteiro para os dados de textura da paleta.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-271">A pointer to the paletted texture data.</span></span> <span data-ttu-id="5c9bb-272">Os dados são tratados como pixels únicos de uma entrada de paleta de textura 1D para uma entrada de paleta.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-272">The data is treated as single pixels of a 1-D texture palette entry for a palette entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c9bb-273">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5c9bb-273">Return value</span></span>

<span data-ttu-id="5c9bb-274">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-274">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5c9bb-275">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="5c9bb-275">Error codes</span></span>

<span data-ttu-id="5c9bb-276">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="5c9bb-276">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="5c9bb-277">Name</span><span class="sxs-lookup"><span data-stu-id="5c9bb-277">Name</span></span>                                                                                                  | <span data-ttu-id="5c9bb-278">Significado</span><span class="sxs-lookup"><span data-stu-id="5c9bb-278">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5c9bb-279"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5c9bb-279"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="5c9bb-280">a *largura* era um número inteiro inválido.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-280">*width* was an invalid integer.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="5c9bb-281"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="5c9bb-281"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="5c9bb-282">*target*, *internalFormat*, *Format* ou *Type* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-282">*target*, *internalFormat*, *format*, or *type* was not an accepted value.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="5c9bb-283"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5c9bb-283"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="5c9bb-284">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="5c9bb-284">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5c9bb-285">Comentários</span><span class="sxs-lookup"><span data-stu-id="5c9bb-285">Remarks</span></span>

<span data-ttu-id="5c9bb-286">As texturas de paleta são definidas com uma paleta de cores e um conjunto de dados de imagem compostos de índices para entradas de cores de uma paleta (uma tabela de cores).</span><span class="sxs-lookup"><span data-stu-id="5c9bb-286">Paletted textures are defined with a palette of colors and a set of image data that is composed of indexes to color entries of a palette (a color table).</span></span>

<span data-ttu-id="5c9bb-287">A função **glColorTableEXT** especifica a paleta de textura de uma textura de destino.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-287">The **glColorTableEXT** function specifies the texture palette of a targeted texture.</span></span> <span data-ttu-id="5c9bb-288">Ele pega os *dados* da memória e converte os dados como se cada entrada da paleta fosse um único pixel de uma textura 1D.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-288">It takes the *data* from memory and converts the data as if each palette entry is a single pixel of a 1-D texture.</span></span> <span data-ttu-id="5c9bb-289">A função **glColorTableEXT** desempacota e converte os dados e os traduz em um formato interno que corresponda ao *formato* fornecido o mais próximo possível.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-289">The **glColorTableEXT** function unpacks and converts the data and translates it into an internal format that matches the given *format* as closely as possible.</span></span>

<span data-ttu-id="5c9bb-290">Se a *largura* de uma paleta for maior que o intervalo dos índices de cores nos dados de textura, algumas das entradas da paleta não serão usadas.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-290">If a palette's *width* is greater than the range of the color indexes in the texture data, some of the palette entries are unused.</span></span> <span data-ttu-id="5c9bb-291">Se a *largura* de uma paleta for menor que o intervalo dos índices de cores nos dados de textura, os bits mais significativos dos dados de textura serão ignorados e somente o número apropriado de bits no índice será usado ao acessar a paleta.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-291">If a palette's *width* is less than the range of the color indexes in the texture data, the most significant bits of the texture data are ignored and only the appropriate number of bits in the index are used when accessing the palette.</span></span> <span data-ttu-id="5c9bb-292">Quando você especifica um *destino* de proxy usando a \_ textura de proxy \_ 1D ou \_ \_ a textura de proxy 2D, a paleta da textura de proxy é redimensionada e seus parâmetros são definidos, mas nenhum dado é transferido ou acessado.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-292">When you specify a proxy *target* using PROXY\_TEXTURE\_1D or PROXY\_TEXTURE\_2D, the palette of the proxy texture is resized and its parameters are set but no data is transferred or accessed.</span></span>

<span data-ttu-id="5c9bb-293">Quando o parâmetro de *destino* for GL proxy ou textura \_ de proxy ingl \_ \_ \_ 2D ou \_ \_ insupport e a implementação não oferecer suporte aos valores especificados para o *formato* ou a *largura*, **glColorTableEXT** poderá falhar ao criar a tabela de cores solicitada.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-293">When the *target* parameter is GL\_PROXY\_TEXTURE\_1D or GL\_PROXY\_TEXTURE\_2D, and the implementation does not support the values specified for either *format* or *width*, **glColorTableEXT** can fail to create the requested color table.</span></span> <span data-ttu-id="5c9bb-294">Nesse caso, a tabela de cores está vazia e todos os parâmetros recuperados serão zero.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-294">In this case, the color table is empty and all parameters retrieved will be zero.</span></span> <span data-ttu-id="5c9bb-295">Você pode determinar se o OpenGL dá suporte a um formato e tamanho de tabela de cores específico chamando **glColorTableEXT** com um destino de proxy e, em seguida, chamando [**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md) ou [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) para determinar se o parâmetro de largura corresponde ao definido por **glColorTableEXT**.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-295">You can determine whether OpenGL supports a particular color table format and size by calling **glColorTableEXT** with a proxy target, and then calling [**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md) or [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) to determine whether the width parameter matches that set by **glColorTableEXT**.</span></span> <span data-ttu-id="5c9bb-296">Se a largura recuperada for zero, a solicitação da tabela de cores por **glColorTable** falhou.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-296">If the retrieved width is zero, the color table request by **glColorTable** failed.</span></span> <span data-ttu-id="5c9bb-297">Se a largura recuperada não for zero, você poderá chamar **glColorTable** com o destino real com textura \_ 1D ou \_ a textura 2D para definir a tabela de cores.</span><span class="sxs-lookup"><span data-stu-id="5c9bb-297">If the retrieved width is not zero, you can call **glColorTable** with the real target with TEXTURE\_1D or TEXTURE\_2D to set the color table.</span></span>

> [!Note]  
> <span data-ttu-id="5c9bb-298">A função **glColorTableEXT** é uma função de extensão que não faz parte da biblioteca OpenGL padrão, mas faz parte da extensão de textura da paleta do GL \_ ext \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5c9bb-298">The **glColorTableEXT** function is an extension function that is not part of the standard OpenGL library but is part of the GL\_EXT\_paletted\_texture extension.</span></span> <span data-ttu-id="5c9bb-299">Para verificar se a implementação do OpenGL dá suporte a **glColorTableEXT**, chame [**glGetString**](glgetstring.md)( \_ extensões GL).</span><span class="sxs-lookup"><span data-stu-id="5c9bb-299">To check whether your implementation of OpenGL supports **glColorTableEXT**, call [**glGetString**](glgetstring.md)(GL\_EXTENSIONS).</span></span> <span data-ttu-id="5c9bb-300">Se ele retornar a \_ textura da paleta do GL ext \_ \_ , haverá suporte para **glColorTableEXT** .</span><span class="sxs-lookup"><span data-stu-id="5c9bb-300">If it returns GL\_EXT\_paletted\_texture, **glColorTableEXT** is supported.</span></span> <span data-ttu-id="5c9bb-301">Para obter o endereço da função de uma função de extensão, chame [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span><span class="sxs-lookup"><span data-stu-id="5c9bb-301">To obtain the function address of an extension function, call [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span></span>

 

<span data-ttu-id="5c9bb-302">Para recuperar os dados da tabela de cores real especificados pela função **glColorTableEXT** , chame [**glGetColorTableEXT**](glgetcolortableext.md).</span><span class="sxs-lookup"><span data-stu-id="5c9bb-302">To retrieve the actual color table data specified by the **glColorTableEXT** function, call [**glGetColorTableEXT**](glgetcolortableext.md).</span></span> <span data-ttu-id="5c9bb-303">Para recuperar os parâmetros, como *largura* e *formato*, da tabela de cores especificada pela função **GlColorTableEXT** , chame a função **glGetColorTableParameterivEXT** ou **glGetColorTableParameterfvEXT** .</span><span class="sxs-lookup"><span data-stu-id="5c9bb-303">To retrieve the parameters, such as *width* and *format*, of the color table specified by the **glColorTableEXT** function, call the **glGetColorTableParameterivEXT** or **glGetColorTableParameterfvEXT** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c9bb-304">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c9bb-304">Requirements</span></span>



| <span data-ttu-id="5c9bb-305">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c9bb-305">Requirement</span></span> | <span data-ttu-id="5c9bb-306">Valor</span><span class="sxs-lookup"><span data-stu-id="5c9bb-306">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="5c9bb-307">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c9bb-307">Minimum supported client</span></span><br/> | <span data-ttu-id="5c9bb-308">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5c9bb-308">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="5c9bb-309">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c9bb-309">Minimum supported server</span></span><br/> | <span data-ttu-id="5c9bb-310">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5c9bb-310">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="5c9bb-311">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5c9bb-311">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c9bb-312"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c9bb-312"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c9bb-313">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c9bb-313">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c9bb-314">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="5c9bb-314">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="5c9bb-315">**glColorSubTableEXT**</span><span class="sxs-lookup"><span data-stu-id="5c9bb-315">**glColorSubTableEXT**</span></span>](glcolorsubtableext.md)
</dt> <dt>

[<span data-ttu-id="5c9bb-316">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="5c9bb-316">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="5c9bb-317">**glGetColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="5c9bb-317">**glGetColorTableEXT**</span></span>](glgetcolortableext.md)
</dt> <dt>

[<span data-ttu-id="5c9bb-318">**glGetColorTableParameterfvEXT**</span><span class="sxs-lookup"><span data-stu-id="5c9bb-318">**glGetColorTableParameterfvEXT**</span></span>](glgetcolortableparameterfvext.md)
</dt> <dt>

[<span data-ttu-id="5c9bb-319">**glGetColorTableParameterivEXT**</span><span class="sxs-lookup"><span data-stu-id="5c9bb-319">**glGetColorTableParameterivEXT**</span></span>](glgetcolortableparameterivext.md)
</dt> <dt>

[<span data-ttu-id="5c9bb-320">**wglGetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="5c9bb-320">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





