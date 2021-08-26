---
title: TVN_KEYDOWN de notificação (Commctrl.h)
description: Notifica a janela pai de um controle de exibição de árvore de que o usuário pressionou uma tecla e o controle de exibição de árvore tem o foco de entrada. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: da0d2b62-2295-4dce-9b37-a250f3be087f
keywords:
- TVN_KEYDOWN código de notificação Windows Controles
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
ms.openlocfilehash: dadd3386e83e541288249b83028119111a42855a111f7ecb398571a1d46ab356
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002466"
---
# <a name="tvn_keydown-notification-code"></a>Código de \_ notificação TVN KEYDOWN

Notifica a janela pai de um controle de exibição de árvore de que o usuário pressionou uma tecla e o controle de exibição de árvore tem o foco de entrada. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_KEYDOWN 

    ptvkd = (LPNMTVKEYDOWN) lParam 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMTVKEYDOWN.**](/windows/win32/api/commctrl/ns-commctrl-nmtvkeydown) O **membro wVKey** especifica o código de chave virtual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o **membro wVKey** de *lParam* for um código de chave de caractere, o caractere será usado como parte de uma pesquisa incremental. Retorne diferente de zero para excluir o caractere da pesquisa incremental ou zero para incluir o caractere na pesquisa. Para todas as outras chaves, o valor de retorno é ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





