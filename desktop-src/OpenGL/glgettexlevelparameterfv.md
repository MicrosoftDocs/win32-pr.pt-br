---
title: função glGetTexLevelParameterfv (GL. h)
description: As funções glGetTexLevelParameterfv e glGetTexLevelParameteriv retornam valores de parâmetro de textura para um nível específico de detalhes. | função glGetTexLevelParameterfv (GL. h)
ms.assetid: 5ea91f2e-c0cd-41ee-be95-df096f1c78ef
keywords:
- função glGetTexLevelParameterfv OpenGL
topic_type:
- apiref
api_name:
- glGetTexLevelParameterfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92f8b55b41d3538f116241a0401cedf643a5e55
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105756396"
---
# <a name="glgettexlevelparameterfv-function"></a><span data-ttu-id="69d6a-105">função glGetTexLevelParameterfv</span><span class="sxs-lookup"><span data-stu-id="69d6a-105">glGetTexLevelParameterfv function</span></span>

<span data-ttu-id="69d6a-106">As funções **glGetTexLevelParameterfv** e [**glGetTexLevelParameteriv**](glgettexlevelparameteriv.md) retornam valores de parâmetro de textura para um nível específico de detalhes.</span><span class="sxs-lookup"><span data-stu-id="69d6a-106">The **glGetTexLevelParameterfv** and [**glGetTexLevelParameteriv**](glgettexlevelparameteriv.md) functions return texture parameter values for a specific level of detail.</span></span>

## <a name="syntax"></a><span data-ttu-id="69d6a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="69d6a-107">Syntax</span></span>


