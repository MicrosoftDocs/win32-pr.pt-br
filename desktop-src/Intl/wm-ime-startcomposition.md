---
description: Enviado imediatamente antes de o IME gerar a cadeia de caracteres de composição como resultado de um pressionamento de tecla. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: 2740d009-8685-4f70-9b01-67b71f4ddcbd
title: Mensagem de WM_IME_STARTCOMPOSITION (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7bd9a93b4c6c2e8dba6658c84b5f431dd9a54e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827153"
---
# <a name="wm_ime_startcomposition-message"></a>\_Mensagem de STARTCOMPOSITION IME do WM \_

Enviado imediatamente antes de o IME gerar a cadeia de caracteres de composição como resultado de um pressionamento de tecla. Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,                
  WM_IME_STARTCOMPOSITION,  
  WPARAM wParam,            
  LPARAM lParam             
);
```



## <a name="parameters"></a>Parâmetros

Esta mensagem não tem parâmetros.

<dl></dl>

## <a name="return-value"></a>Retornar valor

Esta mensagem não tem nenhum valor de retorno.

## <a name="remarks"></a>Comentários

Essa mensagem é uma notificação para uma janela do IME para abrir sua janela de composição. Um aplicativo deve processar essa mensagem se exibir os próprios caracteres de composição.

Se um aplicativo tiver criado uma janela IME, ele deverá passar essa mensagem para essa janela. A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) processa a mensagem passando-a para a janela padrão do IME.

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

 

 
