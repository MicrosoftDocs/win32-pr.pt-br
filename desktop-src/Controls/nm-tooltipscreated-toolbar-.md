---
title: Código de notificação de NM_TOOLTIPSCREATED (barra de ferramentas) (commctrl. h)
description: Notifica uma janela pai da barra de ferramentas que a barra de ferramentas criou um controle ToolTip. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 0e9517c1-aa3f-4b14-82b4-195a4ce99757
keywords:
- Código de notificação de NM_TOOLTIPSCREATED (barra de ferramentas) controles do Windows
topic_type:
- apiref
api_name:
- NM_TOOLTIPSCREATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c13366348da075fab48e7a2f12381f51f7d87bf4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454928"
---
# <a name="nm_tooltipscreated-toolbar-notification-code"></a>\_Código de notificação nm TOOLTIPSCREATED (barra de ferramentas)

Notifica uma janela pai da barra de ferramentas que a barra de ferramentas criou um controle ToolTip. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
NM_TOOLTIPSCREATED

    lpnmttc = (LPNMTOOLTIPSCREATED) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMTOOLTIPSCREATED**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) que contém informações adicionais sobre esta notificação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O controle Toolbar ignora o valor de retorno deste código de notificação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





