---
title: Método IDWriteFactory2 CreateGlyphRunAnalysis
description: Cria um objeto de análise de execução de glifos, que encapsula informações usadas para renderizar uma execução de glifo.
ms.assetid: 13cecfbf-8bb6-88a2-c8b2-3243f6cb92fd
keywords:
- Gravação direta do método CreateGlyphRunAnalysis
- Método CreateGlyphRunAnalysis Direct Write, interface IDWriteFactory2
- IDWriteFactory2 interface de gravação direta, método CreateGlyphRunAnalysis
topic_type:
- apiref
api_name:
- IDWriteFactory2.CreateGlyphRunAnalysis
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abd944c45fc271a22a0942556038073ebcc591cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369750"
---
# <a name="idwritefactory2createglyphrunanalysis-method"></a><span data-ttu-id="b0224-106">Método IDWriteFactory2:: CreateGlyphRunAnalysis</span><span class="sxs-lookup"><span data-stu-id="b0224-106">IDWriteFactory2::CreateGlyphRunAnalysis method</span></span>

<span data-ttu-id="b0224-107">Cria um objeto de análise de execução de glifos, que encapsula informações usadas para renderizar uma execução de glifo.</span><span class="sxs-lookup"><span data-stu-id="b0224-107">Creates a glyph run analysis object, which encapsulates information used to render a glyph run.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0224-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0224-108">Syntax</span></span>


