---
title: Código de notificação de NM_CLICK (barra de status) (commctrl. h)
description: Notifica a janela pai de um controle de barra de status que o usuário clicou com o botão esquerdo do mouse dentro do controle. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 179ccbe9-f51f-4356-b91a-10d7e3607b09
keywords:
- NM_CLICK (barra de status) controles do Windows do código de notificação
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6066f76a8cf0b6ca34b5298cfcdcba2b11e3fa5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824854"
---
# <a name="nm_click-status-bar-notification-code"></a>\_Código de notificação de clique (barra de status) nm

Notifica a janela pai de um controle de barra de status que o usuário clicou com o botão esquerdo do mouse dentro do controle. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
NM_CLICK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contém informações adicionais sobre esta notificação. O membro **dwItemSpec** contém o índice da seção que foi clicada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornar **true** para indicar que o clique do mouse foi tratado e suprimir o processamento padrão pelo sistema. Retorne **false** para permitir o processamento padrão do clique.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





