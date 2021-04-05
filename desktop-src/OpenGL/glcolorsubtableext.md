---
title: função glColorSubTableEXT (GL. h)
description: A função glColorSubTableEXT especifica uma parte da paleta da textura de destino a ser substituída.
ms.assetid: 21430245-f837-4c7a-944f-b44482254b12
keywords:
- função glColorSubTableEXT OpenGL
topic_type:
- apiref
api_name:
- glColorSubTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a0386bda82bf08ae778d20b1be69858698ac7bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824495"
---
# <a name="glcolorsubtableext-function"></a><span data-ttu-id="474fc-104">função glColorSubTableEXT</span><span class="sxs-lookup"><span data-stu-id="474fc-104">glColorSubTableEXT function</span></span>

<span data-ttu-id="474fc-105">A função **glColorSubTableEXT** especifica uma parte da paleta da textura de destino a ser substituída.</span><span class="sxs-lookup"><span data-stu-id="474fc-105">The **glColorSubTableEXT** function specifies a portion of the targeted texture's palette to be replaced.</span></span>

## <a name="syntax"></a><span data-ttu-id="474fc-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="474fc-106">Syntax</span></span>


```C++
void WINAPI glColorSubTableEXT(
         GLenum  target,
         GLsizei start,
         GLsizei count,
         GLenum  format,
         GLenum  type,
   const GLvoid  *data
);
```



## <a name="parameters"></a><span data-ttu-id="474fc-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="474fc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="474fc-108">*destino*</span><span class="sxs-lookup"><span data-stu-id="474fc-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="474fc-109">A textura da paleta de destino que deve ter sua paleta alterada.</span><span class="sxs-lookup"><span data-stu-id="474fc-109">The target paletted texture that is to have its palette changed.</span></span> <span data-ttu-id="474fc-110">Deve ser textura \_ 1D ou 2D de textura \_ .</span><span class="sxs-lookup"><span data-stu-id="474fc-110">Must be TEXTURE\_1D or TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="474fc-111">*start*</span><span class="sxs-lookup"><span data-stu-id="474fc-111">*start*</span></span> 
</dt> <dd>

<span data-ttu-id="474fc-112">A entrada de índice da paleta inicial da paleta a ser alterada.</span><span class="sxs-lookup"><span data-stu-id="474fc-112">The starting palette index entry of the palette to be changed.</span></span>

</dd> <dt>

<span data-ttu-id="474fc-113">*contagem*</span><span class="sxs-lookup"><span data-stu-id="474fc-113">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="474fc-114">O número de entradas de índice de paleta da paleta a ser alterada começando no *início*.</span><span class="sxs-lookup"><span data-stu-id="474fc-114">The number of palette index entries of the palette to be changed beginning at *start*.</span></span> <span data-ttu-id="474fc-115">O parâmetro *Count* determina o intervalo de entradas de índice de paleta que são alteradas.</span><span class="sxs-lookup"><span data-stu-id="474fc-115">The *count* parameter determines the range of palette index entries that are changed.</span></span>

</dd> <dt>

