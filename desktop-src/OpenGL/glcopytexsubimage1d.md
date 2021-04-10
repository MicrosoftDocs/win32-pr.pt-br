---
title: função glCopyTexSubImage1D (GL. h)
description: A função glCopyTexSubImage1D copia uma subimagem de uma imagem de textura unidimensional do framebuffer.
ms.assetid: 718aee8a-6dce-49e1-a441-19beccd89f8d
keywords:
- função glCopyTexSubImage1D OpenGL
topic_type:
- apiref
api_name:
- glCopyTexSubImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64006f9cec7e5fd2f3ca6f860249e579b16dbf10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918681"
---
# <a name="glcopytexsubimage1d-function"></a><span data-ttu-id="d3a85-104">função glCopyTexSubImage1D</span><span class="sxs-lookup"><span data-stu-id="d3a85-104">glCopyTexSubImage1D function</span></span>

<span data-ttu-id="d3a85-105">A função **glCopyTexSubImage1D** copia uma subimagem de uma imagem de textura unidimensional do framebuffer.</span><span class="sxs-lookup"><span data-stu-id="d3a85-105">The **glCopyTexSubImage1D** function copies a sub-image of a one-dimensional texture image from the framebuffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3a85-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3a85-106">Syntax</span></span>


```C++
void WINAPI glCopyTexSubImage1D(
   GLenum  target,
   GLint   level,
   GLint   xoffset,
   GLint   x,
   GLint   y,
   GLsizei width
);
```



## <a name="parameters"></a><span data-ttu-id="d3a85-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3a85-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3a85-108">*destino*</span><span class="sxs-lookup"><span data-stu-id="d3a85-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="d3a85-109">O destino para o qual os dados da imagem serão alterados.</span><span class="sxs-lookup"><span data-stu-id="d3a85-109">The target to which the image data will be changed.</span></span> <span data-ttu-id="d3a85-110">Deve ter o valor GL \_ Texture \_ 1D.</span><span class="sxs-lookup"><span data-stu-id="d3a85-110">Must have the value GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="d3a85-111">*level*</span><span class="sxs-lookup"><span data-stu-id="d3a85-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="d3a85-112">O número de nível de detalhe.</span><span class="sxs-lookup"><span data-stu-id="d3a85-112">The level-of-detail number.</span></span> <span data-ttu-id="d3a85-113">Nível 0 é a imagem base.</span><span class="sxs-lookup"><span data-stu-id="d3a85-113">Level 0 is the base image.</span></span> <span data-ttu-id="d3a85-114">O nível *n* é a imagem de redução *n* º mipmap.</span><span class="sxs-lookup"><span data-stu-id="d3a85-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="d3a85-115">*xoffset*</span><span class="sxs-lookup"><span data-stu-id="d3a85-115">*xoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="d3a85-116">O deslocamento de Texel dentro da matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="d3a85-116">The texel offset within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="d3a85-117">*x*</span><span class="sxs-lookup"><span data-stu-id="d3a85-117">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="d3a85-118">A coordenada do plano x da janela do canto inferior esquerdo da linha de pixels a ser copiada.</span><span class="sxs-lookup"><span data-stu-id="d3a85-118">The window x-plane coordinate of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="d3a85-119">*y*</span><span class="sxs-lookup"><span data-stu-id="d3a85-119">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="d3a85-120">A coordenada de plano y da janela do canto inferior esquerdo da linha de pixels a ser copiada.</span><span class="sxs-lookup"><span data-stu-id="d3a85-120">The window y-plane coordinate of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="d3a85-121">*width*</span><span class="sxs-lookup"><span data-stu-id="d3a85-121">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="d3a85-122">A largura da subimagem da imagem de textura.</span><span class="sxs-lookup"><span data-stu-id="d3a85-122">The width of the sub-image of the texture image.</span></span> <span data-ttu-id="d3a85-123">A especificação de uma subimagem de textura com largura zero não tem efeito.</span><span class="sxs-lookup"><span data-stu-id="d3a85-123">Specifying a texture sub-image with zero width has no effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3a85-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d3a85-124">Return value</span></span>

<span data-ttu-id="d3a85-125">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d3a85-125">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d3a85-126">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="d3a85-126">Error codes</span></span>

