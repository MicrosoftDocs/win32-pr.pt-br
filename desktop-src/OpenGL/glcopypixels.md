---
title: função glCopyPixels (GL. h)
description: A função glCopyPixels copia pixels no framebuffer.
ms.assetid: c4055928-7b8b-4d0f-94f3-e3b9c0503308
keywords:
- função glCopyPixels OpenGL
topic_type:
- apiref
api_name:
- glCopyPixels
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7ba0833534d21e48c251da6491fee2996c3ed9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918583"
---
# <a name="glcopypixels-function"></a><span data-ttu-id="605c0-104">função glCopyPixels</span><span class="sxs-lookup"><span data-stu-id="605c0-104">glCopyPixels function</span></span>

<span data-ttu-id="605c0-105">A função **glCopyPixels** copia pixels no framebuffer.</span><span class="sxs-lookup"><span data-stu-id="605c0-105">The **glCopyPixels** function copies pixels in the framebuffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="605c0-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="605c0-106">Syntax</span></span>


```C++
void WINAPI glCopyPixels(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height,
   GLenum  type
);
```



## <a name="parameters"></a><span data-ttu-id="605c0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="605c0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="605c0-108">*x*</span><span class="sxs-lookup"><span data-stu-id="605c0-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="605c0-109">A coordenada de plano x do canto inferior esquerdo da região retangular de pixels a ser copiada.</span><span class="sxs-lookup"><span data-stu-id="605c0-109">The window x-plane coordinate of the lower-left corner of the rectangular region of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="605c0-110">*y*</span><span class="sxs-lookup"><span data-stu-id="605c0-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="605c0-111">A coordenada de plano y da janela do canto inferior esquerdo da região retangular de pixels a serem copiados.</span><span class="sxs-lookup"><span data-stu-id="605c0-111">The window y-plane coordinate of the lower-left corner of the rectangular region of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="605c0-112">*width*</span><span class="sxs-lookup"><span data-stu-id="605c0-112">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="605c0-113">A dimensão de largura da região retangular de pixels a serem copiadas.</span><span class="sxs-lookup"><span data-stu-id="605c0-113">The width dimension of the rectangular region of pixels to be copied.</span></span> <span data-ttu-id="605c0-114">Deve ser não negativo.</span><span class="sxs-lookup"><span data-stu-id="605c0-114">Must be nonnegative.</span></span>

</dd> <dt>

<span data-ttu-id="605c0-115">*altura*</span><span class="sxs-lookup"><span data-stu-id="605c0-115">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="605c0-116">A dimensão de altura da região retangular de pixels a serem copiadas.</span><span class="sxs-lookup"><span data-stu-id="605c0-116">The height dimension of the rectangular region of pixels to be copied.</span></span> <span data-ttu-id="605c0-117">Deve ser não negativo.</span><span class="sxs-lookup"><span data-stu-id="605c0-117">Must be nonnegative.</span></span>

</dd> <dt>

