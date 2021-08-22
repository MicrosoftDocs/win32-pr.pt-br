---
title: HDN_ENDDRAG de notificação (Commctrl.h)
description: Enviado por um controle de header quando uma operação de arrastar termina em um de seus itens. Esse código de notificação é enviado como uma mensagem WM \_ NOTIFY. Somente os controles de cabeça definidos para o estilo \_ HDS DRAGDROP enviam esse código de notificação.
ms.assetid: a28df985-73f1-4fc7-a1db-81a86a131c06
keywords:
- HDN_ENDDRAG de notificação Windows Controles
topic_type:
- apiref
api_name:
- HDN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05df56beb0b5b4a75716723330711714b7db9f4f27100ffe3296626d2be5798a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544607"
---
# <a name="hdn_enddrag-notification-code"></a>Código de \_ notificação DO HDN ENDDRAG

Enviado por um controle de header quando uma operação de arrastar termina em um de seus itens. Esse código de notificação é enviado como uma [**mensagem WM \_ NOTIFY.**](wm-notify.md) Somente os controles de cabeça definidos para o estilo [**\_ HDS DRAGDROP**](header-control-styles.md) enviam esse código de notificação.


```C++
HDN_ENDDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contém informações sobre o item de header que estava sendo arrastado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para permitir que o controle coloque e reordene automaticamente o item, retorne **FALSE.** Para impedir que o item seja colocado, retorne **TRUE.**

## <a name="remarks"></a>Comentários

Se o proprietário estiver executando o gerenciamento de arrastar e soltar externo (manual), ele deverá retornar **FALSE.** Em seguida, o proprietário deve reordenar itens de header manualmente enviando [**HDM \_ SETITEM**](hdm-setitem.md) ou [**HDM \_ SETORDERARRAY**](hdm-setorderarray.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





