---
title: EN_CHANGE de notificação (Winuser.h)
description: Enviado quando o usuário tiver feito uma ação que pode ter alterado o texto em um controle de edição.
ms.assetid: 8a04e6fb-ae9d-4d94-8047-6de96df899f5
keywords:
- EN_CHANGE código de notificação Windows Controles
topic_type:
- apiref
api_name:
- EN_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86dbfb90376a85df09cad854882fa2616e6b7cb247cab4106850608a4b96ad4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437046"
---
# <a name="en_change-notification-code"></a>Código de \_ notificação EN CHANGE

Enviado quando o usuário tiver feito uma ação que pode ter alterado o texto em um controle de edição. Ao contrário do código de notificação [EN \_ UPDATE,](en-update.md) esse código de notificação é enviado depois que o sistema atualiza a tela. A janela pai do controle de edição recebe esse código de notificação por meio de uma [**mensagem WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
EN_CHANGE

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

**Edição rica:** Com suporte no Microsoft Rich Edit 1.0 e posterior. Para receber códigos \_ de notificação EN CHANGE, especifique [**ENM \_ CHANGE**](rich-edit-control-event-mask-flags.md) na máscara enviada com a [**mensagem EM \_ SETEVENTMASK.**](em-seteventmask.md) Para obter informações sobre a compatibilidade de versões de edição rich com as várias versões do sistema, consulte [Sobre controles de edição rich](about-rich-edit-controls.md).

O código de notificação EN CHANGE não é enviado quando o estilo \_ [**\_ MULTILINE do ES**](edit-control-styles.md) é usado e o texto é enviado por [**meio de WM \_ SETTEXT.**](/windows/desktop/winmsg/wm-settext)

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

[EN \_ UPDATE](en-update.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