<span data-ttu-id="605c0-118">*tipo*</span><span class="sxs-lookup"><span data-stu-id="605c0-118">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="605c0-119">Especifica se **glCopyPixels** é para copiar valores de cor, valores de profundidade ou valores de estêncil.</span><span class="sxs-lookup"><span data-stu-id="605c0-119">Specifies whether **glCopyPixels** is to copy color values, depth values, or stencil values.</span></span> <span data-ttu-id="605c0-120">As constantes simbólicas aceitáveis são.</span><span class="sxs-lookup"><span data-stu-id="605c0-120">The acceptable symbolic constants are.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="605c0-121">Valor</span><span class="sxs-lookup"><span data-stu-id="605c0-121">Value</span></span></th>
<th><span data-ttu-id="605c0-122">Significado</span><span class="sxs-lookup"><span data-stu-id="605c0-122">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_COLOR"></span><span id="gl_color"></span><dl> <span data-ttu-id="605c0-123"><dt><strong>GL_COLOR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="605c0-123"><dt><strong>GL_COLOR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="605c0-124">A função <strong>glCopyPixels</strong> lê índices ou cores RGBA do buffer especificado no momento como o buffer de origem de leitura (consulte <a href="glreadbuffer.md"><strong>glReadBuffer</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="605c0-124">The <strong>glCopyPixels</strong> function reads indexes or RGBA colors from the buffer currently specified as the read source buffer (see <a href="glreadbuffer.md"><strong>glReadBuffer</strong></a>).</span></span> <br/> <span data-ttu-id="605c0-125">Se OpenGL estiver no modo de índice de cor:</span><span class="sxs-lookup"><span data-stu-id="605c0-125">If OpenGL is in color-index mode:</span></span><br/>
<ol>
<li><span data-ttu-id="605c0-126">Cada índice lido desse buffer é convertido em um formato de ponto fixo com um número não especificado de bits à direita do ponto binário.</span><span class="sxs-lookup"><span data-stu-id="605c0-126">Each index that is read from this buffer is converted to a fixed-point format with an unspecified number of bits to the right of the binary point.</span></span></li>
<li><span data-ttu-id="605c0-127">Cada índice é deslocado para a esquerda por GL_INDEX_SHIFT bits e adicionado a GL_INDEX_OFFSET. Se GL_INDEX_SHIFT for negativo, a mudança será à direita.</span><span class="sxs-lookup"><span data-stu-id="605c0-127">Each index is shifted left by GL_INDEX_SHIFT bits, and added to GL_INDEX_OFFSET.If GL_INDEX_SHIFT is negative, the shift is to the right.</span></span> <span data-ttu-id="605c0-128">Em ambos os casos, zero bits ocupam locais de bits não especificados no resultado.</span><span class="sxs-lookup"><span data-stu-id="605c0-128">In either case, zero bits fill otherwise unspecified bit locations in the result.</span></span><br/></li>
<li><span data-ttu-id="605c0-129">Se GL_MAP_COLOR for true, o índice será substituído pelo valor que ele faz referência na tabela de pesquisa GL_PIXEL_MAP_I_TO_I.</span><span class="sxs-lookup"><span data-stu-id="605c0-129">If GL_MAP_COLOR is true, the index is replaced with the value that it references in lookup table GL_PIXEL_MAP_I_TO_I.</span></span></li>
<li><span data-ttu-id="605c0-130">Se a substituição da pesquisa do índice for concluída ou não, a parte inteira do índice será, então, Ed com 2<em><sup>b</sup></em> 1 <strong>, em que</strong> <em>b</em> é o número de bits em um buffer de índice de cor.</span><span class="sxs-lookup"><span data-stu-id="605c0-130">Whether the lookup replacement of the index is done or not, the integer part of the index is then <strong>AND</strong>ed with 2<em><sup>b</sup></em> 1, where <em>b</em> is the number of bits in a color-index buffer.</span></span></li>
</ol>
<span data-ttu-id="605c0-131">Se OpenGL estiver no modo RGBA:</span><span class="sxs-lookup"><span data-stu-id="605c0-131">If OpenGL is in RGBA mode:</span></span><br/>
<ol>
<li><span data-ttu-id="605c0-132">Os componentes vermelho, verde, azul e alfa de cada pixel lido são convertidos em um formato de ponto flutuante interno com precisão não especificada.</span><span class="sxs-lookup"><span data-stu-id="605c0-132">The red, green, blue, and alpha components of each pixel that is read are converted to an internal floating-point format with unspecified precision.</span></span></li>
<li><span data-ttu-id="605c0-133">A conversão mapeia o maior valor de componente representável para 1,0 e o valor de componente de zero a 0,0.</span><span class="sxs-lookup"><span data-stu-id="605c0-133">The conversion maps the largest representable component value to 1.0, and component value zero to 0.0.</span></span></li>
<li><span data-ttu-id="605c0-134">Os valores de cor de ponto flutuante resultantes são então multiplicados por GL_c_SCALE e adicionados a GL_c_BIAS, em que <em>c</em> é vermelho, verde, azul e alfa para os respectivos componentes de cor.</span><span class="sxs-lookup"><span data-stu-id="605c0-134">The resulting floating-point color values are then multiplied by GL_c_SCALE and added to GL_c_BIAS, where <em>c</em> is RED, GREEN, BLUE, and ALPHA for the respective color components.</span></span></li>
<li><span data-ttu-id="605c0-135">Os resultados são clamped para o intervalo [0, 1].</span><span class="sxs-lookup"><span data-stu-id="605c0-135">The results are clamped to the range [0,1].</span></span></li>
<li><span data-ttu-id="605c0-136">Se GL_MAP_COLOR for true, cada componente de cor será dimensionado pelo tamanho da tabela de pesquisa GL_PIXEL_MAP_c_TO_c e, em seguida, substituído pelo valor referenciado nessa tabela; <em>c</em> é R, G, B ou A, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="605c0-136">If GL_MAP_COLOR is true, each color component is scaled by the size of lookup table GL_PIXEL_MAP_c_TO_c, and then replaced by the value that it references in that table; <em>c</em> is R, G, B, or A, respectively.</span></span> <span data-ttu-id="605c0-137">Os índices resultantes ou as cores RGBA são então convertidas em fragmentos anexando as coordenadas de coordenadas <em>z</em>e de textura atuais a cada pixel e, em seguida, atribuindo coordenadas de janela (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>), em que (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) é a posição atual da varredura e o pixel era o pixel na posição <em>i</em> na linha <em>j</em> .</span><span class="sxs-lookup"><span data-stu-id="605c0-137">The resulting indexes or RGBA colors are then converted to fragments by attaching the current raster position <em>z</em>-coordinate and texture coordinates to each pixel, and then assigning window coordinates (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>), where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position, and the pixel was the pixel in the <em>i</em> position in the <em>j</em> row.</span></span> <span data-ttu-id="605c0-138">Esses fragmentos de pixel são tratados exatamente como os fragmentos gerados pela rasterização de pontos, linhas ou polígonos.</span><span class="sxs-lookup"><span data-stu-id="605c0-138">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="605c0-139">O mapeamento de textura, a neblina e todas as operações de fragmento são aplicadas antes que os fragmentos sejam gravados no framebuffer.</span><span class="sxs-lookup"><span data-stu-id="605c0-139">Texture mapping, fog, and all the fragment operations are applied before the fragments are written to the framebuffer.</span></span><br/></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_DEPTH"></span><span id="gl_depth"></span><dl> <span data-ttu-id="605c0-140"><dt><strong>GL_DEPTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="605c0-140"><dt><strong>GL_DEPTH</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="605c0-141">Os valores de profundidade são lidos do buffer de profundidade e convertidos diretamente em um formato de ponto flutuante interno com precisão não especificada.</span><span class="sxs-lookup"><span data-stu-id="605c0-141">Depth values are read from the depth buffer and converted directly to an internal floating-point format with unspecified precision.</span></span> <span data-ttu-id="605c0-142">O valor de profundidade de ponto flutuante resultante é então multiplicado por GL_DEPTH_SCALE e adicionado ao GL_DEPTH_BIAS.</span><span class="sxs-lookup"><span data-stu-id="605c0-142">The resulting floating-point depth value is then multiplied by GL_DEPTH_SCALE and added to GL_DEPTH_BIAS.</span></span> <span data-ttu-id="605c0-143">O resultado é clamped para o intervalo [0, 1].</span><span class="sxs-lookup"><span data-stu-id="605c0-143">The result is clamped to the range [0,1].</span></span> <br/> <span data-ttu-id="605c0-144">Os componentes de profundidade resultantes são então convertidos em fragmentos anexando a cor atual da posição de rasterização ou o índice de cor e as coordenadas de textura a cada pixel e, em seguida, atribuindo coordenadas de janela (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>), em que (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) é a posição atual <em></em> da varredura, e o pixel era o pixel na posição <em>i</em></span><span class="sxs-lookup"><span data-stu-id="605c0-144">The resulting depth components are then converted to fragments by attaching the current raster position color or color index and texture coordinates to each pixel, then assigning window coordinates (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>), where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position, and the pixel was the pixel in the <em>i</em> position in the <em>j</em> row.</span></span> <span data-ttu-id="605c0-145">Esses fragmentos de pixel são tratados exatamente como os fragmentos gerados pela rasterização de pontos, linhas ou polígonos.</span><span class="sxs-lookup"><span data-stu-id="605c0-145">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="605c0-146">O mapeamento de textura, a neblina e todas as operações de fragmento são aplicadas antes que os fragmentos sejam gravados no framebuffer.</span><span class="sxs-lookup"><span data-stu-id="605c0-146">Texture mapping, fog, and all the fragment operations are applied before the fragments are written to the framebuffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_STENCIL"></span><span id="gl_stencil"></span><dl> <span data-ttu-id="605c0-147"><dt><strong>GL_STENCIL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="605c0-147"><dt><strong>GL_STENCIL</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="605c0-148">Os índices de estêncil são lidos do buffer de estêncil e convertidos em um formato de ponto fixo interno com um número não especificado de bits à direita do ponto binário.</span><span class="sxs-lookup"><span data-stu-id="605c0-148">Stencil indexes are read from the stencil buffer and converted to an internal fixed-point format with an unspecified number of bits to the right of the binary point.</span></span> <span data-ttu-id="605c0-149">Cada índice de ponto fixo é então deslocado para a esquerda por GL_INDEX_SHIFT bits e adicionado ao GL_INDEX_OFFSET.</span><span class="sxs-lookup"><span data-stu-id="605c0-149">Each fixed-point index is then shifted left by GL_INDEX_SHIFT bits, and added to GL_INDEX_OFFSET.</span></span> <span data-ttu-id="605c0-150">Se GL_INDEX_SHIFT for negativo, a mudança será à direita.</span><span class="sxs-lookup"><span data-stu-id="605c0-150">If GL_INDEX_SHIFT is negative, the shift is to the right.</span></span> <span data-ttu-id="605c0-151">Em ambos os casos, zero bits ocupam locais de bits não especificados no resultado.</span><span class="sxs-lookup"><span data-stu-id="605c0-151">In either case, zero bits fill otherwise unspecified bit locations in the result.</span></span> <span data-ttu-id="605c0-152">Se GL_MAP_STENCIL for true, o índice será substituído pelo valor que ele faz referência na tabela de pesquisa GL_PIXEL_MAP_S_TO_S.</span><span class="sxs-lookup"><span data-stu-id="605c0-152">If GL_MAP_STENCIL is true, the index is replaced with the value that it references in lookup table GL_PIXEL_MAP_S_TO_S.</span></span> <span data-ttu-id="605c0-153">Se a substituição da pesquisa do índice for concluída ou não, a parte inteira do índice será <strong>, então,</strong>Ed com 2<sup>b</sup> - 1, em que <em>b</em> é o número de bits no buffer do estêncil.</span><span class="sxs-lookup"><span data-stu-id="605c0-153">Whether the lookup replacement of the index is done or not, the integer part of the index is then <strong>AND</strong>ed with 2<sup>b</sup> - 1, where <em>b</em> is the number of bits in the stencil buffer.</span></span> <span data-ttu-id="605c0-154">Os índices de estêncil resultantes são gravados no buffer do estêncil, de modo que o índice lido do local <em>i</em> da linha <em>j</em> seja gravado no local (<em>x</em><sub>r</sub> + <em>i</em>, <em>y</em><sub>r</sub> + <em>j</em>), em que (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) é a posição atual da varredura.</span><span class="sxs-lookup"><span data-stu-id="605c0-154">The resulting stencil indexes are then written to the stencil buffer such that the index read from the <em>i</em> location of the <em>j</em> row is written to location (<em>x</em><sub>r</sub> + <em>i</em>, <em>y</em><sub>r</sub> + <em>j</em>), where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position.</span></span> <span data-ttu-id="605c0-155">Somente o teste de propriedade de pixel, o teste de tesoura e o estêncil writemask afetam essas gravações.</span><span class="sxs-lookup"><span data-stu-id="605c0-155">Only the pixel-ownership test, the scissor test, and the stencil writemask affect these writes.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="605c0-156">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="605c0-156">Return value</span></span>

