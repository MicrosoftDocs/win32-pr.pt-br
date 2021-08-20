---
description: Registra uma nova barra de aplicativos e especifica o identificador de mensagem que o sistema deve usar para enviar mensagens de notificação. Uma barra de aplicativos deve enviar essa mensagem antes de enviar outras mensagens da barra de aplicativos.
ms.assetid: 1da9db13-6fdc-44b3-9985-de32d572675a
title: ABM_NEW mensagem (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 400439e6808d40eb74c18fa4219109a0abca1973cdac4dcb9de5154384fd0071
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460963"
---
# <a name="abm_new-message"></a>Mensagem ABM \_ NEW

Registra uma nova barra de aplicativos e especifica o identificador de mensagem que o sistema deve usar para enviar mensagens de notificação. Uma barra de aplicativos deve enviar essa mensagem antes de enviar outras mensagens da barra de aplicativos.


```C++
fRegistered = (BOOL) SHAppBarMessage(ABM_NEW, pabd); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pabd* 
</dt> <dd>

Um ponteiro para uma [**estrutura APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) que contém o identificador de janela e o identificador de mensagem da nova barra de aplicativos. Você deve especificar os **membros cbSize**, **hWnd** e **uCallbackMessage** ao enviar essa mensagem; todos os outros membros são ignorados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se for bem-sucedido ou **FALSE** se ocorrer um erro ou se a barra de aplicativos já estiver registrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




