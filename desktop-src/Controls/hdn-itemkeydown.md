---
title: HDN_ITEMKEYDOWN de notificação (Commctrl.h)
description: Notifica a janela pai de um controle de header de que uma chave foi pressionada com um item selecionado. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: ab6922ab-907d-44fc-8606-28f395118405
keywords:
- HDN_ITEMKEYDOWN de notificação Windows Controles
topic_type:
- apiref
api_name:
- HDN_ITEMKEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 473222e6cd0da7fd886571db045ee91ea6d8c46ce6bcc20e141af837d5aa92e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435426"
---
# <a name="hdn_itemkeydown-notification-code"></a>Código de \_ notificação ITEMKEYDOWN do HDN

Notifica a janela pai de um controle de header de que uma chave foi pressionada com um item selecionado. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
HDN_ITEMKEYDOWN

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contém informações adicionais sobre a chave que está sendo pressionada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