<span data-ttu-id="605c0-157">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="605c0-157">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="605c0-158">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="605c0-158">Error codes</span></span>

<span data-ttu-id="605c0-159">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="605c0-159">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="605c0-160">Name</span><span class="sxs-lookup"><span data-stu-id="605c0-160">Name</span></span>                                                                                                  | <span data-ttu-id="605c0-161">Significado</span><span class="sxs-lookup"><span data-stu-id="605c0-161">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="605c0-162"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="605c0-162"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="605c0-163">o *tipo* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="605c0-163">*type* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="605c0-164"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="605c0-164"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="605c0-165">A *largura* ou a altura era negativa.</span><span class="sxs-lookup"><span data-stu-id="605c0-165">Either *width* or height was negative.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="605c0-166"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="605c0-166"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="605c0-167">o *tipo* era a profundidade GL e não havia \_ buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="605c0-167">*type* was GL\_DEPTH and there was no depth buffer.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="605c0-168"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="605c0-168"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="605c0-169">o *tipo* foi o estêncil GL e não havia \_ um buffer de estêncil.</span><span class="sxs-lookup"><span data-stu-id="605c0-169">*type* was GL\_STENCIL and there was no stencil buffer.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="605c0-170"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="605c0-170"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="605c0-171">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="605c0-171">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="605c0-172">Comentários</span><span class="sxs-lookup"><span data-stu-id="605c0-172">Remarks</span></span>

