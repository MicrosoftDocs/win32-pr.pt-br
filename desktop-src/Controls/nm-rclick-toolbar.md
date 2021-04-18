---
title: Código de notificação de NM_RCLICK (barra de ferramentas) (commctrl. h)
description: Enviado por um controle Toolbar quando o usuário clica na barra de ferramentas com o botão direito do mouse. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: e9d2d871-e922-444d-a76c-e73f249ed410
keywords:
- Código de notificação de NM_RCLICK (barra de ferramentas) controles do Windows
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6464c30a031aa55aef94bccd3ab852720fb14403
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749307"
---
# <a name="nm_rclick-toolbar-notification-code"></a>\_Código de notificação nm RCLICK (barra de ferramentas)

Enviado por um controle Toolbar quando o usuário clica na barra de ferramentas com o botão direito do mouse. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
NM_RCLICK

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



 

 





