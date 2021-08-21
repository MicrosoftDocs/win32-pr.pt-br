---
title: WM_CTLCOLORLISTBOX mensagem (Winuser.h)
description: Enviado para a janela pai de uma caixa de listagem antes que o sistema desenhe a caixa de listagem. Ao responder a essa mensagem, a janela pai pode definir as cores do texto e da tela de fundo da caixa de listagem usando o guidão de contexto do dispositivo de exibição especificado.
ms.assetid: e128e77f-e966-44c4-9f0e-efcf421b6c82
keywords:
- WM_CTLCOLORLISTBOX controles Windows mensagem
topic_type:
- apiref
api_name:
- WM_CTLCOLORLISTBOX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1713c7251dfe837d5796b708fa5b77f0aa5e372c031c251199cb871dbd7c5608
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077660"
---
# <a name="wm_ctlcolorlistbox-message"></a>Mensagem WM \_ CTLCOLORLISTBOX

Enviado para a janela pai de uma caixa de listagem antes que o sistema desenhe a caixa de listagem. Ao responder a essa mensagem, a janela pai pode definir as cores do texto e da tela de fundo da caixa de listagem usando o guidão de contexto do dispositivo de exibição especificado.


```C++
WM_CTLCOLORLISTBOX

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Lidar com o contexto do dispositivo para a caixa de listagem.

</dd> <dt>

*lParam* 
</dt> <dd>

Lidar com a caixa de listagem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se um aplicativo processa essa mensagem, ele deve retornar um alça para um pincel. O sistema usa o pincel para pintar a plano de fundo da caixa de listagem.

## <a name="remarks"></a>Comentários

Por padrão, a [**função DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleciona as cores padrão do sistema para a caixa de listagem.

A **mensagem WM \_ CTLCOLORLISTBOX** nunca é enviada entre threads. Ele é enviado somente dentro de um thread.

Se um procedimento de caixa de diálogo tratar essa mensagem, ele deverá lançar o valor de retorno desejado para um **\_ PTR INT** e retornar o valor diretamente. Se o procedimento da caixa de diálogo retornar **FALSE,** o tratamento de mensagens padrão será executado. O **valor \_ MSGRESULT** do DWL definido pela função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) é ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Outros recursos**
</dt> <dt>

[**Realizepalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[**Defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

