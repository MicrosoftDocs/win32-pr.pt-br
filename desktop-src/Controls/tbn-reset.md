---
title: TBN_RESET código de notificação (commctrl. h)
description: Notifica a janela pai da barra de ferramentas que o usuário redefiniu o conteúdo da caixa de diálogo Personalizar barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 55efba85-b453-48b9-83df-76820249e7a8
keywords:
- TBN_RESET código de notificação Windows controles
topic_type:
- apiref
api_name:
- TBN_RESET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7852ee64dcf741dd291965e86d3d73f6113c1c8270bfa948d8d547fa99b9c01
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876616"
---
# <a name="tbn_reset-notification-code"></a>\_Código de notificação de redefinição de tbn

Notifica a janela pai da barra de ferramentas que o usuário redefiniu o conteúdo da caixa de diálogo Personalizar barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TBN_RESET 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações sobre o código de notificação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorne TBNRF \_ ENDcustomizate para fechar a caixa de diálogo Personalizar barra de ferramentas. Todos os outros valores de retorno são ignorados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





