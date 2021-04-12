---
title: Código de notificação de NM_RDBLCLK (barra de ferramentas) (commctrl. h)
description: Notifica uma janela pai do controle que o usuário clicou duas vezes com o botão direito do mouse dentro do controle. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 0281a687-3f1c-4fc1-bf1d-19c7ac920cd3
keywords:
- Código de notificação de NM_RDBLCLK (barra de ferramentas) controles do Windows
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec2129b6400c60bd59e441ff8af2083e781ba22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455659"
---
# <a name="nm_rdblclk-toolbar-notification-code"></a>\_Código de notificação nm RDBLCLK (barra de ferramentas)

Notifica uma janela pai do controle que o usuário clicou duas vezes com o botão direito do mouse dentro do controle. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
NM_RDBLCLK

    lpnmmouse = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contém informações sobre este código de notificação. Se o mouse tiver sido clicado em um item da barra de ferramentas, o membro **dwItemSpec** conterá o identificador de item e o membro **dwItemData** conterá os dados do item. Se o mouse tiver sido clicado em um separador ou espaço em branco na barra de ferramentas, o membro **dwItemSpec** conterá-1.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **false** para permitir que o controle Toolbar execute o processamento padrão do evento ou **true** para impedir que o controle processe o evento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





