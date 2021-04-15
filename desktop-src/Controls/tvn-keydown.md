---
title: TVN_KEYDOWN código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de árvore que o usuário pressionou uma tecla e o controle de exibição de árvore tem o foco de entrada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: da0d2b62-2295-4dce-9b37-a250f3be087f
keywords:
- TVN_KEYDOWN de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TVN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ccb18c3bf7dc03056abb55575850821e11eb9bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454615"
---
# <a name="tvn_keydown-notification-code"></a>Código de notificação do TVN \_ KEYDOWN

Notifica uma janela pai do controle de exibição de árvore que o usuário pressionou uma tecla e o controle de exibição de árvore tem o foco de entrada. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TVN_KEYDOWN 

    ptvkd = (LPNMTVKEYDOWN) lParam 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMTVKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtvkeydown) . O membro **wVKey** especifica o código de chave virtual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o membro **wVKey** de *lParam* for um código de chave de caractere, o caractere será usado como parte de uma pesquisa incremental. Retorne diferente de zero para excluir o caractere da pesquisa incremental ou zero para incluir o caractere na pesquisa. Para todas as outras chaves, o valor de retorno é ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





