---
title: função glBitmap (GL. h)
description: A função glBitmap desenha um bitmap.
ms.assetid: 3cd8e41b-016b-4610-833a-048b5e50ae7c
keywords:
- função glBitmap OpenGL
topic_type:
- apiref
api_name:
- glBitmap
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7aeb97bb16a1e3c4c29d1dfb1a5320c02f44404d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009474"
---
# <a name="glbitmap-function"></a><span data-ttu-id="acc5c-104">função glBitmap</span><span class="sxs-lookup"><span data-stu-id="acc5c-104">glBitmap function</span></span>

<span data-ttu-id="acc5c-105">A função **glBitmap** desenha um bitmap.</span><span class="sxs-lookup"><span data-stu-id="acc5c-105">The **glBitmap** function draws a bitmap.</span></span>

## <a name="syntax"></a><span data-ttu-id="acc5c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="acc5c-106">Syntax</span></span>


```C++
void WINAPI glBitmap(
         GLSizei width,
         GLSizei height,
         GLfloat xorig,
         GLfloat yorig,
         GLfloat xmove,
         GLfloat ymove,
   const GLubyte *bitmap
);
```



## <a name="parameters"></a><span data-ttu-id="acc5c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="acc5c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acc5c-108">*width*</span><span class="sxs-lookup"><span data-stu-id="acc5c-108">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="acc5c-109">A largura de pixel da imagem de bitmap.</span><span class="sxs-lookup"><span data-stu-id="acc5c-109">The pixel width of the bitmap image.</span></span>

</dd> <dt>

<span data-ttu-id="acc5c-110">*altura*</span><span class="sxs-lookup"><span data-stu-id="acc5c-110">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="acc5c-111">A altura de pixel da imagem de bitmap.</span><span class="sxs-lookup"><span data-stu-id="acc5c-111">The pixel height of the bitmap image.</span></span>

</dd> <dt>

<span data-ttu-id="acc5c-112">*xorig*</span><span class="sxs-lookup"><span data-stu-id="acc5c-112">*xorig*</span></span> 
</dt> <dd>

<span data-ttu-id="acc5c-113">O local *x* da origem na imagem de bitmap.</span><span class="sxs-lookup"><span data-stu-id="acc5c-113">The *x* location of the origin in the bitmap image.</span></span> <span data-ttu-id="acc5c-114">A origem é medida do canto inferior esquerdo do bitmap, com direções para a direita e para cima sendo os eixos positivos.</span><span class="sxs-lookup"><span data-stu-id="acc5c-114">The origin is measured from the lower-left corner of the bitmap, with right and up directions being the positive axes.</span></span>

</dd> <dt>

<span data-ttu-id="acc5c-115">*yorig*</span><span class="sxs-lookup"><span data-stu-id="acc5c-115">*yorig*</span></span> 
</dt> <dd>

<span data-ttu-id="acc5c-116">A localização *y* da origem na imagem de bitmap.</span><span class="sxs-lookup"><span data-stu-id="acc5c-116">The *y* location of the origin in the bitmap image.</span></span> <span data-ttu-id="acc5c-117">A origem é medida do canto inferior esquerdo do bitmap, com direções para a direita e para cima sendo os eixos positivos.</span><span class="sxs-lookup"><span data-stu-id="acc5c-117">The origin is measured from the lower-left corner of the bitmap, with right and up directions being the positive axes.</span></span>

</dd> <dt>

<span data-ttu-id="acc5c-118">*xmove*</span><span class="sxs-lookup"><span data-stu-id="acc5c-118">*xmove*</span></span> 
</dt> <dd>

<span data-ttu-id="acc5c-119">O deslocamento *x* a ser adicionado à posição de varredura atual após o bitmap ser desenhado.</span><span class="sxs-lookup"><span data-stu-id="acc5c-119">The *x* offset to be added to the current raster position after the bitmap is drawn.</span></span>

</dd> <dt>

<span data-ttu-id="acc5c-120">*ymove*</span><span class="sxs-lookup"><span data-stu-id="acc5c-120">*ymove*</span></span> 
</dt> <dd>

<span data-ttu-id="acc5c-121">O deslocamento *y* a ser adicionado à posição de varredura atual após o bitmap ser desenhado.</span><span class="sxs-lookup"><span data-stu-id="acc5c-121">The *y* offset to be added to the current raster position after the bitmap is drawn.</span></span>

</dd> <dt>

<span data-ttu-id="acc5c-122">*bitmap*</span><span class="sxs-lookup"><span data-stu-id="acc5c-122">*bitmap*</span></span> 
</dt> <dd>

<span data-ttu-id="acc5c-123">O endereço da imagem de bitmap.</span><span class="sxs-lookup"><span data-stu-id="acc5c-123">The address of the bitmap image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acc5c-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="acc5c-124">Return value</span></span>

<span data-ttu-id="acc5c-125">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="acc5c-125">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="acc5c-126">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="acc5c-126">Error codes</span></span>

