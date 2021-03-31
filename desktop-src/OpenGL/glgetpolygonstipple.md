---
title: função glGetPolygonStipple (GL. h)
description: A função glGetPolygonStipple retorna o padrão de polígono Stipple.
ms.assetid: 95c1ebfa-8465-4bc1-b3f5-eed696a83816
keywords:
- função glGetPolygonStipple OpenGL
topic_type:
- apiref
api_name:
- glGetPolygonStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643d0ea6b7583f26565ab7b9233f7df1dce9aead
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824238"
---
# <a name="glgetpolygonstipple-function"></a><span data-ttu-id="4a469-104">função glGetPolygonStipple</span><span class="sxs-lookup"><span data-stu-id="4a469-104">glGetPolygonStipple function</span></span>

<span data-ttu-id="4a469-105">A função **glGetPolygonStipple** retorna o padrão de polígono Stipple.</span><span class="sxs-lookup"><span data-stu-id="4a469-105">The **glGetPolygonStipple** function returns the polygon stipple pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a469-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4a469-106">Syntax</span></span>


```C++
void WINAPI glGetPolygonStipple(
   GLubyte *mask
);
```



## <a name="parameters"></a><span data-ttu-id="4a469-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a469-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a469-108">*mascara*</span><span class="sxs-lookup"><span data-stu-id="4a469-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="4a469-109">Retorna o padrão Stipple.</span><span class="sxs-lookup"><span data-stu-id="4a469-109">Returns the stipple pattern.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a469-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4a469-110">Return value</span></span>

<span data-ttu-id="4a469-111">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4a469-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4a469-112">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="4a469-112">Error codes</span></span>

<span data-ttu-id="4a469-113">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="4a469-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="4a469-114">Name</span><span class="sxs-lookup"><span data-stu-id="4a469-114">Name</span></span>                                                                                                  | <span data-ttu-id="4a469-115">Significado</span><span class="sxs-lookup"><span data-stu-id="4a469-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4a469-116"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4a469-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="4a469-117">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="4a469-117">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4a469-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a469-118">Remarks</span></span>

<span data-ttu-id="4a469-119">A função **glGetPolygonStipple** retorna um padrão de Stipple de polígono de 32x32 por meio do parâmetro *Mask* .</span><span class="sxs-lookup"><span data-stu-id="4a469-119">The **glGetPolygonStipple** function returns a 32x32 polygon stipple pattern through the *mask* parameter.</span></span> <span data-ttu-id="4a469-120">O padrão é empacotado na memória como se [**glReadPixels**](glreadpixels.md) com *altura* e *largura* de 32, *tipo* de \_ bitmap GL e *formato* do índice de cores GL ser \_ \_ chamado, e o padrão Stipple fosse armazenado em um buffer de índice de cores 32x32 interno.</span><span class="sxs-lookup"><span data-stu-id="4a469-120">The pattern is packed into memory as if [**glReadPixels**](glreadpixels.md) with both *height* and *width* of 32, *type* of GL\_BITMAP, and *format* of GL\_COLOR\_INDEX were called, and the stipple pattern were stored in an internal 32x32 color-index buffer.</span></span> <span data-ttu-id="4a469-121">Ao contrário de **glReadPixels**, no entanto, as operações de transferência de pixels (Shift, deslocamento e mapa de pixel) não são aplicadas à imagem Stipple retornada.</span><span class="sxs-lookup"><span data-stu-id="4a469-121">Unlike **glReadPixels**, however, pixel-transfer operations (shift, offset, and pixel map) are not applied to the returned stipple image.</span></span>

<span data-ttu-id="4a469-122">Se um erro for gerado, nenhuma alteração será feita no conteúdo da *máscara*.</span><span class="sxs-lookup"><span data-stu-id="4a469-122">If an error is generated, no change is made to the contents of *mask*.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a469-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a469-123">Requirements</span></span>



| <span data-ttu-id="4a469-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a469-124">Requirement</span></span> | <span data-ttu-id="4a469-125">Valor</span><span class="sxs-lookup"><span data-stu-id="4a469-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a469-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a469-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4a469-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4a469-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4a469-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a469-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4a469-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4a469-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4a469-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4a469-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a469-131"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a469-131"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="4a469-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4a469-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="4a469-133"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a469-133"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4a469-134">DLL</span><span class="sxs-lookup"><span data-stu-id="4a469-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a469-135"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a469-135"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a469-136">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4a469-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a469-137">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="4a469-137">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="4a469-138">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="4a469-138">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="4a469-139">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="4a469-139">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="4a469-140">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="4a469-140">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="4a469-141">**glPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="4a469-141">**glPolygonStipple**</span></span>](glpolygonstipple.md)
</dt> <dt>

[<span data-ttu-id="4a469-142">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="4a469-142">**glReadPixels**</span></span>](glreadpixels.md)
</dt> </dl>

 

 





