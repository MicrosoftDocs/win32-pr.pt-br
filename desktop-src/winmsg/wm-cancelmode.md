---
description: Enviado para cancelar determinados modos, como captura do mouse.
ms.assetid: c801233a-c4d8-4fd9-aaf0-3d4503bbce26
title: Mensagem de WM_CANCELMODE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23b842dfdfde7dc550d8ec6d942bcc83ea25f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807844"
---
# <a name="wm_cancelmode-message"></a>\_Mensagem de cancelamento do WM

Enviado para cancelar determinados modos, como captura do mouse. Por exemplo, o sistema envia essa mensagem para a janela ativa quando uma caixa de diálogo ou caixa de mensagem é exibida. Determinadas funções também enviam essa mensagem explicitamente para a janela especificada, independentemente de ser a janela ativa. Por exemplo, a função [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) envia essa mensagem ao desabilitar a janela especificada.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_CANCELMODE                   0x001F
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **LRESULT**

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

Quando a mensagem de **\_ cancelamento do WM** é enviada, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) cancela o processamento interno da entrada da barra de rolagem padrão, cancela o processamento do menu interno e libera a captura do mouse.

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

[**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

[**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