<span data-ttu-id="605c0-173">A função **glCopyPixels** copia um retângulo de pixels alinhado por tela do local framebuffer especificado para uma região relativa à posição de rasterização atual.</span><span class="sxs-lookup"><span data-stu-id="605c0-173">The **glCopyPixels** function copies a screen-aligned rectangle of pixels from the specified framebuffer location to a region relative to the current raster position.</span></span> <span data-ttu-id="605c0-174">Sua operação será bem definida somente se a região de origem do pixel inteiro estiver dentro da parte exposta da janela.</span><span class="sxs-lookup"><span data-stu-id="605c0-174">Its operation is well defined only if the entire pixel source region is within the exposed portion of the window.</span></span> <span data-ttu-id="605c0-175">Os resultados de cópias de fora da janela, ou de regiões da janela que não são expostas, são dependentes de hardware e indefinidos.</span><span class="sxs-lookup"><span data-stu-id="605c0-175">Results of copies from outside the window, or from regions of the window that are not exposed, are hardware dependent and undefined.</span></span>

<span data-ttu-id="605c0-176">Os parâmetros *x* e *y* especificam as coordenadas da janela do canto inferior esquerdo da região retangular a ser copiada.</span><span class="sxs-lookup"><span data-stu-id="605c0-176">The *x* and *y* parameters specify the window coordinates of the lower-left corner of the rectangular region to be copied.</span></span> <span data-ttu-id="605c0-177">Os parâmetros *Width* e *Height* especificam as dimensões da região retangular a ser copiada.</span><span class="sxs-lookup"><span data-stu-id="605c0-177">The *width* and *height* parameters specify the dimensions of the rectangular region to be copied.</span></span> <span data-ttu-id="605c0-178">A *largura* e a *altura* devem ser não negativas.</span><span class="sxs-lookup"><span data-stu-id="605c0-178">Both *width* and *height* must be nonnegative.</span></span>

