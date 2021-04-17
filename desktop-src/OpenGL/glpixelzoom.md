---
title: função glPixelZoom (GL. h)
description: A função glPixelZoom especifica os fatores de zoom de pixel.
ms.assetid: 57ead7d8-0502-46b4-9f66-dbb3cb75b0f9
keywords:
- função glPixelZoom OpenGL
topic_type:
- apiref
api_name:
- glPixelZoom
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 065e1735ca0228046cfb08e2fb441d3cdc02af74
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105755575"
---
# <a name="glpixelzoom-function"></a><span data-ttu-id="ffdeb-104">função glPixelZoom</span><span class="sxs-lookup"><span data-stu-id="ffdeb-104">glPixelZoom function</span></span>

<span data-ttu-id="ffdeb-105">A função **glPixelZoom** especifica os fatores de zoom de pixel.</span><span class="sxs-lookup"><span data-stu-id="ffdeb-105">The **glPixelZoom** function specifies the pixel zoom factors.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffdeb-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ffdeb-106">Syntax</span></span>


```C++
void WINAPI glPixelZoom(
   GLfloat xfactor,
   GLfloat yfactor
);
```



## <a name="parameters"></a><span data-ttu-id="ffdeb-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ffdeb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffdeb-108">*xfactor*</span><span class="sxs-lookup"><span data-stu-id="ffdeb-108">*xfactor*</span></span> 
</dt> <dd>

<span data-ttu-id="ffdeb-109">O fator de zoom *x* para operações de gravação de pixel.</span><span class="sxs-lookup"><span data-stu-id="ffdeb-109">The *x* zoom factor for pixel write operations.</span></span>

</dd> <dt>

<span data-ttu-id="ffdeb-110">*yfactor*</span><span class="sxs-lookup"><span data-stu-id="ffdeb-110">*yfactor*</span></span> 
</dt> <dd>

<span data-ttu-id="ffdeb-111">O fator de zoom *y* para operações de gravação de pixel.</span><span class="sxs-lookup"><span data-stu-id="ffdeb-111">The *y* zoom factor for pixel write operations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffdeb-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ffdeb-112">Return value</span></span>

<span data-ttu-id="ffdeb-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ffdeb-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ffdeb-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="ffdeb-114">Error codes</span></span>

<span data-ttu-id="ffdeb-115">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="ffdeb-115">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ffdeb-116">Nome</span><span class="sxs-lookup"><span data-stu-id="ffdeb-116">Name</span></span>                                                                                                  | <span data-ttu-id="ffdeb-117">Significado</span><span class="sxs-lookup"><span data-stu-id="ffdeb-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ffdeb-118"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ffdeb-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="ffdeb-119">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="ffdeb-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ffdeb-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="ffdeb-120">Remarks</span></span>

<span data-ttu-id="ffdeb-121">A função **glPixelZoom** especifica valores para os fatores de zoom *x* e *y* .</span><span class="sxs-lookup"><span data-stu-id="ffdeb-121">The **glPixelZoom** function specifies values for the *x* and *y* zoom factors.</span></span> <span data-ttu-id="ffdeb-122">Durante a execução de [**glDrawPixels**](gldrawpixels.md) ou [**glCopyPixels**](glcopypixels.md), if (*x*<sub>r</sub> ,*y*<sub>r</sub> ) é a posição atual da varredura e um determinado elemento está na coluna *n* th e *m* th do retângulo de pixel, em seguida, os pixels cujos centros estão no retângulo com os cantos em</span><span class="sxs-lookup"><span data-stu-id="ffdeb-122">During the execution of [**glDrawPixels**](gldrawpixels.md) or [**glCopyPixels**](glcopypixels.md), if (*x*<sub>r</sub> ,*y*<sub>r</sub> ) is the current raster position, and a given element is in the *n* th row and *m* th column of the pixel rectangle, then pixels whose centers are in the rectangle with corners at</span></span>

![Equação mostrando os locais em que os pixels são candidatos para substituição.](images/pix05.png)

<span data-ttu-id="ffdeb-124">são candidatos para substituição.</span><span class="sxs-lookup"><span data-stu-id="ffdeb-124">are candidates for replacement.</span></span> <span data-ttu-id="ffdeb-125">Qualquer pixel cujo centro esteja na borda inferior ou esquerda dessa região retangular também será modificado.</span><span class="sxs-lookup"><span data-stu-id="ffdeb-125">Any pixel whose center lies on the bottom or left edge of this rectangular region is also modified.</span></span>

<span data-ttu-id="ffdeb-126">Os fatores de zoom de pixel não se limitam a valores positivos.</span><span class="sxs-lookup"><span data-stu-id="ffdeb-126">Pixel zoom factors are not limited to positive values.</span></span> <span data-ttu-id="ffdeb-127">Fatores de zoom negativos refletem a imagem resultante sobre a posição de rasterização atual.</span><span class="sxs-lookup"><span data-stu-id="ffdeb-127">Negative zoom factors reflect the resulting image about the current raster position.</span></span>

<span data-ttu-id="ffdeb-128">As funções a seguir recuperam informações relacionadas ao **glPixelZoom**:</span><span class="sxs-lookup"><span data-stu-id="ffdeb-128">The following functions retrieve information related to **glPixelZoom**:</span></span>

<span data-ttu-id="ffdeb-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL de \_ zoom \_ X</span><span class="sxs-lookup"><span data-stu-id="ffdeb-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ZOOM\_X</span></span>

<span data-ttu-id="ffdeb-130">**glGet** com Argument GL \_ zoom \_ Y</span><span class="sxs-lookup"><span data-stu-id="ffdeb-130">**glGet** with argument GL\_ZOOM\_Y</span></span>

## <a name="requirements"></a><span data-ttu-id="ffdeb-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffdeb-131">Requirements</span></span>



| <span data-ttu-id="ffdeb-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffdeb-132">Requirement</span></span> | <span data-ttu-id="ffdeb-133">Valor</span><span class="sxs-lookup"><span data-stu-id="ffdeb-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffdeb-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ffdeb-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ffdeb-135">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ffdeb-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ffdeb-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ffdeb-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ffdeb-137">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ffdeb-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ffdeb-138">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ffdeb-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffdeb-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffdeb-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ffdeb-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ffdeb-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="ffdeb-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ffdeb-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ffdeb-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ffdeb-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffdeb-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffdeb-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffdeb-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="ffdeb-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffdeb-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="ffdeb-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ffdeb-146">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="ffdeb-146">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="ffdeb-147">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="ffdeb-147">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="ffdeb-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="ffdeb-148">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





