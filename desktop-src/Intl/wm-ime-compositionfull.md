---
description: Enviado a um aplicativo quando a janela do IME não encontra espaço para estender a área para a janela de composição. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: d81d6438-c470-4ae5-8016-8d816bcba9b8
title: Mensagem de WM_IME_COMPOSITIONFULL (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 954a5f91283ca5c4944c274d422508ef0b91b55b8acc34f790cf446f93a598ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811486"
---
# <a name="wm_ime_compositionfull-message"></a>\_Mensagem de COMPOSITIONFULL IME do WM \_

Enviado a um aplicativo quando a janela do IME não encontra espaço para estender a área para a janela de composição. Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,
  WM_IME_COMPOSITIONFULL, 
  WPARAM wParam,
  LPARAM lParam             
);
```



## <a name="parameters"></a>Parâmetros

Esta mensagem não tem parâmetros.

<dl></dl>

## <a name="return-value"></a>Valor retornado

Esta mensagem não tem nenhum valor de retorno.

## <a name="remarks"></a>Comentários

O aplicativo deve usar o [comando \_ SETCOMPOSITIONWINDOW do IMC](imc-setcompositionwindow.md) para especificar como a janela deve ser exibida.

A janela do IME, em vez do IME, envia essa mensagem de notificação pela função [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Mensagens do Gerenciador de métodos de entrada](input-method-manager-messages.md)
</dt> <dt>

[SETCOMPOSITIONWINDOW do IMC \_](imc-setcompositionwindow.md)
</dt> </dl>

 

 
