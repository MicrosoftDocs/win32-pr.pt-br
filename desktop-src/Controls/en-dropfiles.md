---
title: EN_DROPFILES de notificação (Richedit.h)
description: Notifica uma janela pai de controle de edição rica que o usuário está tentando soltar arquivos no controle. Um controle de edição avançado envia esse código de notificação na forma de uma mensagem WM NOTIFY quando recebe a \_ mensagem WM \_ DROPFILES.
ms.assetid: fcae0ff8-ce37-4c71-b14c-cbd6429b4ab3
keywords:
- EN_DROPFILES código de notificação Windows Controles
topic_type:
- apiref
api_name:
- EN_DROPFILES
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8813d3d62883ab607bb898f4aa34a664cbab47b2c8214fbd83fc8cc7913e26ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047776"
---
# <a name="en_dropfiles-notification-code"></a>Código de notificação EN \_ DROPFILES

Notifica uma janela pai de controle de edição rica que o usuário está tentando soltar arquivos no controle. Um controle de edição avançado envia esse código de notificação na forma de uma mensagem [**WM \_ NOTIFY**](wm-notify.md) quando recebe a mensagem [**WM \_ DROPFILES.**](/windows/desktop/shell/wm-dropfiles)


```C++
EN_DROPFILES

      penDropFiles = (ENDROPFILES *) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Uma [**estrutura ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) que recebe informações de arquivos descartados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornar um valor não zero para permitir a operação de soltar.

Retorne zero para ignorar a operação de soltar.

## <a name="remarks"></a>Comentários

Para um controle de edição avançado receber mensagens [**WM \_ DROPFILES,**](/windows/desktop/shell/wm-dropfiles) a janela pai deve registrar o controle como um destino de soltar usando a [**função DragAcceptFiles.**](/windows/desktop/api/shellapi/nf-shellapi-dragacceptfiles) O controle não se registra.

Para receber códigos de notificação EN \_ DROPFILES, especifique [**ENM \_ DROPFILES**](rich-edit-control-event-mask-flags.md) na máscara enviada com a [**mensagem EM \_ SETEVENTMASK.**](em-seteventmask.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles)
</dt> </dl>

 

