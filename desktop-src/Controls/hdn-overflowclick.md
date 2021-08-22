---
title: HDN_OVERFLOWCLICK código de notificação (commctrl. h)
description: Enviado por um controle de cabeçalho para seu pai quando o botão de estouro do cabeçalho é clicado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 770ae00a-b87f-4de2-b869-2a233f2c493e
keywords:
- HDN_OVERFLOWCLICK código de notificação Windows controles
topic_type:
- apiref
api_name:
- HDN_OVERFLOWCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61cee31369bfa1574ba4690f952bc60fb0dde1e5a9bf2f41e98b659356a79625
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576216"
---
# <a name="hdn_overflowclick-notification-code"></a>Código de notificação do HDN \_ OVERFLOWCLICK

Enviado por um controle de cabeçalho para seu pai quando o botão de estouro do cabeçalho é clicado. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
HDN_OVERFLOWCLICK

    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que descreve o código de notificação. O processo de chamada é responsável por alocar essa estrutura, incluindo a estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contida. Defina os membros da estrutura **NMHDR** , incluindo o membro do *código* que deve ser definido como HDN \_ OVERFLOWCLICK.

Defina o membro **iItem** da estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) para o índice do primeiro item de cabeçalho que não está visível e, portanto, deve ser exibido em um estouro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

O receptor de notificação converte **lParam** para recuperar a estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) . **WParam** contém a ID do controle que envia a notificação.

Esta mensagem é enviada somente quando o estilo de [**\_ estouro HDS**](header-control-styles.md) é definido no controle de cabeçalho.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





