---
title: WM_NCPOINTERUP mensagem
description: Postado quando um ponteiro que fez contato na área de não cliente de uma janela quebra o contato.
ms.assetid: 4bdc11da-227c-4be1-bf0b-99704caa1322
keywords:
- Mensagens de entrada e notificações de WM_NCPOINTERUP mensagem
topic_type:
- apiref
api_name:
- WM_NCPOINTERUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: a875814b51558c20de47eeee525f6dd35f716fac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644918"
---
# <a name="wm_ncpointerup-message"></a>WM_NCPOINTERUP mensagem

Postado quando um ponteiro que fez contato na área de não cliente de uma janela quebra o contato. A mensagem é direcionada para a janela sobre a qual o ponteiro faz contato e o ponteiro é, nesse ponto, implicitamente capturado para a janela para que a janela continue a receber entrada para o ponteiro até que ele interrompa o contato, incluindo a notificação de **WM_NCPOINTERUP** .

Se uma janela tiver capturado esse ponteiro, essa mensagem não será postada. Em vez disso, um [**WM_POINTERUP**](wm-pointerup.md) é Postado na janela que capturou esse ponteiro.

> \[! Fundamental\]  
> Os aplicativos da área de trabalho devem ter reconhecimento de DPI. Se seu aplicativo não tiver reconhecimento de DPI, as coordenadas de tela contidas nas mensagens de ponteiro e estruturas relacionadas poderão parecer imprecisas devido à virtualização de DPI. A virtualização de DPI fornece suporte de dimensionamento automático para aplicativos que não têm reconhecimento de DPI e está ativo por padrão (os usuários podem desativá-lo). Para obter mais informações, consulte [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_NCPOINTERUP               0x0243
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contém o identificador de ponteiro e informações adicionais. Use as macros a seguir para recuperar essas informações.

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificador de ponteiro

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): valor de teste de sucesso retornado pelo processamento da mensagem de [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) .

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

Se o aplicativo não processar essa mensagem, o [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) poderá executar uma ou mais ações do sistema, dependendo do resultado do teste de clique incluído na mensagem. Normalmente, os aplicativos não precisam lidar com essa mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Mensagens](messages.md)
</dt> </dl>

 

