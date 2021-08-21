---
title: NM_OUTOFMEMORY de notificação (Commctrl.h)
description: Notifica a janela pai de um controle de que o controle não pôde concluir uma operação porque não havia memória suficiente disponível. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: d7d80515-ae6c-4817-a698-d486a9d86c4a
keywords:
- NM_OUTOFMEMORY código de notificação Windows Controles
topic_type:
- apiref
api_name:
- NM_OUTOFMEMORY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8a2efdd0048006b86d97964dc953d2dbd7c4ecb2687b3c0fb67a5effc63fea0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958105"
---
# <a name="nm_outofmemory-notification-code"></a>Código de \_ notificação OUTOFMEMORY NM

Notifica a janela pai de um controle de que o controle não pôde concluir uma operação porque não havia memória suficiente disponível. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_OUTOFMEMORY

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre essa notificação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado pelo controle .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





