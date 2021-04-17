---
title: função glGetColorTableEXT (GL. h)
description: A função glGetColorTableEXT Obtém os dados da tabela de cores da paleta de textura direcionada atual.
ms.assetid: 9169c4e1-a22e-48fe-bd45-4549c1a10ff0
keywords:
- função glGetColorTableEXT OpenGL
topic_type:
- apiref
api_name:
- glGetColorTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 811dc53b32c937970fbef8d87fa9a2ef4eb8b978
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105813129"
---
# <a name="glgetcolortableext-function"></a><span data-ttu-id="d4395-104">função glGetColorTableEXT</span><span class="sxs-lookup"><span data-stu-id="d4395-104">glGetColorTableEXT function</span></span>

<span data-ttu-id="d4395-105">A função **glGetColorTableEXT** Obtém os dados da tabela de cores da paleta de textura direcionada atual.</span><span class="sxs-lookup"><span data-stu-id="d4395-105">The **glGetColorTableEXT** function gets the color table data of the current targeted texture palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4395-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d4395-106">Syntax</span></span>


```C++
void WINAPI glGetColorTableEXT(
         GLenum target,
         GLenum format,
         GLenum type,
   const GLvoid *data
);
```



## <a name="parameters"></a><span data-ttu-id="d4395-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d4395-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4395-108">*destino*</span><span class="sxs-lookup"><span data-stu-id="d4395-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="d4395-109">A textura de destino que deve ter sua paleta alterada.</span><span class="sxs-lookup"><span data-stu-id="d4395-109">The target texture that is to have its palette changed.</span></span> <span data-ttu-id="d4395-110">Deve ser textura \_ 1D ou 2D de textura \_ .</span><span class="sxs-lookup"><span data-stu-id="d4395-110">Must be TEXTURE\_1D or TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="d4395-111">*format*</span><span class="sxs-lookup"><span data-stu-id="d4395-111">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="d4395-112">O formato dos dados de pixel.</span><span class="sxs-lookup"><span data-stu-id="d4395-112">The format of the pixel data.</span></span> <span data-ttu-id="d4395-113">As constantes simbólicas a seguir são aceitas.</span><span class="sxs-lookup"><span data-stu-id="d4395-113">The following symbolic constants are accepted.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d4395-114">Valor</span><span class="sxs-lookup"><span data-stu-id="d4395-114">Value</span></span></th>
<th><span data-ttu-id="d4395-115">Significado</span><span class="sxs-lookup"><span data-stu-id="d4395-115">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="d4395-116"><dt><strong>GL_RGBA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d4395-116"><dt><strong>GL_RGBA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="d4395-117">Cada pixel é um grupo de quatro componentes na seguinte ordem: vermelho, verde, azul, alfa.</span><span class="sxs-lookup"><span data-stu-id="d4395-117">Each pixel is a group of four components in the following order: red, green, blue, alpha.</span></span> <span data-ttu-id="d4395-118">O formato RGBA é determinado dessa maneira:</span><span class="sxs-lookup"><span data-stu-id="d4395-118">The RGBA format is determined in this way:</span></span> <br/>
<ol>
<li><span data-ttu-id="d4395-119">A função <strong>glGetColorTableEXT</strong> converte valores de ponto flutuante diretamente em um formato interno com precisão não especificada.</span><span class="sxs-lookup"><span data-stu-id="d4395-119">The <strong>glGetColorTableEXT</strong> function converts floating-point values directly to an internal format with unspecified precision.</span></span> <span data-ttu-id="d4395-120">Valores inteiros assinados são mapeados linearmente para o formato interno, de modo que o valor inteiro representável mais positivo seja mapeado para 1,0 e o valor inteiro reapresentável mais negativo seja mapeado para-1,0.</span><span class="sxs-lookup"><span data-stu-id="d4395-120">Signed integer values are mapped linearly to the internal format such that the most positive representable integer value maps to 1.0, and the most negative representable integer value maps to -1.0.</span></span> <span data-ttu-id="d4395-121">Os dados inteiros não assinados são mapeados da mesma forma: o maior valor inteiro é mapeado para 1,0 e zero é mapeado para 0,0.</span><span class="sxs-lookup"><span data-stu-id="d4395-121">Unsigned integer data is mapped similarly: the largest integer value maps to 1.0, and zero maps to 0.0.</span></span></li>
<li><span data-ttu-id="d4395-122">A função <strong>glGetColorTableEXT</strong> multiplica os valores de cor resultantes por GL_c_SCALE e os adiciona ao GL_c_BIAS, em que <em>c</em> é vermelho, verde, azul e alfa para os respectivos componentes de cor.</span><span class="sxs-lookup"><span data-stu-id="d4395-122">The <strong>glGetColorTableEXT</strong> function multiplies the resulting color values by GL_c_SCALE and adds them to GL_c_BIAS, where <em>c</em> is RED, GREEN, BLUE, and ALPHA for the respective color components.</span></span> <span data-ttu-id="d4395-123">Os resultados são clamped para o intervalo [0, 1].</span><span class="sxs-lookup"><span data-stu-id="d4395-123">The results are clamped to the range [0,1].</span></span></li>
<li><span data-ttu-id="d4395-124">Se GL_MAP_COLOR for <strong>true</strong>, <strong>glGetColorTableEXT</strong> dimensionará cada componente de cor pelo tamanho da tabela de pesquisa GL_PIXEL_MAP_c_TO_c e, em seguida, substituirá o componente pelo valor que ele faz referência a essa tabela; <em>c</em> é R, G, B ou A, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d4395-124">If GL_MAP_COLOR is <strong>TRUE</strong>, <strong>glGetColorTableEXT</strong> scales each color component by the size of lookup table GL_PIXEL_MAP_c_TO_c, then replaces the component by the value that it references in that table; <em>c</em> is R, G, B, or A, respectively.</span></span></li>
<li><span data-ttu-id="d4395-125">A função <strong>glGetColorTableEXT</strong> converte as cores de RGBA resultantes em fragmentos, anexando as coordenadas de coordenadas z e de textura atuais a cada pixel, atribuindo coordenadas de janela <em>x</em> e <em>y</em> ao fragmento <em>n</em>-ésimo, como <em>x</em>?</span><span class="sxs-lookup"><span data-stu-id="d4395-125">The <strong>glGetColorTableEXT</strong> function converts the resulting RGBA colors to fragments by attaching the current raster position z-coordinate and texture coordinates to each pixel, then assigning <em>x</em> and <em>y</em> window coordinates to the <em>n</em>th fragment, such that <em>x</em>?</span></span><span data-ttu-id="d4395-126"> = <em>largura</em> <em>x</em><sub>r</sub> + <em>n</em> mod</span><span class="sxs-lookup"><span data-stu-id="d4395-126"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>width</em></span></span><br/> <span data-ttu-id="d4395-127"><em>y</em>?</span><span class="sxs-lookup"><span data-stu-id="d4395-127"><em>y</em>?</span></span><span data-ttu-id="d4395-128"> = <em>y</em><sub>r</sub> + <em>n/largura</em></span><span class="sxs-lookup"><span data-stu-id="d4395-128"> = <em>y</em><sub>r</sub> + <em>n/width</em></span></span><br/> <span data-ttu-id="d4395-129">onde (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) é a posição atual da varredura.</span><span class="sxs-lookup"><span data-stu-id="d4395-129">where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position.</span></span><br/></li>
<li><span data-ttu-id="d4395-130">Esses fragmentos de pixel são tratados exatamente como os fragmentos gerados pela rasterização de pontos, linhas ou polígonos.</span><span class="sxs-lookup"><span data-stu-id="d4395-130">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="d4395-131">A função <strong>glGetColorTableEXT</strong> aplica o mapeamento de textura, sombra e todas as operações de fragmento antes de gravar os fragmentos no framebuffer.</span><span class="sxs-lookup"><span data-stu-id="d4395-131">The <strong>glGetColorTableEXT</strong> function applies texture mapping, fog, and all the fragment operations before writing the fragments to the framebuffer.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="d4395-132"><dt><strong>GL_RED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d4395-132"><dt><strong>GL_RED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="d4395-133">Cada pixel é um único componente vermelho.</span><span class="sxs-lookup"><span data-stu-id="d4395-133">Each pixel is a single red component.</span></span><br/> <span data-ttu-id="d4395-134">A função <strong>glGetColorTableEXT</strong> converte esse componente no formato interno da mesma maneira que o componente vermelho de um pixel RGBA, em seguida, converte-o em um pixel RGBA com verde e azul definido como 0,0 e alfa definido como 1,0.</span><span class="sxs-lookup"><span data-stu-id="d4395-134">The <strong>glGetColorTableEXT</strong> function converts this component to the internal format in the same way that the red component of an RGBA pixel is, then converts it to an RGBA pixel with green and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="d4395-135">Após essa conversão, o pixel é tratado da mesma forma como se tivesse sido lido como um pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="d4395-135">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="d4395-136"><dt><strong>GL_GREEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d4395-136"><dt><strong>GL_GREEN</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="d4395-137">Cada pixel é um único componente verde.</span><span class="sxs-lookup"><span data-stu-id="d4395-137">Each pixel is a single green component.</span></span><br/> <span data-ttu-id="d4395-138">A função <strong>glGetColorTableEXT</strong> converte esse componente no formato interno da mesma forma que o componente verde de um pixel RGBA e, em seguida, converte-o em um pixel RGBA com vermelho e azul definido como 0,0 e alfa definido como 1,0.</span><span class="sxs-lookup"><span data-stu-id="d4395-138">The <strong>glGetColorTableEXT</strong> function converts this component to the internal format in the same way that the green component of an RGBA pixel is, and then converts it to an RGBA pixel with red and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="d4395-139">Após essa conversão, o pixel é tratado da mesma forma como se tivesse sido lido como um pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="d4395-139">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="d4395-140"><dt><strong>GL_BLUE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d4395-140"><dt><strong>GL_BLUE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="d4395-141">Cada pixel é um único componente azul.</span><span class="sxs-lookup"><span data-stu-id="d4395-141">Each pixel is a single blue component.</span></span><br/> <span data-ttu-id="d4395-142">A função <strong>glGetColorTableEXT</strong> converte esse componente no formato interno da mesma forma que o componente azul de um pixel RGBA e, em seguida, converte-o em um pixel RGBA com vermelho e verde definido como 0,0 e alfa definido como 1,0.</span><span class="sxs-lookup"><span data-stu-id="d4395-142">The <strong>glGetColorTableEXT</strong> function converts this component to the internal format in the same way that the blue component of an RGBA pixel is, and then converts it to an RGBA pixel with red and green set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="d4395-143">Após essa conversão, o pixel é tratado da mesma forma como se tivesse sido lido como um pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="d4395-143">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="d4395-144"><dt><strong>GL_ALPHA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d4395-144"><dt><strong>GL_ALPHA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="d4395-145">Cada pixel é um único componente alfa.</span><span class="sxs-lookup"><span data-stu-id="d4395-145">Each pixel is a single alpha component.</span></span><br/> <span data-ttu-id="d4395-146">A função <strong>glGetColorTableEXT</strong> converte esse componente no formato interno da mesma forma que o componente alfa de um pixel RGBA e, em seguida, converte-o em um pixel RGBA com vermelho, verde e azul definido como 0,0.</span><span class="sxs-lookup"><span data-stu-id="d4395-146">The <strong>glGetColorTableEXT</strong> function converts this component to the internal format in the same way that the alpha component of an RGBA pixel is, and then converts it to an RGBA pixel with red, green, and blue set to 0.0.</span></span> <span data-ttu-id="d4395-147">Após essa conversão, o pixel é tratado da mesma forma como se tivesse sido lido como um pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="d4395-147">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="d4395-148"><dt><strong>GL_RGB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d4395-148"><dt><strong>GL_RGB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="d4395-149">Cada pixel é um grupo de três componentes nesta ordem: vermelho, verde, azul.</span><span class="sxs-lookup"><span data-stu-id="d4395-149">Each pixel is a group of three components in this order: red, green, blue.</span></span><br/> <span data-ttu-id="d4395-150">A função <strong>glGetColorTableEXT</strong> converte cada componente no formato interno da mesma maneira que os componentes vermelho, verde e azul de um pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="d4395-150">The <strong>glGetColorTableEXT</strong> function converts each component to the internal format in the same way that the red, green, and blue components of an RGBA pixel are.</span></span> <span data-ttu-id="d4395-151">A cor tripla é convertida em um pixel RGBA com alfa definido como 1,0.</span><span class="sxs-lookup"><span data-stu-id="d4395-151">The color triple is converted to an RGBA pixel with alpha set to 1.0.</span></span> <span data-ttu-id="d4395-152">Após essa conversão, o pixel é tratado da mesma forma como se tivesse sido lido como um pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="d4395-152">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="d4395-153"><dt><strong>GL_BGR_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d4395-153"><dt><strong>GL_BGR_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="d4395-154">Cada pixel é um grupo de três componentes nesta ordem: azul, verde e vermelho.</span><span class="sxs-lookup"><span data-stu-id="d4395-154">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="d4395-155">GL_BGR_EXT fornece um formato que corresponde ao layout de memória dos bitmaps independentes de dispositivo do Microsoft Windows (DIBs).</span><span class="sxs-lookup"><span data-stu-id="d4395-155">GL_BGR_EXT provides a format that matches the memory layout of Microsoft Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="d4395-156">Portanto, seus aplicativos podem usar os mesmos dados com chamadas de função do Windows e chamadas de função de pixel OpenGL.</span><span class="sxs-lookup"><span data-stu-id="d4395-156">Thus, your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="d4395-157"><dt><strong>GL_BGRA_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d4395-157"><dt><strong>GL_BGRA_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="d4395-158">Cada pixel é um grupo de quatro componentes nesta ordem: azul, verde, vermelho, alfa.</span><span class="sxs-lookup"><span data-stu-id="d4395-158">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span><br/> <span data-ttu-id="d4395-159">GL_BGRA_EXT fornece um formato que corresponde ao layout de memória dos bitmaps independentes de dispositivo do Windows (DIBs).</span><span class="sxs-lookup"><span data-stu-id="d4395-159">GL_BGRA_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="d4395-160">Assim, seus aplicativos podem usar os mesmos dados com chamadas de função do Windows e chamadas de função de pixel OpenGL.</span><span class="sxs-lookup"><span data-stu-id="d4395-160">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="d4395-161">*tipo*</span><span class="sxs-lookup"><span data-stu-id="d4395-161">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="d4395-162">O tipo de dados para *dados*.</span><span class="sxs-lookup"><span data-stu-id="d4395-162">The data type for *data*.</span></span> <span data-ttu-id="d4395-163">A seguir estão as constantes simbólicas aceitas e seus significados.</span><span class="sxs-lookup"><span data-stu-id="d4395-163">The following are the accepted symbolic constants and their meanings.</span></span>



