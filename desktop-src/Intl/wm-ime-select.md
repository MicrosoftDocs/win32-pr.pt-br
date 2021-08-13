---
description: Enviado para um aplicativo quando o sistema operacional está prestes a alterar o IME atual. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: 5559b3ab-8d81-4f33-b0af-d05489371328
title: WM_IME_SELECT mensagem (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611ff30bac32fbd38c9aef00e459b49f9760d9702c619f7e6e7f55e6e3b10acb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118644616"
---
# <a name="wm_ime_select-message"></a>Mensagem SELECT \_ do WM IME \_

Enviado para um aplicativo quando o sistema operacional está prestes a alterar o IME atual. Uma janela recebe essa mensagem por meio de [*sua função WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
LRESULT CALLBACK WindowProc(
 HWND  hwnd,       
 WM_IME_SELECT,   
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

Indicador de seleção. Esse parâmetro especifica **TRUE** se o IME indicado estiver selecionado. O parâmetro será definido como **FALSE** se o IME especificado não estiver mais selecionado.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de localidade de entrada associado ao IME.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem não tem nenhum valor de retorno.

## <a name="remarks"></a>Comentários

Um aplicativo que criou uma janela do IME deve passar essa mensagem para essa janela para que ele possa recuperar a alça de layout do teclado para o IME recém-selecionado.

A [**função DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  processa essa mensagem passando as informações para a janela padrão do IME.

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

 

 
