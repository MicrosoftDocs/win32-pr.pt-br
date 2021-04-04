---
title: função glTexImage1D (GL. h)
description: A função glTexImage1D especifica uma imagem de textura unidimensional.
ms.assetid: 4f537b89-2ea2-4e2e-8c57-c372bf53f12c
keywords:
- função glTexImage1D OpenGL
topic_type:
- apiref
api_name:
- glTexImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1865d19c54b9c59654f07162d2480aa5b29c47f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009237"
---
# <a name="glteximage1d-function"></a><span data-ttu-id="03141-104">função glTexImage1D</span><span class="sxs-lookup"><span data-stu-id="03141-104">glTexImage1D function</span></span>

<span data-ttu-id="03141-105">A função **glTexImage1D** especifica uma imagem de textura unidimensional.</span><span class="sxs-lookup"><span data-stu-id="03141-105">The **glTexImage1D** function specifies a one-dimensional texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="03141-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="03141-106">Syntax</span></span>


```C++
void WINAPI glTexImage1D(
         GLenum  target,
         GLint   level,
         GLint   internalformat,
         GLsizei width,
         GLint   border,
         GLint   format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="03141-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="03141-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03141-108">*destino*</span><span class="sxs-lookup"><span data-stu-id="03141-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="03141-109">A textura de destino.</span><span class="sxs-lookup"><span data-stu-id="03141-109">The target texture.</span></span> <span data-ttu-id="03141-110">Deve ser GL \_ Texture \_ 1D.</span><span class="sxs-lookup"><span data-stu-id="03141-110">Must be GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="03141-111">*level*</span><span class="sxs-lookup"><span data-stu-id="03141-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="03141-112">O número de nível de detalhe.</span><span class="sxs-lookup"><span data-stu-id="03141-112">The level-of-detail number.</span></span> <span data-ttu-id="03141-113">Nível 0 é o nível de imagem base.</span><span class="sxs-lookup"><span data-stu-id="03141-113">Level 0 is the base image level.</span></span> <span data-ttu-id="03141-114">O nível *n* é a imagem de redução *n* º mipmap.</span><span class="sxs-lookup"><span data-stu-id="03141-114">Level *n* is the *n* Th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="03141-115">*internalformat*</span><span class="sxs-lookup"><span data-stu-id="03141-115">*internalformat*</span></span> 
</dt> <dd>

<span data-ttu-id="03141-116">Especifica o número de componentes de cor na textura.</span><span class="sxs-lookup"><span data-stu-id="03141-116">Specifies the number of color components in the texture.</span></span> <span data-ttu-id="03141-117">Deve ser 1, 2, 3 ou 4, ou uma das seguintes constantes simbólicas: GL \_ alfa, GL \_ ALPHA4, GL \_ ALPHA8, GL \_ ALPHA12, GL \_ ALPHA16, GL \_ luminescência, GL \_ LUMINANCE4, GL \_ LUMINANCE8, GL \_ LUMINANCE12, GL \_ LUMINANCE16, GL \_ luminância \_ alfa, GL \_ LUMINANCE4 \_ ALPHA4, GL \_ LUMINANCE6 \_ ALPHA2, GL \_ LUMINANCE8 \_ ALPHA8, GL \_ LUMINANCE12 \_ ALPHA4, GL \_ LUMINANCE12 \_ ALPHA12, GL \_ LUMINANCE16 \_ ALPHA16, GL \_ intensidade, GL \_ INTENSITY4, GL \_ INTENSITY8, GL \_ INTENSITY12, GL \_ INTENSITY16, GL \_ RGB, GL \_ R3 \_ G3 \_ B2, GL \_ RGB4, GL \_ RGB5, GL \_ RGB8, GL \_ RGB10, GL \_ RGB12, GL \_ RGB16, GL \_ RGBA, GL \_ RGBA2, GL RGBA4 \_ , GL \_ RGB5 \_ a1, GL \_ RGBA8, GL \_ RGB10 \_ a2, GL \_ RGBA12 ou GL \_ RGBA16.</span><span class="sxs-lookup"><span data-stu-id="03141-117">Must be 1, 2, 3, or 4, or one of the following symbolic constants: GL\_ALPHA, GL\_ALPHA4, GL\_ALPHA8, GL\_ALPHA12, GL\_ALPHA16, GL\_LUMINANCE, GL\_LUMINANCE4, GL\_LUMINANCE8, GL\_LUMINANCE12, GL\_LUMINANCE16, GL\_LUMINANCE\_ALPHA, GL\_LUMINANCE4\_ALPHA4, GL\_LUMINANCE6\_ALPHA2, GL\_LUMINANCE8\_ALPHA8, GL\_LUMINANCE12\_ALPHA4, GL\_LUMINANCE12\_ALPHA12, GL\_LUMINANCE16\_ALPHA16, GL\_INTENSITY, GL\_INTENSITY4, GL\_INTENSITY8, GL\_INTENSITY12, GL\_INTENSITY16, GL\_RGB, GL\_R3\_G3\_B2, GL\_RGB4, GL\_RGB5, GL\_RGB8, GL\_RGB10, GL\_RGB12, GL\_RGB16, GL\_RGBA, GL\_RGBA2, GL\_RGBA4, GL\_RGB5\_A1, GL\_RGBA8, GL\_RGB10\_A2, GL\_RGBA12, or GL\_RGBA16.</span></span>

</dd> <dt>

<span data-ttu-id="03141-118">*width*</span><span class="sxs-lookup"><span data-stu-id="03141-118">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="03141-119">A largura da imagem de textura.</span><span class="sxs-lookup"><span data-stu-id="03141-119">The width of the texture image.</span></span> <span data-ttu-id="03141-120">Deve ser 2 *n* + 2 ( *Border* ) para algum número inteiro *n*.</span><span class="sxs-lookup"><span data-stu-id="03141-120">Must be 2 *n* + 2( *border* ) for some integer *n*.</span></span> <span data-ttu-id="03141-121">A altura da imagem de textura é 1.</span><span class="sxs-lookup"><span data-stu-id="03141-121">The height of the texture image is 1.</span></span>

</dd> <dt>

<span data-ttu-id="03141-122">*borda*</span><span class="sxs-lookup"><span data-stu-id="03141-122">*border*</span></span> 
</dt> <dd>

<span data-ttu-id="03141-123">A largura da borda.</span><span class="sxs-lookup"><span data-stu-id="03141-123">The width of the border.</span></span> <span data-ttu-id="03141-124">Deve ser 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="03141-124">Must be either 0 or 1.</span></span>

</dd> <dt>

<span data-ttu-id="03141-125">*format*</span><span class="sxs-lookup"><span data-stu-id="03141-125">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="03141-126">O formato dos dados de pixel.</span><span class="sxs-lookup"><span data-stu-id="03141-126">The format of the pixel data.</span></span> <span data-ttu-id="03141-127">Ele pode assumir um dos nove valores simbólicos.</span><span class="sxs-lookup"><span data-stu-id="03141-127">It can assume one of nine symbolic values.</span></span>



| <span data-ttu-id="03141-128">Valor</span><span class="sxs-lookup"><span data-stu-id="03141-128">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="03141-129">Significado</span><span class="sxs-lookup"><span data-stu-id="03141-129">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <span data-ttu-id="03141-130"><dt>**\_índice de cores GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="03141-130"><dt>**GL\_COLOR\_INDEX**</dt></span></span> </dl>             | <span data-ttu-id="03141-131">Cada elemento é um único valor, um índice de cores.</span><span class="sxs-lookup"><span data-stu-id="03141-131">Each element is a single value, a color index.</span></span> <span data-ttu-id="03141-132">Ele é convertido em um ponto fixo (com um número não especificado de 0 bits à direita do ponto binário), deslocado para a esquerda ou para a direita, dependendo do valor e do sinal de \_ mudança de índice GL \_ e adicionado ao \_ deslocamento de índice GL \_ (consulte [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="03141-132">It is converted to fixed point (with an unspecified number of 0 bits to the right of the binary point), shifted left or right, depending on the value and sign of GL\_INDEX\_SHIFT, and added to GL\_INDEX\_OFFSET (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span> <span data-ttu-id="03141-133">O índice resultante é convertido em um conjunto de componentes de cor usando o \_ mapa de pixel GL \_ \_ i \_ para \_ R, o GL \_ pixel \_ map \_ i \_ para \_ G, GL \_ pixel \_ map \_ i \_ para \_ B e GL \_ pixel \_ MAP i \_ \_ para \_ tabelas e clamped para o intervalo \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="03141-133">The resulting index is converted to a set of color components using the GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, and GL\_PIXEL\_MAP\_I\_TO\_A tables, and clamped to the range \[0,1\].</span></span><br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="03141-134"><dt>**GL \_ vermelho**</dt></span><span class="sxs-lookup"><span data-stu-id="03141-134"><dt>**GL\_RED**</dt></span></span> </dl>                                      | <span data-ttu-id="03141-135">Cada elemento é um único componente vermelho.</span><span class="sxs-lookup"><span data-stu-id="03141-135">Each element is a single red component.</span></span> <span data-ttu-id="03141-136">Ele é convertido em ponto flutuante e montado em um elemento RGBA anexando 0,0 para verde e azul e 1,0 para alfa.</span><span class="sxs-lookup"><span data-stu-id="03141-136">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for green and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="03141-137">Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="03141-137">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="03141-138"><dt>**GL \_ verde**</dt></span><span class="sxs-lookup"><span data-stu-id="03141-138"><dt>**GL\_GREEN**</dt></span></span> </dl>                                | <span data-ttu-id="03141-139">Cada elemento é um único componente verde.</span><span class="sxs-lookup"><span data-stu-id="03141-139">Each element is a single green component.</span></span> <span data-ttu-id="03141-140">Ele é convertido em ponto flutuante e montado em um elemento RGBA anexando 0,0 para vermelho e azul e 1,0 para alfa.</span><span class="sxs-lookup"><span data-stu-id="03141-140">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="03141-141">Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="03141-141">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                         |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="03141-142"><dt>**\_azul GL**</dt></span><span class="sxs-lookup"><span data-stu-id="03141-142"><dt>**GL\_BLUE**</dt></span></span> </dl>                                   | <span data-ttu-id="03141-143">Cada elemento é um único componente azul.</span><span class="sxs-lookup"><span data-stu-id="03141-143">Each element is a single blue component.</span></span> <span data-ttu-id="03141-144">Ele é convertido em ponto flutuante e montado em um elemento RGBA anexando 0,0 para vermelho e verde e 1,0 para alfa.</span><span class="sxs-lookup"><span data-stu-id="03141-144">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red and green, and 1.0 for alpha.</span></span> <span data-ttu-id="03141-145">Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="03141-145">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="03141-146"><dt>**GL \_ alfa**</dt></span><span class="sxs-lookup"><span data-stu-id="03141-146"><dt>**GL\_ALPHA**</dt></span></span> </dl>                                | <span data-ttu-id="03141-147">Cada elemento é um único componente vermelho.</span><span class="sxs-lookup"><span data-stu-id="03141-147">Each element is a single red component.</span></span> <span data-ttu-id="03141-148">Ele é convertido em ponto flutuante e montado em um elemento RGBA anexando 0,0 para vermelho, verde e azul.</span><span class="sxs-lookup"><span data-stu-id="03141-148">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red, green, and blue.</span></span> <span data-ttu-id="03141-149">Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="03141-149">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                                      |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="03141-150"><dt>**GL em \_ RGB**</dt></span><span class="sxs-lookup"><span data-stu-id="03141-150"><dt>**GL\_RGB**</dt></span></span> </dl>                                      | <span data-ttu-id="03141-151">Cada elemento é um triplo RGB.</span><span class="sxs-lookup"><span data-stu-id="03141-151">Each element is an RGB triple.</span></span> <span data-ttu-id="03141-152">Ele é convertido em ponto flutuante e montado em um elemento RGBA anexando 1,0 para alfa.</span><span class="sxs-lookup"><span data-stu-id="03141-152">It is converted to floating point and assembled into an RGBA element by attaching 1.0 for alpha.</span></span> <span data-ttu-id="03141-153">Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="03141-153">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                     |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="03141-154"><dt>**Se \_ RGBA**</dt></span><span class="sxs-lookup"><span data-stu-id="03141-154"><dt>**GL\_RGBA**</dt></span></span> </dl>                                   | <span data-ttu-id="03141-155">Cada elemento é um elemento RGBA completo.</span><span class="sxs-lookup"><span data-stu-id="03141-155">Each element is a complete RGBA element.</span></span> <span data-ttu-id="03141-156">Ele é convertido em ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="03141-156">It is converted to floating point.</span></span> <span data-ttu-id="03141-157">Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="03141-157">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                                                                         |
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="03141-158"><dt>**\_BGR \_ ext. GL**</dt></span><span class="sxs-lookup"><span data-stu-id="03141-158"><dt>**GL\_BGR\_EXT**</dt></span></span> </dl>                         | <span data-ttu-id="03141-159">Cada pixel é um grupo de três componentes nesta ordem: azul, verde e vermelho.</span><span class="sxs-lookup"><span data-stu-id="03141-159">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="03141-160">GL \_ BGR \_ ext fornece um formato que corresponde ao layout de memória dos bitmaps independentes de dispositivo do Windows (DIBs).</span><span class="sxs-lookup"><span data-stu-id="03141-160">GL\_BGR\_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="03141-161">Assim, seus aplicativos podem usar os mesmos dados com chamadas de função do Windows e chamadas de função de pixel OpenGL.</span><span class="sxs-lookup"><span data-stu-id="03141-161">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/>                                                                                                                                                                                                                                      |
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="03141-162"><dt>**\_BGRA \_ ext. GL**</dt></span><span class="sxs-lookup"><span data-stu-id="03141-162"><dt>**GL\_BGRA\_EXT**</dt></span></span> </dl>                      | <span data-ttu-id="03141-163">Cada pixel é um grupo de quatro componentes nesta ordem: azul, verde, vermelho, alfa.</span><span class="sxs-lookup"><span data-stu-id="03141-163">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span><br/> <span data-ttu-id="03141-164">GL \_ BGRA \_ ext fornece um formato que corresponde ao layout de memória dos bitmaps independentes de dispositivo do Windows (DIBs).</span><span class="sxs-lookup"><span data-stu-id="03141-164">GL\_BGRA\_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="03141-165">Assim, seus aplicativos podem usar os mesmos dados com chamadas de função do Windows e chamadas de função de pixel OpenGL.</span><span class="sxs-lookup"><span data-stu-id="03141-165">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <span data-ttu-id="03141-166"><dt>**\_luminância GL**</dt></span><span class="sxs-lookup"><span data-stu-id="03141-166"><dt>**GL\_LUMINANCE**</dt></span></span> </dl>                    | <span data-ttu-id="03141-167">Cada elemento é um único valor de luminância.</span><span class="sxs-lookup"><span data-stu-id="03141-167">Each element is a single luminance value.</span></span> <span data-ttu-id="03141-168">Ele é convertido em ponto flutuante e, em seguida, montado em um elemento RGBA replicando o valor de luminância três vezes para vermelho, verde e azul e anexando 1,0 para alfa.</span><span class="sxs-lookup"><span data-stu-id="03141-168">It is converted to floating point, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue, and attaching 1.0 for alpha.</span></span> <span data-ttu-id="03141-169">Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="03141-169">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                   |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <span data-ttu-id="03141-170"><dt>**luminância do GL \_ \_ alfa**</dt></span><span class="sxs-lookup"><span data-stu-id="03141-170"><dt>**GL\_LUMINANCE\_ALPHA**</dt></span></span> </dl> | <span data-ttu-id="03141-171">Cada elemento é um par de luminância/alfa.</span><span class="sxs-lookup"><span data-stu-id="03141-171">Each element is a luminance/alpha pair.</span></span> <span data-ttu-id="03141-172">Ele é convertido em ponto flutuante e, em seguida, montado em um elemento RGBA replicando o valor de luminância três vezes para vermelho, verde e azul.</span><span class="sxs-lookup"><span data-stu-id="03141-172">It is converted to floating point, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue.</span></span> <span data-ttu-id="03141-173">Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="03141-173">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="03141-174">*tipo*</span><span class="sxs-lookup"><span data-stu-id="03141-174">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="03141-175">O tipo de dados dos dados de pixel.</span><span class="sxs-lookup"><span data-stu-id="03141-175">The data type of the pixel data.</span></span> <span data-ttu-id="03141-176">Os seguintes valores simbólicos são aceitos: GL \_ não assinado \_ byte, GL byte, renomear \_ \_ bitmap, GL \_ não assinado \_ curto, GL \_ curto, GL \_ não assinado \_ int, GL \_ int e GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="03141-176">The following symbolic values are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="03141-177">*pixels*</span><span class="sxs-lookup"><span data-stu-id="03141-177">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="03141-178">Um ponteiro para os dados da imagem na memória.</span><span class="sxs-lookup"><span data-stu-id="03141-178">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03141-179">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="03141-179">Return value</span></span>

<span data-ttu-id="03141-180">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="03141-180">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="03141-181">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="03141-181">Error codes</span></span>

<span data-ttu-id="03141-182">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="03141-182">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="03141-183">Nome</span><span class="sxs-lookup"><span data-stu-id="03141-183">Name</span></span>                                                                                                  | <span data-ttu-id="03141-184">Significado</span><span class="sxs-lookup"><span data-stu-id="03141-184">Meaning</span></span>                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="03141-185"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="03141-185"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="03141-186">o *destino* não era uma \_ textura GL.</span><span class="sxs-lookup"><span data-stu-id="03141-186">*target* was not an GL\_TEXTURE.</span></span><br/>                                                                                                                                                                                    |
| <dl> <span data-ttu-id="03141-187"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="03141-187"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="03141-188">o *formato* não era uma constante de *formato* aceito.</span><span class="sxs-lookup"><span data-stu-id="03141-188">*format* was not an accepted *format* constant.</span></span> <span data-ttu-id="03141-189">Somente as constantes de formato diferentes do \_ índice de estêncil GL e do \_ \_ componente de profundidade GL \_ são aceitas.</span><span class="sxs-lookup"><span data-stu-id="03141-189">Only format constants other than GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT are accepted.</span></span> <span data-ttu-id="03141-190">Consulte a descrição do parâmetro do *formato* para obter uma lista de valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="03141-190">See the parameter description of *format* for a list of possible values.</span></span><br/> |
| <dl> <span data-ttu-id="03141-191"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="03141-191"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="03141-192">o *tipo* não era uma constante de *tipo* .</span><span class="sxs-lookup"><span data-stu-id="03141-192">*type* was not a *type* constant.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="03141-193"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="03141-193"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="03141-194">o *tipo* was \_ bitmap GL e *Format* não era um índice de \_ cores GL \_ .</span><span class="sxs-lookup"><span data-stu-id="03141-194">*type* was GL\_BITMAP and *format* was not GL\_COLOR\_INDEX.</span></span><br/>                                                                                                                                                        |
| <dl> <span data-ttu-id="03141-195"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="03141-195"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="03141-196">o *nível* era menor que zero ou maior que log2 *Max*, em que *Max* era o valor RETORNADO de \_ tamanho de textura Max GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="03141-196">*level* was less than zero or greater than log2 *max*, where *max* was the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="03141-197"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="03141-197"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="03141-198">*internalformat* não era 1, 2, 3 ou 4.</span><span class="sxs-lookup"><span data-stu-id="03141-198">*internalformat* was was not 1, 2, 3, or 4.</span></span><br/>                                                                                                                                                                         |
| <dl> <span data-ttu-id="03141-199"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="03141-199"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="03141-200">a *largura* era menor que zero ou maior que 2 + GL \_ tamanho máximo de \_ textura \_ ou não pôde ser representada como 2 *n* + 2 (borda) para algum valor inteiro de *n*.</span><span class="sxs-lookup"><span data-stu-id="03141-200">*width* was less than zero or greater than 2 + GL\_MAX\_TEXTURE\_SIZE, or it could not be represented as 2 *n* + 2(border) for some integer value of *n*.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="03141-201"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="03141-201"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="03141-202">a *borda* não era 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="03141-202">*border* was not 0 or 1.</span></span><br/>                                                                                                                                                                                            |
| <dl> <span data-ttu-id="03141-203"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="03141-203"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="03141-204">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="03141-204">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                          |



## <a name="remarks"></a><span data-ttu-id="03141-205">Comentários</span><span class="sxs-lookup"><span data-stu-id="03141-205">Remarks</span></span>

<span data-ttu-id="03141-206">A função **glTexImage1D** especifica uma imagem de textura unidimensional.</span><span class="sxs-lookup"><span data-stu-id="03141-206">The **glTexImage1D** function specifies a one-dimensional texture image.</span></span> <span data-ttu-id="03141-207">Texturing mapeia uma parte de uma *imagem de textura* especificada em cada primitiva gráfica para a qual texturing está habilitado.</span><span class="sxs-lookup"><span data-stu-id="03141-207">Texturing maps a portion of a specified *texture image* onto each graphical primitive for which texturing is enabled.</span></span> <span data-ttu-id="03141-208">O texturing unidimensional é habilitado e desabilitado usando [**glEnable**](glenable.md) e **glDisable** com a textura do argumento GL \_ \_ 1D.</span><span class="sxs-lookup"><span data-stu-id="03141-208">One-dimensional texturing is enabled and disabled using [**glEnable**](glenable.md) and **glDisable** with argument GL\_TEXTURE\_1D.</span></span>

<span data-ttu-id="03141-209">As imagens de textura são definidas com **glTexImage1D**.</span><span class="sxs-lookup"><span data-stu-id="03141-209">Texture images are defined with **glTexImage1D**.</span></span> <span data-ttu-id="03141-210">Os argumentos descrevem os parâmetros da imagem de textura, como largura, largura da borda, número de nível de detalhe (consulte [**glTexParameter**](gltexparameter-functions.md)) e número de componentes de cores fornecidos.</span><span class="sxs-lookup"><span data-stu-id="03141-210">The arguments describe the parameters of the texture image, such as width, width of the border, level-of-detail number (see [**glTexParameter**](gltexparameter-functions.md)), and number of color components provided.</span></span> <span data-ttu-id="03141-211">Os três últimos argumentos descrevem a maneira como a imagem é representada na memória.</span><span class="sxs-lookup"><span data-stu-id="03141-211">The last three arguments describe the way the image is represented in memory.</span></span> <span data-ttu-id="03141-212">Esses argumentos são idênticos aos formatos de pixel usados para [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="03141-212">These arguments are identical to the pixel formats used for [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="03141-213">Os dados são lidos de *pixels* como uma sequência de bytes assinados ou sem sinal, curto ou longo ou valores de ponto flutuante de precisão única, dependendo do *tipo*.</span><span class="sxs-lookup"><span data-stu-id="03141-213">Data is read from *pixels* as a sequence of signed or unsigned bytes, shorts or longs, or single-precision floating-point values, depending on *type*.</span></span> <span data-ttu-id="03141-214">Esses valores são agrupados em conjuntos de um, dois, três ou quatro valores, dependendo do *formato*, para elementos de formulário.</span><span class="sxs-lookup"><span data-stu-id="03141-214">These values are grouped into sets of one, two, three, or four values, depending on *format*, to form elements.</span></span> <span data-ttu-id="03141-215">Se o *tipo* for \_ um bitmap GL, os dados serão considerados como uma cadeia de caracteres de bytes não assinados (e o *formato* deverá ser o índice de \_ cores GL \_ ).</span><span class="sxs-lookup"><span data-stu-id="03141-215">If *type* is GL\_BITMAP, the data is considered as a string of unsigned bytes (and *format* must be GL\_COLOR\_INDEX).</span></span> <span data-ttu-id="03141-216">Cada byte de dados é tratado como elementos de 8 1 bits, com ordenação de bits determinada pelo GL \_ Unpack \_ LSB \_ First (consulte [**glPixelStore**](glpixelstore-functions.md)).</span><span class="sxs-lookup"><span data-stu-id="03141-216">Each data byte is treated as eight 1-bit elements, with bit ordering determined by GL\_UNPACK\_LSB\_FIRST (see [**glPixelStore**](glpixelstore-functions.md)).</span></span>

<span data-ttu-id="03141-217">Uma imagem de textura pode ter até quatro componentes por elemento de textura, dependendo dos *componentes*.</span><span class="sxs-lookup"><span data-stu-id="03141-217">A texture image can have up to four components per texture element, depending on *components*.</span></span> <span data-ttu-id="03141-218">Uma imagem de textura de um componente usa apenas o componente vermelho da cor RGBA extraída de *pixels*.</span><span class="sxs-lookup"><span data-stu-id="03141-218">A one-component texture image uses only the red component of the RGBA color extracted from *pixels*.</span></span> <span data-ttu-id="03141-219">Uma imagem de dois componentes usa o R e valores.</span><span class="sxs-lookup"><span data-stu-id="03141-219">A two-component image uses the R and A values.</span></span> <span data-ttu-id="03141-220">Uma imagem de três componentes usa os valores R, G e B.</span><span class="sxs-lookup"><span data-stu-id="03141-220">A three-component image uses the R, G, and B values.</span></span> <span data-ttu-id="03141-221">Uma imagem de quatro componentes usa todos os componentes RGBA.</span><span class="sxs-lookup"><span data-stu-id="03141-221">A four-component image uses all of the RGBA components.</span></span>

<span data-ttu-id="03141-222">Texturing não tem efeito no modo de índice de cor.</span><span class="sxs-lookup"><span data-stu-id="03141-222">Texturing has no effect in color-index mode.</span></span>

<span data-ttu-id="03141-223">A imagem de textura pode ser representada pelos mesmos formatos de dados que os pixels em um comando [**glDrawPixels**](gldrawpixels.md) , exceto que o \_ índice de estêncil GL e o componente de \_ \_ profundidade GL \_ não podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="03141-223">The texture image can be represented by the same data formats as the pixels in a [**glDrawPixels**](gldrawpixels.md) command, except that GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT cannot be used.</span></span> <span data-ttu-id="03141-224">Os modos [**glPixelStore**](glpixelstore-functions.md) e [**glPixelTransfer**](glpixeltransfer.md) afetam as imagens de textura exatamente como elas afetam o **glDrawPixels**.</span><span class="sxs-lookup"><span data-stu-id="03141-224">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) modes affect texture images in exactly the way they affect **glDrawPixels**.</span></span>

<span data-ttu-id="03141-225">Uma imagem de textura com largura zero indica a textura nula.</span><span class="sxs-lookup"><span data-stu-id="03141-225">A texture image with zero width indicates the null texture.</span></span> <span data-ttu-id="03141-226">Se a textura nula for especificada para o nível de detalhe 0, ela será como se texturing estivesse desabilitada.</span><span class="sxs-lookup"><span data-stu-id="03141-226">If the null texture is specified for level-of-detail 0, it is as if texturing were disabled.</span></span>

<span data-ttu-id="03141-227">As funções a seguir recuperam informações relacionadas ao **glTexImageID**:</span><span class="sxs-lookup"><span data-stu-id="03141-227">The following functions retrieve information related to **glTexImageID**:</span></span>

[<span data-ttu-id="03141-228">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="03141-228">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="03141-229">[**glIsEnabled**](glisenabled.md) com a textura do argumento GL \_ \_ 1D</span><span class="sxs-lookup"><span data-stu-id="03141-229">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_1D</span></span>

## <a name="requirements"></a><span data-ttu-id="03141-230">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03141-230">Requirements</span></span>



| <span data-ttu-id="03141-231">Requisito</span><span class="sxs-lookup"><span data-stu-id="03141-231">Requirement</span></span> | <span data-ttu-id="03141-232">Valor</span><span class="sxs-lookup"><span data-stu-id="03141-232">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03141-233">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03141-233">Minimum supported client</span></span><br/> | <span data-ttu-id="03141-234">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="03141-234">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="03141-235">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03141-235">Minimum supported server</span></span><br/> | <span data-ttu-id="03141-236">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="03141-236">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="03141-237">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="03141-237">Header</span></span><br/>                   | <dl> <span data-ttu-id="03141-238"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="03141-238"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="03141-239">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="03141-239">Library</span></span><br/>                  | <dl> <span data-ttu-id="03141-240"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="03141-240"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="03141-241">DLL</span><span class="sxs-lookup"><span data-stu-id="03141-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03141-242"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03141-242"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03141-243">Confira também</span><span class="sxs-lookup"><span data-stu-id="03141-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03141-244">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="03141-244">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="03141-245">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="03141-245">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="03141-246">**glCopyTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="03141-246">**glCopyTexImage1D**</span></span>](glcopyteximage1d.md)
</dt> <dt>

[<span data-ttu-id="03141-247">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="03141-247">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="03141-248">**glCopyTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="03141-248">**glCopyTexSubImage1D**</span></span>](glcopytexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="03141-249">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="03141-249">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="03141-250">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="03141-250">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="03141-251">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="03141-251">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="03141-252">**glFog**</span><span class="sxs-lookup"><span data-stu-id="03141-252">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="03141-253">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="03141-253">**glGetTexImage**</span></span>](glgetteximage.md)
</dt> <dt>

[<span data-ttu-id="03141-254">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="03141-254">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="03141-255">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="03141-255">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="03141-256">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="03141-256">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="03141-257">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="03141-257">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="03141-258">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="03141-258">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="03141-259">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="03141-259">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="03141-260">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="03141-260">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="03141-261">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="03141-261">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="03141-262">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="03141-262">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





