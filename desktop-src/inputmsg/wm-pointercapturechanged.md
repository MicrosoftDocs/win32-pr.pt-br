---
title: WM_POINTERCAPTURECHANGED mensagem
description: Enviado para uma janela que está perdendo a captura de um ponteiro de entrada.
ms.assetid: 6eec37da-227c-4be1-bf0b-98704caa1322
keywords:
- Mensagens de entrada e notificações de WM_POINTERCAPTURECHANGED mensagem
topic_type:
- apiref
api_name:
- WM_POINTERCAPTURECHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 768dc81be57bb61a23acab7ebea450dba577d60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105794015"
---
# <a name="wm_pointercapturechanged-message"></a>WM_POINTERCAPTURECHANGED mensagem

Enviado para uma janela que está perdendo a captura de um ponteiro de entrada.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_POINTERCAPTURECHANGED           0x024C
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contém informações sobre o ponteiro de entrada que está sendo perdido. Use [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) para obter a ID do ponteiro.

</dd> <dt>

*lParam* 
</dt> <dd>

Contém um identificador para a janela que está capturando o ponteiro de entrada. Esse valor pode ser nulo se o ponteiro não estiver mais sendo capturado pela janela.

Se essa mensagem for gerada a partir do processamento interno, o valor poderá ser o identificador da janela que recebe a mensagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

Se o aplicativo não processar essa mensagem, ele deverá chamar [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Comentários

Uma janela deve usar essa notificação para interromper o processamento de mensagens subsequentes e iniciar qualquer limpeza necessária para que o ponteiro seja perdido. O processamento de gestos associados ao ponteiro também deve ser encerrado (por exemplo, chamando [**StopInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)) e os contatos restantes associados novamente à janela.

Normalmente, se uma janela receber a notificação de **WM_POINTERCAPTURECHANGED** , não serão recebidas notificações subsequentes relacionadas ao ponteiro de entrada. Por isso, não dependa de notificações emparelhadas, como [**WM_POINTERENTER**](wm-pointerenter.md) e [**WM_POINTERLEAVE**](wm-pointerleave.md).

**WM_POINTERCAPTURECHANGED** não inclui dados de [**POINTER_INFO**](/previous-versions/windows/desktop/api) . Além do sinalizador de [**POINTER_FLAG_CAPTURECHANGED**](pointer-flags-contants.md) que está sendo definido, os dados retornados por [**GetPointerInfo**](/previous-versions/windows/desktop/api) (ou qualquer variante) são idênticos aos retornados antes da notificação.

Se o aplicativo não processar essa notificação, o [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) poderá gerar uma ou mais mensagens de [**WM_GESTURE**](../wintouch/wm-gesture.md) ou, se um gesto não for reconhecido, o **DefWindowProc** poderá gerar a entrada do mouse.

Se um aplicativo consumir seletivamente alguma entrada de ponteiro e passar o resto para [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), o comportamento resultante será indefinido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mensagens](messages.md)
</dt> </dl>

 