| <span data-ttu-id="d4395-164">Valor</span><span class="sxs-lookup"><span data-stu-id="d4395-164">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="d4395-165">Significado</span><span class="sxs-lookup"><span data-stu-id="d4395-165">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <span data-ttu-id="d4395-166"><dt>**\_byte não assinado GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d4395-166"><dt>**GL\_UNSIGNED\_BYTE**</dt></span></span> </dl>    | <span data-ttu-id="d4395-167">Inteiro de 8 bits sem sinal</span><span class="sxs-lookup"><span data-stu-id="d4395-167">Unsigned 8-bit integer</span></span><br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <span data-ttu-id="d4395-168"><dt>**\_byte GL**</dt></span><span class="sxs-lookup"><span data-stu-id="d4395-168"><dt>**GL\_BYTE**</dt></span></span> </dl>                                | <span data-ttu-id="d4395-169">Inteiro de 8 bits com sinal</span><span class="sxs-lookup"><span data-stu-id="d4395-169">Signed 8-bit integer</span></span><br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <span data-ttu-id="d4395-170"><dt>**GL \_ não assinado \_ curto**</dt></span><span class="sxs-lookup"><span data-stu-id="d4395-170"><dt>**GL\_UNSIGNED\_SHORT**</dt></span></span> </dl> | <span data-ttu-id="d4395-171">Inteiro de 16 bits sem sinal</span><span class="sxs-lookup"><span data-stu-id="d4395-171">Unsigned 16-bit integer</span></span><br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <span data-ttu-id="d4395-172"><dt>**GL \_ curto**</dt></span><span class="sxs-lookup"><span data-stu-id="d4395-172"><dt>**GL\_SHORT**</dt></span></span> </dl>                             | <span data-ttu-id="d4395-173">Inteiro de 16 bits com sinal</span><span class="sxs-lookup"><span data-stu-id="d4395-173">Signed 16-bit integer</span></span><br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <span data-ttu-id="d4395-174"><dt>**GL \_ não assinado \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="d4395-174"><dt>**GL\_UNSIGNED\_INT**</dt></span></span> </dl>       | <span data-ttu-id="d4395-175">Inteiro de 32 bits sem sinal</span><span class="sxs-lookup"><span data-stu-id="d4395-175">Unsigned 32-bit integer</span></span><br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <span data-ttu-id="d4395-176"><dt>**RAZÃO \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="d4395-176"><dt>**GL\_INT**</dt></span></span> </dl>                                   | <span data-ttu-id="d4395-177">Inteiro de 32 bits</span><span class="sxs-lookup"><span data-stu-id="d4395-177">32-bit integer</span></span><br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <span data-ttu-id="d4395-178"><dt>**GL \_ float**</dt></span><span class="sxs-lookup"><span data-stu-id="d4395-178"><dt>**GL\_FLOAT**</dt></span></span> </dl>                             | <span data-ttu-id="d4395-179">Valor do ponto flutuante de precisão simples</span><span class="sxs-lookup"><span data-stu-id="d4395-179">Single-precision floating-point value</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d4395-180">*data*</span><span class="sxs-lookup"><span data-stu-id="d4395-180">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="d4395-181">Aponta para o local onde as informações da tabela de cores retornadas são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="d4395-181">Points to the location where returned color table information is to be stored.</span></span> <span data-ttu-id="d4395-182">Cada entrada da tabela de cores é armazenada como se fosse um único pixel de uma textura 1D.</span><span class="sxs-lookup"><span data-stu-id="d4395-182">Each color table entry is stored as if it was a single pixel of a 1-D texture.</span></span> <span data-ttu-id="d4395-183">Como todas as texturas têm uma paleta padrão, **glGetColorTableEXT** sempre retorna informações de paleta, mesmo que os dados de textura não estejam em um formato de paleta.</span><span class="sxs-lookup"><span data-stu-id="d4395-183">Because all textures have a default palette, **glGetColorTableEXT** always returns palette information even if the texture data is not in a paletted format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4395-184">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d4395-184">Return value</span></span>

