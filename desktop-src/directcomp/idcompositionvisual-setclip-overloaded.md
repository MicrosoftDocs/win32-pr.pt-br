---
title: Métodos SetClip IDCompositionVisual (DCOMP. h)
description: Define a propriedade Clip deste visual como a região retangular ou o objeto de clipe especificado.
ms.assetid: ACEBA4F9-E1B0-459B-8DC2-272A822AB214
keywords:
- Métodos SetClip DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: e421c916d305b95029bb6ffd8328346b4ea36918
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645127"
---
# <a name="idcompositionvisualsetclip-methods"></a><span data-ttu-id="a5a92-104">Métodos IDCompositionVisual:: SetClip</span><span class="sxs-lookup"><span data-stu-id="a5a92-104">IDCompositionVisual::SetClip methods</span></span>

<span data-ttu-id="a5a92-105">Define a propriedade Clip deste visual como a região retangular ou o objeto de clipe especificado.</span><span class="sxs-lookup"><span data-stu-id="a5a92-105">Sets the Clip property of this visual to the specified rectangular region or clip object.</span></span> <span data-ttu-id="a5a92-106">A propriedade Clip restringe a renderização da subárvore visual que é enraizada neste visual para uma região retangular.</span><span class="sxs-lookup"><span data-stu-id="a5a92-106">The Clip property restricts the rendering of the visual subtree that is rooted at this visual to a rectangular region.</span></span>

### <a name="overload-list"></a><span data-ttu-id="a5a92-107">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="a5a92-107">Overload list</span></span>



| <span data-ttu-id="a5a92-108">Método</span><span class="sxs-lookup"><span data-stu-id="a5a92-108">Method</span></span>                                                                                | <span data-ttu-id="a5a92-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="a5a92-109">Description</span></span>                                                            |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| <span data-ttu-id="a5a92-110">[**SetClip (const D2D \_ Rect \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_))</span><span class="sxs-lookup"><span data-stu-id="a5a92-110">[**SetClip(const D2D\_RECT\_F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_))</span></span> | <span data-ttu-id="a5a92-111">Define a propriedade Clip como a região retangular especificada.</span><span class="sxs-lookup"><span data-stu-id="a5a92-111">Sets the Clip property to the specified rectangular region.</span></span><br/> |
| <span data-ttu-id="a5a92-112">[**SetClip (IDCompositionClip \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip))</span><span class="sxs-lookup"><span data-stu-id="a5a92-112">[**SetClip(IDCompositionClip\*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip))</span></span> | <span data-ttu-id="a5a92-113">Define a propriedade de clipe para o objeto de clipe especificado.</span><span class="sxs-lookup"><span data-stu-id="a5a92-113">Sets the Clip property to the specified clip object.</span></span><br/>        |



## <a name="requirements"></a><span data-ttu-id="a5a92-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5a92-114">Requirements</span></span>



| <span data-ttu-id="a5a92-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5a92-115">Requirement</span></span> | <span data-ttu-id="a5a92-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a5a92-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a5a92-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5a92-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a5a92-118">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a5a92-118">Windows�8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a5a92-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5a92-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a5a92-120">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a5a92-120">Windows Server�2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a5a92-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a5a92-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5a92-122"><dt>DCOMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5a92-122"><dt>Dcomp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a5a92-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a5a92-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="a5a92-124"><dt>DCOMP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5a92-124"><dt>Dcomp.lib</dt></span></span> </dl> |
| <span data-ttu-id="a5a92-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a5a92-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5a92-126"><dt>Dcomp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5a92-126"><dt>Dcomp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5a92-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5a92-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5a92-128">Recorte</span><span class="sxs-lookup"><span data-stu-id="a5a92-128">Clipping</span></span>](clipping.md)
</dt> <dt>

[<span data-ttu-id="a5a92-129">**IDCompositionVisual**</span><span class="sxs-lookup"><span data-stu-id="a5a92-129">**IDCompositionVisual**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> </dl>

<span data-ttu-id="a5a92-130">�</span><span class="sxs-lookup"><span data-stu-id="a5a92-130">�</span></span>

<span data-ttu-id="a5a92-131">�</span><span class="sxs-lookup"><span data-stu-id="a5a92-131">�</span></span>
