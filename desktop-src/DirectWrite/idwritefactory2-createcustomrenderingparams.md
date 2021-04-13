---
title: Método IDWriteFactory2 CreateCustomRenderingParams
description: Cria um objeto de parâmetros de renderização com as propriedades especificadas.
ms.assetid: 947d50fd-888c-2f0b-25c2-b19b0e6fad58
keywords:
- Gravação direta do método CreateCustomRenderingParams
- Método CreateCustomRenderingParams Direct Write, interface IDWriteFactory2
- IDWriteFactory2 interface de gravação direta, método CreateCustomRenderingParams
topic_type:
- apiref
api_name:
- IDWriteFactory2.CreateCustomRenderingParams
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36bd69cde6858061b69b8143dcdd0560342e65f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369751"
---
# <a name="idwritefactory2createcustomrenderingparams-method"></a><span data-ttu-id="15739-106">Método IDWriteFactory2:: CreateCustomRenderingParams</span><span class="sxs-lookup"><span data-stu-id="15739-106">IDWriteFactory2::CreateCustomRenderingParams method</span></span>

<span data-ttu-id="15739-107">Cria um objeto de parâmetros de renderização com as propriedades especificadas.</span><span class="sxs-lookup"><span data-stu-id="15739-107">Creates a rendering parameters object with the specified properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="15739-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15739-108">Syntax</span></span>


