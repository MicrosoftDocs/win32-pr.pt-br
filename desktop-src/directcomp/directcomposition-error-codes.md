---
title: Códigos de erro DirectComposition (Dcomp.h)
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
ms.openlocfilehash: 7d86ab61574af84e0b4b51223c69b181697dc0ebbdd7995c1bff112e286cc3ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891976"
---
# <a name="directcomposition-error-codes"></a>Códigos de erro directComposition

Se ocorrer um erro, o Microsoft DirectComposition retornará um código como **um valor HRESULT.** Esta seção descreve os códigos de erro específicos do DirectComposition. Para ver uma lista de códigos de Component Object Model (COM), consulte [Códigos de erro COM](/windows/desktop/com/com-error-codes).

<dl> <dt>

<span id="DCOMPOSITION_ERROR_ACCESS_DENIED"></span><span id="dcomposition_error_access_denied"></span>**ACESSO DE ERRO DCOMPOSITION \_ \_ \_ NEGADO**
</dt> <dd> <dl> <dt>


</dt> <dt>



O identificador de janela especificado em uma chamada para o método [**IDCompositionDevice::CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) pertence a um processo diferente do que criou o objeto do dispositivo.


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED"></span><span id="dcomposition_error_surface_being_rendered"></span>**SUPERFÍCIE DE ERRO DCOMPOSITION \_ \_ SENDO \_ \_ RENDERIZADA**
</dt> <dd> <dl> <dt>


</dt> <dt>



A superfície já estava sendo renderizada quando o aplicativo chamou o método [**IDCompositionSurface::BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw), [**IDCompositionSurface::SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw)ou [**IDCompositionSurface::ResumeDraw.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) Para obter mais informações, consulte Comentários.


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED"></span><span id="dcomposition_error_surface_not_being_rendered"></span>**A SUPERFÍCIE DE \_ ERRO DCOMPOSITION NÃO ESTÁ SENDO \_ \_ \_ \_ RENDERIZADA**
</dt> <dd> <dl> <dt>


</dt> <dt>



O aplicativo chamou o método [**IDCompositionSurface::SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), [**IDCompositionSurface::ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)ou [**IDCompositionSurface::EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) para uma superfície que não está sendo renderizada. Para obter mais informações, consulte Comentários.


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED"></span><span id="dcomposition_error_window_already_composed"></span>**JANELA DE ERRO \_ DCOMPOSITION \_ JÁ \_ \_ COMPOSTA**
</dt> <dd> <dl> <dt>


</dt> <dt>



O [**método IDCompositionDevice::CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) foi chamado com *os parâmetros hwnd* e *topmost* para os quais uma árvore visual já existe.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Se uma chamada para [**O IDCompositionSurface::BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) foi a ação mais recente:



| Chamando este método:                                    | Retorna este valor:                               |
|---------------------------------------------------------|---------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **SUPERFÍCIE DE ERRO DCOMPOSITION \_ \_ SENDO \_ \_ RENDERIZADA** |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | S \_ OK                                             |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | S \_ OK                                             |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **SUPERFÍCIE DE ERRO DCOMPOSITION \_ \_ SENDO \_ \_ RENDERIZADA** |



 

Se uma chamada para [**O IDCompositionSurface::SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) foi a ação mais recente:



| Chamando este método:                                    | Retorna este valor:                               |
|---------------------------------------------------------|---------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **SUPERFÍCIE DE ERRO DCOMPOSITION \_ \_ SENDO \_ \_ RENDERIZADA** |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | S \_ OK                                             |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | **SUPERFÍCIE DE ERRO DCOMPOSITION \_ \_ SENDO \_ \_ RENDERIZADA** |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | S \_ OK                                             |



 

Se uma chamada para [**IDCompositionSurface::ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) foi a ação mais recente:



| Chamando este método:                                    | Retorna este valor:                                |
|---------------------------------------------------------|----------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **SUPERFÍCIE DE ERRO DCOMPOSITION \_ \_ SENDO \_ \_ RENDERIZADA**  |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | S \_ OK                                              |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | S \_ OK                                              |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **SUPERFÍCIE DE ERRO DCOMPOSITION \_ \_ SENDO \_ \_ RENDERIZADA.** |



 

Se uma chamada para [**IDCompositionSurface::EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) foi a ação mais recente:



| Chamando este método:                                    | Retorna este valor:                                     |
|---------------------------------------------------------|---------------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | S \_ OK                                                   |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | **A SUPERFÍCIE DE \_ ERRO DCOMPOSITION NÃO ESTÁ SENDO \_ \_ \_ \_ RENDERIZADA.** |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | **A SUPERFÍCIE DE \_ ERRO DCOMPOSITION NÃO ESTÁ SENDO \_ \_ \_ \_ RENDERIZADA.** |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **A SUPERFÍCIE DE \_ ERRO DCOMPOSITION NÃO ESTÁ SENDO \_ \_ \_ \_ RENDERIZADA.** |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Dcomp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência do DirectComposition](reference.md)
</dt> </dl>

 

