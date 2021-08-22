---
title: EN_CORRECTTEXT de notificação (Richedit.h)
description: Notifica uma janela pai de controle de edição rica de que ocorreu um gesto SYV CORRECT, dando à janela pai a oportunidade de cancelar a \_ correção do texto. Um controle de edição rich envia esse código de notificação na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: d6f6278f-ff63-4f6a-a352-2b4d70df3e1a
keywords:
- EN_CORRECTTEXT código de notificação Windows Controles
topic_type:
- apiref
api_name:
- EN_CORRECTTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48f03bf0d1bd31cc1f4139c24c6b0efa904f013231af4e108b0f97ef7f308bbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019414"
---
# <a name="en_correcttext-notification-code"></a>Código de notificação EN \_ CORRECTTEXT

Notifica uma janela pai de controle de edição rica de que ocorreu um gesto SYV CORRECT, dando à janela pai a oportunidade de cancelar a \_ correção do texto. Um controle de edição rich envia esse código de notificação na forma de uma [**mensagem WM \_ NOTIFY.**](wm-notify.md)


```C++
EN_CORRECTTEXT

    penCorrectText = (ENCORRECTTEXT *) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Uma [**estrutura ENCORRECTTEXT**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext) que especifica a seleção a ser corrigida.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorne zero para ignorar a ação.

Retorna um valor não zero para processar a ação.

## <a name="remarks"></a>Comentários

Esse código de notificação será enviado somente se os recursos de caneta estão disponíveis.

Para receber códigos de notificação EN \_ CORRECTTEXT, especifique [**ENM \_ CORRECTTEXT**](rich-edit-control-event-mask-flags.md) na máscara enviada com a [**mensagem EM \_ SETEVENTMASK.**](em-seteventmask.md)

> [!Note]  
> O código de notificação EN \_ CORRECTTEXT só tem suporte na versão 1.0 de edição rich. Não há suporte para ele em versões posteriores do rich edit. Para obter informações sobre a compatibilidade de versões de edição rich com as várias versões do sistema, consulte [Sobre controles de edição rich](about-rich-edit-controls.md).

 

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

[**ENCORRECTTEXT**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext)
</dt> </dl>

 

 