```C++
void WINAPI glGetTexLevelParameterfv(
   GLenum  target,
   GLint   level,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="69d6a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69d6a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69d6a-109">*destino*</span><span class="sxs-lookup"><span data-stu-id="69d6a-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="69d6a-110">O nome simbólico da textura de destino: uma textura \_ GL \_ 1D, GL \_ Texture \_ 2D, GL \_ proxybinding bidirecionalmente ou o \_ \_ \_ proxy GL \_ textura \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="69d6a-110">The symbolic name of the target texture: either GL\_TEXTURE\_1D, GL\_TEXTURE\_2D, GL\_PROXY\_TEXTURE\_1D, or GL\_PROXY\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="69d6a-111">*level*</span><span class="sxs-lookup"><span data-stu-id="69d6a-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="69d6a-112">O número de nível de detalhe da imagem desejada.</span><span class="sxs-lookup"><span data-stu-id="69d6a-112">The level-of-detail number of the desired image.</span></span> <span data-ttu-id="69d6a-113">Nível 0 é o nível de imagem base.</span><span class="sxs-lookup"><span data-stu-id="69d6a-113">Level 0 is the base image level.</span></span> <span data-ttu-id="69d6a-114">O nível *n* é a imagem de redução *n* º mipmap.</span><span class="sxs-lookup"><span data-stu-id="69d6a-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="69d6a-115">*pname*</span><span class="sxs-lookup"><span data-stu-id="69d6a-115">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="69d6a-116">O nome simbólico de um parâmetro de textura.</span><span class="sxs-lookup"><span data-stu-id="69d6a-116">The symbolic name of a texture parameter.</span></span> <span data-ttu-id="69d6a-117">Os nomes de parâmetro a seguir são aceitos.</span><span class="sxs-lookup"><span data-stu-id="69d6a-117">The following parameter names are accepted.</span></span>



| <span data-ttu-id="69d6a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="69d6a-118">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="69d6a-119">Significado</span><span class="sxs-lookup"><span data-stu-id="69d6a-119">Meaning</span></span>                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span><dl> <span data-ttu-id="69d6a-120"><dt>**\_largura da textura GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="69d6a-120"><dt>**GL\_TEXTURE\_WIDTH**</dt></span></span> </dl>                                | <span data-ttu-id="69d6a-121">O parâmetro *params* retorna um único valor que contém a largura da imagem de textura.</span><span class="sxs-lookup"><span data-stu-id="69d6a-121">The *params* parameter returns a single value containing the width of the texture image.</span></span> <span data-ttu-id="69d6a-122">Esse valor inclui a borda da imagem de textura.</span><span class="sxs-lookup"><span data-stu-id="69d6a-122">This value includes the border of the texture image.</span></span><br/>                                                                                                                                          |
| <span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span><dl> <span data-ttu-id="69d6a-123"><dt>**\_altura da textura GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="69d6a-123"><dt>**GL\_TEXTURE\_HEIGHT**</dt></span></span> </dl>                             | <span data-ttu-id="69d6a-124">O parâmetro *params* retorna um único valor que contém a altura da imagem de textura.</span><span class="sxs-lookup"><span data-stu-id="69d6a-124">The *params* parameter returns a single value containing the height of the texture image.</span></span> <span data-ttu-id="69d6a-125">Esse valor inclui a borda da imagem de textura.</span><span class="sxs-lookup"><span data-stu-id="69d6a-125">This value includes the border of the texture image.</span></span><br/>                                                                                                                                         |
| <span id="GL_TEXTURE_INTERNAL_FORMAT"></span><span id="gl_texture_internal_format"></span><dl> <span data-ttu-id="69d6a-126"><dt>**\_ \_ formato interno de textura GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="69d6a-126"><dt>**GL\_TEXTURE\_INTERNAL\_FORMAT**</dt></span></span> </dl> | <span data-ttu-id="69d6a-127">O parâmetro *params* retorna um único valor que descreve o formato Texel da textura.</span><span class="sxs-lookup"><span data-stu-id="69d6a-127">The *params* parameter returns a single value which describes the texel format of the texture.</span></span><br/>                                                                                                                                                                                         |
| <span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span><dl> <span data-ttu-id="69d6a-128"><dt>**\_borda de textura GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="69d6a-128"><dt>**GL\_TEXTURE\_BORDER**</dt></span></span> </dl>                             | <span data-ttu-id="69d6a-129">O parâmetro *params* retorna um único valor: a largura em pixels da borda da imagem de textura.</span><span class="sxs-lookup"><span data-stu-id="69d6a-129">The *params* parameter returns a single value: the width in pixels of the border of the texture image.</span></span><br/>                                                                                                                                                                                 |
| <span id="GL_TEXTURE_RED_SIZE"></span><span id="gl_texture_red_size"></span><dl> <span data-ttu-id="69d6a-130"><dt>**\_ \_ tamanho vermelho da textura GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="69d6a-130"><dt>**GL\_TEXTURE\_RED\_SIZE**</dt></span></span> </dl>                      | <span data-ttu-id="69d6a-131">A resolução de armazenamento interno do componente vermelho de um Texel.</span><span class="sxs-lookup"><span data-stu-id="69d6a-131">The internal storage resolution of the red component of a texel.</span></span> <span data-ttu-id="69d6a-132">A resolução escolhida pelo OpenGL será uma correspondência próxima para a resolução solicitada pelo usuário com o argumento de componente de [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="69d6a-132">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>       |
| <span id="GL_TEXTURE_GREEN_SIZE"></span><span id="gl_texture_green_size"></span><dl> <span data-ttu-id="69d6a-133"><dt>**\_ \_ Tamanho verde de textura GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="69d6a-133"><dt>**GL\_TEXTURE\_GREEN\_SIZE**</dt></span></span> </dl>                | <span data-ttu-id="69d6a-134">A resolução de armazenamento interno do componente verde de um Texel.</span><span class="sxs-lookup"><span data-stu-id="69d6a-134">The internal storage resolution of the green component of a texel.</span></span> <span data-ttu-id="69d6a-135">A resolução escolhida pelo OpenGL será uma correspondência próxima para a resolução solicitada pelo usuário com o argumento de componente de [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="69d6a-135">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>     |
| <span id="GL_TEXTURE_BLUE_SIZE"></span><span id="gl_texture_blue_size"></span><dl> <span data-ttu-id="69d6a-136"><dt>**\_ \_ tamanho azul de textura GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="69d6a-136"><dt>**GL\_TEXTURE\_BLUE\_SIZE**</dt></span></span> </dl>                   | <span data-ttu-id="69d6a-137">A resolução de armazenamento interno do componente azul de um Texel.</span><span class="sxs-lookup"><span data-stu-id="69d6a-137">The internal storage resolution of the blue component of a texel.</span></span> <span data-ttu-id="69d6a-138">A resolução escolhida pelo OpenGL será uma correspondência próxima para a resolução solicitada pelo usuário com o argumento de componente de [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="69d6a-138">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>      |
| <span id="GL_TEXTURE_ALPHA_SIZE"></span><span id="gl_texture_alpha_size"></span><dl> <span data-ttu-id="69d6a-139"><dt>**\_ \_ tamanho alfa da textura GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="69d6a-139"><dt>**GL\_TEXTURE\_ALPHA\_SIZE**</dt></span></span> </dl>                | <span data-ttu-id="69d6a-140">A resolução de armazenamento interno do componente alfa de um Texel.</span><span class="sxs-lookup"><span data-stu-id="69d6a-140">The internal storage resolution of the alpha component of a texel.</span></span> <span data-ttu-id="69d6a-141">A resolução escolhida pelo OpenGL será uma correspondência próxima para a resolução solicitada pelo usuário com o argumento de componente de [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="69d6a-141">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>     |
| <span id="GL_TEXTURE_LUMINANCE_SIZE"></span><span id="gl_texture_luminance_size"></span><dl> <span data-ttu-id="69d6a-142"><dt>**\_tamanho de \_ luminância de textura GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="69d6a-142"><dt>**GL\_TEXTURE\_LUMINANCE\_SIZE**</dt></span></span> </dl>    | <span data-ttu-id="69d6a-143">A resolução de armazenamento interno do componente de luminância de um Texel.</span><span class="sxs-lookup"><span data-stu-id="69d6a-143">The internal storage resolution of the luminance component of a texel.</span></span> <span data-ttu-id="69d6a-144">A resolução escolhida pelo OpenGL será uma correspondência próxima para a resolução solicitada pelo usuário com o argumento de componente de [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="69d6a-144">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/> |
| <span id="GL_TEXTURE_INTENSITY_SIZE"></span><span id="gl_texture_intensity_size"></span><dl> <span data-ttu-id="69d6a-145"><dt>**\_tamanho de \_ intensidade de textura GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="69d6a-145"><dt>**GL\_TEXTURE\_INTENSITY\_SIZE**</dt></span></span> </dl>    | <span data-ttu-id="69d6a-146">A resolução de armazenamento interno do componente de intensidade de um Texel.</span><span class="sxs-lookup"><span data-stu-id="69d6a-146">The internal storage resolution of the intensity component of a texel.</span></span> <span data-ttu-id="69d6a-147">A resolução escolhida pelo OpenGL será uma correspondência próxima para a resolução solicitada pelo usuário com o argumento de componente de [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="69d6a-147">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/> |
| <span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span><dl> <span data-ttu-id="69d6a-148"><dt>**\_componentes de textura GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="69d6a-148"><dt>**GL\_TEXTURE\_COMPONENTS**</dt></span></span> </dl>                 | <span data-ttu-id="69d6a-149">O parâmetro *params* retorna um único valor: o número de componentes na imagem de textura.</span><span class="sxs-lookup"><span data-stu-id="69d6a-149">The *params* parameter returns a single value: the number of components in the texture image.</span></span><br/>                                                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="69d6a-150">*params*</span><span class="sxs-lookup"><span data-stu-id="69d6a-150">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="69d6a-151">Retorna os dados solicitados.</span><span class="sxs-lookup"><span data-stu-id="69d6a-151">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69d6a-152">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="69d6a-152">Return value</span></span>

<span data-ttu-id="69d6a-153">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="69d6a-153">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="69d6a-154">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="69d6a-154">Error codes</span></span>

<span data-ttu-id="69d6a-155">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="69d6a-155">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="69d6a-156">Nome</span><span class="sxs-lookup"><span data-stu-id="69d6a-156">Name</span></span>                                                                                                  | <span data-ttu-id="69d6a-157">Significado</span><span class="sxs-lookup"><span data-stu-id="69d6a-157">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="69d6a-158"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="69d6a-158"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="69d6a-159">*target* ou *pname* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="69d6a-159">*target* or *pname* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="69d6a-160"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="69d6a-160"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="69d6a-161">o *nível* é menor que zero ou maior que o *log* 2 *(max)*, em que *Max* é o valor retornado do \_ tamanho de textura Max GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="69d6a-161">*level* is less than zero or greater than *log* 2 *(max)*, where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>      |
| <dl> <span data-ttu-id="69d6a-162"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="69d6a-162"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="69d6a-163">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="69d6a-163">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="69d6a-164">Comentários</span><span class="sxs-lookup"><span data-stu-id="69d6a-164">Remarks</span></span>

<span data-ttu-id="69d6a-165">A função **glGetTexLevelParameter** retorna nos valores de parâmetro de textura de *params* para um valor de nível de detalhe específico, especificado como *nível*.</span><span class="sxs-lookup"><span data-stu-id="69d6a-165">The **glGetTexLevelParameter** function returns in *params* texture parameter values for a specific level-of-detail value, specified as *level*.</span></span> <span data-ttu-id="69d6a-166">O parâmetro de *destino* define a textura de destino, tanto a \_ textura GL \_ 1D, GL \_ Texture \_ 2D, GL \_ proxy \_ \_ de textura 1D ou GL \_ proxy de destino \_ \_ 2D para especificar um texturing unidimensional ou bidimensional.</span><span class="sxs-lookup"><span data-stu-id="69d6a-166">The *target* parameter defines the target texture, either GL\_TEXTURE\_1D, GL\_TEXTURE\_2D, GL\_PROXY\_TEXTURE\_1D, or GL\_PROXY\_TEXTURE\_2D to specify one-dimensional or two-dimensional texturing.</span></span> <span data-ttu-id="69d6a-167">O parâmetro *pname* especifica o parâmetro de textura cujo valor ou valores serão retornados.</span><span class="sxs-lookup"><span data-stu-id="69d6a-167">The *pname* parameter specifies the texture parameter whose value or values will be returned.</span></span>

<span data-ttu-id="69d6a-168">Se um erro for gerado, nenhuma alteração será feita no conteúdo de *params*.</span><span class="sxs-lookup"><span data-stu-id="69d6a-168">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="69d6a-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69d6a-169">Requirements</span></span>



| <span data-ttu-id="69d6a-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="69d6a-170">Requirement</span></span> | <span data-ttu-id="69d6a-171">Valor</span><span class="sxs-lookup"><span data-stu-id="69d6a-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69d6a-172">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69d6a-172">Minimum supported client</span></span><br/> | <span data-ttu-id="69d6a-173">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="69d6a-173">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="69d6a-174">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69d6a-174">Minimum supported server</span></span><br/> | <span data-ttu-id="69d6a-175">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="69d6a-175">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="69d6a-176">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="69d6a-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="69d6a-177"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="69d6a-177"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="69d6a-178">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="69d6a-178">Library</span></span><br/>                  | <dl> <span data-ttu-id="69d6a-179"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69d6a-179"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="69d6a-180">DLL</span><span class="sxs-lookup"><span data-stu-id="69d6a-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69d6a-181"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69d6a-181"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69d6a-182">Confira também</span><span class="sxs-lookup"><span data-stu-id="69d6a-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69d6a-183">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="69d6a-183">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="69d6a-184">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="69d6a-184">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="69d6a-185">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="69d6a-185">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="69d6a-186">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="69d6a-186">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="69d6a-187">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="69d6a-187">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="69d6a-188">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="69d6a-188">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





