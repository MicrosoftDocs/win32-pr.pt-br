---
title: HDN_ITEMDBLCLICK código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de cabeçalho que o usuário clicou duas vezes no controle. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ . Somente os controles de cabeçalho que são definidos para o \_ estilo de botões HDS enviam este código de notificação.
ms.assetid: 72bb00b9-226f-4409-b788-b623868f78b6
keywords:
- HDN_ITEMDBLCLICK de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- HDN_ITEMDBLCLICK
- HDN_ITEMDBLCLICKA
- HDN_ITEMDBLCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e61117303ecc478a998da8799867988dbc1ca08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163618"
---
# <a name="hdn_itemdblclick-notification-code"></a>Código de notificação do HDN \_ ITEMDBLCLICK

Notifica uma janela pai do controle de cabeçalho que o usuário clicou duas vezes no controle. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . Somente os controles de cabeçalho que são definidos para o estilo de [**\_ botões HDS**](header-control-styles.md) enviam este código de notificação.


```C++
HDN_ITEMDBLCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contém informações sobre este código de notificação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **HDN \_ ITEMDBLCLICKW** (Unicode) e **HDN \_ ITEMDBLCLICKA** (ANSI)<br/>         |



 

 





