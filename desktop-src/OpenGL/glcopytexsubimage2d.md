---
title: função glCopyTexSubImage2D (GL. h)
description: A função glCopyTexSubImage2D copia uma subimagem de uma imagem de textura bidimensional do framebuffer.
ms.assetid: cbb644d4-6a23-4d66-8599-5f8b48e9b91f
keywords:
- função glCopyTexSubImage2D OpenGL
topic_type:
- apiref
api_name:
- glCopyTexSubImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c966d031bb154b59cc54ae2e5d254347aa88d2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369696"
---
# <a name="glcopytexsubimage2d-function"></a><span data-ttu-id="77d15-104">função glCopyTexSubImage2D</span><span class="sxs-lookup"><span data-stu-id="77d15-104">glCopyTexSubImage2D function</span></span>

<span data-ttu-id="77d15-105">A função **glCopyTexSubImage2D** copia uma subimagem de uma imagem de textura bidimensional do framebuffer.</span><span class="sxs-lookup"><span data-stu-id="77d15-105">The **glCopyTexSubImage2D** function copies a sub-image of a two-dimensional texture image from the framebuffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="77d15-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="77d15-106">Syntax</span></span>


```C++
void WINAPI glCopyTexSubImage2D(
   GLenum  target,
   GLint   level,
   GLint   xoffset,
   GLint   yoffset,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a><span data-ttu-id="77d15-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77d15-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77d15-108">*destino*</span><span class="sxs-lookup"><span data-stu-id="77d15-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="77d15-109">O destino para o qual os dados da imagem serão alterados.</span><span class="sxs-lookup"><span data-stu-id="77d15-109">The target to which the image data will be changed.</span></span> <span data-ttu-id="77d15-110">Deve ter o valor GL de \_ textura \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="77d15-110">Must have the value GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="77d15-111">*level*</span><span class="sxs-lookup"><span data-stu-id="77d15-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="77d15-112">O número de nível de detalhe.</span><span class="sxs-lookup"><span data-stu-id="77d15-112">The level-of-detail number.</span></span> <span data-ttu-id="77d15-113">Nível 0 é a imagem base.</span><span class="sxs-lookup"><span data-stu-id="77d15-113">Level 0 is the base image.</span></span> <span data-ttu-id="77d15-114">O nível *n* é a imagem de redução *n* º mipmap.</span><span class="sxs-lookup"><span data-stu-id="77d15-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="77d15-115">*xoffset*</span><span class="sxs-lookup"><span data-stu-id="77d15-115">*xoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="77d15-116">O deslocamento de Texel na direção *x* dentro da matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="77d15-116">The texel offset in the *x* direction within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="77d15-117">*yoffset*</span><span class="sxs-lookup"><span data-stu-id="77d15-117">*yoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="77d15-118">O deslocamento de Texel na direção *y* dentro da matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="77d15-118">The texel offset in the *y* direction within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="77d15-119">*x*</span><span class="sxs-lookup"><span data-stu-id="77d15-119">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="77d15-120">As coordenadas do plano x da janela do canto inferior esquerdo da linha de pixels a serem copiadas.</span><span class="sxs-lookup"><span data-stu-id="77d15-120">The window x-plane coordinates of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="77d15-121">*y*</span><span class="sxs-lookup"><span data-stu-id="77d15-121">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="77d15-122">As coordenadas do plano y da janela do canto inferior esquerdo da linha de pixels a serem copiadas.</span><span class="sxs-lookup"><span data-stu-id="77d15-122">The window y-plane coordinates of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="77d15-123">*width*</span><span class="sxs-lookup"><span data-stu-id="77d15-123">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="77d15-124">A largura da subimagem da imagem de textura.</span><span class="sxs-lookup"><span data-stu-id="77d15-124">The width of the sub-image of the texture image.</span></span> <span data-ttu-id="77d15-125">A especificação de uma subimagem de textura com largura zero não tem efeito.</span><span class="sxs-lookup"><span data-stu-id="77d15-125">Specifying a texture sub-image with zero width has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="77d15-126">*altura*</span><span class="sxs-lookup"><span data-stu-id="77d15-126">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="77d15-127">A altura da subimagem da imagem de textura.</span><span class="sxs-lookup"><span data-stu-id="77d15-127">The height of the sub-image of the texture image.</span></span> <span data-ttu-id="77d15-128">A especificação de uma subimagem de textura com largura zero não tem efeito.</span><span class="sxs-lookup"><span data-stu-id="77d15-128">Specifying a texture sub-image with zero width has no effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77d15-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="77d15-129">Return value</span></span>

<span data-ttu-id="77d15-130">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="77d15-130">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="77d15-131">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="77d15-131">Error codes</span></span>

<span data-ttu-id="77d15-132">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="77d15-132">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="77d15-133">Nome</span><span class="sxs-lookup"><span data-stu-id="77d15-133">Name</span></span>                                                                                                  | <span data-ttu-id="77d15-134">Significado</span><span class="sxs-lookup"><span data-stu-id="77d15-134">Meaning</span></span>                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="77d15-135"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="77d15-135"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="77d15-136">o *destino* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="77d15-136">*target* was not an accepted value.</span></span><br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="77d15-137"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="77d15-137"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="77d15-138">o *nível* era menor que zero ou maior que o *log* 2 (*Max*), em que *Max* é o valor retornado do \_ tamanho de textura Max GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="77d15-138">*level* was less than zero or greater than *log* 2 (*max*), where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="77d15-139"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="77d15-139"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="77d15-140">*xoffset* era menor do que *Border* ou (largura de *xoffset*  +  ) era maior que (*l*  +  *Border*), *yoffset* era menor que *Border* ou (*yoffset*  +  *Height*) era maior que(a  +  *Border*), em que *w* é a largura de textura GL \_ \_ e *Border* é a borda de textura GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="77d15-140">*xoffset* was less than *border* or (*xoffset* + *width*)was greater than (*w* + *border*), *yoffset* was less than *border*, or (*yoffset* + *height*) was greater than (*h* + *border*), where *w* is GL\_TEXTURE\_WIDTH and *border* is GL\_TEXTURE\_BORDER.</span></span> <span data-ttu-id="77d15-141">Observe que *w* inclui duas vezes a largura da *borda* .</span><span class="sxs-lookup"><span data-stu-id="77d15-141">Note that *w* includes twice the *border* width.</span></span><br/> |
| <dl> <span data-ttu-id="77d15-142"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="77d15-142"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="77d15-143">a *largura* era menor *que Border* ou *y* era menor que *Border*, em que *Border* é a largura da borda da matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="77d15-143">*width* was less than *border* or *y* was less than *border*, where *border* is the border width of the texture array.</span></span><br/>                                                                                                                                                                                           |
| <dl> <span data-ttu-id="77d15-144"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="77d15-144"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="77d15-145">A matriz de textura não foi definida por uma operação [**glTexImage1D**](glteximage1d.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="77d15-145">The texture array was not defined by a previous [**glTexImage1D**](glteximage1d.md) operation.</span></span><br/>                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="77d15-146"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="77d15-146"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="77d15-147">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="77d15-147">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                                                                                                                       |



## <a name="remarks"></a><span data-ttu-id="77d15-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="77d15-148">Remarks</span></span>

<span data-ttu-id="77d15-149">A função **glCopyTexSubImage2D** substitui uma parte retangular de uma imagem de textura bidimensional por pixels da framebuffer atual, e não da memória principal, como é o caso de [**glTexSubImage2D**](gltexsubimage2d.md).</span><span class="sxs-lookup"><span data-stu-id="77d15-149">The **glCopyTexSubImage2D** function replaces a rectangular portion of a two-dimensional texture image with pixels from the current framebuffer, rather than from main memory as is the case for [**glTexSubImage2D**](gltexsubimage2d.md).</span></span>

<span data-ttu-id="77d15-150">Um retângulo de pixels que começa com as coordenadas da janela *x* e *y* e com a *largura* e a *altura* das dimensões substitui a parte da matriz de textura com os índices *xoffset* por meio de *xoffset* + (*Width* -1), pelos índices *yoffset* por meio de *yoffset* + (*Width* -1) no nível de mipmap especificado pelo *nível*.</span><span class="sxs-lookup"><span data-stu-id="77d15-150">A rectangle of pixels beginning with the *x* and *y* window coordinates and with the dimensions *width* and *height* replaces the portion of the texture array with the indexes *xoffset* through *xoffset* + (*width* - 1), with the indexes *yoffset* through *yoffset* + (*width* - 1) at the mipmap level specified by *level*.</span></span> <span data-ttu-id="77d15-151">O retângulo de destino na matriz de textura não pode incluir nenhum texels fora da matriz de textura especificada originalmente.</span><span class="sxs-lookup"><span data-stu-id="77d15-151">The destination rectangle in the texture array cannot include any texels outside the originally specified texture array.</span></span>

<span data-ttu-id="77d15-152">A função **glCopyTexSubImage2D** processa os pixels em uma linha da mesma maneira que [**glCopyPixels**](glcopypixels.md), exceto que antes da conversão final dos pixels, todos os valores de componentes de pixel são clamped para o intervalo de \[ 0, 1 \] e convertidos para o formato interno da textura para armazenamento na matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="77d15-152">The **glCopyTexSubImage2D** function processes the pixels in a row in the same way as [**glCopyPixels**](glcopypixels.md), except that before the final conversion of the pixels, all pixel component values are clamped to the range \[0,1\] and converted to the texture's internal format for storage in the texture array.</span></span> <span data-ttu-id="77d15-153">A ordenação de pixels é determinada com coordenadas *x* inferiores correspondentes às coordenadas de textura inferiores.</span><span class="sxs-lookup"><span data-stu-id="77d15-153">Pixel ordering is determined with lower *x* coordinates corresponding to lower texture coordinates.</span></span> <span data-ttu-id="77d15-154">Se qualquer um dos pixels dentro de uma linha especificada da framebuffer atual estiver fora da janela associada ao contexto de renderização atual, seus valores serão indefinidos.</span><span class="sxs-lookup"><span data-stu-id="77d15-154">If any of the pixels within a specified row of the current framebuffer are outside the window associated with the current rendering context, then their values are undefined.</span></span>

<span data-ttu-id="77d15-155">Se qualquer um dos pixels dentro do retângulo especificado do framebuffer atual estiver fora da janela de leitura associada ao contexto de renderização atual, os valores obtidos para esses pixels serão indefinidos.</span><span class="sxs-lookup"><span data-stu-id="77d15-155">If any of the pixels within the specified rectangle of the current framebuffer are outside the read window associated with the current rendering context, then the values obtained for those pixels are undefined.</span></span> <span data-ttu-id="77d15-156">Nenhuma alteração é feita no parâmetro *internalFormat*, *largura*, *altura* ou *borda* da matriz de textura especificada ou Texel valores fora da subimagem de textura especificada.</span><span class="sxs-lookup"><span data-stu-id="77d15-156">No change is made to the *internalFormat*, *width*, *height*, or *border* parameter of the specified texture array or to texel values outside the specified texture sub-image.</span></span>

<span data-ttu-id="77d15-157">Você não pode incluir chamadas para **glCopyTexSubImage2D** em listas de exibição.</span><span class="sxs-lookup"><span data-stu-id="77d15-157">You cannot include calls to **glCopyTexSubImage2D** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="77d15-158">A função **glCopyTexSubImage2D** só está disponível no OpenGL versão 1,1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="77d15-158">The **glCopyTexSubImage2D** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="77d15-159">Texturing não tem efeito no modo de índice de cor.</span><span class="sxs-lookup"><span data-stu-id="77d15-159">Texturing has no effect in color-index mode.</span></span> <span data-ttu-id="77d15-160">As funções [**glPixelStore**](glpixelstore-functions.md) e [**glPixelTransfer**](glpixeltransfer.md) afetam as imagens de textura exatamente como elas afetam a maneira como os pixels são desenhados usando [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="77d15-160">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) functions affect texture images in exactly the way they affect the way pixels are drawn using [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="77d15-161">As funções a seguir recuperam informações relacionadas ao **glCopyTexSubImage2D**:</span><span class="sxs-lookup"><span data-stu-id="77d15-161">The following functions retrieve information related to **glCopyTexSubImage2D**:</span></span>

[<span data-ttu-id="77d15-162">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="77d15-162">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="77d15-163">[**glIsEnabled**](glisenabled.md) com a textura do argumento GL \_ \_ 2D</span><span class="sxs-lookup"><span data-stu-id="77d15-163">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_2D</span></span>

## <a name="requirements"></a><span data-ttu-id="77d15-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77d15-164">Requirements</span></span>



| <span data-ttu-id="77d15-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="77d15-165">Requirement</span></span> | <span data-ttu-id="77d15-166">Valor</span><span class="sxs-lookup"><span data-stu-id="77d15-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77d15-167">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77d15-167">Minimum supported client</span></span><br/> | <span data-ttu-id="77d15-168">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="77d15-168">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="77d15-169">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77d15-169">Minimum supported server</span></span><br/> | <span data-ttu-id="77d15-170">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="77d15-170">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="77d15-171">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="77d15-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="77d15-172"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="77d15-172"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="77d15-173">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="77d15-173">Library</span></span><br/>                  | <dl> <span data-ttu-id="77d15-174"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77d15-174"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="77d15-175">DLL</span><span class="sxs-lookup"><span data-stu-id="77d15-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77d15-176"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77d15-176"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77d15-177">Confira também</span><span class="sxs-lookup"><span data-stu-id="77d15-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77d15-178">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="77d15-178">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="77d15-179">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="77d15-179">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="77d15-180">**glCopyTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="77d15-180">**glCopyTexSubImage1D**</span></span>](glcopytexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="77d15-181">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="77d15-181">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="77d15-182">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="77d15-182">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="77d15-183">**glFog**</span><span class="sxs-lookup"><span data-stu-id="77d15-183">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="77d15-184">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="77d15-184">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="77d15-185">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="77d15-185">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="77d15-186">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="77d15-186">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="77d15-187">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="77d15-187">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="77d15-188">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="77d15-188">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="77d15-189">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="77d15-189">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="77d15-190">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="77d15-190">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





