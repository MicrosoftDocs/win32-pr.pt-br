---
title: função glPolygonStipple (GL. h)
description: A função glPolygonStipple define o padrão de polígono stippling.
ms.assetid: e066f9cf-36da-4a3b-a34f-2f8a6f5a0ae6
keywords:
- função glPolygonStipple OpenGL
topic_type:
- apiref
api_name:
- glPolygonStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a2eb0b2e4319f7e3e37191fb197cd7ff86a2a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455319"
---
# <a name="glpolygonstipple-function"></a><span data-ttu-id="b50bd-104">função glPolygonStipple</span><span class="sxs-lookup"><span data-stu-id="b50bd-104">glPolygonStipple function</span></span>

<span data-ttu-id="b50bd-105">A função **glPolygonStipple** define o padrão de polígono stippling.</span><span class="sxs-lookup"><span data-stu-id="b50bd-105">The **glPolygonStipple** function sets the polygon stippling pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="b50bd-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b50bd-106">Syntax</span></span>


```C++
void WINAPI glPolygonStipple(
   const GLubyte *mask
);
```



## <a name="parameters"></a><span data-ttu-id="b50bd-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b50bd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b50bd-108">*mascara*</span><span class="sxs-lookup"><span data-stu-id="b50bd-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="b50bd-109">Um ponteiro para um padrão de 32x32 Stipple que será desempacotado da memória da mesma maneira que o [**glDrawPixels**](gldrawpixels.md) descompacta pixels.</span><span class="sxs-lookup"><span data-stu-id="b50bd-109">A pointer to a 32x32 stipple pattern that will be unpacked from memory in the same way that [**glDrawPixels**](gldrawpixels.md) unpacks pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b50bd-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b50bd-110">Return value</span></span>

<span data-ttu-id="b50bd-111">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b50bd-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b50bd-112">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="b50bd-112">Error codes</span></span>

<span data-ttu-id="b50bd-113">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="b50bd-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b50bd-114">Nome</span><span class="sxs-lookup"><span data-stu-id="b50bd-114">Name</span></span>                                                                                                  | <span data-ttu-id="b50bd-115">Significado</span><span class="sxs-lookup"><span data-stu-id="b50bd-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b50bd-116"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b50bd-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b50bd-117">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="b50bd-117">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b50bd-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="b50bd-118">Remarks</span></span>

<span data-ttu-id="b50bd-119">A função **glPolygonStipple** define o padrão de polígono stippling.</span><span class="sxs-lookup"><span data-stu-id="b50bd-119">The **glPolygonStipple** function sets the polygon stippling pattern.</span></span> <span data-ttu-id="b50bd-120">Stippling Polygon, como line stippling (consulte [**glLineStipple**](gllinestipple.md)), mascara alguns fragmentos produzidos pela rasterização, criando um padrão.</span><span class="sxs-lookup"><span data-stu-id="b50bd-120">Polygon stippling, like line stippling (see [**glLineStipple**](gllinestipple.md)), masks out certain fragments produced by rasterization, creating a pattern.</span></span> <span data-ttu-id="b50bd-121">Stippling é independente de anti-aliasing poligonal.</span><span class="sxs-lookup"><span data-stu-id="b50bd-121">Stippling is independent of polygon antialiasing.</span></span>

<span data-ttu-id="b50bd-122">O parâmetro *Mask* é um ponteiro para um padrão de 32x32 Stipple que é armazenado na memória assim como os dados de pixel fornecidos para **glDrawPixels** com *altura* e *largura* iguais a 32, um *formato* de pixel do \_ índice de cores GL e o \_ *tipo* de dados de \_ bitmap GL.</span><span class="sxs-lookup"><span data-stu-id="b50bd-122">The *mask* parameter is a pointer to a 32x32 stipple pattern that is stored in memory just like the pixel data supplied to **glDrawPixels** with *height* and *width* both equal to 32, a pixel *format* of GL\_COLOR\_INDEX, and data *type* of GL\_BITMAP.</span></span> <span data-ttu-id="b50bd-123">Ou seja, o padrão Stipple é representado como uma matriz de 32 bits de índices de cores de 1 bit empacotados em bytes não assinados.</span><span class="sxs-lookup"><span data-stu-id="b50bd-123">That is, the stipple pattern is represented as a 32x32 array of 1-bit color indexes packed in unsigned bytes.</span></span> <span data-ttu-id="b50bd-124">Os parâmetros da função [**glPixelStore**](glpixelstore-functions.md) , como GL \_ Unpack \_ swap \_ bytes e GL \_ Unpack \_ LSB \_ First, afetam a montagem dos bits em um padrão Stipple.</span><span class="sxs-lookup"><span data-stu-id="b50bd-124">The [**glPixelStore**](glpixelstore-functions.md) function parameters, such as GL\_UNPACK\_SWAP\_BYTES and GL\_UNPACK\_LSB\_FIRST, affect the assembling of the bits into a stipple pattern.</span></span> <span data-ttu-id="b50bd-125">As operações de transferência de pixel (Shift, deslocamento e mapa de pixel) não são aplicadas à imagem Stipple, no entanto.</span><span class="sxs-lookup"><span data-stu-id="b50bd-125">Pixel transfer operations (shift, offset, and pixel map) are not applied to the stipple image, however.</span></span>