<span data-ttu-id="d4395-185">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d4395-185">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d4395-186">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="d4395-186">Error codes</span></span>

<span data-ttu-id="d4395-187">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="d4395-187">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="d4395-188">Nome</span><span class="sxs-lookup"><span data-stu-id="d4395-188">Name</span></span>                                                                                                  | <span data-ttu-id="d4395-189">Significado</span><span class="sxs-lookup"><span data-stu-id="d4395-189">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d4395-190"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="d4395-190"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="d4395-191">o *destino*, o *formato* ou o *tipo* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="d4395-191">*target*, *format*, or *type* was not an accepted value.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="d4395-192"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d4395-192"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d4395-193">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="d4395-193">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d4395-194">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4395-194">Remarks</span></span>

<span data-ttu-id="d4395-195">A função **glGetColorTableEXT** Obtém os dados da tabela de cores real especificados por [**glColorTableEXT**](glcolortableext.md) e [**glColorSubTableEXT**](glcolorsubtableext.md).</span><span class="sxs-lookup"><span data-stu-id="d4395-195">The **glGetColorTableEXT** function gets the actual color table data specified by [**glColorTableEXT**](glcolortableext.md) and [**glColorSubTableEXT**](glcolorsubtableext.md).</span></span>

<span data-ttu-id="d4395-196">A função **glGetColorTableEXT** é uma função de extensão que não faz parte da biblioteca OpenGL padrão, mas faz parte da extensão de textura da paleta do GL \_ ext \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d4395-196">The **glGetColorTableEXT** function is an extension function that is not part of the standard OpenGL library but is part of the GL\_EXT\_paletted\_texture extension.</span></span> <span data-ttu-id="d4395-197">Para verificar se a implementação do OpenGL dá suporte a **glGetColorTableEXT**, chame [**glGetString**](glgetstring.md)( \_ extensões GL).</span><span class="sxs-lookup"><span data-stu-id="d4395-197">To check whether your implementation of OpenGL supports **glGetColorTableEXT**, call [**glGetString**](glgetstring.md)(GL\_EXTENSIONS).</span></span> <span data-ttu-id="d4395-198">Se ele retornar a \_ textura da paleta do GL ext \_ \_ , haverá suporte para **glGetColorTableEXT** .</span><span class="sxs-lookup"><span data-stu-id="d4395-198">If it returns GL\_EXT\_paletted\_texture, **glGetColorTableEXT** is supported.</span></span> <span data-ttu-id="d4395-199">Para obter o endereço da função de uma função de extensão, chame [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span><span class="sxs-lookup"><span data-stu-id="d4395-199">To obtain the function address of an extension function, call [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4395-200">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4395-200">Requirements</span></span>



