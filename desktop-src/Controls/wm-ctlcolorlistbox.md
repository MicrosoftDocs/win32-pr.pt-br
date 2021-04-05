---
title: Mensagem de WM_CTLCOLORLISTBOX (WinUser. h)
description: Enviado para a janela pai de uma caixa de listagem antes de o sistema desenhar a caixa de listagem. Ao responder a essa mensagem, a janela pai pode definir o texto e as cores de plano de fundo da caixa de listagem usando o identificador de contexto do dispositivo de exibição especificado.
ms.assetid: e128e77f-e966-44c4-9f0e-efcf421b6c82
keywords:
- Controles de WM_CTLCOLORLISTBOX de mensagens do Windows
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
ms.openlocfilehash: 8e949af76bd05aa9ad3a3e720c89be33cfe76ed8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085497"
---
# <a name="wm_ctlcolorlistbox-message"></a>Mensagem do WM \_ CTLCOLORLISTBOX

Enviado para a janela pai de uma caixa de listagem antes de o sistema desenhar a caixa de listagem. Ao responder a essa mensagem, a janela pai pode definir o texto e as cores de plano de fundo da caixa de listagem usando o identificador de contexto do dispositivo de exibição especificado.


```C++
WM_CTLCOLORLISTBOX

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador para o contexto do dispositivo da caixa de listagem.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador para a caixa de listagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele deverá retornar um identificador para um pincel. O sistema usa o pincel para pintar o plano de fundo da caixa de listagem.

## <a name="remarks"></a>Comentários

Por padrão, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleciona as cores padrão do sistema para a caixa de listagem.

A mensagem do **WM \_ CTLCOLORLISTBOX** nunca é enviada entre threads. Ele é enviado somente dentro de um thread.

Se um procedimento de caixa de diálogo tratar essa mensagem, ele deverá converter o valor de retorno desejado para um **int \_ PTR** e retornar o valor diretamente. Se o procedimento da caixa de diálogo retornar **false**, a manipulação de mensagens padrão será executada. O valor de **\_ MSGRESULT DWL** definido pela função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) é ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Outros recursos**
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

