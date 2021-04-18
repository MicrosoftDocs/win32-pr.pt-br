---
description: Enviado a uma janela para recuperar um identificador para o ícone grande ou pequeno associado a uma janela. O sistema exibe o ícone grande na caixa de diálogo ALT + TAB e o ícone pequeno na legenda da janela.
ms.assetid: d3101a9b-9658-4a21-b1f6-2920b723926c
title: Mensagem de WM_GETICON (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d2444e70646d8122a7228094187738811a3f68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793241"
---
# <a name="wm_geticon-message"></a>\_Mensagem de GETicon do WM

Enviado a uma janela para recuperar um identificador para o ícone grande ou pequeno associado a uma janela. O sistema exibe o ícone grande na caixa de diálogo ALT + TAB e o ícone pequeno na legenda da janela.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_GETICON                      0x007F
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O tipo de ícone que está sendo recuperado. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                          | Significado                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ICON_BIG"></span><span id="icon_big"></span><dl> <dt>**Ícone \_ do BIG**</dt> <dt>1</dt> </dl>          | Recupere o ícone grande para a janela.<br/>                                                                                                                   |
| <span id="ICON_SMALL"></span><span id="icon_small"></span><dl> <dt>**Ícone \_ do PEQUENO**</dt> <dt>0</dt> </dl>    | Recupere o ícone pequeno da janela.<br/>                                                                                                                   |
| <span id="ICON_SMALL2"></span><span id="icon_small2"></span><dl> <dt>**Ícone \_ do SMALL2**</dt> <dt>2</dt> </dl> | Recupera o ícone pequeno fornecido pelo aplicativo. Se o aplicativo não fornecer um, o sistema usará o ícone gerado pelo sistema para essa janela.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

O DPI do ícone que está sendo recuperado. Isso pode ser usado para fornecer ícones diferentes, dependendo do tamanho do ícone.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HICON**

O valor de retorno é um identificador para o ícone grande ou pequeno, dependendo do valor de *wParam*. Quando um aplicativo recebe essa mensagem, ele pode retornar um identificador para um ícone grande ou pequeno, ou passar a mensagem para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .

## <a name="remarks"></a>Comentários

Quando um aplicativo recebe essa mensagem, ele pode retornar um identificador para um ícone grande ou pequeno, ou passar a mensagem para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retorna um identificador para o ícone grande ou pequeno associado à janela, dependendo do valor de *wParam*.

Uma janela que não tem nenhum ícone definido explicitamente (com o **WM \_ SetIcon**) usa o ícone para a classe de janela registrada e, nesse caso, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retornará 0 para uma mensagem do **WM \_ GetIcon** . Se o envio de uma mensagem do **WM \_ GetIcon** para uma janela retornar 0, tente chamar a função [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra) para a janela. Se isso retornar 0, tente a função [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**ÍCONE do WM \_**](wm-seticon.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
