---
title: EN_OLEOPFAILED de notificação (Richedit.h)
description: Notifica a janela pai de um controle de edição rich que uma ação do usuário em um objeto COM (Component Object Model) falhou. Um controle de edição rich envia esse código de notificação na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: b674c36f-2454-473e-8e1c-368c0afd8c34
keywords:
- EN_OLEOPFAILED código de notificação Windows Controles
topic_type:
- apiref
api_name:
- EN_OLEOPFAILED
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0391bfc61ff9350758ac81ff6f54fb1cff61d0dd1ebbcb2b8ef02ada9fe3fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436676"
---
# <a name="en_oleopfailed-notification-code"></a>Código \_ de notificação EN OLEOPFAILED

Notifica a janela pai de um controle de edição rich que uma ação do usuário em um objeto COM (Component Object Model) falhou. Um controle de edição rich envia esse código de notificação na forma de uma [**mensagem WM \_ NOTIFY.**](wm-notify.md)


```C++
EN_OLEOPFAILED

    penOleOpFailed = (ENOLEOPFAILED *) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Uma [**estrutura ENOLEOPFAILED**](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed) que contém informações sobre a falha.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse código de notificação retorna zero.

## <a name="remarks"></a>Comentários

A janela pai sempre receberá uma mensagem [**WM \_ NOTIFY**](wm-notify.md) para esse evento, não requer uma máscara de notificação enviada com [**EM \_ SETEVENTMASK**](em-seteventmask.md).

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

[**ENOLEOPFAILED**](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed)
</dt> </dl>

 

 





