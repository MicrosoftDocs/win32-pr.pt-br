---
description: A mensagem do WM \_ DEVMODECHANGE é enviada para todas as janelas de nível superior sempre que o usuário altera as configurações do modo de dispositivo.
ms.assetid: 06b625a8-7584-4a98-b8e7-f1de668c274e
title: Mensagem de WM_DEVMODECHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 068e74264a7492bbb1e685fe6de110e909698374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968085"
---
# <a name="wm_devmodechange-message"></a>Mensagem do WM \_ DEVMODECHANGE

A mensagem do **WM \_ DEVMODECHANGE** é enviada para todas as janelas de nível superior sempre que o usuário altera as configurações do modo de dispositivo.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* 
</dt> <dd>

Um identificador para uma janela.

</dd> <dt>

*uMsg* 
</dt> <dd>

DEVMODECHANGE do WM \_

</dd> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma cadeia de caracteres que especifica o nome do dispositivo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um aplicativo deve retornar zero se ele processar essa mensagem.

## <a name="remarks"></a>Comentários

Esta mensagem não pode ser enviada diretamente a uma janela. Para enviar a mensagem do **WM \_ DEVMODECHANGE** para todas as janelas de nível superior, use a função [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) com o parâmetro *HWND* definido como a \_ difusão HWND.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral de contextos de dispositivo](device-contexts.md)
</dt> <dt>

[Mensagens de contexto do dispositivo](device-context-messages.md)
</dt> </dl>

 

 
