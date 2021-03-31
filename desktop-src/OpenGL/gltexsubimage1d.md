---
title: função glTexSubImage1D (GL. h)
description: A função glTexSubImage1D especifica uma parte de uma imagem de textura unidimensional existente. Você não pode definir uma nova textura com glTexSubImage1D.
ms.assetid: e5fcb1a3-96f8-47a6-a9a7-0061faaaa6ac
keywords:
- função glTexSubImage1D OpenGL
topic_type:
- apiref
api_name:
- glTexSubImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfe5510221b738a81f428f9e982a2f9bb2c23588
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644433"
---
# <a name="gltexsubimage1d-function"></a><span data-ttu-id="1f7f5-105">função glTexSubImage1D</span><span class="sxs-lookup"><span data-stu-id="1f7f5-105">glTexSubImage1D function</span></span>

<span data-ttu-id="1f7f5-106">A função **glTexSubImage1D** especifica uma parte de uma imagem de textura unidimensional existente.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-106">The **glTexSubImage1D** function specifies a portion of an existing one-dimensional texture image.</span></span> <span data-ttu-id="1f7f5-107">Você não pode definir uma nova textura com **glTexSubImage1D**.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-107">You cannot define a new texture with **glTexSubImage1D**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f7f5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f7f5-108">Syntax</span></span>