<span data-ttu-id="acc5c-127">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="acc5c-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="acc5c-128">Nome</span><span class="sxs-lookup"><span data-stu-id="acc5c-128">Name</span></span>                                                                                                  | <span data-ttu-id="acc5c-129">Significado</span><span class="sxs-lookup"><span data-stu-id="acc5c-129">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="acc5c-130"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="acc5c-130"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="acc5c-131">a *largura* ou a *altura* é negativa.</span><span class="sxs-lookup"><span data-stu-id="acc5c-131">*width* or *height* is negative.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="acc5c-132"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="acc5c-132"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="acc5c-133">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="acc5c-133">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="acc5c-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="acc5c-134">Remarks</span></span>

<span data-ttu-id="acc5c-135">Um bitmap é uma imagem binária.</span><span class="sxs-lookup"><span data-stu-id="acc5c-135">A bitmap is a binary image.</span></span> <span data-ttu-id="acc5c-136">Quando desenhado, o bitmap é posicionado em relação à posição atual da rasterização e os pixels de framebuffer correspondentes ao 1s no bitmap são gravados usando a cor ou índice de rasterização atual.</span><span class="sxs-lookup"><span data-stu-id="acc5c-136">When drawn, the bitmap is positioned relative to the current raster position, and framebuffer pixels corresponding to 1s in the bitmap are written using the current raster color or index.</span></span> <span data-ttu-id="acc5c-137">Os pixels do buffer de quadros correspondentes a zeros no bitmap não são modificados.</span><span class="sxs-lookup"><span data-stu-id="acc5c-137">Frame-buffer pixels corresponding to zeros in the bitmap are not modified.</span></span>

<span data-ttu-id="acc5c-138">A imagem de bitmap é interpretada como dados de imagem para a função [**glDrawPixels**](gldrawpixels.md) , com *largura* e *altura* correspondentes aos argumentos de largura e altura dessa função, e com o *tipo* definido como bitmap GL \_ e o *formato* definido como o índice de \_ cores GL \_ .</span><span class="sxs-lookup"><span data-stu-id="acc5c-138">The bitmap image is interpreted like image data for the [**glDrawPixels**](gldrawpixels.md) function, with *width* and *height* corresponding to the width and height arguments of that function, and with *type* set to GL\_BITMAP and *format* set to GL\_COLOR\_INDEX.</span></span> <span data-ttu-id="acc5c-139">Os modos que você especifica usando [**glPixelStore**](glpixelstore-functions.md) afetam a interpretação de dados de imagem de bitmap; os modos que você especificar usando [**glPixelTransfer**](glpixeltransfer.md) não.</span><span class="sxs-lookup"><span data-stu-id="acc5c-139">Modes you specify using [**glPixelStore**](glpixelstore-functions.md) affect the interpretation of bitmap image data; modes you specify using [**glPixelTransfer**](glpixeltransfer.md) do not.</span></span>

<span data-ttu-id="acc5c-140">Se a posição atual da rasterização for inválida, **glBitmap** será ignorado.</span><span class="sxs-lookup"><span data-stu-id="acc5c-140">If the current raster position is invalid, **glBitmap** is ignored.</span></span> <span data-ttu-id="acc5c-141">Caso contrário, o canto inferior esquerdo da imagem de bitmap será posicionado nas seguintes coordenadas da janela:</span><span class="sxs-lookup"><span data-stu-id="acc5c-141">Otherwise, the lower-left corner of the bitmap image is positioned at the following window coordinates:</span></span>

<span data-ttu-id="acc5c-142">*x*<sub>w</sub>  =  *x*<sub>r</sub> *x*?</span><span class="sxs-lookup"><span data-stu-id="acc5c-142">*x*<sub>w</sub> = *x*<sub>r</sub> *x*?</span></span>

<span data-ttu-id="acc5c-143">*y*<sub>l</sub>  =  *y*<sub>r</sub> *y*?</span><span class="sxs-lookup"><span data-stu-id="acc5c-143">*y*<sub>w</sub> = *y*<sub>r</sub> *y*?</span></span>

