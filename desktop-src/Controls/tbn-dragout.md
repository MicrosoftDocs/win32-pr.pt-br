---
title: TBN_DRAGOUT código de notificação (commctrl. h)
description: Enviado por um controle Toolbar quando o usuário clica em um botão e, em seguida, move o cursor para fora do botão. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 3566ad60-9744-494f-bb02-d30b41d06351
keywords:
- TBN_DRAGOUT de código de notificação controles do Windows
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
ms.openlocfilehash: 54fa61ef183b56b882c6ecdcb9d0d59edbf13e80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009115"
---
# <a name="tbn_dragout-notification-code"></a>Código de notificação de arrastar e TBN \_

Enviado por um controle Toolbar quando o usuário clica em um botão e, em seguida, move o cursor para fora do botão. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TBN_DRAGOUT

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) que contém informações sobre este código de notificação. Para este código de notificação, somente os membros **HDR** e **iItem** dessa estrutura são válidos. O membro **iItem** dessa estrutura contém o identificador de comando do botão que está sendo arrastado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é ignorado.

## <a name="remarks"></a>Comentários

Esse código de notificação permite que um aplicativo implemente a funcionalidade de arrastar e soltar para botões da barra de ferramentas. Ao processar esse código de notificação, o aplicativo iniciará a operação de arrastar e soltar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