<span data-ttu-id="605c0-179">Vários parâmetros controlam o processamento dos dados de pixel enquanto eles estão sendo copiados.</span><span class="sxs-lookup"><span data-stu-id="605c0-179">Several parameters control the processing of the pixel data while it is being copied.</span></span> <span data-ttu-id="605c0-180">Esses parâmetros são definidos com três funções: [**glPixelTransfer**](glpixeltransfer.md), [**glPixelMap**](glpixelmap.md)e [**glPixelZoom**](glpixelzoom.md).</span><span class="sxs-lookup"><span data-stu-id="605c0-180">These parameters are set with three functions: [**glPixelTransfer**](glpixeltransfer.md), [**glPixelMap**](glpixelmap.md), and [**glPixelZoom**](glpixelzoom.md).</span></span> <span data-ttu-id="605c0-181">Este tópico descreve os efeitos sobre **glCopyPixels** , mas não todos, dos parâmetros especificados por essas três funções.</span><span class="sxs-lookup"><span data-stu-id="605c0-181">This topic describes the effects on **glCopyPixels** of most, but not all, of the parameters specified by these three functions.</span></span>

<span data-ttu-id="605c0-182">A função **glCopyPixels** copia valores de cada pixel com o canto inferior esquerdo em (*x*  +  *i*, *y*  +  *j*) para 0 = *i*  <  *Width* e 0 = *j*  <  *Height*.</span><span class="sxs-lookup"><span data-stu-id="605c0-182">The **glCopyPixels** function copies values from each pixel with the lower-left corner at (*x* + *i*, *y* + *j*) for 0 = *i* < *width* and 0 = *j* < *height*.</span></span> <span data-ttu-id="605c0-183">Esse pixel é considerado o pixel *i* na linha *j* .</span><span class="sxs-lookup"><span data-stu-id="605c0-183">This pixel is said to be the *i* pixel in the *j* row.</span></span> <span data-ttu-id="605c0-184">Os pixels são copiados em ordem de linha do menor para a linha mais alta, da esquerda para a direita em cada linha.</span><span class="sxs-lookup"><span data-stu-id="605c0-184">Pixels are copied in row order from the lowest to the highest row, left to right in each row.</span></span>

