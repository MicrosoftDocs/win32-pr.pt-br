---
title: Código de notificação de NM_LDOWN (barra de ferramentas) (commctrl. h)
description: Notifica uma janela pai da barra de ferramentas que o botão esquerdo do mouse foi pressionado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: f5b356fb-265b-4eb0-a5a3-2a22d688f847
keywords:
- código de notificação de NM_LDOWN (barra de ferramentas) Windows controles
topic_type:
- apiref
api_name:
- NM_LDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf283e8b3e0d1ed780a80d5608849bc42f200b61a5a94692c0924cb2e6241a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919646"
---
# <a name="nm_ldown-toolbar-notification-code"></a>\_Código de notificação nm LDOWN (barra de ferramentas)

Notifica uma janela pai da barra de ferramentas que o botão esquerdo do mouse foi pressionado. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
NM_LDOWN

    lpnmmouse = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contém informações sobre este código de notificação. Se o mouse tiver sido clicado em um item da barra de ferramentas, o membro **dwItemSpec** conterá o identificador de item e o membro **dwItemData** conterá os dados do item. Se o mouse tiver sido clicado em um separador ou espaço em branco na barra de ferramentas, o membro **dwItemSpec** conterá-1.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **false** para permitir que o controle Toolbar execute o processamento padrão do evento ou **true** para impedir que o controle processe o evento.

## <a name="remarks"></a>Comentários

Essa notificação é enviada após o código de notificação do [tbn \_ DROPDOWN](tbn-dropdown.md) ser enviado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