<span data-ttu-id="474fc-116">*format*</span><span class="sxs-lookup"><span data-stu-id="474fc-116">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="474fc-117">O formato dos dados de pixel.</span><span class="sxs-lookup"><span data-stu-id="474fc-117">The format of the pixel data.</span></span> <span data-ttu-id="474fc-118">As constantes simbólicas a seguir são aceitas.</span><span class="sxs-lookup"><span data-stu-id="474fc-118">The following symbolic constants are accepted.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="474fc-119">Valor</span><span class="sxs-lookup"><span data-stu-id="474fc-119">Value</span></span></th>
<th><span data-ttu-id="474fc-120">Significado</span><span class="sxs-lookup"><span data-stu-id="474fc-120">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="474fc-121"><dt><strong>GL_RGBA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="474fc-121"><dt><strong>GL_RGBA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="474fc-122">Cada pixel é um grupo de quatro componentes na seguinte ordem: vermelho, verde, azul, alfa.</span><span class="sxs-lookup"><span data-stu-id="474fc-122">Each pixel is a group of four components in the following order: red, green, blue, alpha.</span></span> <span data-ttu-id="474fc-123">O formato RGBA é determinado dessa maneira:</span><span class="sxs-lookup"><span data-stu-id="474fc-123">The RGBA format is determined in this way:</span></span> <br/>
<ol>
<li><span data-ttu-id="474fc-124">A função <strong>glColorSubTableEXT</strong> converte valores de ponto flutuante diretamente em um formato interno com precisão não especificada.</span><span class="sxs-lookup"><span data-stu-id="474fc-124">The <strong>glColorSubTableEXT</strong> function converts floating-point values directly to an internal format with unspecified precision.</span></span> <span data-ttu-id="474fc-125">Valores inteiros assinados são mapeados linearmente para o formato interno, de modo que o valor inteiro representável mais positivo seja mapeado para 1,0 e o valor reapresentável mais negativo seja mapeado para-1,0.</span><span class="sxs-lookup"><span data-stu-id="474fc-125">Signed integer values are mapped linearly to the internal format such that the most positive representable integer value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="474fc-126">Os dados inteiros não assinados são mapeados da mesma forma: o maior valor inteiro é mapeado para 1,0 e zero é mapeado para 0,0.</span><span class="sxs-lookup"><span data-stu-id="474fc-126">Unsigned integer data is mapped similarly: the largest integer value maps to 1.0, and zero maps to 0.0.</span></span></li>
<li><span data-ttu-id="474fc-127">A função <strong>glColorSubTableEXT</strong> multiplica os valores de cor resultantes por GL_c_SCALE e os adiciona ao GL_c_BIAS, em que <em>c</em> é vermelho, verde, azul e alfa para os respectivos componentes de cor.</span><span class="sxs-lookup"><span data-stu-id="474fc-127">The <strong>glColorSubTableEXT</strong> function multiplies the resulting color values by GL_c_SCALE and adds them to GL_c_BIAS, where <em>c</em> is RED, GREEN, BLUE, and ALPHA for the respective color components.</span></span> <span data-ttu-id="474fc-128">Os resultados são clamped para o intervalo [0, 1].</span><span class="sxs-lookup"><span data-stu-id="474fc-128">The results are clamped to the range [0,1].</span></span></li>
<li><span data-ttu-id="474fc-129">Se GL_MAP_COLOR for <strong>true</strong>, <strong>glColorSubTableEXT</strong> dimensionará cada componente de cor pelo tamanho da tabela de pesquisa GL_PIXEL_MAP_c_TO_c e, em seguida, substituirá o componente pelo valor que ele faz referência a essa tabela; <em>c</em> é R, G, B ou A, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="474fc-129">If GL_MAP_COLOR is <strong>TRUE</strong>, <strong>glColorSubTableEXT</strong> scales each color component by the size of lookup table GL_PIXEL_MAP_c_TO_c, then replaces the component by the value that it references in that table; <em>c</em> is R, G, B, or A, respectively.</span></span></li>
<li><span data-ttu-id="474fc-130">A função <strong>glColorSubTableEXT</strong> converte as cores de RGBA resultantes em fragmentos anexando as coordenadas de coordenadas <em>z</em>e de textura atuais a cada pixel e, em seguida, atribuindo coordenadas de janela <em>x</em> e <em>y</em> ao <em>n</em>º de fragmento como<em>x</em>?</span><span class="sxs-lookup"><span data-stu-id="474fc-130">The <strong>glColorSubTableEXT</strong> function converts the resulting RGBA colors to fragments by attaching the current raster position <em>z</em>-coordinate and texture coordinates to each pixel, then assigning <em>x</em> and <em>y</em> window coordinates to the <em>n</em>th fragment such that<em>x</em>?</span></span><span data-ttu-id="474fc-131"> = <em>largura</em> <em>x</em><sub>r</sub> + <em>n</em> mod</span><span class="sxs-lookup"><span data-stu-id="474fc-131"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>width</em></span></span><br/> <span data-ttu-id="474fc-132"><em>y</em>?</span><span class="sxs-lookup"><span data-stu-id="474fc-132"><em>y</em>?</span></span><span data-ttu-id="474fc-133"> = <em>y</em><sub>r</sub> +<em>n/largura</em></span><span class="sxs-lookup"><span data-stu-id="474fc-133"> = <em>y</em><sub>r</sub> +<em>n / width</em></span></span><br/> <span data-ttu-id="474fc-134">onde (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) é a posição atual da varredura.</span><span class="sxs-lookup"><span data-stu-id="474fc-134">where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position.</span></span><br/></li>
<li><span data-ttu-id="474fc-135">Esses fragmentos de pixel são tratados exatamente como os fragmentos gerados pela rasterização de pontos, linhas ou polígonos.</span><span class="sxs-lookup"><span data-stu-id="474fc-135">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="474fc-136">A função <strong>glColorSubTableEXT</strong> aplica o mapeamento de textura, sombra e todas as operações de fragmento antes de gravar os fragmentos no framebuffer.</span><span class="sxs-lookup"><span data-stu-id="474fc-136">The <strong>glColorSubTableEXT</strong> function applies texture mapping, fog, and all the fragment operations before writing the fragments to the framebuffer.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="474fc-137"><dt><strong>GL_RED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="474fc-137"><dt><strong>GL_RED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="474fc-138">Cada pixel é um único componente vermelho.</span><span class="sxs-lookup"><span data-stu-id="474fc-138">Each pixel is a single red component.</span></span><br/> <span data-ttu-id="474fc-139">A função <strong>glColorSubTableEXT</strong> converte esse componente no formato interno da mesma maneira que o componente vermelho de um pixel RGBA, em seguida, converte-o em um pixel RGBA com verde e azul definido como 0,0 e alfa definido como 1,0.</span><span class="sxs-lookup"><span data-stu-id="474fc-139">The <strong>glColorSubTableEXT</strong> function converts this component to the internal format in the same way that the red component of an RGBA pixel is, then converts it to an RGBA pixel with green and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="474fc-140">Após essa conversão, o pixel é tratado da mesma forma como se tivesse sido lido como um pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="474fc-140">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="474fc-141"><dt><strong>GL_GREEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="474fc-141"><dt><strong>GL_GREEN</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="474fc-142">Cada pixel é um único componente verde.</span><span class="sxs-lookup"><span data-stu-id="474fc-142">Each pixel is a single green component.</span></span><br/> <span data-ttu-id="474fc-143">A função <strong>glColorSubTableEXT</strong> converte esse componente no formato interno da mesma forma que o componente verde de um pixel RGBA e, em seguida, converte-o em um pixel RGBA com vermelho e azul definido como 0,0 e alfa definido como 1,0.</span><span class="sxs-lookup"><span data-stu-id="474fc-143">The <strong>glColorSubTableEXT</strong> function converts this component to the internal format in the same way that the green component of an RGBA pixel is, and then converts it to an RGBA pixel with red and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="474fc-144">Após essa conversão, o pixel é tratado da mesma forma como se tivesse sido lido como um pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="474fc-144">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="474fc-145"><dt><strong>GL_BLUE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="474fc-145"><dt><strong>GL_BLUE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="474fc-146">Cada pixel é um único componente azul.</span><span class="sxs-lookup"><span data-stu-id="474fc-146">Each pixel is a single blue component.</span></span><br/> <span data-ttu-id="474fc-147">A função <strong>glColorSubTableEXT</strong> converte esse componente no formato interno da mesma forma que o componente azul de um pixel RGBA e, em seguida, converte-o em um pixel RGBA com vermelho e verde definido como 0,0 e alfa definido como 1,0.</span><span class="sxs-lookup"><span data-stu-id="474fc-147">The <strong>glColorSubTableEXT</strong> function converts this component to the internal format in the same way that the blue component of an RGBA pixel is, and then converts it to an RGBA pixel with red and green set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="474fc-148">Após essa conversão, o pixel é tratado da mesma forma como se tivesse sido lido como um pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="474fc-148">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="474fc-149"><dt><strong>GL_ALPHA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="474fc-149"><dt><strong>GL_ALPHA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="474fc-150">Cada pixel é um único componente alfa.</span><span class="sxs-lookup"><span data-stu-id="474fc-150">Each pixel is a single alpha component.</span></span><br/> <span data-ttu-id="474fc-151">A função <strong>glColorSubTableEXT</strong> converte esse componente no formato interno da mesma forma que o componente alfa de um pixel RGBA e, em seguida, converte-o em um pixel RGBA com vermelho, verde e azul definido como 0,0.</span><span class="sxs-lookup"><span data-stu-id="474fc-151">The <strong>glColorSubTableEXT</strong> function converts this component to the internal format in the same way that the alpha component of an RGBA pixel is, and then converts it to an RGBA pixel with red, green, and blue set to 0.0.</span></span> <span data-ttu-id="474fc-152">Após essa conversão, o pixel é tratado da mesma forma como se tivesse sido lido como um pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="474fc-152">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="474fc-153"><dt><strong>GL_RGB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="474fc-153"><dt><strong>GL_RGB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="474fc-154">Cada pixel é um grupo de três componentes nesta ordem: vermelho, verde, azul.</span><span class="sxs-lookup"><span data-stu-id="474fc-154">Each pixel is a group of three components in this order: red, green, blue.</span></span><br/> <span data-ttu-id="474fc-155">A função <strong>glColorSubTableEXT</strong> converte cada componente no formato interno da mesma maneira que os componentes vermelho, verde e azul de um pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="474fc-155">The <strong>glColorSubTableEXT</strong> function converts each component to the internal format in the same way that the red, green, and blue components of an RGBA pixel are.</span></span> <span data-ttu-id="474fc-156">A cor tripla é convertida em um pixel RGBA com alfa definido como 1,0.</span><span class="sxs-lookup"><span data-stu-id="474fc-156">The color triple is converted to an RGBA pixel with alpha set to 1.0.</span></span> <span data-ttu-id="474fc-157">Após essa conversão, o pixel é tratado da mesma forma como se tivesse sido lido como um pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="474fc-157">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="474fc-158"><dt><strong>GL_BGR_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="474fc-158"><dt><strong>GL_BGR_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="474fc-159">Cada pixel é um grupo de três componentes nesta ordem: azul, verde e vermelho.</span><span class="sxs-lookup"><span data-stu-id="474fc-159">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="474fc-160">GL_BGR_EXT fornece um formato que corresponde ao layout de memória dos bitmaps independentes de dispositivo do Windows (DIBs).</span><span class="sxs-lookup"><span data-stu-id="474fc-160">GL_BGR_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="474fc-161">Assim, seus aplicativos podem usar os mesmos dados com chamadas de função do Windows e chamadas de função de pixel OpenGL.</span><span class="sxs-lookup"><span data-stu-id="474fc-161">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="474fc-162"><dt><strong>GL_BGRA_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="474fc-162"><dt><strong>GL_BGRA_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="474fc-163">Cada pixel é um grupo de quatro componentes nesta ordem: azul, verde, vermelho, alfa.</span><span class="sxs-lookup"><span data-stu-id="474fc-163">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span><br/> <span data-ttu-id="474fc-164">GL_BGRA_EXT fornece um formato que corresponde ao layout de memória dos bitmaps independentes de dispositivo do Windows (DIBs).</span><span class="sxs-lookup"><span data-stu-id="474fc-164">GL_BGRA_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="474fc-165">Assim, seus aplicativos podem usar os mesmos dados com chamadas de função do Windows e chamadas de função de pixel OpenGL.</span><span class="sxs-lookup"><span data-stu-id="474fc-165">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="474fc-166">*tipo*</span><span class="sxs-lookup"><span data-stu-id="474fc-166">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="474fc-167">O tipo de dados para *dados*.</span><span class="sxs-lookup"><span data-stu-id="474fc-167">The data type for *data*.</span></span> <span data-ttu-id="474fc-168">As constantes simbólicas a seguir são aceitas: GL \_ não assinado \_ byte, GL \_ byte, GL \_ não assinado \_ curto, GL \_ curto, GL \_ não assinado \_ int, GL \_ int e GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="474fc-168">The following symbolic constants are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

