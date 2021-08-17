---
title: EN_UPDATE de notificação (Winuser.h)
description: Enviado quando um controle de edição está prestes a redesenhar a si mesmo.
ms.assetid: 59138736-6cc9-4a3f-95f3-ada9cbf253cb
keywords:
- EN_UPDATE código de notificação Windows Controles
topic_type:
- apiref
api_name:
- EN_UPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c126122336fd878dda633620c395cb86c112de1f5dc89e8e25d2c4e08bd93ebd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436418"
---
# <a name="en_update-notification-code"></a>Código de notificação EN \_ UPDATE

Enviado quando um controle de edição está prestes a redesenhar a si mesmo. Esse código de notificação é enviado depois que o controle formatado o texto, mas antes de exibir o texto. Isso possibilita reessar a janela de controle de edição, se necessário. A janela pai do controle de edição recebe esse código de notificação por meio de uma [**mensagem WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
EN_UPDATE

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

**Rich Edit 1.0:** Para receber códigos de notificação EN \_ UPDATE, especifique [**ENM \_ UPDATE**](rich-edit-control-event-mask-flags.md) na máscara enviada com a [**mensagem EM \_ SETEVENTMASK.**](em-seteventmask.md)

**Edição Rich 2.0 e posterior:** O [**sinalizador UPDATE \_ ENM**](rich-edit-control-event-mask-flags.md) é ignorado. O código de notificação EN \_ UPDATE sempre é recebido. No entanto, quando o Microsoft Rich Edit 3.0 emula o Microsoft Rich Edit 1.0, para receber códigos de notificação EN UPDATE, você deve especificar ENM UPDATE na máscara enviada com a mensagem \_ [**EM \_ SETEVENTMASK.**](em-seteventmask.md) **\_**

Para obter informações sobre a compatibilidade de versões de edição rich com as várias versões do sistema, consulte [Sobre controles de edição rich](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[EN \_ CHANGE](en-change.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

