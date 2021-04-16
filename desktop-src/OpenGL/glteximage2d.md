---
title: função glTexImage2D (GL. h)
description: A função glTexImage2D especifica uma imagem de textura bidimensional.
ms.assetid: e8b9c692-5239-47de-86eb-80c247c60e1d
keywords:
- função glTexImage2D OpenGL
topic_type:
- apiref
api_name:
- glTexImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ba2d5bc6f966d9b10c0dadccb221086e64de827
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105751090"
---
# <a name="glteximage2d-function"></a><span data-ttu-id="d8941-104">função glTexImage2D</span><span class="sxs-lookup"><span data-stu-id="d8941-104">glTexImage2D function</span></span>

<span data-ttu-id="d8941-105">A função **glTexImage2D** especifica uma imagem de textura bidimensional.</span><span class="sxs-lookup"><span data-stu-id="d8941-105">The **glTexImage2D** function specifies a two-dimensional texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8941-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8941-106">Syntax</span></span>


```C++
void WINAPI glTexImage2D(
         GLenum  target,
         GLint   level,
         GLint   internalformat,
         GLsizei width,
         GLsizei height,
         GLint   border,
         GLint   format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="d8941-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8941-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8941-108">*destino*</span><span class="sxs-lookup"><span data-stu-id="d8941-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="d8941-109">A textura de destino.</span><span class="sxs-lookup"><span data-stu-id="d8941-109">The target texture.</span></span> <span data-ttu-id="d8941-110">Deve ser GL de \_ textura \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="d8941-110">Must be GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="d8941-111">*level*</span><span class="sxs-lookup"><span data-stu-id="d8941-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="d8941-112">O número de nível de detalhe.</span><span class="sxs-lookup"><span data-stu-id="d8941-112">The level-of-detail number.</span></span> <span data-ttu-id="d8941-113">Nível 0 é o nível de imagem base.</span><span class="sxs-lookup"><span data-stu-id="d8941-113">Level 0 is the base image level.</span></span> <span data-ttu-id="d8941-114">O nível *n* é a imagem de redução *n* º mipmap.</span><span class="sxs-lookup"><span data-stu-id="d8941-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="d8941-115">*internalformat*</span><span class="sxs-lookup"><span data-stu-id="d8941-115">*internalformat*</span></span> 
</dt> <dd>

<span data-ttu-id="d8941-116">O número de componentes de cor na textura.</span><span class="sxs-lookup"><span data-stu-id="d8941-116">The number of color components in the texture.</span></span> <span data-ttu-id="d8941-117">Deve ser 1, 2, 3 ou 4, ou uma das seguintes constantes simbólicas: GL \_ alfa, GL \_ ALPHA4, GL \_ ALPHA8, GL \_ ALPHA12, GL \_ ALPHA16, GL \_ luminescência, GL \_ LUMINANCE4, GL \_ LUMINANCE8, GL \_ LUMINANCE12, GL \_ LUMINANCE16, GL \_ luminância \_ alfa, GL \_ LUMINANCE4 \_ ALPHA4, GL \_ LUMINANCE6 \_ ALPHA2, GL \_ LUMINANCE8 \_ ALPHA8, GL \_ LUMINANCE12 \_ ALPHA4, GL \_ LUMINANCE12 \_ ALPHA12, GL \_ LUMINANCE16 \_ ALPHA16, GL \_ intensidade, GL \_ INTENSITY4, GL \_ INTENSITY8, GL \_ INTENSITY12, GL \_ INTENSITY16, GL \_ R3 \_ G3 \_ B2, GL \_ RGB, GL \_ RGB4, GL \_ RGB5, GL \_ RGB8, GL \_ RGB10, GL \_ RGB12, GL \_ RGB16, GL \_ RGBA, GL \_ RGBA2, GL \_ RGBA4, GL \_ RGB5 \_ a1, GL \_ RGBA8, GL RGB10 \_ \_ a2, GL \_ RGBA12 ou GL \_ RGBA16.</span><span class="sxs-lookup"><span data-stu-id="d8941-117">Must be 1, 2, 3, or 4, or one of the following symbolic constants: GL\_ALPHA, GL\_ALPHA4, GL\_ALPHA8, GL\_ALPHA12, GL\_ALPHA16, GL\_LUMINANCE, GL\_LUMINANCE4, GL\_LUMINANCE8, GL\_LUMINANCE12, GL\_LUMINANCE16, GL\_LUMINANCE\_ALPHA, GL\_LUMINANCE4\_ALPHA4, GL\_LUMINANCE6\_ALPHA2, GL\_LUMINANCE8\_ALPHA8, GL\_LUMINANCE12\_ALPHA4, GL\_LUMINANCE12\_ALPHA12, GL\_LUMINANCE16\_ALPHA16, GL\_INTENSITY, GL\_INTENSITY4, GL\_INTENSITY8, GL\_INTENSITY12, GL\_INTENSITY16, GL\_R3\_G3\_B2, GL\_RGB, GL\_RGB4, GL\_RGB5, GL\_RGB8, GL\_RGB10, GL\_RGB12, GL\_RGB16, GL\_RGBA, GL\_RGBA2, GL\_RGBA4, GL\_RGB5\_A1, GL\_RGBA8, GL\_RGB10\_A2, GL\_RGBA12, or GL\_RGBA16.</span></span>

</dd> <dt>

<span data-ttu-id="d8941-118">*width*</span><span class="sxs-lookup"><span data-stu-id="d8941-118">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="d8941-119">A largura da imagem de textura.</span><span class="sxs-lookup"><span data-stu-id="d8941-119">The width of the texture image.</span></span> <span data-ttu-id="d8941-120">Deve ser 2 *n* + 2 (*Border*) para algum número inteiro *n*.</span><span class="sxs-lookup"><span data-stu-id="d8941-120">Must be 2 *n* + 2(*border*) for some integer *n*.</span></span>

</dd> <dt>

<span data-ttu-id="d8941-121">*altura*</span><span class="sxs-lookup"><span data-stu-id="d8941-121">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="d8941-122">A altura da imagem de textura.</span><span class="sxs-lookup"><span data-stu-id="d8941-122">The height of the texture image.</span></span> <span data-ttu-id="d8941-123">Deve ser 2 *<sup>m</sup>* + 2 (*Border*) para um inteiro *m*.</span><span class="sxs-lookup"><span data-stu-id="d8941-123">Must be 2 *<sup>m</sup>* + 2(*border*) for some integer *m*.</span></span>

</dd> <dt>

<span data-ttu-id="d8941-124">*borda*</span><span class="sxs-lookup"><span data-stu-id="d8941-124">*border*</span></span> 
</dt> <dd>

<span data-ttu-id="d8941-125">A largura da borda.</span><span class="sxs-lookup"><span data-stu-id="d8941-125">The width of the border.</span></span> <span data-ttu-id="d8941-126">Deve ser 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="d8941-126">Must be either 0 or 1.</span></span>

</dd> <dt>

<span data-ttu-id="d8941-127">*format*</span><span class="sxs-lookup"><span data-stu-id="d8941-127">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="d8941-128">O formato dos dados de pixel.</span><span class="sxs-lookup"><span data-stu-id="d8941-128">The format of the pixel data.</span></span> <span data-ttu-id="d8941-129">Ele pode assumir um dos nove valores simbólicos.</span><span class="sxs-lookup"><span data-stu-id="d8941-129">It can assume one of nine symbolic values.</span></span>



| <span data-ttu-id="d8941-130">Valor</span><span class="sxs-lookup"><span data-stu-id="d8941-130">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="d8941-131">Significado</span><span class="sxs-lookup"><span data-stu-id="d8941-131">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <span data-ttu-id="d8941-132"><dt>**\_índice de cores GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d8941-132"><dt>**GL\_COLOR\_INDEX**</dt></span></span> </dl>             | <span data-ttu-id="d8941-133">Cada elemento é um único valor, um índice de cores.</span><span class="sxs-lookup"><span data-stu-id="d8941-133">Each element is a single value, a color index.</span></span> <span data-ttu-id="d8941-134">Ele é convertido em um ponto fixo (com um número não especificado de 0 bits à direita do ponto binário), deslocado para a esquerda ou para a direita, dependendo do valor e do sinal de \_ mudança de índice GL \_ , e adicionado ao \_ deslocamento de índice GL \_ (consulte [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="d8941-134">It is converted to fixed point (with an unspecified number of 0 bits to the right of the binary point), shifted left or right depending on the value and sign of GL\_INDEX\_SHIFT, and added to GL\_INDEX\_OFFSET (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span> <span data-ttu-id="d8941-135">O índice resultante é convertido em um conjunto de componentes de cor usando o \_ mapa de pixel GL \_ \_ i \_ para \_ R, o GL \_ pixel \_ map \_ i \_ para \_ G, GL \_ pixel \_ map \_ i \_ para \_ B e GL \_ pixel \_ MAP i \_ \_ para \_ tabelas e clamped para o intervalo \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="d8941-135">The resulting index is converted to a set of color components using the GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, and GL\_PIXEL\_MAP\_I\_TO\_A tables, and clamped to the range \[0,1\].</span></span><br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="d8941-136"><dt>**GL \_ vermelho**</dt></span><span class="sxs-lookup"><span data-stu-id="d8941-136"><dt>**GL\_RED**</dt></span></span> </dl>                                      | <span data-ttu-id="d8941-137">Cada elemento é um único componente vermelho.</span><span class="sxs-lookup"><span data-stu-id="d8941-137">Each element is a single red component.</span></span> <span data-ttu-id="d8941-138">Ele é convertido em ponto flutuante e montado em um elemento RGBA anexando 0,0 para verde e azul e 1,0 para alfa.</span><span class="sxs-lookup"><span data-stu-id="d8941-138">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for green and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="d8941-139">Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="d8941-139">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                               |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="d8941-140"><dt>**GL \_ verde**</dt></span><span class="sxs-lookup"><span data-stu-id="d8941-140"><dt>**GL\_GREEN**</dt></span></span> </dl>                                | <span data-ttu-id="d8941-141">Cada elemento é um único componente verde.</span><span class="sxs-lookup"><span data-stu-id="d8941-141">Each element is a single green component.</span></span> <span data-ttu-id="d8941-142">Ele é convertido em ponto flutuante e montado em um elemento RGBA anexando 0,0 para vermelho e azul e 1,0 para alfa.</span><span class="sxs-lookup"><span data-stu-id="d8941-142">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="d8941-143">Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="d8941-143">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                        |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="d8941-144"><dt>**\_azul GL**</dt></span><span class="sxs-lookup"><span data-stu-id="d8941-144"><dt>**GL\_BLUE**</dt></span></span> </dl>                                   | <span data-ttu-id="d8941-145">Cada elemento é um único componente azul.</span><span class="sxs-lookup"><span data-stu-id="d8941-145">Each element is a single blue component.</span></span> <span data-ttu-id="d8941-146">Ele é convertido em ponto flutuante e montado em um elemento RGBA anexando 0,0 para vermelho e verde e 1,0 para alfa.</span><span class="sxs-lookup"><span data-stu-id="d8941-146">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red and green, and 1.0 for alpha.</span></span> <span data-ttu-id="d8941-147">Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="d8941-147">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                               |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="d8941-148"><dt>**GL \_ alfa**</dt></span><span class="sxs-lookup"><span data-stu-id="d8941-148"><dt>**GL\_ALPHA**</dt></span></span> </dl>                                | <span data-ttu-id="d8941-149">Cada elemento é um único componente vermelho.</span><span class="sxs-lookup"><span data-stu-id="d8941-149">Each element is a single red component.</span></span> <span data-ttu-id="d8941-150">Ele é convertido em ponto flutuante e montado em um elemento RGBA anexando 0,0 para vermelho, verde e azul.</span><span class="sxs-lookup"><span data-stu-id="d8941-150">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red, green, and blue.</span></span> <span data-ttu-id="d8941-151">Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="d8941-151">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                                     |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="d8941-152"><dt>**GL em \_ RGB**</dt></span><span class="sxs-lookup"><span data-stu-id="d8941-152"><dt>**GL\_RGB**</dt></span></span> </dl>                                      | <span data-ttu-id="d8941-153">Cada elemento é um triplo RGB.</span><span class="sxs-lookup"><span data-stu-id="d8941-153">Each element is an RGB triple.</span></span> <span data-ttu-id="d8941-154">Ele é convertido em ponto flutuante e montado em um elemento RGBA anexando 1,0 para alfa.</span><span class="sxs-lookup"><span data-stu-id="d8941-154">It is converted to floating point and assembled into an RGBA element by attaching 1.0 for alpha.</span></span> <span data-ttu-id="d8941-155">Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="d8941-155">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                    |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="d8941-156"><dt>**Se \_ RGBA**</dt></span><span class="sxs-lookup"><span data-stu-id="d8941-156"><dt>**GL\_RGBA**</dt></span></span> </dl>                                   | <span data-ttu-id="d8941-157">Cada elemento é um elemento RGBA completo.</span><span class="sxs-lookup"><span data-stu-id="d8941-157">Each element is a complete RGBA element.</span></span> <span data-ttu-id="d8941-158">Ele é convertido em ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="d8941-158">It is converted to floating point.</span></span> <span data-ttu-id="d8941-159">Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="d8941-159">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                                                                                                                 |
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="d8941-160"><dt>**\_BGR \_ ext. GL**</dt></span><span class="sxs-lookup"><span data-stu-id="d8941-160"><dt>**GL\_BGR\_EXT**</dt></span></span> </dl>                         | <span data-ttu-id="d8941-161">Cada pixel é um grupo de três componentes nesta ordem: azul, verde e vermelho.</span><span class="sxs-lookup"><span data-stu-id="d8941-161">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="d8941-162">GL \_ BGR \_ ext fornece um formato que corresponde ao layout de memória dos bitmaps independentes de dispositivo do Windows (DIBs).</span><span class="sxs-lookup"><span data-stu-id="d8941-162">GL\_BGR\_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="d8941-163">Assim, seus aplicativos podem usar os mesmos dados com chamadas de função do Windows e chamadas de função de pixel OpenGL.</span><span class="sxs-lookup"><span data-stu-id="d8941-163">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/>                                                                                                                                                                                                                                     |
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="d8941-164"><dt>**\_BGRA \_ ext. GL**</dt></span><span class="sxs-lookup"><span data-stu-id="d8941-164"><dt>**GL\_BGRA\_EXT**</dt></span></span> </dl>                      | <span data-ttu-id="d8941-165">Cada pixel é um grupo de quatro componentes nesta ordem: azul, verde, vermelho, alfa.</span><span class="sxs-lookup"><span data-stu-id="d8941-165">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span> <span data-ttu-id="d8941-166">GL \_ BGRA \_ ext fornece um formato que corresponde ao layout de memória dos bitmaps independentes de dispositivo do Windows (DIBs).</span><span class="sxs-lookup"><span data-stu-id="d8941-166">GL\_BGRA\_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="d8941-167">Assim, seus aplicativos podem usar os mesmos dados com chamadas de função do Windows e chamadas de função de pixel OpenGL.</span><span class="sxs-lookup"><span data-stu-id="d8941-167">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/>                                                                                                                                                                                                                                         |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <span data-ttu-id="d8941-168"><dt>**\_luminância GL**</dt></span><span class="sxs-lookup"><span data-stu-id="d8941-168"><dt>**GL\_LUMINANCE**</dt></span></span> </dl>                    | <span data-ttu-id="d8941-169">Cada elemento é um único valor de luminância.</span><span class="sxs-lookup"><span data-stu-id="d8941-169">Each element is a single luminance value.</span></span> <span data-ttu-id="d8941-170">Ele é convertido em ponto flutuante e, em seguida, montado em um elemento RGBA replicando o valor de luminância três vezes para vermelho, verde e azul e anexando 1,0 para alfa.</span><span class="sxs-lookup"><span data-stu-id="d8941-170">It is converted to floating point, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue, and attaching 1.0 for alpha.</span></span> <span data-ttu-id="d8941-171">Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="d8941-171">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                         |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <span data-ttu-id="d8941-172"><dt>**luminância do GL \_ \_ alfa**</dt></span><span class="sxs-lookup"><span data-stu-id="d8941-172"><dt>**GL\_LUMINANCE\_ALPHA**</dt></span></span> </dl> | <span data-ttu-id="d8941-173">Cada elemento é um par de luminância/alfa.</span><span class="sxs-lookup"><span data-stu-id="d8941-173">Each element is a luminance/alpha pair.</span></span> <span data-ttu-id="d8941-174">Ele é convertido em ponto flutuante e, em seguida, montado em um elemento RGBA replicando o valor de luminância três vezes para vermelho, verde e azul.</span><span class="sxs-lookup"><span data-stu-id="d8941-174">It is converted to floating point, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue.</span></span> <span data-ttu-id="d8941-175">Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="d8941-175">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="d8941-176">*tipo*</span><span class="sxs-lookup"><span data-stu-id="d8941-176">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="d8941-177">O tipo de dados dos dados de pixel.</span><span class="sxs-lookup"><span data-stu-id="d8941-177">The data type of the pixel data.</span></span> <span data-ttu-id="d8941-178">Os seguintes valores simbólicos são aceitos: GL \_ não assinado \_ byte, GL byte, renomear \_ \_ bitmap, GL \_ não assinado \_ curto, GL \_ curto, GL \_ não assinado \_ int, GL \_ int e GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="d8941-178">The following symbolic values are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="d8941-179">*pixels*</span><span class="sxs-lookup"><span data-stu-id="d8941-179">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="d8941-180">Um ponteiro para os dados da imagem na memória.</span><span class="sxs-lookup"><span data-stu-id="d8941-180">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8941-181">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d8941-181">Return value</span></span>

<span data-ttu-id="d8941-182">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d8941-182">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d8941-183">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="d8941-183">Error codes</span></span>

<span data-ttu-id="d8941-184">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="d8941-184">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="d8941-185">Nome</span><span class="sxs-lookup"><span data-stu-id="d8941-185">Name</span></span>                                                                                                  | <span data-ttu-id="d8941-186">Significado</span><span class="sxs-lookup"><span data-stu-id="d8941-186">Meaning</span></span>                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d8941-187"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="d8941-187"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="d8941-188">o *destino* não era um GL de \_ textura \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="d8941-188">*target* was not an GL\_TEXTURE\_2D.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="d8941-189"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="d8941-189"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="d8941-190">o *formato* não era uma constante de *formato* aceito.</span><span class="sxs-lookup"><span data-stu-id="d8941-190">*format* was not an accepted *format* constant.</span></span> <span data-ttu-id="d8941-191">Somente as constantes de formato diferentes do \_ índice de estêncil GL e do \_ \_ componente de profundidade GL \_ são aceitas.</span><span class="sxs-lookup"><span data-stu-id="d8941-191">Only format constants other than GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT are accepted.</span></span> <span data-ttu-id="d8941-192">Consulte a descrição do parâmetro do *formato* para obter uma lista de valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="d8941-192">See the parameter description of *format* for a list of possible values.</span></span><br/> |
| <dl> <span data-ttu-id="d8941-193"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="d8941-193"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="d8941-194">o *tipo* não era uma constante de *tipo* .</span><span class="sxs-lookup"><span data-stu-id="d8941-194">*type* was not a *type* constant.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="d8941-195"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="d8941-195"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="d8941-196">o *tipo* was \_ bitmap GL e *Format* não era um índice de \_ cores GL \_ .</span><span class="sxs-lookup"><span data-stu-id="d8941-196">*type* was GL\_BITMAP and *format* was not GL\_COLOR\_INDEX.</span></span><br/>                                                                                                                                                        |
| <dl> <span data-ttu-id="d8941-197"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d8941-197"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="d8941-198">o *nível* era menor que zero ou maior que log2 *Max*, em que *Max* era o valor RETORNADO de \_ tamanho de textura Max GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d8941-198">*level* was less than zero or greater than log2 *max*, where *max* was the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="d8941-199"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d8941-199"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="d8941-200">*internalformat* não era 1, 2, 3 ou 4.</span><span class="sxs-lookup"><span data-stu-id="d8941-200">*internalformat* was was not 1, 2, 3, or 4.</span></span><br/>                                                                                                                                                                         |
| <dl> <span data-ttu-id="d8941-201"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d8941-201"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="d8941-202">a *largura* ou a altura era menor que zero ou maior que 2 + GL \_ tamanho máximo de \_ textura \_ ou não pôde ser representada como 2 *n* + 2 (borda) para algum valor inteiro de *n*.</span><span class="sxs-lookup"><span data-stu-id="d8941-202">*width* or height was less than zero or greater than 2 + GL\_MAX\_TEXTURE\_SIZE, or it could not be represented as 2 *n* + 2(border) for some integer value of *n*.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="d8941-203"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d8941-203"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="d8941-204">a *borda* não era 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="d8941-204">*border* was not 0 or 1.</span></span><br/>                                                                                                                                                                                            |
| <dl> <span data-ttu-id="d8941-205"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d8941-205"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d8941-206">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="d8941-206">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                          |



## <a name="remarks"></a><span data-ttu-id="d8941-207">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8941-207">Remarks</span></span>

<span data-ttu-id="d8941-208">A função **glTexImage2D** especifica uma imagem de textura bidimensional.</span><span class="sxs-lookup"><span data-stu-id="d8941-208">The **glTexImage2D** function specifies a two-dimensional texture image.</span></span> <span data-ttu-id="d8941-209">Texturing mapeia uma parte de uma *imagem de textura* especificada em cada primitiva gráfica para a qual texturing está habilitado.</span><span class="sxs-lookup"><span data-stu-id="d8941-209">Texturing maps a portion of a specified *texture image* onto each graphical primitive for which texturing is enabled.</span></span> <span data-ttu-id="d8941-210">O texturing bidimensional é habilitado e desabilitado usando [**glEnable**](glenable.md) e **glDisable** com a textura do argumento GL \_ \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="d8941-210">Two-dimensional texturing is enabled and disabled using [**glEnable**](glenable.md) and **glDisable** with argument GL\_TEXTURE\_2D.</span></span>

<span data-ttu-id="d8941-211">As imagens de textura são definidas com **glTexImage2D**.</span><span class="sxs-lookup"><span data-stu-id="d8941-211">Texture images are defined with **glTexImage2D**.</span></span> <span data-ttu-id="d8941-212">Os argumentos descrevem os parâmetros da imagem de textura, como altura, largura, largura da borda, número de nível de detalhe (consulte [**glTexParameter**](gltexparameter-functions.md)) e número de componentes de cores fornecidos.</span><span class="sxs-lookup"><span data-stu-id="d8941-212">The arguments describe the parameters of the texture image, such as height, width, width of the border, level-of-detail number (see [**glTexParameter**](gltexparameter-functions.md)), and number of color components provided.</span></span> <span data-ttu-id="d8941-213">Os três últimos argumentos descrevem a maneira como a imagem é representada na memória.</span><span class="sxs-lookup"><span data-stu-id="d8941-213">The last three arguments describe the way the image is represented in memory.</span></span> <span data-ttu-id="d8941-214">Esses argumentos são idênticos aos formatos de pixel usados para [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="d8941-214">These arguments are identical to the pixel formats used for [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="d8941-215">Os dados são lidos de *pixels* como uma sequência de bytes assinados ou sem sinal, curto ou longo ou valores de ponto flutuante de precisão única, dependendo do *tipo*.</span><span class="sxs-lookup"><span data-stu-id="d8941-215">Data is read from *pixels* as a sequence of signed or unsigned bytes, shorts or longs, or single-precision floating-point values, depending on *type*.</span></span> <span data-ttu-id="d8941-216">Esses valores são agrupados em conjuntos de um, dois, três ou quatro valores, dependendo do *formato*, para elementos de formulário.</span><span class="sxs-lookup"><span data-stu-id="d8941-216">These values are grouped into sets of one, two, three, or four values, depending on *format*, to form elements.</span></span> <span data-ttu-id="d8941-217">Se o *tipo* for \_ um bitmap GL, os dados serão considerados como uma cadeia de caracteres de bytes não assinados (e o *formato* deverá ser o índice de \_ cores GL \_ ).</span><span class="sxs-lookup"><span data-stu-id="d8941-217">If *type* is GL\_BITMAP, the data is considered as a string of unsigned bytes (and *format* must be GL\_COLOR\_INDEX).</span></span> <span data-ttu-id="d8941-218">Cada byte de dados é tratado como elementos de 8 1 bits, com ordenação de bits determinada pelo GL \_ Unpack \_ LSB \_ First (consulte [**glPixelStore**](glpixelstore-functions.md)).</span><span class="sxs-lookup"><span data-stu-id="d8941-218">Each data byte is treated as eight 1-bit elements, with bit ordering determined by GL\_UNPACK\_LSB\_FIRST (see [**glPixelStore**](glpixelstore-functions.md)).</span></span> <span data-ttu-id="d8941-219">Consulte [**glDrawPixels**](gldrawpixels.md) para obter uma descrição dos valores aceitáveis para o parâmetro de *tipo* .</span><span class="sxs-lookup"><span data-stu-id="d8941-219">Please see [**glDrawPixels**](gldrawpixels.md) for a description of the acceptable values for the *type* parameter.</span></span>

<span data-ttu-id="d8941-220">Uma imagem de textura pode ter até quatro componentes por elemento de textura, dependendo dos *componentes*.</span><span class="sxs-lookup"><span data-stu-id="d8941-220">A texture image can have up to four components per texture element, depending on *components*.</span></span> <span data-ttu-id="d8941-221">Uma imagem de textura de um componente usa apenas o componente vermelho da cor RGBA extraída de *pixels*.</span><span class="sxs-lookup"><span data-stu-id="d8941-221">A one-component texture image uses only the red component of the RGBA color extracted from *pixels*.</span></span> <span data-ttu-id="d8941-222">Uma imagem de dois componentes usa o R e valores.</span><span class="sxs-lookup"><span data-stu-id="d8941-222">A two-component image uses the R and A values.</span></span> <span data-ttu-id="d8941-223">Uma imagem de três componentes usa os valores R, G e B.</span><span class="sxs-lookup"><span data-stu-id="d8941-223">A three-component image uses the R, G, and B values.</span></span> <span data-ttu-id="d8941-224">Uma imagem de quatro componentes usa todos os componentes RGBA.</span><span class="sxs-lookup"><span data-stu-id="d8941-224">A four-component image uses all of the RGBA components.</span></span>

<span data-ttu-id="d8941-225">Texturing não tem efeito no modo de índice de cor.</span><span class="sxs-lookup"><span data-stu-id="d8941-225">Texturing has no effect in color-index mode.</span></span>

<span data-ttu-id="d8941-226">A imagem de textura pode ser representada pelos mesmos formatos de dados que os pixels em um comando **glDrawPixels** , exceto que o \_ índice de estêncil GL e o componente de \_ \_ profundidade GL \_ não podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="d8941-226">The texture image can be represented by the same data formats as the pixels in a **glDrawPixels** command, except that GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT cannot be used.</span></span> <span data-ttu-id="d8941-227">Os modos [**glPixelStore**](glpixelstore-functions.md) e [**glPixelTransfer**](glpixeltransfer.md) afetam as imagens de textura exatamente como elas afetam o **glDrawPixels**.</span><span class="sxs-lookup"><span data-stu-id="d8941-227">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) modes affect texture images in exactly the way they affect **glDrawPixels**.</span></span>

<span data-ttu-id="d8941-228">Uma imagem de textura com altura ou largura zero indica a textura nula.</span><span class="sxs-lookup"><span data-stu-id="d8941-228">A texture image with zero height or width indicates the null texture.</span></span> <span data-ttu-id="d8941-229">Se a textura nula for especificada para o nível de detalhe 0, ela será como se texturing estivesse desabilitada.</span><span class="sxs-lookup"><span data-stu-id="d8941-229">If the null texture is specified for level-of-detail 0, it is as if texturing were disabled.</span></span>

<span data-ttu-id="d8941-230">As funções a seguir recuperam informações relacionadas ao **glTexImage2D**:</span><span class="sxs-lookup"><span data-stu-id="d8941-230">The following functions retrieve information related to **glTexImage2D**:</span></span>

[<span data-ttu-id="d8941-231">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="d8941-231">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="d8941-232">[**glIsEnabled**](glisenabled.md) com a textura do argumento GL \_ \_ 2D</span><span class="sxs-lookup"><span data-stu-id="d8941-232">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_2D</span></span>

## <a name="requirements"></a><span data-ttu-id="d8941-233">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8941-233">Requirements</span></span>



| <span data-ttu-id="d8941-234">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8941-234">Requirement</span></span> | <span data-ttu-id="d8941-235">Valor</span><span class="sxs-lookup"><span data-stu-id="d8941-235">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8941-236">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8941-236">Minimum supported client</span></span><br/> | <span data-ttu-id="d8941-237">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d8941-237">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d8941-238">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8941-238">Minimum supported server</span></span><br/> | <span data-ttu-id="d8941-239">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d8941-239">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d8941-240">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d8941-240">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8941-241"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8941-241"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="d8941-242">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d8941-242">Library</span></span><br/>                  | <dl> <span data-ttu-id="d8941-243"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8941-243"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d8941-244">DLL</span><span class="sxs-lookup"><span data-stu-id="d8941-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8941-245"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8941-245"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8941-246">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8941-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8941-247">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="d8941-247">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="d8941-248">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="d8941-248">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="d8941-249">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="d8941-249">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="d8941-250">**glFog**</span><span class="sxs-lookup"><span data-stu-id="d8941-250">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="d8941-251">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="d8941-251">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="d8941-252">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="d8941-252">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="d8941-253">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="d8941-253">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="d8941-254">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="d8941-254">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="d8941-255">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="d8941-255">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="d8941-256">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="d8941-256">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="d8941-257">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="d8941-257">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





