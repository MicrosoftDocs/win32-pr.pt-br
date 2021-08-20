---
title: HDN_BEGINDRAG código de notificação (commctrl. h)
description: Enviado por um controle de cabeçalho quando uma operação de arrastar começou em um de seus itens. Este código de notificação é enviado somente por controles de cabeçalho que são definidos para o estilo de DRAGDROP da HDS \_ . Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 3dfb7a7c-d783-48e0-ba92-8144104f163a
keywords:
- HDN_BEGINDRAG código de notificação Windows controles
topic_type:
- apiref
api_name:
- HDN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ae1ab3f8ac24b5521fab1afc5313503867e575906e851acf4d4fdbe90fe787d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544686"
---
# <a name="hdn_begindrag-notification-code"></a>Código de notificação do HDN \_ BEGINDRAG

Enviado por um controle de cabeçalho quando uma operação de arrastar começou em um de seus itens. Este código de notificação é enviado somente por controles de cabeçalho que são definidos para o estilo de [**\_ DRAGDROP da HDS**](header-control-styles.md) . Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
HDN_BEGINDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contém informações sobre o item de cabeçalho que está sendo arrastado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para permitir que o controle de cabeçalho gerencie automaticamente as operações de arrastar e soltar, retorne **false**. Se o proprietário do controle estiver executando manualmente a reordenação do tipo "arrastar e soltar", retorne **verdadeiro**.

## <a name="remarks"></a>Comentários

Um controle de cabeçalho usa como padrão o gerenciamento automático da reordenação do tipo "arrastar e soltar". Retornando **true** para indicar que o gerenciamento de arrastar e soltar externo (manual) permite que o proprietário do controle forneça serviços personalizados como parte do processo de arrastar e soltar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





