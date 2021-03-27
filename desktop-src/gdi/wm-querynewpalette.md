---
description: A mensagem do WM \_ QUERYNEWPALETTE informa uma janela de que está prestes a receber o foco do teclado, dando à janela a oportunidade de perceber sua paleta lógica quando recebe o foco.
ms.assetid: bc9f76ca-62af-4f0b-8791-49269a1b23d1
title: Mensagem de WM_QUERYNEWPALETTE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ca664bbb6fb30a0508f9429dd62af489c092db7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967851"
---
# <a name="wm_querynewpalette-message"></a>Mensagem do WM \_ QUERYNEWPALETTE

A mensagem do **WM \_ QUERYNEWPALETTE** informa uma janela de que está prestes a receber o foco do teclado, dando à janela a oportunidade de perceber sua paleta lógica quando recebe o foco.

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

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a janela perceber sua paleta lógica, ela deverá retornar **true**; caso contrário, ele deve retornar **false**.

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

[**PALETTEISCHANGING do WM \_**](wm-paletteischanging.md)
</dt> </dl>

 

 
