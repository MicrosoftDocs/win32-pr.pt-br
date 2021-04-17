---
title: Métodos SetTransform de IDCompositionVisual3 (DCOMP. h)
description: Define a propriedade Transform deste visual. A propriedade Transform especifica uma transformação 3D usada para modificar o sistema de coordenadas deste visual. A propriedade pode especificar uma matriz de transformação 4 por 4 ou um objeto de transformação.
ms.assetid: a59498c2-8659-dd35-8dc2-87457f493965
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
ms.openlocfilehash: 50237d4bbc8504a6bdcc9650f6c02dbdc30d093c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105780349"
---
# <a name="idcompositionvisual3settransform-methods"></a><span data-ttu-id="83edb-106">Métodos IDCompositionVisual3:: SetTransform</span><span class="sxs-lookup"><span data-stu-id="83edb-106">IDCompositionVisual3::SetTransform methods</span></span>

<span data-ttu-id="83edb-107">Define a propriedade Transform deste visual.</span><span class="sxs-lookup"><span data-stu-id="83edb-107">Sets the Transform property of this visual.</span></span> <span data-ttu-id="83edb-108">A propriedade Transform especifica uma transformação 3D usada para modificar o sistema de coordenadas deste visual.</span><span class="sxs-lookup"><span data-stu-id="83edb-108">The Transform property specifies a 3D transform used to modify the coordinate system of this visual.</span></span> <span data-ttu-id="83edb-109">A propriedade pode especificar uma matriz de transformação 4 por 4 ou um objeto de transformação.</span><span class="sxs-lookup"><span data-stu-id="83edb-109">The property can specify either a 4-by-4 transform matrix or a transform object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="83edb-110">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="83edb-110">Overload list</span></span>



| <span data-ttu-id="83edb-111">Método</span><span class="sxs-lookup"><span data-stu-id="83edb-111">Method</span></span>                                                                                  | <span data-ttu-id="83edb-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="83edb-112">Description</span></span>                                                                    |
|:----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="83edb-113">[**SetTransform (D2D \_ Matrix \_ 4X4 \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(constd2d_matrix_4x4_f_))</span><span class="sxs-lookup"><span data-stu-id="83edb-113">[**SetTransform(D2D\_MATRIX\_4X4\_F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(constd2d_matrix_4x4_f_))</span></span>       | <span data-ttu-id="83edb-114">Define a propriedade Transform para a matriz de transformação especificada.</span><span class="sxs-lookup"><span data-stu-id="83edb-114">Sets the Transform property to the specified transform matrix.</span></span><br/>      |
| <span data-ttu-id="83edb-115">[**SetTransform (IDCompositionTransform3D \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(idcompositiontransform3d))</span><span class="sxs-lookup"><span data-stu-id="83edb-115">[**SetTransform(IDCompositionTransform3D\*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(idcompositiontransform3d))</span></span> | <span data-ttu-id="83edb-116">Define a propriedade Transform para o objeto de transformação especificado.</span><span class="sxs-lookup"><span data-stu-id="83edb-116">Sets the Transform property to the specified transformation object.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="83edb-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83edb-117">Requirements</span></span>



| <span data-ttu-id="83edb-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="83edb-118">Requirement</span></span> | <span data-ttu-id="83edb-119">Valor</span><span class="sxs-lookup"><span data-stu-id="83edb-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="83edb-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83edb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="83edb-121">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="83edb-121">Windows�8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="83edb-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83edb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="83edb-123">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="83edb-123">Windows Server�2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="83edb-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="83edb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="83edb-125"><dt>DCOMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="83edb-125"><dt>Dcomp.h</dt></span></span> </dl>   |
| <span data-ttu-id="83edb-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="83edb-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="83edb-127"><dt>DCOMP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83edb-127"><dt>Dcomp.lib</dt></span></span> </dl> |
| <span data-ttu-id="83edb-128">DLL</span><span class="sxs-lookup"><span data-stu-id="83edb-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83edb-129"><dt>Dcomp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83edb-129"><dt>Dcomp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83edb-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="83edb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83edb-131">**IDCompositionVisual3**</span><span class="sxs-lookup"><span data-stu-id="83edb-131">**IDCompositionVisual3**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual3)
</dt> <dt>

[<span data-ttu-id="83edb-132">**IDCompositionMatrixTransform**</span><span class="sxs-lookup"><span data-stu-id="83edb-132">**IDCompositionMatrixTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> <dt>

[<span data-ttu-id="83edb-133">**IDCompositionRotateTransform**</span><span class="sxs-lookup"><span data-stu-id="83edb-133">**IDCompositionRotateTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)
</dt> <dt>

[<span data-ttu-id="83edb-134">**IDCompositionScaleTransform**</span><span class="sxs-lookup"><span data-stu-id="83edb-134">**IDCompositionScaleTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)
</dt> <dt>

[<span data-ttu-id="83edb-135">**IDCompositionSkewTransform**</span><span class="sxs-lookup"><span data-stu-id="83edb-135">**IDCompositionSkewTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)
</dt> <dt>

[<span data-ttu-id="83edb-136">**IDCompositionTransform**</span><span class="sxs-lookup"><span data-stu-id="83edb-136">**IDCompositionTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositiontransform)
</dt> <dt>

[<span data-ttu-id="83edb-137">**IDCompositionTranslateTransform**</span><span class="sxs-lookup"><span data-stu-id="83edb-137">**IDCompositionTranslateTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)
</dt> <dt>

[<span data-ttu-id="83edb-138">**IDCompositionVisual**</span><span class="sxs-lookup"><span data-stu-id="83edb-138">**IDCompositionVisual**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> <dt>

[<span data-ttu-id="83edb-139">**IDCompositionVisual::SetOffsetX**</span><span class="sxs-lookup"><span data-stu-id="83edb-139">**IDCompositionVisual::SetOffsetX**</span></span>](idcompositionvisual-setoffsetx-overloaded.md)
</dt> <dt>

[<span data-ttu-id="83edb-140">**IDCompositionVisual:: setdeslocy**</span><span class="sxs-lookup"><span data-stu-id="83edb-140">**IDCompositionVisual::SetOffsetY**</span></span>](idcompositionvisual-setoffsety-overloaded.md)
</dt> </dl>

<span data-ttu-id="83edb-141">�</span><span class="sxs-lookup"><span data-stu-id="83edb-141">�</span></span>

<span data-ttu-id="83edb-142">�</span><span class="sxs-lookup"><span data-stu-id="83edb-142">�</span></span>