```C++
virtual HRESULT CreateCustomRenderingParams(
        FLOAT                   gamma,
        FLOAT                   enhancedContrast,
        FLOAT                   grayscaleEnhancedContrast,
        FLOAT                   clearTypeLevel,
        DWRITE_PIXEL_GEOMETRY   pixelGeometry,
        DWRITE_RENDERING_MODE   renderingMode,
        DWRITE_GRID_FIT_MODE    gridFitMode,
  [out] IDWriteRenderingParams2 **renderingParams
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="15739-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15739-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15739-110">*gama*</span><span class="sxs-lookup"><span data-stu-id="15739-110">*gamma*</span></span> 
</dt> <dd>

<span data-ttu-id="15739-111">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="15739-111">Type: **FLOAT**</span></span>

<span data-ttu-id="15739-112">O valor de gama usado para correção gama, que deve ser maior que zero e não pode exceder 256.</span><span class="sxs-lookup"><span data-stu-id="15739-112">The gamma value used for gamma correction, which must be greater than zero and cannot exceed 256.</span></span>

</dd> <dt>

<span data-ttu-id="15739-113">*enhancedContrast*</span><span class="sxs-lookup"><span data-stu-id="15739-113">*enhancedContrast*</span></span> 
</dt> <dd>

<span data-ttu-id="15739-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="15739-114">Type: **FLOAT**</span></span>

<span data-ttu-id="15739-115">O valor de aumento de contraste, zero ou maior.</span><span class="sxs-lookup"><span data-stu-id="15739-115">The amount of contrast enhancement, zero or greater.</span></span>

</dd> <dt>

<span data-ttu-id="15739-116">*grayscaleEnhancedContrast*</span><span class="sxs-lookup"><span data-stu-id="15739-116">*grayscaleEnhancedContrast*</span></span> 
</dt> <dd>

<span data-ttu-id="15739-117">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="15739-117">Type: **FLOAT**</span></span>

<span data-ttu-id="15739-118">O valor de aumento de contraste, zero ou maior.</span><span class="sxs-lookup"><span data-stu-id="15739-118">The amount of contrast enhancement, zero or greater.</span></span>

</dd> <dt>

<span data-ttu-id="15739-119">*clearTypeLevel*</span><span class="sxs-lookup"><span data-stu-id="15739-119">*clearTypeLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="15739-120">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="15739-120">Type: **FLOAT**</span></span>

<span data-ttu-id="15739-121">O grau de nível de ClearType, de 0,0 f (sem ClearType) a 1,0 f (ClearType completo).</span><span class="sxs-lookup"><span data-stu-id="15739-121">The degree of ClearType level, from 0.0f (no ClearType) to 1.0f (full ClearType).</span></span>

</dd> <dt>

<span data-ttu-id="15739-122">*pixelGeometry*</span><span class="sxs-lookup"><span data-stu-id="15739-122">*pixelGeometry*</span></span> 
</dt> <dd>

<span data-ttu-id="15739-123">Tipo: **[ **DWRITE \_ pixel \_ Geometry**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry)**</span><span class="sxs-lookup"><span data-stu-id="15739-123">Type: **[**DWRITE\_PIXEL\_GEOMETRY**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry)**</span></span>

<span data-ttu-id="15739-124">A geometria de um pixel de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15739-124">The geometry of a device pixel.</span></span>

</dd> <dt>

<span data-ttu-id="15739-125">*RenderingMode*</span><span class="sxs-lookup"><span data-stu-id="15739-125">*renderingMode*</span></span> 
</dt> <dd>

<span data-ttu-id="15739-126">Tipo: **[ **\_ \_ modo de renderização DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)**</span><span class="sxs-lookup"><span data-stu-id="15739-126">Type: **[**DWRITE\_RENDERING\_MODE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)**</span></span>

<span data-ttu-id="15739-127">Método de renderização de glifos.</span><span class="sxs-lookup"><span data-stu-id="15739-127">Method of rendering glyphs.</span></span> <span data-ttu-id="15739-128">Na maioria dos casos, deve ser o \_ modo de RENDERIZAÇÃO DWRITE \_ \_ padrão para usar automaticamente um modo apropriado.</span><span class="sxs-lookup"><span data-stu-id="15739-128">In most cases, this should be DWRITE\_RENDERING\_MODE\_DEFAULT to automatically use an appropriate mode.</span></span>

</dd> <dt>

<span data-ttu-id="15739-129">*gridFitMode*</span><span class="sxs-lookup"><span data-stu-id="15739-129">*gridFitMode*</span></span> 
</dt> <dd>

<span data-ttu-id="15739-130">Tipo: **[ **\_ modo de \_ ajuste \_ da grade DWRITE**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**</span><span class="sxs-lookup"><span data-stu-id="15739-130">Type: **[**DWRITE\_GRID\_FIT\_MODE**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**</span></span>

<span data-ttu-id="15739-131">Como colocar em grade os contornos de glifos.</span><span class="sxs-lookup"><span data-stu-id="15739-131">How to grid fit glyph outlines.</span></span> <span data-ttu-id="15739-132">Na maioria dos casos, deve ser DWRITE \_ grade \_ se ajustar \_ ao padrão para escolher automaticamente um modo apropriado.</span><span class="sxs-lookup"><span data-stu-id="15739-132">In most cases, this should be DWRITE\_GRID\_FIT\_DEFAULT to automatically choose an appropriate mode.</span></span>

</dd> <dt>

<span data-ttu-id="15739-133">*renderingParams* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="15739-133">*renderingParams* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15739-134">Tipo: **[ **IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2)\*\***</span><span class="sxs-lookup"><span data-stu-id="15739-134">Type: **[**IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2)\*\***</span></span>

<span data-ttu-id="15739-135">Mantém o objeto de parâmetros de renderização recém-criado ou nulo em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="15739-135">Holds the newly created rendering parameters object, or NULL in case of failure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15739-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="15739-136">Return value</span></span>

<span data-ttu-id="15739-137">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="15739-137">Type: **HRESULT**</span></span>

<span data-ttu-id="15739-138">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="15739-138">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="15739-139">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="15739-139">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="15739-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15739-140">Requirements</span></span>



| <span data-ttu-id="15739-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="15739-141">Requirement</span></span> | <span data-ttu-id="15739-142">Valor</span><span class="sxs-lookup"><span data-stu-id="15739-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15739-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15739-143">Minimum supported client</span></span><br/> | <span data-ttu-id="15739-144">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="15739-144">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="15739-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15739-145">Minimum supported server</span></span><br/> | <span data-ttu-id="15739-146">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="15739-146">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="15739-147">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="15739-147">Minimum supported phone</span></span><br/>  | <span data-ttu-id="15739-148">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="15739-148">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="15739-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="15739-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="15739-150"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15739-150"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="15739-151">DLL</span><span class="sxs-lookup"><span data-stu-id="15739-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15739-152"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15739-152"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="15739-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="15739-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15739-154">**IDWriteFactory2**</span><span class="sxs-lookup"><span data-stu-id="15739-154">**IDWriteFactory2**</span></span>](idwritefactory2.md)
</dt> </dl>

 

