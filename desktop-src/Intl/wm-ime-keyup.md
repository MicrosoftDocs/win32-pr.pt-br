---
description: Enviado a um aplicativo pelo IME para notificar o aplicativo de uma versão de chave e manter a ordem das mensagens. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: 652f951f-4e9f-407c-844c-b250b6a9e6f5
title: Mensagem de WM_IME_KEYUP (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e0eb6c6701510a373573ff6d85d5b50a8541b4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813081"
---
# <a name="wm_ime_keyup-message"></a>\_Mensagem KEYUP IME do WM \_

Enviado a um aplicativo pelo IME para notificar o aplicativo de uma versão de chave e manter a ordem das mensagens. Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_KEYUP,    
  WPARAM wParam,   
  LPARAM lParam    
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* 
</dt> <dd>

Um identificador para a janela.

</dd> <dt>

*wParam* 
</dt> <dd>

Código de chave virtual da chave.

</dd> <dt>

*lParam* 
</dt> <dd>

Contagem de repetição, código de verificação, sinalizador de chave estendida, código de contexto, sinalizador de estado de chave anterior e sinalizador de estado de transição, conforme mostrado abaixo.



| bit   | Significado                                                                     |
|-------|-----------------------------------------------------------------------------|
| 0-15  | Contagem de repetições. Esse valor é sempre 1.                                       |
| 16-23 | Código de verificação.                                                                  |
| 24    | Chave estendida. Esse valor será 1 se for uma chave estendida. Caso contrário, é 0. |
| 25-28 | Não usado.                                                                   |
| 29    | Código de contexto. Esse valor é sempre 0.                                       |
| 30    | Estado de chave anterior. Esse valor é sempre 1.                                 |
| 31    | Estado de transição. Esse valor é sempre 1.                                   |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um aplicativo deve retornar 0 se processar essa mensagem.

## <a name="remarks"></a>Comentários

Um aplicativo pode processar essa mensagem ou passá-la para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  para gerar uma mensagem do [**WM \_ KEYUP**](../inputdev/wm-keyup.md) correspondente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Mensagens do Gerenciador de métodos de entrada](input-method-manager-messages.md)
</dt> </dl>

 

 