<span data-ttu-id="605c0-185">O parâmetro de *tipo* especifica se os dados de cor, profundidade ou estêncil devem ser copiados.</span><span class="sxs-lookup"><span data-stu-id="605c0-185">The *type* parameter specifies whether color, depth, or stencil data is to be copied.</span></span>

<span data-ttu-id="605c0-186">A rasterização descrita até o momento pressupõe fatores de zoom de pixel de 1,0.</span><span class="sxs-lookup"><span data-stu-id="605c0-186">The rasterization described thus far assumes pixel zoom factors of 1.0.</span></span> <span data-ttu-id="605c0-187">Se você usar [**glPixelZoom**](glpixelzoom.md) para alterar os fatores de zoom *x* e *y* pixel, os pixels serão convertidos em fragmentos da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="605c0-187">If you use [**glPixelZoom**](glpixelzoom.md) to change the *x* and *y* pixel zoom factors, pixels are converted to fragments as follows.</span></span> <span data-ttu-id="605c0-188">Se (*x*<sub>r</sub> , *y*<sub>r</sub> ) for a posição atual da varredura e um determinado pixel estiver na localização *i* na linha *j* do retângulo do pixel de origem, os fragmentos serão gerados para os pixels cujos centros estão no retângulo com os cantos em</span><span class="sxs-lookup"><span data-stu-id="605c0-188">If (*x*<sub>r</sub> , *y*<sub>r</sub> ) is the current raster position, and a given pixel is in the *i* location in the *j* row of the source pixel rectangle, then fragments are generated for pixels whose centers are in the rectangle with corners at</span></span>

<span data-ttu-id="605c0-189">(*x*<sub>r</sub>  +  *aplicar zoom*? i, y <sub>r</sub>  +  *zoom*<sub>y</sub> *j*)</span><span class="sxs-lookup"><span data-stu-id="605c0-189">(*x*<sub>r</sub> + *zoom*? i, y <sub>r</sub> + *zoom*<sub>y</sub> *j*)</span></span>

<span data-ttu-id="605c0-190">e</span><span class="sxs-lookup"><span data-stu-id="605c0-190">and</span></span>

<span data-ttu-id="605c0-191">(*x*<sub>r</sub>  +  *aplicar zoom*?</span><span class="sxs-lookup"><span data-stu-id="605c0-191">(*x*<sub>r</sub> + *zoom*?</span></span> <span data-ttu-id="605c0-192">(*i* + 1), *y*<sub>r</sub>  +  *zoom*<sub>y</sub> (*j* + 1))</span><span class="sxs-lookup"><span data-stu-id="605c0-192">(*i* + 1), *y*<sub>r</sub> + *zoom*<sub>y</sub> (*j* + 1))</span></span>

<span data-ttu-id="605c0-193">onde *aplicar zoom*? é o valor de GL \_ zoom \_ X e *zoom*<sub>y</sub> é o valor de GL \_ zoom \_ y.</span><span class="sxs-lookup"><span data-stu-id="605c0-193">where *zoom*? is the value of GL\_ZOOM\_X and *zoom*<sub>y</sub> is the value of GL\_ZOOM\_Y.</span></span>

<span data-ttu-id="605c0-194">Os modos especificados por [**glPixelStore**](glpixelstore-functions.md) não têm efeito sobre a operação de **glCopyPixels**.</span><span class="sxs-lookup"><span data-stu-id="605c0-194">Modes specified by [**glPixelStore**](glpixelstore-functions.md) have no effect on the operation of **glCopyPixels**.</span></span>