```C++
virtual HRESULT CreateGlyphRunAnalysis(
  [in]           const DWRITE_GLYPH_RUN           *glyphRun,
  [in, optional] const DWRITE_MATRIX              *transform,
                       DWRITE_RENDERING_MODE      renderingMode,
                       DWRITE_MEASURING_MODE      measuringMode,
                       DWRITE_GRID_FIT_MODE       gridFitMode,
                       DWRITE_TEXT_ANTIALIAS_MODE antialiasMode,
                       FLOAT                      baselineOriginX,
                       FLOAT                      baselineOriginY,
  [out]                IDWriteGlyphRunAnalysis    **glyphRunAnalysis
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="b0224-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0224-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0224-110">*GlyphRun* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b0224-110">*glyphRun* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0224-111">Tipo: \**const [**DWRITE \_ glifo \_ Run**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) \** _</span><span class="sxs-lookup"><span data-stu-id="b0224-111">Type: \**const [**DWRITE\_GLYPH\_RUN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run)\** _</span></span>

<span data-ttu-id="b0224-112">Estrutura que especifica as propriedades da execução de glifo.</span><span class="sxs-lookup"><span data-stu-id="b0224-112">Structure specifying the properties of the glyph run.</span></span>

</dd> <dt>

<span data-ttu-id="b0224-113">_transform \* \[ in, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b0224-113">_transform\* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b0224-114">Tipo: \**const [**DWRITE \_ Matrix**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \** _</span><span class="sxs-lookup"><span data-stu-id="b0224-114">Type: \**const [**DWRITE\_MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix)\** _</span></span>

<span data-ttu-id="b0224-115">Transformação opcional aplicada aos glifos e às suas posições.</span><span class="sxs-lookup"><span data-stu-id="b0224-115">Optional transform applied to the glyphs and their positions.</span></span> <span data-ttu-id="b0224-116">Essa transformação é aplicada após o dimensionamento especificado por emSize e pixelsPerDip.</span><span class="sxs-lookup"><span data-stu-id="b0224-116">This transform is applied after the scaling specified by the emSize and pixelsPerDip.</span></span>

</dd> <dt>

<span data-ttu-id="b0224-117">_renderingMode \*</span><span class="sxs-lookup"><span data-stu-id="b0224-117">_renderingMode\*</span></span> 
</dt> <dd>

<span data-ttu-id="b0224-118">Tipo: **\_ \_ modo de renderização DWRITE**</span><span class="sxs-lookup"><span data-stu-id="b0224-118">Type: **DWRITE\_RENDERING\_MODE**</span></span>

<span data-ttu-id="b0224-119">Especifica o modo de renderização, que deve ser um dos modos de renderização de rasterização (ou seja, não padrão e não contorno).</span><span class="sxs-lookup"><span data-stu-id="b0224-119">Specifies the rendering mode, which must be one of the raster rendering modes (i.e., not default and not outline).</span></span>

</dd> <dt>

<span data-ttu-id="b0224-120">*medirmode*</span><span class="sxs-lookup"><span data-stu-id="b0224-120">*measuringMode*</span></span> 
</dt> <dd>

<span data-ttu-id="b0224-121">Tipo: **[ **\_ \_ modo de medição DWRITE**](/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode)**</span><span class="sxs-lookup"><span data-stu-id="b0224-121">Type: **[**DWRITE\_MEASURING\_MODE**](/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode)**</span></span>

<span data-ttu-id="b0224-122">Especifica o método para medir glifos.</span><span class="sxs-lookup"><span data-stu-id="b0224-122">Specifies the method to measure glyphs.</span></span>

</dd> <dt>

<span data-ttu-id="b0224-123">*gridFitMode*</span><span class="sxs-lookup"><span data-stu-id="b0224-123">*gridFitMode*</span></span> 
</dt> <dd>

<span data-ttu-id="b0224-124">Tipo: **[ **\_ modo de \_ ajuste \_ da grade DWRITE**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**</span><span class="sxs-lookup"><span data-stu-id="b0224-124">Type: **[**DWRITE\_GRID\_FIT\_MODE**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**</span></span>

<span data-ttu-id="b0224-125">Como ajustar os contornos de glifo de grade.</span><span class="sxs-lookup"><span data-stu-id="b0224-125">How to grid-fit glyph outlines.</span></span> <span data-ttu-id="b0224-126">Isso deve ser não padrão.</span><span class="sxs-lookup"><span data-stu-id="b0224-126">This must be non-default.</span></span>

</dd> <dt>

<span data-ttu-id="b0224-127">*antialiasmode*</span><span class="sxs-lookup"><span data-stu-id="b0224-127">*antialiasMode*</span></span> 
</dt> <dd>

<span data-ttu-id="b0224-128">Tipo: **[ **\_ modo de \_ AntiAlias \_ de texto DWRITE**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode)**</span><span class="sxs-lookup"><span data-stu-id="b0224-128">Type: **[**DWRITE\_TEXT\_ANTIALIAS\_MODE**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode)**</span></span>

<span data-ttu-id="b0224-129">Especifica o modo AntiAlias.</span><span class="sxs-lookup"><span data-stu-id="b0224-129">Specifies the antialias mode.</span></span>

</dd> <dt>

<span data-ttu-id="b0224-130">*baselineOriginX*</span><span class="sxs-lookup"><span data-stu-id="b0224-130">*baselineOriginX*</span></span> 
</dt> <dd>

<span data-ttu-id="b0224-131">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="b0224-131">Type: **FLOAT**</span></span>

<span data-ttu-id="b0224-132">Posição horizontal da origem da linha de base, em DIPs.</span><span class="sxs-lookup"><span data-stu-id="b0224-132">Horizontal position of the baseline origin, in DIPs.</span></span>

</dd> <dt>

<span data-ttu-id="b0224-133">*baselineOriginY*</span><span class="sxs-lookup"><span data-stu-id="b0224-133">*baselineOriginY*</span></span> 
</dt> <dd>

<span data-ttu-id="b0224-134">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="b0224-134">Type: **FLOAT**</span></span>

<span data-ttu-id="b0224-135">Posição vertical da origem da linha de base, em DIPs.</span><span class="sxs-lookup"><span data-stu-id="b0224-135">Vertical position of the baseline origin, in DIPs.</span></span>

</dd> <dt>

<span data-ttu-id="b0224-136">*glyphRunAnalysis* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b0224-136">*glyphRunAnalysis* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0224-137">Tipo: **[ **IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis)\*\***</span><span class="sxs-lookup"><span data-stu-id="b0224-137">Type: **[**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis)\*\***</span></span>

<span data-ttu-id="b0224-138">Recebe um ponteiro para o objeto recém-criado.</span><span class="sxs-lookup"><span data-stu-id="b0224-138">Receives a pointer to the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0224-139">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b0224-139">Return value</span></span>

<span data-ttu-id="b0224-140">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b0224-140">Type: **HRESULT**</span></span>

<span data-ttu-id="b0224-141">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b0224-141">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b0224-142">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b0224-142">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0224-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0224-143">Requirements</span></span>



| <span data-ttu-id="b0224-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0224-144">Requirement</span></span> | <span data-ttu-id="b0224-145">Valor</span><span class="sxs-lookup"><span data-stu-id="b0224-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0224-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0224-146">Minimum supported client</span></span><br/> | <span data-ttu-id="b0224-147">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b0224-147">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="b0224-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0224-148">Minimum supported server</span></span><br/> | <span data-ttu-id="b0224-149">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="b0224-149">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="b0224-150">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="b0224-150">Minimum supported phone</span></span><br/>  | <span data-ttu-id="b0224-151">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="b0224-151">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="b0224-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b0224-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="b0224-153"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0224-153"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="b0224-154">DLL</span><span class="sxs-lookup"><span data-stu-id="b0224-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0224-155"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0224-155"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b0224-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0224-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0224-157">**IDWriteFactory2**</span><span class="sxs-lookup"><span data-stu-id="b0224-157">**IDWriteFactory2**</span></span>](idwritefactory2.md)
</dt> </dl>

 

