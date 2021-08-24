---
title: BCN_HOTITEMCHANGE de notificação (Commctrl.h)
description: Notifica o proprietário do controle de botão de que o mouse está inserindo ou deixando a área do cliente do controle de botão. O controle de botão envia esse código de notificação na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 92882e21-b69d-4326-94e9-ae69a0d00a83
keywords:
- BCN_HOTITEMCHANGE código de notificação Windows Controles
topic_type:
- apiref
api_name:
- BCN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6966978dc1d1eee1d84a9e5caa51116ccb96e098d2c196ea143051663abbf4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921366"
---
# <a name="bcn_hotitemchange-notification-code"></a>Código de \_ notificação BCN HOTITEMCHANGE

Notifica o proprietário do controle de botão de que o mouse está inserindo ou deixando a área do cliente do controle de botão. O controle de botão envia esse código de notificação na forma de uma [**mensagem WM \_ NOTIFY.**](wm-notify.md)


```C++
BCN_HOTITEMCHANGE

    pnmbchotitem = (NMBCHOTITEM*) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura NMBCHOTITEM.**](/windows/win32/api/commctrl/ns-commctrl-nmbchotitem)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

> [!Note]  
> Para usar esse código de notificação, você deve fornecer um manifesto especificando Comclt32.dll versão 6.0. Para obter mais informações sobre manifestos, consulte [Habilitando estilos visuais.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





