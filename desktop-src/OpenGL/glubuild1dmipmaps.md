---
title: função gluBuild1DMipmaps (Glu. h)
description: A função gluBuild1DMipmaps cria mipmaps de 1 a D.
ms.assetid: 52ed924f-7a72-4458-b1b8-8e5d3021f60a
keywords:
- função gluBuild1DMipmaps OpenGL
topic_type:
- apiref
api_name:
- gluBuild1DMipmaps
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 089357488c7eae18e26258018473e9008fb29d24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754309"
---
# <a name="glubuild1dmipmaps-function"></a><span data-ttu-id="15888-104">função gluBuild1DMipmaps</span><span class="sxs-lookup"><span data-stu-id="15888-104">gluBuild1DMipmaps function</span></span>

<span data-ttu-id="15888-105">A função **gluBuild1DMipmaps** cria mipmaps de 1 a D.</span><span class="sxs-lookup"><span data-stu-id="15888-105">The **gluBuild1DMipmaps** function creates 1-D mipmaps.</span></span>

## <a name="syntax"></a><span data-ttu-id="15888-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15888-106">Syntax</span></span>


```C++
void WINAPI gluBuild1DMipmaps(
         GLenum target,
         GLint  components,
         GLint  width,
         GLenum format,
         GLenum type,
   const void   *data
);
```



## <a name="parameters"></a><span data-ttu-id="15888-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15888-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15888-108">*destino*</span><span class="sxs-lookup"><span data-stu-id="15888-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="15888-109">A textura de destino.</span><span class="sxs-lookup"><span data-stu-id="15888-109">The target texture.</span></span> <span data-ttu-id="15888-110">Deve ser GL \_ Texture \_ 1D.</span><span class="sxs-lookup"><span data-stu-id="15888-110">Must be GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="15888-111">*QC*</span><span class="sxs-lookup"><span data-stu-id="15888-111">*components*</span></span> 
</dt> <dd>

<span data-ttu-id="15888-112">O número de componentes de cor na textura.</span><span class="sxs-lookup"><span data-stu-id="15888-112">The number of color components in the texture.</span></span> <span data-ttu-id="15888-113">Deve ser 1, 2, 3 ou 4.</span><span class="sxs-lookup"><span data-stu-id="15888-113">Must be 1, 2, 3, or 4.</span></span>

</dd> <dt>

<span data-ttu-id="15888-114">*width*</span><span class="sxs-lookup"><span data-stu-id="15888-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="15888-115">A largura da imagem de textura.</span><span class="sxs-lookup"><span data-stu-id="15888-115">The width of the texture image.</span></span>

</dd> <dt>

<span data-ttu-id="15888-116">*format*</span><span class="sxs-lookup"><span data-stu-id="15888-116">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="15888-117">O formato dos dados de pixel.</span><span class="sxs-lookup"><span data-stu-id="15888-117">The format of the pixel data.</span></span> <span data-ttu-id="15888-118">Os seguintes valores são válidos: o \_ \_ índice de cores GL, GL \_ vermelho, GL \_ verde, GL \_ Blue, GL \_ alfa, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ luminescência ou o GL \_ luminância \_ alfa.</span><span class="sxs-lookup"><span data-stu-id="15888-118">The following values are valid: GL\_COLOR\_INDEX, GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, GL\_RGB, GL\_RGBA, GL\_BGR\_EXT, GL\_BGRA\_EXT, GL\_LUMINANCE, or GL\_LUMINANCE\_ALPHA.</span></span>

</dd> <dt>

<span data-ttu-id="15888-119">*tipo*</span><span class="sxs-lookup"><span data-stu-id="15888-119">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="15888-120">O tipo de dados para *dados*.</span><span class="sxs-lookup"><span data-stu-id="15888-120">The data type for *data*.</span></span> <span data-ttu-id="15888-121">Os seguintes valores são válidos: GL \_ não assinado \_ , byte, GL byte, renome do GL \_ \_ , GL \_ não assinado \_ curto, GL \_ curto, GL \_ não assinado \_ int, GL \_ int ou GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="15888-121">The following values are valid: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, or GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="15888-122">*data*</span><span class="sxs-lookup"><span data-stu-id="15888-122">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="15888-123">Um ponteiro para os dados da imagem na memória.</span><span class="sxs-lookup"><span data-stu-id="15888-123">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15888-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="15888-124">Return value</span></span>