<span data-ttu-id="474fc-169">A tabela a seguir resume o significado das constantes válidas para o parâmetro de *tipo* .</span><span class="sxs-lookup"><span data-stu-id="474fc-169">The following table summarizes the meaning of the valid constants for the *type* parameter.</span></span>



| <span data-ttu-id="474fc-170">Valor</span><span class="sxs-lookup"><span data-stu-id="474fc-170">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="474fc-171">Significado</span><span class="sxs-lookup"><span data-stu-id="474fc-171">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <span data-ttu-id="474fc-172"><dt>**\_byte não assinado GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="474fc-172"><dt>**GL\_UNSIGNED\_BYTE**</dt></span></span> </dl>    | <span data-ttu-id="474fc-173">Inteiro de 8 bits sem sinal</span><span class="sxs-lookup"><span data-stu-id="474fc-173">Unsigned 8-bit integer</span></span><br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <span data-ttu-id="474fc-174"><dt>**\_byte GL**</dt></span><span class="sxs-lookup"><span data-stu-id="474fc-174"><dt>**GL\_BYTE**</dt></span></span> </dl>                                | <span data-ttu-id="474fc-175">Inteiro de 8 bits com sinal</span><span class="sxs-lookup"><span data-stu-id="474fc-175">Signed 8-bit integer</span></span><br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <span data-ttu-id="474fc-176"><dt>**GL \_ não assinado \_ curto**</dt></span><span class="sxs-lookup"><span data-stu-id="474fc-176"><dt>**GL\_UNSIGNED\_SHORT**</dt></span></span> </dl> | <span data-ttu-id="474fc-177">Inteiro de 16 bits sem sinal</span><span class="sxs-lookup"><span data-stu-id="474fc-177">Unsigned 16-bit integer</span></span><br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <span data-ttu-id="474fc-178"><dt>**GL \_ curto**</dt></span><span class="sxs-lookup"><span data-stu-id="474fc-178"><dt>**GL\_SHORT**</dt></span></span> </dl>                             | <span data-ttu-id="474fc-179">Inteiro de 16 bits com sinal</span><span class="sxs-lookup"><span data-stu-id="474fc-179">Signed 16-bit integer</span></span><br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <span data-ttu-id="474fc-180"><dt>**GL \_ não assinado \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="474fc-180"><dt>**GL\_UNSIGNED\_INT**</dt></span></span> </dl>       | <span data-ttu-id="474fc-181">Inteiro de 32 bits sem sinal</span><span class="sxs-lookup"><span data-stu-id="474fc-181">Unsigned 32-bit integer</span></span><br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <span data-ttu-id="474fc-182"><dt>**RAZÃO \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="474fc-182"><dt>**GL\_INT**</dt></span></span> </dl>                                   | <span data-ttu-id="474fc-183">Inteiro de 32 bits</span><span class="sxs-lookup"><span data-stu-id="474fc-183">32-bit integer</span></span><br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <span data-ttu-id="474fc-184"><dt>**GL \_ float**</dt></span><span class="sxs-lookup"><span data-stu-id="474fc-184"><dt>**GL\_FLOAT**</dt></span></span> </dl>                             | <span data-ttu-id="474fc-185">Valor do ponto flutuante de precisão simples</span><span class="sxs-lookup"><span data-stu-id="474fc-185">Single-precision floating-point value</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="474fc-186">*data*</span><span class="sxs-lookup"><span data-stu-id="474fc-186">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="474fc-187">Um ponteiro para os dados de textura da paleta.</span><span class="sxs-lookup"><span data-stu-id="474fc-187">A pointer to the paletted texture data.</span></span> <span data-ttu-id="474fc-188">Os dados são tratados como pixels únicos de uma entrada de paleta de textura 1D para uma entrada de paleta.</span><span class="sxs-lookup"><span data-stu-id="474fc-188">The data is treated as single pixels of a 1-D texture palette entry for a palette entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="474fc-189">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="474fc-189">Return value</span></span>

