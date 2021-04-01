---
title: Mensagem de WM_CTLCOLORDLG (WinUser. h)
description: Enviado para uma caixa de diálogo antes de o sistema desenhar a caixa de diálogo. Ao responder a essa mensagem, a caixa de diálogo pode definir suas cores de texto e de plano de fundo usando o identificador de contexto do dispositivo de vídeo especificado.
ms.assetid: 5b90ab3f-b751-486f-a0fa-33f791c31a26
keywords:
- Caixas de diálogo de WM_CTLCOLORDLG mensagem
topic_type:
- apiref
api_name:
- WM_CTLCOLORDLG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 833d3894a85342b0f26323ceed0f4fb3356c48ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644313"
---
# <a name="wm_ctlcolordlg-message"></a>Mensagem do WM \_ CTLCOLORDLG

Enviado para uma caixa de diálogo antes de o sistema desenhar a caixa de diálogo. Ao responder a essa mensagem, a caixa de diálogo pode definir suas cores de texto e de plano de fundo usando o identificador de contexto do dispositivo de vídeo especificado.


```C++
#define WM_CTLCOLORDLG                  0x0136
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para o contexto do dispositivo para a caixa de diálogo.

</dd> <dt>

*lParam* 
</dt> <dd>

Um identificador para a caixa de diálogo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele deverá retornar um identificador para um pincel. O sistema usa o pincel para pintar o plano de fundo da caixa de diálogo.

## <a name="remarks"></a>Comentários

Por padrão, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleciona as cores padrão do sistema para a caixa de diálogo.

O sistema não destrói automaticamente o pincel retornado. É responsabilidade do aplicativo destruir o pincel quando ele não for mais necessário.

A mensagem do **WM \_ CTLCOLORDLG** nunca é enviada entre threads. Ele é enviado somente dentro de um thread.

Observe que a mensagem do **WM \_ CTLCOLORDLG** é enviada para a própria caixa de diálogo; todas as outras mensagens do **WM \_ CTLCOLOR \** _ são enviadas para o proprietário do controle.

Se um procedimento da caixa de diálogo tratar essa mensagem, ele deverá converter o valor de retorno desejado em um _ *int \_ PTR** e retornar o valor diretamente. Se o procedimento da caixa de diálogo retornar **false**, a manipulação de mensagens padrão será executada. O valor de **\_ MSGRESULT DWL** definido pela função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) é ignorado.

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

[**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Caixas de diálogo](dialog-boxes.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

