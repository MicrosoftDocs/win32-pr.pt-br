---
title: TBN_DRAGOUT de notificação (Commctrl.h)
description: Enviado por um controle de barra de ferramentas quando o usuário clica em um botão e, em seguida, move o cursor para fora do botão. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 3566ad60-9744-494f-bb02-d30b41d06351
keywords:
- TBN_DRAGOUT de notificação Windows Controles
topic_type:
- apiref
api_name:
- TBN_DRAGOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad707fa357a487e271bbe03039745b97521542a1305f9745a71a56044060c950
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077940"
---
# <a name="tbn_dragout-notification-code"></a>Código de notificação \_ do TBN DRAGOUT

Enviado por um controle de barra de ferramentas quando o usuário clica em um botão e, em seguida, move o cursor para fora do botão. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_DRAGOUT

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) que contém informações sobre esse código de notificação. Para esse código de notificação, somente **os membros hdr** e **iItem** dessa estrutura são válidos. O **membro iItem** dessa estrutura contém o identificador de comando do botão que está sendo arrastado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado.

## <a name="remarks"></a>Comentários

Esse código de notificação permite que um aplicativo implemente a funcionalidade do tipo "arrastar e soltar" para botões da barra de ferramentas. Ao processar esse código de notificação, o aplicativo iniciará a operação do tipo "arrastar e soltar".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





