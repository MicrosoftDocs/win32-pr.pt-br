---
title: RBN_AUTOSIZE código de notificação (commctrl. h)
description: Enviado por um controle rebar criado com o estilo de AUTOSIZE do RBS \_ quando o rebar é redimensionado automaticamente. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: d174fe99-13cc-404c-9dc5-d5a93e9807a2
keywords:
- RBN_AUTOSIZE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- RBN_AUTOSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ecfac5a4f84d69d444c25a24956cb911fd90a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749072"
---
# <a name="rbn_autosize-notification-code"></a>Código de notificação do RBN \_ AUTOSIZE

Enviado por um controle rebar criado com o estilo de [**\_ AUTOSIZE do RBS**](rebar-control-styles.md) quando o rebar é redimensionado automaticamente. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
RBN_AUTOSIZE

    lpnmas = (LPNMRBAUTOSIZE) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMRBAUTOSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize) que contém informações sobre a operação de redimensionamento.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno para essa notificação não é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





