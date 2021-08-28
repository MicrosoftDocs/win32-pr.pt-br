---
title: Código de notificação de NM_DBLCLK (barra de ferramentas) (commctrl. h)
description: Notifica a janela pai de um controle ToolBar que o usuário clicou duas vezes com o botão esquerdo do mouse dentro do controle. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: c6198245-cfd4-4e1f-877d-94c1d47e09d2
keywords:
- código de notificação de NM_DBLCLK (barra de ferramentas) Windows controles
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75abaf61938fbf377dbe8b6c5eaca99ff5ab027abe08c670de72a218dd51f1b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919656"
---
# <a name="nm_dblclk-toolbar-notification-code"></a>\_Código de notificação nm DBLCLK (barra de ferramentas)

Notifica a janela pai de um controle ToolBar que o usuário clicou duas vezes com o botão esquerdo do mouse dentro do controle. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
NM_DBLCLK

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

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