<span data-ttu-id="605c0-195">As funções a seguir recuperam informações relacionadas ao **glCopyPixels**:</span><span class="sxs-lookup"><span data-stu-id="605c0-195">The following functions retrieve information related to **glCopyPixels**:</span></span>

<span data-ttu-id="605c0-196">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento \_ GL \_ posição de rasterização atual \_</span><span class="sxs-lookup"><span data-stu-id="605c0-196">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION</span></span>

<span data-ttu-id="605c0-197">**glGet** com Argument GL \_ \_ posição de rasterização atual \_ \_ válida</span><span class="sxs-lookup"><span data-stu-id="605c0-197">**glGet** with argument GL\_CURRENT\_RASTER\_POSITION\_VALID</span></span>

<span data-ttu-id="605c0-198">Para copiar o pixel de cor no canto inferior esquerdo da janela para a posição de rasterização atual, use</span><span class="sxs-lookup"><span data-stu-id="605c0-198">To copy the color pixel in the lower-left corner of the window to the current raster position, use</span></span>

<span data-ttu-id="605c0-199">**glCopyPixels**(0, 0, 1, 1, cor do GL \_ );</span><span class="sxs-lookup"><span data-stu-id="605c0-199">**glCopyPixels**( 0, 0, 1, 1, GL\_COLOR );</span></span>

## <a name="requirements"></a><span data-ttu-id="605c0-200">Requisitos</span><span class="sxs-lookup"><span data-stu-id="605c0-200">Requirements</span></span>



| <span data-ttu-id="605c0-201">Requisito</span><span class="sxs-lookup"><span data-stu-id="605c0-201">Requirement</span></span> | <span data-ttu-id="605c0-202">Valor</span><span class="sxs-lookup"><span data-stu-id="605c0-202">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="605c0-203">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="605c0-203">Minimum supported client</span></span><br/> | <span data-ttu-id="605c0-204">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="605c0-204">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="605c0-205">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="605c0-205">Minimum supported server</span></span><br/> | <span data-ttu-id="605c0-206">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="605c0-206">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="605c0-207">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="605c0-207">Header</span></span><br/>                   | <dl> <span data-ttu-id="605c0-208"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="605c0-208"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="605c0-209">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="605c0-209">Library</span></span><br/>                  | <dl> <span data-ttu-id="605c0-210"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="605c0-210"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="605c0-211">DLL</span><span class="sxs-lookup"><span data-stu-id="605c0-211">DLL</span></span><br/>                      | <dl> <span data-ttu-id="605c0-212"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="605c0-212"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="605c0-213">Consulte também</span><span class="sxs-lookup"><span data-stu-id="605c0-213">See also</span></span>

<dl> <dt>

[<span data-ttu-id="605c0-214">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="605c0-214">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="605c0-215">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="605c0-215">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="605c0-216">**glDrawBuffer**</span><span class="sxs-lookup"><span data-stu-id="605c0-216">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="605c0-217">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="605c0-217">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="605c0-218">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="605c0-218">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="605c0-219">**glGet**</span><span class="sxs-lookup"><span data-stu-id="605c0-219">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="605c0-220">**glPixelMap**</span><span class="sxs-lookup"><span data-stu-id="605c0-220">**glPixelMap**</span></span>](glpixelmap.md)
</dt> <dt>

[<span data-ttu-id="605c0-221">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="605c0-221">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="605c0-222">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="605c0-222">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="605c0-223">**glPixelZoom**</span><span class="sxs-lookup"><span data-stu-id="605c0-223">**glPixelZoom**</span></span>](glpixelzoom.md)
</dt> <dt>

[<span data-ttu-id="605c0-224">**glRasterPos**</span><span class="sxs-lookup"><span data-stu-id="605c0-224">**glRasterPos**</span></span>](glrasterpos-functions.md)
</dt> <dt>

[<span data-ttu-id="605c0-225">**glReadBuffer**</span><span class="sxs-lookup"><span data-stu-id="605c0-225">**glReadBuffer**</span></span>](glreadbuffer.md)
</dt> <dt>

[<span data-ttu-id="605c0-226">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="605c0-226">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="605c0-227">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="605c0-227">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> </dl>

 

 





