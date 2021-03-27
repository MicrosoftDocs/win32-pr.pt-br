---
description: A mensagem do WM \_ PALETTEISCHANGING informa os aplicativos que um aplicativo vai perceber sua paleta lógica.
ms.assetid: 64ec1042-0ab5-496f-9a88-2f293b412704
title: Mensagem de WM_PALETTEISCHANGING (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa2127dc9c682bba1fc4cea4e10b2b96ecc92102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662614"
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

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

O aplicativo que altera sua paleta não aguarda a confirmação desta mensagem antes de alterar a paleta e enviar a mensagem [**de \_ paletachanged do WM**](wm-palettechanged.md) . Como resultado, a paleta pode já ser alterada no momento em que um aplicativo recebe essa mensagem.

Se o aplicativo ignorar ou não processar essa mensagem e um segundo aplicativo perceber sua paleta enquanto o primeiro estiver usando índices de paleta, haverá uma grande possibilidade de que o usuário verá cores inesperadas durante operações de desenho subsequentes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



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

 

 
