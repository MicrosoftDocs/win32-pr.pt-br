---
title: BCN_HOTITEMCHANGE código de notificação (commctrl. h)
description: Notifica o proprietário do controle de botão que o mouse está inserindo ou deixando a área cliente do controle botão. O controle de botão envia esse código de notificação na forma de uma \_ mensagem de notificação do WM.
ms.assetid: 92882e21-b69d-4326-94e9-ae69a0d00a83
keywords:
- BCN_HOTITEMCHANGE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- BCN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67ba6a7e64e95b45d0883b5adf34b384bccac8c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009208"
---
# <a name="bcn_hotitemchange-notification-code"></a>Código de notificação do BCN \_ HOTITEMCHANGE

Notifica o proprietário do controle de botão que o mouse está inserindo ou deixando a área cliente do controle botão. O controle de botão envia esse código de notificação na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
BCN_HOTITEMCHANGE

    pnmbchotitem = (NMBCHOTITEM*) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**NMBCHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmbchotitem) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

> [!Note]  
> Para usar esse código de notificação, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