```C++
void WINAPI glTexSubImage1D(
         GLenum  target,
         GLint   level,
         GLint   xoffset,
         GLsizei width,
         GLenum  format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="1f7f5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f7f5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f7f5-110">*destino*</span><span class="sxs-lookup"><span data-stu-id="1f7f5-110">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="1f7f5-111">A textura de destino.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-111">The target texture.</span></span> <span data-ttu-id="1f7f5-112">Deve ser GL \_ Texture \_ 1D.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-112">Must be GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="1f7f5-113">*level*</span><span class="sxs-lookup"><span data-stu-id="1f7f5-113">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="1f7f5-114">O número de nível de detalhe.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-114">The level-of-detail number.</span></span> <span data-ttu-id="1f7f5-115">Nível 0 é a imagem base.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-115">Level 0 is the base image.</span></span> <span data-ttu-id="1f7f5-116">O nível *n* é a imagem de redução *n* º mipmap.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-116">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="1f7f5-117">*xoffset*</span><span class="sxs-lookup"><span data-stu-id="1f7f5-117">*xoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="1f7f5-118">Um deslocamento de Texel na direção *x* dentro da matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-118">A texel offset in the *x* direction within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="1f7f5-119">*width*</span><span class="sxs-lookup"><span data-stu-id="1f7f5-119">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="1f7f5-120">A largura da subimagem de textura.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-120">The width of the texture sub-image.</span></span>

</dd> <dt>

<span data-ttu-id="1f7f5-121">*format*</span><span class="sxs-lookup"><span data-stu-id="1f7f5-121">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="1f7f5-122">O formato dos dados de pixel.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-122">The format of the pixel data.</span></span> <span data-ttu-id="1f7f5-123">Esse parâmetro pode assumir um dos seguintes valores simbólicos.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-123">This parameter can assume one of the following symbolic values.</span></span>



| <span data-ttu-id="1f7f5-124">Valor</span><span class="sxs-lookup"><span data-stu-id="1f7f5-124">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="1f7f5-125">Significado</span><span class="sxs-lookup"><span data-stu-id="1f7f5-125">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <span data-ttu-id="1f7f5-126"><dt>**\_índice de cores GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1f7f5-126"><dt>**GL\_COLOR\_INDEX**</dt></span></span> </dl>             | <span data-ttu-id="1f7f5-127">Cada elemento é um único valor, um índice de cores.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-127">Each element is a single value, a color index.</span></span> <span data-ttu-id="1f7f5-128">Ele é convertido em formato de ponto fixo (com um número não especificado de 0 bits à direita do ponto binário), deslocado para a esquerda ou para a direita, dependendo do valor e do sinal de \_ mudança de índice GL \_ e adicionado ao \_ deslocamento de índice GL \_ (consulte [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="1f7f5-128">It is converted to fixed point format (with an unspecified number of 0 bits to the right of the binary point), shifted left or right, depending on the value and sign of GL\_INDEX\_SHIFT, and added to GL\_INDEX\_OFFSET (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span> <span data-ttu-id="1f7f5-129">O índice resultante é convertido em um conjunto de componentes de cor usando o \_ mapa de pixel GL \_ \_ i \_ para \_ R, o GL \_ pixel \_ map \_ i \_ para \_ G, GL \_ pixel \_ map \_ i \_ para \_ B e GL \_ pixel \_ MAP i \_ \_ para \_ tabelas e clamped para o intervalo \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="1f7f5-129">The resulting index is converted to a set of color components using the GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, and GL\_PIXEL\_MAP\_I\_TO\_A tables, and clamped to the range \[0,1\].</span></span><br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="1f7f5-130"><dt>**GL \_ vermelho**</dt></span><span class="sxs-lookup"><span data-stu-id="1f7f5-130"><dt>**GL\_RED**</dt></span></span> </dl>                                      | <span data-ttu-id="1f7f5-131">Cada elemento é um único componente vermelho.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-131">Each element is a single red component.</span></span> <span data-ttu-id="1f7f5-132">Ele é convertido em formato de ponto flutuante e montado em um elemento RGBA anexando 0,0 para verde e azul e 1,0 para alfa.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-132">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for green and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="1f7f5-133">Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="1f7f5-133">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="1f7f5-134"><dt>**GL \_ verde**</dt></span><span class="sxs-lookup"><span data-stu-id="1f7f5-134"><dt>**GL\_GREEN**</dt></span></span> </dl>                                | <span data-ttu-id="1f7f5-135">Cada elemento é um único componente verde.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-135">Each element is a single green component.</span></span> <span data-ttu-id="1f7f5-136">Ele é convertido em formato de ponto flutuante e montado em um elemento RGBA anexando 0,0 para vermelho e azul e 1,0 para alfa.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-136">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="1f7f5-137">Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="1f7f5-137">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                         |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="1f7f5-138"><dt>**\_azul GL**</dt></span><span class="sxs-lookup"><span data-stu-id="1f7f5-138"><dt>**GL\_BLUE**</dt></span></span> </dl>                                   | <span data-ttu-id="1f7f5-139">Cada elemento é um único componente azul.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-139">Each element is a single blue component.</span></span> <span data-ttu-id="1f7f5-140">Ele é convertido em formato de ponto flutuante e montado em um elemento RGBA anexando 0,0 para vermelho e verde e 1,0 para alfa.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-140">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red and green, and 1.0 for alpha.</span></span> <span data-ttu-id="1f7f5-141">Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="1f7f5-141">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="1f7f5-142"><dt>**GL \_ alfa**</dt></span><span class="sxs-lookup"><span data-stu-id="1f7f5-142"><dt>**GL\_ALPHA**</dt></span></span> </dl>                                | <span data-ttu-id="1f7f5-143">Cada elemento é um único componente alfa.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-143">Each element is a single alpha component.</span></span> <span data-ttu-id="1f7f5-144">Ele é convertido em formato de ponto flutuante e montado em um elemento RGBA anexando 0,0 para vermelho, verde e azul.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-144">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red, green, and blue.</span></span> <span data-ttu-id="1f7f5-145">Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="1f7f5-145">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                                    |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="1f7f5-146"><dt>**GL em \_ RGB**</dt></span><span class="sxs-lookup"><span data-stu-id="1f7f5-146"><dt>**GL\_RGB**</dt></span></span> </dl>                                      | <span data-ttu-id="1f7f5-147">Cada elemento é um triplo RGB.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-147">Each element is an RGB triple.</span></span> <span data-ttu-id="1f7f5-148">Ele é convertido em ponto flutuante e montado em um elemento RGBA anexando 1,0 para alfa.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-148">It is converted to floating point and assembled into an RGBA element by attaching 1.0 for alpha.</span></span> <span data-ttu-id="1f7f5-149">Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="1f7f5-149">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                            |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="1f7f5-150"><dt>**Se \_ RGBA**</dt></span><span class="sxs-lookup"><span data-stu-id="1f7f5-150"><dt>**GL\_RGBA**</dt></span></span> </dl>                                   | <span data-ttu-id="1f7f5-151">Cada elemento é um elemento RGBA completo.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-151">Each element is a complete RGBA element.</span></span> <span data-ttu-id="1f7f5-152">Ele é convertido em formato de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-152">It is converted to floating point format.</span></span> <span data-ttu-id="1f7f5-153">Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="1f7f5-153">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                                                                         |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <span data-ttu-id="1f7f5-154"><dt>**\_luminância GL**</dt></span><span class="sxs-lookup"><span data-stu-id="1f7f5-154"><dt>**GL\_LUMINANCE**</dt></span></span> </dl>                    | <span data-ttu-id="1f7f5-155">Cada elemento é um único valor de luminância.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-155">Each element is a single luminance value.</span></span> <span data-ttu-id="1f7f5-156">Ele é convertido em formato de ponto flutuante e, em seguida, montado em um elemento RGBA replicando o valor de luminância três vezes para vermelho, verde e azul e anexando 1,0 para alfa.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-156">It is converted to floating point format, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue, and attaching 1.0 for alpha.</span></span> <span data-ttu-id="1f7f5-157">Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="1f7f5-157">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                   |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <span data-ttu-id="1f7f5-158"><dt>**luminância do GL \_ \_ alfa**</dt></span><span class="sxs-lookup"><span data-stu-id="1f7f5-158"><dt>**GL\_LUMINANCE\_ALPHA**</dt></span></span> </dl> | <span data-ttu-id="1f7f5-159">Cada elemento é um par de luminância/alfa.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-159">Each element is a luminance/alpha pair.</span></span> <span data-ttu-id="1f7f5-160">Ele é convertido em formato de ponto flutuante e, em seguida, montado em um elemento RGBA replicando o valor de luminância três vezes para vermelho, verde e azul.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-160">It is converted to floating point format, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue.</span></span> <span data-ttu-id="1f7f5-161">Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="1f7f5-161">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="1f7f5-162">*tipo*</span><span class="sxs-lookup"><span data-stu-id="1f7f5-162">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="1f7f5-163">O tipo de dados dos dados de pixel.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-163">The data type of the pixel data.</span></span> <span data-ttu-id="1f7f5-164">Os seguintes valores simbólicos são aceitos: GL \_ não assinado \_ byte, GL byte, renomear \_ \_ bitmap, GL \_ não assinado \_ curto, GL \_ curto, GL \_ não assinado \_ int, GL \_ int e GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-164">The following symbolic values are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="1f7f5-165">*pixels*</span><span class="sxs-lookup"><span data-stu-id="1f7f5-165">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="1f7f5-166">Um ponteiro para os dados da imagem na memória.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-166">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f7f5-167">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1f7f5-167">Return value</span></span>

<span data-ttu-id="1f7f5-168">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-168">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1f7f5-169">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="1f7f5-169">Error codes</span></span>

<span data-ttu-id="1f7f5-170">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="1f7f5-170">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="1f7f5-171">Name</span><span class="sxs-lookup"><span data-stu-id="1f7f5-171">Name</span></span>                                                                                                  | <span data-ttu-id="1f7f5-172">Significado</span><span class="sxs-lookup"><span data-stu-id="1f7f5-172">Meaning</span></span>                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1f7f5-173"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="1f7f5-173"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="1f7f5-174">o *destino* não era GL \_ Texture \_ 1D.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-174">*target* was not GL\_TEXTURE\_1D.</span></span><br/>                                                                                                                                                                                                                             |
| <dl> <span data-ttu-id="1f7f5-175"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="1f7f5-175"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="1f7f5-176">o *formato* não era uma constante aceita.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-176">*format* was not an accepted constant.</span></span><br/>                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="1f7f5-177"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="1f7f5-177"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="1f7f5-178">o *tipo* não era uma constante aceita.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-178">*type* was not an accepted constant.</span></span><br/>                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="1f7f5-179"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="1f7f5-179"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="1f7f5-180">o *tipo* was \_ bitmap GL e *Format* não era um índice de \_ cores GL \_ .</span><span class="sxs-lookup"><span data-stu-id="1f7f5-180">*type* was GL\_BITMAP and *format* was not GL\_COLOR\_INDEX.</span></span><br/>                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="1f7f5-181"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1f7f5-181"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="1f7f5-182">o *nível* era menor que zero ou maior que log2 *Max*, em que *Max* era o valor RETORNADO de \_ tamanho de textura Max GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1f7f5-182">*level* was less than zero or greater than log2 *max*, where *max* was the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                                                                          |
| <dl> <span data-ttu-id="1f7f5-183"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1f7f5-183"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="1f7f5-184">*xoffset* era menor que *b*, ou   +  a *largura* de deslocamento era maior que *WB*, em que *w* é a largura de \_ textura GL \_ , e *b* é a largura da borda de \_ textura GL \_ da imagem de textura que está sendo modificada.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-184">*xoffset* was less than *b*, or *offset* + *width* was greater than *wb*, where *w* is the GL\_TEXTURE\_WIDTH, and *b* is the width of the GL\_TEXTURE\_BORDER of the texture image being modified.</span></span><br/> <span data-ttu-id="1f7f5-185">Observe que *w* inclui duas vezes a largura da borda.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-185">Note that *w* includes twice the border width.</span></span><br/> |
| <dl> <span data-ttu-id="1f7f5-186"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1f7f5-186"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="1f7f5-187">a *largura* era menor que *b*, onde *b* é a largura da borda da matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-187">*width* was was less than *b*, where *b* is the border width of the texture array.</span></span><br/>                                                                                                                                                                            |
| <dl> <span data-ttu-id="1f7f5-188"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1f7f5-188"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="1f7f5-189">a *borda* não era zero ou 1.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-189">*border* was not zero or 1.</span></span><br/>                                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="1f7f5-190"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1f7f5-190"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="1f7f5-191">A matriz texure não foi definida por uma operação **glTexImage1D** anterior.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-191">The texure array was not defined by a previous **glTexImage1D** operation.</span></span><br/>                                                                                                                                                                                    |
| <dl> <span data-ttu-id="1f7f5-192"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1f7f5-192"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="1f7f5-193">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="1f7f5-193">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                                                                    |



## <a name="remarks"></a><span data-ttu-id="1f7f5-194">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f7f5-194">Remarks</span></span>

<span data-ttu-id="1f7f5-195">Um texturing unidimensional para um primitivo é habilitado usando [**glEnable**](glenable.md) e **glDisable** com o argumento GL \_ Texture \_ 1D.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-195">One-dimensional texturing for a primitive is enabled using [**glEnable**](glenable.md) and **glDisable** with the argument GL\_TEXTURE\_1D.</span></span> <span data-ttu-id="1f7f5-196">Durante a texturing, parte de uma imagem de textura especificada é mapeada em cada primitiva habilitada.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-196">During texturing, part of a specified texture image is mapped into each enabled primitive.</span></span> <span data-ttu-id="1f7f5-197">Use a função **glTexSubImage1D** para especificar uma subimagem contígua de uma imagem de textura unidimensional existente para texturing.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-197">You use the **glTexSubImage1D** function to specify a contiguous sub-image of an existing one-dimensional texture image for texturing.</span></span>

<span data-ttu-id="1f7f5-198">O texels referenciado por *pixels* substitui uma região da matriz de textura existente por índices *x* de *xoffset* e *xoffset* + (*largura* 1), inclusive.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-198">The texels referenced by *pixels* replace a region of the existing texture array with *x* indexes of *xoffset* and *xoffset* + (*width* 1) inclusive.</span></span> <span data-ttu-id="1f7f5-199">Essa região não pode incluir nenhum texels fora do intervalo da matriz de textura especificada originalmente.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-199">This region cannot include any texels outside the range of the originally specified texture array.</span></span>

<span data-ttu-id="1f7f5-200">A especificação de uma subimagem com uma *largura* igual a zero não tem nenhum efeito e não gera um erro.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-200">Specifying a sub-image with a *width* of zero has no effect and does not generate an error.</span></span>

<span data-ttu-id="1f7f5-201">Texturing não tem efeito no modo de índice de cor.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-201">Texturing has no effect in color-index mode.</span></span>

<span data-ttu-id="1f7f5-202">Em geral, as imagens de textura podem ser representadas pelos mesmos formatos de dados que os pixels em um comando [**glDrawPixels**](gldrawpixels.md) , exceto que o \_ índice de estêncil GL e o componente de \_ \_ profundidade GL \_ não podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-202">In general, texture images can be represented by the same data formats as the pixels in a [**glDrawPixels**](gldrawpixels.md) command, except that GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT cannot be used.</span></span> <span data-ttu-id="1f7f5-203">Os modos [**glPixelStore**](glpixelstore-functions.md) e [**glPixelTransfer**](glpixeltransfer.md) afetam as imagens de textura exatamente como elas afetam o **glDrawPixels**.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-203">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) modes affect texture images in exactly the way they affect **glDrawPixels**.</span></span>

<span data-ttu-id="1f7f5-204">As funções a seguir recuperam informações relacionadas ao **glTexSubImage1D**:</span><span class="sxs-lookup"><span data-stu-id="1f7f5-204">The following functions retrieve information related to **glTexSubImage1D**:</span></span>

[<span data-ttu-id="1f7f5-205">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="1f7f5-205">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="1f7f5-206">[**glIsEnabled**](glisenabled.md) com a textura do argumento GL \_ \_ 1D</span><span class="sxs-lookup"><span data-stu-id="1f7f5-206">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_1D</span></span>

## <a name="requirements"></a><span data-ttu-id="1f7f5-207">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f7f5-207">Requirements</span></span>



| <span data-ttu-id="1f7f5-208">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f7f5-208">Requirement</span></span> | <span data-ttu-id="1f7f5-209">Valor</span><span class="sxs-lookup"><span data-stu-id="1f7f5-209">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f7f5-210">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f7f5-210">Minimum supported client</span></span><br/> | <span data-ttu-id="1f7f5-211">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1f7f5-211">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1f7f5-212">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f7f5-212">Minimum supported server</span></span><br/> | <span data-ttu-id="1f7f5-213">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1f7f5-213">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1f7f5-214">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1f7f5-214">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f7f5-215"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f7f5-215"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1f7f5-216">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1f7f5-216">Library</span></span><br/>                  | <dl> <span data-ttu-id="1f7f5-217"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f7f5-217"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1f7f5-218">DLL</span><span class="sxs-lookup"><span data-stu-id="1f7f5-218">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f7f5-219"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f7f5-219"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f7f5-220">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1f7f5-220">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f7f5-221">**glCopyTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="1f7f5-221">**glCopyTexImage1D**</span></span>](glcopyteximage1d.md)
</dt> <dt>

[<span data-ttu-id="1f7f5-222">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="1f7f5-222">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="1f7f5-223">**glCopyTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="1f7f5-223">**glCopyTexSubImage1D**</span></span>](glcopytexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="1f7f5-224">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="1f7f5-224">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="1f7f5-225">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="1f7f5-225">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="1f7f5-226">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="1f7f5-226">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="1f7f5-227">**glFog**</span><span class="sxs-lookup"><span data-stu-id="1f7f5-227">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="1f7f5-228">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="1f7f5-228">**glGetTexImage**</span></span>](glgetteximage.md)
</dt> <dt>

[<span data-ttu-id="1f7f5-229">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="1f7f5-229">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="1f7f5-230">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="1f7f5-230">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="1f7f5-231">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="1f7f5-231">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="1f7f5-232">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="1f7f5-232">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="1f7f5-233">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="1f7f5-233">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="1f7f5-234">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="1f7f5-234">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="1f7f5-235">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="1f7f5-235">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="1f7f5-236">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="1f7f5-236">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> <dt>

[<span data-ttu-id="1f7f5-237">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="1f7f5-237">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> </dl>

 

 





