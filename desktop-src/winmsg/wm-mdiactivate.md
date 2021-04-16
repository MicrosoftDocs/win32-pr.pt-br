---
description: Um aplicativo envia a mensagem do WM \_ MDIACTIVATE para uma janela de cliente MDI (interface de vários documentos) para instruir a janela do cliente a ativar uma janela filho MDI diferente.
ms.assetid: c5de18b5-fac3-4e55-9eca-3b6672df0e7b
title: Mensagem de WM_MDIACTIVATE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b240c41d3b7127a5d69b855f3a5587e194b02d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751346"
---
# <a name="wm_mdiactivate-message"></a>Mensagem do WM \_ MDIACTIVATE

Um aplicativo envia a mensagem do **WM \_ MDIACTIVATE** para uma janela de cliente MDI (interface de vários documentos) para instruir a janela do cliente a ativar uma janela filho MDI diferente.


```C++
#define WM_MDIACTIVATE                  0x0222
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para a janela filho MDI a ser ativado.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **LRESULT**

Se um aplicativo enviar essa mensagem para uma janela de cliente do MDI, o valor de retorno será zero.

Uma janela filho MDI deve retornar zero se ela processar essa mensagem.

## <a name="remarks"></a>Comentários

À medida que a janela do cliente processa essa mensagem, ela envia o **WM \_ MDIACTIVATE** para a janela filho que está sendo desativada e para a janela filho que está sendo ativada. Os parâmetros de mensagem recebidos por uma janela filho MDI são os seguintes:

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Um identificador para a janela filho MDI que está sendo desativada.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Um identificador para a janela filho MDI que está sendo ativada.

</dd> </dl>

Uma janela filho MDI é ativada independentemente da janela do quadro MDI. Quando a janela do quadro se torna ativa, a janela filho ativada pela última vez usando a mensagem do **WM \_ MDIACTIVATE** recebe a mensagem do [**WM \_ NCACTIVATE**](wm-ncactivate.md) para desenhar um quadro de janela ativa e uma barra de título; a janela filho não recebe outra mensagem do **WM \_ MDIACTIVATE** .

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

[**MDIGETACTIVE do WM \_**](wm-mdigetactive.md)
</dt> <dt>

[**MDINEXT do WM \_**](wm-mdinext.md)
</dt> <dt>

[**NCACTIVATE do WM \_**](wm-ncactivate.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Interface de vários documentos](multiple-document-interface.md)
</dt> </dl>

 

 




