---
description: Define o tamanho e a posição da tela de uma barra de aplicativos.
ms.assetid: b3c56278-b9a2-4e08-bf98-7b3e4c8bd082
title: ABM_SETPOS mensagem (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431bbdc02ed202c94d66b6b93ce43aba0ebd40f1fb7058583f56c027cfc29b70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861598"
---
# <a name="abm_setpos-message"></a>Mensagem ABM \_ SETPOS

Define o tamanho e a posição da tela de uma barra de aplicativos. A mensagem especifica uma borda da tela e o retângulo delimitar para a barra de aplicativos. O sistema pode ajustar o retângulo delimitativo para que a barra de aplicativos não interfira na barra de tarefas Windows ou em nenhuma outra barra de aplicativos.


```C++
SHAppBarMessage(ABM_SETPOS, pabd); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pabd* 
</dt> <dd>

Um ponteiro para uma [**estrutura APPBARDATA.**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) O **membro uEdge** especifica uma borda de tela e o membro **rc** contém o retângulo delimitador. Quando a [**função SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) retorna, **rc** contém o retângulo delimitado aprovado. Você deve especificar os **membros cbSize**, **hWnd,** **uEdge** e **rc** ao enviar essa mensagem; todos os outros membros são ignorados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sempre retorna **TRUE.**

## <a name="remarks"></a>Comentários

Essa mensagem faz com que o sistema envie a mensagem de notificação [**\_ POSCHANGED**](abn-poschanged.md) do ABN para todas as barras de aplicativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




