---
description: A mensagem do WM \_ PALETTEISCHANGING informa os aplicativos que um aplicativo vai perceber sua paleta lógica.
ms.assetid: 64ec1042-0ab5-496f-9a88-2f293b412704
title: Mensagem de WM_PALETTEISCHANGING (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b0de17e7957e4b03c0a8fb942e7c0e4f94a3329e53cb039ce1d7f0a8c33aa89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717676"
---
# <a name="wm_paletteischanging-message"></a>Mensagem do WM \_ PALETTEISCHANGING

A mensagem do **WM \_ PALETTEISCHANGING** informa os aplicativos que um aplicativo vai perceber sua paleta lógica.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para a janela que vai perceber sua paleta lógica.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

O aplicativo que altera sua paleta não aguarda a confirmação desta mensagem antes de alterar a paleta e enviar a mensagem [**de \_ paletachanged do WM**](wm-palettechanged.md) . Como resultado, a paleta pode já ser alterada no momento em que um aplicativo recebe essa mensagem.

Se o aplicativo ignorar ou não processar essa mensagem e um segundo aplicativo perceber sua paleta enquanto o primeiro estiver usando índices de paleta, haverá uma grande possibilidade de que o usuário verá cores inesperadas durante operações de desenho subsequentes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral das cores](colors.md)
</dt> <dt>

[Mensagens de cores](color-messages.md)
</dt> <dt>

[**paleta do WMchanged \_**](wm-palettechanged.md)
</dt> <dt>

[**QUERYNEWPALETTE do WM \_**](wm-querynewpalette.md)
</dt> </dl>

 

 
