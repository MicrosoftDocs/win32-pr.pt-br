---
title: função gluBuild2DMipmaps (Glu. h)
description: A função gluBuild2DMipmaps cria mipmaps 2-D.
ms.assetid: ea19a9b0-baf7-436f-afd5-609bc364b3ba
keywords:
- função gluBuild2DMipmaps OpenGL
topic_type:
- apiref
api_name:
- gluBuild2DMipmaps
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92402792e41701711e99f469ead67410d6a8c1b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918150"
---
# <a name="glubuild2dmipmaps-function"></a><span data-ttu-id="9e011-104">função gluBuild2DMipmaps</span><span class="sxs-lookup"><span data-stu-id="9e011-104">gluBuild2DMipmaps function</span></span>

<span data-ttu-id="9e011-105">A função **gluBuild2DMipmaps** cria mipmaps 2-D.</span><span class="sxs-lookup"><span data-stu-id="9e011-105">The **gluBuild2DMipmaps** function creates 2-D mipmaps.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e011-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e011-106">Syntax</span></span>


```C++
void WINAPI gluBuild2DMipmaps(
         GLenum target,
         GLint  components,
         GLint  width,
         GLInt  height,
         GLenum format,
         GLenum type,
   const void   *data
);
```



## <a name="parameters"></a><span data-ttu-id="9e011-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e011-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e011-108">*destino*</span><span class="sxs-lookup"><span data-stu-id="9e011-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="9e011-109">A textura de destino.</span><span class="sxs-lookup"><span data-stu-id="9e011-109">The target texture.</span></span> <span data-ttu-id="9e011-110">Deve ser GL de \_ textura \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="9e011-110">Must be GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="9e011-111">*QC*</span><span class="sxs-lookup"><span data-stu-id="9e011-111">*components*</span></span> 
</dt> <dd>

<span data-ttu-id="9e011-112">O número de componentes de cor na textura.</span><span class="sxs-lookup"><span data-stu-id="9e011-112">The number of color components in the texture.</span></span> <span data-ttu-id="9e011-113">Deve ser 1, 2, 3 ou 4.</span><span class="sxs-lookup"><span data-stu-id="9e011-113">Must be 1, 2, 3, or 4.</span></span>

</dd> <dt>

<span data-ttu-id="9e011-114">*width*</span><span class="sxs-lookup"><span data-stu-id="9e011-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="9e011-115">A largura da imagem de textura.</span><span class="sxs-lookup"><span data-stu-id="9e011-115">The width of the texture image.</span></span>

</dd> <dt>

<span data-ttu-id="9e011-116">*altura*</span><span class="sxs-lookup"><span data-stu-id="9e011-116">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="9e011-117">A altura da imagem de textura.</span><span class="sxs-lookup"><span data-stu-id="9e011-117">The height of the texture image.</span></span>

</dd> <dt>

<span data-ttu-id="9e011-118">*format*</span><span class="sxs-lookup"><span data-stu-id="9e011-118">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="9e011-119">O formato dos dados de pixel.</span><span class="sxs-lookup"><span data-stu-id="9e011-119">The format of the pixel data.</span></span> <span data-ttu-id="9e011-120">Deve ser um dos seguintes: \_ \_ índice de cores GL, GL \_ vermelho, GL \_ verde, GL \_ Blue, GL \_ alfa, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ luminescência ou GL de \_ luminância \_ alfa.</span><span class="sxs-lookup"><span data-stu-id="9e011-120">Must be one of the following: GL\_COLOR\_INDEX, GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, GL\_RGB, GL\_RGBA, GL\_BGR\_EXT, GL\_BGRA\_EXT, GL\_LUMINANCE, or GL\_LUMINANCE\_ALPHA.</span></span>

</dd> <dt>