<span data-ttu-id="d3a85-127">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="d3a85-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="d3a85-128">Nome</span><span class="sxs-lookup"><span data-stu-id="d3a85-128">Name</span></span>                                                                                                  | <span data-ttu-id="d3a85-129">Significado</span><span class="sxs-lookup"><span data-stu-id="d3a85-129">Meaning</span></span>                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d3a85-130"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="d3a85-130"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="d3a85-131">o *destino* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="d3a85-131">*target* was not an accepted value.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="d3a85-132"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d3a85-132"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="d3a85-133">o *nível* era menor que zero ou o *nível* é maior que o *log* 2 (*Max*), em que *Max* é o valor retornado do \_ tamanho de textura Max GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d3a85-133">*level* was less than zero or *level* is greater than *log* 2(*max*), where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="d3a85-134"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d3a85-134"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="d3a85-135">*xoffset* era menor que *Border* ou (  +  *largura* de xoffset) era maior que (*w*  +  *Border*), em que *w* é a \_ \_ largura de textura GL e *Border* é a borda de \_ textura GL \_ .</span><span class="sxs-lookup"><span data-stu-id="d3a85-135">*xoffset* was less than *border* or (*xoffset* + *width*)was greater than (*w* + *border*), where *w* is GL\_TEXTURE\_WIDTH and *border* is GL\_TEXTURE\_BORDER.</span></span> <span data-ttu-id="d3a85-136">Observe que *w* inclui duas vezes a largura da *borda* .</span><span class="sxs-lookup"><span data-stu-id="d3a85-136">Note that *w* includes twice the *border* width.</span></span><br/> |
| <dl> <span data-ttu-id="d3a85-137"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d3a85-137"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="d3a85-138">a *largura* era menor *que Border* ou *y* era menor que *Border*, em que *Border* é a largura da borda da matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="d3a85-138">*width* was less than *border* or *y* was less than *border*, where *border* is the border width of the texture array.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="d3a85-139"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d3a85-139"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d3a85-140">A matriz de textura não foi definida por uma operação [**glTexImage1D**](glteximage1d.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="d3a85-140">The texture array was not defined by a previous [**glTexImage1D**](glteximage1d.md) operation.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="d3a85-141"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d3a85-141"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d3a85-142">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="d3a85-142">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                        |



## <a name="remarks"></a><span data-ttu-id="d3a85-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3a85-143">Remarks</span></span>

<span data-ttu-id="d3a85-144">A função **glCopyTexSubImage1D** substitui uma parte de uma imagem de textura unidimensional usando pixels da framebuffer atual, em vez de memória principal, como é o caso para [**glTexSubImage1D**](gltexsubimage1d.md).</span><span class="sxs-lookup"><span data-stu-id="d3a85-144">The **glCopyTexSubImage1D** function replaces a portion of a one-dimensional texture image using pixels from the current framebuffer, rather than from main memory as is the case for [**glTexSubImage1D**](gltexsubimage1d.md).</span></span>

<span data-ttu-id="d3a85-145">Uma linha de pixels que começa com as coordenadas de janela especificadas por *x* e *y* e com a *largura* de comprimento substitui a parte da matriz de textura pelos índices *xoffset* por meio de *xoffset* + (*Width* -1).</span><span class="sxs-lookup"><span data-stu-id="d3a85-145">A row of pixels beginning with the window coordinates specified by *x* and *y* and with the length *width* replaces the portion of the texture array with the indexes *xoffset* through *xoffset* + (*width* - 1).</span></span> <span data-ttu-id="d3a85-146">O destino na matriz de textura não pode incluir nenhum texels fora da matriz de textura especificada originalmente.</span><span class="sxs-lookup"><span data-stu-id="d3a85-146">The destination in the texture array cannot include any texels outside the originally specified texture array.</span></span>

