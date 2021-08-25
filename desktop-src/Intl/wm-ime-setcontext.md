---
description: Enviado para um aplicativo quando uma janela é ativada. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: ba1e7877-1612-4f2f-aced-0dd982352ad6
title: WM_IME_SETCONTEXT mensagem (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5fb3e65b47b5d62b1d37ffaee4dfc5927d76485d0c3e5de02662da64215e43f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829246"
---
# <a name="wm_ime_setcontext-message"></a>Mensagem \_ \_ SETCONTEXT do WM IME

Enviado para um aplicativo quando uma janela é ativada. Uma janela recebe essa mensagem por meio de [*sua função WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

*Hwnd* 
</dt> <dd>

Um alça para janela.

</dd> <dt>

*wParam* 
</dt> <dd>

**TRUE** se a janela estiver ativa e FALSE, **caso** contrário, .

</dd> <dt>

*lParam* 
</dt> <dd>

Opções de exibição. Esse parâmetro pode ter um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                   | Significado                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="ISC_SHOWUICOMPOSITIONWINDOW"></span><span id="isc_showuicompositionwindow"></span><dl> <dt>**ISC \_ SHOWUICOMPOSITIONWINDOW**</dt> </dl> | Mostrar a janela de composição por janela de interface do usuário.<br/>          |
| <span id="ISC_SHOWUIGUIDWINDOW"></span><span id="isc_showuiguidwindow"></span><dl> <dt>**ISC \_ SHOWUIGUIDWINDOW**</dt> </dl>                      | Mostrar a janela do guia por janela da interface do usuário.<br/>                |
| <span id="ISC_SHOWUISOFTKBD"></span><span id="isc_showuisoftkbd"></span><dl> <dt>**ISC \_ SHOWUISOFTKBD**</dt> </dl>                               | Mostrar o teclado suave pela janela da interface do usuário.<br/>               |
| <span id="ISC_SHOWUICANDIDATEWINDOW"></span><span id="isc_showuicandidatewindow"></span><dl> <dt>**ISC \_ SHOWUICANDIDATEWINDOW**</dt> </dl>       | Mostrar a janela candidata do índice 0 pela janela da interface do usuário.<br/> |
| <dl> <dt>ISC \_ SHOWUICANDIDATEWINDOW << 1</dt> </dl>                                                                                        | Mostrar a janela candidata do índice 1 pela janela da interface do usuário.<br/> |
| <dl> <dt>ISC \_ SHOWUICANDIDATEWINDOW << 2</dt> </dl>                                                                                        | Mostrar a janela candidata do índice 2 pela janela da interface do usuário.<br/> |
| <dl> <dt>ISC \_ SHOWUICANDIDATEWINDOW << 3</dt> </dl>                                                                                        | Mostrar a janela candidata do índice 3 pela janela da interface do usuário.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o valor retornado por [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ou [**ImmIsUIMessage.**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)

## <a name="remarks"></a>Comentários

Se o aplicativo tiver criado uma janela do IME, ele deverá chamar [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea). Caso contrário, ele deverá passar essa mensagem para [**DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)

Se o aplicativo desenhar a janela de composição, a janela padrão do IME não terá que mostrar sua janela de composição. Nesse caso, o aplicativo deve limpar o valor **\_ SHOWUICOMPOSITIONWINDOW isc** do parâmetro *lParam* antes de passar a mensagem para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) [**ou ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea). Para exibir uma determinada janela de interface do usuário, um aplicativo deve remover o valor correspondente para que o IME não o exibirá.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h);</dt> <dt>Imm.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de Métodos de Entrada](input-method-manager.md)
</dt> <dt>

[Mensagens do Gerenciador de Métodos de Entrada](input-method-manager-messages.md)
</dt> <dt>

[**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> </dl>

 

 
