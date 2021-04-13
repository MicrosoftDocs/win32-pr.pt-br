---
title: LVN_GETINFOTIP código de notificação (commctrl. h)
description: Enviado por um ícone grande exibir lista-exibir controle que tem o \_ \_ estilo estendido LVS ex INFOTIP.
ms.assetid: 62be5087-7e49-4722-a63a-1768e030af48
keywords:
- LVN_GETINFOTIP de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_GETINFOTIP
- LVN_GETINFOTIPA
- LVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b4552456a575e2f03e02b2bfb78f7fcc1d8ca1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499868"
---
# <a name="lvn_getinfotip-notification-code"></a>Código de notificação do LVN \_ GETINFOTIP

Enviado por um ícone grande exibir lista-exibir controle que tem o estilo estendido [**LVS \_ ex \_ INFOTIP**](extended-list-view-styles.md) . Esse código de notificação é enviado quando o controle de exibição de lista está solicitando informações de texto adicionais a serem exibidas em uma dica de ferramenta. Ele é enviado na forma de uma mensagem [**de \_ notificação do WM**](wm-notify.md) .


```C++
LVN_GETINFOTIP

    pGetInfoTip = (LPNMLVGETINFOTIP) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) que contém informações sobre este código de notificação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno para essa notificação não é usado.

## <a name="remarks"></a>Comentários

Esse código de notificação é enviado somente por controles de exibição de lista que têm o estilo estendido [**LVS \_ ex \_ INFOTIP**](extended-list-view-styles.md) . O \_ código de notificação LVN GETINFOTIP é enviado somente para o subitem 0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **LVN \_ GETINFOTIPW** (Unicode) e **LVN \_ GETINFOTIPA** (ANSI)<br/>             |



 

 