<span data-ttu-id="474fc-190">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="474fc-190">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="474fc-191">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="474fc-191">Error codes</span></span>

<span data-ttu-id="474fc-192">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="474fc-192">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="474fc-193">Nome</span><span class="sxs-lookup"><span data-stu-id="474fc-193">Name</span></span>                                                                                              | <span data-ttu-id="474fc-194">Significado</span><span class="sxs-lookup"><span data-stu-id="474fc-194">Meaning</span></span>                                                                                                                               |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="474fc-195"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="474fc-195"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="474fc-196">*Start* ou *Count* foi um número inteiro inválido.</span><span class="sxs-lookup"><span data-stu-id="474fc-196">*start* or *count* was an invalid integer.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="474fc-197"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="474fc-197"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="474fc-198">o *destino*, o *formato* ou o *tipo* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="474fc-198">*target*, *format*,or *type* was not an accepted value.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="474fc-199"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="474fc-199"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="474fc-200">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="474fc-200">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="474fc-201">Comentários</span><span class="sxs-lookup"><span data-stu-id="474fc-201">Remarks</span></span>

<span data-ttu-id="474fc-202">A função **glColorSubTableEXT** especifica partes da paleta da textura de destino atual a serem substituídas.</span><span class="sxs-lookup"><span data-stu-id="474fc-202">The **glColorSubTableEXT** function specifies portions of the current targeted texture's palette to be replaced.</span></span> <span data-ttu-id="474fc-203">Ao contrário de [**glColorTableEXT**](glcolortableext.md), você não pode especificar o parâmetro de *destino* como uma paleta de textura de proxy.</span><span class="sxs-lookup"><span data-stu-id="474fc-203">Unlike [**glColorTableEXT**](glcolortableext.md), you cannot specify the *target* parameter to be a proxy texture palette.</span></span>

