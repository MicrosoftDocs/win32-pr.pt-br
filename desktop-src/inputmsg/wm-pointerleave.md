---
title: WM_POINTERLEAVE mensagem
description: Enviado para uma janela quando um ponteiro deixa o intervalo de detecção sobre a janela (passar o mouse) ou quando um ponteiro se move para fora dos limites da janela.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8c1322
keywords:
- WM_POINTERLEAVE mensagens de entrada e notificações
topic_type:
- apiref
api_name:
- WM_POINTERDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 519e354aa43cf31d0a2477aec2f50a1405b7c4a254f2641497229c14f55d4679
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964226"
---
# <a name="wm_pointerleave-message"></a>WM_POINTERLEAVE mensagem

Enviado para uma janela quando um ponteiro deixa o intervalo de detecção sobre a janela (passar o mouse) ou quando um ponteiro se move para fora dos limites da janela.

Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

> \[! Importante\]  
> Os aplicativos da área de trabalho devem estar cientes de DPI. Se o aplicativo não estiver ciente de DPI, as coordenadas de tela contidas em mensagens de ponteiro e estruturas relacionadas poderão aparecer imprecisas devido à virtualização de DPI. A virtualização de DPI oferece suporte de dimensionamento automático para aplicativos que não têm conhecimento de DPI e estão ativos por padrão (os usuários podem desativar). Para obter mais informações, consulte [Escrevendo aplicativos Win32 de alto DPI.](/previous-versions//dd464660(v=vs.85))

 


```C++
#define WM_POINTERLEAVE                 0x024A
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contém o identificador de ponteiro e informações adicionais. Use as macros a seguir para recuperar essas informações.

-   [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): o identificador de ponteiro.
-   [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indica se essa mensagem foi gerada por um ponteiro que não tem o intervalo de detecção à esquerda. Esse sinalizador não é definido quando o ponteiro sai do intervalo de detecção da janela.
-   [**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um sinalizador que indica se essa mensagem foi gerada por um ponteiro que está em contato. Esse sinalizador não está definido para um ponteiro no intervalo de detecção (foco).

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

Se um aplicativo processa essa mensagem, ele deve retornar zero.

Se o aplicativo não processar essa mensagem, ele deverá chamar [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Comentários

A **WM_POINTERLEAVE** pode ser usada por uma janela para alterar o modo ou parar comentários para o usuário enquanto o ponteiro está sobre a superfície da janela.

Essa notificação só é enviada para a janela que está recebendo entrada para o ponteiro. A tabela a seguir lista algumas das situações em que essa notificação é enviada.



| Ação                                        | Conjunto de sinalizadores                                                         | Notificações enviadas para                                |
|-----------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------|
| Um ponteiro de foco cruza os limites da janela. | [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api) | Janela fora de cujo limite o ponteiro foi movido.  |
| Um ponteiro sai do intervalo de detecção.        | N/D                                                               | Janela para a qual o ponteiro sai do intervalo de detecção. |



 

> \[! Importante\]  
> Quando uma janela perde a captura de um ponteiro e recebe a notificação [**WM_POINTERCAPTURECHANGED,**](wm-pointercapturechanged.md) ela normalmente não receberá nenhuma notificação adicional. Por esse motivo, é importante que você não faça suposições com base em notificações WM_POINTERDOWN [](wm-pointerdown.md) / [**WM_POINTERUP WM_POINTERENTER**](wm-pointerup.md) [](wm-pointerenter.md) / **WM_POINTERLEAVE** emparelhadas.

 

Se o contato for mantido com o digitalizador de entrada e o ponteiro se mover para fora da **janela,** WM_POINTERLEAVE será gerado. **WM_POINTERLEAVE** é gerado somente quando um ponteiro de foco cruza os limites da janela ou o contato é encerrado.

**WM_POINTERLEAVE** será postado na fila de mensagens postadas se a entrada for originada de um dispositivo do mouse.

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

**Referência**
</dt> <dt>

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

