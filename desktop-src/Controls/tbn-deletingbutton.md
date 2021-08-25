---
title: Mensagem de TBN_DELETINGBUTTON (commctrl. h)
description: Enviado por um controle Toolbar quando um botão está prestes a ser excluído. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 08116071-36d6-456b-88f9-62a22cdb7ed9
keywords:
- controles de Windows de mensagem de TBN_DELETINGBUTTON
topic_type:
- apiref
api_name:
- TBN_DELETINGBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a426d32af308d6d254a4221bbf35b103b401f07ab1ba6fa74801b6debd46ab70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876966"
---
# <a name="tbn_deletingbutton-message"></a>\_Mensagem tbn DELETINGBUTTON

Enviado por um controle Toolbar quando um botão está prestes a ser excluído. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
 TBN_DELETINGBUTTON 

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) que contém informações sobre o botão que está sendo excluído. Para este código de notificação, somente os membros **HDR** e **iItem** dessa estrutura são válidos. O membro **iItem** dessa estrutura contém o identificador de comando do botão que está sendo excluído.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





