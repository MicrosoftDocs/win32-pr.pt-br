---
title: função gluScaleImage (Glu. h)
description: A função gluScaleImage dimensiona uma imagem para um tamanho arbitrário.
ms.assetid: f47191e8-b22d-4f6a-949a-9c7782d6d338
keywords:
- função gluScaleImage OpenGL
topic_type:
- apiref
api_name:
- gluScaleImage
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da95f1545996a83adeb27deaceb7fab6290005e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369205"
---
# <a name="gluscaleimage-function"></a><span data-ttu-id="7d2e5-104">função gluScaleImage</span><span class="sxs-lookup"><span data-stu-id="7d2e5-104">gluScaleImage function</span></span>

<span data-ttu-id="7d2e5-105">A função **gluScaleImage** dimensiona uma imagem para um tamanho arbitrário.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-105">The **gluScaleImage** function scales an image to an arbitrary size.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d2e5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7d2e5-106">Syntax</span></span>


```C++
int WINAPI gluScaleImage(
         GLenum format,
         GLint  widthin,
         GLint  heightin,
         GLenum typein,
   const void   *datain,
         GLint  widthout,
         GLint  heightout,
         GLenum typeout,
         void   *dataout
);
```



## <a name="parameters"></a><span data-ttu-id="7d2e5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7d2e5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d2e5-108">*format*</span><span class="sxs-lookup"><span data-stu-id="7d2e5-108">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="7d2e5-109">O formato dos dados de pixel.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-109">The format of the pixel data.</span></span> <span data-ttu-id="7d2e5-110">Os seguintes valores simbólicos são válidos: \_ \_ índice de cores GL \_ , \_ índice de estêncil GL, \_ componente de profundidade do GL \_ , GL \_ vermelho, GL \_ verde, GL \_ azul, GL \_ alfa, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ luminescência e a luminância de GL \_ \_ alfa.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-110">The following symbolic values are valid: GL\_COLOR\_INDEX, GL\_STENCIL\_INDEX, GL\_DEPTH\_COMPONENT, GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, GL\_RGB, GL\_RGBA, GL\_BGR\_EXT, GL\_BGRA\_EXT, GL\_LUMINANCE, and GL\_LUMINANCE\_ALPHA.</span></span>

</dd> <dt>

<span data-ttu-id="7d2e5-111">*largura*</span><span class="sxs-lookup"><span data-stu-id="7d2e5-111">*widthin*</span></span> 
</dt> <dd>

<span data-ttu-id="7d2e5-112">A largura da imagem de origem dimensionada.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-112">The width of the source image that is scaled.</span></span>

</dd> <dt>

<span data-ttu-id="7d2e5-113">*altura*</span><span class="sxs-lookup"><span data-stu-id="7d2e5-113">*heightin*</span></span> 
</dt> <dd>

<span data-ttu-id="7d2e5-114">A altura da imagem de origem dimensionada.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-114">The height of the source image that is scaled.</span></span>

</dd> <dt>

<span data-ttu-id="7d2e5-115">*tipo*</span><span class="sxs-lookup"><span data-stu-id="7d2e5-115">*typein*</span></span> 
</dt> <dd>

<span data-ttu-id="7d2e5-116">O tipo de dados para *dados*.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-116">The data type for *datain*.</span></span> <span data-ttu-id="7d2e5-117">Deve ser um dos seguintes: GL \_ não assinado \_ byte, GL \_ byte, \_ bitmap GL, GL \_ não assinado \_ curto, GL \_ curto, GL \_ não assinado \_ int, GL \_ int ou GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-117">Must be one of the following: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, or GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="7d2e5-118">*dados de*</span><span class="sxs-lookup"><span data-stu-id="7d2e5-118">*datain*</span></span> 
</dt> <dd>

<span data-ttu-id="7d2e5-119">Um ponteiro para a imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-119">A pointer to the source image.</span></span>

</dd> <dt>

<span data-ttu-id="7d2e5-120">*largura*</span><span class="sxs-lookup"><span data-stu-id="7d2e5-120">*widthout*</span></span> 
</dt> <dd>

<span data-ttu-id="7d2e5-121">A largura da imagem de destino.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-121">The width of the destination image.</span></span>

</dd> <dt>

<span data-ttu-id="7d2e5-122">*altura de*</span><span class="sxs-lookup"><span data-stu-id="7d2e5-122">*heightout*</span></span> 
</dt> <dd>

<span data-ttu-id="7d2e5-123">A altura da imagem de destino.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-123">The height of the destination image.</span></span>

</dd> <dt>