| <span data-ttu-id="d4395-201">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4395-201">Requirement</span></span> | <span data-ttu-id="d4395-202">Valor</span><span class="sxs-lookup"><span data-stu-id="d4395-202">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="d4395-203">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4395-203">Minimum supported client</span></span><br/> | <span data-ttu-id="d4395-204">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d4395-204">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="d4395-205">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4395-205">Minimum supported server</span></span><br/> | <span data-ttu-id="d4395-206">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d4395-206">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="d4395-207">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d4395-207">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4395-208"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4395-208"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4395-209">Confira também</span><span class="sxs-lookup"><span data-stu-id="d4395-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4395-210">**glColorSubTableEXT**</span><span class="sxs-lookup"><span data-stu-id="d4395-210">**glColorSubTableEXT**</span></span>](glcolorsubtableext.md)
</dt> <dt>

[<span data-ttu-id="d4395-211">**glColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="d4395-211">**glColorTableEXT**</span></span>](glcolortableext.md)
</dt> <dt>

[<span data-ttu-id="d4395-212">**glGetColorTableParameterfvEXT**</span><span class="sxs-lookup"><span data-stu-id="d4395-212">**glGetColorTableParameterfvEXT**</span></span>](glgetcolortableparameterfvext.md)
</dt> <dt>

[<span data-ttu-id="d4395-213">**glGetColorTableParameterivEXT**</span><span class="sxs-lookup"><span data-stu-id="d4395-213">**glGetColorTableParameterivEXT**</span></span>](glgetcolortableparameterivext.md)
</dt> <dt>

[<span data-ttu-id="d4395-214">**wglGetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="d4395-214">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