<span data-ttu-id="15888-125">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="15888-125">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="15888-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="15888-126">Remarks</span></span>

<span data-ttu-id="15888-127">A função **gluBuild1DMipmaps** Obtém a imagem de entrada e gera todas as imagens do mipmap (usando [**gluScaleImage**](gluscaleimage.md)) para que a imagem de entrada possa ser usada como uma imagem de textura mipmapped.</span><span class="sxs-lookup"><span data-stu-id="15888-127">The **gluBuild1DMipmaps** function obtains the input image and generates all mipmap images (using [**gluScaleImage**](gluscaleimage.md)) so that the input image can be used as a mipmapped texture image.</span></span> <span data-ttu-id="15888-128">Em seguida, a função [**glTexImage1D**](glteximage1d.md) é chamada para carregar cada uma das imagens.</span><span class="sxs-lookup"><span data-stu-id="15888-128">The [**glTexImage1D**](glteximage1d.md) function is then called to load each of the images.</span></span> <span data-ttu-id="15888-129">Se a largura da imagem de entrada não for uma potência de dois, a imagem será dimensionada para a potência mais próxima de dois antes de a mipmaps ser gerada.</span><span class="sxs-lookup"><span data-stu-id="15888-129">If the width of the input image is not a power of two, then the image is scaled to the nearest power of two before the mipmaps are generated.</span></span>

<span data-ttu-id="15888-130">Um valor de retorno igual A zero indica êxito.</span><span class="sxs-lookup"><span data-stu-id="15888-130">A return value of zero indicates success.</span></span> <span data-ttu-id="15888-131">Caso contrário, um código de erro GLU será retornado (consulte [**gluErrorString**](gluerrorstring.md)).</span><span class="sxs-lookup"><span data-stu-id="15888-131">Otherwise, a GLU error code is returned (see [**gluErrorString**](gluerrorstring.md)).</span></span>

<span data-ttu-id="15888-132">Para obter uma descrição dos valores aceitáveis para o parâmetro *Format* , consulte **glTexImage1D**.</span><span class="sxs-lookup"><span data-stu-id="15888-132">For a description of the acceptable values for the *format* parameter, see **glTexImage1D**.</span></span> <span data-ttu-id="15888-133">Para obter uma descrição dos valores aceitáveis para o parâmetro de *tipo* , consulte [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="15888-133">For a description of the acceptable values for the *type* parameter, see [**glDrawPixels**](gldrawpixels.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="15888-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15888-134">Requirements</span></span>



| <span data-ttu-id="15888-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="15888-135">Requirement</span></span> | <span data-ttu-id="15888-136">Valor</span><span class="sxs-lookup"><span data-stu-id="15888-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="15888-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15888-137">Minimum supported client</span></span><br/> | <span data-ttu-id="15888-138">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="15888-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="15888-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15888-139">Minimum supported server</span></span><br/> | <span data-ttu-id="15888-140">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="15888-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="15888-141">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="15888-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="15888-142"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="15888-142"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="15888-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="15888-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="15888-144"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15888-144"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="15888-145">DLL</span><span class="sxs-lookup"><span data-stu-id="15888-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15888-146"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15888-146"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15888-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="15888-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15888-148">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="15888-148">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="15888-149">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="15888-149">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="15888-150">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="15888-150">**gluBuild2DMipmaps**</span></span>](glubuild2dmipmaps.md)
</dt> <dt>

[<span data-ttu-id="15888-151">**gluScaleImage**</span><span class="sxs-lookup"><span data-stu-id="15888-151">**gluScaleImage**</span></span>](gluscaleimage.md)
</dt> </dl>

 

 