<span data-ttu-id="b50bd-126">O stippling Polygon está habilitado e desabilitado com [**glEnable**](glenable.md) e **glDisable**, usando o \_ polígono GL Polygon \_ STIPPLE.</span><span class="sxs-lookup"><span data-stu-id="b50bd-126">Polygon stippling is enabled and disabled with [**glEnable**](glenable.md) and **glDisable**, using argument GL\_POLYGON\_STIPPLE.</span></span> <span data-ttu-id="b50bd-127">Se habilitado, um fragmento de polígono rasterizado com coordenadas de janela *x*<sub>w</sub> e *y*<sub>w</sub> será enviado para o próximo estágio do OpenGL se e somente se o (*x*<sub>w</sub> mod 32) de bit na linha (*y*<sub>w</sub> mod 32) th do padrão Stipple for um.</span><span class="sxs-lookup"><span data-stu-id="b50bd-127">If enabled, a rasterized polygon fragment with window coordinates *x*<sub>w</sub> and *y*<sub>w</sub> is sent to the next stage of OpenGL if and only if the (*x*<sub>w</sub> mod 32)th bit in the (*y*<sub>w</sub> mod 32)th row of the stipple pattern is one.</span></span> <span data-ttu-id="b50bd-128">Quando stippling Polygon é desabilitado, é como se o padrão Stipple fosse todos.</span><span class="sxs-lookup"><span data-stu-id="b50bd-128">When polygon stippling is disabled, it is as if the stipple pattern were all ones.</span></span>

<span data-ttu-id="b50bd-129">As funções a seguir recuperam informações relacionadas ao **glPolygonStipple**:</span><span class="sxs-lookup"><span data-stu-id="b50bd-129">The following functions retrieve information related to **glPolygonStipple**:</span></span>

[<span data-ttu-id="b50bd-130">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="b50bd-130">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)

<span data-ttu-id="b50bd-131">[**glIsEnabled**](glisenabled.md) com o argumento GL \_ Polygon \_ STIPPLE</span><span class="sxs-lookup"><span data-stu-id="b50bd-131">[**glIsEnabled**](glisenabled.md) with argument GL\_POLYGON\_STIPPLE</span></span>

## <a name="requirements"></a><span data-ttu-id="b50bd-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b50bd-132">Requirements</span></span>



| <span data-ttu-id="b50bd-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="b50bd-133">Requirement</span></span> | <span data-ttu-id="b50bd-134">Valor</span><span class="sxs-lookup"><span data-stu-id="b50bd-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b50bd-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b50bd-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b50bd-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b50bd-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b50bd-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b50bd-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b50bd-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b50bd-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b50bd-139">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b50bd-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="b50bd-140"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b50bd-140"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b50bd-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b50bd-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="b50bd-142"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b50bd-142"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b50bd-143">DLL</span><span class="sxs-lookup"><span data-stu-id="b50bd-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b50bd-144"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b50bd-144"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b50bd-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="b50bd-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b50bd-146">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b50bd-146">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b50bd-147">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="b50bd-147">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="b50bd-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b50bd-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b50bd-149">**glLineStipple**</span><span class="sxs-lookup"><span data-stu-id="b50bd-149">**glLineStipple**</span></span>](gllinestipple.md)
</dt> <dt>

[<span data-ttu-id="b50bd-150">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="b50bd-150">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="b50bd-151">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="b50bd-151">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> </dl>

 

 





