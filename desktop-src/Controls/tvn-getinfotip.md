---
title: TVN_GETINFOTIP código de notificação (commctrl. h)
description: Enviado por um controle de exibição de árvore que tem o \_ estilo INFOTIP de TVs. Esse código de notificação é enviado quando o controle está solicitando informações de texto adicionais a serem exibidas em uma dica de ferramenta. O código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 20576710-e279-4e61-be6b-bf1d8ea79555
keywords:
- TVN_GETINFOTIP de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TVN_GETINFOTIP
- TVN_GETINFOTIPA
- TVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1336571fa2c06e8b22078b1d761d9841217104e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644838"
---
# <a name="tvn_getinfotip-notification-code"></a>Código de notificação do TVN \_ GETINFOTIP

Enviado por um controle de exibição de árvore que tem o estilo [**\_ INFOTIP de TVs**](tree-view-control-window-styles.md) . Esse código de notificação é enviado quando o controle está solicitando informações de texto adicionais a serem exibidas em uma dica de ferramenta. O código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TVN_GETINFOTIP

    lpGetInfoTip = (LPNMTVGETINFOTIP)lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMTVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtvgetinfotipa) que contém informações sobre este código de notificação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O controle ignora o valor de retorno para este código de notificação.

## <a name="remarks"></a>Comentários

Este código de notificação é enviado somente por controles de exibição de árvore que têm o estilo de [**\_ INFOTIP de TVs**](tree-view-control-window-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TVN \_ GETINFOTIPW** (Unicode) e **TVN \_ GETINFOTIPA** (ANSI)<br/>             |



 

 





