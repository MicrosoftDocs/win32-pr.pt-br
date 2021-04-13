---
title: HDN_ENDDRAG código de notificação (commctrl. h)
description: Enviado por um controle de cabeçalho quando uma operação de arrastar termina em um de seus itens. Esse código de notificação é enviado como uma \_ mensagem de notificação do WM. Somente controles de cabeçalho que são definidos para o \_ estilo HDS DRAGDROP enviam este código de notificação.
ms.assetid: a28df985-73f1-4fc7-a1db-81a86a131c06
keywords:
- HDN_ENDDRAG de código de notificação controles do Windows
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
ms.openlocfilehash: 8eef628dd8ff748829542ace76642e20ad97786f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456057"
---
# <a name="hdn_enddrag-notification-code"></a>Código de notificação do HDN \_ ENDarraste

Enviado por um controle de cabeçalho quando uma operação de arrastar termina em um de seus itens. Esse código de notificação é enviado como uma mensagem de [**\_ notificação do WM**](wm-notify.md) . Somente controles de cabeçalho que são definidos para o estilo [**HDS \_ DRAGDROP**](header-control-styles.md) enviam este código de notificação.


```C++
HDN_ENDDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contém informações sobre o item de cabeçalho que estava sendo arrastado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para permitir que o controle Coloque e reordene automaticamente o item, retorne **false**. Para impedir que o item seja colocado, retorne **true**.

## <a name="remarks"></a>Comentários

Se o proprietário estiver executando o gerenciamento de arrastar e soltar externo (manual), ele deverá retornar **false**. Em seguida, o proprietário deve reordenar os itens de cabeçalho manualmente enviando [**HDM \_ SETITEM**](hdm-setitem.md) ou [**HDM \_ SETORDERARRAY**](hdm-setorderarray.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





