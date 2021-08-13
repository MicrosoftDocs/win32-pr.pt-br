---
title: Mensagem de HDN_ITEMSTATEICONCLICK (commctrl. h)
description: Notifica uma janela pai do controle de cabeçalho que o usuário clicou no ícone de estado de um item. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: a1969579-3a69-49ff-b06e-4b7450146a92
keywords:
- controles de Windows de mensagem de HDN_ITEMSTATEICONCLICK
topic_type:
- apiref
api_name:
- HDN_ITEMSTATEICONCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cba2e475ec3037ab00c379cf0c9ea371d5a336b80458c68e974a7122d9a2427a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435246"
---
# <a name="hdn_itemstateiconclick-message"></a>\_Mensagem HDN ITEMSTATEICONCLICK

Notifica uma janela pai do controle de cabeçalho que o usuário clicou no ícone de estado de um item. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
HDN_ITEMSTATEICONCLICK

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contém informações adicionais sobre o ícone de estado que foi clicado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





