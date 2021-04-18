---
title: função glGetTexImage (GL. h)
description: A função glGetTexImage retorna uma imagem de textura.
ms.assetid: d7235df4-2dd8-4537-aadd-284c130a3f99
keywords:
- função glGetTexImage OpenGL
topic_type:
- apiref
api_name:
- glGetTexImage
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da38ca1d6605fdc3cd6cf73cdd017404b71961e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753128"
---
# <a name="glgetteximage-function"></a><span data-ttu-id="55b4d-104">função glGetTexImage</span><span class="sxs-lookup"><span data-stu-id="55b4d-104">glGetTexImage function</span></span>

<span data-ttu-id="55b4d-105">A função **glGetTexImage** retorna uma imagem de textura.</span><span class="sxs-lookup"><span data-stu-id="55b4d-105">The **glGetTexImage** function returns a texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="55b4d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55b4d-106">Syntax</span></span>


```C++
void WINAPI glGetTexImage(
   GLenum target,
   GLint  level,
   GLenum format,
   GLenum type,
   GLvoid *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="55b4d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="55b4d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55b4d-108">*destino*</span><span class="sxs-lookup"><span data-stu-id="55b4d-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="55b4d-109">Especifica qual textura deve ser obtida.</span><span class="sxs-lookup"><span data-stu-id="55b4d-109">Specifies which texture is to be obtained.</span></span> <span data-ttu-id="55b4d-110">A textura GL \_ \_ 1D e GL de \_ textura \_ 2D são aceitas.</span><span class="sxs-lookup"><span data-stu-id="55b4d-110">GL\_TEXTURE\_1D and GL\_TEXTURE\_2D are accepted.</span></span>

</dd> <dt>

<span data-ttu-id="55b4d-111">*level*</span><span class="sxs-lookup"><span data-stu-id="55b4d-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="55b4d-112">O número de nível de detalhe da imagem desejada.</span><span class="sxs-lookup"><span data-stu-id="55b4d-112">The level-of-detail number of the desired image.</span></span> <span data-ttu-id="55b4d-113">Nível 0 é o nível de imagem base.</span><span class="sxs-lookup"><span data-stu-id="55b4d-113">Level 0 is the base image level.</span></span> <span data-ttu-id="55b4d-114">O nível *n* é a imagem de redução *n* º mipmap.</span><span class="sxs-lookup"><span data-stu-id="55b4d-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="55b4d-115">*format*</span><span class="sxs-lookup"><span data-stu-id="55b4d-115">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="55b4d-116">Um formato de pixel para os dados retornados.</span><span class="sxs-lookup"><span data-stu-id="55b4d-116">A pixel format for the returned data.</span></span> <span data-ttu-id="55b4d-117">Os formatos com suporte são GL \_ vermelho, GL \_ verde, GL \_ Blue, GL \_ alfa, GL \_ RGB, GL \_ RGBA, GL \_ luminescência, GL \_ BGR \_ ext, GL BGRA ext e a luminância de \_ \_ GL \_ \_ alfa.</span><span class="sxs-lookup"><span data-stu-id="55b4d-117">The supported formats are GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, GL\_RGB, GL\_RGBA, GL\_LUMINANCE, GL\_BGR\_EXT, GL\_BGRA\_EXT, and GL\_LUMINANCE\_ALPHA.</span></span>

</dd> <dt>

<span data-ttu-id="55b4d-118">*tipo*</span><span class="sxs-lookup"><span data-stu-id="55b4d-118">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="55b4d-119">Um tipo de pixel para os dados retornados.</span><span class="sxs-lookup"><span data-stu-id="55b4d-119">A pixel type for the returned data.</span></span> <span data-ttu-id="55b4d-120">Os tipos com suporte são GL \_ não assinado \_ , byte GL, GL \_ \_ não assinado \_ curto, GL \_ curto, GL \_ não assinado \_ int, GL \_ int e GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="55b4d-120">The supported types are GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="55b4d-121">*pixels*</span><span class="sxs-lookup"><span data-stu-id="55b4d-121">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="55b4d-122">Retorna a imagem de textura.</span><span class="sxs-lookup"><span data-stu-id="55b4d-122">Returns the texture image.</span></span> <span data-ttu-id="55b4d-123">Deve ser um ponteiro para uma matriz do tipo especificado por *tipo*.</span><span class="sxs-lookup"><span data-stu-id="55b4d-123">Should be a pointer to an array of the type specified by *type*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55b4d-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="55b4d-124">Return value</span></span>

<span data-ttu-id="55b4d-125">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="55b4d-125">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="55b4d-126">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="55b4d-126">Error codes</span></span>

<span data-ttu-id="55b4d-127">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="55b4d-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="55b4d-128">Nome</span><span class="sxs-lookup"><span data-stu-id="55b4d-128">Name</span></span>                                                                                                  | <span data-ttu-id="55b4d-129">Significado</span><span class="sxs-lookup"><span data-stu-id="55b4d-129">Meaning</span></span>                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="55b4d-130"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="55b4d-130"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="55b4d-131">o *destino*, o *formato* ou o *tipo* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="55b4d-131">*target*, *format*, or *type* was not an accepted value.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="55b4d-132"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="55b4d-132"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="55b4d-133">o *nível* é menor que zero ou maior que o *log* 2 (*Max*), em que *Max* é o valor retornado do \_ tamanho de textura Max GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="55b4d-133">*level* is less than zero or greater than *log* 2 (*max*), where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>      |
| <dl> <span data-ttu-id="55b4d-134"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="55b4d-134"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="55b4d-135">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md) .</span><span class="sxs-lookup"><span data-stu-id="55b4d-135">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md) .</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="55b4d-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="55b4d-136">Remarks</span></span>

<span data-ttu-id="55b4d-137">A função **glGetTexImage** retorna uma imagem de textura em *pixels*.</span><span class="sxs-lookup"><span data-stu-id="55b4d-137">The **glGetTexImage** function returns a texture image into *pixels*.</span></span> <span data-ttu-id="55b4d-138">O parâmetro de *destino* especifica se a imagem de textura desejada é uma especificada por [**glTexImage1D**](glteximage1d.md)**(** GL \_ Texture \_ 1D **)** ou por [**glTexImage2D**](glteximage2d.md)**(GL de** \_ textura \_ 2D **)**.</span><span class="sxs-lookup"><span data-stu-id="55b4d-138">The *target* parameter specifies whether the desired texture image is one specified by [**glTexImage1D**](glteximage1d.md)**(** GL\_TEXTURE\_1D **)** or by [**glTexImage2D**](glteximage2d.md)**(** GL\_TEXTURE\_2D **)**.</span></span> <span data-ttu-id="55b4d-139">O parâmetro *Level* especifica o número de nível de detalhe da imagem desejada.</span><span class="sxs-lookup"><span data-stu-id="55b4d-139">The *level* parameter specifies the level-of-detail number of the desired image.</span></span> <span data-ttu-id="55b4d-140">Os parâmetros *Format* e *Type* especificam o formato e o tipo da matriz de imagem desejada.</span><span class="sxs-lookup"><span data-stu-id="55b4d-140">The *format* and *type* parameters specify the format and type of the desired image array.</span></span> <span data-ttu-id="55b4d-141">Para obter uma descrição dos valores aceitáveis para os parâmetros de *formato* e *tipo* , respectivamente, consulte **glTexImage1D** e [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="55b4d-141">For a description of the acceptable values for the *format* and *type* parameters, respectively, see **glTexImage1D** and [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="55b4d-142">A operação de **glGetTexImage** é melhor compreendida considerando-se a imagem de textura de quatro componentes internos selecionada como um buffer de cores RGBA do tamanho da imagem.</span><span class="sxs-lookup"><span data-stu-id="55b4d-142">Operation of **glGetTexImage** is best understood by considering the selected internal four-component texture image to be an RGBA color buffer the size of the image.</span></span> <span data-ttu-id="55b4d-143">A semântica de **glGetTexImage** é, então, idêntica àquelas de [**glReadPixels**](glreadpixels.md) chamadas com o mesmo *formato* e *tipo*, *com x* e *y* definidos como zero, a *largura* é definida como a largura da imagem de textura (incluindo a borda, se uma tiver sido especificada) e a *altura* definida como uma para imagens de 1-d ou a altura da imagem de textura (incluindo a borda, se uma tiver sido especificada) para imagens 2D.</span><span class="sxs-lookup"><span data-stu-id="55b4d-143">The semantics of **glGetTexImage** are then identical to those of [**glReadPixels**](glreadpixels.md) called with the same *format* and *type*, with *x* and *y* set to zero, *width* set to the width of the texture image (including border if one was specified), and *height* set to one for 1-D images, or to the height of the texture image (including border, if one was specified) for 2-D images.</span></span>

<span data-ttu-id="55b4d-144">Como a imagem de textura interna é uma imagem RGBA, o índice de cores GL de formatos de pixel \_ \_ , o índice de \_ estêncil GL e o componente de \_ \_ profundidade GL \_ não são aceitos, e o bitmap do tipo pixel GL \_ não é aceito.</span><span class="sxs-lookup"><span data-stu-id="55b4d-144">Because the internal texture image is an RGBA image, pixel formats GL\_COLOR\_INDEX, GL\_STENCIL\_INDEX, and GL\_DEPTH\_COMPONENT are not accepted, and pixel type GL\_BITMAP is not accepted.</span></span>

<span data-ttu-id="55b4d-145">Se a imagem de textura selecionada não contiver quatro componentes, os mapeamentos a seguir serão aplicados.</span><span class="sxs-lookup"><span data-stu-id="55b4d-145">If the selected texture image does not contain four components, the following mappings are applied.</span></span> <span data-ttu-id="55b4d-146">As texturas de componente único são tratadas como buffers RGBA com vermelho definido como o valor de componente único, e verde, azul e alfa definidos como zero.</span><span class="sxs-lookup"><span data-stu-id="55b4d-146">Single-component textures are treated as RGBA buffers with red set to the single-component value, and green, blue, and alpha set to zero.</span></span>

<span data-ttu-id="55b4d-147">As texturas de dois componentes são tratadas como buffers RGBA, com vermelho definido como o valor do componente zero, alfa definido como o valor do componente um, e verde e azul definidos como zero.</span><span class="sxs-lookup"><span data-stu-id="55b4d-147">Two-component textures are treated as RGBA buffers, with red set to the value of component zero, alpha set to the value of component one, and green and blue set to zero.</span></span> <span data-ttu-id="55b4d-148">Por fim, as texturas de três componentes são tratadas como buffers RGBA com vermelho definido como componente zero, verde definido como componente um, azul definido como componente dois e alfa definido como zero.</span><span class="sxs-lookup"><span data-stu-id="55b4d-148">Finally, three-component textures are treated as RGBA buffers with red set to component zero, green set to component one, blue set to component two, and alpha set to zero.</span></span>

<span data-ttu-id="55b4d-149">Para determinar o tamanho necessário de *pixels*, use [**glGetTexLevelParameter**](glgettexlevelparameter.md) para verificar as dimensões da imagem de textura interna e, em seguida, dimensione o número necessário de pixels pelo armazenamento necessário para cada pixel, com base no *formato* e no *tipo*.</span><span class="sxs-lookup"><span data-stu-id="55b4d-149">To determine the required size of *pixels*, use [**glGetTexLevelParameter**](glgettexlevelparameter.md) to ascertain the dimensions of the internal texture image, and then scale the required number of pixels by the storage required for each pixel, based on *format* and *type*.</span></span> <span data-ttu-id="55b4d-150">Certifique-se de levar os parâmetros de armazenamento de pixel em conta, especialmente o \_ alinhamento do pacote GL \_ .</span><span class="sxs-lookup"><span data-stu-id="55b4d-150">Be sure to take the pixel-storage parameters into account, especially GL\_PACK\_ALIGNMENT.</span></span>

<span data-ttu-id="55b4d-151">Se um erro for gerado, nenhuma alteração será feita no conteúdo de *pixels*.</span><span class="sxs-lookup"><span data-stu-id="55b4d-151">If an error is generated, no change is made to the contents of *pixels*.</span></span>

<span data-ttu-id="55b4d-152">As funções a seguir recuperam informações relacionadas ao **glGetTexImage**:</span><span class="sxs-lookup"><span data-stu-id="55b4d-152">The following functions retrieve information related to **glGetTexImage**:</span></span>

<span data-ttu-id="55b4d-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com \_ alinhamento de pacote do Argument GL \_ e outros</span><span class="sxs-lookup"><span data-stu-id="55b4d-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PACK\_ALIGNMENT and others</span></span>

<span data-ttu-id="55b4d-154">[**glGetTexLevelParameter**](glgettexlevelparameter.md) com largura de textura do argumento GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="55b4d-154">[**glGetTexLevelParameter**](glgettexlevelparameter.md) with argument GL\_TEXTURE\_WIDTH</span></span>

<span data-ttu-id="55b4d-155">**glGetTexLevelParameter** com altura de textura do argumento GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="55b4d-155">**glGetTexLevelParameter** with argument GL\_TEXTURE\_HEIGHT</span></span>

<span data-ttu-id="55b4d-156">**glGetTexLevelParameter** com borda de \_ textura Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="55b4d-156">**glGetTexLevelParameter** with argument GL\_TEXTURE\_BORDER</span></span>

<span data-ttu-id="55b4d-157">**glGetTexLevelParameter** com componentes de \_ textura Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="55b4d-157">**glGetTexLevelParameter** with argument GL\_TEXTURE\_COMPONENTS</span></span>

## <a name="requirements"></a><span data-ttu-id="55b4d-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55b4d-158">Requirements</span></span>



| <span data-ttu-id="55b4d-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="55b4d-159">Requirement</span></span> | <span data-ttu-id="55b4d-160">Valor</span><span class="sxs-lookup"><span data-stu-id="55b4d-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55b4d-161">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55b4d-161">Minimum supported client</span></span><br/> | <span data-ttu-id="55b4d-162">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="55b4d-162">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="55b4d-163">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55b4d-163">Minimum supported server</span></span><br/> | <span data-ttu-id="55b4d-164">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="55b4d-164">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="55b4d-165">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="55b4d-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="55b4d-166"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="55b4d-166"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="55b4d-167">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="55b4d-167">Library</span></span><br/>                  | <dl> <span data-ttu-id="55b4d-168"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55b4d-168"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="55b4d-169">DLL</span><span class="sxs-lookup"><span data-stu-id="55b4d-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55b4d-170"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55b4d-170"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55b4d-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="55b4d-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55b4d-172">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="55b4d-172">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="55b4d-173">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="55b4d-173">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="55b4d-174">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="55b4d-174">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="55b4d-175">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="55b4d-175">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
</dt> <dt>

[<span data-ttu-id="55b4d-176">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="55b4d-176">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="55b4d-177">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="55b4d-177">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="55b4d-178">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="55b4d-178">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





