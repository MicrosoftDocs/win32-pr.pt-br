---
title: função glTexParameteri (GL. h)
description: Define parâmetros de textura. | função glTexParameteri (GL. h)
ms.assetid: 67705f63-7f86-47c1-81f7-deecc0cd2e16
keywords:
- função glTexParameteri OpenGL
topic_type:
- apiref
api_name:
- glTexParameteri
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 207ac902047c5a2b6a5266d08e71f8e47f7ccb97
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298193"
---
# <a name="gltexparameteri-function"></a><span data-ttu-id="dc613-105">função glTexParameteri</span><span class="sxs-lookup"><span data-stu-id="dc613-105">glTexParameteri function</span></span>

<span data-ttu-id="dc613-106">Define parâmetros de textura.</span><span class="sxs-lookup"><span data-stu-id="dc613-106">Sets texture parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc613-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dc613-107">Syntax</span></span>


```C++
void WINAPI glTexParameteri(
   GLenum target,
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a><span data-ttu-id="dc613-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc613-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc613-109">*destino*</span><span class="sxs-lookup"><span data-stu-id="dc613-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="dc613-110">A textura de destino, que deve ser a textura GL \_ \_ 1D ou GL de \_ \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="dc613-110">The target texture, which must be either GL\_TEXTURE\_1D or GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="dc613-111">*pname*</span><span class="sxs-lookup"><span data-stu-id="dc613-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="dc613-112">O nome simbólico de um parâmetro de textura de valor único.</span><span class="sxs-lookup"><span data-stu-id="dc613-112">The symbolic name of a single valued texture parameter.</span></span> <span data-ttu-id="dc613-113">Os símbolos a seguir são aceitos em *pname*.</span><span class="sxs-lookup"><span data-stu-id="dc613-113">The following symbols are accepted in *pname*.</span></span>



| <span data-ttu-id="dc613-114">Valor</span><span class="sxs-lookup"><span data-stu-id="dc613-114">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="dc613-115">Significado</span><span class="sxs-lookup"><span data-stu-id="dc613-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <span data-ttu-id="dc613-116"><dt>**\_filtro de \_ mínimo de textura GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dc613-116"><dt>**GL\_TEXTURE\_MIN\_FILTER**</dt></span></span> </dl> | <span data-ttu-id="dc613-117">A função minificar de textura é usada sempre que o pixel que está sendo texturizado é mapeado para uma área maior do que um elemento de textura.</span><span class="sxs-lookup"><span data-stu-id="dc613-117">The texture minifying function is used whenever the pixel being textured maps to an area greater than one texture element.</span></span> <span data-ttu-id="dc613-118">Há seis funções minificar definidas.</span><span class="sxs-lookup"><span data-stu-id="dc613-118">There are six defined minifying functions.</span></span> <span data-ttu-id="dc613-119">Dois deles usam os elementos de textura mais próximos um ou mais próximo para calcular o valor de textura.</span><span class="sxs-lookup"><span data-stu-id="dc613-119">Two of them use the nearest one or nearest four texture elements to compute the texture value.</span></span> <span data-ttu-id="dc613-120">Os outros quatro usam mipmaps.</span><span class="sxs-lookup"><span data-stu-id="dc613-120">The other four use mipmaps.</span></span> <br/> <span data-ttu-id="dc613-121">Um mipmap é um conjunto ordenado de matrizes que representam a mesma imagem em resoluções progressivamente inferiores.</span><span class="sxs-lookup"><span data-stu-id="dc613-121">A mipmap is an ordered set of arrays representing the same image at progressively lower resolutions.</span></span> <span data-ttu-id="dc613-122">Se a textura tiver dimensões 2nx2<sup>m</sup> , haverá Max (n, m) + 1 mipmaps.</span><span class="sxs-lookup"><span data-stu-id="dc613-122">If the texture has dimensions 2nx2<sup>m</sup> there are max(n, m) + 1 mipmaps.</span></span> <span data-ttu-id="dc613-123">O primeiro mipmap é a textura original, com as dimensões 2nx2<sup>m</sup>.</span><span class="sxs-lookup"><span data-stu-id="dc613-123">The first mipmap is the original texture, with dimensions 2nx2<sup>m</sup>.</span></span> <span data-ttu-id="dc613-124">Cada mipmap subsequente tem dimensões 2<sup>k</sup>1x2<sup>l</sup>1, em que 2<sup>k</sup>X2<sup>l</sup> são as dimensões da mipmap anterior, até k = 0 ou l = 0.</span><span class="sxs-lookup"><span data-stu-id="dc613-124">Each subsequent mipmap has dimensions 2<sup>k</sup>1x2<sup>l</sup>1 where 2<sup>k</sup>x2<sup>l</sup> are the dimensions of the previous mipmap, until either k = 0 or l = 0.</span></span> <span data-ttu-id="dc613-125">Nesse ponto, os mipmaps subsequentes têm Dimension 1x2<sup>l</sup>1 ou 2<sup>k</sup>1x1 até o mipmap final, que tem a dimensão 1x1.</span><span class="sxs-lookup"><span data-stu-id="dc613-125">At that point, subsequent mipmaps have dimension 1x2<sup>l</sup>1 or 2<sup>k</sup>1x1 until the final mipmap, which has dimension 1x1.</span></span> <span data-ttu-id="dc613-126">Mipmaps são definidos usando [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md) com o argumento de nível de detalhe que indica a ordem do mipmaps.</span><span class="sxs-lookup"><span data-stu-id="dc613-126">Mipmaps are defined using [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md) with the level-of-detail argument indicating the order of the mipmaps.</span></span> <span data-ttu-id="dc613-127">Nível 0 é a textura original; o nível máximo em negrito (n, m) é o 1x1 final mipmap.</span><span class="sxs-lookup"><span data-stu-id="dc613-127">Level 0 is the original texture; level bold max(n, m) is the final 1x1 mipmap.</span></span><br/> |
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <span data-ttu-id="dc613-128"><dt>**\_ \_ filtro mag de textura GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dc613-128"><dt>**GL\_TEXTURE\_MAG\_FILTER**</dt></span></span> </dl> | <span data-ttu-id="dc613-129">A função de ampliação de textura é usada quando o pixel que está sendo texturizado é mapeado para uma área menor ou igual a um elemento de textura.</span><span class="sxs-lookup"><span data-stu-id="dc613-129">The texture magnification function is used when the pixel being textured maps to an area less than or equal to one texture element.</span></span> <span data-ttu-id="dc613-130">Ele define a função de ampliação de textura como GL \_ mais próximo ou GL \_ linear.</span><span class="sxs-lookup"><span data-stu-id="dc613-130">It sets the texture magnification function to either GL\_NEAREST or GL\_LINEAR.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <span data-ttu-id="dc613-131"><dt>**\_S de \_ encapsulamento de textura GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dc613-131"><dt>**GL\_TEXTURE\_WRAP\_S**</dt></span></span> </dl>             | <span data-ttu-id="dc613-132">Define o parâmetro Wrap para a coordenada de textura s para GL \_ fixe ou GL \_ REPEAT.</span><span class="sxs-lookup"><span data-stu-id="dc613-132">Sets the wrap parameter for texture coordinate s to either GL\_CLAMP or GL\_REPEAT.</span></span> <span data-ttu-id="dc613-133">GL \_ fixe faz com que as coordenadas de s sejam clampeddas para o intervalo de \[ 0, 1 \] e é útil para evitar a quebra de artefatos ao mapear uma única imagem em um objeto.</span><span class="sxs-lookup"><span data-stu-id="dc613-133">GL\_CLAMP causes s coordinates to be clamped to the range \[0,1\] and is useful for preventing wrapping artifacts when mapping a single image onto an object.</span></span> <span data-ttu-id="dc613-134">O GL \_ REPEAT faz com que a parte inteira da coordenada s seja ignorada; O OpenGL usa apenas a parte fracionária, criando assim um padrão de repetição.</span><span class="sxs-lookup"><span data-stu-id="dc613-134">GL\_REPEAT causes the integer part of the s coordinate to be ignored; OpenGL uses only the fractional part, thereby creating a repeating pattern.</span></span> <span data-ttu-id="dc613-135">Os elementos de textura de borda serão acessados somente se o encapsulamento estiver definido como GL \_ fixe.</span><span class="sxs-lookup"><span data-stu-id="dc613-135">Border texture elements are accessed only if wrapping is set to GL\_CLAMP.</span></span> <span data-ttu-id="dc613-136">Inicialmente, \_ a textura GL \_ encapsula \_ S está definida como GL \_ REPEAT.</span><span class="sxs-lookup"><span data-stu-id="dc613-136">Initially, GL\_TEXTURE\_WRAP\_S is set to GL\_REPEAT.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <span data-ttu-id="dc613-137"><dt>**\_ \_ & encapsulamento de textura GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dc613-137"><dt>**GL\_TEXTURE\_WRAP\_T**</dt></span></span> </dl>             | <span data-ttu-id="dc613-138">Define o parâmetro Wrap para a coordenada de textura t para GL \_ fixe ou GL \_ REPEAT.</span><span class="sxs-lookup"><span data-stu-id="dc613-138">Sets the wrap parameter for texture coordinate t to either GL\_CLAMP or GL\_REPEAT.</span></span> <span data-ttu-id="dc613-139">Consulte a discussão em GL \_ Texture \_ Wrap \_ S.</span><span class="sxs-lookup"><span data-stu-id="dc613-139">See the discussion under GL\_TEXTURE\_WRAP\_S.</span></span> <span data-ttu-id="dc613-140">Inicialmente, o GL de \_ codificação de textura \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="dc613-140">Initially, GL\_TEXTURE\_WRAP\_T is set to GL\_REPEAT</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="dc613-141">*param*</span><span class="sxs-lookup"><span data-stu-id="dc613-141">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="dc613-142">O valor de *pname*.</span><span class="sxs-lookup"><span data-stu-id="dc613-142">The value of *pname*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc613-143">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dc613-143">Return value</span></span>

<span data-ttu-id="dc613-144">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="dc613-144">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="dc613-145">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="dc613-145">Error codes</span></span>

<span data-ttu-id="dc613-146">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="dc613-146">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="dc613-147">Nome</span><span class="sxs-lookup"><span data-stu-id="dc613-147">Name</span></span>                                                                                                  | <span data-ttu-id="dc613-148">Significado</span><span class="sxs-lookup"><span data-stu-id="dc613-148">Meaning</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dc613-149"><dt>**GL \_ \_Enumeração INválida**</dt></span><span class="sxs-lookup"><span data-stu-id="dc613-149"><dt>**GL\_INVALID\_ENUM** </dt></span></span> </dl>     | <span data-ttu-id="dc613-150">*target* ou *pname* não era um dos valores definidos aceitos, ou quando *param* deveria ter um valor constante definido (com base no valor de *pname*) e não.</span><span class="sxs-lookup"><span data-stu-id="dc613-150">*target* or *pname* was not one of the accepted defined values, or when *param* should have had a defined constant value (based on the value of *pname*) and did not.</span></span><br/> |
| <dl> <span data-ttu-id="dc613-151"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dc613-151"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="dc613-152">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="dc613-152">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                            |



## <a name="remarks"></a><span data-ttu-id="dc613-153">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc613-153">Remarks</span></span>

<span data-ttu-id="dc613-154">O mapeamento de textura é uma técnica que aplica uma imagem à superfície de um objeto como se a imagem fosse um Decal ou uma redução de encolhimento de Cellophane.</span><span class="sxs-lookup"><span data-stu-id="dc613-154">Texture mapping is a technique that applies an image onto an object's surface as if the image were a decal or cellophane shrink-wrap.</span></span> <span data-ttu-id="dc613-155">A imagem é criada no espaço de textura, com um sistema de coordenadas (*s*, *t*).</span><span class="sxs-lookup"><span data-stu-id="dc613-155">The image is created in texture space, with an (*s*, *t*) coordinate system.</span></span> <span data-ttu-id="dc613-156">Uma textura é uma imagem única ou bidimensional e um conjunto de parâmetros que determinam como os exemplos são derivados da imagem.</span><span class="sxs-lookup"><span data-stu-id="dc613-156">A texture is a one- or two-dimensional image and a set of parameters that determine how samples are derived from the image.</span></span>

<span data-ttu-id="dc613-157">A função **glTexParameter** atribui o valor ou valores em params para o parâmetro Texture especificado como pname.</span><span class="sxs-lookup"><span data-stu-id="dc613-157">The **glTexParameter** function assigns the value or values in params to the texture parameter specified as pname.</span></span> <span data-ttu-id="dc613-158">O parâmetro de destino define a textura de destino, ou seja, GL \_ textura \_ 1D ou GL de \_ textura \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="dc613-158">The target parameter defines the target texture, either GL\_TEXTURE\_1D or GL\_TEXTURE\_2D.</span></span>

<span data-ttu-id="dc613-159">Como mais elementos de textura são amostrados no processo de minificação, menos artefatos de alias serão aparentes.</span><span class="sxs-lookup"><span data-stu-id="dc613-159">As more texture elements are sampled in the minification process, fewer aliasing artifacts will be apparent.</span></span> <span data-ttu-id="dc613-160">Embora as \_ \_ funções minificação lineares mais próximas e GL possam ser mais rápidas do que as outras quatro, elas amostram apenas um ou quatro elementos de textura para determinar o valor de textura do pixel que está sendo renderizado e podem produzir padrões de moire ou transições irregulares.</span><span class="sxs-lookup"><span data-stu-id="dc613-160">While the GL\_NEAREST and GL\_LINEAR minification functions can be faster than the other four, they sample only one or four texture elements to determine the texture value of the pixel being rendered and can produce moire patterns or ragged transitions.</span></span> <span data-ttu-id="dc613-161">O valor padrão do filtro GL de \_ textura \_ mínimo \_ é GL \_ \_ MIPMAP linear mais próximo \_ .</span><span class="sxs-lookup"><span data-stu-id="dc613-161">The default value of GL\_TEXTURE\_MIN\_FILTER is GL\_NEAREST\_MIPMAP\_LINEAR.</span></span>

<span data-ttu-id="dc613-162">Suponha que texturing esteja habilitado (chamando [**glEnable**](glenable.md) com o argumento GL \_ Texture \_ 1D ou GL \_ Texture \_ 2D) e \_ \_ o filtro GL min Texture \_ seja definido como uma das funções que exigem um mipmap.</span><span class="sxs-lookup"><span data-stu-id="dc613-162">Suppose that texturing is enabled (by calling [**glEnable**](glenable.md) with argument GL\_TEXTURE\_1D or GL\_TEXTURE\_2D) and GL\_TEXTURE\_MIN\_FILTER is set to one of the functions that requires a mipmap.</span></span> <span data-ttu-id="dc613-163">Se as dimensões das imagens de textura definidas no momento (com chamadas anteriores para [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md)) não seguirem a sequência correta para mipmaps, ou se houver menos imagens de textura definidas do que o necessário, ou o conjunto de imagens de textura tiver diferentes números de componentes de textura, será como se o mapeamento de textura estivesse desabilitado.</span><span class="sxs-lookup"><span data-stu-id="dc613-163">If either the dimensions of the texture images currently defined (with previous calls to [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md)) do not follow the proper sequence for mipmaps, or there are fewer texture images defined than are needed, or the set of texture images have differing numbers of texture components, then it is as if texture mapping were disabled.</span></span> <span data-ttu-id="dc613-164">A filtragem linear acessa os quatro elementos de textura mais próximos somente em texturas 2D.</span><span class="sxs-lookup"><span data-stu-id="dc613-164">Linear filtering accesses the four nearest texture elements only in 2-D textures.</span></span> <span data-ttu-id="dc613-165">Em texturas 1D, a filtragem linear acessa os dois elementos de textura mais próximos.</span><span class="sxs-lookup"><span data-stu-id="dc613-165">In 1-D textures, linear filtering accesses the two nearest texture elements.</span></span> <span data-ttu-id="dc613-166">A função a seguir recupera informações relacionadas a **glTexParameterf**, **glTexParameteri**, **glTexParameterfv** e **glTexParameteriv**:</span><span class="sxs-lookup"><span data-stu-id="dc613-166">The following function retrieves information related to **glTexParameterf**, **glTexParameteri**, **glTexParameterfv**, and **glTexParameteriv**:</span></span>

[<span data-ttu-id="dc613-167">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="dc613-167">**glGetTexParameter**</span></span>](glgettexparameter.md)

## <a name="requirements"></a><span data-ttu-id="dc613-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc613-168">Requirements</span></span>



| <span data-ttu-id="dc613-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc613-169">Requirement</span></span> | <span data-ttu-id="dc613-170">Valor</span><span class="sxs-lookup"><span data-stu-id="dc613-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc613-171">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc613-171">Minimum supported client</span></span><br/> | <span data-ttu-id="dc613-172">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dc613-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="dc613-173">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc613-173">Minimum supported server</span></span><br/> | <span data-ttu-id="dc613-174">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dc613-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dc613-175">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="dc613-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc613-176"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc613-176"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="dc613-177">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dc613-177">Library</span></span><br/>                  | <dl> <span data-ttu-id="dc613-178"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc613-178"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="dc613-179">DLL</span><span class="sxs-lookup"><span data-stu-id="dc613-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc613-180"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc613-180"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc613-181">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc613-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc613-182">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="dc613-182">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="dc613-183">**glBindTexture**</span><span class="sxs-lookup"><span data-stu-id="dc613-183">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="dc613-184">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="dc613-184">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="dc613-185">**glCopyTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="dc613-185">**glCopyTexImage1D**</span></span>](glcopyteximage1d.md)
</dt> <dt>

[<span data-ttu-id="dc613-186">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="dc613-186">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="dc613-187">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="dc613-187">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="dc613-188">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="dc613-188">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="dc613-189">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="dc613-189">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="dc613-190">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="dc613-190">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="dc613-191">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="dc613-191">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="dc613-192">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="dc613-192">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="dc613-193">**glPrioritizeTextures**</span><span class="sxs-lookup"><span data-stu-id="dc613-193">**glPrioritizeTextures**</span></span>](glprioritizetextures.md)
</dt> <dt>

[<span data-ttu-id="dc613-194">glTexEnv</span><span class="sxs-lookup"><span data-stu-id="dc613-194">glTexEnv</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="dc613-195">glTexGen</span><span class="sxs-lookup"><span data-stu-id="dc613-195">glTexGen</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="dc613-196">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="dc613-196">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="dc613-197">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="dc613-197">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="dc613-198">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="dc613-198">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="dc613-199">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="dc613-199">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> </dl>

 

 





