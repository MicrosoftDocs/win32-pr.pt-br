---
title: PGN_CALCSIZE de notificação (Commctrl.h)
description: Enviado por um controle de pager para obter as dimensões roláveis da janela contida.
ms.assetid: a15f4191-2f26-4139-bdaf-bab219449b78
keywords:
- PGN_CALCSIZE código de notificação Windows Controles
topic_type:
- apiref
api_name:
- PGN_CALCSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c2f6da5153457a871918afea60ac1251496454831a09426f16579ac47342406
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078870"
---
# <a name="pgn_calcsize-notification-code"></a>Código de \_ notificação CALCSIZE DO PGN

Enviado por um controle de pager para obter as dimensões roláveis da janela contida. Essas dimensões são usadas pelo controle pager para determinar o tamanho rolável da janela contida. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
PGN_CALCSIZE

    lpnmcs = (LPNMPGCALCSIZE) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) que contém e recebe informações sobre o código de notificação. O **membro dwFlag** dessa estrutura indica qual dimensão está sendo calculada. Dependendo do valor **de dwFlag**, você deve colocar a dimensão desejada no **membro iWidth** ou **iHeight** dessa estrutura.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





