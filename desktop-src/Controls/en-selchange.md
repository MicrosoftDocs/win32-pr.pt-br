---
title: EN_SELCHANGE de notificação (Richedit.h)
description: Notifica a janela pai de um controle de edição rich que a seleção atual foi alterada. Um controle de edição rich envia esse código de notificação na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 53d47b53-a73c-4652-889c-2374f8e99382
keywords:
- EN_SELCHANGE código de notificação Windows Controles
topic_type:
- apiref
api_name:
- EN_SELCHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9a2398abd5058f57eeef6ad73f559a723e7df29315d38dfc9794a707740c89f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047416"
---
# <a name="en_selchange-notification-code"></a>Código \_ de notificação EN SELCHANGE

Notifica a janela pai de um controle de edição rich que a seleção atual foi alterada. Um controle de edição rich envia esse código de notificação na forma de uma [**mensagem WM \_ NOTIFY.**](wm-notify.md)


```C++
EN_SELCHANGE

    pSelChange = (SELCHANGE *) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Uma [**estrutura SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange) que recebe informações sobre a seleção.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse código de notificação não retorna um valor.

## <a name="remarks"></a>Comentários

Para receber códigos de notificação EN \_ SELCHANGE, especifique [**ENM \_ SELCHANGE**](rich-edit-control-event-mask-flags.md) na máscara enviada com a [**mensagem EM \_ SETEVENTMASK.**](em-seteventmask.md)

Esse código de notificação é enviado quando a posição do acidade muda e nenhum texto é selecionado (a seleção está vazia). A posição do cursor pode mudar quando o usuário clica no mouse, digita ou pressiona uma tecla de seta.

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

[**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange)
</dt> <dt>

[**WM \_ NOTIFY**](wm-notify.md)
</dt> </dl>

 

 





