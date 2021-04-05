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
# <a name="directcomposition-error-codes"></a>Códigos de erro DirectComposition

Se ocorrer um erro, o Microsoft DirectComposition retornará um código como um valor **HRESULT** . Esta seção descreve os códigos de erro específicos do DirectComposition. Para obter uma lista de códigos de erro de Component Object Model geral (COM), consulte [códigos de erro com](/windows/desktop/com/com-error-codes).

<dl> <dt>

<span id="DCOMPOSITION_ERROR_ACCESS_DENIED"></span><span id="dcomposition_error_access_denied"></span>**\_ \_ acesso \_ negado ao erro DCOMPOSITION**
</dt> <dd> <dl> <dt>


</dt> <dt>



O identificador de janela que foi especificado em uma chamada para o método [**IDCompositionDevice:: CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) pertence a um processo diferente daquele que criou o objeto Device.


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED"></span><span id="dcomposition_error_surface_being_rendered"></span>**\_superfície de erro DCOMPOSITION \_ \_ sendo \_ processada**
</dt> <dd> <dl> <dt>


</dt> <dt>



A superfície já estava sendo renderizada quando o aplicativo chamou o método [**IDCompositionSurface:: BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw), [**IDCompositionSurface:: SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw)ou [**IDCompositionSurface:: ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) . Para obter mais informações, consulte Comentários.


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED"></span><span id="dcomposition_error_surface_not_being_rendered"></span>**\_superfície de erro DCOMPOSITION \_ \_ não \_ está sendo \_ renderizada**
</dt> <dd> <dl> <dt>


</dt> <dt>



O aplicativo chamou o método [**IDCompositionSurface:: SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), [**IDCompositionSurface:: ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)ou [**IDCompositionSurface:: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) para uma superfície que não está sendo renderizada. Para obter mais informações, consulte Comentários.


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED"></span><span id="dcomposition_error_window_already_composed"></span>**\_janela de erro DCOMPOSITION \_ \_ já \_ composta**
</dt> <dd> <dl> <dt>


</dt> <dt>



O método [**IDCompositionDevice:: CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) foi chamado com *HWND* e parâmetros mais *altos* para os quais uma árvore visual já existe.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Se uma chamada para o [**IDCompositionSurface:: BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) foi a ação mais recente:



| Chamando este método:                                    | Retorna este valor:                               |
|---------------------------------------------------------|---------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **\_superfície de erro DCOMPOSITION \_ \_ sendo \_ processada** |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | S \_ OK                                             |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | S \_ OK                                             |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **\_superfície de erro DCOMPOSITION \_ \_ sendo \_ processada** |



 

Se uma chamada para o [**IDCompositionSurface:: SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) foi a ação mais recente:



| Chamando este método:                                    | Retorna este valor:                               |
|---------------------------------------------------------|---------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **\_superfície de erro DCOMPOSITION \_ \_ sendo \_ processada** |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | S \_ OK                                             |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | **\_superfície de erro DCOMPOSITION \_ \_ sendo \_ processada** |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | S \_ OK                                             |



 

Se uma chamada para o [**IDCompositionSurface:: ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) foi a ação mais recente:



| Chamando este método:                                    | Retorna este valor:                                |
|---------------------------------------------------------|----------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **\_superfície de erro DCOMPOSITION \_ \_ sendo \_ processada**  |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | S \_ OK                                              |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | S \_ OK                                              |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **\_superfície de erro DCOMPOSITION \_ \_ que está sendo \_ renderizada.** |



 

Se uma chamada para [**IDCompositionSurface:: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) foi a ação mais recente:



| Chamando este método:                                    | Retorna este valor:                                     |
|---------------------------------------------------------|---------------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | S \_ OK                                                   |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | **a \_ superfície de erro DCOMPOSITION \_ \_ não \_ está sendo \_ renderizada.** |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | **a \_ superfície de erro DCOMPOSITION \_ \_ não \_ está sendo \_ renderizada.** |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **a \_ superfície de erro DCOMPOSITION \_ \_ não \_ está sendo \_ renderizada.** |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>DCOMP. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência de DirectComposition](reference.md)
</dt> </dl>

 

