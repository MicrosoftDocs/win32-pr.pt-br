---
title: Métodos SetTransform de IDCompositionVisual (DCOMP. h)
description: Define a propriedade Transform deste visual. A propriedade Transform especifica uma transformação 2D usada para modificar o sistema de coordenadas deste visual. A propriedade pode especificar uma matriz de transformação 3-by-2 ou um objeto de transformação.
ms.assetid: DA3CBBB6-DB0A-4FCE-9DAC-7A767783A18D
keywords:
- Métodos SetTransform DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 00f5da890cd22c5c827a36062a0b0c3f9bc19cc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295881"
---
# <a name="idcompositionvisualsettransform-methods"></a><span data-ttu-id="bf397-106">Métodos IDCompositionVisual:: SetTransform</span><span class="sxs-lookup"><span data-stu-id="bf397-106">IDCompositionVisual::SetTransform methods</span></span>

<span data-ttu-id="bf397-107">Define a propriedade Transform deste visual.</span><span class="sxs-lookup"><span data-stu-id="bf397-107">Sets the Transform property of this visual.</span></span> <span data-ttu-id="bf397-108">A propriedade Transform especifica uma transformação 2D usada para modificar o sistema de coordenadas deste visual.</span><span class="sxs-lookup"><span data-stu-id="bf397-108">The Transform property specifies a 2D transform used to modify the coordinate system of this visual.</span></span> <span data-ttu-id="bf397-109">A propriedade pode especificar uma matriz de transformação 3-by-2 ou um objeto de transformação.</span><span class="sxs-lookup"><span data-stu-id="bf397-109">The property can specify either a 3-by-2 transform matrix or a transform object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="bf397-110">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="bf397-110">Overload list</span></span>



| <span data-ttu-id="bf397-111">Método</span><span class="sxs-lookup"><span data-stu-id="bf397-111">Method</span></span>                                                                                                    | <span data-ttu-id="bf397-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf397-112">Description</span></span>                                                                    |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="bf397-113">[**SetTransform (D2D \_ Matrix \_ 3X2 \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_))</span><span class="sxs-lookup"><span data-stu-id="bf397-113">[**SetTransform(D2D\_MATRIX\_3X2\_F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_))</span></span>          | <span data-ttu-id="bf397-114">Define a propriedade Transform para a matriz de transformação especificada.</span><span class="sxs-lookup"><span data-stu-id="bf397-114">Sets the Transform property to the specified transform matrix.</span></span><br/>      |
| <span data-ttu-id="bf397-115">[**SetTransform (IDCompositionTransform \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(idcompositiontransform))</span><span class="sxs-lookup"><span data-stu-id="bf397-115">[**SetTransform(IDCompositionTransform\*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(idcompositiontransform))</span></span> | <span data-ttu-id="bf397-116">Define a propriedade Transform para o objeto de transformação especificado.</span><span class="sxs-lookup"><span data-stu-id="bf397-116">Sets the Transform property to the specified transformation object.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="bf397-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf397-117">Requirements</span></span>



| <span data-ttu-id="bf397-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf397-118">Requirement</span></span> | <span data-ttu-id="bf397-119">Valor</span><span class="sxs-lookup"><span data-stu-id="bf397-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bf397-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf397-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bf397-121">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="bf397-121">Windows�8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bf397-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf397-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bf397-123">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="bf397-123">Windows Server�2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bf397-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bf397-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf397-125"><dt>DCOMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf397-125"><dt>Dcomp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bf397-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bf397-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="bf397-127"><dt>DCOMP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf397-127"><dt>Dcomp.lib</dt></span></span> </dl> |
| <span data-ttu-id="bf397-128">DLL</span><span class="sxs-lookup"><span data-stu-id="bf397-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf397-129"><dt>Dcomp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf397-129"><dt>Dcomp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf397-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf397-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf397-131">**IDCompositionMatrixTransform**</span><span class="sxs-lookup"><span data-stu-id="bf397-131">**IDCompositionMatrixTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> <dt>

[<span data-ttu-id="bf397-132">**IDCompositionRotateTransform**</span><span class="sxs-lookup"><span data-stu-id="bf397-132">**IDCompositionRotateTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)
</dt> <dt>

[<span data-ttu-id="bf397-133">**IDCompositionScaleTransform**</span><span class="sxs-lookup"><span data-stu-id="bf397-133">**IDCompositionScaleTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)
</dt> <dt>

[<span data-ttu-id="bf397-134">**IDCompositionSkewTransform**</span><span class="sxs-lookup"><span data-stu-id="bf397-134">**IDCompositionSkewTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)
</dt> <dt>

[<span data-ttu-id="bf397-135">**IDCompositionTransform**</span><span class="sxs-lookup"><span data-stu-id="bf397-135">**IDCompositionTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositiontransform)
</dt> <dt>

[<span data-ttu-id="bf397-136">**IDCompositionTranslateTransform**</span><span class="sxs-lookup"><span data-stu-id="bf397-136">**IDCompositionTranslateTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)
</dt> <dt>

[<span data-ttu-id="bf397-137">**IDCompositionVisual**</span><span class="sxs-lookup"><span data-stu-id="bf397-137">**IDCompositionVisual**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> <dt>

[<span data-ttu-id="bf397-138">**IDCompositionVisual::SetOffsetX**</span><span class="sxs-lookup"><span data-stu-id="bf397-138">**IDCompositionVisual::SetOffsetX**</span></span>](idcompositionvisual-setoffsetx-overloaded.md)
</dt> <dt>

[<span data-ttu-id="bf397-139">**IDCompositionVisual:: setdeslocy**</span><span class="sxs-lookup"><span data-stu-id="bf397-139">**IDCompositionVisual::SetOffsetY**</span></span>](idcompositionvisual-setoffsety-overloaded.md)
</dt> </dl>

<span data-ttu-id="bf397-140">�</span><span class="sxs-lookup"><span data-stu-id="bf397-140">�</span></span>

<span data-ttu-id="bf397-141">�</span><span class="sxs-lookup"><span data-stu-id="bf397-141">�</span></span>
