---
title: EN_VSCROLL de notificação (Winuser.h)
description: Enviado quando o usuário clica na barra de rolagem vertical de um controle de edição ou quando o usuário rola a roda do mouse sobre o controle de edição.
ms.assetid: 46307dee-3c5c-4020-9c2b-ec4638a0cea5
keywords:
- EN_VSCROLL código de notificação Windows Controles
topic_type:
- apiref
api_name:
- EN_VSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c716ecb36c0d27b445446a30eb0a026edf3fd88641f469e50daef1763cd6ca66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047376"
---
# <a name="en_vscroll-notification-code"></a>Código de \_ notificação do EN VSCROLL

Enviado quando o usuário clica na barra de rolagem vertical de um controle de edição ou quando o usuário rola a roda do mouse sobre o controle de edição. A janela pai do controle de edição recebe esse código de notificação por meio de uma [**mensagem WM \_ COMMAND.**](/windows/desktop/menurc/wm-command) A janela pai é notificada antes que a tela seja atualizada.


```C++
EN_VSCROLL

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador do controle de edição. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.

</dd> <dt>

*lParam* 
</dt> <dd>

Um alça para o controle de edição.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa mensagem é enviada para os seguintes eventos do mouse na barra de rolagem vertical: clicando no botão de seta ou clicando entre o botão de seta e o polegar. No entanto, a mensagem não é enviada ao clicar no mouse da barra de rolagem em si. A mensagem também é enviada quando um evento de teclado causa uma alteração na área de exibição do controle de edição, por exemplo, pressionando HOME, END, PAGE UP, PAGE DOWN, SETA PARA CIMA ou SETA PARA BAIXO.

A roda do mouse é um mouse que tem uma roda central que rola. Para obter mais informações, consulte "A roda do mouse" em [Sobre a entrada do mouse.](/windows/desktop/inputdev/about-mouse-input)

**Edição rica:** Com suporte no Microsoft Rich Edit 1.0 e posterior. Para receber códigos de \_ notificação en VSCROLL, especifique [**ENM \_ SCROLL**](rich-edit-control-event-mask-flags.md) na máscara enviada com a [**mensagem EM \_ SETEVENTMASK.**](em-seteventmask.md) Para obter informações sobre a compatibilidade de versões de edição rich com as várias versões do sistema, consulte [Sobre controles de edição rich](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[EN \_ HSCROLL](en-hscroll.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Usando editar controles](using-edit-controls.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

