---
title: Códigos de erro DirectComposition (DCOMP. h)
description: Esta seção descreve os códigos de erro específicos do DirectComposition.
ms.assetid: 8DFBFC34-DBD0-4731-8305-B33E90C96C54
topic_type:
- apiref
api_name:
- DCOMPOSITION_ERROR_ACCESS_DENIED
- DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED
- DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED
- DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED
api_location:
- Dcomp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96a76a7527bacf8caa756a0fad75ca70f4bf9a77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085960"
---
# <a name="directcomposition-error-codes"></a><span data-ttu-id="29817-103">Códigos de erro DirectComposition</span><span class="sxs-lookup"><span data-stu-id="29817-103">DirectComposition error codes</span></span>

<span data-ttu-id="29817-104">Se ocorrer um erro, o Microsoft DirectComposition retornará um código como um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="29817-104">If an error occurs, Microsoft DirectComposition returns a code as an **HRESULT** value.</span></span> <span data-ttu-id="29817-105">Esta seção descreve os códigos de erro específicos do DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="29817-105">This section describes the error codes that are specific to DirectComposition.</span></span> <span data-ttu-id="29817-106">Para obter uma lista de códigos de erro de Component Object Model geral (COM), consulte [códigos de erro com](/windows/desktop/com/com-error-codes).</span><span class="sxs-lookup"><span data-stu-id="29817-106">For a list of general Component Object Model (COM) error codes, see [COM Error Codes](/windows/desktop/com/com-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="29817-107"><span id="DCOMPOSITION_ERROR_ACCESS_DENIED"></span><span id="dcomposition_error_access_denied"></span>**\_ \_ acesso \_ negado ao erro DCOMPOSITION**</span><span class="sxs-lookup"><span data-stu-id="29817-107"><span id="DCOMPOSITION_ERROR_ACCESS_DENIED"></span><span id="dcomposition_error_access_denied"></span>**DCOMPOSITION\_ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="29817-108"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="29817-108"><dt>


</dt> <dt></span></span>



<span data-ttu-id="29817-109">O identificador de janela que foi especificado em uma chamada para o método [**IDCompositionDevice:: CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) pertence a um processo diferente daquele que criou o objeto Device.</span><span class="sxs-lookup"><span data-stu-id="29817-109">The window handle that was specified in a call to the [**IDCompositionDevice::CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) method belongs to a different process from the one that created the device object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="29817-110"><span id="DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED"></span><span id="dcomposition_error_surface_being_rendered"></span>**\_superfície de erro DCOMPOSITION \_ \_ sendo \_ processada**</span><span class="sxs-lookup"><span data-stu-id="29817-110"><span id="DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED"></span><span id="dcomposition_error_surface_being_rendered"></span>**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="29817-111"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="29817-111"><dt>


</dt> <dt></span></span>



<span data-ttu-id="29817-112">A superfície já estava sendo renderizada quando o aplicativo chamou o método [**IDCompositionSurface:: BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw), [**IDCompositionSurface:: SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw)ou [**IDCompositionSurface:: ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) .</span><span class="sxs-lookup"><span data-stu-id="29817-112">The surface was already being rendered when the application called the [**IDCompositionSurface::BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw), [**IDCompositionSurface::SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), or [**IDCompositionSurface::ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) method.</span></span> <span data-ttu-id="29817-113">Para obter mais informações, consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="29817-113">For more information, see Remarks.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="29817-114"><span id="DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED"></span><span id="dcomposition_error_surface_not_being_rendered"></span>**\_superfície de erro DCOMPOSITION \_ \_ não \_ está sendo \_ renderizada**</span><span class="sxs-lookup"><span data-stu-id="29817-114"><span id="DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED"></span><span id="dcomposition_error_surface_not_being_rendered"></span>**DCOMPOSITION\_ERROR\_SURFACE\_NOT\_BEING\_RENDERED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="29817-115"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="29817-115"><dt>


</dt> <dt></span></span>



<span data-ttu-id="29817-116">O aplicativo chamou o método [**IDCompositionSurface:: SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), [**IDCompositionSurface:: ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)ou [**IDCompositionSurface:: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) para uma superfície que não está sendo renderizada.</span><span class="sxs-lookup"><span data-stu-id="29817-116">The application called the [**IDCompositionSurface::SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), [**IDCompositionSurface::ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw), or [**IDCompositionSurface::EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) method for a surface that is not being rendered.</span></span> <span data-ttu-id="29817-117">Para obter mais informações, consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="29817-117">For more information, see Remarks.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="29817-118"><span id="DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED"></span><span id="dcomposition_error_window_already_composed"></span>**\_janela de erro DCOMPOSITION \_ \_ já \_ composta**</span><span class="sxs-lookup"><span data-stu-id="29817-118"><span id="DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED"></span><span id="dcomposition_error_window_already_composed"></span>**DCOMPOSITION\_ERROR\_WINDOW\_ALREADY\_COMPOSED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="29817-119"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="29817-119"><dt>


</dt> <dt></span></span>



<span data-ttu-id="29817-120">O método [**IDCompositionDevice:: CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) foi chamado com *HWND* e parâmetros mais *altos* para os quais uma árvore visual já existe.</span><span class="sxs-lookup"><span data-stu-id="29817-120">The [**IDCompositionDevice::CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) method was called with *hwnd* and *topmost* parameters for which a visual tree already exists.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29817-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="29817-121">Remarks</span></span>

<span data-ttu-id="29817-122">Se uma chamada para o [**IDCompositionSurface:: BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) foi a ação mais recente:</span><span class="sxs-lookup"><span data-stu-id="29817-122">If a call to the [**IDCompositionSurface::BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) was the most recent action:</span></span>



| <span data-ttu-id="29817-123">Chamando este método:</span><span class="sxs-lookup"><span data-stu-id="29817-123">Calling this method:</span></span>                                    | <span data-ttu-id="29817-124">Retorna este valor:</span><span class="sxs-lookup"><span data-stu-id="29817-124">Returns this value:</span></span>                               |
|---------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="29817-125">**BeginDraw**</span><span class="sxs-lookup"><span data-stu-id="29817-125">**BeginDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | <span data-ttu-id="29817-126">**\_superfície de erro DCOMPOSITION \_ \_ sendo \_ processada**</span><span class="sxs-lookup"><span data-stu-id="29817-126">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span> |
| [<span data-ttu-id="29817-127">**EndDraw**</span><span class="sxs-lookup"><span data-stu-id="29817-127">**EndDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | <span data-ttu-id="29817-128">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="29817-128">S\_OK</span></span>                                             |
| [<span data-ttu-id="29817-129">**SuspendDraw**</span><span class="sxs-lookup"><span data-stu-id="29817-129">**SuspendDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | <span data-ttu-id="29817-130">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="29817-130">S\_OK</span></span>                                             |
| [<span data-ttu-id="29817-131">**ResumeDraw**</span><span class="sxs-lookup"><span data-stu-id="29817-131">**ResumeDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | <span data-ttu-id="29817-132">**\_superfície de erro DCOMPOSITION \_ \_ sendo \_ processada**</span><span class="sxs-lookup"><span data-stu-id="29817-132">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span> |



 

<span data-ttu-id="29817-133">Se uma chamada para o [**IDCompositionSurface:: SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) foi a ação mais recente:</span><span class="sxs-lookup"><span data-stu-id="29817-133">If a call to the [**IDCompositionSurface::SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) was the most recent action:</span></span>



| <span data-ttu-id="29817-134">Chamando este método:</span><span class="sxs-lookup"><span data-stu-id="29817-134">Calling this method:</span></span>                                    | <span data-ttu-id="29817-135">Retorna este valor:</span><span class="sxs-lookup"><span data-stu-id="29817-135">Returns this value:</span></span>                               |
|---------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="29817-136">**BeginDraw**</span><span class="sxs-lookup"><span data-stu-id="29817-136">**BeginDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | <span data-ttu-id="29817-137">**\_superfície de erro DCOMPOSITION \_ \_ sendo \_ processada**</span><span class="sxs-lookup"><span data-stu-id="29817-137">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span> |
| [<span data-ttu-id="29817-138">**EndDraw**</span><span class="sxs-lookup"><span data-stu-id="29817-138">**EndDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | <span data-ttu-id="29817-139">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="29817-139">S\_OK</span></span>                                             |
| [<span data-ttu-id="29817-140">**SuspendDraw**</span><span class="sxs-lookup"><span data-stu-id="29817-140">**SuspendDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | <span data-ttu-id="29817-141">**\_superfície de erro DCOMPOSITION \_ \_ sendo \_ processada**</span><span class="sxs-lookup"><span data-stu-id="29817-141">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span> |
| [<span data-ttu-id="29817-142">**ResumeDraw**</span><span class="sxs-lookup"><span data-stu-id="29817-142">**ResumeDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | <span data-ttu-id="29817-143">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="29817-143">S\_OK</span></span>                                             |



 

<span data-ttu-id="29817-144">Se uma chamada para o [**IDCompositionSurface:: ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) foi a ação mais recente:</span><span class="sxs-lookup"><span data-stu-id="29817-144">If a call to the [**IDCompositionSurface::ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) was the most recent action:</span></span>



| <span data-ttu-id="29817-145">Chamando este método:</span><span class="sxs-lookup"><span data-stu-id="29817-145">Calling this method:</span></span>                                    | <span data-ttu-id="29817-146">Retorna este valor:</span><span class="sxs-lookup"><span data-stu-id="29817-146">Returns this value:</span></span>                                |
|---------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="29817-147">**BeginDraw**</span><span class="sxs-lookup"><span data-stu-id="29817-147">**BeginDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | <span data-ttu-id="29817-148">**\_superfície de erro DCOMPOSITION \_ \_ sendo \_ processada**</span><span class="sxs-lookup"><span data-stu-id="29817-148">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span>  |
| [<span data-ttu-id="29817-149">**EndDraw**</span><span class="sxs-lookup"><span data-stu-id="29817-149">**EndDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | <span data-ttu-id="29817-150">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="29817-150">S\_OK</span></span>                                              |
| [<span data-ttu-id="29817-151">**SuspendDraw**</span><span class="sxs-lookup"><span data-stu-id="29817-151">**SuspendDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | <span data-ttu-id="29817-152">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="29817-152">S\_OK</span></span>                                              |
| [<span data-ttu-id="29817-153">**ResumeDraw**</span><span class="sxs-lookup"><span data-stu-id="29817-153">**ResumeDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | <span data-ttu-id="29817-154">**\_superfície de erro DCOMPOSITION \_ \_ que está sendo \_ renderizada.**</span><span class="sxs-lookup"><span data-stu-id="29817-154">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED.**</span></span> |



 

<span data-ttu-id="29817-155">Se uma chamada para [**IDCompositionSurface:: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) foi a ação mais recente:</span><span class="sxs-lookup"><span data-stu-id="29817-155">If a call to the [**IDCompositionSurface::EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) was the most recent action:</span></span>



| <span data-ttu-id="29817-156">Chamando este método:</span><span class="sxs-lookup"><span data-stu-id="29817-156">Calling this method:</span></span>                                    | <span data-ttu-id="29817-157">Retorna este valor:</span><span class="sxs-lookup"><span data-stu-id="29817-157">Returns this value:</span></span>                                     |
|---------------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="29817-158">**BeginDraw**</span><span class="sxs-lookup"><span data-stu-id="29817-158">**BeginDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | <span data-ttu-id="29817-159">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="29817-159">S\_OK</span></span>                                                   |
| [<span data-ttu-id="29817-160">**EndDraw**</span><span class="sxs-lookup"><span data-stu-id="29817-160">**EndDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | <span data-ttu-id="29817-161">**a \_ superfície de erro DCOMPOSITION \_ \_ não \_ está sendo \_ renderizada.**</span><span class="sxs-lookup"><span data-stu-id="29817-161">**DCOMPOSITION\_ERROR\_SURFACE\_NOT\_BEING\_RENDERED.**</span></span> |
| [<span data-ttu-id="29817-162">**SuspendDraw**</span><span class="sxs-lookup"><span data-stu-id="29817-162">**SuspendDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | <span data-ttu-id="29817-163">**a \_ superfície de erro DCOMPOSITION \_ \_ não \_ está sendo \_ renderizada.**</span><span class="sxs-lookup"><span data-stu-id="29817-163">**DCOMPOSITION\_ERROR\_SURFACE\_NOT\_BEING\_RENDERED.**</span></span> |
| [<span data-ttu-id="29817-164">**ResumeDraw**</span><span class="sxs-lookup"><span data-stu-id="29817-164">**ResumeDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | <span data-ttu-id="29817-165">**a \_ superfície de erro DCOMPOSITION \_ \_ não \_ está sendo \_ renderizada.**</span><span class="sxs-lookup"><span data-stu-id="29817-165">**DCOMPOSITION\_ERROR\_SURFACE\_NOT\_BEING\_RENDERED.**</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="29817-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29817-166">Requirements</span></span>



| <span data-ttu-id="29817-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="29817-167">Requirement</span></span> | <span data-ttu-id="29817-168">Valor</span><span class="sxs-lookup"><span data-stu-id="29817-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="29817-169">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29817-169">Minimum supported client</span></span><br/> | <span data-ttu-id="29817-170">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="29817-170">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="29817-171">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29817-171">Minimum supported server</span></span><br/> | <span data-ttu-id="29817-172">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="29817-172">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="29817-173">parâmetro</span><span class="sxs-lookup"><span data-stu-id="29817-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="29817-174"><dt>DCOMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="29817-174"><dt>Dcomp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29817-175">Confira também</span><span class="sxs-lookup"><span data-stu-id="29817-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29817-176">Referência de DirectComposition</span><span class="sxs-lookup"><span data-stu-id="29817-176">DirectComposition Reference</span></span>](reference.md)
</dt> </dl>

 