<span data-ttu-id="d3a85-147">A função **glCopyTexSubImage1D** processa os pixels em uma linha da mesma maneira que [**glCopyPixels**](glcopypixels.md) , exceto que antes da conversão final dos pixels, todos os valores de componentes de pixel são clamped para o intervalo de \[ 0, 1 \] e convertidos para o formato interno da textura para armazenamento na matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="d3a85-147">The **glCopyTexSubImage1D** function processes the pixels in a row in the same way as [**glCopyPixels**](glcopypixels.md) except that before the final conversion of the pixels, all pixel component values are clamped to the range \[0,1\] and converted to the texture's internal format for storage in the texture array.</span></span> <span data-ttu-id="d3a85-148">A ordenação de pixels é determinada com coordenadas *x* inferiores correspondentes às coordenadas de textura inferiores.</span><span class="sxs-lookup"><span data-stu-id="d3a85-148">Pixel ordering is determined with lower *x* coordinates corresponding to lower texture coordinates.</span></span> <span data-ttu-id="d3a85-149">Se qualquer um dos pixels dentro de uma linha especificada da framebuffer atual estiver fora da janela associada ao contexto de renderização atual, seus valores serão indefinidos.</span><span class="sxs-lookup"><span data-stu-id="d3a85-149">If any of the pixels within a specified row of the current framebuffer are outside the window associated with the current rendering context, then their values are undefined.</span></span>

<span data-ttu-id="d3a85-150">Nenhuma alteração é feita no parâmetro *internalFormat*, *Width* ou *Border* da matriz de textura especificada ou para Texel valores fora da subimagem de textura especificada.</span><span class="sxs-lookup"><span data-stu-id="d3a85-150">No change is made to the *internalFormat*, *width*, or *border* parameter of the specified texture array or to texel values outside the specified texture sub-image.</span></span>

<span data-ttu-id="d3a85-151">Você não pode incluir chamadas para **glCopyTexSubImage1D** em listas de exibição.</span><span class="sxs-lookup"><span data-stu-id="d3a85-151">You cannot include calls to **glCopyTexSubImage1D** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="d3a85-152">A função **glCopyTexSubImage1D** só está disponível no OpenGL versão 1,1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="d3a85-152">The **glCopyTexSubImage1D** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="d3a85-153">Texturing não tem efeito no modo de índice de cor.</span><span class="sxs-lookup"><span data-stu-id="d3a85-153">Texturing has no effect in color-index mode.</span></span> <span data-ttu-id="d3a85-154">As funções [**glPixelStore**](glpixelstore-functions.md) e [**glPixelTransfer**](glpixeltransfer.md) afetam as imagens de textura exatamente como elas afetam a maneira como os pixels são desenhados usando [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="d3a85-154">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) functions affect texture images in exactly the way they affect the way pixels are drawn using [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="d3a85-155">As funções a seguir recuperam informações relacionadas ao **glCopyTexSubImage1D**:</span><span class="sxs-lookup"><span data-stu-id="d3a85-155">The following functions retrieve information related to **glCopyTexSubImage1D**:</span></span>

[<span data-ttu-id="d3a85-156">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="d3a85-156">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="d3a85-157">[**glIsEnabled**](glisenabled.md) com a textura do argumento GL \_ \_ 1D</span><span class="sxs-lookup"><span data-stu-id="d3a85-157">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_1D</span></span>

## <a name="requirements"></a><span data-ttu-id="d3a85-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3a85-158">Requirements</span></span>



| <span data-ttu-id="d3a85-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3a85-159">Requirement</span></span> | <span data-ttu-id="d3a85-160">Valor</span><span class="sxs-lookup"><span data-stu-id="d3a85-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3a85-161">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3a85-161">Minimum supported client</span></span><br/> | <span data-ttu-id="d3a85-162">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d3a85-162">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d3a85-163">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3a85-163">Minimum supported server</span></span><br/> | <span data-ttu-id="d3a85-164">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d3a85-164">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d3a85-165">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d3a85-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3a85-166"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3a85-166"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="d3a85-167">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d3a85-167">Library</span></span><br/>                  | <dl> <span data-ttu-id="d3a85-168"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3a85-168"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d3a85-169">DLL</span><span class="sxs-lookup"><span data-stu-id="d3a85-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3a85-170"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3a85-170"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3a85-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3a85-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3a85-172">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="d3a85-172">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="d3a85-173">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="d3a85-173">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="d3a85-174">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="d3a85-174">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="d3a85-175">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="d3a85-175">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="d3a85-176">**glFog**</span><span class="sxs-lookup"><span data-stu-id="d3a85-176">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="d3a85-177">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="d3a85-177">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="d3a85-178">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="d3a85-178">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="d3a85-179">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="d3a85-179">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="d3a85-180">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="d3a85-180">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="d3a85-181">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="d3a85-181">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="d3a85-182">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="d3a85-182">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="d3a85-183">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="d3a85-183">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="d3a85-184">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="d3a85-184">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="d3a85-185">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="d3a85-185">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





