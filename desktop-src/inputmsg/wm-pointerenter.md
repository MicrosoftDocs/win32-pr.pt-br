---
title: WM_POINTERENTER mensagem
description: Enviado a uma janela quando um novo ponteiro entra no intervalo de detecção na janela (focalizado) ou quando um ponteiro existente se move dentro dos limites da janela.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8a0222
keywords:
- Mensagens de entrada e notificações de WM_POINTERENTER mensagem
topic_type:
- apiref
api_name:
- WM_POINTERENTER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 4d0f6304408514390bb40f2d0e78a766f9e2d118
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105765998"
---
# <a name="wm_pointerenter-message"></a>WM_POINTERENTER mensagem

Enviado a uma janela quando um novo ponteiro entra no intervalo de detecção na janela (focalizado) ou quando um ponteiro existente se move dentro dos limites da janela.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

> \[! Fundamental\]  
> Os aplicativos da área de trabalho devem ter reconhecimento de DPI. Se seu aplicativo não tiver reconhecimento de DPI, as coordenadas de tela contidas nas mensagens de ponteiro e estruturas relacionadas poderão parecer imprecisas devido à virtualização de DPI. A virtualização de DPI fornece suporte de dimensionamento automático para aplicativos que não têm reconhecimento de DPI e está ativo por padrão (os usuários podem desativá-lo). Para obter mais informações, consulte [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_POINTERENTER                 0x0249
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contém o identificador de ponteiro e informações adicionais. Use as macros a seguir para recuperar informações específicas no parâmetro wParam.

-   [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): o identificador do ponteiro.
-   [**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indica se esta mensagem é a primeira mensagem gerada por um novo ponteiro inserindo intervalo de detecção (focalizado).
-   [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indica se esta mensagem foi gerada por um ponteiro que não tem o intervalo de detecção restante. Esse sinalizador é sempre definido para mensagens de **WM_POINTERENTER** .
-   [**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um sinalizador que indica se esta mensagem foi gerada por um ponteiro que está em contato. Este sinalizador não está definido para um ponteiro no intervalo de detecção (focalizar).

</dd> <dt>

*lParam* 
</dt> <dd>

Contém o local do ponto do ponteiro.

> [!Note]  
> Como o ponteiro pode fazer contato com o dispositivo em uma área não trivial, esse local de ponto pode ser uma simplificação de uma área de ponteiro mais complexa. Sempre que possível, um aplicativo deve usar as informações completas da área do ponteiro em vez do local do ponto.

 

Use as macros a seguir para recuperar as coordenadas de tela física do ponto.

-   [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): a coordenada X (ponto horizontal).
-   [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): a coordenada Y (ponto vertical).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

Se o aplicativo não processar essa mensagem, ele deverá chamar [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Comentários

A notificação de **WM_POINTERENTER** pode ser usada por uma janela para fornecer comentários ao usuário enquanto o ponteiro está sobre sua superfície ou para reagir à presença de um ponteiro sobre sua superfície.

Essa notificação é enviada somente para a janela que está recebendo entrada para o ponteiro. A tabela a seguir lista algumas das situações em que essa notificação é enviada.



| Ação                                                   | Conjunto de sinalizadores                                                                                                                                         | Notificações enviadas para                                 |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| Um novo ponteiro entra no intervalo de detecção (focalizado).            | [**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)<br/> [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)<br/> | Janela sobre a qual o ponteiro entra no intervalo de detecção. |
| Um ponteiro em foco cruza dentro dos limites da janela. | [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)<br/>                                                                      | Janela dentro da qual o ponteiro foi cruzado.          |



 

> \[! Fundamental\]  
> Quando uma janela perde a captura de um ponteiro e recebe a notificação de [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) , ela normalmente não receberá notificações adicionais. Por esse motivo, é importante que você não faça nenhuma suposição com base em WM_POINTERDOWN igualmente emparelhadas [](wm-pointerdown.md) / [**WM_POINTERUP**](wm-pointerup.md) ou **WM_POINTERENTER** / notificações de [**WM_POINTERLEAVE**](wm-pointerleave.md) .

 

Quando as entradas vêm do mouse, como resultado da integração de mensagens de ponteiro e mouse, **WM_POINTERENTER** não é enviada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mensagens](messages.md)
</dt> <dt>

**Referência**
</dt> <dt>

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

