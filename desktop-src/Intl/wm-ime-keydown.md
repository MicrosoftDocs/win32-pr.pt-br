---
description: Enviado a um aplicativo pelo IME para notificar o aplicativo de uma tecla pressionada e manter a ordem da mensagem. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: db7075fb-b3d4-4d32-a0db-096d17d67c72
title: WM_IME_KEYDOWN mensagem (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beed8bb074e1bae300d52c52867cc8d1f26b84bb8abf358ad2858df7356a0a0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535306"
---
# <a name="wm_ime_keydown-message"></a>Mensagem WM \_ IME \_ KEYDOWN

Enviado a um aplicativo pelo IME para notificar o aplicativo de uma tecla pressionada e manter a ordem da mensagem. Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,        
  WM_IME_KEYDOWN,  
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

Repita a contagem, o código de verificação, o sinalizador de chave estendido, o código de contexto, o sinalizador de estado de chave anterior e o sinalizador de estado de transição, conforme mostrado na tabela a seguir.



| bit   | Significado                                                                     |
|-------|-----------------------------------------------------------------------------|
| 0-15  | Contagem de repetição.                                                               |
| 16-23 | Digitalizar código.                                                                  |
| 24    | Chave estendida. Esse valor será 1 se for uma chave estendida. Caso contrário, é 0. |
| 25-28 | Não usado.                                                                   |
| 29    | Código de contexto. Esse valor é sempre 0.                                       |
| 30    | Estado da chave anterior. Esse valor será 1 se a chave estiver inobada ou 0 se ela estiver para cima.    |
| 31    | Estado de transição. Esse valor é sempre 0.                                   |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um aplicativo deverá retornar 0 se ele processa essa mensagem.

## <a name="remarks"></a>Comentários

Um aplicativo pode processar essa mensagem ou passá-la para a [**função DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  para gerar uma mensagem [**WM \_ KEYDOWN**](../inputdev/wm-keydown.md) correspondente.

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

 

 
