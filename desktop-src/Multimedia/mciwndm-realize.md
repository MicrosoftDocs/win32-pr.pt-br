---
title: MCIWNDM_REALIZE mensagem (Vfw.h)
description: A mensagem REALIZE MCIWNDM realiza a paleta atualmente usada pelo dispositivo \_ MCI em uma janela MCIWnd. Essa macro é definida com a mensagem REALIZE MCIWNDM. \_ Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndRealize.
ms.assetid: fe8803b5-3500-44b4-97f7-784bedf0b362
keywords:
- MCIWNDM_REALIZE mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- MCIWNDM_REALIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d3fdbee3757e1fd3aada5292b86cc37577ccb718315c5b81140ceb14278c37c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012614"
---
# <a name="mciwndm_realize-message"></a>Mensagem REALIZE MCIWNDM \_

A **mensagem REALIZE \_ MCIWNDM** realiza a paleta atualmente usada pelo dispositivo MCI em uma janela MCIWnd. Essa macro é definida com a **mensagem REALIZE \_ MCIWNDM.** Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndRealize.**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize)


```C++
MCIWNDM_REALIZE 
wParam = (WPARAM) (BOOL) fBkgnd; 
lParam = 0; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="fBkgnd"></span><span id="fbkgnd"></span><span id="FBKGND"></span>*fBkgnd*
</dt> <dd>

Sinalizador de plano de fundo. **Especifique TRUE** para esse parâmetro se a janela for um aplicativo em segundo plano.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="remarks"></a>Comentários

**MCIWNDM \_ REALIZE** usa a paleta do dispositivo MCI e chama a [**função RealizePalette.**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) Se seu aplicativo tratar explicitamente as mensagens [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) e [**WM \_ QUERYNEWPALETTE,**](/windows/desktop/gdi/wm-querynewpalette) você deverá usar essa mensagem em seu aplicativo em vez de usar **RealizePalette**. Se o corpo de um desses manipuladores de mensagens contiver apenas **RealizePalette,** encaminhe a mensagem para a janela MCIWnd, que perceberá automaticamente a paleta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize)
</dt> <dt>

[**Realizepalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged)
</dt> <dt>

[**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette)
</dt> </dl>

 