> [!Note]  
> <span data-ttu-id="474fc-204">A função **glColorSubTableEXT** é uma função de extensão que não faz parte da biblioteca OpenGL padrão, mas faz parte da extensão de textura da paleta do GL \_ ext \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="474fc-204">The **glColorSubTableEXT** function is an extension function that is not part of the standard OpenGL library but is part of the GL\_EXT\_paletted\_texture extension.</span></span> <span data-ttu-id="474fc-205">Para verificar se a implementação do OpenGL dá suporte a **glColorSubTableEXT**, chame [**glGetString**](glgetstring.md)( \_ extensões GL).</span><span class="sxs-lookup"><span data-stu-id="474fc-205">To check whether your implementation of OpenGL supports **glColorSubTableEXT**, call [**glGetString**](glgetstring.md)(GL\_EXTENSIONS).</span></span> <span data-ttu-id="474fc-206">Se ele retornar a \_ textura da paleta do GL ext \_ \_ , haverá suporte para **glColorSubTableEXT** .</span><span class="sxs-lookup"><span data-stu-id="474fc-206">If it returns GL\_EXT\_paletted\_texture, **glColorSubTableEXT** is supported.</span></span> <span data-ttu-id="474fc-207">Para obter o endereço da função de uma função de extensão, chame [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span><span class="sxs-lookup"><span data-stu-id="474fc-207">To obtain the function address of an extension function, call [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="474fc-208">Requisitos</span><span class="sxs-lookup"><span data-stu-id="474fc-208">Requirements</span></span>



| <span data-ttu-id="474fc-209">Requisito</span><span class="sxs-lookup"><span data-stu-id="474fc-209">Requirement</span></span> | <span data-ttu-id="474fc-210">Valor</span><span class="sxs-lookup"><span data-stu-id="474fc-210">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="474fc-211">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="474fc-211">Minimum supported client</span></span><br/> | <span data-ttu-id="474fc-212">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="474fc-212">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="474fc-213">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="474fc-213">Minimum supported server</span></span><br/> | <span data-ttu-id="474fc-214">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="474fc-214">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="474fc-215">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="474fc-215">Header</span></span><br/>                   | <dl> <span data-ttu-id="474fc-216"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="474fc-216"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="474fc-217">Confira também</span><span class="sxs-lookup"><span data-stu-id="474fc-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="474fc-218">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="474fc-218">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="474fc-219">**glColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="474fc-219">**glColorTableEXT**</span></span>](glcolortableext.md)
</dt> <dt>

[<span data-ttu-id="474fc-220">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="474fc-220">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="474fc-221">**glGetColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="474fc-221">**glGetColorTableEXT**</span></span>](glgetcolortableext.md)
</dt> <dt>

[<span data-ttu-id="474fc-222">**glGetColorTableParameterfvEXT**</span><span class="sxs-lookup"><span data-stu-id="474fc-222">**glGetColorTableParameterfvEXT**</span></span>](glgetcolortableparameterfvext.md)
</dt> <dt>

[<span data-ttu-id="474fc-223">**glGetColorTableParameterivEXT**</span><span class="sxs-lookup"><span data-stu-id="474fc-223">**glGetColorTableParameterivEXT**</span></span>](glgetcolortableparameterivext.md)
</dt> <dt>

[<span data-ttu-id="474fc-224">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="474fc-224">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="474fc-225">**wglGetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="474fc-225">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





