---
title: WM_PARENTNOTIFY mensagem
description: Enviado para uma janela quando ocorre uma ação significativa em uma janela descendente.
ms.assetid: 4bdc37da-227c-4be1-bf0b-99704caa1444
keywords:
- WM_PARENTNOTIFY mensagens de entrada e notificações
topic_type:
- apiref
api_name:
- WM_PARENTNOTIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5de0845f906e72a42fa8d9a290c6cd8ac16cc0e96cae21ac25b3e9d7810309e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829566"
---
# <a name="wm_parentnotify-message"></a>WM_PARENTNOTIFY mensagem

Enviado para uma janela quando ocorre uma ação significativa em uma janela descendente. Essa mensagem agora é estendida para incluir o [**WM_POINTERDOWN**](wm-pointerdown.md) evento. Quando a janela filho está sendo criada, o sistema envia WM_PARENTNOTIFY [**antes**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) que a função [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) que cria a janela retorne. Quando a janela filho está sendo destruída, o sistema envia a mensagem antes de qualquer processamento para destruir a janela.

Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

> \[! Importante\]  
> Os aplicativos da área de trabalho devem estar cientes de DPI. Se o aplicativo não estiver ciente de DPI, as coordenadas de tela contidas em mensagens de ponteiro e estruturas relacionadas poderão aparecer imprecisas devido à virtualização de DPI. A virtualização de DPI oferece suporte de dimensionamento automático para aplicativos que não têm conhecimento de DPI e estão ativos por padrão (os usuários podem desativar). Para obter mais informações, consulte [Escrevendo aplicativos Win32 de alto DPI.](/previous-versions//dd464660(v=vs.85))

 


```C++
#define WM_PARENTNOTIFY             0x0210
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A palavra de ordem baixa *de wParam* especifica o evento para o qual o pai está sendo notificado. O valor da palavra de ordem alta depende do valor da palavra de ordem baixa. Esse parâmetro pode usar um dos valores a seguir.



| LOWORD(*wParam*)                                                                                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WM_CREATE"></span><span id="wm_create"></span><dl> <dt>**WM_CREATE**</dt> <dt>0x0001</dt> </dl>                | A janela filho está sendo criada.<br/> HIWORD(*wParam*) é o identificador da janela filho.<br/> *lParam* é um handle para a janela filho.<br/>                                                                                                                                                                                                                          |
| <span id="WM_DESTROY"></span><span id="wm_destroy"></span><dl> <dt>**WM_DESTROY**</dt> <dt>0x0002</dt> </dl>             | A janela filho está sendo destruída.<br/> HIWORD(*wParam*) é o identificador da janela filho.<br/> *lParam* é um handle para a janela filho.<br/>                                                                                                                                                                                                                        |
| <span id="WM_LBUTTONDOWN"></span><span id="wm_lbuttondown"></span><dl> <dt>**WM_LBUTTONDOWN**</dt> <dt>0x0201</dt> </dl> | O usuário colocou o cursor sobre a janela filho e clicou no botão esquerdo do mouse.<br/> HIWORD(*wParam*) é indefinido.<br/> *lParam* é a coordenada X do cursor é a palavra de ordem baixa e a coordenada y do cursor é a palavra de ordem alta.<br/>                                                                                                       |
| <span id="WM_MBUTTONDOWN"></span><span id="wm_mbuttondown"></span><dl> <dt>**WM_MBUTTONDOWN**</dt> <dt>0x0207</dt> </dl> | O usuário colocou o cursor sobre a janela filho e clicou no botão do meio do mouse.<br/> HIWORD(*wParam*) é indefinido.<br/> *lParam* é a coordenada X do cursor é a palavra de ordem baixa e a coordenada y do cursor é a palavra de ordem alta.<br/>                                                                                                     |
| <span id="WM_RBUTTONDOWN"></span><span id="wm_rbuttondown"></span><dl> <dt>**WM_RBUTTONDOWN**</dt> <dt>0x0204</dt> </dl> | O usuário colocou o cursor sobre a janela filho e clicou no botão direito do mouse.<br/> HIWORD(*wParam*) é indefinido.<br/> *lParam* é a coordenada X do cursor é a palavra de ordem baixa e a coordenada y do cursor é a palavra de ordem alta.<br/>                                                                                                      |
| <span id="WM_XBUTTONDOWN"></span><span id="wm_xbuttondown"></span><dl> <dt>**WM_XBUTTONDOWN**</dt> <dt>0x020B</dt> </dl> | O usuário colocou o cursor sobre a janela filho e clicou no primeiro ou segundo botão X.<br/> HIWORD(*wParam*) indica qual botão foi pressionado. Esse parâmetro pode ser um dos seguintes valores: XBUTTON1 ou XBUTTON2.<br/> *lParam* é a coordenada X do cursor é a palavra de ordem baixa e a coordenada y do cursor é a palavra de ordem alta.<br/> |
| <span id="WM_POINTERDOWN"></span><span id="wm_pointerdown"></span><dl> <dt>**WM_POINTERDOWN**</dt> <dt>0x0246</dt> </dl> | Um ponteiro fez contato com a janela filho.<br/> HIWORD(*wParam*) contém o identificador do ponteiro que gerou o [**WM_POINTERDOWN**](wm-pointerdown.md) evento.<br/>                                                                                                                                                                                            |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Contém o local do ponto do ponteiro.

> [!Note]  
> Como o ponteiro pode fazer contato com o dispositivo em uma área não trivial, esse local de ponto pode ser uma simplificação de uma área de ponteiro mais complexa. Sempre que possível, um aplicativo deve usar as informações completas da área do ponteiro em vez do local do ponto.

 

Use as macros a seguir para recuperar as coordenadas de tela física do ponto.

-   [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): a coordenada x (ponto horizontal).
-   [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): a coordenada y (ponto vertical).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o aplicativo processa essa mensagem, ele retorna zero.

Se o aplicativo não processar essa mensagem, ele chamará [**DefWindowProc.**](/windows/win32/api/winuser/nf-winuser-defwindowproca)

## <a name="remarks"></a>Comentários

Essa mensagem também é enviada para todas as janelas ancestrais da janela filho, incluindo a janela de nível superior.

Todas as janelas filho, exceto aquelas que têm **o** WS_EX_NOPARENTNOTIFY de janela estendida, enviam essa mensagem para suas janelas pai. Por padrão, as janelas filho em uma caixa de diálogo têm o estilo **WS_EX_NOPARENTNOTIFY,** a menos que a função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) seja chamada para criar a janela filho sem esse estilo.

Essa notificação fornece às janelas ancestrais da janela filho uma oportunidade de examinar as informações do ponteiro e, se necessário, capturar o ponteiro usando as funções de captura de ponteiro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                               |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mensagens](messages.md)
</dt> <dt>

[**Createwindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**Createwindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[**Hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**Loword**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**Wm_create**](../winmsg/wm-create.md)
</dt> <dt>

[**Wm_destroy**](../winmsg/wm-destroy.md)
</dt> <dt>

[**WM_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md)
</dt> <dt>

[**WM_MBUTTONDOWN**](../inputdev/wm-mbuttondown.md)
</dt> <dt>

[**Wm_rbuttondown**](../inputdev/wm-rbuttondown.md)
</dt> <dt>

[**WM_XBUTTONDOWN**](../inputdev/wm-xbuttondown.md)
</dt> </dl>

 

