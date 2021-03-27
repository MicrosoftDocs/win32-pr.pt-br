---
description: Registra um novo AppBar e especifica o identificador da mensagem que o sistema deve usar para enviar mensagens de notificação. Um AppBar deve enviar essa mensagem antes de enviar qualquer outra mensagem AppBar.
ms.assetid: 1da9db13-6fdc-44b3-9985-de32d572675a
title: Mensagem de ABM_NEW (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fad11e6712d0afd0c1a5e9de07fd3d690800db13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646852"
---
# <a name="abm_new-message"></a>ABM \_ nova mensagem

Registra um novo AppBar e especifica o identificador da mensagem que o sistema deve usar para enviar mensagens de notificação. Um AppBar deve enviar essa mensagem antes de enviar qualquer outra mensagem AppBar.


```C++
fRegistered = (BOOL) SHAppBarMessage(ABM_NEW, pabd); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pabd* 
</dt> <dd>

Um ponteiro para uma estrutura de [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) que contém o identificador de janela e a identificação de mensagem do novo AppBar. Você deve especificar os membros **cbSize**, **HWND** e **uCallbackMessage** ao enviar esta mensagem; todos os outros membros são ignorados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se for bem-sucedido ou **false** se ocorrer um erro ou se o AppBar já estiver registrado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