<span data-ttu-id="acc5c-144">Nessas coordenadas, (*x*<sub>r</sub> , *y*<sub>r</sub> ) é a posição da rasterização e (*x*?</span><span class="sxs-lookup"><span data-stu-id="acc5c-144">In these coordinates, (*x*<sub>r</sub> , *y*<sub>r</sub> ) is the raster position, and (*x*?</span></span> <span data-ttu-id="acc5c-145">, *y*?</span><span class="sxs-lookup"><span data-stu-id="acc5c-145">, *y*?</span></span> <span data-ttu-id="acc5c-146">) é a origem do bitmap.</span><span class="sxs-lookup"><span data-stu-id="acc5c-146">) is the bitmap origin.</span></span> <span data-ttu-id="acc5c-147">Os fragmentos são então gerados para cada pixel correspondente a um 1 na imagem de bitmap.</span><span class="sxs-lookup"><span data-stu-id="acc5c-147">Fragments are then generated for each pixel corresponding to a 1 in the bitmap image.</span></span> <span data-ttu-id="acc5c-148">Esses fragmentos são gerados usando a coordenada *z* de rasterização atual, o índice de cor ou cor e as coordenadas de textura de rasterização atuais.</span><span class="sxs-lookup"><span data-stu-id="acc5c-148">These fragments are generated using the current raster *z*-coordinate, color or color index, and current raster texture coordinates.</span></span> <span data-ttu-id="acc5c-149">Eles são tratados como se tivessem sido gerados por um ponto, uma linha ou um polígono, incluindo o mapeamento de textura, fogging e todas as operações por fragmento, como os testes alfa e Depth.</span><span class="sxs-lookup"><span data-stu-id="acc5c-149">They are then treated just as if they had been generated by a point, line, or polygon, including texture mapping, fogging, and all per-fragment operations such as alpha and depth testing.</span></span>

<span data-ttu-id="acc5c-150">Depois que o bitmap tiver sido desenhado, as coordenadas *x* e *y* da posição de rasterização atual serão compensadas por *xmove* e *ymove*.</span><span class="sxs-lookup"><span data-stu-id="acc5c-150">After the bitmap has been drawn, the *x* and *y* coordinates of the current raster position are offset by *xmove* and *ymove*.</span></span> <span data-ttu-id="acc5c-151">Nenhuma alteração é feita na coordenada *z* da posição atual de rasterização ou nas coordenadas de cor de rasterização, índice ou textura atuais.</span><span class="sxs-lookup"><span data-stu-id="acc5c-151">No change is made to the *z*-coordinate of the current raster position, or to the current raster color, index, or texture coordinates.</span></span>

<span data-ttu-id="acc5c-152">As funções a seguir recuperam informações relacionadas à função **glBitmap** :</span><span class="sxs-lookup"><span data-stu-id="acc5c-152">The following functions retrieve information related to the **glBitmap** function:</span></span>

<span data-ttu-id="acc5c-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento \_ GL \_ posição de rasterização atual \_</span><span class="sxs-lookup"><span data-stu-id="acc5c-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION</span></span>

 

<span data-ttu-id="acc5c-154">**glGet** com o argumento \_ GL \_ cor de rasterização atual \_</span><span class="sxs-lookup"><span data-stu-id="acc5c-154">**glGet** with argument GL\_CURRENT\_RASTER\_COLOR</span></span>

 

<span data-ttu-id="acc5c-155"> \_ \_ índice de varredura atual glGet com Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="acc5c-155">**glGet** with argument GL\_CURRENT\_RASTER\_INDEX</span></span>

 

<span data-ttu-id="acc5c-156">**glGet** com Argument GL \_ \_ textura de rasterização atual \_ \_ CoOrds</span><span class="sxs-lookup"><span data-stu-id="acc5c-156">**glGet** with argument GL\_CURRENT\_RASTER\_TEXTURE\_COORDS</span></span>

 

<span data-ttu-id="acc5c-157">**glGet** com Argument GL \_ \_ posição de rasterização atual \_ \_ válida</span><span class="sxs-lookup"><span data-stu-id="acc5c-157">**glGet** with argument GL\_CURRENT\_RASTER\_POSITION\_VALID</span></span>

## <a name="requirements"></a><span data-ttu-id="acc5c-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="acc5c-158">Requirements</span></span>



| <span data-ttu-id="acc5c-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="acc5c-159">Requirement</span></span> | <span data-ttu-id="acc5c-160">Valor</span><span class="sxs-lookup"><span data-stu-id="acc5c-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="acc5c-161">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="acc5c-161">Minimum supported client</span></span><br/> | <span data-ttu-id="acc5c-162">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="acc5c-162">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="acc5c-163">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="acc5c-163">Minimum supported server</span></span><br/> | <span data-ttu-id="acc5c-164">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="acc5c-164">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="acc5c-165">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="acc5c-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="acc5c-166"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="acc5c-166"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="acc5c-167">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="acc5c-167">Library</span></span><br/>                  | <dl> <span data-ttu-id="acc5c-168"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="acc5c-168"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="acc5c-169">DLL</span><span class="sxs-lookup"><span data-stu-id="acc5c-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acc5c-170"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acc5c-170"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acc5c-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="acc5c-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acc5c-172">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="acc5c-172">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="acc5c-173">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="acc5c-173">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="acc5c-174">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="acc5c-174">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="acc5c-175">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="acc5c-175">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="acc5c-176">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="acc5c-176">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="acc5c-177">**glRasterPos**</span><span class="sxs-lookup"><span data-stu-id="acc5c-177">**glRasterPos**</span></span>](glrasterpos-functions.md)
</dt> </dl>

 

 





