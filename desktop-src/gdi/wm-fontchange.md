---
description: Um aplicativo envia a mensagem do WM \_ FONTCHANGE para todas as janelas de nível superior no sistema após a alteração do pool de recursos de fonte.
ms.assetid: 4774308e-2f18-4a35-a769-56871f3c29a2
title: Mensagem de WM_FONTCHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c88edaf2db356fea2b92ce05769360ac9c8664e913ff6e5a05daaf245d1204
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119399926"
---
# <a name="wm_fontchange-message"></a>Mensagem do WM \_ FONTCHANGE

Um aplicativo envia a mensagem do **WM \_ FONTCHANGE** para todas as janelas de nível superior no sistema após a alteração do pool de recursos de fonte.

Para enviar essa mensagem, chame a função [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) com os parâmetros a seguir.


```C++
SendMessage( 
  (HWND)  hWnd,              
  WM_FONTCHANGE,            
  (WPARAM)  wParam,          
  (LPARAM)  lParam            
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Um aplicativo que adiciona ou remove fontes do sistema (por exemplo, usando a função [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) ou [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) ) deve enviar essa mensagem para todas as janelas de nível superior.

Para enviar a mensagem do **WM \_ FONTCHANGE** para todas as janelas de nível superior, um aplicativo pode chamar a função **SendMessage** com o parâmetro *HWND* definido como broadcast de HWND \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral de fontes e texto](fonts-and-text.md)
</dt> <dt>

[Mensagens de fonte e texto](font-and-text-messages.md)
</dt> <dt>

[**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea)
</dt> <dt>

[**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea)
</dt> </dl>

 

 
