---
description: Enviado a um aplicativo quando o sistema operacional está prestes a alterar o IME atual. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: 5559b3ab-8d81-4f33-b0af-d05489371328
title: Mensagem de WM_IME_SELECT (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 940858e12c616b1d6281c23633b2f0f5e9657a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758133"
---
# <a name="wm_ime_select-message"></a>\_Selecionar mensagem do IME do WM \_

Enviado a um aplicativo quando o sistema operacional está prestes a alterar o IME atual. Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


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

*HWND* 
</dt> <dd>

Um identificador para a janela.

</dd> <dt>

*wParam* 
</dt> <dd>

Indicador de seleção. Esse parâmetro especifica **true** se o IME indicado for selecionado. O parâmetro será definido como **false** se o IME especificado não estiver mais selecionado.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de localidade de entrada associado ao IME.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esta mensagem não tem nenhum valor de retorno.

## <a name="remarks"></a>Comentários

Um aplicativo que criou uma janela IME deve passar essa mensagem para essa janela para que ela possa recuperar o identificador de layout do teclado para o IME selecionado recentemente.

A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  processa essa mensagem passando as informações para a janela padrão do IME.

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

 

 
