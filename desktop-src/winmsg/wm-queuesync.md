---
description: Enviado por um aplicativo de treinamento baseado em computador (CBT) para separar mensagens de entrada de usuário de outras mensagens enviadas por meio do \_ procedimento JOURNALPLAYBACK do qu.
ms.assetid: 9ac265be-1fcc-476f-9dee-3e961340b5a1
title: Mensagem de WM_QUEUESYNC (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d859f858ab7cf8182282cc20dbf514cfc2d9b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751530"
---
# <a name="wm_queuesync-message"></a>Mensagem do WM \_ QUEUESYNC

Enviado por um aplicativo de treinamento baseado em computador (CBT) para separar mensagens de entrada de usuário de outras mensagens enviadas por meio do procedimento [**\_ JOURNALPLAYBACK do qu**](about-hooks.md) .


```C++
#define WM_QUEUESYNC                    0x0023
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **void**

Um aplicativo CBT deve retornar zero se ele processar essa mensagem.

## <a name="remarks"></a>Comentários

Sempre que um aplicativo CBT usa o procedimento [**qu \_ JOURNALPLAYBACK**](about-hooks.md) , a primeira e a última mensagem são o **WM \_ QUEUESYNC**. Isso permite que o aplicativo CBT intercepte e examine as mensagens iniciadas pelo usuário sem fazer isso para os eventos que ele envia.

Se um aplicativo especificar um identificador de janela **nulo** , a mensagem será postada na fila de mensagens da janela ativa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))
</dt> <dt>

[**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Ganchos](hooks.md)
</dt> </dl>

 

 
