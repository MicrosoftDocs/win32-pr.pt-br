---
description: Enviado a uma janela quando a janela está prestes a ser ocultada ou exibida.
ms.assetid: dea7c9aa-eba7-4b93-a4c5-9b2d36999780
title: Mensagem de WM_SHOWWINDOW (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbca6cbb4c73ff1cad31754b1b581e0c892970e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296763"
---
# <a name="wm_showwindow-message"></a>Mensagem de janela do WM \_

Enviado a uma janela quando a janela está prestes a ser ocultada ou exibida.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_SHOWWINDOW                   0x0018
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Indica se uma janela está sendo mostrada. Se *wParam* for **true**, a janela será mostrada. Se *wParam* for **false**, a janela estará sendo ocultada.

</dd> <dt>

*lParam* 
</dt> <dd>

O status da janela que está sendo mostrada. Se *lParam* for zero, a mensagem foi enviada devido a uma chamada para a função de [**janela**](/windows/win32/api/winuser/nf-winuser-showwindow) . caso contrário, *lParam* será um dos valores a seguir.



| Valor                                                                                                                                                                                                                         | Significado                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="SW_OTHERUNZOOM"></span><span id="sw_otherunzoom"></span><dl> <dt>**SW \_ OTHERUNZOOM**</dt> <dt>4</dt> </dl>       | A janela está sendo descoberta porque uma janela maximizada foi restaurada ou minimizada.<br/> |
| <span id="SW_OTHERZOOM"></span><span id="sw_otherzoom"></span><dl> <dt>**SW \_ OTHERZOOM**</dt> <dt>2</dt> </dl>             | A janela está sendo coberta por outra janela que foi maximizada.<br/>             |
| <span id="SW_PARENTCLOSING"></span><span id="sw_parentclosing"></span><dl> <dt>**SW \_ PARENTCLOSING**</dt> <dt>1</dt> </dl> | A janela do proprietário da janela está sendo minimizada.<br/>                                      |
| <span id="SW_PARENTOPENING"></span><span id="sw_parentopening"></span><dl> <dt>**SW \_ PARENTOPENING**</dt> <dt>3</dt> </dl> | A janela do proprietário da janela está sendo restaurada.<br/>                                       |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **LRESULT**

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) oculta ou mostra a janela, conforme especificado pela mensagem. Se uma janela tiver o estilo do [**WS \_ visível**](window-styles.md) quando for criada, a janela receberá essa mensagem depois que ela for criada, mas antes de ser exibida. Uma janela também recebe essa mensagem quando seu estado de visibilidade é alterado pela [**ShowOwnedPopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups) ou função de [**janela**](/windows/win32/api/winuser/nf-winuser-showwindow) .

A mensagem de **\_ janela do WM** não é enviada nas seguintes circunstâncias:

-   Quando uma janela de nível superior sobreposta é criada com o estilo [**WS \_ Maxim**](window-styles.md) ou **WS \_ minimize** .
-   Quando o sinalizador de **SW \_ innormal** é especificado na chamada para a função de [**janela**](/windows/win32/api/winuser/nf-winuser-showwindow) .

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

[**ShowOwnedPopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups)
</dt> <dt>

[**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
