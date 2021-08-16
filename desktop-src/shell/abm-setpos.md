---
description: Define o tamanho e a posição da tela de um AppBar.
ms.assetid: b3c56278-b9a2-4e08-bf98-7b3e4c8bd082
title: Mensagem de ABM_SETPOS (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431bbdc02ed202c94d66b6b93ce43aba0ebd40f1fb7058583f56c027cfc29b70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861598"
---
# <a name="abm_setpos-message"></a>\_Mensagem ABM SETPOS

Define o tamanho e a posição da tela de um AppBar. A mensagem Especifica uma borda de tela e o retângulo delimitador para o AppBar. o sistema pode ajustar o retângulo delimitador para que o appbar não interfira na barra de tarefas Windows ou em qualquer outro appbars.


```C++
SHAppBarMessage(ABM_SETPOS, pabd); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pabd* 
</dt> <dd>

Um ponteiro para uma estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) . O membro **uEdge** especifica uma borda de tela e o membro **RC** contém o retângulo delimitador. Quando a função [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) retorna, **RC** contém o retângulo delimitador aprovado. Você deve especificar os membros **cbSize**, **HWND**, **uEdge** e **RC** ao enviar esta mensagem; todos os outros membros são ignorados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sempre retorna **true**.

## <a name="remarks"></a>Comentários

Essa mensagem faz com que o sistema envie a mensagem de notificação do [**ABN \_ POSCHANGED**](abn-poschanged.md) para todos os appbars.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




