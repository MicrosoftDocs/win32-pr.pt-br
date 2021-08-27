---
description: Enviado para um aplicativo pelo IME para notificar o aplicativo de uma versão de chave e para manter a ordem da mensagem. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: 652f951f-4e9f-407c-844c-b250b6a9e6f5
title: WM_IME_KEYUP mensagem (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f65d80876643cc27136223c112c1e045bc797adbd0bf160adda1c3cea894767e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102066"
---
# <a name="wm_ime_keyup-message"></a>Mensagem WM \_ IME \_ KEYUP

Enviado para um aplicativo pelo IME para notificar o aplicativo de uma versão de chave e para manter a ordem da mensagem. Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

*Hwnd* 
</dt> <dd>

Um alça para janela.

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
| 0-15  | Contagem de repetição. Esse valor é sempre 1.                                       |
| 16-23 | Digitalizar código.                                                                  |
| 24    | Chave estendida. Esse valor será 1 se for uma chave estendida. Caso contrário, é 0. |
| 25-28 | Não usado.                                                                   |
| 29    | Código de contexto. Esse valor é sempre 0.                                       |
| 30    | Estado da chave anterior. Esse valor é sempre 1.                                 |
| 31    | Estado de transição. Esse valor é sempre 1.                                   |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um aplicativo deverá retornar 0 se ele processa essa mensagem.

## <a name="remarks"></a>Comentários

Um aplicativo pode processar essa mensagem ou passá-la para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  para gerar uma mensagem [**WM \_ KEYUP**](../inputdev/wm-keyup.md) correspondente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de Métodos de Entrada](input-method-manager.md)
</dt> <dt>

[Mensagens do Gerenciador de Métodos de Entrada](input-method-manager-messages.md)
</dt> </dl>

 

 