<span data-ttu-id="9e011-121">*tipo*</span><span class="sxs-lookup"><span data-stu-id="9e011-121">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="9e011-122">O tipo de dados para *dados*.</span><span class="sxs-lookup"><span data-stu-id="9e011-122">The data type for *data*.</span></span> <span data-ttu-id="9e011-123">Deve ser um dos seguintes: GL \_ não assinado \_ byte, GL \_ byte, \_ bitmap GL, GL \_ não assinado \_ curto, GL \_ curto, GL \_ não assinado \_ int, GL \_ int ou GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="9e011-123">Must be one of the following: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, or GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="9e011-124">*data*</span><span class="sxs-lookup"><span data-stu-id="9e011-124">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="9e011-125">Um ponteiro para os dados da imagem na memória.</span><span class="sxs-lookup"><span data-stu-id="9e011-125">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e011-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9e011-126">Return value</span></span>

<span data-ttu-id="9e011-127">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9e011-127">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e011-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e011-128">Remarks</span></span>

<span data-ttu-id="9e011-129">A função **gluBuild2DMipmaps** Obtém a imagem de entrada e gera todas as imagens do mipmap (usando [**gluScaleImage**](gluscaleimage.md)) para que a imagem de entrada possa ser usada como uma imagem de textura mipmapped.</span><span class="sxs-lookup"><span data-stu-id="9e011-129">The **gluBuild2DMipmaps** function obtains the input image and generates all mipmap images (using [**gluScaleImage**](gluscaleimage.md)) so the input image can be used as a mipmapped texture image.</span></span> <span data-ttu-id="9e011-130">Para carregar cada uma das imagens, chame [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="9e011-130">To load each of the images, call [**glTexImage2D**](glteximage2d.md).</span></span> <span data-ttu-id="9e011-131">Se as dimensões da imagem de entrada não forem potências de dois, a imagem será dimensionada de forma que a largura e a altura sejam potências de dois antes de os mipmaps serem gerados.</span><span class="sxs-lookup"><span data-stu-id="9e011-131">If the dimensions of the input image are not powers of two, then the image is scaled so that both the width and height are powers of two before the mipmaps are generated.</span></span>

<span data-ttu-id="9e011-132">Um valor de retorno igual A zero indica êxito.</span><span class="sxs-lookup"><span data-stu-id="9e011-132">A return value of zero indicates success.</span></span> <span data-ttu-id="9e011-133">Caso contrário, um código de erro GLU será retornado (consulte [**gluErrorString**](gluerrorstring.md)).</span><span class="sxs-lookup"><span data-stu-id="9e011-133">Otherwise, a GLU error code is returned (see [**gluErrorString**](gluerrorstring.md)).</span></span>

<span data-ttu-id="9e011-134">Para obter uma descrição dos valores aceitáveis para o parâmetro *Format* , consulte **glTexImage2D**.</span><span class="sxs-lookup"><span data-stu-id="9e011-134">For a description of the acceptable values for the *format* parameter, see **glTexImage2D**.</span></span> <span data-ttu-id="9e011-135">Para obter uma descrição dos valores aceitáveis para o *tipo*, consulte [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="9e011-135">For a description of the acceptable values for *type*, see [**glDrawPixels**](gldrawpixels.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e011-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e011-136">Requirements</span></span>



| <span data-ttu-id="9e011-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e011-137">Requirement</span></span> | <span data-ttu-id="9e011-138">Valor</span><span class="sxs-lookup"><span data-stu-id="9e011-138">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9e011-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e011-139">Minimum supported client</span></span><br/> | <span data-ttu-id="9e011-140">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9e011-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9e011-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e011-141">Minimum supported server</span></span><br/> | <span data-ttu-id="9e011-142">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9e011-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9e011-143">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9e011-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e011-144"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e011-144"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="9e011-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9e011-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="9e011-146"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e011-146"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9e011-147">DLL</span><span class="sxs-lookup"><span data-stu-id="9e011-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e011-148"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e011-148"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e011-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e011-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e011-150">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="9e011-150">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="9e011-151">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="9e011-151">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="9e011-152">**gluBuild1DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="9e011-152">**gluBuild1DMipmaps**</span></span>](glubuild1dmipmaps.md)
</dt> <dt>

[<span data-ttu-id="9e011-153">**gluScaleImage**</span><span class="sxs-lookup"><span data-stu-id="9e011-153">**gluScaleImage**</span></span>](gluscaleimage.md)
</dt> </dl>

 

 





