---
description: Enviado a um aplicativo quando uma janela é ativada. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: ba1e7877-1612-4f2f-aced-0dd982352ad6
title: Mensagem de WM_IME_SETCONTEXT (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b36cb1e80127d1a451dabcc457dc364a27878ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164512"
---
# <a name="wm_ime_setcontext-message"></a>\_Mensagem de contexto IME do WM \_

Enviado a um aplicativo quando uma janela é ativada. Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,  
  WM_IME_SETCONTEXT,  
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

**True** se a janela estiver ativa e **false** caso contrário.

</dd> <dt>

*lParam* 
</dt> <dd>

Opções de exibição. Esse parâmetro pode ter um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                   | Significado                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="ISC_SHOWUICOMPOSITIONWINDOW"></span><span id="isc_showuicompositionwindow"></span><dl> <dt>**SHOWUICOMPOSITIONWINDOW da ISC \_**</dt> </dl> | Mostrar a janela de composição por janela de interface do usuário.<br/>          |
| <span id="ISC_SHOWUIGUIDWINDOW"></span><span id="isc_showuiguidwindow"></span><dl> <dt>**SHOWUIGUIDWINDOW da ISC \_**</dt> </dl>                      | Mostrar a janela de guia por janela de interface do usuário.<br/>                |
| <span id="ISC_SHOWUISOFTKBD"></span><span id="isc_showuisoftkbd"></span><dl> <dt>**SHOWUISOFTKBD da ISC \_**</dt> </dl>                               | Mostrar o teclado virtual por janela de interface do usuário.<br/>               |
| <span id="ISC_SHOWUICANDIDATEWINDOW"></span><span id="isc_showuicandidatewindow"></span><dl> <dt>**SHOWUICANDIDATEWINDOW da ISC \_**</dt> </dl>       | Mostrar a janela candidata da janela do índice 0 por interface do usuário.<br/> |
| <dl> <dt>ISC \_ SHOWUICANDIDATEWINDOW << 1</dt> </dl>                                                                                        | Mostrar a janela candidata do índice 1 pela janela da interface do usuário.<br/> |
| <dl> <dt>ISC \_ SHOWUICANDIDATEWINDOW << 2</dt> </dl>                                                                                        | Mostrar a janela de candidato do índice 2 pela janela de interface do usuário.<br/> |
| <dl> <dt>ISC \_ SHOWUICANDIDATEWINDOW << 3</dt> </dl>                                                                                        | Mostrar a janela candidata do índice 3 pela janela da interface do usuário.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o valor retornado por [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ou [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).

## <a name="remarks"></a>Comentários

Se o aplicativo tiver criado uma janela IME, ele deverá chamar [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea). Caso contrário, ele deve passar essa mensagem para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

Se o aplicativo desenhar a janela de composição, a janela padrão do IME não precisará mostrar sua janela de composição. Nesse caso, o aplicativo deve limpar o valor **de \_ SHOWUICOMPOSITIONWINDOW do ISC** do *parâmetro lParam* antes de passar a mensagem para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ou [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea). Para exibir uma determinada janela de interface do usuário, um aplicativo deve remover o valor correspondente para que o IME não o exiba.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                                                      |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h); </dt> <dt>IMM. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Mensagens do Gerenciador de métodos de entrada](input-method-manager-messages.md)
</dt> <dt>

[**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> </dl>

 

 