<span data-ttu-id="7d2e5-124">*tipoout*</span><span class="sxs-lookup"><span data-stu-id="7d2e5-124">*typeout*</span></span> 
</dt> <dd>

<span data-ttu-id="7d2e5-125">O tipo de dados para *dataout*.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-125">The data type for *dataout*.</span></span> <span data-ttu-id="7d2e5-126">Deve ser um dos seguintes: GL \_ não assinado \_ byte, GL \_ byte, \_ bitmap GL, GL \_ não assinado \_ curto, GL \_ curto, GL \_ não assinado \_ int, GL \_ int ou GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-126">Must be one of the following: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, or GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="7d2e5-127">*Data de*</span><span class="sxs-lookup"><span data-stu-id="7d2e5-127">*dataout*</span></span> 
</dt> <dd>

<span data-ttu-id="7d2e5-128">Um ponteiro para a imagem de destino.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-128">A pointer to the destination image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d2e5-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7d2e5-129">Return value</span></span>

<span data-ttu-id="7d2e5-130">Se a função obtiver êxito, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-130">If the function succeeds, the return value is zero.</span></span>

<span data-ttu-id="7d2e5-131">Se a função falhar, o valor de retorno será um código de erro GLU (consulte [**gluErrorString**](gluerrorstring.md)).</span><span class="sxs-lookup"><span data-stu-id="7d2e5-131">If the function fails, the return value is a GLU error code (see [**gluErrorString**](gluerrorstring.md)).</span></span>

## <a name="remarks"></a><span data-ttu-id="7d2e5-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d2e5-132">Remarks</span></span>

<span data-ttu-id="7d2e5-133">A função **gluScaleImage** dimensiona uma imagem de pixel usando os modos de armazenamento de pixel apropriados para desempacotar dados da imagem de origem e os dados de pacote na imagem de destino.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-133">The **gluScaleImage** function scales a pixel image using the appropriate pixel store modes to unpack data from the source image and pack data into the destination image.</span></span>

<span data-ttu-id="7d2e5-134">Ao reduzir uma imagem, o **gluScaleImage** usa um filtro de caixa para exemplificar a imagem de origem e criar pixels para a imagem de destino.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-134">When shrinking an image, **gluScaleImage** uses a box filter to sample the source image and create pixels for the destination image.</span></span> <span data-ttu-id="7d2e5-135">Ao ampliar uma imagem, os pixels da imagem de origem são interpolados linearmente para criar a imagem de destino.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-135">When magnifying an image, the pixels from the source image are linearly interpolated to create the destination image.</span></span>

<span data-ttu-id="7d2e5-136">Para obter uma descrição dos valores aceitáveis para o *formato*, *digite* e parâmetros de *tipoout* , consulte [**glReadPixels**](glreadpixels.md).</span><span class="sxs-lookup"><span data-stu-id="7d2e5-136">For a description of the acceptable values for the *format*, *typein*, and *typeout* parameters, see [**glReadPixels**](glreadpixels.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7d2e5-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d2e5-137">Requirements</span></span>



| <span data-ttu-id="7d2e5-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d2e5-138">Requirement</span></span> | <span data-ttu-id="7d2e5-139">Valor</span><span class="sxs-lookup"><span data-stu-id="7d2e5-139">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7d2e5-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d2e5-140">Minimum supported client</span></span><br/> | <span data-ttu-id="7d2e5-141">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7d2e5-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7d2e5-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d2e5-142">Minimum supported server</span></span><br/> | <span data-ttu-id="7d2e5-143">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7d2e5-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7d2e5-144">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7d2e5-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d2e5-145"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d2e5-145"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="7d2e5-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7d2e5-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="7d2e5-147"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d2e5-147"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7d2e5-148">DLL</span><span class="sxs-lookup"><span data-stu-id="7d2e5-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d2e5-149"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d2e5-149"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d2e5-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d2e5-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d2e5-151">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="7d2e5-151">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="7d2e5-152">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="7d2e5-152">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="7d2e5-153">**gluBuild1DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="7d2e5-153">**gluBuild1DMipmaps**</span></span>](glubuild1dmipmaps.md)
</dt> <dt>

[<span data-ttu-id="7d2e5-154">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="7d2e5-154">**gluBuild2DMipmaps**</span></span>](glubuild2dmipmaps.md)
</dt> <dt>

[<span data-ttu-id="7d2e5-155">**gluErrorString**</span><span class="sxs-lookup"><span data-stu-id="7d2e5-155">**gluErrorString**</span></span>](gluerrorstring.md)
</dt> </dl>

 

 





